# Agile Planning

## What is a user story?

A user story represents a small piece of business value that a team can deliver in an iteration.

Stories should contain:
- A brief description of the need and business value
  - document a person requesting a function to achieve a goal
  - As a [role], I need [some function], so that [some benefit]
  - Based on the business value we can then prioritize user stories
- Any assumptions or details
  - List important documents we already know
  - List any assumptions
  - Details that may help the developer
- The acceptance criteria
  - Describe what done means
  - Given some [preconditions], when some [event] happens, then some [outcome]

Stories should be:
- **Independent** --> sometimes dependencies might occur, which is fine, as long as they are visible
- **Negotiable** --> we should be able to rank stories based on their value
- **Valuable** --> stories without any value should be discarded 
- **Estimable** --> we should be able to estimate the amount of work needed roughly
- **Small** --> should be generally small so that we can finish them in an iteration
- **Testable** --> To ensure the acceptance criterias are actually met

### Example

**Description**
- **As a** Marketing Manager, **I need** a list of customer names and emails, **so that** I can notify them of marketing promotions.

**Assumptions and Details**
- We maintain customer emails
- Customers have opted-in to promotions

**Acceptance Criteria**
- **Given** there are 100 customers in the database, and 90 have opted into email promotion, **when** I request the customer email list, **then** I should see a list of 90 customer emails.

## What is an epic?

An Epic is a large body of work that can be broken down into many smaller User Stories. 
If a story is too big to fit into a single Sprint (the 2-week work cycle), it’s usually an Epic.

Epics help the Product Owner group related work together to track progress on big features.

Backlog items tend to start as as epics when they are lower priority and less defined.

**Quick questions to be sure if it's an epic**
1. Can I estimate the work (eg. the estimation too vague because of unkowns etc.)? --> No = Epic
2. Can I complete the user story in less than 2 weeks (eg. the user stories effects many parts of the system and could thus be broken down into smaller user stories)? --> No = Epic

## Prioritizing User Stories - Story Points

Story points is a *metric* used to estimate the *difficulty of implementing* a given user story. It is an *abstract* measure of overall effort.

**What does a story point measure?**
- Effort: how much work do I need to put into it?
- Complexity: how complex/easy is the work?
- Uncertainity: did I do such task already or is it completly new?

Instead of predicting the actual time it may take to do something, story points use **relative T-Shirt sizes** (S=3, M=5, L=8, XL=13).

Agree on what "medium" means, since story points are relative!

**What story points are not meant for**
- A story point is not a wall-clock time!
- Humans are bad at estimating time!

## Building a product backlog

A product backlog contains all the unimplemented stories not yet in a sprint ranked.
Stories are ranked in order of importance and/or business value. Stories are more detailed at the top, less detailed ones
are at the bottom.

### Backlog Refinement
- Keept the product backlog ranked by priority so that important stories are always on top and ready for the next sprint.
- Break large stories down into smaller ones if needed
- Make sure that stories near the top of the backlog are groomed and complete
- Remove any duplicates or non-stories

This can be done in a Backlog refinement meeting. Attendes should be
- Product owner --> main person who writes the stories
- Scrum master
- Lead developer/architect

What is the goal?
- Groom the backlog by ranking the stories in order of importance
- Make sure the stories contain enough information for a dev to start working, we dont want to add details during the sprint planning meeting!
- At the end of the backlog refinment meeting, the New Issues column should be empty
