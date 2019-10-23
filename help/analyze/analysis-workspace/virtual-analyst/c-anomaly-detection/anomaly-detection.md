---
description: Datenanomalien können kontextbezogen in Analysis Workspace angezeigt und analysiert werden.
seo-description: Datenanomalien können kontextbezogen in Analysis Workspace angezeigt und analysiert werden.
seo-title: Übersicht über die Anomalieerkennung
title: Übersicht über die Anomalieerkennung
uuid: 991fde08-198c-4410-9606-d5a4f3dd8339
translation-type: tm+mt
source-git-commit: ca9f1ed00295b556250894ae4e7fa377ef8a593d

---


# Übersicht über die Anomalieerkennung

Sie können Datenanomalien kontextuell im Analysis Workspace anzeigen und analysieren.

[Anomalieerkennung auf YouTube](https://www.youtube.com/watch?v=krXyQCjXoeU&index=63&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) (4:53)

[Beitragsanalyse auf YouTube](https://www.youtube.com/watch?v=MbpeJIADtGk&index=64&list=PL2tCx83mn7GuNnQdYGOtlyCu0V5mEZ8sS) (3:20)

> [!IMPORTANT] Die Anomalieerkennung ist nur in Analysis Workspace verfügbar. Kunden von Adobe Analytics Select und Foundation haben nur Zugriff auf die "Granularität pro Tag"-Anomalieerkennung in Workspace. Weitere Informationen finden Sie unter [Anomalieerkennung und Beitragsanalyse – Berechtigungen](../contribution-analysis/ca-tokens.md).

Die Anomalieerkennung bietet eine statistische Methode, mit der festgestellt wird, wie sich eine bestimmte Metrik in Bezug auf frühere Daten verändert hat.

Die Anomalieerkennung ermöglicht es Ihnen, „echte Signale“ von „Rauschen“ zu unterscheiden. Zudem hilft sie Ihnen anschließend dabei, potenzielle Faktoren zu bestimmen, die zu diesen Signalen oder Anomalien beigesteuert haben. Auf diese Weise können Sie feststellen, welche statistischen Schwankungen relevant sind, und anschließend die Ursache eines echten Fehlers feststellen. Zudem erhalten Sie eine zuverlässige Metrikvorhersage (KPI).

Zu Beispielen von Fehlern, die ein Eingreifen Ihrerseits erfordern, zählen:

* Erhebliche Verwerfungen im durchschnittlichen Bestellwert
* Spitzen in Bestellungen mit geringem Umsatz
* Spitzen oder Verwerfungen in Testprogrammregistrierungen
* Verwerfungen bei Landingpage-Aufrufen
* Spitzen in Videopufferereignissen
* Spitzen in niedrigen Video-Bitraten

Sowohl die Anomalieerkennung als auch die [Beitragsanalyse](https://marketing.adobe.com/resources/help/en_US/analytics/contribution/ca_main.html) sind zentrale Workflows in Analysis Workspace. Sie können Beitragsanalysen zu jeder beliebigen täglichen Anomalie ausführen und das Ergebnis in Ihr Analysis Workspace-Projekt einbetten.

Der Algorithmus der Analysis Workspace-Anomalieerkennung umfasst:

* Unterstützung für die Einstellungen „Stündlich“, „Wöchentlich“ und „Monatlich“ (zusätzlich zur vorhandenen Einstellung „Täglich“)
* Berücksichtigung von besonderen Tagen (wie z. B. Black Friday) und Feiertagen
