---
title: Geräteübergreifende Analyse einrichten
description: Erfahren Sie, wie Sie geräteübergreifende Analysen einrichten, nachdem Sie die Voraussetzungen erfüllt haben.
translation-type: tm+mt
source-git-commit: 1ab4c27d6635167be475b6669ff6ed1913adc455

---


# Geräteübergreifende Analyse einrichten

> [!IMPORTANT] Alle Voraussetzungen müssen erfüllt sein, bevor diese Schritte ausgeführt werden. Wenn alle Voraussetzungen nicht erfüllt sind, ist die Funktion nicht verfügbar oder funktioniert nicht. Siehe [geräteübergreifende Analyse](cda-home.md) für Voraussetzungen und Einschränkungen.

Sobald alle Voraussetzungen erfüllt sind, verwenden Sie die folgenden Schritte, um geräteübergreifende Analysen zu aktivieren. Sie müssen einer Produktprofil-Administratorgruppe angehören oder über Administratorrechte in Adobe Analytics verfügen, um diese Schritte auszuführen.

## Geräteübergreifende Report Suite auswählen, die für CDA aktiviert werden soll

Wenn Ihr Unternehmen für die Verwendung von CDA freigeschaltet ist, wählen Sie die gewünschte Report Suite aus. Diese Auswahl kann über Ihren Adobe-Kundenbetreuer erfolgen. Anschließend aktiviert Adobe die ausgewählte Report Suite für die CDA-Verarbeitung.

## Geräteübergreifende Virtual Report Suite erstellen, um die geräteübergreifende Ansicht anzuzeigen

Administratoren mit Zugriff auf Virtual Report Suites können wie folgt CDA Virtual Report Suites erstellen:

1. Navigieren Sie zu [experiencecloud.adobe.com](https://experiencecloud.adobe.com) und melden Sie sich mit Ihren adobeid-Anmeldeinformationen an.
2. Klicken Sie oben auf das 9-Rastersymbol und dann auf Analytics.
3. Bewegen Sie den Mauszeiger oben über Komponenten und klicken Sie dann auf Virtual Report Suites.
4. Klicken Sie auf Hinzufügen.
5. Geben Sie einen Namen für Ihre Virtual Report Suite ein und stellen Sie sicher, dass die CDA-aktivierte Report Suite ausgewählt ist.
6. Klicken Sie auf das Kontrollkästchen "Zeitverarbeitung für Bericht aktivieren" , wodurch mehrere weitere Optionen (einschließlich geräteübergreifender Analysen) aktiviert werden.
7. Klicken Sie auf das Kontrollkästchen "Benutzerbesuche geräteübergreifend" .
8. Klicken Sie auf Weiter, konfigurieren Sie die Virtual Report Suite und klicken Sie dann auf Speichern.

![CDA-Kontrollkästchen](assets/cda-checkbox.png)

## Ergänzungen und Änderungen an geräteübergreifenden Virtual Report Suites

Wenn geräteübergreifende Analysen in einer Virtual Report Suite aktiviert sind, beachten Sie folgende Änderungen:

* Neben dem Namen der Virtual Report Suite wird ein neues geräteübergreifendes Symbol angezeigt. Dieses Symbol gilt ausschließlich für geräteübergreifende Virtual Report Suites.
* Neue Metriken mit der Bezeichnung "Personen" und" Individuelle Geräte" sind verfügbar.
* Die Metrik "Unique Visitors" ist nicht verfügbar, da sie durch Personen und individuelle Geräte ersetzt wird.
* Beim Erstellen von Segmenten wird der Segmentbehälter "Besucher" durch einen" Person" -Behälter ersetzt.

## Die berechnete Metrik für die Komprimierung

Ob geräteübergreifend Geräte zusammengefügt werden können, hängt von einer breiten Palette von Faktoren ab. Die Effektivität der Funktion der Funktion kann mit einer berechneten Metrik namens Komprimierung gemessen werden. Faktoren, die zur Komprimierung beitragen, umfassen:

* Verwenden des Co-op-Diagramms oder des privaten Diagramms: Im Allgemeinen werden Unternehmen, die die Geräte-Kooperation verwenden, tendenziell bessere Komprimierungsraten anzeigen als Unternehmen, die das private Diagramm verwenden.
* Anmelderate: Je mehr Benutzer sich auf Ihrer Site anmelden, desto mehr kann Adobe Besucher auf allen Geräten identifizieren und anordnen. Bei Sites mit einer niedrigen Rate werden ebenfalls niedrige Komprimierungsraten verzeichnet.
* Experience Cloud ID-Abdeckung: Es können nur Besucher mit einer ECID gefüllt werden. Ein niedrigerer Prozentsatz der Besucher Ihrer Site mit einer ECID verwandelt sich mit niedrigeren Komprimierungsraten.
* Mehrere Gerätenutzung: Wenn Besucher auf Ihrer Site nicht mehrere Geräte verwenden, können Sie niedrigere Komprimierungsraten sehen.
* Berichtsgranularität: Die Komprimierung nach Tag ist normalerweise kleiner als die Komprimierung nach Monat oder Jahr. Die Wahrscheinlichkeit, dass eine Person mehrere Geräte verwendet, wird innerhalb eines Tages kleiner als in einem ganzen Monat. Die Segmentierung, Filterung oder Verwendung von Unterteilungsdimensionen kann auch eine niedrigere Komprimierungsrate aufweisen.

So zeigen Sie die Komprimierung Ihres Unternehmens für einen bestimmten Zeitraum an:

1. Klicken Sie oben auf Workspace und dann auf'Create New Project ' (Neues Projekt erstellen).
2. Beginnen Sie mit einem leeren Projekt und klicken Sie dann auf Erstellen.
3. Ziehen Sie die Metrik "Unique Devices" auf die Arbeitsfläche mit der Bezeichnung" Metrik hier ablegen" .
4. Ziehen Sie die Metrik "Personen" direkt auf die Arbeitsfläche rechts neben der Metrik" Unique Devices" , sodass die beiden Metriken nebeneinander stehen.
5. Klicken Sie auf der linken Seite neben den verfügbaren Metriken auf das Symbol " +" , um den Generator für berechnete Metriken zu öffnen.
6. Geben Sie diese berechnete Metrik die folgenden Einstellungen an:
   * Name: Geräteübergreifende Komprimierung
   * Format: Prozent
   * Dezimalstellen: 2
   * Definition: `[Static Number: 1] minus [People] divided by [Unique Devices]`
      > [!NOTE] Klicken Sie oben rechts im Definitionsbereich auf "Hinzufügen" , um eine statische Zahl hinzuzufügen. Ziehen Sie Personen und individuelle Geräte aus der Liste der verfügbaren Metriken auf der linken Seite.
7. Klicken Sie auf „Speichern“.
8. Ziehen Sie die neue berechnete Metrik direkt auf die Arbeitsfläche rechts neben der Metrik "Personen" , sodass alle drei Metriken nebeneinander stehen.
9. Optional: Der Arbeitsbereich lädt die Dimension "Tag" standardmäßig. Ziehen Sie eine alternative Datumsdimension, z. B. Woche oder Monat, auf die Dimension "Tag" , wenn eine andere Zeitgranularität gewünscht wird.
