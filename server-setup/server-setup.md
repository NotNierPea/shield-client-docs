---
description: How to setup up the server.
---

# How To Set Up The Server

**Download server from** [**here.**](https://github.com/NotNierPea/shield-client-docs/releases/download/release/DWServer-New.zip)

### Open ports

#### Automatic

Download `FIREWALL.RULES-AUTO.bat` [here.](https://github.com/NotNierPea/shield-client-docs/releases/download/release/FIREWALL.RULES-AUTO.BAT) then run the file as administrator. optionally, to make the webserver accessible over external network, run the `FIREWALL.RULES.WEBSERVER.BAT` file as administrator.

#### Manual

Open Windows Defender Firewall with Advanced Security by pressing Windows+R, type `WF.msc` and press ok.

* In the Inbound Rules tab, create a new rule by pressing the "New Rule..." button.

For the type, select `Port`. In the protocol and ports menu, select TCP and specific ports. With the value `3074,6542,8080`. You can keep the default settings for the next menus and give `ShieldServer-TCP` as a name.

* Create another rule with the "New Rule..." button, also with the type `Port`.

In the protocol and ports menu, select UDP and specific ports. With the value `3074`. You can keep the default settings for the next menus and give `ShieldServer-UDP` as a name.

* In the Outbound Rules tab, create a new rule by pressing the "New Rule..." button.

For the type, select `Port`. In the protocol and ports menu, select TCP and specific ports. With the value `3074,6542`. You can keep the default settings for the next menus and give `ShieldServer-TCP` as a name.

* Create another rule with the "New Rule..." button, also with the type `Port`.

In the protocol and ports menu, select UDP and specific ports. With the value `3074`.

* Create another rule with the "New Rule..." button, also with the type `Port`.

In the protocol and ports menu, select UDP and specific ports. With the value `3074`.\
You can keep the default settings for the next menus and give `ShieldServer-UDP` as a name. If you want to play with players outside your local netword, you also need the forward your ports with your router. Or use `radmin` / `zero tier`. This website can help with most of the routers: [https://portforward.com/router.htm](https://portforward.com/router.htm) The ports are:

```
TCP: 3074, 6542
UDP: 3074
```

The webserver ports are:

```
TCP: 8080
```
