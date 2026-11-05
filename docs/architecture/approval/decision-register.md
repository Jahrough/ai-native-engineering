# Architecture Decision Register

All entries are proposals. Approval status remains **PENDING** until named
decision owners record an explicit decision. See the [ADR index](../adr/README.md).

| Decision ID | Decision statement / recommended direction | Alternatives | Accountable owner | Required approvers | Blocking ADRs | Status | Outstanding question |
|---|---|---|---|---|---|---|---|
| D-001 | Use positive 64-bit monotonic versions; do not reuse aggregate IDs, or define explicit incarnation. | 32-bit; timestamps; reuse/reset; incarnation | Catalog domain owner (TBD) | Catalog, Search, architecture | ADR-001 | PENDING | Is same-ID recreation required? |
| D-002 | Persist minimal versioned tombstones and filter them from all Search results. | Physical delete; full retained row; minimal tombstone | Catalog domain + privacy owner (TBD) | Catalog, Search, privacy/legal | ADR-002 | PENDING | What may be retained and for how long? |
| D-003 | Rebuild into isolated generation from explicit Kafka offset vector plus repeatable-read Catalog snapshot, under conditional writes. | Quiesced rebuild; full replay; snapshot-only | Search/platform architecture owner (TBD) | Catalog, Search, database, Kafka | ADR-003 | PENDING | What proves connector/topic continuity? |
| D-004 | Use protected external monotonic recovery authority; GitOps is a mirror, not authority. | GitOps-only; external record; recovery service | Platform recovery owner (TBD) | Platform, Security, Catalog, Search | ADR-004 | PENDING | Which record and independent audit source? |
| D-005 | Use strict external versions and identity/fingerprint comparison; use tombstone documents. | Inbox-only; read-then-write; external_gte; physical delete | Search owner (TBD) | Search, Catalog, platform | ADR-005 | PENDING | Verify server/client semantics and fingerprint format. |
| D-006 | Define at-least-once processing, explicit commit behavior, and operator-controlled audited DLT replay. | Auto-commit; transactions; automatic replay | Search/Kafka owner (TBD) | Search, platform, operations | ADR-006 | PENDING | Which listener groups are required? |
| D-007 | Set retention, WAL thresholds, and RPO/RTO only from measurements and owner decisions. | Indefinite; fixed defaults; measured horizons | Service/business + DB owners (TBD) | Product, platform, security | ADR-007 | PENDING | What recovery horizons are required? |
| D-008 | Assign telemetry to source owners and define a shared operational backend only when approved. | Logs only; immediate centralized stack; staged shared backend | Operations/observability owner (TBD) | All service/platform owners | ADR-008 | PENDING | Who owns `platform-observability` and alerts? |
| D-009 | Canonical cross-system ADRs live in ai-native-engineering; owner repos link rather than duplicate. | Per-repo duplicates; central project repo; no ADRs | Architecture governance owner (TBD) | All repository owners | All | PENDING | Who maintains canonical records and approvals? |
| D-010 | Keep an epoch monotonic across Catalog PITR and fail closed on missing/mismatched authority. | Roll back with Catalog; infer from Git; external record | Recovery owner (TBD) | Security, platform, Catalog, Search | ADR-004 | PENDING | What is the break-glass quorum? |
| D-011 | Treat schema compatibility as an explicit coordinated rollout policy with CI contract gates. | Strict coordinated deploy; backward-compatible evolution; Schema Registry | Catalog/Search owners (TBD) | Service owners | ADR-001, ADR-006 | PENDING | Which producer/consumer skew must be supported? |
| D-012 | Establish named implementation, operational, and approval owners per repository. | Shared/unassigned ownership; single central team | Engineering leadership (TBD) | All repository owners | ADR-008 | PENDING | Who is accountable for incidents and changes? |

## Approval record

Record decision ID, outcome, approver(s), date, rationale, and any conditions.
An ADR status changes only after the required owners have approved it.
