---
title: Häufig verwendete Metriken im Übersetzungshandbuch für andere Plattformen
description: Verstehen Sie, wie Sie Metrikdaten für viele häufig verwendete Berichte abrufen können, indem Sie Terminologie verwenden, die für Google Analytics-Benutzer besser bekannt ist.
translation-type: tm+mt
source-git-commit: 3ce18f3f222286aed08c81dd2c958dab7e443df3

---


# Häufig verwendete Metriken im Übersetzungshandbuch für andere Plattformen

Auf anderen Plattformen wie Google Analytics verwenden viele Berichte eine gemeinsame Anzahl von Metriken. Auf dieser Seite erfahren Sie, wie Sie die in vielen Berichten verwendeten Metriken neu erstellen.

Um einer Freiformtabelle im Arbeitsbereich mehrere Metriken hinzuzufügen, ziehen Sie die Metrik aus dem Komponentenbereich neben der Metriküberschrift im Arbeitsbereich:

![Zusätzliche Metrik](/help/technotes/ga-to-aa/assets/new_metric.png)

## Akquise-Metriken

**Benutzer** sind ungefähr gleich **Unique Visitors** in Workspace. Weitere Informationen finden Sie in der Metrik " [Individuelle Besucher](/help/components/c-variables/c-metrics/metrics-unique-visitors.md) "im Komponenten-Benutzerhandbuch.

**Neue Benutzer** erhalten Sie wie folgt:

1. Ziehen Sie die Metrik " **Individuelle Besucher** "in den Arbeitsbereich.
2. Ziehen Sie das Segment " **Erstbesuche** "über die Metriküberschriften "Individuelle Besucher":

   ![Erstbesuche](../assets/first_time_visits.png)

**Sitzungen** entsprechen ungefähr den **Besuchen** im Arbeitsbereich für Analysen. Weitere Informationen finden Sie in der Metrik [Besuche](/help/components/c-variables/c-metrics/metrics-visit.md) im Komponenten-Benutzerhandbuch.

![Akquise-Metriken](../assets/acquisition_metrics.png)

## Verhaltensmetriken

**Die Absprungrate** steht in Analysis Workspace als Metrik zur Verfügung. Weitere Informationen finden Sie in der Metrik " [Absprungrate](/help/components/c-variables/c-metrics/metrics-bounce-rate.md) "im Komponenten-Benutzerhandbuch.

**Seiten/Sitzung** ist eine berechnete Metrik. Es ist erhältlich bei:

1. Wenn Sie diese berechnete Metrik bereits erstellt haben, suchen Sie sie unter "Metriken"und ziehen Sie sie in den Arbeitsbereich.
2. Wenn Sie diese berechnete Metrik noch nicht erstellt haben, klicken Sie auf das Symbol **+** neben der Metrikliste, um den Generator für berechnete Metriken zu öffnen.
3. Geben Sie den Titel "Seitenansichten pro Besuch"und ggf. eine Beschreibung ein.
4. Legen Sie das Format auf "Dezimal"fest und setzen Sie die Anzahl der Dezimalstellen auf 2.
5. Ziehen Sie die Metrik **Seitenansichten** und **Besuche** in den Definitionsbereich.
6. Ordnen Sie die Definition so an, dass die Formel **Seitenansichten dividiert durch Besuche** ist.

   ![Seitenansichten pro Besuch](/help/technotes/ga-to-aa/assets/page_views_per_visit.png)

7. Klicken Sie auf Speichern, um zu Ihrem Arbeitsbereich zurückzukehren.
8. Ziehen Sie die neu definierte berechnete Metrik in den Arbeitsbereich.

   Weitere Informationen zu [berechneten Metriken](/help/components/c-variables/c-metrics/calculated-metric.md) finden Sie im Komponenten-Benutzerhandbuch.

**Durchschnittl. Die Sitzungsdauer** entspricht ungefähr der **Zeit pro Besuch (Sekunden)**. Weitere Informationen zu [Besuchszeitmetriken](/help/components/c-variables/c-metrics/metrics-time-spent.md) finden Sie im Komponenten-Benutzerhandbuch.

## Konversionsmetriken

**Die Zielumrechnungsrate**, die **Zielabschlüsse** und der **Zielwert** erfordern eine zusätzliche Implementierung auf beiden Plattformen. Wenn Ihre Implementierung bereits die Produktdimension und das Kaufereignis berücksichtigt, sollten Sie die folgenden Schritte beachten:

1. Ziehen Sie die Metriken **Bestellungen** , **Umsatz** und **Besuche** in den Arbeitsbereich.
1. Erstellen Sie eine berechnete Metrik aus **Bestellungen pro Besuch**. Verwenden Sie Strg+Klick (Windows) oder Cmd+Klick (Mac) für beide Metrik-Überschriften, um sie hervorzuheben. Klicken Sie mit der rechten Maustaste auf eine der Überschriften, wählen Sie Metrik aus Auswahl **erstellen** und klicken Sie dann auf **Unterteilen**. Diese neue Metrik ähnelt einer Zielkonversionsrate.
1. Falls Dezimalstellen erforderlich sind, bearbeiten Sie die berechnete Metrik. Klicken Sie auf die Schaltfläche Info in der Metrik-Kopfzeile und dann auf das Stiftsymbol. Fügen Sie im Fenster Aufbau berechneter Metriken 1 oder 2 Dezimalstellen hinzu und klicken Sie dann auf Speichern.

   ![Bestellungen pro Besuch](/help/technotes/ga-to-aa/assets/orders_per_visit.png)

Wenn Ihre Implementierung noch keine Produkt- oder Konversionsdaten enthält, empfiehlt Adobe, mit einem Implementierungsberater zusammenzuarbeiten, um die Datenqualität und -integrität sicherzustellen.
