#### Getting a git repository
- ###### Initializing a Repository in an Existing Directory
```shell
$ git init
```
- ###### Cloning an Existing Repository
```shell
$ git clone [url] [name]
```

#### Recording changes
- ###### File states
Snapshot - particular record of the state of working directory
  - untracked
  - tracked
    - unmodified
    - modified
    - staged

```shell
$ git status
```
- ###### Tracking new files - creating snapshots
```shell
$ git add <file> #tracked & staged to be commited
```
```shell
$ git reset HEAD <file> #unstage file
```
- ###### Viewing changes
```shell
$ git diff #shows exact lines that were changed or removed,  --staged
```
- ###### Commiting changes
Everything in staging area is now commited to the branch, recorded snapshot.
``` shell
$ git commit #-a -m -v
```
- ###### Removing files
```shell
$ git rm # removes from working directory and tracked files(unlike rm)
```
```shell
$ git rm --cached <file> # untracks the file, but keeps in the working directory
```

#### Viewing the commit history
```shell
$ git log # -p --stat --graph --pretty
```
#### Undoing things
```shell
$ git log commit --amend # recommit
```
```shell
$ git reset HEAD <file> # unstage file
```
```shell
$ git checkout -- <file> # revert the file back to the last commit
```
#### Remotes
- ###### Show configured Remotes
```shell
$ git remote [ add [shortname] [url] ]
$ git remote show [remote-name] # get info about remote
```
- ###### Fetch & Pull & Push
```shell
$ git fetch [remote-name] # no merging
```
```shell
$ git pull # merges with the branch which has upstream
```
```shell
$ git push [remote-name] [branch] # release changes
```
