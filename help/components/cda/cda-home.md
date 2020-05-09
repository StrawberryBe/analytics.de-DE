---
title: Geräteübergreifende Analyse
description: Die geräteübergreifende Analyse verändert Ihre Daten von geräteorientiert zu personenorientiert, indem sie Gerätedaten zuordnet.
translation-type: tm+mt
source-git-commit: 40d4dae0c54b8a71325846ae7f1c02947f9d36ea
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 90%

---


# Geräteübergreifende Analyse

>[!NOTE] Die Dokumentation zur geräteübergreifenden Analyse kann sich ändern, wenn die Funktion weiterentwickelt wird. Achten Sie regelmäßig auf Updates.

Die geräteübergreifende Analyse ist eine Funktion, mit der Analytics von einer geräteorientierten Ansicht zu einer personenorientierten Ansicht wechselt. Diese Funktion verwendet das Co-op-Diagramm oder das private Diagramm des Identity Service der Adobe Experience Platform, um zu ermitteln, welche Geräte zu Einzelanwendern gehören, und sie zuzuordnen. Analysten können so das Benutzerverhalten über Browser, Geräte oder Apps hinweg nachvollziehen. Mithilfe von CDA können Sie Fragen beantworten wie z. B.:

* Wie viele Menschen interagieren mit meinem Unternehmen? Wie viele und welche Gerätetypen verwenden sie? Wie überschneiden sich diese?
* Wie oft beginnen Personen mit einer Aufgabe auf einem Mobilgerät und wechseln dann zu einem Desktop-PC, um die Aufgabe abzuschließen? Führen Kampagnen-Clickthroughs auf einem Gerät zur Konversion auf einem anderen Gerät?
* Wie ändern sich meine Daten zur Wirksamkeit einer Kampagne, wenn ich geräteübergreifende Journeys berücksichtige? Wie ändert sich meine Trichteranalyse?
* Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo schließen sie ihre Aktion erfolgreich ab?
* Wie unterscheidet sich das Verhalten von Benutzern mit mehreren Geräten von Benutzern mit nur einem Gerät?

Beim Zuordnen von Geräten wird die variable Persistenz über Geräte hinweg übernommen. Beispiel: Ein Benutzer besucht Ihre Site zum ersten Mal über eine Werbeanzeige auf seinem Desktop. Der Benutzer findet Ihre mobile App, installiert sie und tätigt schließlich einen Einkauf auf seinem Mobilgerät. Mithilfe der geräteübergreifenden Analyse kann der Umsatz der Werbeanzeige zugeordnet werden, auf die der Benutzer auf seinem Desktop geklickt hat.

Weitere Informationen zu den Funktionen der geräteübergreifenden Analyse finden Sie unter [Journey IQ: Spark-Seite der geräteübergreifenden Analyse](http://adobe.ly/aacda).

## Voraussetzungen

Ab September 2019 gelten für die geräteübergreifende Analyse folgende Voraussetzungen. Arbeiten Sie mit Teams in Ihrer Organisation und Ihrem Adobe-Kundenbetreuer zusammen, um sicherzustellen, dass Sie die folgenden Kriterien alle erfüllen.

>[!IMPORTANT] Wenn nicht alle Voraussetzungen erfüllt sind, ist die Aktivierung der geräteübergreifenden Analyse unter Umständen nicht möglich oder die Ergebnisse bei der Datenzuordnung sind schlecht.

* Die Daten Ihrer Organisation müssen sich im Rechenzentrum „Pazifischer Nordwesten“ von Adobe befinden. Die Unterstützung von Rechenzentren in anderen Regionen der Welt ist in Planung.
* Wenden Sie sich an den Kundenbetreuer Ihrer Organisation, um die folgenden wichtigen Punkte zu klären:
   * Es muss ein Vertrag bei Adobe mit Adobe Analytics Ultimate abgeschlossen werden.
   * Ihre Organisation muss das Co-op-Diagramm oder das private Diagramm des Identity Service der Adobe Experience Platform verwenden. Weitere Informationen finden Sie unter [Startseite](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) im Benutzerhandbuch zur Co-op-Funktion des Geräts.
   * Aus dem Geist der Partnerschaft und Transparenz wollen wir, dass unsere Kunden wissen, wie wir Microsoft Azurblau in Verbindung mit Cross-Device Analytics verwenden. Adobe verwendet Azurblase zum Speichern von Gerätediagrammdaten und zum Durchführen von geräteübergreifenden Heften. Daher werden Adobe Analytics-Daten zwischen dem Datenverarbeitungscenter von Adobe und den von Adobe bereitgestellten Instanzen von Microsoft Epos hin und her weitergeleitet.
* Die geräteübergreifende Analyse wird pro Report Suite aktiviert. Für Report Suites mit aktivierter geräteübergreifender Analyse gelten folgende Voraussetzungen:
   * Die Report Suite kann nicht mehr als 500 Millionen Treffer pro Tag haben.
   * Adobe empfiehlt, dass eine Report Suite geräteübergreifende Daten enthält, d. h. Daten von mehreren Gerätetypen (Web, App usw.). Einige Organisationen bezeichnen dieses Konzept als „globale“ Report Suite, obwohl die geräteübergreifende Analyse aus geografischer Sicht nicht unbedingt global sein muss. Die geräteübergreifende Analyse funktioniert nicht in allen Report Suites und kombiniert auch keine Daten aus mehreren Report Suites.
* Ihre Implementierung muss folgende Anforderungen erfüllen:
   * Die neueste Version des Experience Cloud ID-Dienstes muss bereitgestellt sein. Weitere Informationen finden Sie unter [Startseite](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html) im Benutzerhandbuch des Experience Cloud ID-Dienstes. Bei den meisten Implementierungen mit Adobe Experience Platform Launch ist ECID wahrscheinlich bereits bereitgestellt.
   * Rufen Sie die `setCustomerIDs`-Funktion immer dann auf, wenn eine Person identifiziert werden kann, z. B. wenn sich ein Benutzer anmeldet oder eine E-Mail öffnet. Diese Anforderung gilt für alle Plattformen, einschließlich mobiler Apps, wenn sie verwendet werden. Weitere Informationen finden Sie unter [Festlegen von Kunden-IDs](https://docs.adobe.com/content/help/de-DE/id-service/using/id-service-api/methods/setcustomerids.html) im Benutzerhandbuch des Experience Cloud ID-Dienstes.

## Einschränkungen

Die geräteübergreifende Analyse ist eine innovative und zuverlässige Funktion, die jedoch Einschränkungen hinsichtlich ihrer Verwendung aufweist.

* Die geräteübergreifende Analyse ist nur über Analysis Workspace verfügbar.
* Eine Zuordnung kann nicht in allen Report Suites durchgeführt werden, wie in den oben stehenden Voraussetzungen beschrieben.
* Adobe Analytics-Report Suites können nicht mit mehr als einem IMS-Tag verknüpft werden. Da die geräteübergreifende Analyse Geräte innerhalb einer Report Suite zuordnet, kann die geräteübergreifende Analyse nicht zum Zuordnen von Daten über mehrere IMS-Organisationen hinweg verwendet werden.
* Die geräteübergreifende Analyse ist derzeit nicht mit Kundenattributen kompatibel. Kundenattribute können nicht zum Erstellen einer Virtual Report Suite für die geräteübergreifende Analyse, innerhalb geräteübergreifender Segmente oder zur Berichterstellung in einem Analysis Workspace-Projekt verwendet werden, das auf einer Virtual Report Suite für die geräteübergreifende Analyse basiert.
   > [!TIP] Obwohl Kundenattribute nicht in der geräteübergreifenden Analyse verwendet werden können, basieren beide Features auf der Funktion `setCustomerIDs`. Diese beiden Features können gleichzeitig in separaten (Virtual) Report Suites verwendet werden.
* Die geräteübergreifende Analyse erfordert entweder ein Co-op-Diagramm oder ein privates Diagramm. Gerätediagramme von Drittanbietern werden nicht unterstützt.
* Veraltete Analytics-IDs werden nicht unterstützt. Nur Besucher mit Experience Cloud IDs werden zugeordnet.
* Die Kundenunterstützung unterstützt diese Funktion noch nicht vollständig. Das [geräteübergreifende Analytics-Forum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/cross-device-analytics/overview) kann für Support zu dieser Funktion verwendet werden, wobei Adobe-Produktmanager aktiv und direkt beteiligt sind.
* Die geräteübergreifende Analyse verwendet eine Virtual Report Suite und eine Berichtszeitverarbeitung, die ihre eigenen Einschränkungen haben. Weitere Informationen zu diesen Einschränkungen finden Sie unter [Virtual Report Suites](../vrs/vrs-about.md) und [Berichtszeitverarbeitung](../vrs/vrs-report-time-processing.md).
* Die 1.4 API wird nicht unterstützt. Power BI-Connectoren und Report Builder basieren beide auf der 1.4 API und sind daher nicht mit der geräteübergreifenden Analyse kompatibel.
* Wenn Ihr Unternehmen das private Diagramm verwendet, dauert es bis zu 24 Stunden, bis neue Geräte geheftet werden.
* Neue Geräte, die Ihre Site besuchen, können bis zu zwei Wochen dauern, bis sie mit dem Co-op-Diagramm verarbeitet werden. Die Zuordnungsrate in der geräteübergreifenden Analyse in den letzten zwei Wochen ist in der Regel niedriger als in Datumsbereichen, die älter als zwei Wochen sind.
* Historische Daten in der Virtual Report Suite ändern sich je nach Erkennung und Zuordnung von Geräten von Adobe. Die Daten in der Quell-Report Suite bleiben unverändert.

Sobald Ihre Organisation alle Anforderungen erfüllt und die Einschränkungen versteht, können Sie mit der [Einrichtung der geräteübergreifenden Analyse](cda-setup.md) beginnen.
