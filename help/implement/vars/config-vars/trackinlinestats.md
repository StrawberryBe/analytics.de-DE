---
title: trackInlineStats
description: Aktivieren oder deaktivieren Sie Activity Map in Ihrer Implementierung.
translation-type: tm+mt
source-git-commit: 979a95ca749a3e21c4ddf48ba2d2a95672938a20

---


# trackInlineStats

Activity Map ist eine Funktion in Adobe Analytics, mit der Daten gesammelt werden, auf die Besucher klicken und auf die sie klicken. Sie können diese Daten in Analytics-Berichten oder mithilfe einer Browser-Erweiterungs-Überlagerung anzeigen. Aktivieren Sie diese Variable, wenn Sie Activity Map-Funktionen verwenden möchten.

Wenn diese Option aktiviert ist, erfasst AppMeasurement Informationen zum Link und sendet diese Daten in der nächsten Bildanforderung. Informationen aus jedem Klick werden in einem Cookie mit der Bezeichnung `s_sq`.

## ClickMap in Adobe Experience Platform Launch aktivieren

[!UICONTROL ClickMap] aktivieren ist ein Kontrollkästchen unter dem Akkordeon &quot; [!UICONTROL Linkverfolgung] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Linktracking] &quot;, das das Kontrollkästchen &quot;ClickMap [!UICONTROL aktivieren] &quot;anzeigt.

Aktivieren Sie das Kontrollkästchen, um die Activity Map-Verfolgung zu aktivieren.

## s.trackInlineStats in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die Variable `s.trackInlineStats` ist ein boolescher Wert, der die Activity Map-Verfolgung aktiviert oder deaktiviert. Its default value is `false`. Legen Sie diesen Wert fest, `true` wenn Sie die Activity Map-Datenerfassung aktivieren möchten.

```js
s.trackInlineStats = true;
```
