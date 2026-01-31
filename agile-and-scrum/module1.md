# Introduction to Agile Development and Scrum

## Course objectives 

After completing this course, you will be able to: 

- Define Agile and describe its guiding philosophy and principles 
- Compare Agile to other methodologies such as Waterfall, XP, and Kanban 
- Apply Scrum roles, events, and artifacts within Agile teams
- Write and manage user stories, assign story points, and refine product backlogs
- Build and track progress on a Kanban board
- Conduct sprint planning, reviews, retrospectives, and daily stand-ups
- Use burndown charts to forecast the team’s ability to achieve the sprint goal

## What is Agile?

Agile is an *iterative* approach to project management that helps team be *responsive* and *deliver* value to 
their customers faster.

- ***adaptive planning*** --> plan small iterations, rather than a whole year
- ***evolutionary development*** --> develop the product in small increments, rather than the whole thing at once
- ***early delivery*** --> get faster feedback from customers
- ***continual improvement*** --> customer feedback allows for faster improvements or the team knowing their on the right track

> **Agile Manifesto**
> 
> *We have come to value:*
> 
> - **Individuals and interactions** over processes and tools
> - **Working software** over comprehensive documentation
> - **Customer collaboration** over contract negotiation
> - **Responding to change** over following a plan
>
> *That is, while there is value in the items on the right, we value the items on the left more.*

In agile software development we emphasize on
- flexibility
- interactivity
- transparency 
- small, self-organized teams

This allows a team to build what ***is*** needed, not what ***was*** planned!

## Traditional Waterfall Development

Structured, step-by-step development process that.

1. ***Requirements Phase:*** all about documenting the needs of the customers first.
2. ***Design Phase:*** Architects define - from the requirements - the final design of the software.
3. ***Code Phase:*** Developers code the software - from the design.
4. ***Integration Phase:*** The whole software comes together for the first time.
5. ***Testing Phase:*** The whole software is tested, any bugs may lead to entering coding, or even worse, design phase again
6. ***Deploy Phase:*** The software can be deployed

### Problems with waterfall approach

- No provision for changing requirements, each stage has strict entrance and exit criterions
- No idea if it works until the end
- Each step ends, when the next begins
- Mistakes found in later stages are more expensive to fix
- Long time between software releases
- Teams work separately, unaware of their impact on each other

## Working Agile

In order to actually work agile, we should focus on the following steps when tackling a new project. 

1. **The strategy: Define Minimum Viable Product (MVP)**
    - Cheapest/easiest thing you can do to test a hypothesis an learn

2. **The Definition: Use Behavior Driven Development (BDD)**
    - Define the behaviour of the system from the **outside in** (from a customers perspective)
    - Use simple plain text scenarios so devs and stakeholdrs can agree on the outcome
      - As a [role], I need [some functionality], So that [some business value]
      - Given a [set of preconditions], when an [event] occurs, then some [outcome] is observed

3. **The Execution: Test Driven Development (TDD) & Pair Programming**
    - Test the functions of the system from the **inside out** (from a developers perspective)
    - Write the tests first for the code you wish you had, then you write the code to make the tests pass
    - Discover defects earlier and increase code quality by peer reviewing continously
    - **Work in Small Batches**, rather then implementing the whole product at once

### Example
*Let's introduce a simple example. We are tasked to build a file conversion service. The service runs on daily schedule and converts 
files from format A into format B. More specific, we need two distinct format A files to process it into format B. There exists 24 
conversions a day, but the logic for converting stays the same for all 24 conversions. The files arrive from an already existing 
service at a given time a day, but the arrival time can be delayed, missing, or multiple versions of format A file might arrive.* 

1. The heart of our service is the conversion. So our MVP would be a service that processes two local format A files into format B
2. Before we write a single line of code, write the "Behavior" in plain English and ensures you and your stakeholders agree on what "done" looks like.
    - Scenario: Successful conversion of a pair.
      - Given I have "File_1.A" and "File_2.A" in the landing zone.
      - When the conversion trigger occurs.
      - Then a single "Output.B" should be generated and the source files archived.
3. Now, sit down with a teammate. One of you explains the logic, the other types. This prevents you from getting stuck on a single bug for three hours.
    - Write a test that looks for Output.B. It will fail because the file doesn't exist yet. Then, write just enough code to make that file appear.
    - Work in Small Batches: Don't try to code the "delay schedule" and the "format converter" in the same afternoon.
      - Batch 1: Function to merge two files. (Commit code)
      - Batch 2: Logic to check if 2 files exist. (Commit code)
      - Batch 3: The "Delay" timer. (Commit code)
