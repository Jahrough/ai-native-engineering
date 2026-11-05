# Distributed Product Platform ADRs

These are cross-repository proposals for the Product Catalog -> Debezium ->
Kafka -> Product Search system. They are governance documents, not evidence
that proposed capabilities exist.

## Status and approval

All records in this package are `PROPOSED`. No approval is inferred from this
package, prior discussion, silence, or the previous implementation-readiness
verdict. The designated decision owners must record an explicit approval in the
decision register before an ADR is changed to `ACCEPTED`.

Status vocabulary:

- `PROPOSED`: drafted, not approved
- `ACCEPTED`: explicitly approved by the designated owners
- `REJECTED`: explicitly rejected
- `SUPERSEDED`: replaced by a later accepted decision
- `DEFERRED`: intentionally postponed

## Decision records

| ADR | Title | Status | Primary implementation owners | Depends on |
|---|---|---|---|---|
| [ADR-001](ADR-001-aggregate-identity-and-versioning.md) | Aggregate Identity and Versioning | PROPOSED | product-catalog, product-search | Domain identity and reuse policy |
| [ADR-002](ADR-002-durable-deletion-and-tombstones.md) | Durable Deletion and Tombstones | PROPOSED | product-catalog, product-search | ADR-001 |
| [ADR-003](ADR-003-snapshot-and-cdc-rebuild-protocol.md) | Snapshot and CDC Projection Rebuild Protocol | PROPOSED | product-search, platform-infrastructure, platform-gitops | ADR-001, ADR-002, ADR-004, ADR-005, ADR-006, ADR-007 |
| [ADR-004](ADR-004-recovery-epoch-and-authority.md) | Recovery Epoch and Disaster-Recovery Authority | PROPOSED | platform-infrastructure, platform-gitops, product-catalog, product-search | Recovery authority and approval policy |
| [ADR-005](ADR-005-search-projection-consistency.md) | Search Projection Consistency and Conditional Writes | PROPOSED | product-search | ADR-001, ADR-002, ADR-004 |
| [ADR-006](ADR-006-kafka-consumer-and-dlt-semantics.md) | Kafka Consumer Acknowledgment and DLT Semantics | PROPOSED | product-search, platform-infrastructure | ADR-001, ADR-004, ADR-005, ADR-007 |
| [ADR-007](ADR-007-retention-wal-and-recovery-objectives.md) | Retention, WAL Capacity, and Recovery Objectives | PROPOSED | platform-infrastructure, product-catalog, product-search | Recovery and replay horizons; owner-set RPO/RTO |
| [ADR-008](ADR-008-observability-and-operational-ownership.md) | Distributed-System Observability and Operational Ownership | PROPOSED | all service/platform repositories | Named operational owners and approved signals |

## Evidence baseline

The proposals were grounded in static inspection of these local `main` HEADs
on 2026-11-05. No fetch was performed. The two service branches were behind
their locally recorded upstream tracking refs, so this is not a claim about
the latest remote state.

| Repository | Branch and inspected HEAD | Inspection limitation |
|---|---|---|
| ai-native-engineering | main, `fd63b976a670486289deaa428bed1a44e5508bbc` | Clean |
| product-catalog | main, `63b19ade9356d0a0d759243d2a51c5299dff12ba` | Two commits behind recorded origin/main; dirty worktree preserved |
| product-search | main, `42164291379c8962b336d5b52403541541806e79` | Three commits behind recorded origin/main; dirty worktree preserved; secondary worktrees excluded |
| platform-infrastructure | main, `0d91ef93ab9cdf608c203aeeaeb58094abe88a81` | Dirty worktree preserved |
| platform-gitops | main, `577420e6225c8f315925699ba56bdad87acc26a1` | Dirty worktree preserved |
| platform-observability | main, `de9c90e20c88ae4e639450eb15777d39835bb7c3` | README-only repository |

Evidence labels used in the ADRs:

- **CONFIRMED**: directly visible in the inspected source/configuration.
- **PARTIALLY CONFIRMED**: some source evidence exists but material details are
  unresolved.
- **UNVERIFIED**: requires runtime, dependency-resolution, or operations
  evidence; no such evidence is claimed here.
- **PROPOSED**: a future decision or capability.
- **NOT IMPLEMENTED IN INSPECTED SOURCE**: not found in the cited application
  or configuration paths; this is not proof that no external process exists.

All source references identify the owning repository and a relative path.
They refer to the HEAD listed above unless a later evidence baseline is
explicitly recorded. Tests, builds, failure injection, databases, cloud
resources, and production behavior were not exercised for this package.

## Approval workflow

1. Assign decision and operational owners in the [decision register](../approval/decision-register.md).
2. Resolve blocking questions and dependencies; see the [unresolved questions](../approval/unresolved-questions.md) and [implementation gates](../approval/implementation-gates.md).
3. Review cross-document consistency and repository boundaries in the [ownership matrix](../approval/repository-ownership.md) and [dependency map](../approval/implementation-dependency-map.md).
4. Record explicit approval and approver identity/date for each ADR before changing its status.
5. Authorize implementation separately. Accepted ADRs alone do not authorize code, infrastructure, deployment, or operational changes.
