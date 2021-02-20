---
title: trackExternalLinks
description: Aktivieren oder deaktivieren Sie das automatische Linktracking für Exitlinks.
translation-type: tm+mt
source-git-commit: 94218548dc4e3efd57df95c992003e94640e4330
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---


# trackExternalLinks

Adobe bietet die Möglichkeit, ausgehende Links zu verfolgen, ohne die [`tl()`](../functions/tl-method.md)-Methode für jeden Exitlink manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie das automatische Linktracking für Exitlinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle geklickten Link-URLs mit den Werten in [`linkInternalFilters`](linkinternalfilters.md) und [`linkExternalFilters`](linkexternalfilters.md). Bei Übereinstimmung wird automatisch ein Exitlinktracking-Aufruf ausgelöst.

## Verfolgen von ausgehenden Links in Adobe Experience Platform Launch

„Ausgehende Links verfolgen“ ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL Ausgehende Links verfolgen] angezeigt wird.

Aktivieren Sie das Kontrollkästchen, um das automatische Tracking von Exitlinks zu aktivieren.

## s.trackExternalLinks in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

`s.trackExternalLinks` ist ein boolescher Wert, der das automatische Tracking von Exitlinks aktiviert oder deaktiviert. Wenn Sie ausgehende Links nicht verfolgen oder die `tl()`-Methode zum Tracking von Exitlinks lieber manuell aufrufen möchten, setzen Sie diese Variable auf `false`.

```js
s.trackExternalLinks = true;
```
