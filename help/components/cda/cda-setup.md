---
title: Geräteübergreifende Analyse einrichten
description: Erfahren Sie, wie Sie die geräteübergreifende Analyse einrichten, wenn Sie die Voraussetzungen erfüllen.
translation-type: ht
source-git-commit: 8c5e8d18ce4e09049d3fea07b8dd75ded6894313

---


# Geräteübergreifende Analyse einrichten

> [!NOTE] Die Dokumentation zur geräteübergreifenden Analyse kann sich ändern, wenn die Funktion weiterentwickelt wird. Achten Sie regelmäßig auf Updates.

Wenn alle Voraussetzungen erfüllt sind, aktivieren Sie die geräteübergreifende Analyse mit den folgenden Schritten. Sie müssen einer Produktprofil-Administratorgruppe angehören oder über Administratorrechte in Adobe Analytics verfügen, um diese Schritte ausführen zu können.

> [!IMPORTANT] Alle Voraussetzungen müssen erfüllt sein, bevor Sie diese Schritte durchführen. Wenn nicht alle Voraussetzungen erfüllt sind, ist die Funktion nicht verfügbar oder sie funktioniert nicht. Informationen zu Voraussetzungen und Einschränkungen finden Sie unter [Geräteübergreifende Analyse](cda-home.md).

## Auswahl einer geräteübergreifenden Report Suite zur Aktivierung für die geräteübergreifende Analyse

Wenn Ihre Organisation für die Verwendung der geräteübergreifenden Analyse vorgesehen ist, wählen Sie die zu verwendende Report Suite aus. Diese Entscheidung können Sie Ihrem Adobe-Kundenbetreuer mitteilen. Adobe aktiviert dann Ihre ausgewählte Report Suite für die Verarbeitung der geräteübergreifenden Analyse.

## Erstellung einer geräteübergreifenden Virtual Report Suite zur geräteübergreifenden Ansicht

Administratoren mit Zugriff auf Virtual Report Suites können Virtual Report Suites für die geräteübergreifende Analyse wie folgt erstellen:

1. Navigieren Sie zu [experiencecloud.adobe.com](https://experiencecloud.adobe.com) und melden Sie sich mit Ihren AdobeID-Anmeldeinformationen an.
2. Klicken Sie oben auf das 9-Raster-Symbol und dann auf Analytics.
3. Bewegen Sie den Mauszeiger über die Komponenten oben und klicken Sie dann auf „Virtual Report Suites“.
4. Klicken Sie auf Hinzufügen.
5. Geben Sie einen Namen für Ihre Virtual Report Suite ein und stellen Sie sicher, dass die für die geräteübergreifende Analyse aktivierte Report Suite ausgewählt ist.
6. (Optional) Wenden Sie ein Segment auf die Virtual Report Suite an. Sie können beispielsweise ein Segment anwenden, das die Virtual Report Suite auf Daten beschränkt, die nach dem Datum liegen, an dem die geräteübergreifende Analyse aktiviert wurde und die Suche begonnen hat. Dieses Segment ermöglicht es Benutzern, nur zugewiesene Datumsbereiche innerhalb der VRS anzuzeigen.
7. Aktivieren Sie das Kontrollkästchen „Berichtszeitverarbeitung aktivieren“, wodurch mehrere weitere Optionen, einschließlich der geräteübergreifenden Analyse, aktiviert werden.
8. Aktivieren Sie das Kontrollkästchen „Benutzerbesuche geräteübergreifend zuordnen“.
9. Klicken Sie auf „Weiter“, konfigurieren Sie die Virtual Report Suite und klicken Sie dann auf „Speichern“.

![Kontrollkästchen „Geräteübergreifende Analyse“](assets/cda-checkbox.png)

## Hinzufügungen und Änderungen an geräteübergreifenden Virtual Report Suites

Wenn die geräteübergreifende Analyse für eine Virtual Report Suite aktiviert ist, beachten Sie die folgenden Änderungen:

* Neben dem Namen der Virtual Report Suite wird ein neues geräteübergreifendes Symbol angezeigt. Dieses Symbol ist ausschließlich für geräteübergreifende Virtual Report Suites vorgesehen.
* Es sind neue Metriken mit den Bezeichnungen „Personen“ und „Eindeutige Geräte“ verfügbar.
* Die Metrik „Unique Visitors“ ist nicht verfügbar, da sie durch „Personen“ und „Eindeutige Geräte“ ersetzt wurde.
* Beim Erstellen von Segmenten wird der Segmentcontainer „Besucher“ durch den Container „Person“ ersetzt.

## Die berechnete Metrik „Komprimierung“

Die Fähigkeit der geräteübergreifenden Analyse, Geräte einander zuzuordnen, hängt von einer Vielzahl von Faktoren ab. Die Effektivität der Funktion beim Zuordnen von Daten kann mit einer berechneten Metrik, der so genannten Komprimierung, gemessen werden. Folgende Faktoren tragen unter anderem zur Komprimierung bei:

* Verwenden des Co-op-Diagramms oder des privaten Diagramms: Im Allgemeinen erhalten Organisationen, die die Co-op-Funktion von Geräten verwenden, bessere Komprimierungsraten als Organisationen, die das private Diagramm verwenden.
* Anmelderate: Je mehr Benutzer sich auf Ihrer Site anmelden, desto besser kann Adobe Besucher geräteübergreifend identifizieren und zuordnen. Sites mit einer niedrigen Anmelderate haben auch niedrige Komprimierungsraten.
* Experience Cloud ID-Abdeckung: Es können nur Besucher mit einer ECID zugeordnet werden. Ein geringerer Prozentsatz der Besucher Ihrer Site, die eine ECID verwenden, steht im Zusammenhang mit niedrigeren Kompressionsraten.
* Verwendung mehrerer Geräte: Wenn Besucher Ihrer Site nicht mehrere Geräte verwenden, erhalten Sie niedrigere Komprimierungsraten.
* Berichtsgranularität: Die Komprimierung nach Tag ist in der Regel kleiner als die Komprimierung nach Monat oder Jahr. Die Wahrscheinlichkeit, dass eine Person mehrere Geräte verwendet, ist innerhalb eines Tages geringer als innerhalb eines ganzen Monats. Bei der Segmentierung, Filterung oder Verwendung von Aufschlüsselungsdimensionen kann es auch zu einer niedrigeren Komprimierungsrate kommen.

So sehen Sie die Komprimierung Ihrer Organisation für einen bestimmten Zeitraum:

1. Klicken Sie oben in Workspace auf „Neues Projekt erstellen“.
2. Beginnen Sie mit einem leeren Projekt und klicken Sie dann auf „Erstellen“.
3. Ziehen Sie die Metrik „Eindeutige Geräte“ in den Arbeitsflächenbereich mit der Bezeichnung „Metrik hier ablegen“.
4. Ziehen Sie die Metrik „Personen“ direkt rechts neben der Überschrift der Metrik „Eindeutige Geräte“ auf die Arbeitsfläche, damit sich die beiden Metriken nebeneinander befinden.
5. Klicken Sie links neben den verfügbaren Metriken auf das Symbol „`+`“, um den Generator für berechnete Metriken zu öffnen.
6. Geben Sie für diese berechnete Metrik die folgenden Einstellungen ein:
   * Name: Geräteübergreifende Komprimierung
   * Format: Prozent
   * Dezimalstellen: 2
   * Definition: `[Static Number: 1] minus [People] divided by [Unique Devices]`
      > [!TIP] Klicken Sie oben rechts im Definitionsbereich auf „Hinzufügen“, um eine statische Zahl hinzuzufügen. Ziehen Sie „Personen“ und „Eindeutige Geräte“ aus der Liste der verfügbaren Metriken auf der linken Seite.
7. Klicken Sie auf „Speichern“.
8. Ziehen Sie die neue berechnete Metrik direkt rechts neben der Überschrift der Metrik „Personen“ auf die Arbeitsfläche, damit sich alle drei Metriken nebeneinander befinden.
9. Optional: Der Arbeitsbereich lädt standardmäßig die Dimension „Tag“. Ziehen Sie eine alternative Datumsdimension (z. B. „Woche“ oder „Monat“) auf die Dimension „Tag“, wenn eine andere Zeitgranularität gewünscht wird.
