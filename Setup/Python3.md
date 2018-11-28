# python3 安装

`brew install python3`

```bash
==> Installing dependencies for python: openssl and xz
==> Installing python dependency: openssl
==> Downloading https://homebrew.bintray.com/bottles/openssl-1.0.2q.mojave.bottle.tar.gz
######################################################################## 100.0%
==> Pouring openssl-1.0.2q.mojave.bottle.tar.gz
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
🍺  /usr/local/Cellar/openssl/1.0.2q: 1,794 files, 12.1MB
==> Installing python dependency: xz
==> Downloading https://homebrew.bintray.com/bottles/xz-5.2.4.mojave.bottle.tar.gz
######################################################################## 100.0%
==> Pouring xz-5.2.4.mojave.bottle.tar.gz
🍺  /usr/local/Cellar/xz/5.2.4: 92 files, 1MB
==> Installing python
==> Downloading https://homebrew.bintray.com/bottles/python-3.7.1.mojave.bottle.tar.gz
######################################################################## 100.0%
==> Pouring python-3.7.1.mojave.bottle.tar.gz
==> /usr/local/Cellar/python/3.7.1/bin/python3 -s setup.py --no-user-cfg install --force --verbose --install-scripts=/usr/local/Cellar/python/3.7.1/bin --install-lib=/usr/local/lib/python3.7/site-packages --single-version-externally-manag
==> /usr/local/Cellar/python/3.7.1/bin/python3 -s setup.py --no-user-cfg install --force --verbose --install-scripts=/usr/local/Cellar/python/3.7.1/bin --install-lib=/usr/local/lib/python3.7/site-packages --single-version-externally-manag
==> /usr/local/Cellar/python/3.7.1/bin/python3 -s setup.py --no-user-cfg install --force --verbose --install-scripts=/usr/local/Cellar/python/3.7.1/bin --install-lib=/usr/local/lib/python3.7/site-packages --single-version-externally-manag
==> Caveats
Python has been installed as
  /usr/local/bin/python3

Unversioned symlinks `python`, `python-config`, `pip` etc. pointing to
`python3`, `python3-config`, `pip3` etc., respectively, have been installed into
  /usr/local/opt/python/libexec/bin

If you need Homebrew's Python 2.7 run
  brew install python@2

You can install Python packages with
  pip3 install <package>
They will install into the site-package directory
  /usr/local/lib/python3.7/site-packages

See: https://docs.brew.sh/Homebrew-and-Python
==> Summary
🍺  /usr/local/Cellar/python/3.7.1: 3,820 files, 59.2MB
==> Caveats
==> openssl
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

==> python
Python has been installed as
  /usr/local/bin/python3

Unversioned symlinks `python`, `python-config`, `pip` etc. pointing to
`python3`, `python3-config`, `pip3` etc., respectively, have been installed into
  /usr/local/opt/python/libexec/bin

If you need Homebrew's Python 2.7 run
  brew install python@2

You can install Python packages with
  pip3 install <package>
They will install into the site-package directory
  /usr/local/lib/python3.7/site-packages

See: https://docs.brew.sh/Homebrew-and-Python
```
