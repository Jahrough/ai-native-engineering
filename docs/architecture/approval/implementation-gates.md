# Implementation Authorization Gates

No phase below is authorized merely by accepting an ADR. Each gate requires
separate implementation scope approval and controlled test environments.

## Before Phase 1

- ADR-001 through ADR-008 have explicit owner decisions; unresolved decisions
  are either closed or explicitly accepted as non-blocking.
- Named decision, implementation, security, database, operations, and incident
  owners are recorded.
- Recovery authority, Catalog ID/incarnation/version semantics, tombstone and
  privacy policy, event compatibility policy, consumer-group/DLT behavior, and
  replay authorization are approved.
- RPO/RTO and retention values are owner-approved from measured data, or
  recovery claims are explicitly limited until values are established.
- Acceptance tests and failure-injection plan are reviewed; test environment,
  data handling, rollback, and approvals are specified.
- Cross-repository implementation scope is separately authorized.

## Phase gates

| Phase | Gate | Observable pass/fail evidence |
|---|---|---|
| 1. Minimum viable correctness | ADR-001/002/005/006 accepted; compatible event rollout approved | Concurrent updates do not duplicate/regress versions; deletion persists a fence; stale/equal/conflicting events produce the specified result; crash after OpenSearch before inbox and after inbox before offset commit is safe; no claim of end-to-end exactly-once |
| 2. Recovery authority | ADR-004 accepted; authority/audit/access control provisioned and reviewed | Unauthorized/stale epoch changes fail; Catalog PITR cannot lower authority; mismatch blocks Search writes/promotion; partial transition resumes forward; authority restore rollback is detected and requires independent reconciliation |
| 3. Projection rebuild | ADR-003 accepted; continuity, topic identity, snapshot/export, and conditional writes implemented | All snapshot/CDC timeline cases pass; loss of slot/WAL, topic change, expired offsets, interruption, or failed validation aborts; validated new generation alone can be promoted |
| 4. Operational readiness | ADR-007/008 accepted; owners, policies, and alert routes in place | Retention and WAL headroom are measured; alerts are tested; DLT and lag have response procedures; RPO/RTO exercises meet owner-approved targets; no unknown signal is presented as healthy |
| 5. Performance/capacity | Production-like workload and measured targets approved | Benchmarks meet explicitly agreed throughput/latency/capacity criteria; no target is invented by this package |

## Global stop conditions

Stop and preserve current state when authority is unavailable or inconsistent,
CDC continuity cannot be proven, a topic/partition identity changes, required
WAL/offsets have expired, snapshot/export is not repeatable, projection
validation fails, DLT replay authorization is absent, or an alias transition
cannot be fenced. Recovery requires a new approved transition or rebuild; do
not reset offsets or lower epochs to make a run proceed.
