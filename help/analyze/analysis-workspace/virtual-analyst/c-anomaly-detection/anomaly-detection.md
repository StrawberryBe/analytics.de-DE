---
description: Datenanomalien können kontextbezogen in Analysis Workspace angezeigt und analysiert werden.
title: Übersicht über die Anomalieerkennung
uuid: 991fde08-198c-4410-9606-d5a4f3dd8339
feature: AI-Tools
role: Geschäftspraktiker, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 89%

---


# Übersicht über die Anomalieerkennung

Datenanomalien können kontextbezogen in Analysis Workspace angezeigt und analysiert werden.

[Videoschulung](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/data-science/anomaly-detection-in-analysis-workspace.html)  zur Anomalieerkennung (4:53)

[Video-Tutorial](https://docs.adobe.com/content/help/en/analytics-learn/tutorials/data-science/contribution-analysis-workspace.html)  zur Beitrags-Analyse (3:20)

>[!IMPORTANT]
>
>Die Anomalieerkennung wurde aus dem Funktionsumfang von Reports &amp; Analytics entfernt und ist nun nur noch über Analysis Workspace verfügbar. Beachten Sie, dass Kunden von Adobe Analytics Select und Adobe Analytics Foundation in Workspace nur Zugriff auf die Anomalieerkennung „tägliche Granularität“ haben. Weitere Informationen finden Sie unter [Anomalieerkennung und Beitragsanalyse – Berechtigungen](/help/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.md#section_9278D58F21A840AA9B1ED1BD07A1EF0A).

Die Anomalieerkennung bietet eine statistische Methode, mit der festgestellt wird, wie sich eine bestimmte Metrik in Bezug auf frühere Daten verändert hat.

Die Anomalieerkennung ermöglicht es Ihnen, „echte Signale“ von „Rauschen“ zu unterscheiden. Zudem hilft sie Ihnen anschließend dabei, potenzielle Faktoren zu bestimmen, die zu diesen Signalen oder Anomalien beigesteuert haben. Auf diese Weise können Sie feststellen, welche statistischen Schwankungen relevant sind, und anschließend die Ursache eines echten Fehlers feststellen. Zudem erhalten Sie eine zuverlässige Metrikvorhersage (KPI).

Zu Beispielen von Fehlern, die ein Eingreifen Ihrerseits erfordern, zählen:

* Erhebliche Verwerfungen im durchschnittlichen Bestellwert
* Spitzen in Bestellungen mit geringem Umsatz
* Spitzen oder Verwerfungen in Testprogrammregistrierungen
* Verwerfungen bei Landingpage-Aufrufen
* Spitzen in Videopufferereignissen
* Spitzen in niedrigen Video-Bitraten

Sowohl die Anomalieerkennung als auch die [Beitragsanalyse](https://docs.adobe.com/content/help/de-DE/analytics/analyze/analysis-workspace/virtual-analyst/anomaly-detection/anomaly-detection.html) sind zentrale Workflows in Analysis Workspace. Sie können Beitragsanalysen zu jeder beliebigen täglichen Anomalie ausführen und das Ergebnis in Ihr Analysis Workspace-Projekt einbetten.

Der Algorithmus der Analysis Workspace-Anomalieerkennung umfasst:

* Unterstützung für die Einstellungen „Stündlich“, „Wöchentlich“ und „Monatlich“ (zusätzlich zur vorhandenen Einstellung „Täglich“)
* Berücksichtigung von besonderen Tagen (wie z. B. Black Friday) und Feiertagen
