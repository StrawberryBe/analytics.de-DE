---
title: Interner Traffic
description: Das Plug-in „Interner Traffic“ identifiziert dynamisch Besucher, die aus einem internen Netzwerk stammen.
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Interner Traffic

Das Plug-in „Interner Traffic“ identifiziert dynamisch Besucher, die aus einem internen Netzwerk stammen.

Die Identifizierung des internen und externen Traffics fördert eine höhere Genauigkeit in allen Berichtstypen, indem ein Mechanismus zur Filterung und Segmentierung der erfassten Daten bereitgestellt wird. Bei ordnungsgemäßer Implementierung entfällt dadurch auch die Notwendigkeit einer VISTA-Regel oder einer Verarbeitungsregel, die typische Ansätze zur Identifizierung des Traffics darstellen.

## Wie funktioniert das Plug-in „Interner Traffic“?

Das Plug-in versucht, eine Datei zu laden, die nur innerhalb des internen Netzwerks/Intranets verfügbar wäre, d. h. ein transparentes 1x1-Pixel. Bei erfolgreichem Laden würde der Traffic für diesen Besucher als intern identifiziert. Alles andere wäre externer Traffic.

## Zu beachten

* Der einzige Nachteil dieses Ansatzes ist, dass auf der ersten Seite des Besuchs in der Browser-Konsole ein Fehler 404 für externe Besucher angezeigt wird. Dies hat keine Auswirkungen auf die Benutzererfahrung.
* Wir empfehlen dringend, dass Sie die Genehmigung von Ihrem Netzwerk- oder InfoSec-Team erhalten, bevor Sie versuchen, ein Pixel zu laden, das intern gehostet wird.
* Obwohl das Plug-in Traffic nicht zu einer anderen Report Suite verschiebt oder von der Berichterstellung ausschließt (wie dies bei einer VISTA-Regel der Fall ist), kann eine benutzerdefinierte Logik in die Implementierung einbezogen werden, sodass diese Funktion Client-seitig eingesetzt werden kann.

## Implementierung

1. Fügen Sie Ihr Intranet-Pixel hinzu: Sie können beliebige Dateitypen in Ihrem Intranet hinzufügen, auf die das Plug-in zugreifen möchte. Es wird ein transparentes 1x1-Pixel empfohlen. Es sollte an einem Ort in Ihrem Intranet platziert werden, der von Ihrem internen Netzwerk bzw. Ihren internen Netzen aus leicht zugänglich ist.
1. Konfigurieren einer eVar: In Ihrer Ziel-Report Suite muss eine eVar hinzugefügt werden. Sie sollte einen Ablauf von „Besuch“ und eine Zuordnung von „Ausgangswert (Erster)“ haben.
1. Definieren Sie die interne URL: Definieren Sie innerhalb der AppMeasurement-Konfigurationsvariablen und vor der Instanziierung von doPlugins die interne URL-Variable (s.intURL) für die Pixel- oder andere Datei, die für die Traffic-Prüfung verwendet werden kann. Beispiel: `s.intURL = "https://www.yourdomainhere.com/trafficCheck.gif"`
1. Ändern Sie doPlugins und legen Sie die eVar fest: Das Plug-in kann dann initialisiert werden, indem Sie diese Codezeile im Abschnitt „doPlugins“ Ihres AppMeasurement-Bibliothekscodes einschließen und dabei die in Schritt 1 definierte eVar verwenden: `s.eVarXX = s.intCheck();`
Der Variablenwert wird auf „intern“ oder „extern“ eingestellt.
1. Fügen Sie den Plug-in-Quellcode hinzu: Schließen Sie den Plug-in-Code unter dem doPlugins-Abschnitt Ihrer AppMeasurement-Datei ein.

## Plug-in-Quellcode

Fügen Sie diesen Code unter dem Abschnitt doPlugins Ihrer AppMeasurement-Bibliothek hinzu.

```JavaScript
s.intCheck=new Function("",""
+"var s=this;if(document.cookie.indexOf('intChk=')==-1){try{document."
+"cookie='intChk=1';var x=new XMLHttpRequest(),y;x.open('GET',s.intUr"
+"l,false);x.send();if(x.status===200&&x.statusText==='OK'){y='intern"
+"al';}}catch(e){y='external'}finally{return y}}");
```

## Weitere Hinweise

* Testen Sie stets die Installation des Plug-ins, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie es in die Produktionsumgebung übernehmen.
* Ihre Implementierung verwendet möglicherweise einen anderen Objektnamen als das Standardobjekt von Adobe Analytics. Aktualisieren Sie in diesem Fall den Objektnamen entsprechend.
* Wenn Sie ein Tag Management-System verwenden, führen Sie die entsprechenden Schritte aus, um doPlugins und andere benutzerdefinierte Plug-ins zu aktualisieren.
