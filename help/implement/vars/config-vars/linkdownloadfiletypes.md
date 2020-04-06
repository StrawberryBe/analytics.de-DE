---
title: linkDownloadFileTypes
description: Legen Sie Dateierweiterungen fest, die automatisch als Downloadlinks verfolgt werden.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkDownloadFileTypes

When [`trackDownloadLinks`](trackdownloadlinks.md) is enabled and a visitor clicks on a link, AppMeasurement checks the URL of the link for filetype extensions. Wenn die Link-URL einen in `linkDownloadFileTypes` gefundenen Dateityp enthält, wird automatisch eine Bildanforderung für den Downloadlink gesendet.

Verwenden Sie `linkDownloadFileTypes`, um anzupassen, welche Dateierweiterungen Sie als Download-Links zählen möchten.

>[!NOTE] Nur tatsächliche Klicks werden automatisch verfolgt. Die folgenden Link-Typen werden nicht automatisch verfolgt:
>
> * Datei-Downloads, die beim Laden einer Seite automatisch eingeleitet werden
> * Downloads, die nach einer Umleitung ausgelöst werden
> * Mit der rechten Maustaste klicken und „Ziel speichern unter...“ auswählen
> * Links, die JavaScript verwenden, wie z. B. `javascript:openLink()`
>
> 
For these download types, you can manually call the [`tl()`](../functions/tl-method.md) method.

Wenn ein geklickter Link sowohl den Kriterien für Exitlinks als auch für Downloadlinks entspricht, hat der Downloadlink-Typ Priorität.

## Download-Erweiterungen in Adobe Experience Platform Launch

Download Extensions is a list of file extensions with a field to add more under the [!UICONTROL Link Tracking] accordion when configuring the Adobe Analytics extension.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Link Tracking] Akkordeon, das das [!UICONTROL Download Extensions] Feld aufdeckt.

Add file extensions to the list by entering text in the field and clicking [!UICONTROL Add]. Entfernen Sie Dateierweiterungen aus der Liste, indem Sie auf das entsprechende X-Symbol klicken.

## s.linkDownloadFileTypes in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.linkDownloadFileTypes`-Variable ist eine Zeichenfolge aus kommagetrennten Dateierweiterungen. Verwenden Sie keine Leerzeichen.

Wenn diese Variable nicht definiert ist, funktioniert das automatische Tracking von Downloadlinks nicht (auch wenn [`trackDownloadLinks`](trackdownloadlinks.md) den Wert `true` aufweist).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
