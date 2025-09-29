# The Sia Foundation Grants Development Guide

This document outlines the repository structure and reporting requirements for
approved [grants under the Sia Foundation](https://sia.tech/grants). A milestone
is only considered complete when all associated tasks have been completed and
have been reported during the monthly update using the structure outlined in
this document.

## Milestones

Each grant will have a set of milestones defined in the grant proposal and
approved by the Sia Foundation. Before applying for a grant, applicants should
ensure that the milestones are **well-defined** and **achievable** within the
proposed timeline. After the milestones are defined, they should be broken down
into smaller, logical tasks that can be implemented in one or more small pull
requests. These pull requests will eventually be linked in [the monthly progress
reports](https://sia.tech/monthly-grant-report-template) to determine the
completion of each milestone.

## Development Process

With your milestones and tasks defined, you can begin development. The following
steps outline the process for implementing your previously defined tasks:

1. Start each task with a new branch. The name of the branch should resemble the
   task you are working on. If a task requires updating multiple repositories,
   create matching branches in each repository.
2. Implement the task in small, focused pull requests. Each pull request should
   address a single logical change and be as small as possible to facilitate
   easier review. Refer to the Sia Foundation's [developer
   guidelines](developer-guidelines.md) for more details on our coding standards
   and pull request best practices.
3. When the task is complete, open a pull request against the default branch of
   the repository. The pull request should contain a clear title and description
   of the changes made. If the task can't be completed fully, mention what
   difficulties were encountered and what remains to be done.
4. If applicable, include a description of how the changes can be tested, e.g.
   by running a specific integration test, trying out a new feature in the UI,
   etc.
5. Make sure the code is buildable.
6. Merge the pull request and move on to the next task.

ℹ️ As you complete tasks, make sure to also update the README files in each of
your repositories. Reviewers should be able to understand the purpose and
functionality of your code by reading the README files as well as being able to
run and test the code based on the instructions provided. A short example of a
README file can be found [here](example-grant/README.md). The minimum
requirements for a README file are a brief overview of the repo and its purpose
as well as instructions on how to build the code.

### Checklist

The following checklist summarizes the key points of the development process:

- [ ] At least one pull request per task
- [ ] Pull requests have
  - [ ] Clear title
  - [ ] Clear description
  - [ ] Testing instructions for reviewers or a note on why testing is not applicable
- [ ] Code is buildable
- [ ] README files contain
  - [ ] Overview of the repository and its purpose
  - [ ] Instructions on how to build and run the code

## Progress Reporting

Progress on milestones should be [reported
monthly](https://sia.tech/grants#when-are-monthly-progress-reports-due) by
providing a summary of tasks that have been completed. List all the milestones
for which progress is being reported and all the associated tasks that have been
completed. For each task, include a link to the corresponding pull request(s)
that implement the task.

The following table outlines the expected format for reporting:

| Milestone                             | Task                                  | Pull Request(s)                                            | Additional Notes                |
|---------------------------------------|---------------------------------------|------------------------------------------------------------|---------------------------------|
| 1: Improve Application Output         | 1. Print "Hello, World!"              | [#1](https://github.com/SiaFoundation/grants-guide/pull/1) |                                 |
| 1: Improve Application Output         | 2. Print "Goodbye, World!"            | [#2](https://github.com/SiaFoundation/grants-guide/pull/2) | Took slightly longer because saying "Goodbye" is hard |

⚠️ Existing grants that were approved before the publication of this document may
follow a different development process. In such cases, you may link to commits
instead of pull requests and use the "Additional Notes" column to add context on
the changes made.

## Conclusion

By following the guidelines outlined in this document, grant recipients can
ensure a clear, organized, and transparent development and reporting process.
Well-defined milestones, thorough documentation, and consistent progress updates
help both the Sia Foundation and grantees track achievements and address
challenges effectively.
