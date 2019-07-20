---
description: Einstellungen, die definieren, wie alle Berichte angezeigt werden, und Informationen, die die Standardmenüoptionen an ihre Position im vereinfachten Menü anpassen.
seo-description: Einstellungen, die definieren, wie alle Berichte angezeigt werden, und Informationen, die die Standardmenüoptionen an ihre Position im vereinfachten Menü anpassen.
seo-title: Berichtsanzeigeeinstellungen und Navigation
solution: Analytics
title: Berichtsanzeigeeinstellungen und Navigation
topic: Berichte,Reports and Analytics
uuid: e 7 e 771 ce-a 1 cf -4714-b 400-9571805 ceeac
translation-type: tm+mt
source-git-commit: 612cbb694f16b5b4fcbf2d9cae55bc52103cc0b9

---


# Berichtsanzeigeeinstellungen und Navigation

Einstellungen, die definieren, wie alle Berichte angezeigt werden, und Informationen, die die Standardmenüoptionen ihrem Standort im vereinfachten Menü zuordnen.

## Report display settings and navigation {#concept_09832A2CA0FF4982B1AA37C1B635220B}

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Komponenten]** &gt; **[!UICONTROL Berichtseinstellungen]**

<!--Meike, I replaced this table with one from https://marketing.adobe.com/resources/help/en_US/sc/user/report_settings.html -bob -->

| Element | Beschreibung |
|--- |--- |
| **Allgemeine Einstellungen** |  |
| Einschließlich betreffenden Metrikabschnitt  | Betreffende Metriken sind eng mit dem aktuell angezeigten Bericht verbunden (beispielsweise die obersten 5 Seiten im Bericht „Seitenansichten“). |
| Internet-Durchschnitt im Detailabschnitt anzeigen | Drückt den Durchschnittswert einer bestimmten Statistik aus, der aus Tausenden von kommerziellen Websites ermittelt wurde. Wenn diese Option aktiviert ist, wird dieser Abschnitt als getrennte Spalte in den Abschnitten Berichtszusammenfassung und Berichtsdetails angezeigt. Diese Funktion wird nur von den Traffic-Berichten in der Technologiegruppe sowie den Suchmaschinen-, Sprachen- und Domänenberichten verwendet. |
| Standardmenüstruktur von Adobe anzeigen | Ignoriert alle Einstellungen in den Admin Tools, mit denen Administratoren die Berichtmenüs auf Benutzerwunsch anpassen, und stellt das Berichtmenü wieder mit den ursprünglichen Einstellungen her. |
| Spaltenbreite bei Berichtanzeige forcieren | Forciert die Berichtspaltenbreite auf ein ansprechendes Einheitsmaß. Diese Einstellung ist nützlich, wenn mehr als drei Metriken angezeigt werden. |
| **Diagramme** |  |
| Wochenenden im Trenddiagramm hervorheben | Hebt Wochenenddaten senkrecht in Trendberichten hervor. Trendberichte lassen sich einfacher auswerten, wenn die Wochenenden gekennzeichnet sind. |
| Einschließlich Vorschau in Diagramm und Zusammenfassung | Schätzt, wie oft eine bestimmte Statistik in Zukunft auftritt. Bei Aktivierung erscheint die Vorschau im Abschnitt „Berichtzusammenfassung“. |
| Kalenderereignisse in Berichte einbeziehen | Verfolgt die Seiten-Performance in Bezug auf bestimmte Ereignisse. Bei aktivierter Option erscheinen diese Ereignisse in Ihren Berichten. |
| Flash-Diagramm verwenden | Aktiviert Flash-Diagramme in Ihren Berichten. Flash-Diagramme liefern schärfere, interaktivere Bilder; die Bilder können jedoch nicht so mühelos kopiert oder gespeichert werden. Wenn Sie Bilder schnell kopieren und speichern möchten, deaktivieren Sie diese Option (Bilder sind im .gif-Format). Wenn diese Option nicht markiert ist, erscheint die Schaltfläche „Diagramm kopieren“ nicht in der Berichtsymbolleiste. |
| Daten von „Alle anderen“ in ausgewählten Diagrammen anzeigen | Zeigt alle weiteren Daten, die nicht zu den Top-5 gehören, als Einzelobjekt an. (Balkendiagramme zeigen die Top-5 Webseiten oder andere Daten aus Ihrem Bericht an.) |
| Daten von „Keine“, „Nicht angegeben“ und „Eingegeben/mit Lesezeichen versehen“ in Berichtsdiagrammen anzeigen | Zeigt Metriken, bei denen keine Werte zu Gutschriften für die angegebenen Metriken führten. |
| Wortgrafiken in Rangberichten einblenden  | Zeigt eine Wortgrafik im Gesamtsummenfeld von Rangberichten an. Hiermit erhalten Sie einen schnellen Überblick über den Gesamttrend, ohne einen separaten Bericht zu erzeugen. |
| **Beschleunigung** |  |
| Report-Beschleuniger aktivieren, um Berichte schneller anzuzeigen | Aktiviert den Berichtbeschleuniger, der einen zeitbasierten Algorithmus verwendet, um kürzlich angeforderte Berichte zwischenzuspeichern und nur die mosthäufig auftretenden eindeutigen Elemente zu untersuchen, was zu einer schnelleren Auslieferung von Berichten führt. Wenn die angeforderten Berichte für 15 Minuten im Cache abgelegt werden, kann der Report-Beschleuniger diese Berichte für nachfolgende Anfragen praktisch umgehend abrufen. Diese Einstellung ist nützlich, wenn Sie vorwärts und rückwärts browsen, Berichte ausdrucken oder für den häufigen Zugriff auf dieselben Berichte. Bei der Deaktivierung dieser Option werden Berichte bei jeder Anforderung vom System neu erstellt. |
| Aktivieren des Dashboard-Beschleunigers und Anzeigen der verfügbaren Cache-Versionen | Aktiviert den Dashboard-Beschleuniger, der eine Version Ihres Dashboards für die spätere Anzeige im Cache speichert. Durch die 24-Stunden-Cache-Speicherung Ihres Dashboards kann der Dashboard-Beschleuniger diese Ansicht umgehend wiederherstellen, da die intensive Datenbankabfrage und -verarbeitung bereits erfolgt sind. Wenn die im Cache verfügbare Version über 24 Stunden alt ist, wird ein neues Dashboard und eine neue Version im Cache erstellt. Genauso wird eine neue Version im Cache erstellt, wenn Sie das Dashboard (oder ein Reportlet, das im Dashboard angezeigt wird) aktualisieren. Der Cache ist benutzerbasierend. Andere Benutzer, die ein freigegebenes Dashboard anzeigen, sehen eine Version, die auf ihrer eigenen Nutzung des Dashboard-Beschleunigers und der Aktualisierung des Dashboards basiert. |
| Netzwerkbeschleunigung für bessere Berichterstellung aktivieren | Beschleunigt durch Pfadoptimierung zwischen der Adobe-Infrastruktur und Ihrer Umgebung die Auslieferung von Daten an Ihren Standort. |
| Regionale Beschleunigung für ein schnelleres Benutzererlebnis in China aktivieren | Der Regional Accelerator verwendet regionsspezifische beschleunigte Domänen, um ein schnelleres Benutzererlebnis innerhalb einer bestimmten Region zu ermöglichen. Derzeit wird die regionale Beschleunigung nur für China unterstützt. Die Aktivierung dieser Funktion durch Benutzer, die sich nicht in China befinden, führt zu einer langsameren Benutzererfahrung. Nach Aktivierung der regionalen Beschleunigung müssen Sie sich erneut anmelden, damit die Einstellung wirksam wird. Wenn Sie den Regional Accelerator deaktivieren möchten, deaktivieren Sie dieses Kontrollkästchen. |
| **Sprache/Währung/Kodierung** |  |
| Tausendertrennzeichen | Wählen Sie ein Trennzeichen für jede/n/s Tausende (Dezimalzeichen oder Komma). Viele Länder verwenden einen Punkt, um die Tausenderzahlen zu trennen. (Dieses Trennzeichen wird auf alle Zahlen im System angewendet, nicht nur auf die Währung.) |
| Standardwährung der Report Suite verwenden | Gibt an, ob die Standardwährung der Report Suite verwendet werden soll. |
| Währung | Die Währung, in die Sie Ihre Daten umrechnen möchten. Wenn bei dieser Einstellung ein Wert ausgewählt wird, sind die in der Datenbank gespeicherten Daten nicht betroffen, werden aber als konvertierter Wert basierend auf dem aktuellen Tageswechselkurs angezeigt. Wenn diese Währungsoptionen nicht konfiguriert (auf Standard eingestellt) werden, findet keine Währungskonversion statt und alle Werte werden in US-Dollar (USD) gespeichert und angezeigt. Wenden Sie sich an Ihren Kundenbetreuer, um die Währung bei Datenverarbeitung (d. h. vor Ansicht) umzurechnen.  |
| Kodierung des terminierten Berichts | Shift-JIS für japanische Zeichenkodierung. Verwenden Sie EUC-JP für Extended Unix Code, hauptsächlich für Japanisch, Koreanisch und vereinfachtes Chinesisch. |
| CSV-Trennzeichen | Das Zeichen, das Sie zum Trennen für CSV-Werte verwenden möchten. |

## Navigationsmenü {#concept_1525EE52F8094535B4240F03B70DD75D}

<!-- 

nav_menu.xml

 -->

Wenn Sie an das Standardmenü gewöhnt sind, können Sie die Menüoptionen im vereinfachten Menü anhand der folgenden Tabelle leichter finden.

| Position im Standardmenü | Position im vereinfachten Menü |
|---|---|
| **Sitemetriken** |  |  |
|  | Site-Übersicht | Metriken &gt; Site-Übersicht |
|  | Schlüsselmetriken | Metriken &gt; Schlüsselmetriken |
|  | Seitenansichten | Metriken &gt; Seitenansichten |
|  | Besuche | Metriken &gt; Besuche |
|  | Besucher | Metriken &gt; Besucher |
|  | Zeit pro Besuch | Metriken &gt; Zeit pro Besuch |
|  | Zeit vor Ereignis | Konversion &gt; Zeit vor Ereignis |
|  | Einkäufe | Metriken &gt; Einkäufe |
|  | Warenkorb | Metriken &gt; Warenkorb |
|  | Benutzerspezifische Ereignisse | Metriken &gt; Benutzerspezifische Ereignisse |
|  | Bots | Zielgruppe &gt; Bots |
|  | Anomalieerkennung | Metriken &gt; Anomalieerkennung |
|  | Echtzeit | Metriken &gt; Echtzeit |
| **Site-Content** |  |  |
|  | Seiten | Inhalt &gt; Seiten |
|  | Sitebereiche | Inhalt &gt; Sitebereiche |
|  | Server | Inhalt &gt; Server |
|  | Links | Navigation &gt; Benutzerspezifische Links; Navigation &gt; Exitlinks; Navigation &gt; ClickMap; Navigation &gt; Dateidownloads |
|  | Seiten nicht gefunden | Navigation &gt; Seiten nicht gefunden |
| **Mobil** |  |  |
|  | Geräte | Zielgruppe &gt; Mobil &gt; Geräte |
|  | Gerätetyp | Zielgruppe &gt; Mobil &gt; Gerätetyp |
|  | Hersteller | Zielgruppe &gt; Mobil &gt; Hersteller |
|  | Bildschirmgröße | Zielgruppe &gt; Mobil &gt; Bildschirmgröße |
|  | Bildschirmhöhe | Zielgruppe &gt; Mobil &gt; Bildschirmhöhe |
|  | Bildschirmbreite | Zielgruppe &gt; Mobil &gt; Bildschirmbreite |
|  | Cookie-Unterstützung | Zielgruppe &gt; Mobil &gt; Cookie-Unterstützung |
|  | Bildunterstützung | Zielgruppe &gt; Mobil &gt; Bildunterstützung |
|  | Farbtiefe | Zielgruppe &gt; Mobil &gt; Farbtiefe |
|  | Audiounterstützung | Zielgruppe &gt; Mobil &gt; Audio-Unterstützung |
|  | Video-Unterstützung | Zielgruppe &gt; Mobil &gt; Video-Unterstützung |
|  | Betriebssystem | Zielgruppe &gt; Mobil &gt; Betriebssystem |
| **Pfade** |  |  |
|  | Seiten | Navigation &gt; Pfade &gt; Seiten |
|  | Interne Suchbegriffe | Navigation &gt; Pfade &gt; Interne Suchbegriffe |
| **Traffic-Quellen** |  |  |
|  | Keyword – Alle | Traffic-Quellen &gt; Keyword – Alle |
|  | Keyword – Bezahlt | Traffic-Quellen &gt; Keyword – Bezahlt |
|  | Keyword – Natürlich | Traffic-Quellen &gt; Keyword – Natürlich |
|  | Suchmaschinen – Alle | Traffic-Quellen &gt; Suchmaschinen – Alle |
|  | Suchmaschinen – Gebührenpflichtig | Traffic-Quellen &gt; Suchmaschinen – Gebührenpflichtig |
|  | Suchmaschinen – Kostenlos | Traffic-Quellen &gt; Suchmaschinen – Kostenlos |
|  | Rangansicht aller Suchseiten | Traffic-Quellen &gt; Rangansicht aller Suchseiten |
|  | Verweisende Domänen | Traffic-Quellen &gt; Verweisende Domänen |
|  | Ursprünglich verweisende Domänen | Traffic-Quellen &gt; Ursprünglich verweisende Domänen |
|  | Verweisende Stellen | Traffic-Quellen &gt; Verweisende Stellen |
|  | Typen der verweisenden Stellen | Traffic-Quellen &gt; Typen der verweisenden Stellen |
| **Kampagnen** |  |  |
|  | Kampagnenkonversionstrichter | Traffic-Quellen &gt; Kampagnen &gt; Kampagnenkonversionstrichter |
|  | Trackingcode | Traffic-Quellen &gt; Kampagnen &gt; Trackingcode |
| **Produkte** |  |  |
|  | Produktkonversionstrichter | Konversion &gt; Produkte &gt; Produktkonversionstrichter |
|  | Produkte | Konversion &gt; Produkte &gt; Produkte |
|  | Cross-Sell | Konversion &gt; Produkte &gt; Cross-Sell |
|  | Kategorien | Konversion &gt; Produkte &gt; Kategorien |
| **Besuchertreue** |  |  |
|  | Rückkehrhäufigkeit | Zielgruppe &gt; Besuchertreue &gt; Rückkehrhäufigkeit |
|  | Rückkehrende Besucher | Zielgruppe &gt; Besuchertreue &gt; Rückkehrende Besucher |
|  | Rückkehrende Besucher pro Tag | Zielgruppe &gt; Besuchertreue &gt; Rückkehrende Besucher pro Tag |
|  | Besuchsnummer | Zielgruppe &gt; Besuchertreue &gt; Besuchsnummer |
|  | Verkaufszyklus | Zielgruppe &gt; Besuchertreue &gt; Verkaufszyklus |
| **Besucherprofil** |  |  |
|  | GeoSegmentation | Zielgruppe &gt; Besucherprofil &gt; GeoSegmentation |
|  | Sprachen | Zielgruppe &gt; Besucherprofil &gt; Sprachen |
|  | Zeitzonen | Zielgruppe &gt; Besucherprofil &gt; Zeitzonen |
|  | Domänen | Zielgruppe &gt; Besucherprofil &gt; Domänen |
|  | Domänen auf oberster Ebene | Zielgruppe &gt; Besucherprofil &gt; Domänen auf oberster Ebene |
|  | Technologie | Zielgruppe &gt; Besucherprofil &gt; Technologie |
|  | Bundesstaat des Besuchers | Zielgruppe &gt; Besucherprofil &gt; Bundesstaat des Besuchers |
|  | PLZ/Postleitzahlen des Besuchers | Zielgruppe &gt; Besucherprofil &gt; PLZ/Postleitzahlen des Besuchers |
| **Benutzerspezifische Konversion** |  |  |
|  | Benutzerspez. Konversion 1-10 | Konversion &gt; Benutzerspezifische Konversion &gt; Benutzerspez. Konversion 1-10 |
|  | Benutzerspez. Konversion 11-20 | Konversion &gt; Benutzerspezifische Konversion &gt; Benutzerspez. Konversion 11-20 |
| **Benutzerspez. Traffic ** |  |  |
|  | Benutzerspez. Traffic 1-10 | Inhalt &gt; Benutzerspezifischer Traffic &gt; Benutzerspez. Traffic 1-10 |
| **Test&amp;Target ** |  | Konversion &gt; Test&amp;Target |
| **Survey** |  | Zielgruppe &gt; Survey |
| **Marketing-Kanäle** |  |  |
|  | Kanalübersichtsbericht | Traffic-Quellen &gt; Marketing-Kanäle &gt; Kanalübersichtsbericht |
|  | Erstkontakt Kanal | Traffic-Quellen &gt; Marketing-Kanäle &gt; Erstkontakt Kanal |
|  | Erstkontakt Kanaldetail | Traffic-Quellen &gt; Marketing-Kanäle &gt; Erstkontakt Kanaldetail |
|  | Letztkontakt Kanal | Traffic-Quellen &gt; Marketing-Kanäle &gt; Letztkontakt Kanal |
|  | Letztkontakt Kanaldetail | Traffic-Quellen &gt; Marketing-Kanäle &gt; Letztkontakt Kanaldetail |
| **Mobile Anwendung** |  |  |
|  | Übersicht Mobile Anwendung | Inhalt &gt; Mobile Anwendung &gt; Übersicht Mobile Anwendung |
|  | Lebenszyklus-Berichte | Inhalt &gt; Mobile Anwendung &gt; Lebenszyklus-Berichte |
| **Benutzerspezifische Berichte ** |  |  |
|  | Benutzerspezifische Berichte werden nur angezeigt, wenn Sie welche eingerichtet haben. | Benutzerspezifische Berichte |
|  |  |  |

