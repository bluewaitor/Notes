# Node 安装

`brew install node`

```bash
Updating Homebrew...
==> Installing dependencies for node: icu4c
==> Installing node dependency: icu4c
==> Downloading https://homebrew.bintray.com/bottles/icu4c-62.1.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring icu4c-62.1.high_sierra.bottle.tar.gz
==> Caveats
icu4c is keg-only, which means it was not symlinked into /usr/local,
because macOS provides libicucore.dylib (but nothing else).

If you need to have icu4c first in your PATH run:
  echo 'export PATH="/usr/local/opt/icu4c/bin:$PATH"' >> ~/.zshrc
  echo 'export PATH="/usr/local/opt/icu4c/sbin:$PATH"' >> ~/.zshrc

For compilers to find icu4c you may need to set:
  export LDFLAGS="-L/usr/local/opt/icu4c/lib"
  export CPPFLAGS="-I/usr/local/opt/icu4c/include"

==> Summary
🍺  /usr/local/Cellar/icu4c/62.1: 250 files, 67.3MB
==> Installing node
==> Downloading https://homebrew.bintray.com/bottles/node-10.12.0.high_sierra.bottle.tar.gz
###################################################################       93.7%
curl: (56) LibreSSL SSL_read: SSL_ERROR_SYSCALL, errno 54
Error: Failed to download resource "node"
Download failed: https://homebrew.bintray.com/bottles/node-10.12.0.high_sierra.bottle.tar.gz
Warning: Bottle installation failed: building from source.
==> Installing dependencies for node: pkg-config, gdbm, openssl, readline, sqlite and python@2
==> Installing node dependency: pkg-config
==> Downloading https://homebrew.bintray.com/bottles/pkg-config-0.29.2.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring pkg-config-0.29.2.high_sierra.bottle.tar.gz
🍺  /usr/local/Cellar/pkg-config/0.29.2: 11 files, 627.2KB
==> Installing node dependency: gdbm
==> Downloading https://homebrew.bintray.com/bottles/gdbm-1.18.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring gdbm-1.18.high_sierra.bottle.tar.gz
🍺  /usr/local/Cellar/gdbm/1.18: 20 files, 584.4KB
==> Installing node dependency: openssl
==> Downloading https://homebrew.bintray.com/bottles/openssl-1.0.2p.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring openssl-1.0.2p.high_sierra.bottle.tar.gz
==> Caveats
A CA file has been bootstrapped using certificates from the SystemRoots
keychain. To add additional certificates (e.g. the certificates added in
the System keychain), place .pem files in
  /usr/local/etc/openssl/certs

and run
  /usr/local/opt/openssl/bin/c_rehash

openssl is keg-only, which means it was not symlinked into /usr/local,
because Apple has deprecated use of OpenSSL in favor of its own TLS and crypto libraries.

If you need to have openssl first in your PATH run:
  echo 'export PATH="/usr/local/opt/openssl/bin:$PATH"' >> ~/.zshrc

For compilers to find openssl you may need to set:
  export LDFLAGS="-L/usr/local/opt/openssl/lib"
  export CPPFLAGS="-I/usr/local/opt/openssl/include"

For pkg-config to find openssl you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/openssl/lib/pkgconfig"

==> Summary
🍺  /usr/local/Cellar/openssl/1.0.2p: 1,793 files, 12.3MB
==> Installing node dependency: readline
==> Downloading https://homebrew.bintray.com/bottles/readline-7.0.5.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring readline-7.0.5.high_sierra.bottle.tar.gz
==> Caveats
readline is keg-only, which means it was not symlinked into /usr/local,
because macOS provides the BSD libedit library, which shadows libreadline.
In order to prevent conflicts when programs look for libreadline we are
defaulting this GNU Readline installation to keg-only.

For compilers to find readline you may need to set:
  export LDFLAGS="-L/usr/local/opt/readline/lib"
  export CPPFLAGS="-I/usr/local/opt/readline/include"

==> Summary
🍺  /usr/local/Cellar/readline/7.0.5: 46 files, 1.5MB
==> Installing node dependency: sqlite
==> Downloading https://homebrew.bintray.com/bottles/sqlite-3.25.2.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring sqlite-3.25.2.high_sierra.bottle.tar.gz
==> Caveats
sqlite is keg-only, which means it was not symlinked into /usr/local,
because macOS provides an older sqlite3.

If you need to have sqlite first in your PATH run:
  echo 'export PATH="/usr/local/opt/sqlite/bin:$PATH"' >> ~/.zshrc

For compilers to find sqlite you may need to set:
  export LDFLAGS="-L/usr/local/opt/sqlite/lib"
  export CPPFLAGS="-I/usr/local/opt/sqlite/include"

For pkg-config to find sqlite you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/sqlite/lib/pkgconfig"

==> Summary
🍺  /usr/local/Cellar/sqlite/3.25.2: 11 files, 3.7MB
==> Installing node dependency: python@2
==> Downloading https://homebrew.bintray.com/bottles/python@2-2.7.15_1.high_sierra.bottle.6.tar.gz
######################################################################## 100.0%
==> Pouring python@2-2.7.15_1.high_sierra.bottle.6.tar.gz
==> /usr/local/Cellar/python@2/2.7.15_1/bin/python -s setup.py --no-user-cfg install --force --verbose --single-version-externally-managed --record=installed.txt --install-scripts=/usr/local/Cellar/python@2/2.7.15_1/bin --install-lib=/usr
==> /usr/local/Cellar/python@2/2.7.15_1/bin/python -s setup.py --no-user-cfg install --force --verbose --single-version-externally-managed --record=installed.txt --install-scripts=/usr/local/Cellar/python@2/2.7.15_1/bin --install-lib=/usr
==> /usr/local/Cellar/python@2/2.7.15_1/bin/python -s setup.py --no-user-cfg install --force --verbose --single-version-externally-managed --record=installed.txt --install-scripts=/usr/local/Cellar/python@2/2.7.15_1/bin --install-lib=/usr
==> Caveats
Pip and setuptools have been installed. To update them
  pip install --upgrade pip setuptools

You can install Python packages with
  pip install <package>

They will install into the site-package directory
  /usr/local/lib/python2.7/site-packages

See: https://docs.brew.sh/Homebrew-and-Python
==> Summary
🍺  /usr/local/Cellar/python@2/2.7.15_1: 4,665 files, 82.6MB
==> Downloading https://nodejs.org/dist/v10.12.0/node-v10.12.0.tar.gz
######################################################################## 100.0%
==> ./configure --prefix=/usr/local/Cellar/node/10.12.0 --without-npm --with-intl=system-icu
==> make install


Updating Homebrew...
==> Downloading https://homebrew.bintray.com/bottles/node-10.12.0.high_sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring node-10.12.0.high_sierra.bottle.tar.gz
==> Caveats
Bash completion has been installed to:
  /usr/local/etc/bash_completion.d
==> Summary
🍺  /usr/local/Cellar/node/10.12.0: 3,939 files, 46.6MB
```

# nvm
```bash
Updating Homebrew...
==> Auto-updated Homebrew!
Updated 1 tap (homebrew/cask).
No changes to formulae.

==> Downloading https://github.com/creationix/nvm/archive/v0.34.0.tar.gz
==> Downloading from https://codeload.github.com/nvm-sh/nvm/tar.gz/v0.34.0
######################################################################## 100.0%
==> Caveats
Please note that upstream has asked us to make explicit managing
nvm via Homebrew is unsupported by them and you should check any
problems against the standard nvm install method prior to reporting.

You should create NVM's working directory if it doesn't exist:

  mkdir ~/.nvm

Add the following to ~/.zshrc or your desired shell
configuration file:

  export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/usr/local/opt/nvm/etc/bash_completion" ] && . "/usr/local/opt/nvm/etc/bash_completion"  # This loads nvm bash_completion

You can set $NVM_DIR to any location, but leaving it unchanged from
/usr/local/opt/nvm will destroy any nvm-installed Node installations
upon upgrade/reinstall.

Type `nvm help` for further information.

Bash completion has been installed to:
  /usr/local/etc/bash_completion.d
==> Summary
🍺  /usr/local/Cellar/nvm/0.34.0: 7 files, 141.7KB, built in 12 seconds
```

`mkdir ~/.nvm`  
`vim ~/.zshrc`  

将这些配置添加到zshrc中  
```
  export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/usr/local/opt/nvm/etc/bash_completion" ] && . "/usr/local/opt/nvm/etc/bash_completion"  # This loads nvm bash_completion
```
