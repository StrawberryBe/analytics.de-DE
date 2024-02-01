---
description: Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.
title: Intelligente Warnhinweise
feature: Alerts
exl-id: 1b23211e-7632-4b33-a27d-c58b3bbbbab1
source-git-commit: be5a73347d417c8dc6667d4059e7d46ef5f0f5cd
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 68%

---

# Intelligente Warnhinweise

Das neue System für intelligente Warnhinweise erlaubt eine feiner abgestufte Kontrolle über Warnhinweise und integriert die Anomalieerkennung in das Warnhinweissystem.

Im Folgenden finden Sie eine Videoübersicht:

>[!VIDEO](https://video.tv.adobe.com/v/25446/?quality=12)

## Überblick {#section_6AC8CA81DEA94E99B0F192B60D0FDF03}

>[!IMPORTANT]
>
>Intelligente Warnhinweise sind nur für Kunden von Adobe [!DNL Analytics] Prime und Adobe [!DNL Analytics] Ultimate verfügbar.

Mithilfe intelligenter Warnhinweise können Sie

* Warnhinweise erstellen, die auf Anomalien basieren (90-%-, 95-%-, 99-%-, 99,75-%- und 99,9-%-Schwellen, Änderungen in %, darüber/darunter).
* In einer Vorschau anzeigen, wie oft ein Warnhinweis ausgelöst wird.
* Warnhinweise per E-Mail oder SMS mit Links zu automatisch erstellten Projekten in Analysis Workspace verschicken.
* „Gestapelte“ Warnhinweise erstellen, die mehrere Metriken in einem Warnhinweis vereinen.

Das neue Warnhinweissystem enthält die folgenden Komponenten: Warnhinweiserstellung, Warnhinweis-Manager, Warnhinweisvorschau. Es bietet darüber hinaus einen besseren kontextbezogenen Zugang zur Erstellung von Warnhinweisen. Die Benutzeroberfläche für das alte Warnhinweissystem wird nicht mehr zur Verfügung stehen, die Warnhinweise werden jedoch migriert. Einige alte Warnhinweisfunktionen [werden nicht mehr zur Verfügung stehen](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/alerts.html?lang=de).

Es gibt drei Möglichkeiten, zur Warnhinweiserstellung zu gelangen:

* Mithilfe des folgenden Tastaturbefehls in Analysis Workspace:

  `ctrl (or cmd) + shift + a`
* Indem Sie direkt zur Warnhinweiserstellung wechseln: **[!UICONTROL Workspace]** > **[!UICONTROL Komponenten]** > **[!UICONTROL neuer Warnhinweis]** .
* Indem Sie ein oder mehrere Freiform-Tabellenzeilenelemente auswählen, mit der rechten Maustaste klicken und **[!UICONTROL Warnhinweis aus Auswahl erstellen auswählen]**. Dadurch wird die Warnhinweiserstellung geöffnet, und die entsprechenden Metriken und angewendeten Filter aus der Tabelle werden automatisch eingetragen sein. Falls erforderlich, können Sie den Warnhinweis dann bearbeiten.

  ![](assets/create-alert-from-selection.png)


## FAQs: Wie werden Warnhinweise berechnet und ausgelöst? {#trigger}

Bei den prozentualen Schwellenwerten handelt es sich um Standardabweichungen. Beispiel: 95 % = 2 Standardabweichungen und 99 % = 3 Standardabweichungen. Abhängig von der ausgewählten Zeitgranularität [verschiedene Modelle](/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md) werden verwendet, um zu berechnen, wie weit (wie viele Standardabweichungen) jeder Datenpunkt von der Norm entfernt ist. Wenn Sie einen niedrigeren Schwellenwert festlegen (z. B. 90 %), erhalten Sie mehr Anomalien als bei einem höheren Schwellenwert (99 %). Die Schwellenwerte 99,75 % und 99,99 % wurden speziell für die Granularität „Stündlich“ eingeführt, damit nicht allzu viele Anomalien ausgelöst werden.

+++ Wie weit reicht die Anomalieerkennung des Warnhinweises zurück, um Datenanomalien zu ermitteln?

Der Trainingszeitraum hängt von der ausgewählten Granularität ab. Weitere Informationen finden Sie unter den statistischen Verfahren für die <a href="/help/analyze/analysis-workspace/c-anomaly-detection/statistics-anomaly-detection.md">Anomalieerkennung</a>. Zusammenfassung:

* Monatlich = 15 Monate + derselbe Bereich im letzten Jahr
* Wöchentlich = 15 Wochen + derselbe Bereich im letzten Jahr
* Täglich = 35 Tage + derselbe Bereich im letzten Jahr
* Stündlich = 336 Stunden

+++

+++ Kann ich die Anomaliefunktion verwenden oder einen absoluten Wert verwenden, um nur auf einen Rückgang des Verhaltens oder nur auf einen Anstieg des Verhaltens hingewiesen zu werden?

Wenn Sie den absoluten Wert verwenden, werden weiterhin Trigger-Warnhinweise für Tiefpunkte und Spitzen angezeigt. Sie können keine gesonderten Warnhinweise nur für Rückgänge oder nur für Anstiege einrichten.

+++

+++ Kann ich Warnhinweise nur zu bestimmten Tageszeiten für den Trigger konfigurieren (z. B. Geschäftszeiten im Vergleich zu Geschäftszeiten außerhalb der Geschäftszeiten)?

Derzeit ist dies leider nicht möglich.

+++

+++ Kann ich eine Tabelle der &quot;erwarteten Werte&quot;, die die gepunktete Linie ausmachen, oder eine Art Ausgabe davon erhalten, was diese Werte sind?

Nicht in Workspace, aber Sie können in Report Builder. Siehe [dieses Video](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/exporting/report-builder/anomaly-detection-in-report-builder.html?lang=de) zur Anomalieerkennung im Report Builder.

Beachten Sie, dass in Report Builder weniger ausgefeilte Methoden zur Anomalieerkennung angewandt werden. Es wird ein fester 30-tägiger Schulungzeitraum verwendet, festes 95-%-Intervall.

+++
