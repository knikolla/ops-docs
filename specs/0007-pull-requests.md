# What makes a good pull request?

This document discusses our standards for pull requests and commits.

## Problem Description

A poorly constructed pull request can be a frustrating experience both
for the person making the pull request and for those people that are
trying to review it. By setting forth some guidelines in this
document, we hope to make the review process a useful and productive
experience for everyone involved.

## Policy

### What makes a good pull request?

A good pull request is **clean**. In most cases it should be made
against the current version of the primary branch in the repository
(usually `master`, `main`, or `trunk`). It should be free of syntax
errors and linting problems. Your local development environment should
be configured to notify you of those problems in your editor and/or in
a `pre-commit` hook. Your pull request should pass any unit tests that
exist in the repository (and if you are introducing a new feature,
your pull request should include tests appropriate to that feature).

Whenever possible, your project should use tooling that enforces a
consistent code formatting standard. This ensures that apparent
changes aren't solely caused by differences in formatting style
between the author of the original code and the author of the proposed
change.

A good pull request is **focused**. It should only contain a few
closely related commits, and each commit should have a clear purpose.
Commits should be **isolated** such that a single commit can be
reverted without invalidating everything else in the pull request.
Keeping commits small and focused like this makes it easier for
reviewers to understand and review the pull request in a timely
fashion. Google has [an entire document][small-cls] on the benefit of
small changes.

[small-cls]: https://google.github.io/eng-practices/review/developer/small-cls.html

Commit messages in your pull request should be **meaningful**.  They
should follow common community standards ([1][], [2][], [3][]),
such as:

[1]: https://www.theserverside.com/video/Follow-these-git-commit-message-guidelines
[2]: https://reflectoring.io/meaningful-commit-messages/
[3]: https://cbea.ms/git-commit/

1. Separate subject from body with a blank line
1. Limit the subject line to around 50 characters
1. Capitalize the subject line
1. Do not end the subject line with a period
1. Use the imperative mood in the subject line
1. Wrap the body at 72 characters
1. Use the body to explain what and why vs. how

("Use the imperative mood" means that your subject makes sense when
preceded by the phrase "This commit will…".)

If your commit addresses specific issues from an issue tracker, they
should be called out in the commit message.

Commit messages that should explicitly be avoided are those that
provide no information about the contents of the commit, such as:

- "Responding to review feedback"
- "Integrated changes from Bob"
- "Refactored code"

Your pull request description should provide a broad summary of the
changes included in the request. Unlike commit messages, the pull
request description can take advantage of GitHub formatting for
clarity (e.g., including diagrams, linking to documentation, etc).
This is a good place to provide any background that you think would be
useful to reviewers.

### As an author

- Provide reviewable pull requests

  Ensure that your pull requests meet the guidelines set forth earlier
  in this document.

- Recognize that you will need to change your code

  People are imperfect, and even though you've spent hours working on
  a new feature implementation, someone is going to spot something
  that you missed or bring a different perspective to the review that
  may result in a request for changes.

  Over time, participating in code reviews will make the code better
  and will make you a better developer.

- Respond to change requests promptly

  If people are taking the time to review your code, you should
  respond promptly to those reviews. This may mean you need to pivot
  away from working on an exciting new feature in order to address the
  requested changes.

- Append commits to your pull request rather than rebasing

  This makes it easier for reviewers to see what has changed when you
  update the pull request. Multiple commits can be squashed together
  when the pull request merges.

### As a reviewer

- Recognize that pull requests take time

  Even a well-written pull request will require time for the review.
  Make pull request reviews a part of your day, rather than an
  afterthought, so that you don't feel like you're trying to cram
  reviews in between other work.

- Respond to review requests promptly

  If there is a code review, someone is waiting for your feedback,
  possibly before they can continue with their work. Try to respond to
  review requests in a timely fashion.

- Provide constructive feedback

  Don't just tell people that something is broken. Explain why you
  believe something needs changing, and consider providing examples
  where appropriate.

## Alternatives & History

N/A

## Implementation

### Author(s)

Primary author:
  - Lars Kellogg-Stedman <lars@redhat.com>

### Milestones

N/A

### Work Items

N/A

## References

There are a variety of posts available on this topic. Here are a few
that I found useful:

- https://google.github.io/eng-practices/review/reviewer/
- https://developers.google.com/blockly/guides/modify/contribute/write_a_good_pr
- https://www.atlassian.com/blog/git/written-unwritten-guide-pull-requests
- https://betterprogramming.pub/how-to-make-a-perfect-pull-request-3578fb4c112

## License

This work is licensed under a Creative Commons Attribution 3.0
Unported License.
<http://creativecommons.org/licenses/by/3.0/legalcode>
