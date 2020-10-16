Log:

```console
% git init
Initialized empty Git repository in /home/taiki/dev/src/github.com/buzztaiki/whichis-gh-initial-default-branch/.git/

% touch .gitignore && git add .gitignore

% git commit -m 'first commit'
[master (root-commit) 3795f99] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 .gitignore

% git branch
* master

% git branch -M oreno

% git branch
* oreno

% gh repo create $(basename $(pwd)) --public --confirm
✓ Created repository buzztaiki/whichis-gh-initial-default-branch on GitHub
✓ Added remote git@github.com:buzztaiki/whichis-gh-initial-default-branch.git

% git remote -v
origin  git@github.com:buzztaiki/whichis-gh-initial-default-branch.git (fetch)
origin  git@github.com:buzztaiki/whichis-gh-initial-default-branch.git (push)

% git push -u origin oreno
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 218 bytes | 218.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:buzztaiki/whichis-gh-initial-default-branch.git
 * [new branch]      oreno -> oreno
Branch 'oreno' set up to track remote branch 'oreno' from 'origin'.

% gh api /repos/:owner/:repo | jq '.default_branch'
"oreno"
```
