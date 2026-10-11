# FlexFit Studio: Salesforce Admin Portfolio Project

A fictional gym that uses Salesforce to run its business operations. I'm building it while training for the Salesforce Administrator certification, so I can practice real admin work instead of only studying exam topics.

## Goals
- Practice hands-on admin skills in a realistic business scenario
- Document what I build and why
- Keep my org's configuration in version control

## Data Model
Custom objects: Member, Membership Plan, Trainer, Class, Enrollment

Enrollment is a junction object with master-detail relationships to both Member and Class, creating a many-to-many relationship between members and classes. Each Class also has a lookup to its Trainer.

## Completed
- Custom objects and relationships
- Profiles


## Up Next
- Permission sets


## Tools
Salesforce Developer Edition org, Salesforce CLI, VS Code, Git/GitHub
