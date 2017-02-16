# Reverting a Commit

### What is reverting a commit ?
If you change your mind about a commit after you create it, you can revert the commit.
When you revert to a previous commit, the revert is also a commit. In addition, the original commit remains in the repository's history. You can always revert a revert if necessary, we do it all the time!

```
Tip: When you revert multiple commits, it's best to revert in order from newest to oldest. 
If you revert commits in any other order, you may see merge conflicts.
```    
Reference - [reverting a commit](https://www.atlassian.com/git/tutorials/undoing-changes#git-revert)

### Git reset  
If **git revert** is a **“safe” way** to undo changes, you can think of git reset as the dangerous method.  
When you undo with git reset(and the commits are no longer referenced by any ref or the reflog), there is no way to retrieve the original copy—it is a permanent undo.  
Care must be taken when using this tool, as it’s one of the only Git commands that has the potential to lose your work.

###Reverting vs. Resetting
It's important to understand that git revert undoes a single commit—it does not "revert" back to the previous state of a project by removing all subsequent commits.  
In Git, this is actually called a reset, not a revert.

### Git Revert
The git revert command undoes a committed snapshot. But, instead of removing the commit from the project history, it figures out how to undo the changes introduced by the commit and appends a new commit with the resulting content.  
This prevents Git from losing history, which is important for the integrity of your revision history and for reliable collaboration.
You can check your commit number typing this following command 
```
$ git log
```
Then, you can excute git revert command typing these commands  
```
$ git revert <commit>
```  
or  
```
$ git revert HEAD
```  

Reference - [git revert command](https://www.atlassian.com/git/tutorials/undoing-changes)
