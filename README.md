# GMCQ-benchmark

**GitHub Multiple Choice Questions** (GMCQ) is a benchmark developed to evaluate a language model's ability to determine the pull request that closes a bug fix issue from a real-world GitHub repository.

### Task Format

Given a GitHub issue title and description, without any additional context, the model must determine the correct pull request that closed the issue.

There is one correct issue and three false choices that are pull requests from the same repository that closed different issues.

The pull request description contains the filenames that were changed and the code patch that changed.

```
Task description:
<GitHub issue title and description>

---

Choice A:

<filenames and code patches>

---

Choice B:

<filenames and code patches>

---

Choice C:

<filenames and code patches>

---

Choice D:

<filenames and code patches>

```

### Dataset Generation Method

We took 82 GitHub closed issues with the bug label, along with the pull requests that closed the issue, from the Mastodon/Mastodon GitHub repository. 
