---
description: Server webpanel instructions.
---

# Server Webpanel Instructions

## Change The Server Access

Edit the `server-config.json` if you want to change the access IP to limit people connecting to the webpanel.

```
"httpserver": {
    "access_ip": "0.0.0.0"
}
```

<figure><img src="../.gitbook/assets/Screenshot 2026-03-06 103554.png" alt=""><figcaption></figcaption></figure>

Replace `"0.0.0.0"` or whatever value you have with the IP address you only want to be able to access the webpanel. (Leaving it `"0.0.0.0"` - will allow anyone to access the webpanel with your ip:8080 ) To know your IP address, you can use this website: [https://whatismyipaddress.com/](https://whatismyipaddress.com/), only you will be able to connect to the webpanel.
