# Objective of Raiven

We are developing a platform for encapsulation, orchestration, and application of image processing algorithms in radiology and medical imaging. Using our platform, researchers and physicians can easily prototype and use pipelines that include AI models, and radiomics/biomarkers (typically implement as distinct libraries/executables). Our goal is to bring advanced technologies to clinical practice at BC Cancer and worldwide, so that they can directly benefit patients suffering from cancer and other debilitating diseases.

The platform consists of the main application, called Raiven, as well as auxiliary/supporting applications to perform specific tasks, for example data anonymization. During your co-op, you may be asked to work on the main application as well as supporting applications.

# Rationale

This exercise has two goals

- It helps us to understand what to expect from you as a developer, how you write production code, how you reason about design and how you communicate when trying to understand a problem before you solve it.
- It helps you get a feel for what it would be like to work at Raiven, as this exercise aims to simulate our day-as-usual and expose you to the type of work we're doing here.

## Exercise Project

Imagine that we have a set of executables, each of them take some input from `STDIN`, do some processing and output something in `STDOUT`.
Design a framework for arbitrarily connecting `STDIN` and `STDOUT` of different executables together.
Allow for one `STDOUT` to be connected to multiple `STDIN`s.
Implement a simple example program to construct such pipelines.

Specifically, address the following:
What kind of definitions would you require for a sound framework design?
How would a pipeline with various processes be formally defined?
Think of restrictions that make sense in this scenario.
How would you represent a layout in this scenario?

# Requirements

# Tools

This execise task should be implemented in python 3 and should work on 64-bit Linux machines.

# Timing

You will have one week to work on this excercie, starting immediately after your Zoom interview with us.

Within this timeframe, we don't give higher scores to challenges submitted more quickly. We only evaluate the quality of the submission.

We will be accept solutions completed to different degrees - the more you're able to complete, the better! However, higher preference will be given to more complete solutions.

We recommend to allocate the first days for drafting a design document about your approach.
The rest would be for implementation of your design.

## Design Document

Before writing the actual code, create a brief design document in Markdown in Github and share the link with us. The design document should cover the design approach and edge cases. The document can follow any layout or formatting that you prefer.

Be sure to also cover user experience in your design, with a couple examples of what it may look like to design/build a pipeline. This allows us an opportunity to envision how we will run the program.

Once your design document is completed, share a link to it with the reviewers via Teams. After that, start working on the implementation, incliding an example of program that uses any library or libraries that you develop.

We expect the design document to be complete roughly within the first 3 days. This is to ensure you have enough time to work on the implementation.
Avoid writing an overly detailed design document. Two to three pages is sufficient.
Avoid sending us draft design documents, it is difficult to evaluate what parts are draft and which parts are complete.
Instead we encourage asking questions in Teams and sharing a design document that is ready to be reviewed.

# Guidance

## Development process

While working on this execice, you can join a Teams channel where you will be assigned an engineer to answer any questions that you may have about the excercie.

## Code and project ownership

We will not use any code that you submit as a part of this exercise. This is your work, and you retain full rights to it.

## Areas of focus

Raiven focuses on AI pipelines.

These are the areas we will be evaluating in the submission:

* Use consistent coding style.
* Create tests for invalid user inputs.
* Make sure builds are reproducible. Pick python3.
* Ensure error handling and error reporting is consistent. The system should
  report clear errors and not crash under non-critical conditions.

## Trade-offs

Write as little code as possible, otherwise this task will consume too much time and code quality will suffer.

Please cut corners, for example configuration tends to take a lot of time, and is not important for this task.

Use hardcoded values as much as possible and simply add TODO items showing your thinking, for example:

```
  // TODO: Add configuration system.
  // Consider using CLI library to support both
  // environment variables and reasonable default values,
```

Comments like this one are really helpful to us. They save yourself a lot of time and demonstrate that you've spent time thinking about this problem and provide a clear path to a solution.

Consider making other reasonable trade-offs. Make sure you communicate them to the interview team.

Here are some other trade-offs that will help you to spend less time on the task:

* Do not implement a system that scales or is highly performing. Describe which performance improvements you would add in the future.
* It is OK if the system is not highly available. Write down how you would make the system highly available and why your system is not.

## Pitfalls and Gotchas

To help you out, we've composed a list of things that previously resulted in a no-pass from the interview team:

* Scope creep. Candidates who try to implement too much run out of time and energy. To avoid this pitfall, use the simplest solution that will work. Avoid writing too much code.
* Avoid global state as much as possible; if using global state, write down a good description why it is necessary and protect it against data races.
* Unstructured code. Don't leave commented chunks of code, having one large file with all the code, not having code structure at all.

## Questions

It is OK to ask questions about the assignment, but not about potential solutions. Do not avoid asking questions to in fear of appearing less experienced!

This is the question we expect candidates to figure out on their own:

> What exact version of Python should I use?

Unless specified in the requirements, pick the solution that works best for you.


GOOD LUCK!
