## Install
```bash
brew update
brew install php
brew link php --force
```
To use `php` from brew instead of the default one:
```
echo 'export PATH="/usr/local/opt/php/bin:$PATH"' >> ~/.zshrc
echo 'export PATH="/usr/local/opt/php/sbin:$PATH"' >> ~/.zshrc
```

### Xdebug
```bash
pecl install xdebug
```
If `Failed loading xdebug.so`, add a symolic link with :
```
ln -s [where the file is] [where it should be]
```
