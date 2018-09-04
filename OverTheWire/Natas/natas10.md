# Natas 10

Username: natas10

Password: ```nOpp1igQAkUzaI1GUUjzn1bFVj7xCNzu```

URL: <http://natas10.natas.labs.overthewire.org/>

The page looks the same as natas9, but if we look at the source code, we can see that they've disallowed the use of some special characters.

```PHP
<?
$key = "";

if(array_key_exists("needle", $_REQUEST)) {
    $key = $_REQUEST["needle"];
}

if($key != "") {
    if(preg_match('/[;|&]/',$key)) {
        print "Input contains an illegal character!";
    } else {
        passthru("grep -i $key dictionary.txt");
    }
}
?>
```

Reading up about the grep function [here](http://www.robelle.com/smugbook/regexpr.html) shows that grep can be used with regex characters, notably `.` in this instance, where it can match one character of any value. As the `#` value is not blocked, we can enter `. /etc/natas_webpass/natas11 #` into the input bar to get the password to natas11. The `#` character is used to comment out lines in linux, so if we place the character after the file path, it should comment out `dictionary.txt` allowing us to search the system instead.

When we enter the _payload_, we get the password to natas11.

<details>
    <summary>Flag</summary>
    U82q5TCMMQ9xuFoI3dYX61s7OZD9JKoK
</details>
