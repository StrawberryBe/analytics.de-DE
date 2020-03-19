---
title: linkLeaveQueryString
description: Ermöglicht die Beibehaltung von Abfragen-Zeichenfolgen in den Dimensionen der Linktracking.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkLeaveQueryString

AppMeasurement entfernt standardmäßig Abfragen-Zeichenfolgen von Link-Tracking-URLs. Verwenden Sie die `linkLeaveQueryString` Variable, um die Zeichenfolgen der Abfrage in den Abmessungen der Linktracking beizubehalten.

Bei einigen Exitlinks und Downloadlinks kann sich der wichtige Teil der URL in der Abfrage-Zeichenfolge befinden. Beispielsweise enthält ein Downloadlink wie `https://example.com/download.asp?filename=myfile.exe` er wichtige Linkinformationen in der Abfrage-Zeichenfolge.

Wenn die Linktracking-Informationen nicht in den URLs Ihrer Site enthalten sind, ist die Verwendung dieser Variablen nicht erforderlich. Durch Entfernen von Abfragen-Zeichenfolgen aus Link-Tracking-URLs wird die Anzahl der eindeutigen Werte in der Dimension eingeschränkt.

Die Aktivierung `linkLeaveQueryString` gilt für alle Dimensionen der Linktracking (einschließlich benutzerspezifischer Links, Exitlinks und Downloadlinks).

> [!TIP] Diese Variable wirkt sich nicht auf Dimensionen außerhalb der Linktracking aus. Dies betrifft nur benutzerspezifische Links, Ausstiegslinks und Downloadlinks.

## URL-Parameter beim Starten der Adobe Experience Platform beibehalten

[!UICONTROL Keep URL Parameters] ein Kontrollkästchen unter dem [!UICONTROL Link Tracking] Akkordeon beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Link Tracking] Akkordeon, das das [!UICONTROL Keep URL Parameters] Kontrollkästchen einblenden soll.

Aktivieren Sie dieses Kontrollkästchen, wenn Sie Abfragen-Zeichenfolgen in die Abmessungen der Linktracking einbeziehen möchten.

## s.linkLeaveQueryString im AppMeasurement- und Launch-Editor für benutzerdefinierten Code

Die `s.linkLeaveQueryString` Variable ist ein boolescher Wert. Its default value is `false`.

* Wenn diese Variable auf `true`festgelegt ist, bleiben die Zeichenfolgen der Abfrage in den Linktracking-URLs erhalten.
* Wenn diese Variable auf `false` oder nicht definiert ist, werden Abfragen-Zeichenfolgen aus den Linktracking-URLs entfernt.

```js
s.linkLeaveQueryString = true;
```

## Beispiel

Seien Sie vorsichtig, wenn Sie diese Variable auf &quot;true&quot;setzen, da dies Auswirkungen auf Filter wie [`linkInternalFilters`](linkinternalfilters.md), [`linkExternalFilters`](linkexternalfilters.md)und [`linkDownloadFiletypes`](linkdownloadfiletypes.md)die Linktracking haben kann.

Betrachten Sie das folgende Beispiel, als wäre es auf `adobe.com`:

```html
<script>
  s.linkInternalFilters = "adobe.com";
  s.linkLeaveQueryString = true;
</script>

<!--This link is not an exit link because the internal filter matches part of the query string -->
<a href = "example.com?r=adobe.com">Example link</a>
```
