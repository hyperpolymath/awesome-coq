# Contribution Guidelines

This list aims to provide a concise list of noteworthy Coq projects and
resources. This means that suggested projects are:

1.  widely recommended, regardless of personal opinion

2.  highly discussed in the community due to its innovative nature

3.  absolutely unique in its approach and function

4.  a niche product that fills a gap

## Pull Requests

There are several required criteria for a pull request:

1.  If an entry has a similar scope as other entries in the same
    category, the description must state the unique features that
    distinguishes it from the other entries.

2.  If an entry does not meet conditions *(a)* to *(d)* there has to be
    an explanation either in the description or the pull request why it
    should be added to the list.

Self-promotion is viewed critically, but suggestions will be approved if
the criteria match.

Furthermore, please ensure your pull request follows the following
guidelines:

- Please search previous suggestions before making a new one, as yours
  may be a duplicate.

- Please make an individual pull request for each suggestion.

- Use the following format for entries: `-` `[Name](URL)` `-`
  `Description.`

- Entries should be sorted in ascending alphabetical order, i.e., A to
  Z.

- New categories or improvements to the existing categorization are
  welcome.

- Keep descriptions short, simple and unbiased.

- End all descriptions with a full stop/period.

- Check your spelling and grammar.

- Make sure your text editor is set to remove trailing whitespace.

Thank you for your suggestions!

## Signed commits

Every commit that reaches the default branch must be signed; a ruleset refuses
unsigned pushes. Estate policy:
[SIGNING-POLICY](https://github.com/hyperpolymath/standards/blob/main/docs/SIGNING-POLICY.adoc).

- **People and interactive agents** sign with an SSH key registered on GitHub
  as a *signing* key (`gpg.format=ssh`, `user.signingkey=<key>.pub`,
  `commit.gpgsign=true`). The committer email must be verified on that account.
- **Apps, bots and workflows** never `git push` local commits. They write
  through the API (`createCommitOnBranch` or the estate `signed-push` action)
  so that GitHub signs each commit.
- Merge PRs with **squash**. The ruleset checks every commit on the PR branch,
  not just the result, so one unsigned commit blocks the merge. Re-create such a
  branch with signed commits (`git cherry-pick -S`) and open a new PR.
  Rebase-merge replays commits unsigned and is disabled.
