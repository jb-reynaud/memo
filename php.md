## Install
```bash
brew update
brew install php
brew link php --force
```

### Xdebug
```bash
pecl install xdebug
```
If `Failed loading xdebug.so`, add a symolic link with :
```
ln -s [where the file is] [where it should be]
```
