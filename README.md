# Submodules
Submodules are repositories referenced in a different repository. In this training
this repository will be referenced as `parent`. The `submodules` will be referenced
as `dependency`.

## Adding a submodule
Add a submodule:
`git submodule add [repository]`

Commit your newly added submodule:

```
git add .
git commit
```

## Initializing a repository with submodules
Clone repository:
`git clone [repo]`

Mark an submodule to be initialized:
`git submodule init [submodule]`

Mark all submodules to be initialized:
`git submodule init`

Clone and initialize all submodules:
`git clone [repo] --recursive`

## Detached HEAD
- every commit is a change set based on a different commit, the parent commit
- a branch is a dynamic label that points to a specific commit
- a tag is a static label that points to a specific commit
- a detached HEAD is a checked out commit without a label

You can always `apply a label` on a `detached HEAD`:
`git checkout -b <new branch name>`

## Update
Checkout the referenced commit in the `.gitmodules` in a detached HEAD:
`git submodule update`

## reflog
History of your last commits, including all the `detached HEAD` commits:
`git reflog`

## foreach
Run a command for every submodule checked out:
`git submodule foreach 'echo hello $name'`
