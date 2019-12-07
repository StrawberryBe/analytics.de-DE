---
description: Analysecode erstellt ein Image-Objekt – ein unsichtbares Bild, das auf einer Seite nicht angezeigt wird.
keywords: Analytics Implementation
title: Analytics-Code im Head-Tag platzieren
topic: Developer and implementation
uuid: e8f91d3c-cb72-454d-9bd4-ff54d83d981f
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Analytics-Code im Head-Tag platzieren

Analysecode erstellt ein Image-Objekt – ein unsichtbares Bild, das auf einer Seite nicht angezeigt wird.

>[!NOTE]
>
>Dieser Abschnitt gilt nur für die s_code.js-Implementierung. [AppMeasurement for JavaScript 1.0](/help/implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md) unterstützt die Bereitstellung von Bibliothek und Seiten-Code im `<head>`-Tag.

Zuvor bestand die gängige Implementierungsmethode darin, den JavaScript-Code für Analytics zwischen den <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> und </head> Tags zu platzieren. Aufgrund der Platzierung des Codes zwischen den Tags hatte das Bild, das von der an Adobe-Server gesendeten Anforderung zurückgegeben wurde, keinerlei Auswirkungen auf das Seitenlayout. Durch die Platzierung des Codes im Head-Teil des Dokuments wird erreicht, dass der Code an einer vorderen Position im Code steht. Dadurch wird er früher ausgeführt, sodass Seitenansichten auch bei partiell geladenen Seiten effizienter gezählt werden können.

Bestimmte Elemente des Codes setzen voraus, dass ein Body-Objekt vorhanden ist. Da Webbrowser Code in der Reihenfolge ausführen, in der sie ihn erhalten, wird Analytics-JavaScript-Code, der im Kopfteil des Dokuments untergebracht ist, schon ausgeführt, bevor das Body-Objekt erstellt ist. Das hat zur Folge, dass Ihre Implementierung keine [!UICONTROL ClickMap]-Daten erfasst und keine automatische Verfolgung von Dateidownloads oder [!UICONTROL Exitlinks] verfügbar ist. Sie erhalten keine Daten über den Verbindungstyp oder die Homepage von Besuchern. Eine Platzierung des Codes im Kopfteil des Dokuments funktioniert zwar, schränkt aber die in Analytics verfügbaren Ergebnisse stark ein. Außerdem könnten sich Benutzer fragen, warum in bestimmten Berichten und Tools (wie [!UICONTROL ClickMap]) keine Daten aufgezeichnet werden.

Der Analytics-Code kann an einer beliebigen Stelle innerhalb der BODY-Tags (<BODY></BODY>) einer wohlgeformten HTML-Seite platziert werden. Adobe empfiehlt, den Code in einer globalen Include-Datei auszulagern und diese am Anfang der Seite (innerhalb des HTML-Body-Tags) zu referenzieren. Der Code kann an einer beliebigen Stelle auf der Seite platziert werden, mit Ausnahme der folgenden Einschränkungen:

* In einer Tabelle darf der Code nur innerhalb der <td></td> Tags stehen. Platzieren Sie beispielsweise den Code nicht zwischen einem ersten <tr> und einem ersten <td> Tag.
* Der Code, in dem die Variablem festgelegt werden, muss sich hinter dem Verweis auf die Datei s_code.js befinden.
* Vergewissern Sie sich, dass die [!UICONTROL Report Suite-IDs ]in der Variable *`s_account`* in der Datei s_code.js korrekt festgelegt sind. Diese Variable ist meist richtig eingestellt, wenn der Code über den Code-Manager für eine bestimmte Report Suite heruntergeladen oder von einem technischen Adobe-Berater zur Verfügung gestellt wurde.

Wenn Sie Analytics mit Target integrieren möchten, muss die JavaScript-Include-Datei am Ende der Seite platziert werden. Eine korrekte Platzierung von Analytics-Code zeigt das nächste Beispiel:

```js
<html> 
<head></head> 
<body> 
<!-- Analytics code version: H.20.3.
Copyright 1997-2009 Omniture, Inc. More info available at 
https://www.omniture.com --> 
<script language="JavaScript" type="text/javascript" src="https://www.yourdomain.com/js/s_code.js"></script> 
<script language="JavaScript" type="text/javascript"><!-- 
/* You may give each page an identifying name, server, and channel on 
the next lines. */ 
s.pageName="" 
s.server="" 
s.channel="" 
s.pageType="" 
s.prop1="" 
s.prop2="" 
s.prop3="" 
s.prop4="" 
s.prop5="" 
/* Conversion Variables */ 
s.campaign="" 
s.state="" 
s.zip="" 
s.events="" 
s.products="" 
s.purchaseID="" 
s.eVar1="" 
s.eVar2="" 
s.eVar3="" 
s.eVar4="" 
s.eVar5="" 
/************* DO NOT ALTER ANYTHING BELOW THIS LINE ! **************/ 
var s_code=s.t();if(s_code)document.write(s_code)//--></script> 
<!-- End Analytics code version: H.20.3. --> 
</body> 
</html> 
```

