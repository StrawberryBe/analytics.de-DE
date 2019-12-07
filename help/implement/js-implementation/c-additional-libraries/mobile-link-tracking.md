---
description: 'null'
keywords: Analytics Implementation;link reference;redir
title: Benutzerdefinierte Link-Messungen bei Mobilfunkprotokollen
topic: Developer and implementation
uuid: eb82de26-da2e-41c2-8924-59b6b5ccef28
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Benutzerdefinierte Link-Messungen bei Mobilfunkprotokollen

Viele Mobilgerätenutzer laden Dateien auf ihre Geräte herunter, wie Podcasts, Klingeltöne u. Ä. Da zahlreiche Mobilgeräte JavaScript nicht unterstützen, müssen Link-Messungen über Linkumleitungen implementiert werden. Um Linkumleitungen verwenden zu können, müssen Sie ein Element „REDIR“ in die HREF-Links im HTML-Code integrieren. Das allgemeine Format für einen benutzerdefinierten Link sieht wie folgt aus:

```
https://<your_Namespace>.112.2o7.net/b/ss/<RSID>/4/REDIR/
?url=<destination_URL>&pe=<link_type>&pev1=<current_URL>&pev2=<link_name>
```

Beachten Sie Folgendes, wenn Sie einen Linkverweis erstellen:

* Der URL-Wert muss URL-kodiert sein.
* Sie müssen den Parameter „pageName“ oder „pageURL“ (g) festlegen.
* Dynamische Variablen können den URL-Parameter zwar lesen, ihn aber nicht festlegen.
* Wenn kein Cookie festgelegt wurde, führen die Adobe-Server einen standardmäßigen Cookie-Handshake aus.
* Um Links nachverfolgen zu können, müssen Sie die Parameter „pe“, „pev1“ und „pev2“ einbeziehen.

Eine benutzerdefinierte URL für die Link-Messung sieht wie folgt aus:

```
<a href=" https://johnny_appleseed.122.2o7.net/b/ss/appleseedpodcasts/4/REDIR/
?url=http%3A%2F%2Fwww.johnny_appleseed.org%2Fmpegs%2Fplanting_apple_trees.mpeg&pe=lnk_d
&pev1=http%3A%2F%2Fwww.johnny_appleseed.org%2Fmpegs%2Fplanting_apple_trees.mpeg&pev2=pl anting_apple_trees&">Planting an Apple Tree</a>
```

Weitere Informationen finden Sie im Whitepaper [Exit Link Tracking Redirects](https://marketing.adobe.com/resources/help/en_US/whitepapers/redirects/) (Redirects zum Verfolgen von Exitlinks).
