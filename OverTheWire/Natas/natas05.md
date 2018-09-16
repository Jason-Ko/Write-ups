# Natas 5

Username: natas5

Password: ```iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq```

URL: <http://natas5.natas.labs.overthewire.org>

When we open the page we see,

```Access disallowed. You are not logged in```

Opening the developer tools and checking the headers, we can see the `Cookie` header with a value of `loggedin=0` after the `__cfduid` value.

Using either the `Mod Header` extension or burp suite, we can change the value from `0` to `1` then forward or request to page to be presented with the credentials for natas6.

<details>
    <summary>Flag</summary>
    aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1
</details>