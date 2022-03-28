# Objective of Raiven

TODO Ivan

# Rationale

This exercise has two goals

- It helps us to understand what to expect from you as a developer, how you write production code, how you reason about design and how you communicate when trying to understand a problem before you solve it.
- It helps you get a feel for what it would be like to work at Raiven, as this exercise aims to simulate our day-as-usual and expose you to the type of work we're doing here.

# Requirements

There are three levels to this interview.
Each level is built on top of the previous level.
This excercise will take one week to complete.
We recommend to allocate the first days for drafting a design document about your approach.
The rest would be for implementation of your design.
We recommand using python for your implementation.

Before you start one week, please decide and let us know what level you'd like to do.
After that, you can start the one week at your own time.

## Design Document

Start with a brief doc that covers the edge cases and design approach. At Raiven, we prefer Markdown for our designs.

Be sure to cover the following in your design:

user experience: a couple examples of what it may look like to design a pipeline. This allows us an opportunity to envision how we will run the program.
Open a pull request with your design and share a link with the reviewers via Teams. After the doc is approved, implement interfaces and an example program using the library.

A few notes about the design document:

We expect the design document to be complete roughly within the first 3 days. This is to ensure you have enough time to work on the implementation.
Avoid writing an overly detailed design document. Two to three pages is sufficient.
Avoid sending us draft design documents, it is difficult to evaluate what parts are draft and which parts are complete.
Instead we encourage asking questions in Teams and sharing a design document that is ready to be reviewed.

## Project

Imagine that we have a set of executables each of them take some input from `STDIN`, do some processing and output something in `STDOUT`.
design a framework for arbitrarily connecting `STDIN` and `STDOUT` of different executables together.
Allow for one `STDOUT` to be connected to multiple `STDIN`s.
What kind of definitions would you require for a sound framework design?
How would a pipeline with various processes be formally defined
Think of restrictions that make sense in this scenario.
How would u represent a layout in this scenario?

# Guidance

## Interview process

The interview team will join the teams channel. The team consists of the
engineers who will be working with you. Ask them about the engineering culture,
work and life balance, or anything else that you would like to learn about
Teleport.

Before writing the actual code, create a brief design document in markdown in Github and share with the team.

This document should cover at least: design approach, trade-offs, scope.

Please avoid writing an overly detailed design document. Use this document to
make sure the team could provide feedback on your design and demonstrate that
you've investigated the problem space.

Split your code submission using pull requests and give the team an opportunity
to review the PRs. A good "rule of thumb" to follow is that the final PR
submission is a formality adding a small feature set - it means that the team
had an opportunity to contribute the feedback during multiple well defined
stages of your work.

Our team will do their best to provide a high quality review of the submitted
pull requests in a reasonable time frame. You are spending your time on this, we
are going to contribute our time too.

After the final submission, the interview team will assemble and vote using a
"+1, -2" anonymous voting system: +1 is submitted whenever a team member accepts
the submission, -2 otherwise.

In case of a positive result, we will connect with you further for an offer.

In case of a negative score result, hiring manager will contact you and share a
list of the key observations from the team that affected the result.

## Code and project ownership

This is a test challenge and we have no intent of using the code you've
submitted in production. This is your work, and you are free to do whatever you
feel is reasonable with it. In the scenario where you don't pass, you can open
source it with any license and use it as a portfolio project.

## Areas of focus

Raiven focuses on AI pipelines.

These are the areas we will be evaluating in the submission:

* Use consistent coding style.
* At the minimum, create tests for invalid user inputs
* Make sure builds are reproducible. Pick python3.
* Ensure error handling and error reporting is consistent. The system should
  report clear errors and not crash under non-critical conditions.

## Trade-offs

Write as little code as possible, otherwise this task will consume too much time
and code quality will suffer.

Please cut corners, for example configuration tends to take a lot of time, and
is not important for this task.

Use hardcoded values as much as possible and simply add TODO items showing your
thinking, for example:

```
  // TODO: Add configuration system.
  // Consider using CLI library to support both
  // environment variables and reasonable default values,
```

Comments like this one are really helpful to us. They save yourself a lot of
time and demonstrate that you've spent time thinking about this problem and
provide a clear path to a solution.

Consider making other reasonable trade-offs. Make sure you communicate them to
the interview team.

Here are some other trade-offs that will help you to spend less time on the task:

* Do not implement a system that scales or is highly performing. Describe which
  performance improvements you would add in the future.
* It is OK if the system is not highly available. Write down how you would make
  the system highly available and why your system is not.

## Pitfalls and Gotchas

To help you out, we've composed a list of things that previously resulted in a no-pass from the interview team:

* Scope creep. Candidates have tried to implement too much and ran out of time
  and energy. To avoid this pitfall, use the simplest solution that will work.
  Avoid writing too much code. We've seen candidates' code introducing caching
  and making many mistakes in the caching layer validation logic. Not having
  caching would have solved this problem.
* Data races. We will scan the code with a race detector and do our best to find
  data races in the code. Avoid global state as much as possible; if using
  global state, write down a good description why it is necessary and protect it
  against data races.
* Unstructured code. We've seen candidates leaving commented chunks of code,
  having one large file with all the code, not having code structure at all.
* Not communicating. Some candidates have submitted all their code to the master
  branch without raising pull requests, which does not give us the ability to
  provide feedback on the various implementation phases. We are a distributed
  team, so structured, asynchronous communication is critical to us.

## Questions

It is OK to ask the interview team questions. Some folks stay away from asking
questions to avoid appearing less experienced, so we provide examples of
questions to ask and questions we expect candidates to figure out on their own.

It demonstrates that you thought about this problem domain, recognize the trade
off and are saving you and the team time by not implementing it.

This is the question we expect candidates to figure out on their own:

> What exact version of Python should I use?

Unless specified in the requirements, pick the solution that works best for you.

# Tools

This task should be implemented in python 3 and should work on 64-bit Linux machines.

# Timing

You can split coding over a couple of weekdays or weekends and find time to ask
questions and receive feedback.

Once you join the Teams channel, you have between 1 week to complete the
challenge.

Within this timeframe, we don't give higher scores to challenges submitted more
quickly. We only evaluate the quality of the submission.

We only start the coding challenge if there are several open positions available.
