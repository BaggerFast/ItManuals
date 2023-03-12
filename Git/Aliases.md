## Useful Git aliases
1. Add base aliases
```
git config --global alias.br "branch"
git config --global alias.cim "commit -m"
git config --global alias.cob "checkout -b"
git config --global alias.bra "branch -a -vv"

git config --global alias.pl "pull"
git config --global alias.ph "push"
git config --global alias.cl "clone"
git config --global alias.st "status"

git config --global alias.main "checkout -b main"
git config --global alias.dev "checkout -b develop"

git config --global alias.aliases "config --get-regexp ^alias" 
```
2. Delete aliases 
```
git config --global --unset alias.name
```