# Cross-Repository Ownership Matrix

This matrix proposes responsibility boundaries; it does not assign named
individuals or transfer existing ownership. Named decision and operational
owners remain open.

| Responsibility | Canonical decision owner | Primary implementation owner | Supporting repository | Operational owner / approval |
|---|---|---|---|---|
| Cross-system ADRs and decision register | Architecture governance owner (TBD) | ai-native-engineering maintains canonical docs only | All repositories provide evidence | Repository owners approve relevant ADRs |
| Aggregate ID, version, outbox, Catalog snapshot export | Catalog domain owner (TBD) | product-catalog | product-search consumes contract | Catalog operations; domain owner approves semantics |
| Event envelope/schema compatibility | Catalog and Search contract owners (TBD) | Producer: product-catalog; validation: product-search | platform-infrastructure for Connect mapping | Both service owners approve compatibility policy |
| Durable deletion/tombstone source state | Catalog domain/privacy owner (TBD) | product-catalog | product-search projection/filter | Catalog operator and privacy/legal approver |
| Kafka, PostgreSQL logical replication, Debezium, managed services | Platform/database owner (TBD) | platform-infrastructure | platform-gitops deploys Kubernetes Connect components | Platform operations; DB/Kafka owner approves recovery |
| Kubernetes desired state, epoch pre-sync, generation orchestration | Platform deployment owner (TBD) | platform-gitops | platform-infrastructure supplies infrastructure outputs | GitOps operator; platform owner approves sync guards |
| Consumer groups, inbox, OpenSearch projection, DLT replay | Search owner (TBD) | product-search | platform-infrastructure provisions managed dependencies | Search on-call; replay approver TBD |
| Search generation validation and alias promotion | Search owner (TBD) | product-search | platform-gitops orchestrates approved controls | Search/recovery operator; two-person approval policy TBD |
| Recovery authority resource and independent audit | Recovery/security owner (TBD) | platform-infrastructure, with GitOps mirror in platform-gitops | Catalog and Search enforce local mirrors | Recovery approver(s) and security owner TBD |
| Metrics, dashboards, alert routing, runbooks | Operations/observability owner (TBD) | Each source repo instruments its component; platform-observability only if staffed | platform-infrastructure currently owns selected CloudWatch signals | Named incident responders TBD |
| Retention, WAL, backup, RPO/RTO | Business/service + database owners (TBD) | platform-infrastructure controls; services define semantic needs | product-catalog, product-search, platform-gitops | Owners approve targets and test evidence |

## Ownership constraints

- Cross-system decisions have one canonical record in ai-native-engineering;
  implementation details remain in their owning repositories.
- Do not duplicate operational policy or configuration across repositories.
- `platform-observability` currently contains only a README. Assigning it as
  primary owner requires an explicit team and implementation scope.
- `platform-infrastructure` owns Terraform/managed infrastructure; GitOps owns
  Kubernetes desired state. Avoid overlapping reconcilers.
- The architecture owner is not automatically the implementation or on-call
  owner. All three roles need explicit assignment.
