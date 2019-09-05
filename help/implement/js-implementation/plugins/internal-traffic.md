---
title: Interner Traffic
description: Das Plugin für interne Traffic identifiziert Besucher dynamisch aus einem internen Netzwerk.
seo-description: Internal Traffic Plugin
seo-title: Internal Traffic Plugin
translation-type: tm+mt
source-git-commit: 8c2b28ee1ca2e9448b9dec99a0505d0fae525e94

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
1. Ändern Sie doplugins und legen Sie die evar fest: Das Plug-Plugin kann dann initialisiert werden, indem diese Codezeile im Abschnitt doplugins Ihres appmeasurement-Bibliothekscodes verwendet wird, wobei die in Schritt 1 definierte evar verwendet wird: `s.eVarXX = s.intCheck();`
Der variable Wert wird auf "intern" oder" extern" festgelegt.
1. Fügen Sie den Plug-In-Quellcode hinzu: Schließen Sie den Plugin-Code unter dem doplugins-Abschnitt Ihrer appmeasurement-Datei ein.

## Plugin-Quellcode

Fügen Sie diesen Code unter dem doplugins-Abschnitt Ihrer appmeasurement-Bibliothek hinzu.

```JavaScript
s.intCheck=new Function("",""
+"var s=this;if(document.cookie.indexOf('intChk=')==-1){try{document."
+"cookie='intChk=1';var x=new XMLHttpRequest(),y;x.open('GET',s.intUr"
+"l,false);x.send();if(x.status===200&&x.statusText==='OK'){y='intern"
+"al';}}catch(e){y='external'}finally{return y}}");
```

## Andere Hinweise

* Testen Sie stets die Installation von Plug-Ins, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie sie in einer Produktionsumgebung bereitstellen.
* Ihre Implementierung verwendet möglicherweise einen anderen Objektnamen als das standardmäßige Adobe Analytics "Objekt" . Aktualisieren Sie in diesem Fall den Objektnamen entsprechend.
* Wenn Sie ein Tag-Management-System verwenden, führen Sie die entsprechenden Schritte aus, um doplugins und andere benutzerdefinierte Plugins zu aktualisieren.
