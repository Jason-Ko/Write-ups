# Natas 3

Username: natas3

Password: ```sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14```

URL: <http://natas3.natas.labs.overthewire.org>

Pop open the developer tools, see the comment 

`<!-- No more information leaks!! Not even Google will find it this time... -->`

When google searching, you'll often see that website descriptions/previews are blocked by a `robots.txt` file. `robot.txt` files usually tell web crawlers not to access or scrape certain directories on the site and will often include the directories in the txt file itself.

The `robots.txt` can be accessed by typing `/robots.txt` after the URL of the page. When we access the txt file, we see that the `/s3cr3t/` is disallowed. Accessing the `/s3cr3t/` director gives us access to the 'users.txt` file which contains the credentials to natas4.

<details>
    <summary>Flag</summary>
    Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
</details>