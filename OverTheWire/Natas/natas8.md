# Natas 8

Username: natas8

Password: ```DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe```

URL: <http://natas8.natas.labs.overthewire.org/>

When opening the page, we can see the familiar input box and submit button from natas6, but with different source code.

Checking the PHP function, we see,

```PHP
<?
$encodedSecret = "3d3d516343746d4d6d6c315669563362";

function encodeSecret($secret) {
    return bin2hex(strrev(base64_encode($secret)));
}

if(array_key_exists("submit", $_POST)) {
    if(encodeSecret($_POST['secret']) == $encodedSecret) {
    print "Access granted. The password for natas9 is <censored>";
    } else {
    print "Wrong secret";
    }
}
?>
```

To calculate the variable `$encodedSecret`, it seems that the `$secret` variable is encoded with base64, then reversed, then is changed from binary to hex with bin2hex. To decode the `$encodedSecret` we should decode it in the reverse order.

So first:

1. Get the `$encodedSecret`, decode the hexadecimal to binary.
   * (<https://convertstring.com/EncodeDecode/HexDecode>, `==QcCtmMml1ViV3b`)

2. Then we reverse the string.  
   * (<https://www.strreverse.com/>, `b3ViV1lmMmtCcQ==`)

3. Then we base64 decode it.
   * (<https://www.base64decode.org/>, `oubWYf2kBq`)

Input `oubWYf2kBq` into the input bar to get the credentials for natas9.

<details>
    <summary>Flag</summary>
    W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl
</details>