---
title: Geräteübergreifende Analyse
description: Geräteübergreifende Analysen verändern Ihre Daten von geräteorientierter zu personalorientierter Datenbindung.
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Geräteübergreifende Analyse

> [!NOTE] Die Dokumentation zu geräteübergreifenden Analysen kann sich ändern, wenn die Funktion weiterentwickelt wird. Suchen Sie regelmäßig nach Updates.

Geräteübergreifende Analyse ist eine Funktion, mit der Analytics von einer geräteorientierten Ansicht in eine personenzentrierte Ansicht umgewandelt wird. Diese Funktion verwendet das Co-op-Diagramm für den Identitätsdienst von Adobe Experience Platform oder das Private Graph, um zu ermitteln, welche Geräte zu einzelnen Geräten gehören, und sie zu verbinden. Analysten können daher das Benutzerverhalten von Browsern, Geräten oder Apps verstehen. Mithilfe von CDA können Sie Fragen beantworten wie z. B.:

* Wie viele Menschen interagieren mit meinem Unternehmen? Wie viele und welche Gerätetypen verwenden sie? Wie überschneiden sich diese?
* Wie oft beginnen Personen mit einer Aufgabe auf einem Mobilgerät und wechseln dann zu einem Desktop-PC, um die Aufgabe abzuschließen? Führen Kampagnen-Clickthroughs auf einem Gerät zur Konversion auf einem anderen Gerät?
* Wie ändern sich meine Daten zur Wirksamkeit einer Kampagne, wenn ich geräteübergreifende Journeys berücksichtige? Wie ändert sich meine Trichteranalyse?
* Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo schließen sie ihre Aktion erfolgreich ab?
* Wie unterscheidet sich das Verhalten von Benutzern mit mehreren Geräten von Benutzern mit nur einem Gerät?

Beim Verbinden von Geräten wird die variable Persistenz über Geräte hinweg übernommen. Beispielsweise besucht ein Benutzer Ihre Site zum ersten Mal über eine Werbung auf seinem Desktop-Computer. Der Benutzer findet Ihre mobile App, installiert sie und kauft sie schließlich auf seinem Mobilgerät ein. Bei der geräteübergreifenden Analyse kann der Umsatz der Anzeige zugeschrieben werden, auf die sie auf ihrem Desktop-Computer geklickt haben.

Siehe [Journey IQ: Geräteübergreifende Analyse-Spark-Seite](http://adobe.ly/aacda) , um mehr über die Funktionen und Funktionen von geräteübergreifender Analyse zu erfahren.

## Voraussetzungen

Ab September 2019 erfordert die geräteübergreifende Analyse Folgendes. Arbeiten Sie mit Teams in Ihrem Unternehmen und Ihrem Adobe-Kundenbetreuer zusammen, um sicherzustellen, dass Sie alle folgenden Kriterien erfüllen:

> [!IMPORTANT] Wenn nicht alle Voraussetzungen erfüllt sind, kann die Aktivierung der geräteübergreifenden Analyse nicht möglich sein oder die Ergebnisse beim Zusammenfügen der Daten sind schlecht.

* Die Daten Ihres Unternehmens müssen sich im Pacific Northwest-Rechenzentrum von Adobe befinden. Die Unterstützung von Rechenzentren in anderen Regionen der Welt ist geplant.
* Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, um die folgenden wichtigen Punkte festzustellen:
   * Ein Vertrag muss mit Adobe unterzeichnet werden, der Adobe Analytics Ultimate enthält.
   * Ihr Unternehmen muss das Co-op-Diagramm des Adobe Experience Platform Identity Service oder das Private Graph verwenden. Siehe [Startseite](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) im Benutzerhandbuch für die Gerätekooperation.
   * Ihr Unternehmen muss zustimmen, Adobe die Verarbeitung und Speicherung von Analytics-Daten auf Microsoft Azurblase-Servern zu gestatten. Adobe verwendet Azurblase zum Speichern von Gerätediagrammdaten und zum Durchführen der Gerätezuordnung. Daher werden Adobe Analytics-Daten zwischen dem Datenverarbeitungscenter von Adobe und der Präsenz von Adobe in Microsoft Azur hin- und hergeleitet.
* Geräteübergreifende Analysen werden pro Report Suite aktiviert. Für Report Suites, die für CDA aktiviert wurden, ist Folgendes erforderlich:
   * Die Report Suite kann nicht mehr als 100 Millionen Treffer pro Tag haben. Diese Schwelle wird sich in den kommenden Monaten erhöhen.
   * Adobe empfiehlt, dass eine Report Suite geräteübergreifende Daten enthält, d. h. Daten aus mehreren Gerätetypen (Web, App usw.). Einige Organisationen bezeichnen dieses Konzept als "globale"Report Suite, obwohl CDA aus geografischer Sicht nicht unbedingt global sein muss. Geräteübergreifende Analysen funktionieren nicht in allen Report Suites und kombinieren auch keine Daten aus mehreren Report Suites.
* Ihre Implementierung muss die folgenden Anforderungen erfüllen:
   * Die neueste Version des Experience Cloud ID-Diensts muss bereitgestellt werden. Siehe [Startseite](https://docs.adobe.com/content/help/en/id-service/using/home.html) im Benutzerhandbuch zum Experience Cloud-Identitätsdienst. Bei den meisten Implementierungen mit Adobe Experience Platform Launch ist möglicherweise ECID bereits bereitgestellt.
   * Rufen Sie die `setCustomerIDs` Funktion immer dann auf, wenn eine Person identifiziert werden kann, z. B. wenn sich ein Benutzer anmeldet oder eine E-Mail öffnet. Diese Anforderung gilt für alle Plattformen, einschließlich mobiler Apps, wenn sie verwendet werden. Siehe [setCustomerIDs](https://docs.adobe.com/content/help/en/id-service/using/id-service-api/methods/setcustomerids.html) im Benutzerhandbuch zum Experience Cloud-Identitätsdienst.

## Einschränkungen

Geräteübergreifende Analysen sind eine bahnbrechende und robuste Funktion, die jedoch Einschränkungen hinsichtlich ihrer Verwendung aufweist.

* CDA ist nur über den Analysis Workspace verfügbar.
* Stitching kann nicht in allen Report Suites durchgeführt werden, wie in den oben stehenden Voraussetzungen beschrieben.
* Adobe Analytics-Report Suites können nicht mehr als einem IMS-Tag zugeordnet werden. Da CDA Geräte innerhalb einer Report Suite zusammenfügt, kann CDA nicht zum Verbinden von Daten über mehrere IMS-Orgs hinweg verwendet werden.
* CDA ist derzeit nicht mit Kundenattributen kompatibel. Kundenattribute können nicht zum Erstellen einer virtuellen CDA-Report Suite, innerhalb geräteübergreifender Segmente oder zur Berichterstellung in einem Analysis Workspace-Projekt verwendet werden, das auf einer Virtual Report Suite der CDA basiert.
* CDA erfordert entweder ein Co-op-Diagramm oder ein privates Diagramm. Gerätediagramme von Drittanbietern werden nicht unterstützt.
* Ältere Analytics-IDs werden nicht unterstützt. Nur Besucher mit Experience Cloud IDs werden zugeordnet.
* Die Kundenunterstützung unterstützt diese Funktion noch nicht vollständig. Das [geräteübergreifende Analytics-Forum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/cross-device-analytics/overview) kann für die Unterstützung dieser Funktion verwendet werden, die eine aktive und direkte Beteiligung von Adobe-Produktmanagern beinhaltet.
* Geräteübergreifende Analysen verwenden eine Virtual Report Suite und eine Berichtszeitverarbeitung, die ihre eigenen Einschränkungen haben. Weitere Informationen zu diesen Einschränkungen finden Sie unter [Virtual Report Suites](../vrs/vrs-about.md) und [Berichtszeitverarbeitung](../vrs/vrs-report-time-processing.md) .
* Neue Geräte, die Ihre Site besuchen, können bis zu zwei Wochen dauern, bis sie mit dem Co-op-Diagramm oder dem privaten Diagramm verarbeitet werden. Die Heftungsrate in CDA in den letzten zwei Wochen ist in der Regel niedriger als in Datumsbereichen, die älter als zwei Wochen sind. Adobe plant, den Identitätsdienst für die Adobe Experience Platform zu verbessern, um in Zukunft neue Geräte in Echtzeit einzurichten.
* Historische Daten in der Virtual Report Suite ändern sich je nach Erkennungs- und Zusammenfügegerät von Adobe. Die Daten in der Quell-Report Suite bleiben unverändert.

Sobald Ihr Unternehmen alle Anforderungen erfüllt hat und die Einschränkungen versteht, können Sie mit der [Einrichtung von geräteübergreifenden Analysen](cda-setup.md)beginnen.
