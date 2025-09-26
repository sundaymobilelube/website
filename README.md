# website

## Resolving Pull Request Merge Conflicts

When GitHub says "This branch has conflicts that must be resolved," it means the feature branch includes changes that clash with the latest version of the base branch (often `main`). GitHub cannot automatically merge the pull request because the same parts of a file have been edited in both branches. To move forward:

1. **Fetch and switch to the feature branch locally.** Make sure you have the most recent commits from both the feature branch and the base branch.
2. **Merge or rebase the base branch into the feature branch.** This brings the latest base-branch changes into your branch so you can handle the conflicts locally.
3. **Resolve the conflicts manually.** Open each conflicted file, decide which changes to keep (or how to combine them), and remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).
4. **Commit the resolved files.** After saving the fixes, stage the files and commit the resolution.
5. **Push the updated branch.** Once the conflicts are resolved locally and pushed, GitHub will detect that the branch is mergeable again.

Only after these steps will the pull request show as conflict-free and ready for merge. If you are unsure which changes to keep, coordinate with the teammate who made the conflicting updates so the final result reflects the correct version.

## Resolving Conflicts in the GitHub Web Editor

If you do not have Git installed locally, you can still fix simple merge conflicts directly in the GitHub interface:

1. **Open your pull request** and look for the yellow banner that says "This branch has conflicts that must be resolved." Click the **Resolve conflicts** button.
2. **Review each conflicted file** in the web editor. GitHub highlights the same `<<<<<<<`, `=======`, and `>>>>>>>` markers you would see locally. Decide which version to keep—or edit the block so it contains the correct combined changes.
3. **Delete the conflict markers** once the content looks right. The file should read normally with no leftover markers.
4. **Mark the file as resolved** by selecting **Mark as resolved** at the top of the editor. Repeat for any remaining conflicted files.
5. **Commit the merge** by clicking **Commit merge** (or **Commit changes**) after all conflicts are resolved. GitHub creates a merge commit for you and updates the pull request.

When you return to the pull request page, the conflict banner should disappear and the **Merge** button becomes available. If GitHub shows a new error, refresh the page to make sure all files were committed, or reopen the editor to finish resolving the outstanding conflicts.
