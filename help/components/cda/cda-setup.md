---
title: Geräteübergreifende Analyse einrichten
description: Erfahren Sie, wie Sie die geräteübergreifende Analyse einrichten, wenn Sie die Voraussetzungen erfüllen.
translation-type: tm+mt
source-git-commit: d847fb9dc1427727a0162be993ddc4a73c52f192
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 63%

---


# Geräteübergreifende Analyse einrichten

Wenn alle Voraussetzungen erfüllt sind, aktivieren Sie die geräteübergreifende Analyse mit den folgenden Schritten. Sie müssen einer Produktprofil-Administratorgruppe angehören oder über Administratorrechte in Adobe Analytics verfügen, um diese Schritte ausführen zu können.

>[!IMPORTANT] Alle Voraussetzungen müssen erfüllt sein, bevor Sie diese Schritte durchführen. Wenn nicht alle Voraussetzungen erfüllt sind, ist die Funktion nicht verfügbar oder sie funktioniert nicht. Informationen zu Voraussetzungen und Einschränkungen finden Sie unter [Geräteübergreifende Analyse](cda-home.md).

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
* Eine neue Dimension mit der Bezeichnung &quot;Identifizierter Status&quot;ist verfügbar. Diese Dimension bestimmt, ob die Experience Cloud-ID bei diesem Treffer vom Gerätediagramm zu diesem Zeitpunkt bekannt ist.
* Es sind neue Metriken mit den Bezeichnungen „Personen“ und „Eindeutige Geräte“ verfügbar.
* Die Metrik &quot;Individuelle Besucher&quot;ist nicht verfügbar, da sie durch &quot;Personen&quot;und &quot;Unique Devices&quot;ersetzt wird.
* Beim Erstellen von Segmenten wird der Segmentcontainer „Besucher“ durch den Container „Person“ ersetzt.

## CDA Workspace-Vorlage

Adobe Angebot eine Vorlage, um wichtige geräteübergreifende Leistungsdaten anzuzeigen.

1. Navigieren Sie zu [experiencecloud.adobe.com](https://experiencecloud.adobe.com) und melden Sie sich mit Ihren AdobeID-Anmeldeinformationen an.
1. Klicken Sie oben auf das 9-Raster-Symbol und dann auf Analytics.
1. Click [!UICONTROL Workspace] at the top, then click [!UICONTROL Create New Project].
1. Suchen Sie nach dem &quot;Journey IQ: &quot;Geräteübergreifende Analyse&quot;-Vorlage und klicken Sie dann auf [!UICONTROL Erstellen].
1. Ändern Sie bei Aufforderung die Report Suite in eine Report Suite, die CDA unterstützt.

Es wird ein Analyse Workspace-Projekt erstellt, das mehrere Bereiche enthält. Oben werden ein Inhaltsverzeichnis und eine Einführung angezeigt, die den Kontext zum Bericht und die Navigation zu einzelnen Berichten ermöglichen. Klicken Sie auf einen Link im Inhaltsverzeichnis oder erweitern Sie das Akkordeon eines Bereichs, um diese Berichte zur Ansicht zu verwenden.

<!-->The content below is mirrored in /help/analyze/analysis-workspace/build-workspace-project/starter-projects.md<-->

* **Besondere Anmerkung für die Mitglieder des Kooperationdiagramms**: Zeigt, welcher Teil Ihrer Report Suite Besucher in Regionen enthält, in denen das Co-op-Diagramm unterstützt wird, und in Regionen, in denen es nicht unterstützt wird.
* **Identifizierung der Benutzer**: Zeigt, wie oft Besucher Ihrer Site anhand von geräteübergreifenden Analysen identifiziert werden.
* **Messen der Audience**: Zeigt einen Vergleich von &quot;Unique Devices&quot;mit &quot;People&quot;an. Der Anteil dieser beiden Zahlen wird als &quot;geräteübergreifende Komprimierung&quot;bezeichnet, eine berechnete Metrik, die in diesem Bedienfeld sichtbar ist. Diese Komprimierungsmetrik hängt von einem breiten Spektrum von Faktoren ab:
   * Verwenden des Co-op-Diagramms oder des privaten Diagramms: Im Allgemeinen erhalten Organisationen, die die Co-op-Funktion von Geräten verwenden, bessere Komprimierungsraten als Organisationen, die das private Diagramm verwenden.
   * Anmelderate: Je mehr Benutzer sich auf Ihrer Site anmelden, desto besser kann Adobe Besucher geräteübergreifend identifizieren und zuordnen. Sites mit einer niedrigen Anmelderate haben auch niedrige Komprimierungsraten.
   * Experience Cloud ID-Abdeckung: Es können nur Besucher mit einer ECID zugeordnet werden. Ein geringerer Prozentsatz der Besucher Ihrer Site, die eine ECID verwenden, steht im Zusammenhang mit niedrigeren Kompressionsraten.
   * Verwendung mehrerer Geräte: Wenn Besucher Ihrer Site nicht mehrere Geräte verwenden, erhalten Sie niedrigere Komprimierungsraten.
   * Berichtsgranularität: Die Komprimierung nach Tag ist in der Regel kleiner als die Komprimierung nach Monat oder Jahr. Die Wahrscheinlichkeit, dass eine Person mehrere Geräte verwendet, ist innerhalb eines Tages geringer als innerhalb eines ganzen Monats. Bei der Segmentierung, Filterung oder Verwendung von Aufschlüsselungsdimensionen kann es auch zu einer niedrigeren Komprimierungsrate kommen.
* **Benutzerbasierte Segmente**: Enthält ein Segment-Dropdown, das die Ansicht gerätespezifischer Daten ermöglicht. In diesem Bereich wird empfohlen, mit Segmenten zu experimentieren, um zu sehen, wie sich das Ein- oder Ausschließen von Gerätetypen auf Berichte auswirkt.
* **Analyse der geräteübergreifenden Reise**: Bietet Fluss- und Trichteranalyseberichte je nach Gerätetyp.
* **Geräteübergreifende Zuordnung**: Kombinieren Sie die Funktionen von Journey IQ und Attribution IQ zusammen.
* **Weitere Tipps und Tricks**: Hilfreiche Themen rund um CDA, mit denen Sie mehr aus der Nutzung herausholen können.
