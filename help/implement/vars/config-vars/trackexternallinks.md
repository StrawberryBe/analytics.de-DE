---
title: trackExternalLinks
description: Aktivieren oder deaktivieren Sie die automatische Linktracking für Exitlinks.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# trackExternalLinks

Adobe Angebots bietet die Möglichkeit, ausgehende Links zu verfolgen, ohne die [`tl()`](../functions/tl-method.md) Methode für jeden Ausstiegslink manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie die automatische Linktracking für Ausstiegslinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle angeklickten Link-URL mit Werten in [`linkInternalFilters`](linkinternalfilters.md) und [`linkExternalFilters`](linkexternalfilters.md). Wenn eine Übereinstimmung vorliegt, wird automatisch ein Ausstiegslink-Verfolgungsaufruf ausgelöst.

## Ausgehende Links in Adobe Experience Platform Launch verfolgen

Ausgehende Links verfolgen ist ein Kontrollkästchen unter dem [!UICONTROL Link Tracking] Akkordeon, wenn die Adobe Analytics-Erweiterung konfiguriert wird.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Link Tracking] Akkordeon, das das [!UICONTROL Track outbound links] Kontrollkästchen einblenden soll.

Markieren Sie das Kontrollkästchen, um die automatische Verfolgung von Ausstiegslinks zu aktivieren.

## s.trackExternalLinks in AppMeasurement und Benutzerdefinierter Code-Editor starten

Der `s.trackExternalLinks` ist ein boolescher Wert, der die automatische Ausstiegslink-Verfolgung aktiviert oder deaktiviert. Wenn Sie ausgehende Links nicht verfolgen möchten oder die `tl()` Methode zur Verfolgung von Ausstiegslinks lieber manuell aufrufen möchten, setzen Sie diese Variable auf `false`.

```js
s.trackDownloadLinks = true;
```
