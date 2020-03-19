---
title: trackDownloadLinks
description: Aktivieren oder deaktivieren Sie die automatische Linktracking für Downloadlinks.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# trackDownloadLinks

Adobe Angebots bietet die Möglichkeit, Downloadlinks zu verfolgen, ohne die [`tl()`](../functions/tl-method.md) Methode für jeden Downloadlink manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie die automatische Linktracking für Downloadlinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle angeklickten Link-URL mit den Werten in [`linkDownloadFileTypes`](linkdownloadfiletypes.md). Wenn eine Übereinstimmung vorliegt, wird automatisch ein Downloadlink-Verfolgungsaufruf ausgelöst.

## Nachverfolgen von Download-Links in Adobe Experience Platform Launch

Links zum Verfolgen von Downloads sind ein Kontrollkästchen unter dem [!UICONTROL Link Tracking] Akkordeon, wenn Sie die Adobe Analytics-Erweiterung konfigurieren.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Link Tracking] Akkordeon, das das [!UICONTROL Track download links] Kontrollkästchen einblenden soll.

Aktivieren Sie das Kontrollkästchen, um die automatische Verfolgung von Downloadlinks zu aktivieren.

## s.trackDownloadLinks in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Der `s.trackDownloadLinks` ist ein boolescher Wert, der die automatische Verfolgung von Downloadlinks aktiviert oder deaktiviert. Wenn Sie Downloadlinks nicht verfolgen möchten oder die `tl()` Methode zum Verfolgen von Downloads lieber manuell aufrufen möchten, setzen Sie diese Variable auf `false`.

```js
s.trackDownloadLinks = true;
```
