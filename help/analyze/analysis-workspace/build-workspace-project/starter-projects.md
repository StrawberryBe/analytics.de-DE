---
description: Erstellen Sie Workspace-Projekte auf der Grundlage von Standard- oder benutzerdefinierten Vorlagen.
title: Vorlagen
feature: Workspace Basics
role: User, Admin
exl-id: 751399fe-6d4f-47cc-8827-82c992079b52
source-git-commit: be913fb9bae7954864b180490364c275c7bf7f15
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 95%

---

# Vorlagen

Für die Erstellung eines Projekts gibt es folgende Ausgangspunkte:

* **Leeres Projekt (Standard)**: Anweisungen hierzu finden Sie unter [Erstellen eines Projekts in Analysis Workspace](/help/analyze/analysis-workspace/home.md).
* **Standardvorlage**: Diese Vorlagen werden von Adobe erstellt und mit dem Produkt geliefert.
* **Benutzerdefinierte Vorlage**: Diese Vorlagen können von Benutzern mit Administratorrechten oder von Nichtadministratoren erstellt, freigegeben oder gelöscht werden, sofern ihnen die Berechtigung [!UICONTROL Analysis Workspace: als Vorlage speichern] in der Admin Console erteilt wurde. [Weitere Informationen ...](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/product-profile.html?lang=de)

![](assets/start_modal.png)

## Erstellen benutzerdefinierter Vorlagen {#create-custom-template}

Benutzer mit Administratorrechten können aus jedem erstellten Projekt eine benutzerdefinierte Vorlage machen. So geht’s:

1. Öffnen Sie das Projekt.
1. Wählen Sie **[!UICONTROL Projekt]** > **[!UICONTROL Als Vorlage speichern]**.

   ![](assets/save_project_template.png)

   Das Projekt wird unter dem aktuellen Projektnamen gefolgt von dem Wort (Vorlage) in Klammern gespeichert. Administratoren können diese Benennung durch Bearbeiten der Vorlage ändern.

   >[!NOTE]
   >
   >Projektvorlagen sind standardmäßig für jeden in Ihrer Organisation sichtbar. Sie können sie ordnen, indem Sie Tags auf sie anwenden. (Wählen Sie **[!UICONTROL Projekt]** > **[!UICONTROL Projektinfo und Einstellungen]** aus, um Tags und Beschreibungen zu bearbeiten.)

Im Folgenden finden Sie ein Video zum Erstellen und Verwalten benutzerdefinierter Vorlagen:

>[!VIDEO](https://video.tv.adobe.com/v/23231/?quality=12)

### Verwalten benutzerdefinierter Vorlagen {#manage-custom-template}

| Aktion | Beschreibung |
|--- |--- |
| Vorlage   bearbeiten | Lässt einen Administrator die Vorlage durch Änderung der Datenquelle, Anpassung von Komponenten, Visualisierungen, Datumsbereichen usw. bearbeiten.  Um eine Standardvorlage zu bearbeiten, können Sie entweder<ul><li>die Liste von benutzerdefinierten Vorlagen in Analysis Workspace öffnen, eine auswählen und auf „Vorlage bearbeiten“ klicken oder</li><li>in Analytics „Komponenten“ > „Projekte“ auswählen und dann nach Vorlagen filtern. Klicken Sie auf den Namen der Vorlage, die Sie bearbeiten möchten.</li></ul>**Hinweis:** Nachdem Sie eine Vorlage bearbeitet haben, haben Sie je nach Situation zwei Optionen: „Speichern“ oder „Speichern unter“. Sie unterscheiden sich in Folgendem:<ul><li>**Speichern:** Die benutzerdefinierte Vorlage wird für alle Benutzer aktualisiert. Wenn jemand anderer ein Projekt aus dieser benutzerdefinierten Vorlage erstellt, sieht er die von Ihnen gemachten Änderungen.</li><li>**Speichern unter:** Erstellt eine Kopie der benutzerdefinierten Vorlage mit Ihren Änderungen. (Dass Sie im Bearbeitungsmodus sind, lässt sich daran erkennen, dass das Menüelement „Freigabe“ > „Projekt freigeben“ deaktiviert ist.)</li></ul> |
| Nach Vorlagen suchen | Klicken Sie im Dialogfeld „Benutzerdefinierte Vorlagen“ auf „Vorlagen suchen“. |
| Vorlagen ordnen | Sie können Vorlagen alphabetisch, nach Relevanz und nach Erstellungsdatum ordnen.  Klicken Sie im Dialogfeld „Benutzerdefinierte Vorlagen“ auf „Ordnen“. |
| Tags auf eine Vorlage anwenden | Öffnen Sie die Vorlage und wählen Sie „Projekt“ > „Projektinfo und Einstellungen“. Klicken Sie auf „Tags hinzufügen“. |
| Vorlagenbeschreibung ändern | Öffnen Sie die Vorlage und wählen Sie „Projekt“ > „Projektinfo und Einstellungen“. Doppelklicken Sie auf die Beschreibung und bearbeiten Sie sie. |


## Standardvorlagen

Wenn Sie einen Workspace zum ersten Mal öffnen, sind Vorlagen in der linken Leiste verfügbar. Analysis Workspace-Vorlagen decken häufige Anwendungsfälle ab. Diese sind senkrecht danach gruppiert, wohin sie gehören, und werden je nach der Report Suite, die Sie auswählen, mit verschiedenen Dimensionen, Segmenten, Metriken und Visualisierungen aufgefüllt.

Sie können diese fertig ausgefüllten Vorlagen unverändert übernehmen oder an Ihre spezifischen Anforderungen anpassen (indem Sie beispielsweise Metriken oder Visualisierungen hinzufügen oder austauschen) und dann unter einem neuen Namen speichern.

Hier finden Sie ein Tutorial zu [Standardvorlagen in Analysis Workspace](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/analysis-workspace-basics/standard-templates-in-analysis-workspace.html?lang=de) (2:46)

Im Folgenden finden Sie verfügbare Vorlagen und die Fragen, die die einzelnen Vorlagen beantworten.

### Schulung

Diese Standardvorlage führt Sie durch die gängige Terminologie und die Schritte zur Erstellung Ihrer ersten Analyse in Workspace. Sie ist als Standardvorlage unter „Neues Projekt“ enthalten und ersetzt das Beispielprojekt, das bislang neuen Anwendern angeboten wurde, die keine anderen Projekte in ihrer Liste haben.

Im Folgenden finden Sie ein Video zur Vorlage [!UICONTROL Schulungsanleitung]:

>[!VIDEO](https://video.tv.adobe.com/v/33773/?quality=12)

### Werbung

>[!IMPORTANT]
>
>Werbevorlagen sind nur verfügbar, wenn Ihre Report Suite für [Advertising Analytics](https://experienceleague.adobe.com/docs/analytics/integration/advertising-analytics/overview.html?lang=de) aktiviert ist.

* **Paid Search-Suchmaschinen**: Diese Vorlage bietet eine Aufschlüsselung nach Werbe-Trends, Anzeigenplattformen, Keywords, Konten, Kampagnen und mehr.

### Handel

* **Magento: Marketing und Handel**: Diese Vorlage schlüsselt Ihre E-Commerce-Konversionen nach der Marketing-Kanal-Attribution auf und bietet Einblicke nach Suchbegriff, Landingpage, Standort und mehr. Hier finden Sie ein Video-Tutorial zum Thema [Magento: Marketing- und Commerce-Vorlage](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/magento/magento-analysis-workspace-template.html?lang=de).

### Datenerfassung

* **Auswirkung von ITP**: Informationen dazu, wie sich ITP von Apple auf Ihre Daten auswirkt und Sie die Berichterstattung entsprechend anpassen können.

### Medien

* **Nutzung von Inhalten**: Wer sind meine treuen Leser?
* **Neuigkeit – Häufigkeit – Treue**: Welche Inhalte werden am häufigsten genutzt und sind für Benutzer besonders interessant?
* **Nutzung von Streaming-Medien**: Liefert die Entwicklung und die wichtigsten Metriken der Mediennutzung auf allen digitalen Geräten. Im Folgenden finden Sie ein Video zur Vorlage zur Nutzung von Streaming-Medien:

   >[!VIDEO](https://video.tv.adobe.com/v/23901/?quality=12)

### Mobil

>[!IMPORTANT]
>
>Mobile Vorlagen sind nur dann verfügbar, wenn Ihre Report Suite für die Analyse von Mobile Apps aktiviert ist.

* **Akquise:** Hier erfahren Sie mehr zur Leistung von mobilen Akquise-Links.
* **Anwendungsnutzung:** Wie viele Anwendungsbenutzer, Starts und erste Starts hat die Anwendung verzeichnet und wie lange dauerte eine durchschnittliche Sitzung?
* **Journeys:** Welche markanten Verwendungsmuster weist meine Anwendung auf?
* **Schlüsselmetriken:** Sehen Sie sich die wichtigsten Metriken Ihrer Anwendung genauer an.
* **Standort:** Beinhaltet eine Karte zur Anzeige von Standortdaten.
* **Messaging:** Zeigt die Leistung von In-App- und Push-Nachrichten.
* **Leistung:** Welche Leistung erzielt die Anwendung und wo haben Benutzer Probleme?
* **Bindungsgrad:** Wer sind meine treuen Benutzer und was tun sie?

### Einzelhandel

* **Kampagnenleistung:** Welche Kampagnen erzielen den höchsten Umsatz?
* **Produkte:** Welche Produkte schneiden am besten ab?

### Web

* **Akquise:** Was sind die wichtigsten Faktoren, durch die Traffic auf meine Website geleitet wird?
* **AEM Site-Performance – Übersicht:** Welche Leistung erzielt meine Adobe Experience Manager-Site?
* **Content-Konsum:** Wohin navigieren Besucher auf meiner Website am häufigsten?
* **Bindungsgrad:** Welche Arten von Benutzern bleiben meiner Website wahrscheinlich treu?
* **Technologie:** Welche Technologien werden verwendet, um auf meine Website zu gelangen?

### Personen

Diese Vorlage basiert auf der Personen-Metrik, die eine deduplizierte Version der Metrik „Unique Visitors“ ist. Die Metrik für Personen bietet einen Messwert im Hinblick darauf, wie oft Verbraucher, die mehrere Geräte verwenden, mit Ihrer Marke interagieren. Mithilfe der Vorlage können Sie:

* Segmentieren Sie Ihre Daten für die USA/Kanada im Vergleich zum Rest der Welt.
* Metriken für Personen und Unique Visitors nebeneinander vergleichen
* Sehen Sie die &quot;Komprimierungsrate&quot;, eine berechnete Metrik, die berechnet, wie viel kleiner die Metrik für Personen als Prozentsatz von Unique Visitors ist.
* die Gesamtzahlen der Gerätetypen vergleichen, die Ihre Kunden verwenden;
* Ermitteln Sie, wie viele Geräte pro Person im Durchschnitt verwendet werden
* herausfinden, wie Sie die Segmentstapelung mit der Metrik für Personen verwenden
* Entdecken Sie, wie die Experience Cloud ID in Ihrer Umgebung zur Effizienzverbesserung der Metrik für Personen beiträgt

### Journey-IQ: Vorlage für geräteübergreifende Analysen

<!--This content is mirrored in the CDA doc.-->

Mit dieser Vorlage können Sie wichtige geräteübergreifende Leistungsdaten erfassen. Sie steht nur Kunden zur Verfügung, die Zugriff auf [geräteübergreifende Analysen](https://experienceleague.adobe.com/docs/analytics/components/cda/overview.html?lang=de) (Cross-Device Analytics, CDA) haben.

* **Identifizierung der Benutzer**: Zeigt an, wie oft Besucher Ihrer Site mit Methoden identifiziert werden, die auf geräteübergreifenden Analysen basieren.
* **Messen der Zielgruppengröße**: Zeigt einen Vergleich von „Eindeutige Geräte“ mit „Personen“ an. Der Anteil dieser beiden Zahlen wird als „geräteübergreifende Komprimierung“ bezeichnet, eine berechnete Metrik, die in diesem Bedienfeld angezeigt wird. Diese Komprimierungsmetrik hängt von einer Vielzahl von Faktoren ab:
   * **Anmelderate**: Je mehr Benutzer sich auf Ihrer Site anmelden, desto besser kann Adobe Besucher geräteübergreifend identifizieren und zuordnen. Sites mit einer niedrigen Anmelderate haben auch niedrige Komprimierungsraten.
   * **Experience Cloud ID-Abdeckung**: Es können nur Besucher mit einer ECID zugeordnet werden. Ein geringerer Prozentsatz der Site-Besucher, die eine ECID verwenden, steht im Zusammenhang mit niedrigeren Komprimierungsraten.
   * **Verwendung mehrerer Geräte**: Wenn Besucher Ihrer Site nicht mehrere Geräte verwenden, erhalten Sie niedrigere Komprimierungsraten.
   * **Berichtsgranularität**: Die Komprimierung nach Tag ist in der Regel kleiner als die Komprimierung nach Monat oder Jahr. Die Wahrscheinlichkeit, dass eine Person mehrere Geräte verwendet, ist innerhalb eines Tages geringer als innerhalb eines ganzen Monats. Bei der Segmentierung, Filterung oder Verwendung von Aufschlüsselungsdimensionen kann es auch zu einer niedrigeren Komprimierungsrate kommen.
* **Personenbasierte Segmente**: Enthält eine Segment-Dropdown-Liste, mit der Sie gerätespezifische Daten anzeigen können. In diesem Bedienfeld können Sie mit Segmenten experimentieren, um festzustellen, wie sich das Einschließen oder Ausschließen von Gerätetypen auf Berichte auswirkt.
* **Analyse der geräteübergreifenden Journey**: Bietet Fluss- und Fallout-Berichte je nach Gerätetyp.
* **Geräteübergreifende Zuordnung**: Kombinieren Sie die Funktionen von Journey IQ und Attribution IQ miteinander.
* **Weitere Tipps und Tricks**: Hilfreiche Themen rund um CDA, mit denen Sie die Nutzung optimieren können.
