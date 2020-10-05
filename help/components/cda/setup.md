---
title: Geräteübergreifende Analyse einrichten
description: Konfigurieren Sie eine Virtual Report Suite, um die geräteübergreifende Analyse (CDA) zu aktivieren.
translation-type: tm+mt
source-git-commit: 60fe85adaebee8ca390e59727dda949c12c1ee26
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 91%

---


# Geräteübergreifende Analyse einrichten

Wenn alle Voraussetzungen erfüllt sind, aktivieren Sie die geräteübergreifende Analyse mit den folgenden Schritten. Sie müssen einer Produktprofil-Administratorgruppe angehören oder über Administratorrechte in Adobe Analytics verfügen, um diese Schritte ausführen zu können.

>[!IMPORTANT]
>
>Alle Voraussetzungen müssen erfüllt sein, bevor Sie diese Schritte durchführen. Wenn nicht alle Voraussetzungen erfüllt sind, ist die Funktion nicht verfügbar oder sie funktioniert nicht. Siehe die [Übersichtsseite](overview.md) und die gewünschte Stitching-Methode ([feldbasiertes Stitching](field-based-stitching.md) oder [Gerätediagramm](device-graph.md)) für Voraussetzungen und Einschränkungen.

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
8. Aktivieren Sie das Kontrollkästchen „Besuche von Benutzern geräteübergreifend zuordnen“.
9. Klicken Sie auf „Weiter“, konfigurieren Sie die Virtual Report Suite und klicken Sie dann auf „Speichern“.

![Kontrollkästchen „Geräteübergreifende Analyse“](assets/cda-checkbox.png)

## Hinzufügungen und Änderungen an geräteübergreifenden Virtual Report Suites

Wenn die geräteübergreifende Analyse für eine Virtual Report Suite aktiviert ist, beachten Sie die folgenden Änderungen:

* Neben dem Namen der Virtual Report Suite wird ein neues geräteübergreifendes Symbol angezeigt. Dieses Symbol ist ausschließlich für geräteübergreifende Virtual Report Suites vorgesehen.
* A new dimension labeled [Identified state](../dimensions/identified-state.md) is available. Diese Dimension bestimmt, ob die Experience Cloud ID für diesen Treffer dem Gerätediagramm zu diesem Zeitpunkt bekannt ist.
* New metrics labeled [People](../metrics/people.md) and [Unique Devices](../metrics/unique-devices.md) are available.
* The metric [Unique Visitors](../metrics/unique-visitors.md) is not available, as it is replaced with &#39;People&#39; and &#39;Unique Devices&#39;.
* Beim Erstellen von Segmenten wird der Segmentcontainer „Besucher“ durch den Container „Person“ ersetzt.
