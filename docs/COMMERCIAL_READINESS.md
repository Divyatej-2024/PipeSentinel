# PipeSentinel commercial readiness

Status: prototype; not approved for paid or production use.

## Initial product scope
A SOC learning dashboard using synthetic events only. No customer infrastructure monitoring or real customer logs in the initial pilot. No claims of enterprise protection.

## Release gates
- [ ] Replace development credential defaults with explicit production configuration; review secret handling and restrict allowed origins.
- [ ] Verify authentication and authorization for every API and socket connection.
- [ ] Verify isolation between users and classrooms; the existing schema alone does not establish isolation.
- [ ] Verify synthetic data labeling and reset behavior.
- [ ] Add automated tests for configuration, access controls, data isolation, and dashboard behavior.
- [ ] Verify dependency licenses, ownership and third-party assets before selecting distribution terms.
- [ ] Document privacy, retention, deletion, accessibility, support and incident handling.
- [ ] Verify deployment, backups, restoration and operating costs.
- [ ] Collect feedback on a free educational pilot before selecting pricing.
- [ ] Review hosting terms, payment account eligibility and legal requirements with an eligible account owner before enabling billing.

## Current evidence
The root package test script is a placeholder. The database defines users, assets, events and alerts, but isolation is not established by the schema. Configuration has development defaults. Socket connections need an access-control review. These findings require implementation review and testing, not just documentation.

## Change control
Keep main unchanged until reviewed. Do not activate billing, buy hosting, or ingest customer data as part of this preparation.
