# learngit-branching
https://learngitbranching.js.org/


# Main

### 1.1 Introduction to Git Commits
```
git commit
git commit
```
### 1.2 Branching in Git
```
git branch bugFix
git checkout bugFix
```
### 1.3 Merging in Git
```
git checkout -b bugFix
git commit
git checkout main
git commit
git merge bugFix
```
### 1.4 Rebase Introduction
```
git branch bugFix
git checkout bugFix
git commit
git checkout main
git commit
git rebase main bugFix
```

### 2.1 Detach yo' HEAD
```
git checkout C4
```
### 2.2 Relative Refs (^)
```
git checkout HEAD^
```
### 2.3 Relative Refs #2 (~)
```
git branch -f bugFix C0
git branch -f main C6
git checkout C1
```
### 2.4 Reversing Changes in Git
```
git reset C1
git checkout pushed
git revert pushed
```

### 3.1 Cherry-pick Intro
```
git cherry-pick C3 C4 C7
```
### 3.2 Interactive Rebase Intro
```
git rebase -i C1
(remove C2 and change C4/C5)
```

### 4.1 Grabbing Just 1 Commit
```
git checkout main
git cherry-pick C4
```

### 4.2 Juggling Commits
```
git rebase -i main
(change C2 and C3)
git commit --amend
git rebase -i main
(change C2 and C3)
git branch -f main caption

```
### 4.3 Juggling Commits #2
```
git checkout main
git cherry-pick C2
git commit --amend
git cherry-pick C3
```
### 4.4 Git Tags
```
git tag v0 C1
git checkout C2
git tag v1
```
### 4.5 Git Describe
```
git describe main
git describe side
git describe bugFix
git commit
```

### 5.1 Rebasing over 9000 times
```
git rebase main bugFix
git rebase bugFix side
git rebase side another
git branch -f main another
```
### 5.2 Multiple parents
```
git branch bugWork main~^2~1
```
### 5.3 Branch Spaghetti
```
git checkout one
git cherry-pick C4 C3 C2
git checkout two
git cherry-pick C5 C4 C3 C2
git checkout two
git branch -f three c2
```


# Remote
### 1.1 Clone Intro
```
test
```
### 1.2 Remote Branches
```
test
```
### 1.3 Git Fetchin'
```
test
```
### 1.4 Git Pullin'
```
test
```
### 1.5 Faking Teamwork
```
test
```
### 1.6 Git Pushin'
```
test
```
### 1.7 Diverged History
```
test
```
### 1.8 Locked Main
```
test
```

### 2.1 Push Main!
```
test
```
### 2.2 Merging with remotes
```
test
```
### 2.3 Remote Tracking
```
test
```
### 2.4 Git push arguments
```
test
```
### 2.5 Git push arguments -- Expanded!
```
test
```
### 2.6 Fetch arguments
```
test
```
### 2.7 Source of nothing
```
test
```
### 2.8 Pull arguments
```
test
```
