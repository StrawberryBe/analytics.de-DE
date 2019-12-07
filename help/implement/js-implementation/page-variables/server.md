---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# server

Die Variable „“ gibt entweder die Domäne einer Webseite an (damit Sie wissen, welche Ihrer Domänen besucht wird) oder den Server, von dem die Seite stammt (als Referenz für Lastenausgleichszwecke).


<!-- 

server.xml

 -->

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | server | Server | "" |

Wenn die Inhalte Ihrer Site aus mehreren Domänen stammen, kann mithilfe der Variable *`server`* auch verfolgt werden, welche dieser Domänen von Besuchern verwendet wird. Das folgende JavaScript trägt die Domäne der Seite in die „server“-Variable ein.

```js
s.server=window.location.hostname
```

Wenn Sie die „server“-Variable als Orientierungshilfe beim Lastenausgleich einsetzen, können Sie in dieser Variable einen Servernamen oder eine Nummer ablegen. Siehe folgendes Beispiel:

```js
s.server="server 14"
```

Der Bericht [!UICONTROL Bevorzugte Server] kann zwar als Orientierungshilfe beim Lastenausgleich genutzt werden, stellt jedoch keine präzise Messung von Serverlasten dar. So führt zum Beispiel Datenverkehr, der über die Schaltfläche „Zurück“ erzeugt wird, nicht zu einer Erhöhung der Serverlast, wird jedoch in Berichten angezeigt. Der Bericht gibt nicht an, von welchen Servern Bilder oder große Downloads stammen.

**Syntax und mögliche Werte** {#section_48E4B9BFEBFF4409A246D86EC0C0FB13}

```js
s.server="server_name"
```

Die Variable *`server`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_78B9EE3C27FB491384869E3D0BD503D6}

```js
s.server="server 18" 
s.server=window.location.hostname 
```

**Konfigurationseinstellungen** {#section_969DB379D5BD469FBEE8D505D3000E49}

Keine

**Probleme, Fragen und Tipps** {#section_42A28F9B01574F38891D9D54B411D8FE}

Die Variable *`server`* kann eingesetzt werden, um anzugeben, welche Domänen die beliebtesten sind oder von welchen Servern die meisten Seiten kommen.

