---
title: Geräteübergreifende Analyse einrichten
description: Erfahren Sie, wie Sie geräteübergreifende Analysen einrichten, nachdem Sie die Voraussetzungen erfüllt haben.
translation-type: tm+mt
source-git-commit: 8c5e8d18ce4e09049d3fea07b8dd75ded6894313

---


# Geräteübergreifende Analyse einrichten

> [!NOTE] Die Dokumentation zu geräteübergreifenden Analysen kann sich ändern, wenn die Funktion weiterentwickelt wird. Suchen Sie regelmäßig nach Updates.

Sobald alle Voraussetzungen erfüllt sind, aktivieren Sie die geräteübergreifende Analyse mit den folgenden Schritten. Sie müssen zu einer Produktprofil-Administratorgruppe gehören oder über Administratorrechte in Adobe Analytics verfügen, um diese Schritte ausführen zu können.

> [!IMPORTANT] Alle Voraussetzungen müssen erfüllt sein, bevor Sie diese Schritte durchführen. Wenn nicht alle Voraussetzungen erfüllt sind, ist die Funktion nicht verfügbar oder funktioniert nicht. Voraussetzungen und Einschränkungen finden Sie unter [Geräteübergreifende Analyse](cda-home.md) .

## Wählen Sie die geräteübergreifende Report Suite, die für CDA aktiviert werden soll

Wenn Ihr Unternehmen für die Verwendung von CDA vorgesehen ist, wählen Sie die zu verwendende Report Suite aus. Diese Auswahl kann von Ihrem Adobe-Kundenbetreuer mitgeteilt werden. Adobe aktiviert dann Ihre ausgewählte Report Suite für die CDA-Verarbeitung.

## Erstellen Sie eine geräteübergreifende Virtual Report Suite, um die geräteübergreifende Ansicht anzuzeigen

Administratoren mit Zugriff auf Virtual Report Suites können CDA Virtual Report Suites wie folgt erstellen:

1. Navigieren Sie zu [experiencecloud.adobe.com](https://experiencecloud.adobe.com) und melden Sie sich mit Ihren AdobeID-Anmeldeinformationen an.
2. Klicken Sie oben auf das 9-Raster-Symbol und dann auf Analytics.
3. Bewegen Sie den Mauszeiger über die Komponenten oben und klicken Sie dann auf Virtual Report Suites.
4. Klicken Sie auf Hinzufügen.
5. Geben Sie einen Namen für Ihre Virtual Report Suite ein und stellen Sie sicher, dass die CDA-fähige Report Suite ausgewählt ist.
6. (Optional) Wenden Sie ein Segment auf die Virtual Report Suite an. Sie können beispielsweise ein Segment anwenden, das die Virtual Report Suite auf Daten beschränkt, nachdem CDA aktiviert und die Suche begonnen hat. Dieses Segment ermöglicht es Benutzern, nur zugewiesene Datumsbereiche innerhalb der VRS anzuzeigen.
7. Klicken Sie auf das Kontrollkästchen "Berichtzeitverarbeitung aktivieren", das mehrere weitere Optionen einschließlich geräteübergreifender Analysen aktiviert.
8. Markieren Sie das Kontrollkästchen "Benutzerbesuche geräteübergreifend zusammenfügen".
9. Klicken Sie auf Weiter, konfigurieren Sie die Virtual Report Suite und klicken Sie dann auf Speichern.

![CDA-Kontrollkästchen](assets/cda-checkbox.png)

## Hinzufügungen und Änderungen zu geräteübergreifenden Virtual Report Suites

Wenn geräteübergreifende Analysen für eine Virtual Report Suite aktiviert sind, beachten Sie die folgenden Änderungen:

* Neben dem Namen der Virtual Report Suite wird ein neues geräteübergreifendes Symbol angezeigt. Dieses Symbol ist ausschließlich für geräteübergreifende Virtual Report Suites vorgesehen.
* Es sind neue Metriken mit den Bezeichnungen "Personen"und "Unique Devices"verfügbar.
* Die Metrik "Individuelle Besucher"ist nicht verfügbar, da sie durch "Personen und Unique Devices"ersetzt wird.
* Beim Erstellen von Segmenten wird der Segmentbehälter "Besucher"durch den Behälter "Person"ersetzt.

## Die berechnete Metrik "Komprimierung"

Die Fähigkeit von geräteübergreifender Analytics, Geräte miteinander zu verbinden, hängt von einer Vielzahl von Faktoren ab. Die Effektivität der Funktion zum Verbinden von Daten kann mit einer berechneten Metrik, der so genannten Komprimierung, gemessen werden. Zu den Faktoren, die zur Komprimierung beitragen, gehören:

* Verwenden des Co-op-Diagramms oder des privaten Diagramms: Im Allgemeinen sehen Organisationen, die die Geräte-Co-op verwenden, bessere Komprimierungsraten als Organisationen, die das private Diagramm verwenden.
* Anmelderate: Je mehr Benutzer sich auf Ihrer Site anmelden, desto mehr kann Adobe Besucher geräteübergreifend identifizieren und verbinden. Sites mit einer niedrigen Anmelderate haben ebenfalls niedrige Komprimierungsraten.
* Erlebnis-Cloud-ID-Abdeckung: Es können nur Besucher mit einer ECID verknüpft werden. Ein geringerer Prozentsatz der Besucher Ihrer Site, die eine ECID verwenden, korreliert mit niedrigeren Komprimierungsraten.
* Verwendung mehrerer Geräte: Wenn Besucher Ihrer Site nicht mehrere Geräte verwenden, sehen Sie niedrigere Komprimierungsraten.
* Berichtsgranularität: Die Komprimierung nach Tag ist in der Regel kleiner als die Komprimierung nach Monat oder Jahr. Die Wahrscheinlichkeit, dass eine Person mehrere Geräte verwendet, wird innerhalb eines Tages geringer als innerhalb eines ganzen Monats. Die Segmentierung, Filterung oder Verwendung von Aufschlüsselungsdimensionen können auch eine niedrigere Komprimierungsrate anzeigen.

So sehen Sie die Komprimierung Ihres Unternehmens für einen bestimmten Zeitraum:

1. Klicken Sie oben auf Arbeitsbereich und dann auf Neues Projekt erstellen.
2. Beginnen Sie mit einem leeren Projekt und klicken Sie dann auf Erstellen.
3. Ziehen Sie die Metrik "Individuelle Geräte"in den Arbeitsflächenbereich mit der Bezeichnung "Metrik hier ablegen".
4. Ziehen Sie die Metrik "Personen"direkt rechts neben der Metriküberschrift "Individuelle Geräte"auf die Arbeitsfläche, damit die beiden Metriken nebeneinander angezeigt werden.
5. Klicken Sie links neben den verfügbaren Metriken auf das Symbol "`+`", um den Generator für berechnete Metriken zu öffnen.
6. Geben Sie für diese berechnete Metrik die folgenden Einstellungen ein:
   * Name: Geräteübergreifende Komprimierung
   * Format: Prozent
   * Dezimalstellen: 2
   * Definition: `[Static Number: 1] minus [People] divided by [Unique Devices]`
      > [!TIP] Klicken Sie oben rechts im Definitionsbereich auf "Hinzufügen", um eine statische Zahl hinzuzufügen. Ziehen Sie Personen und individuelle Geräte aus der Liste der verfügbaren Metriken auf der linken Seite.
7. Klicken Sie auf „Speichern“.
8. Ziehen Sie die neue berechnete Metrik direkt rechts neben der Metriküberschrift "Personen"auf die Arbeitsfläche, sodass alle drei Metriken nebeneinander stehen.
9. Optional: Der Arbeitsbereich lädt standardmäßig die Dimension "Tag". Ziehen Sie eine alternative Datumsdimension (z. B. Woche oder Monat) auf die Dimension "Tag", wenn eine andere Zeitgranularität gewünscht wird.
