# Java 安装

`brew cask install java`

```bash
Updating Homebrew...
==> Auto-updated Homebrew!
Updated 2 taps (homebrew/core and homebrew/cask).
==> New Formulae
aom                                                                             astrometry-net                                                                  minica
==> Updated Formulae
ansible-cmdb              crosstool-ng              faas-cli                  jdnssec-tools             mpich                     pandoc                    pgroonga                  php@7.1                   sourcekitten
cayley                    davix                     haskell-stack             lcm                       nghttp2                   pcl                       php@5.6                   pygobject3                swift
cockroach                 elasticsearch             jbig2dec                  logstash                  nginx                     pdal                      php@7.0                   sdcc                      zsh-autosuggestions

==> Satisfying dependencies
==> Downloading https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_osx-x64_bin.tar.gz
######################################################################## 100.0%
==> Verifying SHA-256 checksum for Cask 'java'.
==> Installing Cask java
Password:
🍺  java was successfully installed!
```

`brew cask install homebrew/cask-versions/java8`

```bash
➜  ~ brew cask install homebrew/cask-versions/java8
==> Tapping homebrew/cask-versions
Cloning into '/usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask-versions'...
remote: Enumerating objects: 230, done.
remote: Counting objects: 100% (230/230), done.
remote: Compressing objects: 100% (223/223), done.
remote: Total 230 (delta 14), reused 46 (delta 5), pack-reused 0
Receiving objects: 100% (230/230), 92.57 KiB | 202.00 KiB/s, done.
Resolving deltas: 100% (14/14), done.
Tapped 209 casks (250 files, 351.3KB).
==> Caveats
This Cask makes minor modifications to the JRE to prevent issues with
packaged applications, as discussed here:

  https://bugs.eclipse.org/bugs/show_bug.cgi?id=411361

If your Java application still asks for JRE installation, you might need
to reboot or logout/login.

Installing java8 means you have AGREED to the license at
  https://www.oracle.com/technetwork/java/javase/terms/license/index.html

==> Satisfying dependencies
==> Downloading https://download.oracle.com/otn-pub/java/jdk/8u192-b12/750e1c8617c5452694857ad95c3ee230/jdk-8u192-macosx-x64.dmg
==> Downloading from https://download.oracle.com/otn-pub/java/jdk/8u192-b12/750e1c8617c5452694857ad95c3ee230/jdk-8u192-macosx-x64.dmg?AuthParam=1543979248_698b3569894d9718c0ebc5d67c9bb680
######################################################################## 100.0%
==> Verifying SHA-256 checksum for Cask 'java8'.
==> Installing Cask java8
==> Running installer for java8; your password may be necessary.
==> Package installers may write to any location; options such as --appdir are ignored.
Password:
installer: Package name is JDK 8 Update 192
installer: Installing at base path /
installer: The install was successful.
🍺  java8 was successfully installed!
```
