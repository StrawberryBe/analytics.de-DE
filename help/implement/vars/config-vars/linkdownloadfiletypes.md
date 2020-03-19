---
title: linkDownloadFileTypes
description: Legen Sie Dateierweiterungen fest, die automatisch als Downloadlinks verfolgt werden.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkDownloadFileTypes

Wenn [`trackDownloadLinks`](trackdownloadlinks.md) die Option aktiviert ist und ein Besucher auf einen Link klickt, prüft AppMeasurement die URL des Links auf Dateierweiterungen. Wenn die Link-URL einen in enthaltenen Dateityp enthält, `linkDownloadFileTypes`wird automatisch eine Bildanforderung für den Download-Link gesendet.

Passen Sie `linkDownloadFileTypes` an, welche Dateierweiterungen als Downloadlinks gezählt werden sollen.

> [!NOTE] Nur tatsächliche Klicks werden automatisch verfolgt. Die folgenden Linktypen werden nicht automatisch verfolgt:
>
> * Datei lädt diesen Beginn automatisch herunter, wenn eine Seite geladen wird
> * Downloads, die nach einer Umleitung ausgelöst werden
> * Klicken Sie mit der rechten Maustaste und wählen Sie &quot;Zielgruppe speichern unter...&quot;.
> * Links, die JavaScript verwenden, z. B. `javascript:openLink()`
>
> 
Bei diesen Downloadtypen können Sie die [`tl()`](../functions/tl-method.md) Methode manuell aufrufen.

Wenn ein angeklickter Link sowohl den Kriterien für Ausstiegslinks als auch für Downloadlinks entspricht, hat der Linktyp Priorität.

## Herunterladen von Erweiterungen in Adobe Experience Platform Launch

Download-Erweiterungen sind eine Liste von Dateierweiterungen mit einem Feld, um mehr unter dem [!UICONTROL Link Tracking] Akkordeon hinzuzufügen, wenn Sie die Adobe Analytics-Erweiterung konfigurieren.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Link Tracking] Akkordeon, das das [!UICONTROL Download Extensions] Feld aufdeckt.

Hinzufügen Sie Dateierweiterungen zur Liste durch Eingabe von Text in das Feld und Klicken auf [!UICONTROL Add]. Entfernen Sie Dateierweiterungen aus der Liste, indem Sie auf das entsprechende X-Symbol klicken.

## s.linkDownloadFileTypes in AppMeasurement und Starten des benutzerdefinierten Codeeditors

Die `s.linkDownloadFileTypes` Variable ist eine Zeichenfolge aus kommagetrennten Dateierweiterungen. Verwenden Sie keine Leerzeichen.

Wenn diese Variable nicht definiert ist, funktioniert die automatische Verfolgung von Downloadlinks nicht (auch wenn [`trackDownloadLinks`](trackdownloadlinks.md) dies `true`der Fall ist).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v";
```
