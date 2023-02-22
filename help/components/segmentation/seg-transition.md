---
description: Häufig gestellte Fragen zur Verwaltung von Legacy-Segmenten.
title: Häufig gestellte Fragen zu veralteten Segmenten
feature: Segmentation
exl-id: 316e2a2e-55d3-4c23-9985-9a6d90390e86
source-git-commit: e1ba6e93bcea4ece6e06941a97227a54116e2c25
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 94%

---

# Häufig gestellte Fragen zu veralteten Segmenten

Beantwortet häufige Fragen zu Best Practices für die Verwaltung älterer Segmente - Segmente, die vor 2014 erstellt wurden.

## Best Practices {#best-practices}

+++ **Was mache ich mit doppelten Segmenten, die denselben Namen und unterschiedliche Definitionen haben?**
Nachdem Segmente jetzt von unterschiedlichen Report-Suites genutzt werden können, kann es vorkommen, dass Sie mehrere Segmente mit demselben Namen haben. Wir empfehlen Folgendes:

* Benennen Sie Segmente um, die denselben Namen, aber unterschiedliche Definitionen haben, oder
* Löschen Sie Segmente, die Sie nicht mehr benötigen.

+++

+++ **Welche Empfehlungen hat Adobe bezüglich der Segmentbereinigung?**

* Markieren Sie alle alten Segmente mit einem Tag.
* Überprüfen Sie all Ihre Segmente.
* Fügen Sie Ihre Segmente gegebenenfalls zu einer Segmentbibliothek hinzu.
* Genehmigen Sie vorschriftsmäßige Segmente.
* Taggen Sie Segmente unter Einhaltung der  [Best Practices](/help/components/segmentation/segmentation-workflow/seg-workflow.md).

+++

## Verwaltung alter Segmente {#legacy}

+++ **Was ist mit meinen vorhandenen Segmenten passiert?**

Ihre vorhandenen Segmente funktionieren weiterhin wie bisher. Alle Berichte, auf die diese Segmente angewendet wurden, funktionieren weiterhin korrekt. [Mehr …](/help/components/segmentation/seg-transition.md)

Die meisten bisherigen vordefinierten und Suite-Segmente werden als  Segmentvorlagen in den Segmentaufbau migriert. Segmentvorlagen werden verwendet, um schnell benutzerdefinierte Segmente mit gängigen Zielgruppen zu erstellen. Segmentvorlagen können nicht direkt auf einen Bericht angewendet werden, sie können aber problemlos in einem benutzerdefinierten Segment gespeichert werden.

Segmentvorlagen sind im Segmentaufbau durch ein spezielles Symbol gekennzeichnet:

![](assets/seg_templates.png)

+++

+++ **Was ist mit terminierten Berichten passiert, auf die Segmente angewendet sind?**

Terminierte Berichte werden weiterhin fehlerfrei mit den von Ihnen definierten Segmenten ausgeführt.

Wenn Sie ein Segment löschen, funktionieren terminierte Berichte und Dashboards, auf die dieses Segment angewendet wird, weiter normal, d. h., das Segment bzw. das Dashboard verwendet weiterhin das gelöschte Segment.

Terminierte Berichte werden nicht aktualisiert, wenn Sie ein Segment mit demselben Namen aktualisieren. Ein Beispiel: Angenommen, Sie haben 2 Segmente mit demselben Namen in unterschiedlichen Report Suites:

![](assets/duplicate_seg_names.png)

Sie haben ein Lesezeichen, das das Segment für die Report Suite „mainprod“ referenziert. Dann löschen Sie das Segment, weil es sich um ein Duplikat handelt. Das Lesezeichen funktioniert weiterhin und referenziert die Definition des gelöschten Segments. Wenn Sie die Segmentdefinition des maindev-Segments ändern und „Catalina Island“ und „Tijuana Mexiko“ einfügen, wird das auf das Lesezeichen angewendete Segment nicht geändert. Es verwendet weiterhin die alte Definition. Um dies zu beheben, müssen Sie das Lesezeichen aktualisieren, damit es die neue Definition referenziert. Wenn Sie nicht sicher sind, ob ein Lesezeichen, ein Dashboard oder ein terminierter Bericht ein gelöschtes Segment verwendet, können Sie den Namen des Segments ändern, damit deutlich wird, ob das Lesezeichen das Segment verwendet.

+++

+++ **Was ist mit Data Warehouse-Segmenten passiert?**

Alle vorhandenen Data Warehouse-Segmente funktionieren weiterhin in Data Warehouse. Die meisten Data Warehouse-Segmente funktionieren auch in anderen Komponenten, z. B. Analysis Workspace und Reports &amp; Analytics.

Sie können neue Data Warehouse-Segmente im Segment Builder/Segment-Manager erstellen oder bearbeiten. Durch den Produktkompatibilitätsmechanismus wird im Segment Builder automatisch ermittelt, ob ein Segment mit Data Warehouse kompatibel ist.

+++

**Was ist mit vorkonfigurierten Segmenten passiert?**

* **Einzelseitenbesuche**
* **Besuche von Mobilgeräten**
* **Besuche über eine kostenlose Suche**
* **Besuche über eine gebührenpflichtige Suche**
* **Besuche mit Besucher-ID-Cookie**

Diese Segmente werden als Segmentvorlagen in den Segmentaufbau migriert. Vorhandene Berichte, für die diese Segmente angewendet werden, funktionieren weiterhin fehlerfrei.

+++

+++ **Was ist mit Experience Cloud (Suite)-Segmenten passiert?**

* Nichtkäufer
* Käufern
* Erstbesuche
* Besuche von sozialen Netzwerken aus
* Besuche, die länger als 10 Minuten dauern*
* Besuche mit mehr als 5 vorherigen Besuchen*
* Besuche von Facebook*

Die meisten dieser Segmente (mit Ausnahme der mit einem Sternchen * markierten) wurden als Segmentvorlagen in den Segment-Builder migriert. Darüber hinaus wurden einige neue Segmente hinzugefügt.

Vorhandene Berichte, auf die diese Segmente angewendet werden, funktionieren weiterhin fehlerfrei.

+++

+++ **Was geschieht mit Admin-Segmenten (auch bekannt als „globale“ Segmente)?**

**Admin**-Segmente werden in die neue Segmentoberfläche migriert und werden dort als für alle freigegebene Segmente angezeigt.

Der Eigentümer dieser Segmente wird mit dem ältesten Konto in der Liste der Admin-Benutzer in der Organisation als Admin angelegt. Es können jedoch alle Administratoren diese Segmente löschen, bearbeiten und teilen.

Die Segmentverwaltungsoberfläche der Admin Console, über die Administratoren diese globalen Segmente erstellen und verwalten konnten, gibt es nicht mehr. Administratoren sollten jetzt den neuen Segmentaufbau verwenden, um Segmente zu erstellen und für geeignete Gruppen, für alle oder für einzelne Personen freizugeben.

Vorhandene Segmente, die Logik verwenden, die wie in diesem Dokument beschrieben geändert wurde, funktionieren weiterhin fehlerfrei, müssen jedoch aktualisiert werden, damit sie erneut gespeichert werden können. Wenn Sie z. B. ein vorhandenes Segment haben, in dem „US-Bundesstaaten“ „New York“ enthalten, funktioniert es weiterhin fehlerfrei. Wenn Sie das Segment jedoch das nächste Mal bearbeiten, müssen Sie es im Hinblick auf die Verwendung des Aufzählungstyps mit einer Gleich-Bedingung aktualisieren.

+++

### Tipps zur Migration

Folgende Tipps helfen Ihnen bei der Migration allgemeiner Dimensionen:

* Geo-Stadt/Region/Land – Suche nach und Auswahl bestimmter Städte, Regionen oder Länder, anstelle einer teilweisen Übereinstimmung.
* Browser – benutzen Sie die Browsertypen-Dimension, um alle Browser eines Typs zu erhalten, z. B. Google Chrome.
* Betriebssysteme – benutzen Sie die Betriebssystemtypen-Dimensionen, um alle Betriebssysteme eines Typs zu erhalten, z. B. Microsoft Windows.

* [Neue und umbenannte Dimensionen](/help/components/segmentation/seg-transition.md#section_73CF121B64A24DEF8E6499F3167BF742)
* [Änderungen an „Enthält“](/help/components/segmentation/seg-transition.md#section_1A9EDEE5CBC44B5AA6262560052ABE77)
* [Änderungen an „Weniger als“ und „Mehr als“](/help/components/segmentation/seg-transition.md#section_84A8AAD0344148AD9F9211D3EB271903)

## Neue und umbenannte Dimensionen {#renamed}

Die folgende Tabelle enthält eine Liste mit Dimensionen, die im Segmentaufbau umbenannt wurden.

| Neuer Dimensionsname | Vorheriger Name | Hinweise |
|--- |--- |--- |
| Betriebssystemtypen | Neu | Hinzugefügt im Frühling 2015. |
| Browser-Breite – zusammengefasst | Browser-Breite | Diese Dimension ist mit allen Benutzeroberflächen kompatibel und wird in eine Liste aufgezählter Bereiche, anstelle bestimmter Ganzzahlwerte unterteilt. Wenn Sie bestimmte Werte segmentieren müssen, benutzen Sie die granulare Version dieser Dimension in einem Data Warehouse-Segment. |
| Browser-Höhe – zusammengefasst | Browser-Höhe | Diese Dimension ist mit allen Benutzeroberflächen kompatibel und wird in eine Liste aufgezählter Bereiche, anstelle bestimmter Ganzzahlwerte unterteilt. Wenn Sie bestimmte Werte segmentieren müssen, benutzen Sie die granulare Version dieser Dimension in einem Data Warehouse-Segment. |
| Browserbreite – Granular | Browser-Breite | Diese Dimension wurde umbenannt und ist jetzt nur mit Data Warehouse kompatibel. Wenn Sie Segmente definieren wollen, die mit allen Benutzeroberflächen kompatibel sind, benutzen Sie den Aufzählungstyp „Browserbreite – Zusammengefasst“. |
| Browserhöhe – Granular | Browser-Höhe | Diese Dimension wurde umbenannt und ist jetzt nur mit Data Warehouse kompatibel. Wenn Sie Segmente definieren wollen, die mit allen Benutzeroberflächen kompatibel sind, benutzen Sie den Aufzählungstyp „Browserhöhe – Zusammengefasst“. |
| Cookie-Unterstützung | Cookies | – |
| Farbtiefe | Bildschirmfarbtiefe | – |
| – | „App - *“ | Die „App -“-Präfixe wurden aus einigen Dimensionstypen entfernt. Da mobile App-Daten in der Regel in einer Report Suite erfasst werden, die keine Webdaten enthält, waren diese Präfixe nicht erforderlich. |
| Ursprüngliche Entrypage | Ursprüngliche Einstiegsseite | – |
| Java aktiviert | Java | – |
| Maximale mobile Browser-URL-Länge | Länge der mobilen Browser-URL | – |
| Mobilgerät – Mail-Design | Mobile Design-Mail-Unterstützung | – |
| Mobilgerät | Mobilgerätname | – |
| Maximale mobile Lesezeichenlänge | Mobil Max. Lesezeichen URL-Länge | – |
| Maximale mobile E-Mail-Länge | Mobil Max. Mail URL-Länge | – |
| Mobiles Betriebssystem (Veraltet) | Mobilbetriebssystem | Benutzen Sie die Betriebssystem-Dimension und wenden Sie stattdessen Besuche von Mobilgerätesegmenten an. |
| Mobiles PTT | Mobile PTT | – |
| Umfrageansichten | Umfrageansichten insgesamt | – |
| Umfrageantworten | Umfrageantworten insgesamt | – |
| Besuchstiefe | Path Length | – |
| Postleitzahl | Postleitzahl | – |

{style=&quot;table-layout:auto&quot;}

## Änderungen an auf Zeichenketten basierenden Dimensionen, die bekannte Werte besitzen {#string-based-dims}

Auf Zeichenketten basierende Dimensionen, die einen bekannten Satz Werte besitzen, wurden in Aufzählungstypen geändert. Wenn Sie mit diesen Dimensionen ein Segment erstellen, wird die Liste mit allen bekannten Werten vorbelegt und „Gleich“ wird als einziger Operator unterstützt. So können Sie die genauen Werte, nach denen Sie suchen, schnell segmentieren, ohne nicht beabsichtigte Werte auszuwählen, die bei einer weniger restriktiven Übereinstimmung auftreten.

Folgende Dimensionen wurden in Aufzählungslisten geändert:

| Mobilgerätehersteller | Mobile E-Mail-Länge | Farbtiefe |
|---|---|---|
| Mobilgerät – Bildschirmgröße | Mobilgerätenummer | Bildschirmauflösung |
| Mobilgerät – Bildschirmhöhe | Gebührenpflichtige Suche | Plugin |
| Mobilgerät – Cookie-Unterstützung | Mobilgerät – Mail-Design | Betriebssystem |
| Mobilgerät – Bildunterstützung | Mobile Informationsdienste | Referrer-Typ |
| Mobilgerät – Farbtiefe | Mobilgerätetyp | Suchmaschine |
| Mobilgerät – Audio-Unterstützung | Browser-Typ | state |
| Mobilgerät – Video-Unterstützung | browser | Geo-Land |
| Mobil-DRM | Verbindungstyp | Geo-Region |
| Mobile Netzprotokolle | Mobilnetzbetreiber | Geo-Stadt |
| Mobilbetriebssystem | Cookie | Geo-DMA |
| Mobile Java-VM | Kundenloyalität | Persistentes Cookie |
| Mobile Lesezeichenlänge | Java aktiviert | Paid Search |
| Mobil URL-Länge | Sprache |  |

## Änderungen an auf Ganzzahlen basierenden Dimensionen, die bekannte Werte besitzen {#integer-based-dims}

Auf Ganzzahlen basierende Dimensionen (wie die Browserbreite) mit einem bekannten Satz Werten werden in Aufzählungsbereiche aufgeteilt, sodass Sie schnell Segmente für einen bestimmten Bereich definieren können. Diese Aufzählungslisten erhalten nach dem Namen der Dimension den Zusatz „– Zusammengefasst“. Der folgende Bildschirm zeigt, wie diese Dimensionen mit der früheren und der neuen Segmentaufbauoberfläche segmentiert werden:

![](assets/seg_browser_dimension.png)

Die Operatoren „kleiner als“, „größer als“ und vergleichbare Operatoren sind jetzt nur noch mit Data Warehouse-Segmenten kompatibel. Segmente, die mit allen Berichtsoberflächen kompatibel sein sollen, müssen die „Zusammengefasst“-Version der Metrik mit dem Operator „Gleich“ verwenden.
