---
title: trackInlineStats
description: Aktivieren oder deaktivieren Sie Activity Map in Ihrer Implementierung.
keywords: Activity Map deaktivieren
feature: Variables
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 78%

---

# trackInlineStats

Activity Map ist eine Funktion in Adobe Analytics, mit der Daten darüber erfasst werden, wo Besucher klicken und worauf sie klicken. Sie können diese Daten in Analytics-Berichten oder mithilfe eines Browser-Erweiterungs-Overlays anzeigen. Aktivieren Sie diese Variable, wenn Sie Activity Map-Funktionen verwenden möchten.

Wenn diese Option aktiviert ist, erfasst AppMeasurement Informationen zum Link und sendet diese Daten in der nächsten Bildanforderung. Informationen aus jedem Klick werden in einem Cookie mit der Bezeichnung `s_sq` gespeichert.

## Activity Map mithilfe des Web SDK

Das Web SDK unterstützt noch keine Activity Map-Datenerfassung.

## Aktivieren von ClickMap mithilfe der Adobe Analytics-Erweiterung

[!UICONTROL ClickMap aktivieren] ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Anmelden bei [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL ClickMap aktivieren] angezeigt wird.

Aktivieren Sie das Kontrollkästchen, um Activity Map-Tracking zu aktivieren.

## s.trackInlineStats in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

`s.trackInlineStats` ist ein boolescher Wert, der Activity Map-Tracking aktiviert oder deaktiviert. Der Standardwert lautet `false`. Setzen Sie diesen Wert auf `true`, wenn Sie die Activity Map-Datenerfassung aktivieren möchten.

```js
s.trackInlineStats = true;
```
