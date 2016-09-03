# Git Style Guide

1. [Commit Messages](#1---commit-messages)
2. [Feature Branches](#2---feature-branches)
3. [Commit Timing](#3---commit-timing)
4. [Pull Request Timing](#4---pull-request-timing)
5. [Merging and Rebasing](#5---merging-and-rebasing)
6. [Releasing](#6---releasing)

## 1 - Commit Messages

1. Separate subject from body with a blank line
2. Limit the subject line to 50 characters
3. Capitalize the subject line
4. Do not end the subject line with a period
5. Use the imperative mood in the subject line
6. Use the body to explain *what* and *why* vs. *how*

Example:

```
Summarize changes in 50 characters or less

More detailed explanatory text, if necessary. Wrap it to about 72
characters or so. In some contexts, the first line is treated as the
subject of the commit and the rest of the text as the body. The
blank line separating the summary from the body is critical (unless
you omit the body entirely); various tools like `log`, `shortlog`
and `rebase` can get confused if you run the two together.

Explain the problem that this commit is solving. Focus on why you
are making this change as opposed to how (the code explains that).
Are there side effects or other unintuitive consequences of this
change?

Use `Resolves:` to close issues from the commit like so:

Resolves #123
Resolves #456
Resolves #789
```

[Read more](http://chris.beams.io/posts/git-commit/)

## 2 - Feature Branches

A branch should be created for each logical feature *in your own fork* using the format `ftr-x`. For example, a branch including vision tracking could be called `ftr-vision` in your own fork of the main repository.

## 3 - Commit Timing

**Commit often!**

You should commit after every logical change in the application using a commit message formatted to comply with the [Commit Messages](#1.1-commit-messages) section.

## 4 - Pull Request Timing

Pull Requests should be created to the `dev` branch of the base repository after the completion or during the development of a feature using a [Feature Branch](#1.2-feature-branches).

## 5 - Merging and Rebasing

Pull Requests should be squashed before being merged, which should be set as the default in the repository settings when the repository is created.

Branches should be rebased into other branches.

## 6 - Releasing

Releases should follow the format `MAJOR.MINOR.PATCH` which should be incremented as follows:

1. MAJOR version when you make incompatible API changes
    - e.g. new methods
2. MINOR version when you add functionality in a backwards-compatible manner
    - e.g. significant edits to existing methods
3. PATCH version when you make backwards-compatible bug fixes
    - e.g. tiny fixes to existing methods

A release should be created every time `master` is rebased to reflect changes on `dev`.
