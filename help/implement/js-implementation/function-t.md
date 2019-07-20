---
description: Die s.t()-Funktion stellt aus allen auf der Seiten definierten Variablen eine Bildanforderung zusammen und sendet diese an unsere Server.
keywords: track; Analytics-Implementierung; Seitenverfolgung; track-Seite
seo-description: Die s.t()-Funktion stellt aus allen auf der Seiten definierten Variablen eine Bildanforderung zusammen und sendet diese an unsere Server.
seo-title: Die s.t()-Funktion – Seitenverfolgung
solution: Analytics
subtopic: Funktionen
title: Die s.t()-Funktion – Seitenverfolgung
topic: Entwickler und Implementierung
uuid: 67696 e 46-1 e 0 d -4200-bmode -4217 d 1023948
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Die s.t()-Funktion – Seitenverfolgung

Die s.t()-Funktion stellt aus allen auf der Seiten definierten Variablen eine Bildanforderung zusammen und sendet diese an unsere Server.

## Eigenschaften der Funktion {#section_DB1F3E216DCD4E12AE42BBDCD25B9626}

* Wenn der Aufruf der [!UICONTROL s.t()]-Funktion entfernt wird, können keine Daten mehr zu [!DNL Analytics] gelangen. Je mehr [!UICONTROL s.t()]-Aufrufe vorhanden sind, umso mehr Bildanforderungen werden veranlasst (wodurch sich der für Ihre Website verzeichnete Datenverkehr vervielfacht).

* Wenn beim Laden einer einzelnen Seite mehrere Bildanforderungen veranlasst werden sollen, empfiehlt sich ein Einsatz der [!UICONTROL s.tl()]-Funktion.
* Ein Auslösen dieser Funktion erhöht die Seitenansichten ([!UICONTROL pageviews]) und enthält immer die Variable [!UICONTROL s.pageName].

## Implementierung {#section_F75C7BD4A8954CD5BE066C6B88A4A01C}

Wenn Code im [!UICONTROL Code-Manager] generiert wird, steht am Ende des Seiten-Codes Folgendes:

```js
var s_code=s.t();if(s_code)document.write(s_code)//--></script> 
<script language="JavaScript" type="text/javascript"><!--if(navigator.appVersion.indexOf('MSIE')>=0)document.write(unescape('%3C')+'\!-'+'-')//--></script> 
<noscript><img src="https://yournameserver.112.2o7.net/b/ss/yourreportsuiteid/1/H.23.6--NS/0" height="1" width="1" border="0" alt="" /></noscript> 
```

Jede Codezeile erfüllt einen bestimmten Zweck:

```js
var s_code=s.t();if(s_code)document.write(s_code)//-->
```

Das ist die Codezeile, in der die JavaScript-Funktion aufgerufen wird. Die Variable [!UICONTROL s_code] und die zugehörige „document.write“-Methode sind für Browser gedacht, die Image-Objekte nicht unterstützen (Netscape-Browser vor der Version 3 und Internet Explorer vor der Version 4, das sind weniger als rund 0,5 % aller Internetbenutzer).

```js
<script language="JavaScript" type="text/javascript"><!--if(navigator.appVersion.indexOf('MSIE')>=0)document.write(unescape('%3C')+'\!-'+'-')//--></script> 
<noscript><img  
src="https://yournameserver.112.2o7.net/b/ss/yourreportsuiteid/1/H.23.6--NS/0" height="1" width="1" border="0" alt="" />
```

Wenn Sie noch weitere Fragen zu der [!UICONTROL s.t()]-Funktion haben, wenden Sie sich bitte an Ihren Kundenbetreuer. Dieser kann ein Treffen mit einem Berater für Adobe-Implementierungen arrangieren, von dem Sie dann weitere Hilfe erhalten.
