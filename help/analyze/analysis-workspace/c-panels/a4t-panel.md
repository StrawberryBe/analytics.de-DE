---
description: Mit dem Bedienfeld "Analytics for Target (A4T)"können Sie Ihre Adobe Target-Aktivitäten und -Erlebnisse in Analysis Workspace analysieren.
title: Bedienfeld "Analytics für Target"(A4T)
translation-type: tm+mt
source-git-commit: 9363888ec740b182bc523c6138f9623e1ab0ffda
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 16%

---


# Bedienfeld &quot;Analytics für Target&quot;(A4T)

>[!IMPORTANT]
>
>**[!UICONTROL Analytics for Target (A4T)]** -Bedienfeld befindet sich derzeit in eingeschränkten Tests. [Mehr Infos](https://docs.adobe.com/content/help/de-DE/analytics/landing/an-releases.html)

Im Bereich Analytics for Target (A4T) können Sie Ihre Adobe Target-Aktivitäten und -Erlebnisse in Analysis Workspace analysieren. Sie ermöglicht Ihnen außerdem, Steigerung und Konfidenz für bis zu drei Erfolgsmetriken zu sehen. Um auf das A4T-Bedienfeld zuzugreifen, navigieren Sie zu einer Report Suite mit aktivierten A4T-Komponenten. Klicken Sie dann auf das Bedienfeldsymbol ganz links und ziehen Sie das Bedienfeld &quot;Analytics für Target&quot;in das Analysis Workspace-Projekt.

## Bereichseingänge {#Input}

Sie können das A4T-Bedienfeld mithilfe der folgenden Eingabeeinstellungen konfigurieren:

| Einstellung | Beschreibung |
|---|---|
| Target-Aktivität | Wählen Sie aus einer Liste von Target-Aktivitäten oder ziehen Sie eine Aktivität per Drag &amp; Drop aus der linken Leiste.<br>**Hinweis:**Die Liste wird mit den letzten 6 Monaten von Aktivitäten gefüllt, die mindestens einen Treffer hatten. Wenn Sie keine Aktivität in der Liste sehen, kann sie älter als 6 Monate sein. Es kann noch von der linken Leiste hinzugefügt werden, die eine Wartezeit von bis zu 18 Monaten hat. |
| Control-Erlebnis | Wählen Sie Ihr Kontrollerlebnis aus. Sie können sie bei Bedarf im Dropdown-Menü ändern. |
| Normalisierungsmetrik | Wählen Sie aus &quot;Individuelle Besucher&quot;, &quot;Besuche&quot;oder &quot;Aktivitäten-Impressionen&quot;. Für die meisten Anwendungsfälle der Analyse werden individuelle Besucher empfohlen. Diese Metrik (auch als Zählmethodik bezeichnet) wird zum Nenner der Steigerungsberechnung. Sie wirkt sich auch darauf aus, wie die Daten aggregiert werden, bevor die Konfidenzberechnung angewendet wird. |
| Erfolgsmetriken | Wählen Sie bis zu 3 standardmäßige (nicht berechnete) Erfolgsmetriken aus den Dropdown-Ereignissen oder ziehen Sie Metriken per Drag &amp; Drop aus der linken Leiste. Jede Metrik verfügt über eine dedizierte Tabelle und Visualisierung im gerenderten Bedienfeld. |
| Kalenderdatumsbereich | Dies wird automatisch aufgefüllt, basierend auf dem Datumsbereich der Aktivität von Adobe Target. Sie können es bei Bedarf ändern. |

![Bedienfeldaufbau](assets/a4t-panel-builder.png)

## Bereichsausgabe {#Output}

Das Bedienfeld &quot;Analytics für Target&quot;enthält umfangreiche Daten und Visualisierungen, die Ihnen helfen, die Leistung Ihrer Adobe Target-Aktivität und -Erlebnisse besser zu verstehen. Oben im Bedienfeld wird eine Übersichtszeile angezeigt, die Sie an die ausgewählten Bedienfeldeinstellungen erinnert. Sie können das Bedienfeld jederzeit bearbeiten, indem Sie oben rechts auf den Stift zum Bearbeiten klicken.

Für jede ausgewählte Erfolgsmetrik wird eine Freiformtabelle und ein Konversionsrat-Trend angezeigt:

![gerendert](assets/a4t-rendered.png)


Jede Freiform-Tabelle zeigt die folgenden Metrikspalten:

| Metrik | Beschreibung |
|---|---|
| Normalisieren von Metriken | Impressionen zu individuellen Besuchern, Besuchen oder Aktivitäten. |
| Erfolgsmetrik | Die im Builder ausgewählte Metrik |
| Konversionsrate | Erfolgsmetrik/Normalisierungsmetrik |
| Steigerung | Vergleicht für jedes Erlebnis die Konversionsrate mit dem Kontrollerlebnis.<br>**Hinweis:**Steigerung ist eine &quot;gesperrte Metrik&quot;für Target-Erlebnisse. Es kann nicht mit anderen Dimensionen aufgeschlüsselt oder verwendet werden. |
| Steigerung (Mindestwert) | Stellt den schlechtesten Aufstieg dar, den ein Variantenerlebnis im Vergleich zum Kontrollerlebnis aufweisen könnte. |
| Steigerung (mittlerer Wert) | Stellt den mittleren Aufstieg dar, den ein Variantenerlebnis bei einem Konfidenzintervall von 95 % im Vergleich zum Kontrollerlebnis aufweisen könnte. Dies ist &quot;Steigerung&quot;in Reports &amp; Analytics. |
| Steigerung (Maximalwert) | Stellt den besten Aufstieg dar, den ein Variantenerlebnis im Vergleich zum Kontrollerlebnis aufweisen könnte. |
| Konfidenz | Der Studierende-t-Test berechnet das Konfidenzniveau, das die Wahrscheinlichkeit angibt, dass die Ergebnisse dupliziert würden, wenn der Test erneut ausgeführt würde. Auf die Metrik wurde ein fester Bereich für die bedingte Formatierung von 75 %/85 %/95 % angewendet. Diese Formatierung kann bei Bedarf unter Spalteneinstellungen angepasst werden. <br>**Hinweis:**Konfidenz ist eine &quot;gesperrte Metrik&quot; für Target-Erlebnisse. Es kann nicht mit anderen Dimensionen aufgeschlüsselt oder verwendet werden. |

Wie bei allen Bedienfeldern in Analysis Workspace können Sie Ihre Analyse fortsetzen, indem Sie zusätzliche Tabellen und [Visualisierungen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) hinzufügen, die Ihnen bei der Analyse Ihrer Adobe Target-Aktivitäten helfen.

## Häufig gestellte Fragen (FAQ){#FAQ}

| Frage | Antwort |
|---|---|
| Welche Aktivitäten werden von A4T unterstützt? | [Erfahren Sie mehr](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-activity-setup.html) darüber, welche Aktivitäten unterstützt werden. |
| Werden berechnete Metriken im A4T-Berichte unterstützt? | Nein. [Erfahren Sie mehr](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-lift-and-confidence.html) darüber, warum berechnete Metriken nicht unterstützt werden. |
| Warum unterscheiden sich individuelle Besucher zwischen Target und Analytics? | [Erfahren Sie mehr](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports.html) über die Varianzen individueller Besucher zwischen den Produkten. |
| Warum werden nicht verwandte Erlebnisse zurückgegeben, wenn ich in meiner Analyse ein Treffersegment für eine bestimmte Target-Aktivität anwenden möchte? | Die A4T-Dimension ist eine Variable zur Liste, d. h. sie kann mehrere Aktivitäten (und Erlebnisse) gleichzeitig enthalten. [Mehr Infos](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t-faq/a4t-faq-viewing-reports.html) |

Weitere Informationen zu Analytics für Target Berichte finden Sie im [A4T-Berichte](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/reporting.html)
