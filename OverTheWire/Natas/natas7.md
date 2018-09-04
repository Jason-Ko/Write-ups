# Natas 7

Username: natas7

Password: ```7z3hEENjQtflzgnT29q7wAvMNfZdh0i9```

URL: <http://natas7.natas.labs.overthewire.org/>

When we open the page, we are presented with a mini menu with the `home` and `about` links.

Checking the developer tools, we can see the comment,

```<!-- hint: password for webuser natas8 is in /etc/natas_webpass/natas8 -->```

Looking at the url, we notice ```index.php?page=home```. the `?` indicates a query string, so we change the page from `home` to `/etc/natas_webpass/natas8` instead and are presented with the credentials to natas8.

<details>
    <summary>Flag</summary>
    DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe
</details>