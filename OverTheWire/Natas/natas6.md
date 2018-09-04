# Natas 6

Username: natas6

Password: ```aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1```

URL: <http://natas6.natas.labs.overthewire.org>

When opening the page, we are presented with an input box, a submit button and a link to view the source code.

Checking out the source code will allow you to check out a PHP function that will return the flag for natas7 if we make a post request with the correct secret that will match with the `$_secret` variable.

From the source code, we can see that the PHP code requres `includes/secret.inc` which looks like a file path. Navigating to the file path specified, we are presented with the value of `$_secret`. Submitting that value into the input box, we get access to the credentials for natas7.


<details>
    <summary>Flag</summary>
    7z3hEENjQtflzgnT29q7wAvMNfZdh0i9
</details>
