---
description: Stellen Sie sicher, dass auf der Seite korrekt auf die JS-Datei verwiesen wird. Der Pfad kann entweder relativ zum aktuellen Dokument oder in absoluter Form angegeben werden.
keywords: Analytics-Implementierung
seo-description: Stellen Sie sicher, dass auf der Seite korrekt auf die JS-Datei verwiesen wird. Der Pfad kann entweder relativ zum aktuellen Dokument oder in absoluter Form angegeben werden.
seo-title: JavaScript-JS-Datei
solution: Analytics
title: JavaScript-JS-Datei
topic: Entwickler und Implementierung
uuid: 6e83223f-2127-41d3-9806-bd085fa2a747
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# JavaScript-JS-Datei

Stellen Sie sicher, dass auf der Seite korrekt auf die JS-Datei verwiesen wird. Der Pfad kann entweder relativ zum aktuellen Dokument oder in absoluter Form angegeben werden.

```js
<script language="JavaScript" 
src="https://www.sampleco.com/javascript/includes/s_code.js"></script>
```

Wenn einige Seiten der Website mit einem sicheren Protokoll (HTTPS) geladen werden und auf die [!DNL AppMeasurement] für JavaScript-Datei verweisen, müssen Sie sicherstellen, dass der Verweis auf die Datei sicher ist (HTTPS), oder den Verweiscode wie unten gezeigt formulieren. Dieses Beispiel übernimmt das Protokoll der aktuellen Seite und unterdrückt die Warnung, dass einige Elemente nicht sicher sind.

```js
<script language="JavaScript" 
src="//www.sampleco.com/javascript/includes/s_code.js"></script>
```

Vergewissern Sie sich, dass für die [!DNL .JS]-Datei auf den Webservern entsprechende Berechtigungen festgelegt sind, damit die Datei von Besuchern der Website heruntergeladen und ausgeführt werden kann. Wenn auf Entwicklungsservern eine andere [!DNL .JS]-Datei verwendet wird, setzen Sie das Attribut „schreibgeschützt“ für die [!DNL .JS]-Datei auf Produktionsservern, damit die Datei nicht überschrieben wird. Falls Einstellungen verändert wurden, vergewissern Sie sich, dass zu Beginn der [!DNL .JS]-Datei die folgenden Einstellungen passend festgelegt sind:

```js
/************************** CONFIG SECTION **************************/
/* You may add or alter any code config here.                       */
/* Link Tracking Config */
s.trackDownloadLinks=false /* true for download tracking */
s.trackExternalLinks=false /* true for exit link tracking */
s.trackInlineStats=false /* true for ClickMap support */
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,doc,pdf,xls"
s.linkInternalFilters="javascript:"
s.linkLeaveQueryString=false
s.linkTrackVars="None" 
s.linkTrackEvents="None"
```

Wenn *`s_account`* oben in der [!DNL .JS]-Datei ein Wert zugewiesen ist, müssen Sie überprüfen, ob die (in der [!UICONTROL s_account ]-Variable eingetragene) Report Suite-ID korrekt ist. Stellen Sie außerdem sicher, dass der Code auf der Seite nicht die [!UICONTROL Report Suite ID] (Variable *`s_account`*) setzt.

Überprüfen Sie die Bildanforderung und die Variablen dahingehend, ob die Bildanforderung auch wirklich von der [!DNL .JS]-Datei erstellt wird und nicht von der Ausweichmethode (die im oben gezeigten Beispiel im dritten Teil des „Aufteilungs“-Codes steht). Das kann man daran erkennen, dass Bildanforderungen, die nur ein Minimum an Informationen enthalten, von der Ausweichmethode stammen.
