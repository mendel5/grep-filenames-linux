# grep-filenames-linux

```
You cannot use the following characters anywhere in a site name,
in a subsite name, or in a site or Active Directory group name:

Tilde (~)
Number sign (#)
Percent (%)
Ampersand (&)
Asterisk (*)
Braces ({ })
Backslash (\)
Colon (:)
Angle brackets (< >)
Question mark (?)
Slash (/)
Plus sign (+)
Pipe (|)
Quotation mark (“)

---

Very strict (Whitelist):
find . -type f | grep -i '[^a-z0-9\.\/_ ,()\-]'

Very strict (Blacklist):
find . -name '*[~#%&*()\[\]{}/\\:<>?+|"!§$=]*'

Very strict (Blacklist):
find . -name '*[~#%&*\[\]{}/\\:<>?|"!§$=]*'
missing ()+ compared to above

Quite strict:
find . -name '*[~#%&*()\[\]{}/\\:<>?+|"]*'

Relatively strict:
find . -name '*[~#%*{}/\\:<>?|"]*'
missing &()[]+ compared to above

Microsoft naming conventions:
find . -name '*[<>:"/\\|?*~#$]*'


To check:
!"§$%&/()[]{}=?\+*~#'|<>

```


Links:
- https://stackoverflow.com/questions/19008614/find-files-with-illegal-windows-characters-in-the-name-on-linux
- https://serverfault.com/questions/348482/how-to-remove-invalid-characters-from-filenames/871184#871184 - detox
- https://askubuntu.com/questions/113188/character-encoding-problem-with-filenames-find-broken-filenames
- https://stackoverflow.com/questions/623764/find-non-utf8-filenames-on-linux-file-system
- https://serverfault.com/questions/805621/how-can-i-find-all-files-in-a-directory-with-illegal-characters-in-the-file-name
- https://moredvikas.wordpress.com/2016/05/05/sharepoint-file-names-cant-contain-the-following-characters/
- https://gist.github.com/doctaphred/d01d05291546186941e1b7ddc02034d3
- https://docs.microsoft.com/en-us/windows/win32/fileio/naming-a-file
- https://unix.stackexchange.com/questions/319568/find-files-by-character-encoding
