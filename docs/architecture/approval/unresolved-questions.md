# Unresolved Questions and Assumptions

These questions cannot be settled by static source inspection. **Blocking**
means implementation or a recovery guarantee must wait for an answer.

| ID | Question / assumption | Why it matters | Required owner/evidence | Blocks |
|---|---|---|---|---|
| Q-01 | Can a product ID or SKU be reused after deletion, import, or PITR, and how will a non-repeating ID allocation survive sequence rollback? | Determines whether monotonic version alone identifies an aggregate lifecycle; a database identity sequence may also rewind under PITR. | Catalog domain owner; business identity rules, import paths, and allocation strategy | ADR-001, ADR-004, Phase 1 |
| Q-02 | Which deleted-product fields must be erased, and which tombstone metadata may remain? | Privacy/legal constraints set tombstone contents and purge conditions. | Privacy/legal and Catalog owner; data classification/retention obligations | ADR-002 |
| Q-03 | What maximum historical replay and restore horizon is supported? | Determines inbox, tombstone, Kafka, DLT, and backup retention. | Business/service/operations owners; recovery requirements | ADR-002/007 |
| Q-04 | What protected record can provide conditional monotonic epoch advance and independent audit? | GitOps and Catalog snapshots can roll back; a restored authority backup may also be stale. | Platform/security owner; control-plane capabilities, backup and audit evidence | ADR-004 |
| Q-05 | Who may advance epoch, authorize break-glass, and reconcile authority rollback? | Defines security and human approval boundary. | Security/recovery owners; access model and audit policy | ADR-004 |
| Q-06 | What precisely proves Debezium slot/WAL continuity and Kafka topic identity? | Offset capture is only useful if no event can be omitted or offsets reused. | Database/Kafka owners; runtime metadata and controlled restart/slot-loss experiments | ADR-003 |
| Q-07 | Is the offset-before-snapshot protocol supported by actual Debezium/Kafka transaction semantics and commit-before-publish behavior? | The two systems do not share an atomic snapshot. | Database/Kafka/Search owners; version-pinned integration/failure tests | ADR-003 |
| Q-08 | Can Catalog provide a repeatable-read export including deletion fences, and how long can it run? | A long snapshot can retain old row versions; missing tombstones compromise rebuild. | Catalog/DB owner; API design and measured snapshot/vacuum impact | ADR-002/003 |
| Q-09 | What producer/consumer version skew and schema evolution are required? | Current v1 schema rejects unknown fields; coordinated deployment may be required. | Catalog/Search owners; release cadence and contract tests | ADR-001/006 |
| Q-10 | What is the resolved Spring Kafka version and effective ack/auto-commit behavior? | Retry/DLT semantics depend on dependency and runtime configuration. | Search owner; dependency resolution and runtime configuration evidence | ADR-006 |
| Q-11 | Does the deployed OpenSearch server/client pair support the required strict external version and tombstone operations? | Projection correctness depends on atomic version conflict semantics. | Search/platform owner; version-pinned integration tests | ADR-005 |
| Q-12 | Are both current Search consumer groups required? | They independently consume records; one can succeed while the other fails. | Search product owner; intended responsibilities and production use | ADR-006 |
| Q-13 | Who may inspect/replay DLT records, and where does replay publish? | Prevents unauthorized or looped replay and establishes audit semantics. | Search operations/security owner; runbook and authorization policy | ADR-006 |
| Q-14 | What RPO/RTO and capacity targets are acceptable? | No numeric targets can be responsibly proposed without business requirements and measurements. | Business/service/platform owners; timed restore/rebuild exercises | ADR-007 |
| Q-15 | Who owns alert response and the `platform-observability` repository? | README states an intended platform, but no implementation or team ownership is evidenced. | Engineering leadership/operations; named team, backend, and on-call | ADR-008 |
| Q-16 | Can old OpenSearch generations remain current enough for rollback, and how is that proven? | An old alias target may be stale and unsafe as a rollback. | Search owner; catch-up/freshness protocol and test | ADR-003/005 |
| Q-17 | Are the local `main` revisions still authoritative after the audit? | Catalog/Search tracking refs indicated local branches behind; no fetch was performed. | Repository owners; approved update/fetch and re-audit | Evidence baseline |

## Explicit assumptions in the proposals

- Catalog commits product state and outbox intent in one PostgreSQL transaction,
  as the inspected service annotations and persistence calls indicate; this
  does not establish atomicity with Kafka or OpenSearch.
- A Kafka offset vector is a set of partition-local positions, not a global
  transaction boundary.
- A source event delayed until after the captured offsets can be safe only
  under the snapshot/version assumptions in ADR-003.
- OpenSearch conditional write behavior, effective consumer commits, and
  external infrastructure retention remain unverified until tested.
- Documentation and prior test reports are not proof of current runtime
  behavior.
