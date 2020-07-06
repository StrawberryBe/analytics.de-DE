---
title: linkDownloadFileTypes
description: Legen Sie Dateierweiterungen fest, die automatisch als Downloadlinks verfolgt werden.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 100%

---


# linkDownloadFileTypes

Wenn [`trackDownloadLinks`](trackdownloadlinks.md) aktiviert ist und ein Besucher auf einen Link klickt, überprüft AppMeasurement die URL des Links auf Dateityp-Erweiterungen. Wenn die Link-URL einen in `linkDownloadFileTypes` gefundenen Dateityp enthält, wird automatisch eine Bildanforderung für den Downloadlink gesendet.

Verwenden Sie `linkDownloadFileTypes`, um anzupassen, welche Dateierweiterungen Sie als Download-Links zählen möchten.

>[!NOTE]
>
>Nur tatsächliche Klicks werden automatisch verfolgt. Die folgenden Link-Typen werden nicht automatisch verfolgt:
>
> * Datei-Downloads, die beim Laden einer Seite automatisch eingeleitet werden
> * Downloads, die nach einer Umleitung ausgelöst werden
> * Mit der rechten Maustaste klicken und „Ziel speichern unter...“ auswählen
> * Links, die JavaScript verwenden, wie z. B. `javascript:openLink()`

>
> 
Bei diesen Download-Typen können Sie die [`tl()`](../functions/tl-method.md)-Methode manuell aufrufen.

Wenn ein geklickter Link sowohl den Kriterien für Exitlinks als auch für Downloadlinks entspricht, hat der Downloadlink-Typ Priorität.

## Download-Erweiterungen in Adobe Experience Platform Launch

Download-Erweiterungen sind eine Liste von Dateierweiterungen mit einem Feld, um bei der Konfiguration der Adobe Analytics-Erweiterung unter dem Akkordeon [!UICONTROL Linktracking] weitere hinzuzufügen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Feld [!UICONTROL Download-Erweiterungen] angezeigt wird.

Fügen Sie der Liste Dateierweiterungen hinzu, indem Sie Text in das Feld eingeben und auf [!UICONTROL Hinzufügen] klicken. Entfernen Sie Dateierweiterungen aus der Liste, indem Sie auf das entsprechende X-Symbol klicken.

## s.linkDownloadFileTypes in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.linkDownloadFileTypes`-Variable ist eine Zeichenfolge aus kommagetrennten Dateierweiterungen. Verwenden Sie keine Leerzeichen.

Wenn diese Variable nicht definiert ist, funktioniert das automatische Tracking von Downloadlinks nicht (auch wenn [`trackDownloadLinks`](trackdownloadlinks.md) den Wert `true` aufweist).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
