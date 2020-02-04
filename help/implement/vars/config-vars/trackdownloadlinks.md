---
title: trackDownloadLinks
description: Aktivieren oder deaktivieren Sie die automatische Linktracking für Downloadlinks.
translation-type: tm+mt
source-git-commit: 04b97e93a95691132680d4da197dc62eb2b9fdd1

---


# trackDownloadLinks

Adobe bietet die Möglichkeit, Downloadlinks zu verfolgen, ohne die `tl()` Funktion für jeden Download-Link manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie die automatische Linktracking für Downloadlinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle angeklickten Link-URL mit den Werten in `downloadLinkFileTypes`. Bei Übereinstimmung wird automatisch ein Downloadlink-Verfolgungsaufruf ausgelöst.

## Nachverfolgen von Download-Links in Adobe Experience Platform Launch

Links zum Verfolgen von Downloads sind ein Kontrollkästchen unter dem Akkordeon &quot; [!UICONTROL Linktracking] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Linktracking] &quot;, in dem das Kontrollkästchen &quot;Links [!UICONTROL zum Verfolgen von Downloads] &quot;angezeigt wird.

Aktivieren Sie das Kontrollkästchen, um die automatische Verfolgung von Downloadlinks zu aktivieren.

## s.trackDownloadLinks in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Der `s.trackDownloadLinks` ist ein boolescher Wert, der die automatische Verfolgung von Downloadlinks aktiviert oder deaktiviert. Wenn Sie Downloadlinks nicht verfolgen möchten oder die `tl()` Funktion lieber manuell aufrufen möchten, um Downloads zu verfolgen, setzen Sie diese Variable auf `false`.

```js
s.trackDownloadLinks = true;
```
