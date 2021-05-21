---
title: Echtzeitberichte in Adobe Analytics
description: Erfahren Sie, wie Sie Echtzeitberichte in Adobe Analytics abrufen, die auf Anwender ausgerichtet sind, die mit Google Analytics besser vertraut sind.
exl-id: 0ca27992-fff8-4bb4-8582-31fd401b23f6
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '979'
ht-degree: 100%

---

# Echtzeitberichte

Echtzeitberichte zeigen, was gerade auf Ihrer Site geschieht. Diese Berichtstypen sind besonders wertvoll, um die sofortigen Ergebnisse von Updates Ihrer Site zu sehen. Ein Unternehmen, das am Black Friday einen Verkauf durchführt, kann beispielsweise den Traffic auf bestimmten Seiten messen und festlegen, welche Verkäufe je nach Leistung in diesem Moment vorrangig behandelt werden sollen.

![Echtzeitbericht](/help/technotes/ga-to-aa/assets/realtime.png)

Echtzeitberichte sind eine der wenigen Funktionen, die noch nicht in Analysis Workspace eingeführt wurden. Verwenden Sie Reports &amp; Analytics, um diese Daten abzurufen. Sie erfordern eine einfache Konfiguration, um mit der Datenerfassung zu beginnen.

So rufen Sie die Seite zur Konfiguration von Echtzeitberichten auf (Administratorberechtigungen erforderlich):

1. Klicken Sie in der oberen Navigationsleiste von Adobe Analytics auf [!UICONTROL Berichte].
2. Klicken Sie im linken Menü auf *[!UICONTROL Site-Metriken]* > *[!UICONTROL Echtzeit]*.
3. Wenn Echtzeit in der Report Suite noch nicht aktiviert ist, wird eine Meldung mit einem Link zur Konfiguration der Report Suite angezeigt. Wenn Echtzeit in der Report Suite aktiviert ist, klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren].

Adobe ermöglicht bis zu drei Echtzeitberichte, die Daten gleichzeitig erfassen. Jede muss konfiguriert werden, bevor sie mit der Datenerfassung in Echtzeit beginnen.

![Konfiguration von Echtzeitberichten](/help/technotes/ga-to-aa/assets/realtime_config.png)

## Echtzeitstandorte

Die Echtzeitstandorte zeigen Ihnen, wo sich Besucher während des Besuchs Ihrer Site im aktuellen Moment befinden. So konfigurieren Sie einen Ihrer drei Echtzeitberichte, um Standortdaten anzuzeigen:

1. Klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren].
2. Unter einem der Slots für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht, z. B. mit „Standorte“.
   * Als Metrik wird in der Regel „Instanzen“ verwendet. „Benutzer“/„Unique Visitors“ stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Als primäre Dimension wird in der Regel „GeoSegmentation Land“ verwendet. „GeoSegmentation Region“, „GeoSegmentation U.S. DMA“ und „GeoSegmentation Stadt“ sind ebenfalls verfügbar.
   * Verwenden Sie als die beiden sekundären Dimensionen die gewünschten zusätzlichen Daten, die Sie für diesen Traffic anzeigen möchten. Sekundäre Dimensionen müssen nicht standortspezifisch sein.
3. Klicken Sie auf [!UICONTROL Speichern und Bericht anzeigen].

## Echtzeit-Traffic-Quellen

Echtzeit-Traffic-Quellen geben an, woher Besucher während des Besuchs Ihrer Site im aktuellen Moment kamen. So konfigurieren Sie einen Ihrer drei Echtzeitberichte, um Traffic-Quellen anzuzeigen:

1. Klicken Sie neben dem Titel des Echtzeitberichts auf „Konfigurieren“.
2. Unter einem der Slots für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht, z. B. mit „Traffic-Quellen“.
   * Als Metrik wird in der Regel „Instanzen“ verwendet. „Benutzer“/„Unique Visitors“ stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Als primäre Dimension wird in der Regel „Referrer-Domäne“ verwendet. „Suchmaschine“ und „Suchbegriff“ sind ebenfalls verfügbar.
   * Verwenden Sie als die beiden sekundären Dimensionen die gewünschten zusätzlichen Daten, die Sie für diesen Traffic anzeigen möchten. Sekundäre Dimensionen müssen nicht Traffic-Quellen-spezifisch sein.
3. Klicken Sie auf [!UICONTROL Speichern und Bericht anzeigen].

## Echtzeitinhalt

Echtzeitinhalt zeigt Ihnen an, welche Seiten Ihre Besucher derzeit anzeigen. So konfigurieren Sie einen Ihrer drei Echtzeitberichte, um Inhaltsdaten anzuzeigen:

1. Klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren].
2. Unter einem der Slots für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht, z. B. mit „Inhalt“.
   * Als Metrik wird in der Regel „Instanzen“ verwendet. „Benutzer“/„Unique Visitors“ stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Als primäre Dimension wird in der Regel „Seite“ verwendet. „Sitebereich“ und „Server“ sind ebenfalls verfügbar, wenn Ihre Implementierung diese Variablen definiert.
   * Verwenden Sie als die beiden sekundären Dimensionen die gewünschten zusätzlichen Daten, die Sie für diesen Traffic anzeigen möchten. Sekundäre Dimensionen müssen nicht inhaltsspezifisch sein.
3. Klicken Sie auf [!UICONTROL Speichern und Bericht anzeigen].

## Echtzeitereignisse

Echtzeitereignisse zeigen Ihnen, welche Ereignisse derzeit auf Ihrer Site am häufigsten auftreten. In Google Analytics erfasst ein Ereignis, wie oft eine bestimmte Aktion (im Allgemeinen eine Aktion, die nicht mit einer Seitenansicht in Zusammenhang steht) aufgetreten ist. GA-Ereignisse werden mit einer Kategorie, einer Bezeichnung und einer Aktion gesendet. In Adobe Analytics sind benutzerspezifische Ereignisse Metriken, denen in der Admin Console benutzerfreundliche Namen zugewiesen werden und die neben jeder Dimension analysiert werden können. Wenn Sie in Adobe Analytics nach einer Dimension suchen, die Google Analytics-Ereignissen ähnlich ist, sollten Sie die Dimension „Benutzerspezifischer Link“ anwenden. Diese Dimension wird häufig als Sammelbegriff für Daten verwendet, die nicht mit Seitenansichten in Zusammenhang stehen (zusätzlich zu Exit-Links für Ausstiehe- und Downloadlinks für Downloads).

>[!NOTE]
>
>Bei Verwendung benutzerdefinierter Ereignisse in Echtzeitberichten muss der Dimensionswert im selben Treffer wie das benutzerspezifische Ereignis definiert werden. Wenn Sie beispielsweise ein benutzerdefiniertes Ereignis „Registrierungen“ für die Dimension „Referrer-Domäne“ anzeigen, werden ohne zusätzliche Implementierung keine Daten zurückgegeben. Da die verweisende Domäne nur beim ersten Treffer angezeigt wird und ein benutzerspezifisches Ereignis normalerweise später während des Besuchs auftritt, können die Daten nicht in Echtzeitberichten verknüpft werden. Diese Daten stehen in Analysis Workspace mit einer standardmäßigen Verarbeitungslatenz von 30 bis 90 Minuten zur Verfügung.

## Echtzeitkonversionen

Echtzeitkonversionen stellen Daten zwischen Plattformen unterschiedlich dar. Zielvorhaben in Google Analytics sind mit Metriken und Erfolgsereignissen in Adobe Analytics vergleichbar. Sie können die meisten Metriken in Adobe Analytics (sowohl benutzerspezifische Metriken wie Erfolgsereignisse als auch Standardmetriken wie den Umsatz) in Echtzeitberichten verwenden. Ähnlich wie Google Analytics können Sie auch Dimensionen wie Produktname, Trackingcode und Kampagnenleistung in Echtzeitberichten anwenden.

1. Klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren].
2. Unter einem der Slots für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht, z. B. mit „Konversionen“.
   * Als Metrik wird in der Regel „Instanzen“ verwendet. „Benutzer“/„Unique Visitors“ stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Als primäre Dimension wird in der Regel „Trackingcode“ verwendet. Die Dimension „Produkte“ ist ebenfalls verfügbar, wenn Ihre Implementierung sie verwendet.
   * Verwenden Sie als die beiden sekundären Dimensionen die gewünschten zusätzlichen Daten, die Sie für diesen Traffic anzeigen möchten. Sekundäre Dimensionen müssen nicht konversionsspezifisch sein.
3. Klicken Sie auf [!UICONTROL Speichern und Bericht anzeigen].

>[!NOTE]
>
>Wenn Sie Ereignisse außerhalb von Instanzen verwenden, z. B. Bestellungen, stellen Sie sicher, dass Ihre Implementierung die Dimension und das Ereignis im selben Treffer definiert. Wenn Dimensionen und Ereignisse nicht im selben Treffer ausgelöst werden, stehen diese Daten in Analysis Workspace mit einer standardmäßigen Verarbeitungslatenz (in der Regel 30 bis 90 Minuten) zur Verfügung.
