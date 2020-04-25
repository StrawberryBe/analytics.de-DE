---
description: 'null'
title: Vorlagen
uuid: d6d1b745-a684-41c1-879b-9f9a9503fe00
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Vorlagen

Für die Erstellung eines Projekts gibt es folgende Ausgangspunkte:

* **Leeres Projekt (Standard)**: Anweisungen hierzu finden Sie unter [Erstellen eines Analyse Workspace-Projekts](/help/analyze/analysis-workspace/build-workspace-project/t-freeform-project.md).
* **Standardvorlage**: Diese Vorlagen werden von Adobe erstellt und mit dem Produkt geliefert.
* **Benutzerdefinierte Vorlage**: Diese Vorlagen können von Benutzern mit Administratorrechten oder von Nichtadministratoren erstellt, freigegeben oder gelöscht werden, sofern ihnen die [!UICONTROL Analysis Workspace: Save as Template] Berechtigung in der Admin-Konsole erteilt wurde. [Mehr Infos...](https://docs.adobe.com/content/help/en/analytics/admin/admin-console/permissions/product-profile.html)

![](assets/start_modal.png)

## Erstellen einer benutzerdefinierten Vorlage {#create-custom-template}

Benutzer mit Administratorrechten können aus jedem erstellten Projekt eine benutzerdefinierte Vorlage machen. So geht’s:

1. Öffnen Sie das Projekt.
1. Öffnen von **[!UICONTROL Project]** > **[!UICONTROL Save As Template]**.

   ![](assets/save_project_template.png)

   Das Projekt wird unter dem aktuellen Projektnamen gefolgt von dem Wort (Vorlage) in Klammern gespeichert. Administratoren können diese Benennung durch Bearbeiten der Vorlage ändern.

   >[!NOTE]
   >
   >Projektvorlagen sind standardmäßig für jeden in Ihrer Organisation sichtbar. Sie können sie ordnen, indem Sie Tags auf sie anwenden. (Gehen Sie zu **[!UICONTROL Project]** > **[!UICONTROL Project Info & Settings]** , um Tags und Beschreibungen zu bearbeiten.)

### Auf benutzerdefinierte Vorlagen anwendbare Aktionen

![](assets/custom_templates.png)

| Aktion | Beschreibung |
|--- |--- |
| Vorlage  bearbeiten | Lässt einen Administrator die Vorlage durch Änderung der Datenquelle, Anpassung von Komponenten, Visualisierungen, Datumsbereichen usw. bearbeiten.  Um eine Standardvorlage zu bearbeiten, können Sie entweder<ul><li>die Liste von benutzerdefinierten Vorlagen in Analysis Workspace öffnen, eine auswählen und auf Vorlage bearbeiten klicken oder</li><li>in Analytics Komponenten > Projekte wählen und dann nach Vorlagen filtern. Klicken Sie auf den Namen der Vorlage, die Sie bearbeiten möchten.</li></ul>**Hinweis:** Nachdem Sie eine Vorlage bearbeitet haben, haben Sie je nach Situation zwei Optionen: Speichern, Speichern unter. Sie unterscheiden sich in Folgendem:<ul><li>**Speichern:** Aktualisiert die benutzerdefinierte Vorlage für alle Benutzer. Wenn jemand anderer ein Projekt aus dieser benutzerdefinierten Vorlage erstellt, sehen sie die von Ihnen gemachten Änderungen.</li><li>**Speichern unter:** Erstellt eine Kopie der benutzerdefinierten Vorlage mit Ihren Änderungen. (Dass Sie im Bearbeitungsmodus sind, lässt sich daran erkennen, dass das Menüelement Freigabe > Projekt freigeben deaktiviert ist.)</li></ul> |
| Nach Vorlagen suchen | Klicken Sie im Dialogfeld „Benutzerdefinierte Vorlagen“ auf Vorlagen suchen. |
| Vorlagen ordnen | Sie können Vorlagen alphabetisch, nach Relevanz und nach Erstellungsdatum ordnen.  Klicken Sie im Dialogfeld „Benutzerdefinierte Vorlagen“ auf Ordnen:. |
| Tags auf eine Vorlage anwenden | Öffnen Sie die Vorlage und wählen Sie Projekt > Projektinfo und Einstellungen. Klicken Sie auf Tags hinzufügen. |
| Vorlagenbeschreibung ändern | Öffnen Sie die Vorlage und wählen Sie Projekt > Projektinfo und Einstellungen. Doppelklicken Sie auf die Beschreibung und bearbeiten Sie sie. |


## Standardvorlagen

Wenn Sie einen Workspace zum ersten Mal öffnen, sind Vorlagen in der linken Leiste verfügbar. Analysis Workspace-Vorlagen decken häufige Anwendungsfälle ab. Diese sind senkrecht danach gruppiert, wohin sie gehören, und werden je nach der Report Suite, die Sie auswählen, mit verschiedenen Dimensionen, Segmenten, Metriken und Visualisierungen aufgefüllt.

Sie können diese fertig ausgefüllten Vorlagen unverändert übernehmen oder an Ihre spezifischen Anforderungen anpassen (indem Sie beispielsweise Metriken oder Visualisierungen hinzufügen oder austauschen) und dann unter einem neuen Namen speichern.

[Standardvorlagen in Analysis Workspace auf YouTube](https://www.youtube.com/watch?v=aRgYwPneVXg&amp;list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS&amp;index=6) (2:46)

Im Folgenden finden Sie verfügbare Vorlagen und die Fragen, die die einzelnen Vorlagen beantworten.

### Schulung

* **Schulungslehrgang**: Diese Standardvorlage führt Sie durch die gängige Terminologie und Schritte zum Aufbau Ihrer ersten Analyse in Workspace. Sie ist als Standardvorlage im Modul „Neues Projekt“ enthalten und ersetzt das Beispielprojekt, das bislang neuen Anwendern angeboten wurde, die keine anderen Projekte in ihrer Liste haben.

### Werbung

>[!IMPORTANT]
>
>Werbevorlagen sind nur verfügbar, wenn Ihre Report Suite für Advertising Cloud aktiviert ist.

* **Gebührenpflichtige Suchmaschinen**: Diese Vorlage unterteilt Werbetrends, Anzeigenplattformen, Suchbegriffe, Konten, Kampagnen und mehr.

### Handel

* **Magento: Marketing und Handel**: Diese Vorlage schlüsselt Ihre E-Commerce-Konversionen nach der Marketing-Kanal-Attribution auf und bietet Einblicke nach Suchbegriff, Einstiegsseite, Standort und mehr. Eine Videoübersicht finden Sie unter >[!VIDEO](https://www.youtube.com/watch?v=AQOViVLEMHw)

### Medien

* **Audio-Konsum**: Welche Inhalte werden von Benutzern am häufigsten aufgerufen?
* **Neuigkeit - Häufigkeit - Treue**: Wer sind meine treuen Leser?

### Mobile

>[!IMPORTANT]
>
>Mobile Vorlagen sind nur dann verfügbar, wenn Ihre Report Suite für „Mobile“ aktiviert ist.

* **Messaging:** Mit Augenmerk auf die Leistung von In-App- und Push-Nachrichten
* **Standort:** Beinhaltet eine Karte zur Anzeige von Standortdaten
* **Schlüsselmetriken:** Sehen Sie sich die wichtigsten Metriken Ihrer App genauer an.
* **App-Nutzung:** Wie viele App-Benutzer, Starts und erste Starts hat die App verzeichnet und wie lange dauerte eine durchschnittliche Sitzung?
* **Akquise:** Erfahren Sie mehr zur Leistung von mobilen Akquiselinks
* **Leistung:** Welche Leistung erzielt die Anwendung und wo haben Benutzer Probleme?
* **Bindungsgrad:** Wer sind meine treuen Benutzer und was tun sie?
* **Journeys:** Welche markanten Verwendungsmuster weist meine App auf?

### Einzelhandel

* **Kampagnenleistung:** Welche Kampagnen erzielen den höchsten Umsatz?
* **Produkte:** Welche Produkte schneiden am besten ab?

### Web

* **Akquise:** Was sind die wichtigsten Faktoren, durch die Traffic auf meine Website geleitet wird?
* **Content-Konsum:** Wohin navigieren Besucher auf meiner Website am häufigsten?
* **Bindungsgrad:** Welche Arten von Benutzern bleiben meiner Website wahrscheinlich treu?
* **Technologie:** Welche Technologien werden verwendet, um auf meine Website zu gelangen?

### Personen

>[!NOTE] Die Personenvorlage und die zugehörige Metrik für Personen sind nur im Rahmen von [Adobe Experience Cloud Device Co-op](https://marketing.adobe.com/resources/help/de_DE/mcdc/mcdc-people.html) verfügbar.

Diese Vorlage basiert auf der Metrik &quot;Personen&quot;, bei der es sich um eine deduplizierte Version der Metrik &quot;Individuelle Besucher&quot;handelt. Die Metrik für Personen bietet einen Messwert im Hinblick darauf, wie oft Verbraucher, die mehrere Geräte verwenden, mit Ihrer Marke interagieren. Mithilfe der Vorlage können Sie

* Ihre Daten für die USA/Kanada gegen die restliche Welt segmentieren (Device Co-op ist momentan nur in Nordamerika verfügbar);
* die Metriken für Personen und Unique Visitors nebeneinander vergleichen;
* die Komprimierungsrate anzeigen (dabei handelt es sich um eine berechnete Metrik, mit der Sie bestimmen können, um wie viel geringer die Metrik für Personen als Prozentsatz der Unique Visitors ist);
* die Gesamtzahlen der Gerätetypen vergleichen, die Ihre Kunden verwenden;
* anzeigen, wie viele Geräte durchschnittlich pro Person verwendet werden;
* herausfinden, wie Sie die Segmentstapelung mit der Metrik für Personen verwenden;
* Entdecken Sie, wie die Experience Cloud ID in Ihrer Umgebung zur Effizienzverbesserung der Metrik für Personen beiträgt.

### IQ: Geräteübergreifende Analytics-Vorlage

<!-->This content is mirrored in the CDA doc.<-->

Mit dieser Vorlage können Sie wichtige geräteübergreifende Leistungsdaten anzeigen. Sie steht nur Kunden zur Verfügung, die Zugriff auf [geräteübergreifende Analysen](https://docs.adobe.com/content/help/de-DE/analytics/components/cda/cda-home.html) haben.

* **Besondere Anmerkung für die Mitglieder des Kooperationdiagramms**: Zeigt, welcher Teil Ihrer Report Suite Besucher in Regionen enthält, in denen das Co-op-Diagramm unterstützt wird, und in Regionen, in denen es nicht unterstützt wird.
* **Identifizierung der Benutzer**: Zeigt, wie oft Besucher Ihrer Site anhand von geräteübergreifenden Analysen identifiziert werden.
* **Messen der Audience**: Zeigt einen Vergleich von &quot;Unique Devices&quot;mit &quot;People&quot;an. Der Anteil dieser beiden Zahlen wird als &quot;geräteübergreifende Komprimierung&quot;bezeichnet, eine berechnete Metrik, die in diesem Bedienfeld sichtbar ist. Diese Komprimierungsmetrik hängt von einem breiten Spektrum von Faktoren ab:
   * **Verwenden des Co-op-Diagramms oder des privaten Diagramms**: Im Allgemeinen sehen Organisationen, die die Geräte-Co-op verwenden, bessere Komprimierungsraten als Organisationen, die das private Diagramm verwenden.
   * **Anmeldungsrate**: Je mehr Benutzer sich auf Ihrer Site anmelden, desto mehr kann Adobe Besucher geräteübergreifend identifizieren und verbinden. Sites mit einer niedrigen Anmelderate haben auch niedrige Komprimierungsraten.
   * **Erlebnis-Cloud-ID-Abdeckung**: Es können nur Besucher mit einer ECID zusammengefügt werden. Ein geringerer Prozentsatz der Besucher Ihrer Site, die eine ECID verwenden, steht im Zusammenhang mit niedrigeren Kompressionsraten.
   * **Verwendung** mehrerer Geräte: Wenn Besucher Ihrer Site nicht mehrere Geräte verwenden, können Sie niedrigere Komprimierungsraten sehen.
   * **Berichte-Granularität**: Die Komprimierung nach Tag ist in der Regel kleiner als die Komprimierung nach Monat oder Jahr. Die Wahrscheinlichkeit, dass eine Person mehrere Geräte verwendet, ist innerhalb eines Tages geringer als innerhalb eines ganzen Monats. Bei der Segmentierung, Filterung oder Verwendung von Aufschlüsselungsdimensionen kann es auch zu einer niedrigeren Komprimierungsrate kommen.
* **Benutzerbasierte Segmente**: Enthält ein Segment-Dropdown, das die Ansicht gerätespezifischer Daten ermöglicht. In diesem Bereich wird empfohlen, mit Segmenten zu experimentieren, um zu sehen, wie sich das Ein- oder Ausschließen von Gerätetypen auf Berichte auswirkt.
* **Analyse der geräteübergreifenden Reise**: Bietet Fluss- und Trichteranalyseberichte je nach Gerätetyp.
* **Geräteübergreifende Zuordnung**: Kombinieren Sie die Funktionen von Journey IQ und Attribution IQ zusammen.
* **Weitere Tipps und Tricks**: Hilfreiche Themen rund um CDA, mit denen Sie mehr aus der Nutzung herausholen können.