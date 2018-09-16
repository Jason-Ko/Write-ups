# Natas 4

Username: natas4

Password: ```Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ```

URL: <http://natas4.natas.labs.overthewire.org>

Opening the page, we see the comment,

```... while authorized users should come only from "http://natas5.natas.labs.overthewire.org/"```

Check the headers of the page for the `referer` header (intentionally mispelled), the `referer` will either be empty or contain the `referer` page (the page where the request originated) depending on how you accessed the page.

To modify the header, you can use burp suite to intercept the request and modify the `referer` header before forwarding the request, or if on Google Chrome, you can download the `ModHeader` extension and modify the `referer` header before sending the page.

After completing either of the two actions above, you are presented with the page with the credentials for natas5.

<details>
    <summary>Flag</summary>
    iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq
</details>

