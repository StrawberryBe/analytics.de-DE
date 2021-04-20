---
description: Einstellungen, die festlegen, wie alle Berichte angezeigt werden, und Informationen, die Ihnen helfen, Standardmenüoptionen im vereinfachten Menü zu finden.
title: Einstellungen zur Berichtsanzeige und Navigation
uuid: e7e571ce-a1cf-4714-b400-9571805ceeac
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 99%

---


# Einstellungen zur Berichtsanzeige und Navigation

Einstellungen, die festlegen, wie alle Berichte angezeigt werden, und Informationen, die Ihnen helfen, Standardmenüoptionen im vereinfachten Menü zu finden.

## Einstellungen zur Berichtsanzeige und Navigation {#concept_09832A2CA0FF4982B1AA37C1B635220B}

**[!UICONTROL Analysen]** > **[!UICONTROL Komponenten]** > **[!UICONTROL Berichtseinstellungen]**

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
| Report-Beschleuniger aktivieren, um Berichte schneller anzuzeigen | Aktiviert den Berichtbeschleuniger, der einen zeitbasierten Algorithmus einsetzt, um die zuletzt abgerufenen Berichte im Cache zu speichern und prüft nur die häufigsten Einzelelemente, was zu einer schnelleren Bereitstellung der Berichte führt. Wenn die angeforderten Berichte für 15 Minuten im Cache abgelegt werden, kann der Report-Beschleuniger diese Berichte für nachfolgende Anfragen praktisch umgehend abrufen. Diese Einstellung ist nützlich, wenn Sie vorwärts und rückwärts browsen, Berichte ausdrucken oder für den häufigen Zugriff auf dieselben Berichte. Bei der Deaktivierung dieser Option werden Berichte bei jeder Anforderung vom System neu erstellt. |
| Aktivieren des Dashboard-Beschleunigers und Anzeigen der verfügbaren Cache-Versionen | Aktiviert den Dashboard-Beschleuniger, der eine Version Ihres Dashboards für die spätere Anzeige im Cache speichert. Durch die 24-Stunden-Cache-Speicherung Ihres Dashboards kann der Dashboard-Beschleuniger diese Ansicht umgehend wiederherstellen, da die intensive Datenbankabfrage und -verarbeitung bereits erfolgt sind. Wenn die im Cache verfügbare Version über 24 Stunden alt ist, wird ein neues Dashboard und eine neue Version im Cache erstellt. Genauso wird eine neue Version im Cache erstellt, wenn Sie das Dashboard (oder ein Reportlet, das im Dashboard angezeigt wird) aktualisieren. Der Cache ist benutzerbasierend. Andere Benutzer, die ein freigegebenes Dashboard anzeigen, sehen eine Version, die auf ihrer eigenen Nutzung des Dashboard-Beschleunigers und der Aktualisierung des Dashboards basiert. |
| Netzwerkbeschleunigung für bessere Berichterstellung aktivieren | Beschleunigt durch Pfadoptimierung zwischen der Adobe-Infrastruktur und Ihrer Umgebung die Auslieferung von Daten an Ihren Standort. |
| Regionale Beschleunigung für ein schnelleres Benutzererlebnis in China aktivieren | Der Regional Accelerator verwendet regionsspezifische beschleunigte Domänen, um ein schnelleres Benutzererlebnis innerhalb einer bestimmten Region zu ermöglichen. Derzeit wird die regionale Beschleunigung nur für China unterstützt. Die Aktivierung dieser Funktion durch Benutzer, die sich nicht in China befinden, führt zu einer langsameren Benutzererfahrung. Nach Aktivierung der regionalen Beschleunigung müssen Sie sich erneut anmelden, damit die Einstellung wirksam wird. Wenn Sie den Regional Accelerator deaktivieren möchten, deaktivieren Sie dieses Kontrollkästchen. |
| **Sprache/Währung/Kodierung** |  |
| Tausendertrennzeichen | Wählen Sie ein Trennzeichen für jede Tausenderzahl (Punkt oder Komma). Viele Länder verwenden einen Punkt, um die Tausenderzahlen zu trennen. (Dieses Trennzeichen wird auf alle Zahlen im System angewendet, nicht nur auf die Währung.) |
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
|  | Site-Übersicht | Metriken > Site-Übersicht |
|  | Schlüsselmetriken | Metriken > Schlüsselmetriken |
|  | Seitenansichten | Metriken > Seitenansichten |
|  | Besuche | Metriken > Besuche |
|  | Besucher | Metriken   > Besucher |
|  | Zeit pro Besuch | Metriken > Zeit pro Besuch |
|  | Zeit vor Ereignis | Konversion > Zeit vor Ereignis |
|  | Einkäufe | Metriken > Einkäufe |
|  | Warenkorb | Metriken > Warenkorb |
|  | Benutzerspezifische Ereignisse | Metriken > Benutzerspezifische Ereignisse |
|  | Bots | Zielgruppe > Bots |
|  | Anomalieerkennung | Metriken > Anomalieerkennung |
|  | Echtzeit | Metriken > Echtzeit |
| **Site-Content** |  |  |
|  | Seiten | Inhalt > Seiten |
|  | Sitebereiche | Inhalt > Sitebereiche |
|  | Server | Inhalt > Server |
|  | Links | Navigation > Benutzerspezifische Links; Navigation > Exitlinks; Navigation > ClickMap; Navigation > Dateidownloads |
|  | Seiten nicht gefunden | Navigation > Seiten nicht gefunden |
| **Mobile** |  |  |
|  | Geräte | Zielgruppe > Mobil > Geräte |
|  | Gerätetyp | Zielgruppe > Mobil > Gerätetyp |
|  | Hersteller | Zielgruppe > Mobil > Hersteller |
|  | Bildschirmgröße | Zielgruppe > Mobil > Bildschirmgröße |
|  | Bildschirmhöhe | Zielgruppe > Mobil > Bildschirmhöhe |
|  | Bildschirmbreite | Zielgruppe > Mobil > Bildschirmbreite |
|  | Cookie-Unterstützung | Zielgruppe > Mobil > Cookie-Unterstützung |
|  | Bildunterstützung | Zielgruppe > Mobil > Bildunterstützung |
|  | Farbtiefe | Zielgruppe > Mobil > Farbtiefe |
|  | Audiounterstützung | Zielgruppe > Mobil > Audio-Unterstützung |
|  | Video-Unterstützung | Zielgruppe > Mobil > Video-Unterstützung |
|  | Betriebssystem | Zielgruppe > Mobil > Betriebssystem |
| **Pfade** |  |  |
|  | Seiten | Navigation > Pfade > Seiten |
|  | Interne Suchbegriffe | Navigation > Pfade > Interne Suchbegriffe |
| **Traffic-Quellen** |  |  |
|  | Keyword – Alle | Traffic-Quellen > Keyword – Alle |
|  | Suchbegriff – bezahlt | Traffic-Quellen > Keyword – Bezahlt |
|  | Suchbegriff – kostenlos | Traffic-Quellen > Keyword – Natürlich |
|  | Suchmaschinen – Alle | Traffic-Quellen > Suchmaschinen – Alle |
|  | Suchmaschinen – Gebührenpflichtig | Traffic-Quellen > Suchmaschinen – Gebührenpflichtig |
|  | Suchmaschinen – Kostenlos | Traffic-Quellen > Suchmaschinen – Kostenlos |
|  | Rangansicht aller Suchseiten | Traffic-Quellen > Rangansicht aller Suchseiten |
|  | Referrerdomänen | Traffic-Quellen > Verweisende Domänen |
|  | Ursprünglich Referrerdomänen | Traffic-Quellen > Ursprünglich verweisende Domänen |
|  | Verweisende Stellen | Traffic-Quellen > Verweisende Stellen |
|  | Referrertypen | Traffic-Quellen > Typen der verweisenden Stellen |
| **Kampagnen** |  |  |
|  | Kampagnenkonversionstrichter | Traffic-Quellen > Kampagnen > Kampagnenkonversionstrichter |
|  | Trackingcode | Traffic-Quellen > Kampagnen > Trackingcode |
| **Produkte** |  |  |
|  | Produktkonversionstrichter | Konversion > Produkte > Produktkonversionstrichter |
|  | Produkte | Konversion > Produkte > Produkte |
|  | Cross-Sell | Konversion > Produkte > Cross-Sell |
|  | Kategorien | Konversion > Produkte > Kategorien |
| **Besuchertreue** |  |  |
|  | Rückkehrhäufigkeit | Zielgruppe > Besuchertreue > Rückkehrhäufigkeit |
|  | Rückkehrende Besucher | Zielgruppe > Besuchertreue > Rückkehrende Besucher |
|  | Rückkehrende Besucher pro Tag | Zielgruppe > Besuchertreue > Rückkehrende Besucher pro Tag |
|  | Besuchsnummer | Zielgruppe > Besuchertreue > Besuchsnummer |
|  | Verkaufszyklus | Zielgruppe > Besuchertreue > Verkaufszyklus |
| **Besucherprofil** |  |  |
|  | GeoSegmentation | Zielgruppe > Besucherprofil > GeoSegmentation |
|  | Sprachen | Zielgruppe > Besucherprofil > Sprachen |
|  | Zeitzonen | Zielgruppe > Besucherprofil > Zeitzonen |
|  | Domänen | Zielgruppe > Besucherprofil > Domänen |
|  | Domänen auf oberster Ebene | Zielgruppe > Besucherprofil > Domänen auf oberster Ebene |
|  | Technologie | Zielgruppe > Besucherprofil > Technologie |
|  | Bundesland des Besuchers | Zielgruppe > Besucherprofil > Bundesstaat des Besuchers |
|  | Postleitzahl des Besuchers | Zielgruppe > Besucherprofil > PLZ/Postleitzahlen des Besuchers |
| **Benutzerspezifische Konversion** |  |  |
|  | Benutzerspez. Konversion 1-10 | Konversion > Benutzerspezifische Konversion > Benutzerspez. Konversion 1-10 |
|  | Benutzerspez. Konversion 11-20 | Konversion > Benutzerspezifische Konversion > Benutzerspez. Konversion 11-20 |
| **Benutzerspezifischer Traffic** |  |  |
|  | Benutzerspez. Traffic 1-10 | Inhalt > Benutzerspezifischer Traffic > Benutzerspez. Traffic 1-10 |
| **Test&amp;Target** |  | Konversion > Test&amp;Target |
| **Umfrage** |  | Zielgruppe > Survey |
| **Marketing-Kanäle** |  |  |
|  | Kanalübersichtsbericht | Traffic-Quellen > Marketing-Kanäle > Kanalübersichtsbericht |
|  | Erstkontakt-Kanal | Traffic-Quellen > Marketing-Kanäle > Erstkontakt Kanal |
|  | Erstkontakt-Kanaldetail | Traffic-Quellen > Marketing-Kanäle > Erstkontakt Kanaldetail |
|  | Letztkontakt-Kanal | Traffic-Quellen > Marketing-Kanäle > Letztkontakt Kanal |
|  | Letztkontakt-Kanaldetail | Traffic-Quellen > Marketing-Kanäle > Letztkontakt Kanaldetail |
| **Mobile App** |  |  |
|  | Übersicht Mobile Anwendung | Inhalt > Mobile Anwendung > Übersicht Mobile Anwendung |
|  | Lebenszyklus-Berichte | Inhalt > Mobile Anwendung > Lebenszyklus-Berichte |
| **Benutzerspezifische Berichte** |  |  |
|  | Benutzerspezifische Berichte werden nur angezeigt, wenn Sie welche eingerichtet haben. | Benutzerspezifische Berichte |
|  |  |  |

