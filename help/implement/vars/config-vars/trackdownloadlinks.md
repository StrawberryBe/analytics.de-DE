---
title: trackDownloadLinks
description: Aktivieren oder deaktivieren Sie das automatische Linktracking für Downloadlinks.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# trackDownLoadLinks

Adobe offers the ability to track download links without manually setting the [`tl()`](../functions/tl-method.md) method for each download link. Aktivieren Sie diese Variable, wenn Sie das automatische Linktracking für Downloadlinks verwenden möchten.

Wenn diese Option aktiviert ist, vergleicht AppMeasurement alle geklickten Link-URLs mit den Werten in [`linkDownloadFileTypes`](linkdownloadfiletypes.md). Bei Übereinstimmung wird automatisch ein Download-Linktracking-Aufruf ausgelöst.

## Verfolgen von Downloadlinks in Adobe Experience Platform Launch

„Downloadlinks verfolgen“ ist ein Kontrollkästchen unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Kontrollkästchen [!UICONTROL Downloadlinks verfolgen] angezeigt wird.

Aktivieren Sie das Kontrollkästchen, um das automatische Tracking von Downloadlinks zu aktivieren.

## s.trackDownloadLinks in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

`s.trackDownloadLinks` ist ein boolescher Wert, der das automatische Tracking von Downloadlinks aktiviert oder deaktiviert. If you do not want to track download links, or would prefer to manually call the `tl()` method to track downloads, set this variable to `false`.

```js
s.trackDownloadLinks = true;
```
