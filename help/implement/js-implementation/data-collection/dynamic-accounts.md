---
description: Die .js-Datei kann so konfiguriert werden, dass sie automatisch eine Report Suite-ID auswählt.
keywords: Analytics-Implementierung
seo-description: Die .js-Datei kann so konfiguriert werden, dass sie automatisch eine Report Suite-ID auswählt.
seo-title: Report Suite-IDs - dynamische Konten
solution: Analytics
title: Report Suite-IDs - dynamische Konten
topic: Entwickler und Implementierung
uuid: 763 a 9741-309 d -4795-8819-6543866047 d 5
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Report Suite-IDs - dynamische Konten

Die .js-Datei kann so konfiguriert werden, dass sie automatisch eine Report Suite-ID auswählt. Die JS-Datei sendet das angeforderte Bild basierend auf der URL automatisch an die Report Suite. Wenn die URL beispielsweise `www.mysite.com` lautet, wird die Bildanforderung automatisch an Report Suite A gesendet. Lautet die URL `www.mysite1.com`, geht die Bildanforderung automatisch an Report Suite B.

Solche Zeichenfolgen können sich an den folgenden Stellen befinden:

* Host/Domäne (Standardeinstellung)
* Pfad
* Abfragezeichenfolge
* Host/Domäne und Pfad
* Pfad und Abfragezeichenfolge
* Vollständige URL

Weitere Informationen über die Konfiguration von [!DNL Analytics] zur automatischen Auswahl einer [!UICONTROL Report Suite-ID] erhalten Sie vom Adobe Live Support.

## Definieren des zu vergleichenden URL-Segments {#section_8099162F75F641CFBE46FD814450EF36}

Für die folgende Beispiel-URL sind unten die einzelnen Teile der URL zusammen mit der festzulegenden Variablen `s.dynamicAccountMatch` aufgeführt. (Wenn `s.dynamicAccountMatch` nicht definiert ist, wird standardmäßig nur im Host-/Domänennamen gesucht.)
Beispiel-URL: `https://www.client.com/directory1/directory2/filename.html?param1=1234&param2=4321`

| Teil | Beispiel (aus oben angegebener URL) |
|---|---|
| Host-/Domänenname | `www.client.com` |
| Pfad | `directory1/directory2/filename.html` |
| Abfragezeichenfolge | `param1=1234&param2=4321` |
| Host/Domäne und Pfad | `www.client.com/directory1/directory2/filename.html` |
| Pfad und Abfragezeichenfolge | `directory1/directory2/filename.html?param1=1234&param2=4321` |
| URL | `https://www.client.com/directory1/directory2/filename.html?param1=1234&param2=4321` |
| Teil | `s.dynamicAccountmatch` |
| Host-/Domänenname | Nicht definiert |
| Pfad | `window.location.pathname` |
| Abfragezeichenfolge | `(window.location.search?window.location.search:"?")` |
| Host/Domäne und Pfad | `window.location.host+window.location.pathname` |
| Pfad und Abfragezeichenfolge | `window.location.pathname+(window.location.search?window.location.search:"?")` |
| URL | `window.location.href` |

Siehe folgendes Beispiel:

* `s.dynamicAccountSelection=true`
* `s.dynamicAccountList="devreportsuite1=qa.client.com;reportsuite2=clientdirectory;reportsuite1=client.com"`
* `s.dynamicAccountMatch=window.location.host+window.location.pathname`

## Mehrere Regeln {#section_163FED1C1FA74C48BCB78B0D67EF36AE}

Bei Auswahl mehrerer Regeln (siehe Beispiel oben) werden die Regeln von links nach rechts ausgeführt. Sobald eine Übereinstimmung gefunden ist, wird die Auswertung der Regeln beendet (wie oben anhand der angegebenen Regeln gezeigt).

* `s.dynamicAccountSelection=true`
* `s.dynamicAccountList="devreportsuite1=qa.client.com;reportsuite1=client.com"`

The code first checks to determine if `qa.client.com` exists within the Host/Domain Name. If so, the report suite `devreportsuite1` is selected, and the match stops. Mehrere Regeln werden mit Semikolons getrennt.

## Standardmäßige Report Suite {#section_0360D724929348B0B211708B5BA15647}

The `s_account` variable can be set first, and acts as a default value in case any of the specified strings cannot be found. Siehe folgendes Beispiel:

```javascript
var s_account="defaultreportsuiteid" 
s.dynamicAccountSelection=true 
s.dynamicAccountList="devreportsuite1=qa.client.com;reportsuite1=client.com" 
```

In the case above, if the host/domain name did not contain either `qa.client.com` or `client.com`, the report suite *defaultreportsuiteid* would be used.
