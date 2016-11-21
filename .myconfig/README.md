# gitconfig

```
git clone --separate-git-dir=$HOME/.myconfig git@github.com:RonanDaly/gitconfig.git myconfig-tmp
find myconfig-tmp -type f -not -path '*/.git/*' -exec cp --parents '{}' $HOME \;
rm --recursive myconfig-tmp
alias config='git --git-dir=$HOME/.myconfig/ --work-tree=$HOME'
config config status.showUntrackedFiles no
```
