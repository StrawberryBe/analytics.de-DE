---
title: linkLeaveQueryString
description: Ermöglicht die Beibehaltung von Abfragezeichenfolgen in den Dimensionen der Linktracking.
translation-type: tm+mt
source-git-commit: e500332fe16887fa004858b07b59644837e183aa

---


# linkLeaveQueryString

AppMeasurement entfernt Abfragezeichenfolgen standardmäßig aus Link-Tracking-URLs. Verwenden Sie die Variable &quot;linkLeaveQueryString&quot;, um Abfragezeichenfolgen in den Linkverfolgungsdimensionen beizubehalten.

Bei einigen Exitlinks und Downloadlinks kann sich der wichtige Teil der URL in der Abfragezeichenfolge befinden. Beispielsweise enthält ein Download-Link wie `https://example.com/download.asp?filename=myfile.exe` er wichtige Linkinformationen in der Abfragezeichenfolge.

Wenn die Linktracking-Informationen nicht in den URLs Ihrer Site enthalten sind, ist die Verwendung dieser Variablen nicht erforderlich. Das Entfernen von Abfragezeichenfolgen aus Link-Tracking-URLs hilft, die Anzahl der eindeutigen Werte, die die Dimension enthält, zu begrenzen.

Die Aktivierung `linkLeaveQueryString` gilt für alle Dimensionen der Linktracking (einschließlich benutzerspezifischer Links, Exitlinks und Downloadlinks).

> [!TIP] Diese Variable hat keine Auswirkungen auf Dimensionen außerhalb der Linktracking. Dies betrifft nur benutzerspezifische Links, Ausstiegslinks und Downloadlinks.

## URL-Parameter beim Starten der Adobe Experience Platform beibehalten

[!UICONTROL Bei der Konfiguration der Adobe Analytics-Erweiterung ist das Kontrollkästchen &quot;URL-Parameter] beibehalten&quot;im Akkordeon &quot; [!UICONTROL Linktracking] &quot;aktiviert.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Linktracking] &quot;, das das Kontrollkästchen &quot;URL-Parameter [!UICONTROL beibehalten] &quot;anzeigt.

Aktivieren Sie dieses Kontrollkästchen, wenn Sie Abfragezeichenfolgen in die Dimensionen der Linktracking einbeziehen möchten.

## s.linkLeaveQueryString in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.linkLeaveQueryString` Variable ist ein boolescher Wert. Its default value is `false`.

* Wenn diese Variable auf `true`festgelegt ist, werden Abfragezeichenfolgen in Linktracking-URLs beibehalten.
* Wenn diese Variable auf `false` oder nicht definiert ist, werden Abfragezeichenfolgen aus den Linktracking-URLs entfernt.

```js
s.linkLeaveQueryString = true;
```

## Beispiel

Seien Sie vorsichtig, wenn Sie diese Variable auf &quot;true&quot;setzen, da dies Auswirkungen auf Link-Verfolgungsfilter wie `linkInternalFilters`, `linkExternalFilters`und `linkDownloadFiletypes`haben kann.

Betrachten Sie das folgende Beispiel, als wäre es auf `adobe.com`:

```html
<script>
  s.linkInternalFilters = "adobe.com";
  s.linkLeaveQueryString = true;
</script>

<!--This link is not an exit link because the internal filter matches part of the query string -->
<a href = "example.com?r=adobe.com">Example link</a>
```
