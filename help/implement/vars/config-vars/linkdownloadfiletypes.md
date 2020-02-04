---
title: linkDownloadFileTypes
description: Legen Sie Dateierweiterungen fest, die automatisch als Downloadlinks verfolgt werden.
translation-type: tm+mt
source-git-commit: 8f7baa770f800ffe800e760f1eca59911d3db348

---


# linkDownloadFileTypes

Wenn `trackDownloadLinks` die Einstellung auf festgelegt ist `true` und ein Besucher auf einen Link klickt, prüft AppMeasurement die URL des Links auf Dateierweiterungen. Wenn die Link-URL einen in enthaltenen Dateityp enthält, `linkDownloadFileTypes`wird automatisch eine Bildanforderung für den Download-Link gesendet.

Passen Sie `linkDownloadFileTypes` an, welche Dateierweiterungen als Downloadlinks gezählt werden sollen.

> [!NOTE] Nur tatsächliche Klicks werden automatisch verfolgt. Die folgenden Linktypen werden nicht automatisch verfolgt:
>
> * Dateidownloads, die beim Laden einer Seite automatisch starten
> * Downloads, die nach einer Umleitung ausgelöst werden
> * Klicken Sie mit der rechten Maustaste und wählen Sie &quot;Ziel speichern unter...&quot;.
> * Links, die JavaScript verwenden, z. B. `javascript:openLink()`
>
> 
Bei diesen Downloadtypen können Sie die `tl()` Funktion manuell aufrufen.

Wenn ein angeklickter Link sowohl den Kriterien für Ausstiegslinks als auch für Downloadlinks entspricht, hat der Linktyp Priorität.

## Herunterladen von Erweiterungen in Adobe Experience Platform Launch

Download-Erweiterungen sind eine Liste von Dateierweiterungen mit einem Feld, um weitere Informationen zum Konfigurieren der Adobe Analytics-Erweiterung im Akkordeon &quot; [!UICONTROL Linktracking] &quot;hinzuzufügen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Linktracking] &quot;, in dem das Feld &quot; [!UICONTROL Download-Erweiterungen] &quot;angezeigt wird.

Fügen Sie der Liste Dateierweiterungen hinzu, indem Sie Text in das Feld eingeben und auf [!UICONTROL Hinzufügen]klicken. Entfernen Sie Dateierweiterungen aus der Liste, indem Sie auf das entsprechende X-Symbol klicken.

## s.linkDownloadFileTypes in AppMeasurement und Starten des benutzerdefinierten Codeeditors

Die `s.linkDownloadFileTypes` Variable ist eine Zeichenfolge aus kommagetrennten Dateierweiterungen. Verwenden Sie keine Leerzeichen.

Wenn diese Variable nicht definiert ist, funktioniert die automatische Verfolgung von Downloadlinks nicht (auch wenn `trackDownloadLinks` dies `true`der Fall ist).

```js
s.linkDownloadFileTypes = "doc,docx,eps,jpg,png,svg,xls,ppt,pptx,pdf,xlsx,tab,csv,zip,txt,vsd,vxd,xml,js,css,rar,exe,wma,mov,avi,wmv,mp3,wav,m4v"
```
