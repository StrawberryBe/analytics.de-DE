---
title: Echtzeitberichte in Adobe Analytics
description: Erfahren Sie, wie Sie Echtzeitberichte in Adobe Analytics abrufen, die auf Benutzer ausgerichtet sind, die mit Google Analytics besser vertraut sind.
translation-type: tm+mt
source-git-commit: 3ce18f3f222286aed08c81dd2c958dab7e443df3

---


# Echtzeitberichte

Echtzeitberichte zeigen, was gerade auf Ihrer Site geschieht. Diese Berichtstypen sind besonders wertvoll, um die sofortigen Ergebnisse von Aktualisierungen Ihrer Site zu sehen. Ein Unternehmen, das am Black Friday einen Verkauf durchführt, kann beispielsweise den Traffic zu bestimmten Seiten messen und festlegen, welche Verkäufe je nach Leistung in diesem Moment vorrangig behandelt werden sollen.

![Echtzeitbericht](/help/technotes/ga-to-aa/assets/realtime.png)

Echtzeitberichte sind eine der wenigen Funktionen, die noch nicht in Analysis Workspace eingeführt wurden. Verwenden Sie Reports &amp; Analysen, um diese Daten abzurufen. Sie erfordern eine einfache Konfiguration, um mit der Datenerfassung zu beginnen.

So rufen Sie die Seite zur Konfiguration von Echtzeitberichten auf (Administratorberechtigungen erforderlich):

1. Klicken Sie in der Kopfzeilennavigation von Adobe Analytics auf [!UICONTROL Berichte] .
2. Klicken Sie im linken Menü auf *[!UICONTROL Site-Metriken]* &gt; *[!UICONTROL Echtzeit]*.
3. Wenn die Report Suite noch nicht in Echtzeit aktiviert ist, wird eine Meldung mit einem Link zur Konfiguration der Report Suite angezeigt. Wenn die Report Suite in Echtzeit aktiviert ist, klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren] .

Adobe ermöglicht bis zu drei Echtzeitberichte, Daten gleichzeitig zu erfassen. Jede muss konfiguriert werden, bevor sie mit der Datenerfassung in Echtzeit beginnen.

![Konfiguration von Echtzeitberichten](/help/technotes/ga-to-aa/assets/realtime_config.png)

## Positionen in Echtzeit

Die Positionen in Echtzeit zeigen Ihnen, wo sich Besucher während des Besuchs Ihrer Site im aktuellen Moment befinden. So konfigurieren Sie einen Ihrer drei Echtzeitberichte, um Standortdaten anzuzeigen:

1. Klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren] .
2. Unter einem der Zeitfenster für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht; z. B. "Speicherorte".
   * Instanzen werden normalerweise als Metrik verwendet. Benutzer/Individuelle Besucher stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Bei der primären Dimension wird in der Regel GeoSegmentation Country verwendet. GeoSegmentation Region, GeoSegmentation US DMA und GeoSegmentation City sind ebenfalls verfügbar.
   * Verwenden Sie für die beiden sekundären Dimensionen die bevorzugten zusätzlichen Daten, die Sie für diesen Traffic sehen möchten. Sekundäre Dimensionen müssen nicht spezifisch für den Ort sein.
3. Click [!UICONTROL Save and View Report].

## Echtzeit-Traffic-Quellen

Echtzeit-Traffic-Quellen geben an, woher Besucher während des Besuchs Ihrer Site im aktuellen Moment kamen. So konfigurieren Sie einen Ihrer drei Echtzeitberichte, um Daten zu Traffic-Quellen anzuzeigen:

1. Klicken Sie neben dem Titel des Echtzeitberichts auf "Konfigurieren".
2. Unter einem der Zeitfenster für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht; zum Beispiel "Traffic-Quellen".
   * Instanzen werden normalerweise als Metrik verwendet. Benutzer/Individuelle Besucher stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Bei primären Dimensionen wird in der Regel verweisende Domäne verwendet. Suchmaschine und Suchbegriff sind ebenfalls verfügbar.
   * Verwenden Sie für die beiden sekundären Dimensionen die bevorzugten zusätzlichen Daten, die Sie für diesen Traffic sehen möchten. Sekundäre Dimensionen müssen nicht spezifisch für Traffic-Quellen sein.
3. Click [!UICONTROL Save and View Report].

## Inhalt in Echtzeit

Echtzeit-Inhalte zeigen Ihnen an, welche Seiten Ihre Besucher derzeit anzeigen. So konfigurieren Sie einen Ihrer drei Echtzeitberichte, um Inhaltsdaten anzuzeigen:

1. Klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren] .
2. Unter einem der Zeitfenster für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht; zum Beispiel "Inhalt".
   * Instanzen werden normalerweise als Metrik verwendet. Benutzer/Individuelle Besucher stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Bei der primären Dimension wird in der Regel Seite verwendet. Site-Abschnitt und Server sind auch verfügbar, wenn Ihre Implementierung diese Variablen definiert.
   * Verwenden Sie für die beiden sekundären Dimensionen die bevorzugten zusätzlichen Daten, die Sie für diesen Traffic sehen möchten. Sekundäre Dimensionen müssen nicht inhaltlich spezifisch sein.
3. Click [!UICONTROL Save and View Report].

## Echtzeit-Ereignisse

Echtzeit-Ereignisse zeigen Ihnen, welche Ereignisse auf Ihrer Site am häufigsten auftreten. In Google Analytics erfasst ein Ereignis, wie oft eine bestimmte Aktion (im Allgemeinen eine Aktion, die nicht mit einer Seitenansicht in Zusammenhang steht) aufgetreten ist. GA-Ereignisse werden mit einer Kategorie, einer Bezeichnung und einer Aktion gesendet. In Adobe Analytics sind benutzerspezifische Ereignisse Metriken, denen in der Admin-Konsole benutzerfreundliche Namen zugewiesen werden und die neben jeder Dimension analysiert werden können. Wenn Sie in Adobe Analytics nach einer Dimension suchen, die Google Analytics-Ereignissen ähnlich ist, sollten Sie die Dimension "Benutzerspezifischer Link"anwenden. Diese Dimension wird häufig als Sammelbegriff für Daten verwendet, die nicht mit Seitenansichten in Zusammenhang stehen (zusätzlich zu Ausstiegslinks - für Ausstiege - und Downloadlinks - für Downloads).

> [!NOTE] Bei Verwendung benutzerspezifischer Ereignisse in Echtzeitberichten muss der Dimensionswert im selben Treffer wie das benutzerspezifische Ereignis definiert werden. Wenn Sie beispielsweise ein benutzerdefiniertes Ereignis "Registrierungen"für die Dimension "Verweisende Domäne"anzeigen, werden ohne zusätzliche Implementierung keine Daten zurückgegeben. Da die verweisende Domäne nur beim ersten Treffer angezeigt wird und ein benutzerspezifisches Ereignis normalerweise später während des Besuchs auftritt, können die Daten nicht in Echtzeitberichten verknüpft werden. Diese Daten stehen in Analysis Workspace mit einer standardmäßigen Verarbeitungslatenz von 30-90 Minuten zur Verfügung.

## Konvertierungen in Echtzeit

Echtzeit-Konvertierungen stellen Daten zwischen Plattformen unterschiedlich dar. Ziele in Google Analytics sind mit Metriken und Erfolgsereignissen in Adobe Analytics vergleichbar. Sie können die meisten Metriken in Adobe Analytics (sowohl benutzerspezifische Metriken wie Erfolgsereignisse als auch Standardmetriken wie Umsatz) in Echtzeitberichten verwenden. Ähnlich wie Google Analytics können Sie auch Dimensionen wie Produktname, Rückverfolgungscode und Kampagnenleistung in Echtzeitberichten anwenden.

1. Klicken Sie neben dem Titel des Echtzeitberichts auf [!UICONTROL Konfigurieren] .
2. Unter einem der Zeitfenster für Echtzeitberichte:
   * Benennen Sie Ihren Echtzeitbericht; zum Beispiel "Konversionen".
   * Instanzen werden normalerweise als Metrik verwendet. Benutzer/Individuelle Besucher stehen derzeit in Echtzeitberichten nicht zur Verfügung.
   * Bei der primären Dimension wird in der Regel Trackingcode verwendet. Die Dimension "Produkte"ist auch verfügbar, wenn Ihre Implementierung sie verwendet.
   * Verwenden Sie für die beiden sekundären Dimensionen die bevorzugten zusätzlichen Daten, die Sie für diesen Traffic sehen möchten. Sekundäre Dimensionen müssen nicht spezifisch für Konversionen sein.
3. Click [!UICONTROL Save and View Report].

> [!NOTE] Wenn Sie Ereignisse außerhalb von Instanzen verwenden, z. B. Bestellungen, stellen Sie sicher, dass Ihre Implementierung die Dimension und das Ereignis für denselben Treffer definiert. Wenn Dimensionen und Ereignisse bei demselben Treffer nicht ausgelöst werden, stehen diese Daten in Analysis Workspace mit einer standardmäßigen Verarbeitungslatenz (in der Regel 30-90 Minuten) zur Verfügung.
