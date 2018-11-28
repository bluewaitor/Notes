# Homebrew 安装

[Homebrew官网](https://brew.sh/)

使用命令：
`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

出现提示：

```bash
==> This script will install:
/usr/local/bin/brew
/usr/local/share/doc/homebrew
/usr/local/share/man/man1/brew.1
/usr/local/share/zsh/site-functions/_brew
/usr/local/etc/bash_completion.d/brew
/usr/local/Homebrew
==> The following new directories will be created:
/usr/local/bin
/usr/local/etc
/usr/local/include
/usr/local/lib
/usr/local/sbin
/usr/local/share
/usr/local/var
/usr/local/opt
/usr/local/share/zsh
/usr/local/share/zsh/site-functions
/usr/local/var/homebrew
/usr/local/var/homebrew/linked
/usr/local/Cellar
/usr/local/Caskroom
/usr/local/Homebrew
/usr/local/Frameworks
==> The Xcode Command Line Tools will be installed.

Press RETURN to continue or any other key to abort
```

按下回车继续安装

```bash
==> /usr/bin/sudo /bin/mkdir -p /usr/local/bin /usr/local/etc /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/share /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
Password:
==> /usr/bin/sudo /bin/chmod g+rwx /usr/local/bin /usr/local/etc /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/share /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
==> /usr/bin/sudo /bin/chmod 755 /usr/local/share/zsh /usr/local/share/zsh/site-functions
==> /usr/bin/sudo /usr/sbin/chown blue /usr/local/bin /usr/local/etc /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/share /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
==> /usr/bin/sudo /usr/bin/chgrp admin /usr/local/bin /usr/local/etc /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/share /usr/local/var /usr/local/opt /usr/local/share/zsh /usr/local/share/zsh/site-functions /usr/local/var/homebrew /usr/local/var/homebrew/linked /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
==> /usr/bin/sudo /bin/mkdir -p /Users/blue/Library/Caches/Homebrew
==> /usr/bin/sudo /bin/chmod g+rwx /Users/blue/Library/Caches/Homebrew
==> /usr/bin/sudo /usr/sbin/chown blue /Users/blue/Library/Caches/Homebrew
==> /usr/bin/sudo /bin/mkdir -p /Library/Caches/Homebrew
==> /usr/bin/sudo /bin/chmod g+rwx /Library/Caches/Homebrew
==> /usr/bin/sudo /usr/sbin/chown blue /Library/Caches/Homebrew
==> Searching online for the Command Line Tools
==> /usr/bin/sudo /usr/bin/touch /tmp/.com.apple.dt.CommandLineTools.installondemand.in-progress
==> Installing Command Line Tools (macOS High Sierra version 10.13) for Xcode-10.0
==> /usr/bin/sudo /usr/sbin/softwareupdate -i Command\ Line\ Tools\ (macOS\ High\ Sierra\ version\ 10.13)\ for\ Xcode-10.0
Software Update Tool


Downloading Command Line Tools (macOS High Sierra version 10.13) for Xcode
```

```bash
Installing Command Line Tools (macOS High Sierra version 10.13) for Xcode
Done with Command Line Tools (macOS High Sierra version 10.13) for Xcode
Done.
==> /usr/bin/sudo /bin/rm -f /tmp/.com.apple.dt.CommandLineTools.installondemand.in-progress
Password:
Sorry, try again.
Password:
==> /usr/bin/sudo /usr/bin/xcode-select --switch /Library/Developer/CommandLineTools
==> Downloading and installing Homebrew...
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
Receiving objects:  26% (29744/113116), 8.66 MiB | 140.00 KiB/s

remote: Total 113116 (delta 0), reused 1 (delta 0), pack-reused 113115
Receiving objects: 100% (113116/113116), 26.02 MiB | 166.00 KiB/s, done.
Resolving deltas: 100% (82735/82735), done.
From https://github.com/Homebrew/brew
 * [new branch]          master     -> origin/master
 * [new tag]             0.1        -> 0.1
 * [new tag]             0.2        -> 0.2
 * [new tag]             0.3        -> 0.3
 * [new tag]             0.4        -> 0.4
 * [new tag]             0.5        -> 0.5
 * [new tag]             0.6        -> 0.6
 * [new tag]             0.7        -> 0.7
 * [new tag]             0.7.1      -> 0.7.1
 * [new tag]             0.8        -> 0.8
 * [new tag]             0.8.1      -> 0.8.1
 * [new tag]             0.9        -> 0.9
 * [new tag]             0.9.1      -> 0.9.1
 * [new tag]             0.9.2      -> 0.9.2
 * [new tag]             0.9.3      -> 0.9.3
 * [new tag]             0.9.4      -> 0.9.4
 * [new tag]             0.9.5      -> 0.9.5
 * [new tag]             0.9.8      -> 0.9.8
 * [new tag]             0.9.9      -> 0.9.9
 * [new tag]             1.0.0      -> 1.0.0
 * [new tag]             1.0.1      -> 1.0.1
 * [new tag]             1.0.2      -> 1.0.2
 * [new tag]             1.0.3      -> 1.0.3
 * [new tag]             1.0.4      -> 1.0.4
 * [new tag]             1.0.5      -> 1.0.5
 * [new tag]             1.0.6      -> 1.0.6
 * [new tag]             1.0.7      -> 1.0.7
 * [new tag]             1.0.8      -> 1.0.8
 * [new tag]             1.0.9      -> 1.0.9
 * [new tag]             1.1.0      -> 1.1.0
 * [new tag]             1.1.1      -> 1.1.1
 * [new tag]             1.1.10     -> 1.1.10
 * [new tag]             1.1.11     -> 1.1.11
 * [new tag]             1.1.12     -> 1.1.12
 * [new tag]             1.1.13     -> 1.1.13
 * [new tag]             1.1.2      -> 1.1.2
 * [new tag]             1.1.3      -> 1.1.3
 * [new tag]             1.1.4      -> 1.1.4
 * [new tag]             1.1.5      -> 1.1.5
 * [new tag]             1.1.6      -> 1.1.6
 * [new tag]             1.1.7      -> 1.1.7
 * [new tag]             1.1.8      -> 1.1.8
 * [new tag]             1.1.9      -> 1.1.9
 * [new tag]             1.2.0      -> 1.2.0
 * [new tag]             1.2.1      -> 1.2.1
 * [new tag]             1.2.2      -> 1.2.2
 * [new tag]             1.2.3      -> 1.2.3
 * [new tag]             1.2.4      -> 1.2.4
 * [new tag]             1.2.5      -> 1.2.5
 * [new tag]             1.2.6      -> 1.2.6
 * [new tag]             1.3.0      -> 1.3.0
 * [new tag]             1.3.1      -> 1.3.1
 * [new tag]             1.3.2      -> 1.3.2
 * [new tag]             1.3.3      -> 1.3.3
 * [new tag]             1.3.4      -> 1.3.4
 * [new tag]             1.3.5      -> 1.3.5
 * [new tag]             1.3.6      -> 1.3.6
 * [new tag]             1.3.7      -> 1.3.7
 * [new tag]             1.3.8      -> 1.3.8
 * [new tag]             1.3.9      -> 1.3.9
 * [new tag]             1.4.0      -> 1.4.0
 * [new tag]             1.4.1      -> 1.4.1
 * [new tag]             1.4.2      -> 1.4.2
 * [new tag]             1.4.3      -> 1.4.3
 * [new tag]             1.5.0      -> 1.5.0
 * [new tag]             1.5.1      -> 1.5.1
 * [new tag]             1.5.10     -> 1.5.10
 * [new tag]             1.5.11     -> 1.5.11
 * [new tag]             1.5.12     -> 1.5.12
 * [new tag]             1.5.13     -> 1.5.13
 * [new tag]             1.5.14     -> 1.5.14
 * [new tag]             1.5.2      -> 1.5.2
 * [new tag]             1.5.3      -> 1.5.3
 * [new tag]             1.5.4      -> 1.5.4
 * [new tag]             1.5.5      -> 1.5.5
 * [new tag]             1.5.6      -> 1.5.6
 * [new tag]             1.5.7      -> 1.5.7
 * [new tag]             1.5.8      -> 1.5.8
 * [new tag]             1.5.9      -> 1.5.9
 * [new tag]             1.6.0      -> 1.6.0
 * [new tag]             1.6.1      -> 1.6.1
 * [new tag]             1.6.10     -> 1.6.10
 * [new tag]             1.6.11     -> 1.6.11
 * [new tag]             1.6.12     -> 1.6.12
 * [new tag]             1.6.13     -> 1.6.13
 * [new tag]             1.6.14     -> 1.6.14
 * [new tag]             1.6.15     -> 1.6.15
 * [new tag]             1.6.16     -> 1.6.16
 * [new tag]             1.6.17     -> 1.6.17
 * [new tag]             1.6.2      -> 1.6.2
 * [new tag]             1.6.3      -> 1.6.3
 * [new tag]             1.6.4      -> 1.6.4
 * [new tag]             1.6.5      -> 1.6.5
 * [new tag]             1.6.6      -> 1.6.6
 * [new tag]             1.6.7      -> 1.6.7
 * [new tag]             1.6.8      -> 1.6.8
 * [new tag]             1.6.9      -> 1.6.9
 * [new tag]             1.7.0      -> 1.7.0
 * [new tag]             1.7.1      -> 1.7.1
 * [new tag]             1.7.2      -> 1.7.2
 * [new tag]             1.7.3      -> 1.7.3
 * [new tag]             1.7.4      -> 1.7.4
 * [new tag]             1.7.5      -> 1.7.5
 * [new tag]             1.7.6      -> 1.7.6
 * [new tag]             1.7.7      -> 1.7.7
HEAD is now at fdd8e9b7c Merge pull request #5148 from MikeMcQuaid/travis-only-macos
==> Downloading https://homebrew.bintray.com/bottles-portable-ruby/portable-ruby-2.3.7.leopard_64.bottle.tar.gz
######################################################################## 100.0%
==> Pouring portable-ruby-2.3.7.leopard_64.bottle.tar.gz
==> Homebrew is run entirely by unpaid volunteers. Please consider donating:
  https://github.com/Homebrew/brew#donations
==> Tapping homebrew/core
Cloning into '/usr/local/Homebrew/Library/Taps/homebrew/homebrew-core'...
remote: Enumerating objects: 4858, done.
remote: Counting objects: 100% (4858/4858), done.
remote: Compressing objects: 100% (4656/4656), done.
remote: Total 4858 (delta 57), reused 323 (delta 12), pack-reused 0
Receiving objects: 100% (4858/4858), 4.05 MiB | 21.00 KiB/s, done.
Resolving deltas: 100% (57/57), done.
Tapped 2 commands and 4644 formulae (4,900 files, 12.6MB).
==> Migrating /Library/Caches/Homebrew to /Users/blue/Library/Caches/Homebrew...
==> Deleting /Library/Caches/Homebrew...
Already up-to-date.
==> Installation successful!

==> Homebrew has enabled anonymous aggregate formulae and cask analytics.
Read the analytics documentation (and how to opt-out) here:
  https://docs.brew.sh/Analytics.html

==> Homebrew is run entirely by unpaid volunteers. Please consider donating:
  https://github.com/Homebrew/brew#donations
==> Next steps:
- Run `brew help` to get started
- Further documentation:
    https://docs.brew.sh
```

安装完之后就可以使用`brew`这个命令了
