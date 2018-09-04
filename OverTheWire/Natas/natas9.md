# Natas 9

Username: natas9

Password: ```W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl```

URL: <http://natas9.natas.labs.overthewire.org/>

On the page we see a page containing a search bar, output of the search and a link to the source code. Examining the source code,  we see another PHP function,

```PHP
<?
$key = "";

if(array_key_exists("needle", $_REQUEST)) {
    $key = $_REQUEST["needle"];
}

if($key != "") {
    passthru("grep -i $key dictionary.txt");
}
?>
```

From the PHP code, we see that if the `$key` is not empty, the script greps dictionary.txt for the `$key` you input into the box.

Reading up on the `passthru` method, we can see that it will execute methods passed through it. As grep is a linux command, we can try and use directory traversal (../../../../) to try and access the root directory and then try and get the flag from `/etc/natas_webpass/natas10`.

If we enter `; cat ../../../../../../etc/natas_webpass/natas10` into the search bar, we get the entire dictionary list as well as the password for natas10.

<details>
    <summary>Flag</summary>
    nOpp1igQAkUzaI1GUUjzn1bFVj7xCNzu
</details>