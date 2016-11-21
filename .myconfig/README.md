# gitconfig

```
git clone --separate-git-dir=$HOME/.myconfig git@github.com:RonanDaly/gitconfig.git myconfig-tmp
cd myconfig-tmp
find . -type f -not -path '*/.git/*' -exec cp "{}" "$HOME/{}" \;
cd ..
rm -r myconfig-tmp
alias config='git --git-dir=$HOME/.myconfig/ --work-tree=$HOME'
config config status.showUntrackedFiles no
```
