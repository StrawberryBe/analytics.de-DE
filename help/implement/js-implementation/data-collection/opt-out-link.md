---
description: Geben Sie einen Ausschluss-Link an und personalisieren Sie das Branding dieses Links. Besucher Ihrer Website können sich entscheiden, ihre Aktivitäten nicht in den Analyseprodukten von Adobe nachverfolgen zu lassen, indem sie die Ausschluss-Seite für Ihre Datenerfassungsdomäne besuchen.
keywords: Analytics Implementation
subtopic: Troubleshooting
title: Ausschluss-Link hinzufügen
topic: Developer and implementation
uuid: c12092be-3be7-4621-b838-d6b78d074f84
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Ausschluss-Link hinzufügen

Geben Sie einen Ausschluss-Link an und personalisieren Sie das Branding dieses Links. Besucher Ihrer Website können sich entscheiden, ihre Aktivitäten nicht in den Analyseprodukten von Adobe nachverfolgen zu lassen, indem sie die Ausschluss-Seite für Ihre Datenerfassungsdomäne besuchen.

Wenn ein Benutzer nicht nachverfolgt werden möchte und ein Ausschluss-Cookie gesetzt ist, sendet Ihre JavaScript-Datei zwar weiterhin Daten an die Adobe-Server, allerdings werden die Daten nicht verarbeitet oder in Berichten verwendet.

Bei dem Abschnitt „collection_domain“ der URL-Struktur handelt es sich um den Nachverfolgungsserver, der in Ihrer JavaScript-Datei verwendet wird. Die für Ihre Adobe Analytics-Implementierung verwendete Erfassungsdomäne kann im DigitalPulse-Debugger in der ersten Zeile der Adobe Analytics-Tabelle angezeigt werden. Die Bezeichnung lautet je nach Implementierung entweder "Erstanbieter-Cookies"oder "Drittanbieter-Cookies". Die Erfassungsdomäne für Ihre Website kann die Domänen 2o7.net, omtrdc.net oder Ihre Website-Domäne wie metrics.example.com enthalten.

Besucher können sich von der Nachverfolgung ausschließen lassen, indem sie auf den Link auf der Ausschluss-Seite klicken, und dadurch einen entsprechenden Cookie in ihrem Browser setzen. Mit dem Cookie `omniture_optout` für die jeweilige Nachverfolgungsdomäne, werden die Aktivitäten des Benutzers nicht in die Berichte von Adobe Analytics aufgenommen. Sie können einen eigenen Link zum Ausschluss-Cookie bereitstellen oder die Schritte unten befolgen, um den Ausschluss-Cookie zu setzen.

Adobe bietet Ausschlussmöglichkeiten für alle Implementierungsarten. Sie sind selbst für Ihre eigenen Datenschutzrichtlinien und die Einhaltung der vereinbarten Bedingungen verantwortlich. Beachten Sie, dass der Link zur Ausschluss-Seite je nach Implementierungsart unterschiedlich sein kann.

Wenn Sie Adobe Analytics-Produkte und -Dienste so implementieren, dass Cookies auf Domänen von Adobe gesetzt sind (d. h. 207.net oder omtrdc.net), können Sie die Website-Besucher für alle Webseiten, die Adobe-Cookies für Adobe Analytics-Produkte und Dienste verwenden, auf den Ausschluss-Mechanismus im [Datenschutzzentrum von Adobe](https://www.adobe.com/privacy/opt-out.html) verweisen. Der direkte Link zum Adobe-Ausschluss-Mechanismus ist `https:// *collection_domain* /optout.html`.

More information about Adobe Analytics privacy practices can be found at [https://www.adobe.com/privacy/advertising-services.html](https://www.adobe.com/privacy/advertising-services.html).

* [URL-Struktur der Ausschluss-Seite](/help/implement/js-implementation/data-collection/opt-out-link.md#section_E0462428D2E440E7863E24D2F6DBF748)
* [Beispiel-Ausschluss-URLs](/help/implement/js-implementation/data-collection/opt-out-link.md#section_258DE5226AA0483CA790D2C9C5318B2E)
* [Branding Ihrer Ausschluss-URL](/help/implement/js-implementation/data-collection/opt-out-link.md#section_674AB62E810B414AB8F1615C0E3061F8)

## URL-Struktur der Ausschluss-Seite {#section_E0462428D2E440E7863E24D2F6DBF748}

Ihre Ausschluss-Seite befindet sich unter der folgenden URL:

```
https://collection_domain/optout.html[?optional_parameters]
```

`optional_parameters` umfasst:

`locale=[code]`: Stellt eine übersetzte Version der Ausschluss-Seite bereit. Die folgenden Sprachen werden unterstützt:

* en_US (Standard)
* de_DE
* es_ES
* fr_FR
* jp_JP
* ko_KR
* zh_CN
* zh_TW

`popup=1`: Behandelt die Seite als Popup und bietet die Schaltfläche "Fenster schließen".

## Beispiel-Ausschluss-URLs {#section_258DE5226AA0483CA790D2C9C5318B2E}

Eine englischsprachige Webseite in einem vollständigen Fenster mit einem Link verhindert, dass der Besucher auf metrics.example.com nachverfolgt wird, wenn der Link angeklickt wird:

```
https://metrics.example.com/optout.html
```

Eine französischsprachige Webseite in einem vollständigen Fenster mit einem Link verhindert, dass der Besucher auf example.d3.sc.omtrdc.net nachverfolgt wird, wenn der Link angeklickt wird:

```
https://example.d3.sc.omtrdc.net/optout.html?locale=fr_FR
```

Eine deutschsprachige Webseite in einem Popup-Fenster mit einem Link verhindert, dass der Besucher auf example.112.2o7.net nachverfolgt wird, wenn der Link angeklickt wird:

```
https://example.112.2o7.net/optout.html?popup=1&locale=de_DE
```

## Branding Ihrer Ausschluss-URL {#section_674AB62E810B414AB8F1615C0E3061F8}

Sie können einen Link wie den Folgenden auf Ihrer Website bereitstellen:

```
 <a href=" https://stats.adobe.com/optout.html?optout=1&confirm_change=1">
Click Here to Opt Out! </a>
```

Dabei wird *`stats.adobe.com`* mit dem Wert ersetzt, der für die Variable *`s.trackingServer`* eingestellt ist.

Möchten Sie dagegen einen Einschluss-Link bereitstellen, so verwenden Sie dieselbe URL, ersetzen darin aber `?optout=1` durch `?optin=1`. `confirm_change=1` bleibt hingegen unverändert.
