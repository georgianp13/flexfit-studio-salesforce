# FlexFit Studio: Salesforce Admin Portfolio Project

A fictional gym that uses Salesforce to run its business operations. I'm building it while training for the Salesforce Administrator certification, so I can practice real admin work instead of only studying exam topics.

## Goals

- Practice hands-on admin skills in a realistic business scenario
- Document what I build and why
- Keep my org's configuration in version control

## Data Model

Custom objects: Member, Membership Plan, Trainer, Class, Enrollment

Enrollment is a junction object with master-detail relationships to both Member and Class, creating a many-to-many relationship between members and classes. Each Class also has a lookup to its Trainer, and each Trainer has a lookup to a Salesforce User so classes can be tied to the trainer teaching them.

## Security

- **Profiles:** Front Desk Staff (limited access) and Studio Manager (full access)
- **Permission set:** Trainer access (in progress)
- Tabs created for all five custom objects

## Automation

**Class - Sync Owner to Trainer User** is a record-triggered Flow on Class. When a Trainer is assigned or changed, it finds the Trainer's linked User and sets that user as the Class owner. A Decision element skips the update if no user is linked, so records still save cleanly. This makes ownership-based sharing possible for trainers.

## Write-Up

- [Flow write-up](docs/class-owner-sync-flow.pdf)
- Video walkthrough: coming soon

## Up Next

- Tighten the Class org-wide default to Public Read Only
- Ownership-based sharing rule so trainers can edit their own classes
- Finish and assign the Trainer permission set
- Reports and dashboards
- Agentforce use case

## Tools

Salesforce Developer Edition org, Salesforce CLI, VS Code, Git/GitHub
