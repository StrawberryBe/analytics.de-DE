---
title: trackInlineStats
description: Aktivieren oder deaktivieren Sie ClickMap in Ihrer Implementierung.
keywords: ClickMap deaktivieren
feature: Variables
exl-id: a52adc1d-1be7-4002-b393-7ce66332b483
source-git-commit: a3df69f7de45ba3694e1212e5c16a10bb4602cd6
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 31%

---

# trackInlineStats

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt. Siehe [Activity Map aktivieren](/help/analyze/activity-map/activitymap-getting-started/activitymap-getting-started-admins/activitymap-enable.md) anstatt.

ClickMap ist eine veraltete Funktion in Adobe Analytics, mit der Daten darüber erfasst werden, wo Besucher klicken und worauf sie klicken. Die Funktion wurde durch [Activity Map](/help/analyze/activity-map/activity-map.md).

Wenn diese Option aktiviert ist, erfasst AppMeasurement Informationen zum Link und sendet diese Daten in der nächsten Bildanforderung. Informationen aus jedem Klick werden in einem Cookie mit der Bezeichnung `s_sq`.

## Aktivieren von ClickMap mithilfe der Adobe Analytics-Erweiterung

[!UICONTROL ClickMap aktivieren] ist ein Kontrollkästchen unter dem [!UICONTROL Linktracking] Akkordeon beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche **[!UICONTROL Konfigurieren]**.
4. Erweitern Sie die [!UICONTROL Linktracking] Akkordeon, das die [!UICONTROL ClickMap aktivieren] aktivieren.

>[!NOTE]
>
>Dieses Kontrollkästchen unterscheidet sich vom [!UICONTROL Activity Map verwenden] Kontrollkästchen, das sich unter dem [!UICONTROL Bibliotheksverwaltung] Akkordeon.

## s.trackInlineStats in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.trackInlineStats` ist ein boolescher Wert, der das ClickMap-Tracking aktiviert oder deaktiviert. Da die Funktion eingestellt wurde, empfiehlt Adobe nicht, diese Variable festzulegen. Der Standardwert lautet `false`.

```js
s.trackInlineStats = false;
```
