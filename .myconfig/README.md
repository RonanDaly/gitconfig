# gitconfig
## First clone the repoistory
### If we can push
```
git clone --separate-git-dir=$HOME/.myconfig git@github.com:RonanDaly/gitconfig.git myconfig-tmp
```

### If we can't
```
git clone --separate-git-dir=$HOME/.myconfig https://github.com/RonanDaly/gitconfig.git myconfig-tmp

```

## Then setup
```
cd myconfig-tmp
find . -type f -not -path '*/.git/*' -exec cp "{}" "$HOME/{}" \;
cd ..
rm -r myconfig-tmp
alias config='git --git-dir=$HOME/.myconfig/ --work-tree=$HOME'
config config status.showUntrackedFiles no
```



