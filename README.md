# learngit-branching
https://learngitbranching.js.org/

![image](https://github.com/user-attachments/assets/edfa57c2-23c1-4b48-80fc-29ad86e13603)


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

![image](https://github.com/user-attachments/assets/8c1331fa-c935-4f1d-990f-9509025e2e15)



# Remote
### 1.1 Clone Intro
```
git clone
```
### 1.2 Remote Branches
```
git commit
git checkout o/main
git commit
```
### 1.3 Git Fetchin'
```
git fetch
```
### 1.4 Git Pullin'
```
git pull
```
### 1.5 Faking Teamwork
```
git clone
git fakeTeamwork main 2
git commit
git pull
```
### 1.6 Git Pushin'
```
git commit
git commit
git push
```
### 1.7 Diverged History
```
git clone
git fakeTeamwork main 1
git commit
git pull --rebase
git push
```
### 1.8 Locked Main
```
git branch -f main o/main
git checkout -b feature C2
git push origin feature
```
### 2.1 Push Main!
```
git checkout main
git pull --rebase
git checkout side1
git rebase C8
git checkout side2
git rebase side1
git checkout side3
git rebase side2
git branch -f main side3
git checkout main
git push
```
### 2.2 Merging with remotes
```
git fetch
git branch -f main C8
git checkout main
git merge side1
git merge side2
git merge side3
git push
```
### 2.3 Remote Tracking
```
git checkout -b side o/main
git commit
git pull --rebase
git push
```
### 2.4 Git push arguments
```
git push origin foo
git push origin main
```
### 2.5 Git push arguments -- Expanded!
```
git push origin foo:main
git push origin HEAD^:foo
```
### 2.6 Fetch arguments
```
git fetch origin C6:main
git fetch origin C3:foo
git checkout foo
git merge main
```
### 2.7 Source of nothing
```
git push origin :foo
git fetch origin :bar
```
### 2.8 Pull arguments
```
git fetch origin C3:foo
git fetch origin C2:side
git merge foo
git merge side
```
