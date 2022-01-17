

## Team Projects

- Name ```team_$wellchosenname```
- To allow a team to see which bugs,feature requests and stories are relevant in their current scrum
- Each day they should check what issues need to be worked on and which ones should have been done already
- Priorities:
    - "priority_cricital" means team needs to do it the same day (every other work needs to be suspended until done)
        - if it cannot be done in time, escalation needs to happen asap (not next day)
    - "priority_major" means the task should be done within 48 hours (exceptional 3 days, if its simply a too big issue)
        - this means, any priority task gets priority on everything else

The used swimlanes:

- ```Backlog``` 
    - A stakeholder or team lead suggests a feature/story/bug to be executed in the team
- ```Accepted```
    - The team lead accepts the item to be worked on in relation to the priority 
    - Once accepted = then escalation is needed if it can not be done in time (means < 1 week) or faster depending priority state
    - Everything which gets in the team Kanban on 'Accepted' needs to be resolved < 1 week from the day it was attached to team Kanban
- ```In progress```
    - The issue is being worked on
- ```Slow Cooker```
    - We are working on it but it goes slower
- ```Blocked```       
    - We are using the Kanban way of thinking; something in this swimlane needs to be resolved asap, can be e.g. a question
    - Means issue cannot be completed, attention from e.g. stakeholders is needed
- ```Verification```        : work is being verified
    - The team delivered the feature/bug/story
    - Stakeholders need to agree that the issue has been resolved appropriately
    - Project owner can never go from 'Verification' to 'Done' without approval from stakeholders (often represented by QA team)
- ```Done```
    - Everyone agreed; (project owner and stakeholders) agreed that the issue was done ok
    - check that the item is also in a project release and on right state (if relevant, not everything is on product release project)
