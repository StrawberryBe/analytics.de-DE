---
title: Interner Traffic
description: Das Plugin für interne Traffic identifiziert Besucher dynamisch aus einem internen Netzwerk.
seo-description: Internal Traffic Plugin
seo-title: Internal Traffic Plugin
translation-type: tm+mt
source-git-commit: ee0cb9b64a3915786f8f77d80b55004daa68cab6

---


# Interner Traffic

Das Plugin für interne Traffic identifiziert Besucher dynamisch aus einem internen Netzwerk.

Die Identifizierung interner und externer Traffic fördert eine größere Genauigkeit in allen Berichtstypen, indem er einen Mechanismus bereitstellt, der erfasste Daten filtert und segmentiert. Eine korrekte Implementierung würde ebenfalls den Bedarf an VISTA-Regeln oder Verarbeitungsregeln beseitigen, die typische Ansätze zur Identifizierung solcher Datenverkehr sind.

## Wie funktioniert das Plugin für interne Traffic?

Das Plug-In versucht, eine Datei zu laden, die nur in Ihrem internen Netzwerk/Intranet verfügbar wäre, z. B. ein transparentes 1 x 1-Pixel. Wenn er erfolgreich geladen wird, wird der Traffic für diesen Besucher als intern identifiziert. Alles andere wäre externer Traffic.

## Zu beachten

* Der einzige Nachteil dieser Vorgehensweise besteht darin, dass ein 404-Fehler in der Browserkonsole für externe Besucher auf der ersten Seite ihres Besuchs angezeigt wird. Dies wirkt sich nicht auf die Benutzererfahrung aus.
* Wir empfehlen dringend, die Genehmigung Ihres Netzwerks oder infosec-Teams zu erhalten, bevor Sie ein intern gehostetes Pixel laden können.
* Obwohl das Plug-plugin den Traffic nicht zu einer anderen Report Suite verschieben oder ihn aus der Berichterstellung ausschließen kann (wie dies ggf. mit einer VISTA-Regel möglich ist), kann die benutzerdefinierte Logik in die Implementierung eingeschlossen werden, sodass diese Funktion clientseitig eingesetzt werden kann.

## Implementierung

1. Fügen Sie Ihr Intranet Pixel hinzu: Sie können in Ihrem Intranet beliebige Dateitypen hinzufügen, auf die das Plug-in zugreifen würde. Ein transparentes 1 x 1-Pixel wird empfohlen. Sie sollte an einer Stelle in Ihrem Intranet platziert werden, auf die in Ihrem (n) internen Netzwerk (n) zugegriffen werden kann.
1. Eine evar konfigurieren: In Ihrer Ziel-Report Suite muss eine evar hinzugefügt werden. Es sollte über einen Ablauf von "Besuch" und die Zuordnung von" Ausgangswert (Erster)" verfügen.
1. Definieren Sie die interne URL: Definieren Sie innerhalb der appmeasurement-Konfigurationsvariablen und bevor doplugins instanziiert werden, die interne URL-Variable (s. inturl) für das Pixel oder andere Dateien, die für die Traffic-Prüfung verwendet werden können. Beispiel: `s.intURL = "https://www.yourdomainhere.com/trafficCheck.gif"`
1. Modify doPlugins and set the eVar: The plugin can then be initialized by including this line of code within the doPlugins section of your AppMeasurement library code, using the eVar defined in step one: `s.eVarXX = s.intCheck();`
The variable value will be set to “internal” or “external”.
1. Fügen Sie den Plug-In-Quellcode hinzu: Schließen Sie den Plugin-Code unter dem doplugins-Abschnitt Ihrer appmeasurement-Datei ein.

## Plugin-Quellcode

Fügen Sie diesen Code unter dem doplugins-Abschnitt Ihrer appmeasurement-Bibliothek hinzu.

```s.intCheck=new Function("",""
+"var s=this;if(document.cookie.indexOf('intChk=')==-1){try{document."
+"cookie='intChk=1';var x=new XMLHttpRequest(),y;x.open('GET',s.intUr"
+"l,false);x.send();if(x.status===200&&x.statusText==='OK'){y='intern"
+"al';}}catch(e){y='external'}finally{return y}}");```

## Other Notes

* Always test plug-in installations to ensure that data collection happens as expected before deploying them in a production environment.
* Your implementation might be using a different object name than the default Adobe Analytics "s" object. If so, please update the object name accordingly.
* If you employ a Tag Management System, please follow its steps to update doPlugins and the other custom plugins.

