# devenv
開発環境に関して、広く記載します。
狙いは、新しい開発環境を作る時の手間を減らすことです。

## git commands alias
#### コマンド
```
git config --global alias.commit co
git config --global alias.branch br
git config --global alias.status st
git config --global alias.fetch fe
git config --global alias.pull pu
```

#### .gitconfig
```
[alias]
        co = checkout
        st = status
        br = branch
        fetch = fe
        pull = pu
        brdel = "branch --delete"
```

## git-completion
#### インストール
```
mkdir ~/.zsh
cd ~/.zsh

curl -o git-completion.bash https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash
curl -o _git https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.zsh
```

#### セットアップ
.zshrcに追記
```
# git-completionの読み込み
fpath=(~/.zsh $fpath)
zstyle ':completion:*:*:git:*' script ~/.zsh/git-completion.bash
autoload -Uz compinit && compinit
```
