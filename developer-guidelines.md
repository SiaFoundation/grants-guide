## Developers Guidelines

The following is a copy of the Sia Foundation developer guidelines. It is
provided here for participants of the grants program to understand how we work
and what we consider best practices. It is not a requirement to strictly follow
these guidelines for grant projects, but we do encourage it.

## How We Work

- **Think before you code:**
  Take time to fully understand the problem before jumping into implementation. Discuss various implementations with your coworkers. If you need clarification, ask.

- **Consider complexity and future maintenance:**
  Simple solutions scale better. Every choice impacts the future. Design with maintainability in mind.

- **Focus on usability:**
  When adding features or endpoints, always think about how they’ll be consumed. Simplicity benefits users and makes future expansions easier. Don’t add additional knobs unless absolutely necessary.

- **Don’t hesitate to start over:**
  If your approach isn’t working quite right, it’s okay to pivot. Reworking early often leads to better results later.

- **Collaboration improves results:**
  Early peer feedback can improve end results. Leverage your team’s diverse expertise.

- **Prioritize quality over quantity:**
  Focus on delivering well-crafted, reliable solutions rather than rushing to implement more features. High-quality work ensures long-term success and reduces technical debt.

- **Don’t trust, verify:**
  A gut feeling is good but verification is better. If you fix a bug, verify it with a regression test first. If you optimize something, verify the performance improvement with a benchmark. Adding checks helps protect against regressions.

- **Post important updates in `#team-dev-updates`:**
  This creates a helpful, digestible history of changes other teams can use for content creation.

---

## Things We Like

- Simple, "inert" data structures
- Locally-defined interfaces
- Tests
- Short, descriptive names

## Things We Dislike

- Big objects with tons of state, methods, and mutexes
- Reflection
- Dependencies
- Tiny, fragmented packages
- Unorganized “utils” packages

---

## The Process

All development should start with an issue. If you feel like something needs to be done for which there is no issue, create one under Triage. Avoid PRs without associated, planned issues. This enables us to plan releases and prioritize milestones. Always prioritize milestones that are closer. If you don’t feel like you know what we are working towards, schedule a meeting and plan things out. Development is a lot more fun when you understand the goals and have a clear roadmap.

---

## Pull Requests

All code destined for the main branch must be merged through a pull request. All pull requests must be reviewed by at least one senior developer, not including the creator.

---

### Guidelines

- **Keep diffs simple.** Small focused PRs help reviewers and improve code quality. Larger PRs take more time to review.

#### Don’t

- Move unrelated code around in your PRs.
- Fix unrelated bugs in your PRs.
- Implement multiple isolated changes within a single PR.

#### Instead

- Refactor code in dedicated PRs.
- Keep bug fixes in dedicated PRs.
- Open one PR per logical change.
- Keep your PRs as small as possible.

---

### Communicate Effectively

- The reason for a PR should be obvious. Create a clear title, description and link an issue. Reviewers should never need to look at code to know what awaits them.
- Explain your reasoning. Reviews are a big part of how developers grow their skills and learn.
- **Review first, code later.** Asynchronous development is great but we need to work together to make sure it works smoothly. If you’re assigned to review a PR, prioritize the review over other tasks to unblock your coworkers quickly.

---

## For Small Isolated Changes

1. Assign yourself to the issue in GitHub.
2. Create a new feature branch in your local repository. Make the name short and descriptive, i.e. `chris/fix-sqlite-contract-query`.
3. Think about your code.
4. Code your feature.
5. Add tests.
6. Push the branch.
7. Create a pull request targeting the master branch.
8. Request a review from at least two senior developers with one preferably being the code owner.
9. Close the related Issue.

---

## For Large Refactors

1. Assign yourself to the issue in GitHub.
2. Break the feature up into small logical chunks and create sub-issues as necessary. If you are working with other team members in parallel, consider how you can split it up to block each other as little as possible.
   _E.g. an issue titled “Price Pinning” might have sub-issues “Implement PinManager”, “Add pinning endpoint”, “Integrate price pinning into UI”._
3. Create a new feature branch in your local repository. Make the name short and descriptive i.e. `rhp4`.
4. Push the feature branch.
5. For each logical chunk of work, create a new branch in your local repository. Make the name short and descriptive i.e. `chris/rhp4-add-initial-spec`.
6. Code the feature.
7. Create a pull request targeting the feature branch (i.e. `chris/rhp4-add-initial-spec` → `rhp4`)
8. Request a review from the code owner or a senior developer.
9. While waiting for them to review, move on to the next logical chunk.
10. Repeat until all work is complete and merged into the feature branch.
11. Create a PR to merge the feature branch (`rhp4`) into the master branch.
