---
title: Geräteübergreifende Analyse
description: Ändern Sie Ihre Daten von gerätespezifisch zu personalorientiert, indem Sie Gerätedaten zusammenfügen.
translation-type: tm+mt
source-git-commit: eb2bee26dd58dcff13b4ddf41c6f6ab337d8d374
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 72%

---


# Geräteübergreifende Analyse

Die geräteübergreifende Analyse ist eine Funktion, mit der Analytics von einer geräteorientierten Ansicht zu einer personenorientierten Ansicht wechselt. Analysten können so das Benutzerverhalten über Browser, Geräte oder Apps hinweg nachvollziehen. Adobe unterstützt zwei übergreifende Workflows zum Verknüpfen von Gerätedaten:

* [**Feldbasierte Suche **](field-based-stitching.md): Ermöglicht die Auswahl einer Analytics-Variablen als Grundlage für geräteübergreifende Stiche in einer Virtual Report Suite. Verwendet deterministische Übereinstimmung, um Geräte miteinander zu verknüpfen. Adobe empfiehlt für die meisten bestimmungsgemäßen Anwendungsfälle die Verwendung von field-based stitching.
* [**Gerätediagramm **](device-graph.md): CDA kommuniziert mit einem Gerätediagramm, um Geräte miteinander zu verbinden. Das Co-op-Diagramm verwendet sowohl deterministische als auch provisorische Übereinstimmung.

Mit CDA können Sie Fragen wie folgende beantworten:

* Wie viele Personen interagieren mit meiner Marke? Wie viele und welche Gerätetypen verwenden sie? Wie überschneiden sich diese?
* Wie oft beginnen Personen mit einer Aufgabe auf einem Mobilgerät und wechseln dann zu einem Desktop-PC, um die Aufgabe abzuschließen? Führen Kampagnen-Clickthroughs auf einem Gerät zur Konversion auf einem anderen Gerät?
* Wie ändern sich meine Daten zur Wirksamkeit einer Kampagne, wenn ich geräteübergreifende Journeys berücksichtige? Wie ändert sich meine Trichteranalyse?
* Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo schließen sie ihre Aktion erfolgreich ab?
* Wie unterscheidet sich das Verhalten von Benutzern mit mehreren Geräten von Benutzern mit nur einem Gerät?

Beim Zuordnen von Geräten wird die variable Persistenz über Geräte hinweg übernommen. Beispiel: Ein Benutzer besucht Ihre Site zum ersten Mal über eine Werbeanzeige auf seinem Desktop. Der Benutzer findet Ihre mobile App, installiert sie und tätigt schließlich einen Einkauf auf seinem Mobilgerät. Mithilfe der geräteübergreifenden Analyse kann der Umsatz der Werbeanzeige zugeordnet werden, auf die der Benutzer auf seinem Desktop geklickt hat.

Aus Gründen der Partnerschaft und Transparenz möchten wir, dass unsere Kunden sich unserer Verwendung von Microsoft Azure in Verbindung mit geräteübergreifenden Analysen bewusst werden. Adobe verwendet Azur zum Speichern von Gerätediagrammdaten und zum Durchführen geräteübergreifender Zuordnungen. Daher werden Adobe Analytics-Daten zwischen dem Datenverarbeitungscenter von Adobe und den von Adobe bereitgestellten Instanzen von Microsoft Azure hin- und hergeleitet.

See the [Journey IQ: Cross-Device Analytics Spark page](http://adobe.ly/aacda) to learn more about the capabilities and features of Cross-Device Analytics.

## Voraussetzungen

Die Verwendung von CDA erfordert alle folgenden Maßnahmen: [Feldbasierte Heftungs](field-based-stitching.md) - und [Gerätediagrammmethoden](device-graph.md) haben ebenfalls eigene spezifische Voraussetzungen.

* Es muss ein Vertrag bei Adobe mit Adobe Analytics Ultimate abgeschlossen werden.
* Die geräteübergreifende Analyse wird pro Report Suite aktiviert. Adobe empfiehlt eine Report Suite, die geräteübergreifende Daten enthält, d. h. Daten aus mehreren Gerätetypen (Web, App usw.). Einige Organisationen bezeichnen dieses Konzept als „globale“ Report Suite, obwohl die geräteübergreifende Analyse aus geografischer Sicht nicht unbedingt global sein muss.

## Einschränkungen

Die geräteübergreifende Analyse ist eine innovative und zuverlässige Funktion, die jedoch Einschränkungen hinsichtlich ihrer Verwendung aufweist. [Feldbasierte Heftungs](field-based-stitching.md) - und [Gerätediagrammmethoden](device-graph.md) haben ebenfalls eigene Einschränkungen.

* Die geräteübergreifende Analyse ist nur über Analysis Workspace verfügbar.
* Die geräteübergreifende Analyse funktioniert nicht in allen Report Suites und kombiniert auch keine Daten aus mehreren Report Suites.
* Adobe Analytics-Report Suites können nicht mit mehr als einem IMS-Tag verknüpft werden. Da die geräteübergreifende Analyse Geräte innerhalb einer Report Suite zuordnet, kann die geräteübergreifende Analyse nicht zum Zuordnen von Daten über mehrere IMS-Organisationen hinweg verwendet werden.
* Die geräteübergreifende Analyse ist derzeit nicht mit Kundenattributen kompatibel. Diese beiden Funktionen können in separaten Virtual Report Suites zusammenfallen, die auf dieselbe Quell-Report Suite verweisen.
* Die geräteübergreifende Analyse verwendet eine Virtual Report Suite und eine Berichtszeitverarbeitung, die ihre eigenen Einschränkungen haben. Weitere Informationen zu diesen Einschränkungen finden Sie unter [Virtual Report Suites](../vrs/vrs-about.md) und [Berichtszeitverarbeitung](../vrs/vrs-report-time-processing.md).
* Die 1.4 API wird nicht unterstützt. Power BI-Connectoren und Report Builder basieren beide auf der 1.4 API und sind daher nicht mit der geräteübergreifenden Analyse kompatibel.
* Historische Daten in der Virtual Report Suite ändern sich je nach Erkennung und Zuordnung von Geräten von Adobe. Die Daten in der Quell-Report Suite bleiben unverändert.
