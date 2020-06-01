---
description: Im Bereich "Analytics für Zielgruppe"(A4T) können Sie Ihre Adobe-Zielgruppe-Aktivitäten und -Erlebnisse im Arbeitsbereich für Analysen analysieren.
title: Bereich "Analyse für Zielgruppe"(A4T)
translation-type: tm+mt
source-git-commit: 516557c04acbc7300925ed3d13ac3c087f3ed3de
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 14%

---


# Bereich &quot;Analyse für Zielgruppe&quot;(A4T)

>[!IMPORTANT]
>
>**[!UICONTROL Das Bedienfeld]** &quot;Analytics für Zielgruppen&quot;befindet sich derzeit in eingeschränkten Tests. [Mehr Infos](https://docs.adobe.com/content/help/en/analytics/landing/an-releases.html)

Im Bereich &quot;Analyse für Zielgruppe&quot;(A4T) können Sie Ihre Adobe-Zielgruppe-Aktivitäten und -Erlebnisse im Arbeitsbereich für Analysen analysieren. Sie ermöglicht Ihnen außerdem, Steigerung und Konfidenz für bis zu drei Erfolgsmetriken zu sehen. Um auf das A4T-Bedienfeld zuzugreifen, navigieren Sie zu einer Report Suite mit aktivierten A4T-Komponenten. Klicken Sie dann auf das Bedienfeldsymbol ganz links und ziehen Sie das Bedienfeld &quot;Analytics für Zielgruppe&quot;in Ihr Analyse Workspace-Projekt.

## Bedienfeldaufbau

Sie können das A4T-Bedienfeld mithilfe der folgenden Einstellungen konfigurieren:

| Einstellung | Beschreibung |
|---|---|
| Target-Aktivität | Wählen Sie aus einer Liste von Zielgruppen-Aktivitäten aus oder ziehen Sie eine Aktivität per Drag &amp; Drop aus der linken Leiste.<br>**Hinweis:**Die Liste wird mit den letzten 6 Monaten von Aktivitäten gefüllt, die mindestens einen Treffer hatten. Wenn Sie keine Aktivität in der Liste sehen, kann sie älter als 6 Monate sein. Es kann noch von der linken Leiste hinzugefügt werden, die eine Wartezeit von bis zu 18 Monaten hat. |
| Control-Erlebnis | Wählen Sie Ihr Kontrollerlebnis aus. Sie können sie bei Bedarf im Dropdown-Menü ändern. |
| Normalisierungsmetrik | Wählen Sie aus &quot;Individuelle Besucher&quot;, &quot;Besuche&quot;oder &quot;Aktivitäten-Impressionen&quot;. Für die meisten Anwendungsfälle der Analyse werden individuelle Besucher empfohlen. |
| Erfolgsmetriken | Wählen Sie bis zu 3 standardmäßige Erfolgsmetriken aus den Dropdown-Listen oder ziehen Sie Metriken per Drag &amp; Drop aus der linken Leiste. Jede Metrik verfügt über eine dedizierte Tabelle und Visualisierung im gerenderten Bedienfeld. |
| Kalenderdatumsbereich | Dies wird automatisch aufgefüllt, basierend auf dem Datumsbereich der Aktivität von Adobe Zielgruppe. Sie können es bei Bedarf ändern. |

![](assets/a4t-panel-builder.png)

## Bereichsausgabe

Das Bedienfeld &quot;Analytics für Zielgruppen&quot;enthält umfangreiche Daten und Visualisierungen, die Ihnen helfen, die Leistung Ihrer Adobe-Zielgruppe-Aktivität und -Erlebnisse besser zu verstehen. Oben im Bedienfeld wird eine Übersichtszeile angezeigt, die Sie an die ausgewählten Bedienfeldeinstellungen erinnert. Sie können das Bedienfeld jederzeit bearbeiten, indem Sie oben rechts auf den Stift zum Bearbeiten klicken.

Für jede ausgewählte Erfolgsmetrik wird eine Freiformtabelle und ein Konversionsrat-Trend angezeigt:

![](assets/a4t-rendered.png)

Jede Freiform-Tabelle zeigt die folgenden Metrikspalten:

| Metrik | Beschreibung |
|---|---|
| Normalisieren von Metriken | Impressionen zu individuellen Besuchern, Besuchen oder Aktivitäten. |
| Erfolgsmetrik | Die im Builder ausgewählte Metrik |
| Konversionsrate | Erfolgsmetrik/Normalisierungsmetrik |
| Steigerung | Vergleicht für jedes Erlebnis die Konversionsrate mit dem Kontrollerlebnis.<br>**Hinweis:**Steigerung ist eine &quot;gesperrte Metrik&quot;für Erlebnisse in der Zielgruppe. Es kann nicht mit anderen Dimensionen aufgeschlüsselt oder verwendet werden. |
| Steigerung (Mindestwert) | Stellt den schlechtesten Aufstieg dar, den ein Variantenerlebnis im Vergleich zum Kontrollerlebnis aufweisen könnte. |
| Steigerung (mittlerer Wert) | Stellt den mittleren Aufstieg dar, den ein Variantenerlebnis bei einem Konfidenzintervall von 95 % im Vergleich zum Kontrollerlebnis aufweisen könnte. Dies ist &quot;Steigerung&quot;in Reports &amp; Analysen. |
| Steigerung (Maximalwert) | Stellt den besten Aufstieg dar, den ein Variantenerlebnis im Vergleich zum Kontrollerlebnis aufweisen könnte. |
| Konfidenz | Der Studierende-t-Test berechnet das Konfidenzniveau, das die Wahrscheinlichkeit angibt, dass die Ergebnisse dupliziert würden, wenn der Test erneut ausgeführt würde. Auf die Metrik wurde ein fester Bereich für die bedingte Formatierung von 75 %/85 %/95 % angewendet. Diese Formatierung kann bei Bedarf unter Spalteneinstellungen angepasst werden. <br>**Hinweis:**Konfidenz ist eine &quot;gesperrte Metrik&quot;für Erlebnisse in der Adobe-Zielgruppe. Es kann nicht heruntergebrochen oder mit anderen Dimensionen verwendet werden. |

Wie bei allen Bedienfeldern im Arbeitsbereich für Analysen können Sie Ihre Analyse fortsetzen, indem Sie zusätzliche Tabellen und [Visualisierungen](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html) hinzufügen, die Ihnen bei der Analyse Ihrer Adobe Zielgruppe-Aktivitäten helfen.

Weitere Optionen zu Analytics für Zielgruppe Berichte finden Sie im [A4T-Berichte](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/reporting.html)
