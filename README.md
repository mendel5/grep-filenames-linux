# grep-filenames-linux

```
$ find . -type f | grep -i '[^a-z0-9\.\/_ ,()\-]'
```


Links:
- https://stackoverflow.com/questions/19008614/find-files-with-illegal-windows-characters-in-the-name-on-linux
- https://serverfault.com/questions/348482/how-to-remove-invalid-characters-from-filenames/871184#871184 - detox
- https://askubuntu.com/questions/113188/character-encoding-problem-with-filenames-find-broken-filenames
- https://stackoverflow.com/questions/623764/find-non-utf8-filenames-on-linux-file-system
- https://serverfault.com/questions/805621/how-can-i-find-all-files-in-a-directory-with-illegal-characters-in-the-file-name
- https://moredvikas.wordpress.com/2016/05/05/sharepoint-file-names-cant-contain-the-following-characters/
