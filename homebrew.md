## Errors

When I was trying to install mysql I had `ERROR 2002 MYSQL socket /tmp/mysql.sock`

The solution came by giving more access to user:
```bash
sudo chown -R "$USER":admin /usr/local
sudo chown -R "$USER":admin /Library/Caches
```
https://stackoverflow.com/questions/16432071/how-to-fix-homebrew-permissions
