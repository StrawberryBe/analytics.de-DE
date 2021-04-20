---
description: Häufig gestellte Fragen zur Segmentierung.
title: Häufig gestellte Fragen
feature: Segmentation
uuid: f49dc829-1d53-4183-9add-1aeaa5219d89
exl-id: 316e2a2e-55d3-4c23-9985-9a6d90390e86
translation-type: tm+mt
source-git-commit: f9b5380cfb2cdfe1827b8ee70f60c65ff5004b48
workflow-type: tm+mt
source-wordcount: '2078'
ht-degree: 100%

---

# Häufig gestellte Fragen

Beantwortet häufige Fragen zu Segmentierungsfunktionen, Zugriff, Berechtigungen, Best Practices und Verwaltung alter Segmente.

## Funktionen {#section_BD58629D1A9346BF879E229FA6BEC7A2}

* Segmentierung in Analysis Workspace:

   * Sie können [Segmente vergleichen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html).
   * Verwenden Sie [Segmente als Dimensionen](https://docs.adobe.com/content/help/de-DE/core-services/interface/audiences/audience-library.html) bei Vergleichen.
   * Verwenden Sie Segmente in der [Fallout-Analyse](https://docs.adobe.com/help/de-DE/analytics/analyze/analysis-workspace/visualizations/fallout/compare-segments-fallout.html).

* Sie können [mehrere Segmente auf einen Bericht oder ein Projekt anwenden](/help/components/segmentation/segmentation-workflow/seg-workflow.md).
* Alle Segmente gelten nun für alle Report Suites.
* Der [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-workflow.md) vereinfacht das Erstellen von Segmenten.
* Der neue [Segment-Manager](/help/components/segmentation/segmentation-workflow/seg-workflow.md) ermöglicht die Einrichtung von [Workflows](/help/components/segmentation/segmentation-workflow/seg-workflow.md) und bietet Funktionen zum Teilen, Taggen, Prüfen und Genehmigen.
* Sie können Segmente zum Organisieren und Suchen [taggen](/help/components/segmentation/segmentation-workflow/seg-workflow.md), anstatt Ordner zu verwenden.
* Sie können [sequenzielle Segmente](/help/components/segmentation/segmentation-workflow/seg-sequential-build.md) erstellen.
* Der Seitenansichts-Container wurde in Treffer-Container umbenannt, um anzuzeigen, dass dieser Container alle Datentypen segmentiert und nicht nur Seitenansichten. So werden z. B. Linktracking-Aufrufe und trackAction-Aufrufe aus den Mobile SDKs durch den Treffercontainer vollständig ein- oder ausgeschlossen. Beachten Sie, dass sich die Funktionsweise dieses Containers nicht geändert hat. Er wurde lediglich umbenannt.

Weitere Details finden Sie im Beitrag [Verbesserung der Segmentierung in Adobe Analytics](https://blogs.adobe.com/digitalmarketing/analytics/improving-segmentation-adobe-analytics/) im Digital Marketing Blog.

## Zugriff auf die Segmentierungswerkzeuge {#section_088AD0E4E21943DFA8CF7206AEC485DD}

**Wie komme ich zum Segment Builder?**

Sie können wie folgt auf den Segment Builder zugreifen:

* öffnen Sie einen vorhandenen Bericht und klicken Sie auf das Segmentsymbol ![](assets/segment_icon.png) im linken Navigationsmenü. Klicken Sie in der angezeigten Segmentleiste auf **[!UICONTROL Hinzufügen]** oder

* Klicken Sie oben im Segment-Manager auf **[!UICONTROL + Hinzufügen]**.  ![](assets/add_button.png)

   oder

* klicken Sie im Segment-Manager auf einen Segmenttitel, um das Segment im Segment Builder zu bearbeiten.

**Wie komme ich zum Segment-Manager?**

Sie können wie folgt auf den Segment-Manager zugreifen:

* Wechseln Sie in der oberen Navigation zu **[!UICONTROL Analysen]** > **[!UICONTROL Komponenten]**. Klicken Sie anschließend auf **[!UICONTROL Segmente]** oder

* öffnen Sie einen vorhandenen Bericht und klicken Sie auf das Segmentsymbol ![](assets/segment_icon.png) im linken Navigationsmenü. Klicken Sie anschließend auf **[!UICONTROL Verwalten]** oder

* drücken Sie an einer beliebigen Stelle die Schrägstrich-Taste (/) und suchen Sie nach Segment Manager.

**Wo ist das Dropdown-Feld für Segmente?**

Die Dropdown-Liste „Segmente“ in Reports &amp; Analytics wurde durch eine wesentlich umfangreichere Benutzeroberfläche des [Segment Builder](/help/components/segmentation/segmentation-workflow/seg-workflow.md) ersetzt, mit der Sie „universelle“ Segmente erstellen können, die über Report Suites und Adobe Analytics-Lösungen hinweg nutzbar sind. Um eine Liste der vorhandenen Segmente anzuzeigen, klicken Sie auf das Segmentsymbol ![](assets/segment_icon.png)

in der linken Navigation, woraufhin die Segmentleiste angezeigt wird.

**Wo ist das Dropdown-Feld für die Report Suite?**

Das Dropdown-Feld für die Report Suite wurde in die obere rechte Ecke jedes Berichts oder Dashboards neben die Datumsauswahl verschoben.

![](assets/report_suite_selector.png)

## Zugriffsberechtigung {#section_648DFA3A882146C485A84ED014EEC707}

**Welche Rechte und Privilegien benötige ich, um Segmente zu verwenden, zu erstellen und zu verwalten?**

Standardmäßig können alle Benutzer persönliche Segmente erstellen und bearbeiten. Administratoren können jedoch entscheiden, wer [Berechtigungen zur Erstellung von Segmenten](https://docs.adobe.com/content/help/de-DE/analytics/admin/user-product-management/user-groups/groups.html) erhält, und sie bestimmten Gruppen zuweisen. Diese Segmente können direkt für andere Analytics-Benutzer freigegeben werden.

Administratoren können alle Segmente bearbeiten und Segmente für Gruppen und alle Personen der Organisation freigeben. [Mehr …](/help/components/segmentation/seg-reference/seg-rights.md)

**Kann ich alle in meinem Unternehmen vorhandenen Segmente sehen?**

Ja, Administratoren können alle Segmente innerhalb der Benutzeroberflächen von [!DNL Analysis Workspace] und [!DNL Reports & Analytics] sehen.

Ad-hoc-Analysen und Report Builder zeigen Segmente an, deren Inhaber Sie sind, sowie Segmente, die für Sie freigegeben wurden.

**Kann ich alle Analytics-Segmente im Segment-Manager verwalten?**

Ja, alle Segmente können in Segment Manager verwaltet werden. Der Segment-Manager zeigt Segmente an, die für den Inhaber (den Benutzer, der das Segment erstellt hat), Benutzer, für die diese freigegeben sind, und Administratorbenutzer sichtbar sind. Die Segmentauswahl zeigt Segmente an, deren Inhaber der Benutzer ist, und solche, die für ihn freigegeben wurden.

Administratoren können alle Segmente innerhalb der Benutzeroberflächen von Analysis Workspace und [!DNL Reports & Analytics] sehen.

Report Builder zeigt nur von Ihnen erstellte Segmente oder Segmente, die für Sie freigegeben wurden, an.

**Warum kann ich dieses Segment nicht löschen?**

In der [Experience Cloud](/help/components/segmentation/segmentation-workflow/seg-workflow.md) veröffentlichte Segmente können nicht gelöscht oder bearbeitet werden. Sie können das Segment jedoch kopieren und die Kopie bearbeiten.

## Best Practices {#section_E2C3A1B4B4274D1B86CAA9C0359D049C}

**Was mache ich mit doppelten Segmenten, die denselben Namen und unterschiedliche Definitionen haben?**
Nachdem Segmente jetzt von unterschiedlichen Report-Suites genutzt werden können, kann es vorkommen, dass Sie mehrere Segmente mit demselben Namen haben. Wir empfehlen Folgendes:

* Benennen Sie Segmente um, die denselben Namen, aber unterschiedliche Definitionen haben, oder
* Löschen Sie Segmente, die Sie nicht mehr benötigen.

**Welche Empfehlungen hat Adobe bezüglich der Segmentbereinigung?**

* Markieren Sie alle alten Segmente mit einem Tag.
* Überprüfen Sie all Ihre Segmente.
* Fügen Sie Ihre Segmente gegebenenfalls zu einer Segmentbibliothek hinzu.
* Genehmigen Sie vorschriftsmäßige Segmente.
* Taggen Sie Segmente unter Einhaltung der [Best Practices](/help/components/segmentation/segmentation-workflow/seg-workflow.md).

## Verwaltung alter Segmente {#section_76CF47142D1A4FB6A0718AD9073049FE}

**Was ist mit meinen vorhandenen Segmenten passiert?**

Ihre vorhandenen Segmente funktionieren weiterhin wie bisher. Alle Berichte, auf die diese Segmente angewendet wurden, funktionieren weiterhin korrekt. [Mehr …](/help/components/segmentation/seg-transition.md)

Die meisten bisherigen vordefinierten und Suite-Segmente werden als Segmentvorlagen in den Segmentaufbau migriert. Segmentvorlagen werden verwendet, um schnell benutzerdefinierte Segmente mit gängigen Zielgruppen zu erstellen. Segmentvorlagen können nicht direkt auf einen Bericht angewendet werden, sie können aber problemlos in einem benutzerdefinierten Segment gespeichert werden.

Segmentvorlagen sind im Segmentaufbau durch ein spezielles Symbol gekennzeichnet:

![](assets/seg_templates.png)

**Was ist mit terminierten Berichten passiert, auf die Segmente angewendet sind?**

Terminierte Berichte werden weiterhin fehlerfrei mit den von Ihnen definierten Segmenten ausgeführt.

Wenn Sie ein Segment löschen, funktionieren terminierte Berichte und Dashboards, auf die dieses Segment angewendet wird, weiter normal, d. h., das Segment bzw. das Dashboard verwendet weiterhin das gelöschte Segment.

Terminierte Berichte werden nicht aktualisiert, wenn Sie ein Segment mit demselben Namen aktualisieren. Ein Beispiel: Angenommen, Sie haben 2 Segmente mit demselben Namen in unterschiedlichen Report Suites:

![](assets/duplicate_seg_names.png)

Sie haben ein Lesezeichen, das das Segment für die Report Suite „mainprod“ referenziert. Dann löschen Sie das Segment, weil es sich um ein Duplikat handelt. Das Lesezeichen funktioniert weiterhin und referenziert die Definition des gelöschten Segments. Wenn Sie die Segmentdefinition des maindev-Segments ändern und „Catalina Island“ und „Tijuana Mexiko“ einfügen, wird das auf das Lesezeichen angewendete Segment nicht geändert. Es verwendet weiterhin die alte Definition. Um dies zu beheben, müssen Sie das Lesezeichen aktualisieren, damit es die neue Definition referenziert. Wenn Sie nicht sicher sind, ob ein Lesezeichen, ein Dashboard oder ein terminierter Bericht ein gelöschtes Segment verwendet, können Sie den Namen des Segments ändern, damit deutlich wird, ob das Lesezeichen das Segment verwendet.

**Was passiert mit Data Warehouse-Segmenten?**

Alle vorhandenen Data Warehouse-Segmente funktionieren weiterhin in Data Warehouse. Die meisten Data Warehouse-Segmente funktionieren auch in anderen Komponenten, z. B. Analysis Workspace und Reports &amp; Analytics.

Sie können neue Data Warehouse-Segmente im Segment Builder/Segment-Manager erstellen oder bearbeiten. Durch den Produktkompatibilitätsmechanismus wird im Segment Builder automatisch ermittelt, ob ein Segment mit Data Warehouse kompatibel ist.

**Was geschieht mit vorkonfigurierten Segmenten?**

* **Einzelseitenbesuche**
* **Besuche von Mobilgeräten**
* **Besuche über eine kostenlose Suche**
* **Besuche über eine gebührenpflichtige Suche**
* **Besuche mit Besucher-ID-Cookie**

Diese Segmente werden als Segmentvorlagen in den Segmentaufbau migriert. Vorhandene Berichte, für die diese Segmente angewendet werden, funktionieren weiterhin fehlerfrei.

**Was geschieht mit Experience Cloud (Suite)-Segmenten?**

* Nichtkäufer
* Käufern
* Erstbesuche
* Besuche von sozialen Netzwerken aus
* Besuche, die länger als 10 Minuten dauern*
* Besuche mit mehr als 5 vorherigen Besuchen*
* Besuche von Facebook*

Die meisten dieser Segmente (ausgenommen die mit einem Sternchen * gekennzeichneten) werden als Segmentvorlagen in den Segmentaufbau migriert. Darüber hinaus wurden einige neue Segmente hinzugefügt.

Vorhandene Berichte, für die diese Segmente angewendet werden, funktionieren weiterhin fehlerfrei.

**Was geschieht mit Admin-Segmenten (auch bekannt als „globale“ Segmente)?**

**Admin**-Segmente werden in die neue Segmentoberfläche migriert und werden dort als für alle freigegebene Segmente angezeigt.

Der Eigentümer dieser Segmente wird mit dem ältesten Konto in der Liste der Admin-Benutzer in der Organisation als Admin angelegt. Es können jedoch alle Administratoren diese Segmente löschen, bearbeiten und teilen.

Die Segmentverwaltungsoberfläche der Admin Console, über die Administratoren diese globalen Segmente erstellen und verwalten konnten, gibt es nicht mehr. Administratoren sollten jetzt den neuen Segmentaufbau verwenden, um Segmente zu erstellen und für geeignete Gruppen, für alle oder für einzelne Personen freizugeben.

<!-- 

seg_definition.xml

 -->

Vorhandene Segmente, die Logik verwenden, die wie in diesem Dokument beschrieben geändert wurde, funktionieren weiterhin fehlerfrei, müssen jedoch aktualisiert werden, damit sie erneut gespeichert werden können. Wenn Sie z. B. ein vorhandenes Segment haben, in dem „US-Bundesstaaten“ „New York“ enthalten, funktioniert es weiterhin fehlerfrei. Wenn Sie das Segment jedoch das nächste Mal bearbeiten, müssen Sie es im Hinblick auf die Verwendung des Aufzählungstyps mit einer Gleich-Bedingung aktualisieren.

**Tipps zur Migration**

Folgende Tipps helfen Ihnen bei der Migration allgemeiner Dimensionen:

* Geo-Stadt/Region/Land – Suche nach und Auswahl bestimmter Städte, Regionen oder Länder, anstelle einer teilweisen Übereinstimmung.
* Browser – benutzen Sie die Browsertypen-Dimension, um alle Browser eines Typs zu erhalten, z. B. Google Chrome.
* Betriebssysteme – benutzen Sie die Betriebssystemtypen-Dimensionen, um alle Betriebssysteme eines Typs zu erhalten, z. B. Microsoft Windows.

* [Neue und umbenannte Dimensionen](/help/components/segmentation/seg-transition.md#section_73CF121B64A24DEF8E6499F3167BF742)
* [Änderungen an „Enthält“](/help/components/segmentation/seg-transition.md#section_1A9EDEE5CBC44B5AA6262560052ABE77)
* [Änderungen an „Weniger als“ und „Mehr als“](/help/components/segmentation/seg-transition.md#section_84A8AAD0344148AD9F9211D3EB271903)

## Neue und umbenannte Dimensionen {#section_73CF121B64A24DEF8E6499F3167BF742}

Die folgende Tabelle enthält eine Liste mit Dimensionen, die im Segmentaufbau umbenannt wurden.

<table id="table_1A8C1940FD0446FA8414C6A7DE66E44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Neuer Dimensionsname </th> 
   <th colname="col2" class="entry"> Vorheriger Name </th> 
   <th colname="col3" class="entry"> Hinweise </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Betriebssystemtypen </td> 
   <td colname="col2"> Neu </td> 
   <td colname="col3"> Hinzugefügt im Frühling 2015. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browser-Breite – zusammengefasst </td> 
   <td colname="col2"> Browser-Breite </td> 
   <td colname="col3"> Diese Dimension ist mit allen Benutzeroberflächen kompatibel und wird in eine Liste aufgezählter Bereiche, anstelle bestimmter Ganzzahlwerte unterteilt. Wenn Sie bestimmte Werte segmentieren müssen, benutzen Sie die granulare Version dieser Dimension in einem Data Warehouse-Segment. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browser-Höhe – zusammengefasst </td> 
   <td colname="col2"> Browser-Höhe </td> 
   <td colname="col3"> Diese Dimension ist mit allen Benutzeroberflächen kompatibel und wird in eine Liste aufgezählter Bereiche, anstelle bestimmter Ganzzahlwerte unterteilt. Wenn Sie bestimmte Werte segmentieren müssen, benutzen Sie die granulare Version dieser Dimension in einem Data Warehouse-Segment. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browserbreite – Granular </td> 
   <td colname="col2"> Browser-Breite </td> 
   <td colname="col3"> <p>Diese Dimension wurde umbenannt und ist jetzt nur mit Data Warehouse kompatibel. Wenn Sie Segmente definieren wollen, die mit allen Benutzeroberflächen kompatibel sind, benutzen Sie den Aufzählungstyp „Browserbreite – Zusammengefasst“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Browserhöhe – Granular </td> 
   <td colname="col2"> Browser-Höhe </td> 
   <td colname="col3"> <p>Diese Dimension wurde umbenannt und ist jetzt nur mit Data Warehouse kompatibel. Wenn Sie Segmente definieren wollen, die mit allen Benutzeroberflächen kompatibel sind, benutzen Sie den Aufzählungstyp „Browserhöhe – Zusammengefasst“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Cookie-Unterstützung </td> 
   <td colname="col2"> Cookies </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Farbtiefe </td> 
   <td colname="col2"> Bildschirmfarbtiefe </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> – </td> 
   <td colname="col2"> „App - *“ </td> 
   <td colname="col3"> Die „App -“-Präfixe wurden aus einigen Dimensionstypen entfernt. Da mobile App-Daten in der Regel in einer Report Suite erfasst werden, die keine Webdaten enthält, waren diese Präfixe nicht erforderlich. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ursprüngliche Entrypage </td> 
   <td colname="col2"> Ursprüngliche Entrypage </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Java aktiviert </td> 
   <td colname="col2"> Java </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maximale mobile Browser-URL-Länge </td> 
   <td colname="col2"> Länge der mobilen Browser-URL </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobilgerät – Mail-Design </td> 
   <td colname="col2"> Mobile Design-Mail-Unterstützung </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobilgerät </td> 
   <td colname="col2"> Mobilgerätname </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maximale mobile Lesezeichenlänge </td> 
   <td colname="col2"> Mobil Max. Lesezeichen URL-Länge </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Maximale mobile E-Mail-Länge </td> 
   <td colname="col2"> Mobil Max. Mail URL-Länge </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobiles Betriebssystem (Veraltet) </td> 
   <td colname="col2"> Mobilbetriebssystem </td> 
   <td colname="col3"> Benutzen Sie die Betriebssystem-Dimension und wenden Sie stattdessen Besuche von Mobilgerätesegmenten an. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobiles PTT </td> 
   <td colname="col2"> Mobile PTT </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Umfrageansichten </td> 
   <td colname="col2"> Umfrageansichten insgesamt </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Umfrageantworten </td> 
   <td colname="col2"> Umfrageantworten insgesamt </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Besuchstiefe </td> 
   <td colname="col2"> Path Length </td> 
   <td colname="col3"> – </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Postleitzahl </td> 
   <td colname="col2"> Postleitzahl </td> 
   <td colname="col3"> – </td> 
  </tr> 
 </tbody> 
</table>

## Änderungen an auf Zeichenketten basierenden Dimensionen, die bekannte Werte besitzen {#section_1A9EDEE5CBC44B5AA6262560052ABE77}

Auf Zeichenketten basierende Dimensionen, die einen bekannten Satz Werte besitzen, wurden in Aufzählungstypen geändert. Wenn Sie mit diesen Dimensionen ein Segment erstellen, wird die Liste mit allen bekannten Werten vorbelegt und „Gleich“ wird als einziger Operator unterstützt. So können Sie die genauen Werte, nach denen Sie suchen, schnell segmentieren, ohne nicht beabsichtigte Werte auszuwählen, die bei einer weniger restriktiven Übereinstimmung auftreten.

Folgende Dimensionen wurden in Aufzählungslisten geändert:

| Mobilgerätehersteller | Mobile E-Mail-Länge | Farbtiefe |
|---|---|---|
| Mobilgerät – Bildschirmgröße | Mobilgerätenummer | Bildschirmauflösung |
| Mobilgerät – Bildschirmhöhe | Mobilgerät – PTT | Plugin |
| Mobilgerät – Cookie-Unterstützung | Mobilgerät – Mail-Design | Betriebssystem |
| Mobilgerät – Bildunterstützung | Mobile Informationsdienste | Referrer-Typ |
| Mobilgerät – Farbtiefe | Mobilgerätetyp | Suchmaschine |
| Mobilgerät – Audio-Unterstützung | Browser-Typ | state |
| Mobilgerät – Video-Unterstützung | browser | Geo-Land |
| Mobil-DRM | Verbindungstyp | Geo-Region |
| Mobile Netzprotokolle | Mobilnetzbetreiber | Geo-Stadt |
| Mobilbetriebssystem | Cookie | Geo-DMA |
| Mobile Java-VM | Kundenloyalität | Persistentes Cookie |
| Mobile Lesezeichenlänge | Java aktiviert | Gebührenpflichtige Suche |
| Mobil URL-Länge | Sprache |  |

## Änderungen an auf Ganzzahlen basierenden Dimensionen, die bekannte Werte besitzen  {#section_84A8AAD0344148AD9F9211D3EB271903}

Auf Ganzzahlen basierende Dimensionen (wie die Browserbreite) mit einem bekannten Satz Werten werden in Aufzählungsbereiche aufgeteilt, sodass Sie schnell Segmente für einen bestimmten Bereich definieren können. Diese Aufzählungslisten erhalten nach dem Namen der Dimension den Zusatz „– Zusammengefasst“. Der folgende Bildschirm zeigt, wie diese Dimensionen mit der früheren und der neuen Segmentaufbauoberfläche segmentiert werden:

![](assets/seg_browser_dimension.png)

Die Operatoren „kleiner als“, „größer als“ und vergleichbare Operatoren sind jetzt nur noch mit Data Warehouse-Segmenten kompatibel. Segmente, die mit allen Berichtsoberflächen kompatibel sein sollen, müssen die „Zusammengefasst“-Version der Metrik mit dem Operator „Gleich“ verwenden.
