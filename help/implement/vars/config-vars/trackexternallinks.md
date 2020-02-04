---
title: trackExternalLinks
description: Aktivieren oder deaktivieren Sie die automatische Linktracking für Exitlinks.
translation-type: tm+mt
source-git-commit: 04b97e93a95691132680d4da197dc62eb2b9fdd1

---


# trackExternalLinks

Adobe bietet die Möglichkeit, ausgehende Links zu verfolgen, ohne die `tl()` Funktion für jeden Ausstiegslink manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie die automatische Linktracking für Ausstiegslinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle angeklickten Link-URL mit Werten in `linkInternalFilters` und `linkExternalFilters`. Bei Übereinstimmung wird automatisch ein Ausstiegslink-Verfolgungsaufruf ausgelöst.

## Ausgehende Links in Adobe Experience Platform Launch verfolgen

Ausgehende Links verfolgen ist ein Kontrollkästchen unter dem Akkordeon &quot; [!UICONTROL Linktracking] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Linktracking] &quot;, in dem das Kontrollkästchen &quot;Ausgehende Links [!UICONTROL verfolgen&quot;angezeigt wird] .

Markieren Sie das Kontrollkästchen, um die automatische Verfolgung von Ausstiegslinks zu aktivieren.

## s.trackExternalLinks in AppMeasurement und Benutzerdefinierter Code-Editor starten

Der `s.trackExternalLinks` ist ein boolescher Wert, der die automatische Ausstiegslink-Verfolgung aktiviert oder deaktiviert. Wenn Sie ausgehende Links nicht verfolgen möchten oder die `tl()` Funktion lieber manuell aufrufen möchten, um Ausstiegslinks zu verfolgen, setzen Sie diese Variable auf `false`.

```js
s.trackDownloadLinks = true;
```
