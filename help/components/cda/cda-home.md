---
title: Geräteübergreifende Analyse
description: Geräteübergreifende Analysen bewirken, dass Ihre Daten geräteorientiert sind, indem Sie geräteübergreifende Gerätedaten zusammenführen.
translation-type: tm+mt
source-git-commit: 40d8ecae1ac7e0a1df4a2df17f5104bee6ecf336

---


# Geräteübergreifende Analyse

> [!NOTE] Die geräteübergreifende Analytics-Dokumentation kann sich ändern, wenn die Funktion weiter entwickelt wurde. Überprüfen Sie regelmäßig nach Updates.

Device Analytics ist eine Funktion, die Analytics von einer gerätespezifischen Ansicht in eine persönliche Ansicht umwandelt. Diese Funktion verwendet das Adobe Experience Platform Identity Service Co-op Graph oder Privates Diagramm, um zu identifizieren, welche Geräte zu Einzelpersonen gehören. Daher können Analysten das Benutzerverhalten verstehen, das Browser, Geräte oder Apps durchkreuzt. Mithilfe von CDA können Sie Fragen beantworten wie z. B.:

* Wie viele Menschen interagieren mit meinem Unternehmen? Wie viele und welche Gerätetypen verwenden sie? Wie überschneiden sich diese?
* Wie oft beginnen Personen mit einer Aufgabe auf einem Mobilgerät und wechseln dann zu einem Desktop-PC, um die Aufgabe abzuschließen? Führen Kampagnen-Clickthroughs auf einem Gerät zur Konversion auf einem anderen Gerät?
* Wie ändern sich meine Daten zur Wirksamkeit einer Kampagne, wenn ich geräteübergreifende Journeys berücksichtige? Wie ändert sich meine Trichteranalyse?
* Welche sind die häufigsten Pfade, die Benutzer beim Wechsel von einem Gerät zum anderen verwenden? Wo steigen sie aus? Wo schließen sie ihre Aktion erfolgreich ab?
* Wie unterscheidet sich das Verhalten von Benutzern mit mehreren Geräten von Benutzern mit nur einem Gerät?

Wenn Geräte gestipft werden, wird die variable Persistenz auf allen Geräten übertragen. Beispiel: Ein Benutzer besucht Ihre Site zunächst über eine Werbung auf ihrem Desktop-Computer. Der Benutzer findet Ihre mobile App, installiert ihn und kauft schließlich auf ihrem Mobilgerät ein. Bei geräteübergreifender Analyse kann der Umsatz der Anzeige zugeschrieben werden, auf die sie auf ihrem Desktop-Computer geklickt haben.

Siehe [Journey IQ: Geräteübergreifende Analytics-Spark-Seite](http://adobe.ly/aacda) , um mehr über die Funktionen und Funktionen von Device Analytics zu erfahren.

## Voraussetzungen

Im September 2019 erfordert Device Analytics Folgendes: Arbeiten Sie mit Teams in Ihrem Unternehmen und Ihrem Adobe-Kundenbetreuer zusammen, um sicherzustellen, dass Sie alle folgenden Anforderungen erfüllen.

> [!IMPORTANT] Wenn Sie nicht alle Voraussetzungen erfüllen, kann dies dazu führen, dass geräteübergreifende Analysen oder schlechte Ergebnisse beim Zusammenführen von Daten nicht möglich sind.

* Die Daten Ihrer Organisation müssen sich im Rechenzentrum von Adobe Pacific Northwest befinden. Die Unterstützung für Rechenzentren in anderen Regionen der Welt ist geplant.
* Wenden Sie sich an den Kundenbetreuer Ihrer Organisation, um diese wichtigen Punkte festzulegen:
   * Ein Vertrag muss mit Adobe signiert werden, der Adobe Analytics Ultimate enthält.
   * Ihr Unternehmen muss das Adobe Experience Platform Identity Service Co-op Graph oder Privates Diagramm verwenden. Weitere Informationen finden Sie auf der [Startseite](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) im Device Co-op Benutzerhandbuch.
   * Ihr Unternehmen muss genehmigen, dass Adobe Analytics-Daten auf Microsoft Azure-Servern verarbeiten und speichern kann. Adobe verwendet Azure zum Speichern von Gerätediagrammdaten und zum Durchführen von Gerätestitching. Somit werden Adobe Analytics-Daten zwischen dem Datenverarbeitungscenter von Adobe und der Präsenz von Adobe in Microsoft Azure weitergeleitet.
* Geräteübergreifende Analysen sind pro Report Suite aktiviert. Für Ihre Report Suite ist Folgendes erforderlich:
   * Derzeit kann eine Report Suite maximal 100 Mio. Treffer pro Tag aufweisen. Dieser Schwellenwert wird in den kommenden Monaten zunehmen.
   * Eine "geräteübergreifende" Report Suite, d. h. alle geräteübergreifenden Daten müssen an dieselbe Report Suite gesendet werden. Einige Organisationen bezeichnen dies als eine globale Report Suite, obwohl CDA aus geografischer Sicht nicht unbedingt global sein muss. Geräteübergreifende Analysen funktionieren nicht über Report Suites hinweg.
* Ihre Implementierung muss die folgenden Anforderungen erfüllen:
   * Die neueste Version des Experience Cloud ID-Diensts muss bereitgestellt werden. Weitere Informationen finden Sie auf der [Startseite](https://docs.adobe.com/content/help/en/id-service/using/home.html) im Benutzerhandbuch für die Experience Cloud-Identitätsdienst-ID. Bei den meisten Implementierungen mit Adobe Experience Platform Start ist wahrscheinlich bereits ECID bereitgestellt.
   * Rufen Sie die `setCustomerIDs` Funktion auf, wenn eine Person identifiziert werden kann, z. B. wenn sich ein Benutzer anmeldet oder eine E-Mail öffnet. Diese Anforderung gilt für alle Plattformen, einschließlich Apps, wenn sie verwendet werden. Siehe [setcustomerids](https://docs.adobe.com/content/help/en/id-service/using/id-service-api/methods/setcustomerids.html) im Benutzerhandbuch für die Experience Cloud-Identitätsdienst-ID.

## Einschränkungen

Geräteübergreifende Analysen sind eine bahnbrechende und robuste Funktion, die jedoch Einschränkungen hinsichtlich der Verwendung bietet.

* CDA ist nur über Analysis Workspace verfügbar.
* Das Stitching kann nicht über IMS-Organisationen erfolgen. Stellen Sie sicher, dass Sie nicht mehrere IMS-Orgs in Ihrer Implementierung verwenden.
* Das Stitching kann nicht über Report Suites erfolgen, wie unter Voraussetzungen oben beschrieben.
* CDA ist derzeit nicht mit Kundenattributen kompatibel. Kundenattribute können nicht verwendet werden, um eine virtuelle CDA-Report Suite, innerhalb von geräteübergreifenden Segmenten oder für die Berichterstellung innerhalb eines Analysis Workspace-Projekts zu erstellen, das auf einer virtuellen CDA-Report Suite basiert.
* CDA erfordert entweder Co-Op-Diagramm oder privates Diagramm. Gerätediagramme von Drittanbietern werden nicht unterstützt.
* Legacy-Analytics-Ids werden nicht unterstützt. Nur Besucher mit Experience Cloud Ids werden gestipft.
* Die Kundenunterstützung unterstützt diese Funktion noch nicht vollständig. Das [geräteübergreifende Analytics-Forum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/cross-device-analytics/overview) kann für die Unterstützung dieser Funktion verwendet werden, die eine aktive und direkte Einbindung von Adobe-Produktmanagern beinhaltet.
* Geräteübergreifende Analysen verwenden eine Virtual Report Suite und eine Berichtszeitverarbeitung mit eigenen Einschränkungen. Weitere Informationen zu diesen Einschränkungen finden Sie unter [Virtual Report Suites](../vrs/vrs-about.md) und [Berichtszeitverarbeitung](../vrs/vrs-report-time-processing.md) .
* Neue Geräte, die Ihre Site besuchen, können bis zu zwei Wochen dauern, bis das Co-op-Diagramm oder das private Diagramm verarbeitet wird. Die Ebene der Stitching in CDA für die letzten beiden Wochen ist normalerweise niedriger als bei Datumsbereichen, die älter als zwei Wochen sind. Adobe plant, den Adobe Experience Platform Identity Service zu verbessern, um in Zukunft neue Geräte zu stiften.
* Historische Daten in der Virtual Report Suite werden auf der Grundlage von Adobe erkennt und zusammengefügt. Daten in der Quell-Report Suite werden nicht geändert.

Sobald Ihr Unternehmen alle Anforderungen erfüllt und die Einschränkungen einnimmt, können Sie mit der [Einrichtung geräteübergreifender Analysen beginnen](cda-setup.md).
