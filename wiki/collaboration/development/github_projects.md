
**Github project based**

## Service / Product (account level)

Each product has a clear name and a version.

- The name is ```product_$name_$versionnr``` and is hosted on account level

- Each product is defined on a product page in the "home" repo
- The home page in the home repo links to the product pages
- Each product is linked to components which are relevant for the next release
- Each component is clearly defined by a version nr. That component corresponds with 1 (exceptional more) Github repo's, where repo projects show the next release. The common release linked to the product release is marked on the product page in clear ways.
- Each product links to release notes which show history and per release (note) there are links to the components as used at that point
- A product can link to another product too which then links to the component!
- A product can link to a 3rd party product; also there specify the used version nrs

## Component Project (on repo level)

Generally only **1** github repo, there can be **exceptional** cases where 1 component spans multiple repos but this is the exception. Normally it means its just more than 1 component.

The used swimlanes:

- ```Backlog``` 
    - Stakeholder or project owner suggests a feature/story/bug to be resolved in this release
- ```Accepted```
    - The project owner accepts the item, the issue will be worked on and he commits to solve within the release
    - Once accepted = then escalation is needed if it can not be done in time
- ```In progress```
    - The issue is being worked on
- ```Blocked```       
    - We are using the Kanban way of thinking - something in this swimlane needs to be resolved asap, can be e.g. a question
    - Means issue cannot be completed, attention from e.g. stakeholders is needed
- ```Verification```        : work is being verified
    - The team delivered the feature/bug/story
    - Stakeholders need to agree that the issue has been resolved appropriately
    - Project owner can never go from 'Verification' to 'Done' without approval from stakeholders (often represented by QA team)
- ```Done```
    - Everyone agreed (project owner and stakeholders) agreed that the issue was done ok
    
> exception only: when component is more than 1 repo, make the project on account level, in any other case its in the repo.

Example:

```markdown
**eVDC 2.3**

- Requires: TFGrid 2.3 and 3bot 2.3
- Linked components: None

**TFGrid 2.3**

- Requires: Nothing
- Linked components: ZOSv0.5, HUBv..., ZDBv..., ...

**3Bot 2.3**

- Requires: Nothing
- Compatible with: TFGrid 2.3
- Linked components: jsng..., jssdk...

```

You see how different products can be made up out of other products. Its up to the product manager to link the right components to it.
