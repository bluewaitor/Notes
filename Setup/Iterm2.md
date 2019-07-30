# iterm2 安装

`brew cask install iterm2`

- 设置iterm2的显示位置

> `Preferences->Profile->Default->Window->Style->Full-Width Top of Screen`

- 设置iterm2的透明度  

> `Preferences->Profile->Default->Window->Transparency`

- 设置显示/隐藏iterm2的快捷键  

> `Preferences->Keys->Hotkey->Show/hide all windows with a system-wide hotkey->cmd+i`

## 添加oh-my-zsh

`sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

```bash
Cloning Oh My Zsh...
Cloning into '/Users/blue/.oh-my-zsh'...
remote: Enumerating objects: 970, done.
remote: Counting objects: 100% (970/970), done.
remote: Compressing objects: 100% (870/870), done.
remote: Total 970 (delta 26), reused 793 (delta 18), pack-reused 0
Receiving objects: 100% (970/970), 633.25 KiB | 29.00 KiB/s, done.
Resolving deltas: 100% (26/26), done.
Looking for an existing zsh config...
Using the Oh My Zsh template file and adding it to ~/.zshrc
Time to change your default shell to zsh!
Changing shell for blue.
Password for blue:
         __                                     __
  ____  / /_     ____ ___  __  __   ____  _____/ /_
 / __ \/ __ \   / __ `__ \/ / / /  /_  / / ___/ __ \
/ /_/ / / / /  / / / / / / /_/ /    / /_(__  ) / / /
\____/_/ /_/  /_/ /_/ /_/\__, /    /___/____/_/ /_/
                        /____/                       ....is now installed!


Please look over the ~/.zshrc file to select plugins, themes, and options.

p.s. Follow us at https://twitter.com/ohmyzsh.

p.p.s. Get stickers and t-shirts at https://shop.planetargon.com.
```

## 安装antigen

`brew install antigen`

```bash
==> Downloading https://github.com/zsh-users/antigen/releases/download/v2.2.3/v2.2.3.tar.gz
Already downloaded: /Users/blue/Library/Caches/Homebrew/downloads/10098bb80b0c20c8e50edce8fabff39fc0a45c4ddd57c63964a9427204a213de--v2.2.3.tar.gz
==> Caveats
To activate antigen, add the following to your ~/.zshrc:
  source /usr/local/share/antigen/antigen.zsh
==> Summary
🍺  /usr/local/Cellar/antigen/2.2.3: 5 files, 79.7KB, built in 1 second
```

要使antigen生效，需要执行  
`source /usr/local/share/antigen/antigen.zsh`
