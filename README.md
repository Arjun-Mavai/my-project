# my-project
checking branch features through this repository


# branch after raising a pull request
- I deleted the branch on github , then in local I did commands on local like
- git fetch --prune
- git branch -d branch_name ///// -b for creating a branch // git checkout for switching between branches
- git remote update origin --prune


If you have already merged and deleted the branch on GitHub, but it is still showing in your local system, you need to perform a few additional steps to update your local repository.

Here's what you can do to clean up your local system:

**Step 1: Fetch the latest changes from the remote repository:**
In your terminal or Git client, navigate to your local repository's root directory and run the following command:

```bash
git fetch --prune
```

The `--prune` flag tells Git to remove any remote-tracking references (like branches) that no longer exist on the remote repository (GitHub, in this case).

**Step 2: Delete the local branch:**
After fetching the latest changes, you can delete the local branch that you have already merged. To delete the branch, run the following command:

```bash
git branch -d branch_name
```

Replace `branch_name` with the name of the branch you want to delete. The `-d` flag stands for "delete." If the branch contains any unmerged changes, Git will not allow you to delete it. In that case, you can use `-D` (uppercase) instead to force delete the branch, but be careful as you might lose any unmerged changes.

**Step 3: Update the list of remote branches:**
To ensure your local branch list is updated, run the following command:

```bash
git remote update origin --prune
```

This command updates the list of remote branches and prunes any branches that were deleted on the remote repository (GitHub).

After following these steps, your local repository should no longer show the branch that was already merged and deleted on GitHub.

Keep in mind that Git is a distributed version control system, and the local repository might not immediately reflect all changes made on the remote repository. By following the steps above, you ensure that your local repository is up to date and in sync with the changes made on GitHub.






