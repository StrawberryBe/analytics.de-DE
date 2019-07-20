---
description: Analysecode erstellt ein Image-Objekt – ein unsichtbares Bild, das auf einer Seite nicht angezeigt wird.
keywords: Analytics-Implementierung
seo-description: Analysecode erstellt ein Image-Objekt – ein unsichtbares Bild, das auf einer Seite nicht angezeigt wird.
seo-title: Platzieren von Analytics-Code im head-Tag
solution: Analytics
title: Platzieren von Analytics-Code im head-Tag
topic: Entwickler und Implementierung
uuid: e 8 f 91 d 3 c-cb 72-454 d -9 bd 4-ff 54 d 83 d 981 f
translation-type: tm+mt
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# Platzieren von Analytics-Code im head-Tag

Analysecode erstellt ein Image-Objekt – ein unsichtbares Bild, das auf einer Seite nicht angezeigt wird.

>[!NOTE]
>
>Dieser Abschnitt gilt nur für die s_ code. js-Implementierung. [Appmeasurement for javascript 1.0](../../../implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md#concept_F3957D7093A94216BD79F35CFC1557E8) unterstützt die Bereitstellung der Bibliothek und des Seitencodes im `<head>` Tag.

Bisher bestand eine übliche Implementierungsmethode darin, den Analytics javascript-Code zwischen der <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> und </head> Tags. Aufgrund der Platzierung des Codes zwischen den Tags hatte das Bild, das von der an Adobe-Server gesendeten Anforderung zurückgegeben wurde, keinerlei Auswirkungen auf das Seitenlayout. Durch die Platzierung des Codes im Head-Teil des Dokuments wird erreicht, dass der Code an einer vorderen Position im Code steht. Dadurch wird er früher ausgeführt, sodass Seitenansichten auch bei partiell geladenen Seiten effizienter gezählt werden können.

Bestimmte Elemente des Codes setzen voraus, dass ein Body-Objekt vorhanden ist. Da Webbrowser Code in der Reihenfolge ausführen, in der sie ihn erhalten, wird Analytics-JavaScript-Code, der im Kopfteil des Dokuments untergebracht ist, schon ausgeführt, bevor das Body-Objekt erstellt ist. Das hat zur Folge, dass Ihre Implementierung keine [!UICONTROL ClickMap]-Daten erfasst und keine automatische Verfolgung von Dateidownloads oder [!UICONTROL Exitlinks] verfügbar ist. Sie erhalten keine Daten über den Verbindungstyp oder die Homepage von Besuchern. Eine Platzierung des Codes im Kopfteil des Dokuments funktioniert zwar, schränkt aber die in Analytics verfügbaren Ergebnisse stark ein. Außerdem könnten sich Benutzer fragen, warum in bestimmten Berichten und Tools (wie [!UICONTROL ClickMap]) keine Daten aufgezeichnet werden.

Der Analytics-Code kann an einer beliebigen Stelle innerhalb des BODY-Tags platziert werden (<BODY></BODY>) einer gut formatierten HTML-Seite. Adobe empfiehlt, den Code in einer globalen Include-Datei auszulagern und diese am Anfang der Seite (innerhalb des HTML-Body-Tags) zu referenzieren. Der Code kann an einer beliebigen Stelle auf der Seite platziert werden, mit Ausnahme der folgenden Einschränkungen:

* Wenn Sie in eine Tabelle platziert werden, können Sie den Code nur innerhalb der <td></td> Tags. Fügen Sie beispielsweise den Code nicht zwischen einem öffnenden <tr> Tag und öffnen <td> -tag.
* Der Code, in dem die Variablem festgelegt werden, muss sich hinter dem Verweis auf die Datei s_code.js befinden.
* Make certain that the [!UICONTROL report suite ID]s in the *`s_account`* variable in the s_code.js file are set correctly. Diese Variable ist meist richtig eingestellt, wenn der Code über den Code-Manager für eine bestimmte Report Suite heruntergeladen oder von einem technischen Adobe-Berater zur Verfügung gestellt wurde.

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

