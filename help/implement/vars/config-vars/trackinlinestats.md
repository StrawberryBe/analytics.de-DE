---
title: trackInlineStats
description: Aktivieren oder deaktivieren Sie Activity Map in Ihrer Implementierung.
keywords: Activity Map deaktivieren
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: ht
source-wordcount: '196'
ht-degree: 100%

---

# trackInlineStats

Activity Map ist eine Funktion in Adobe Analytics, mit der Daten darüber erfasst werden, wo Besucher klicken und worauf sie klicken. Sie können diese Daten in Analytics-Berichten oder mithilfe eines Browser-Erweiterungs-Overlays anzeigen. Aktivieren Sie diese Variable, wenn Sie Activity Map-Funktionen verwenden möchten.

Wenn diese Option aktiviert ist, erfasst AppMeasurement Informationen zum Link und sendet diese Daten in der nächsten Bildanforderung. Informationen aus jedem Klick werden in einem Cookie mit der Bezeichnung `s_sq` gespeichert.

## Aktivieren von ClickMap mithilfe von Tags in Adobe Experience Platform

[!UICONTROL ClickMap aktivieren] ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL ClickMap aktivieren] angezeigt wird.

Aktivieren Sie das Kontrollkästchen, um Activity Map-Tracking zu aktivieren.

## s.trackInlineStats in AppMeasurement und im benutzerdefinierten Code-Editor

`s.trackInlineStats` ist ein boolescher Wert, der Activity Map-Tracking aktiviert oder deaktiviert. Der Standardwert lautet `false`. Setzen Sie diesen Wert auf `true`, wenn Sie die Activity Map-Datenerfassung aktivieren möchten.

```js
s.trackInlineStats = true;
```
