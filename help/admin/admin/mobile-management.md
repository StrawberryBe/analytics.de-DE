---
description: Durch die Aktivierung der App-Verwaltung aktivieren Sie die mobilen Lösungsvariablen, die Lebenszyklusmetriken und andere Metriken aus Mobile Apps.
title: App-Verwaltung
feature: Admin Tools
exl-id: ec19695a-2961-45e4-bf44-434f0ff9e3c9
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 100%

---

# App-Verwaltung

Durch die Aktivierung der App-Verwaltung aktivieren Sie die mobilen Lösungsvariablen, die Lebenszyklusmetriken und andere Metriken aus Mobile Apps.

Mithilfe dieser Integration zwischen Adobe Analytics und Mobile Services:

* können Sie Ihre KPI (Key Performance Indicator)-Daten aus Mobile Services in Adobe Analytics freigeben.
* können Sie die Standortverfolgung aktivieren.
* werden unter „Analytics > Berichte > Mobile App“ neue Berichte hinzugefügt.
* werden 25 neue Adobe Mobile-Klassifizierungen hinzugefügt.
* werden 5 neue Adobe Mobile-Metriken hinzugefügt.
* werden neue Adobe Mobile-Dimensionen hinzugefügt.
* werden Daten alle 15 Minuten mit Analytics synchronisiert

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL App-Verwaltung]** > **[!UICONTROL App-Reporting]**.

## Schritt 1. Aktivieren von Anwendungsberichten {#section_FBADF80AED2B4978A904ABB770B3B931}

Aktivieren Sie Anwendungsberichte v3.0, um die folgenden Metriken zu messen:

* **Akquise**: Verfolgen Sie Referrer-URLs für App-Download-Kampagnen.
* **Lebenszyklus**: Basisebene der Berichterstellung durch die Messung bei jedem App-Start.
* **App-Aktionen**: Berichte und Pfade basierend auf App-internen Aktionen.
* **Lebenszeitwert**: Vollziehen Sie mithilfe von App-KPIs nach, wie Benutzer mit der Zeit Werte schaffen (z. B. Käufe, Ad-Ansichten, beendete Videos, Teilen in sozialen Netzwerken und Foto-Uploads).
* **Zeitgesteuerte Ereignisse**: Messen Sie die Zeit (in der App und insgesamt) zwischen wichtigen App-Aktionen (z. B. Zeit bis zum ersten Einkauf).

## Schritt 2. Aktivieren von Standort-Tracking {#section_2CCBD205191C4CA3B7B71A6F11FF97EC}

Durch die Aktivierung der Standortverfolgung können Sie:

* Daten zum Breiten- und Längengrad verfolgen und entsprechende Berichte in Analysis Workspace und Mobile Services erstellen.
* spezielle Zielpunkte (POIs) in Mobile Services identifizieren, erstellen und visualisieren. Zielpunkte müssen in der mobilen SDK-Konfigurationsdatei definiert werden.
* Bluetooth-Beacons (UUID, Major-Wert, Minor-Wert und Nähe) verfolgen.

## Schritt 3. (Optional) Die alte Berichterstellung und Zuweisung für Hintergrund-Hits aktivieren/deaktivieren {#section_1708BCAA87AA4884986F7532759C5DD4}

Aktivierte Hintergrundtreffer (generierte Treffer, wenn die App im Hintergrund ist) werden als reguläre Vordergrundtreffer behandelt. Sie werden von nun an in der regulären Berichterstellung angezeigt. Dies betrifft auch die Zuweisung. Diese Konfiguration ist normalerweise nur zum Aufrechterhalten der Konsistenz mit alten Implementierungen hilfreich.

Stattdessen empfehlen wird, Hintergrund-Hits in eine [Virtual Report Suite](/help/components/vrs/vrs-about.md) aufzunehmen. Dadurch können Sie die Hits anzeigen, es gibt jedoch keine negativen Auswirkungen auf die Besuchs- und Besucherzahlen.
Mobile Klassifizierungen sind aktiviert, wenn Sie **[!UICONTROL App-Verwaltung]** > **[!UICONTROL App-Reporting]** aktivieren.

Klassifizierungen werden verwendet, um Werte in Gruppen zu kategorisieren und auf Gruppenebene zu berichten. Sie können beispielsweise alle gebührenpflichtigen Suchkampagnen in eine Kategorie wie Popmusikbegriffe kategorisieren und über den Erfolg dieser Kategorie in Bezug zu Metriken wie Instanzen (auch Clickthroughs genannt) und Konversion in Erfolgsereignisse berichten.

| Klassifizierung | Definition |
|--- |--- |
| Erster Starttermin | Datum des ersten Starts nach der Installation oder Neuinstallation.   MM/TT/JJJJ |
| App-ID | Speichert den App-Namen und die Version im folgenden Format:      `[AppName] [BundleVersion]`  Beispiel, `myapp 1.1.` |
| Launch-Nummer | Gibt an, wie oft die App gestartet bzw. aus dem Hintergrund gebracht wurde. |
| Tage seit der ersten Verwendung | Anzahl der Tage seit dem ersten Ausführen. |
| Tage seit der letzten Verwendung | Anzahl der Tage seit der letzten Verwendung. |
| Stunde des Tages | Uhrzeit, zu der die App gestartet wurde, im 24-Stunden-Format. Wird für die Zeitunterteilung verwendet, um Spitzennutzungszeiten zu ermitteln. |
| Wochentag | Nummer des Wochentags, an dem die App gestartet wurde. |
| Gerätename | Speichert den Gerätenamen.  Zweistellige, kommagetrennte Zeichenfolge, die das Gerät angibt. Die erste Ziffer steht üblicherweise für die Gerätegeneration, die zweite weist die Version der verschiedenen Mitglieder der Gerätefamilie aus. |
| Betriebssystemversion | Betriebssystemversion. |
| Auflösung | Breite x Höhe in Pixel. |
| Lebenszeitwert (eVar) | Erfasst durch trackLifetimeValue-Methoden. |
| Akquisequelle |  |
| Akquisemedium |  |
| Akquisebedingung |  |
| Akquiseinhalt |  |
| Akquisename |  |
| Standort (bis 10 km) | Erfasst durch trackLocation-Methoden. |
| Standort (bis 100 m) | Erfasst durch trackLocation-Methoden. |
| Standort (bis 1 m) | Erfasst durch trackLocation-Methoden. |
| Zielpunkt-Bezeichnung | Wird durch trackLocation-Methoden aufgefüllt, wenn sich das Gerät in einem definierten POI befindet. |
| Entfernung zum Zentrum des Zielpunkts | Wird durch trackLocation-Methoden aufgefüllt, wenn sich das Gerät in einem definierten POI befindet. |
| In-App-Nachrichten-ID |  |
| In-App-Online-Nachricht |  |
| Push-Abonnement |  |
| Nutzlast-ID |  |
