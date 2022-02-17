---
title: trackDownloadLinks
description: Aktivieren oder deaktivieren Sie das automatische Linktracking für Downloadlinks.
feature: Variables
exl-id: d92f722b-d605-40ad-bb55-ec71219a47e3
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 100%

---

# trackDownLoadLinks

Adobe bietet die Möglichkeit, Downloadlinks zu verfolgen, ohne die [`tl()`](../functions/tl-method.md)-Methode für jeden Downloadlink manuell festzulegen. Aktivieren Sie diese Variable, wenn Sie das automatische Linktracking für Downloadlinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle geklickten Link-URLs mit den Werten in [`linkDownloadFileTypes`](linkdownloadfiletypes.md). Bei Übereinstimmung wird automatisch ein Download-Linktracking-Aufruf ausgelöst.

## Tracking von Downloadlinks mithilfe von Tags in Adobe Experience Platform

„Downloadlinks verfolgen“ ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL Downloadlinks verfolgen] angezeigt wird.

Aktivieren Sie das Kontrollkästchen, um das automatische Tracking von Downloadlinks zu aktivieren.

## s.trackDownloadLinks in AppMeasurement und im benutzerdefinierten Code-Editor

`s.trackDownloadLinks` ist ein boolescher Wert, der das automatische Tracking von Downloadlinks aktiviert oder deaktiviert. Wenn Sie Downloadlinks nicht verfolgen oder die `tl()`-Methode zum Tracking von Downloads lieber manuell aufrufen möchten, setzen Sie diese Variable auf `false`.

```js
s.trackDownloadLinks = true;
```
