## Development Branching

We encourage collaborative branching. Meaning any group of people working within the same scope are highly encouraged to work on the same branch, trusting and communicating with one another.

Our branching strategy is: 

- `master` is the last stable release
- `master_$hotfix` is only for solving BLOCKING issues which are in the field on the last release
    - short living
- `development` is where all stories branch from, and the one that has hotfixes if needed
- `development_$storyname`
    - branch for a story
    - always updated from development(_hotfixes)
- `development_$storyname_$reviewname`
    - short living branch for when reviews are needed for a story
- `development_hotfixes` short living hotfix(es) to allow people to review and then put on development
    - now everyone should update from or development or development_hotfixes
    - development_hotfixes is always newer than development
- `integration` is a branch used to integrate development branches
    - never develop on it, its for verifying & doing tests

We have branches for new features/disruptive changes. These have a prefix of `development_<relevantname>`

Each project and story should define which branches to use & the branching strategy.

There should never be any branch on the system which can not be found back by looking at the stories in the "home" repo.
Title of the story in between [] 
