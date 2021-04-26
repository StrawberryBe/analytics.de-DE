---
title: Geräteübergreifende Analyse
description: Ändern Sie Ihre Daten von geräteorientiert zu personenorientiert, indem Sie die Gerätedaten zuordnen.
exl-id: e1c0d1e5-399d-45c2-864c-50ef93a77449
translation-type: tm+mt
source-git-commit: 99fea634dafc5d0992898f8f9f89471b51191fc6
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 85%

---

# Geräteübergreifende Analyse

Die geräteübergreifende Analyse ist eine Funktion, mit der Analytics von einer geräteorientierten Ansicht zu einer personenorientierten Ansicht wechselt. Analysten können so das Benutzerverhalten über Browser, Geräte oder Apps hinweg nachvollziehen. Adobe unterstützt zwei übergreifende Workflows zum Verknüpfen von Gerätedaten:

* [**Feldbasiertes Stitching**](field-based-stitching.md): Ermöglicht die Auswahl einer Analytics-Variablen als Grundlage für geräteübergreifendes Zuordnen in einer Virtual Report Suite. Verwendet deterministische Abgleiche, um Geräte miteinander zu verknüpfen. Adobe empfiehlt die Verwendung von feldbasiertem Stitching für die meisten Anwendungsfälle des deterministischen Abgleichs.
* [**Gerätediagramm**](device-graph.md): Die geräteübergreifende Analyse kommuniziert mit einem Gerätediagramm, um Geräte einander zuzuordnen. Das Co-op-Diagramm nutzt sowohl deterministische als auch probabilistische Abgleiche.

Mithilfe der geräteübergreifenden Analyse können Sie Fragen beantworten wie z. B.:

* Wie viele Menschen interagieren mit meiner Marke? Wie viele und welche Gerätetypen verwenden sie? Wie überschneiden sich diese?
* Wie oft beginnen Personen mit einer Aufgabe auf einem Mobilgerät und wechseln dann zu einem Desktop-PC, um die Aufgabe abzuschließen? Führen Kampagnen-Clickthroughs auf einem Gerät zur Konversion auf einem anderen Gerät?
* Wie ändern sich meine Daten zur Wirksamkeit einer Kampagne, wenn ich geräteübergreifende Journeys berücksichtige? Wie ändert sich meine Trichteranalyse?
* Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo schließen sie ihre Aktion erfolgreich ab?
* Wie unterscheidet sich das Verhalten von Benutzern mit mehreren Geräten von Benutzern mit nur einem Gerät?

Beim Zuordnen von Geräten wird die variable Persistenz über Geräte hinweg übernommen. Beispiel: Ein Benutzer besucht Ihre Site zum ersten Mal über eine Werbeanzeige auf seinem Desktop. Der Benutzer findet Ihre Mobile App, installiert sie und tätigt schließlich einen Einkauf auf seinem Mobilgerät. Mit der geräteübergreifenden Analyse können Sie den Umsatz auf dem Mobilgerät einer Anzeige zuordnen, auf die auf dem Desktop-Computer geklickt wurde.

Aus Gründen der Partnerschaft und Transparenz möchten wir, dass unsere Kunden sich unserer Verwendung von Microsoft Azure in Verbindung mit geräteübergreifenden Analysen bewusst werden. Adobe verwendet Azur zum Speichern von Gerätediagrammdaten und zum Durchführen geräteübergreifender Zuordnungen. Daher werden Adobe Analytics-Daten zwischen dem Datenverarbeitungscenter von Adobe und den von Adobe bereitgestellten Instanzen von Microsoft Azure hin- und hergeleitet.

Weitere Informationen zu den Funktionen der geräteübergreifenden Analyse finden Sie unter [Journey IQ: Spark-Seite der geräteübergreifenden Analyse](http://adobe.ly/aacda).

## Voraussetzungen

Die Verwendung der geräteübergreifenden Analyse erfordert Folgendes: Die Methoden zum [feldbasierten Stitching](field-based-stitching.md) und der [Gerätediagrammme](device-graph.md) haben ebenfalls eigene spezifische Voraussetzungen.

* Es muss ein Vertrag bei Adobe mit Adobe Analytics Ultimate abgeschlossen werden.
* Geräteübergreifende Analysen werden pro Report Suite aktiviert. Adobe empfiehlt, dass eine Report Suite geräteübergreifende Daten enthält, d. h. Daten von mehreren Gerätetypen (Web, App usw.). Einige Organisationen bezeichnen dieses Konzept als „globale“ Report Suite, obwohl die geräteübergreifende Analyse aus geografischer Sicht nicht unbedingt global sein muss.

## Einschränkungen

Die geräteübergreifende Analyse ist eine innovative und zuverlässige Funktion, die jedoch Einschränkungen hinsichtlich ihrer Verwendung aufweist. Die Methoden zum [feldbasierten Stitching](field-based-stitching.md) und der [Gerätediagrammme](device-graph.md) haben ebenfalls eigene spezifische Einschränkungen.

* Die geräteübergreifende Analyse ist nur über Analysis Workspace verfügbar.
* Die geräteübergreifende Analyse funktioniert nicht in allen Report Suites und kombiniert auch keine Daten aus mehreren Report Suites.
* Adobe Analytics-Report Suites können nicht mit mehr als einem IMS-Tag verknüpft werden. Da die geräteübergreifende Analyse Geräte innerhalb einer Report Suite zuordnet, kann die geräteübergreifende Analyse nicht zum Zuordnen von Daten über mehrere IMS-Organisationen hinweg verwendet werden.
* Private Graph nutzt die gleichen ID-Syncs wie die, die von der Funktion [Kundenattribute](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=en#customer-attributes) in Experience Cloud und Adobe Analytics verwendet werden. Virtual Report Suites von CDA (unabhängig davon, ob sie auf einer privaten Grafik oder einer feldbasierten Suche basieren) sind jedoch nicht mit den übrigen Funktionen für Kundenattribute kompatibel. Kundenattribute-basierte Dimensionen stehen also nicht zur Verwendung in Virtual Report Suites von CDA zur Verfügung.
* CDA ist derzeit nicht mit A4T kompatibel.
* Die geräteübergreifende Analyse verwendet eine Virtual Report Suite und eine Berichtszeitverarbeitung, die ihre eigenen Einschränkungen haben. Weitere Informationen zu diesen Einschränkungen finden Sie unter [Virtual Report Suites](../vrs/vrs-about.md) und [Berichtszeitverarbeitung](../vrs/vrs-report-time-processing.md).
* Die 1.4 API wird nicht unterstützt. Power BI-Connectoren und Report Builder basieren beide auf der 1.4 API und sind daher nicht mit der geräteübergreifenden Analyse kompatibel.
* Historische Daten in der Virtual Report Suite ändern sich je nach Erkennung und Zuordnung von Geräten von Adobe. Die Daten in der Quell-Report Suite bleiben unverändert.
* Die aktive Überwachung des CDA-Heftprozesses nach Adobe ist nur auf Produktions-Report Suites beschränkt.
* CDA ist derzeit nicht mit der Adobe Analytics [Datenreparatur-API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/data-repair.md) kompatibel
