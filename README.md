# website

## Resolving Pull Request Merge Conflicts

When GitHub says "This branch has conflicts that must be resolved," it means the feature branch includes changes that clash with the latest version of the base branch (often `main`). GitHub cannot automatically merge the pull request because the same parts of a file have been edited in both branches. To move forward:

1. **Fetch and switch to the feature branch locally.** Make sure you have the most recent commits from both the feature branch and the base branch.
2. **Merge or rebase the base branch into the feature branch.** This brings the latest base-branch changes into your branch so you can handle the conflicts locally.
3. **Resolve the conflicts manually.** Open each conflicted file, decide which changes to keep (or how to combine them), and remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
4. **Commit the resolved files.** After saving the fixes, stage the files and commit the resolution.
5. **Push the updated branch.** Once the conflicts are resolved locally and pushed, GitHub will detect that the branch is mergeable again.

Only after these steps will the pull request show as conflict-free and ready for merge. If you are unsure which changes to keep, coordinate with the teammate who made the conflicting updates so the final result reflects the correct version.
