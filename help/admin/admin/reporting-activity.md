---
description: Erfahren Sie, wie Sie mit dem Reporting Activity Manager Kapazitätsprobleme während Spitzenzeiten der Berichterstellung diagnostizieren und beheben können.
title: Reporting Activity Manager
feature: Admin Tools
hide: true
hidefromtoc: true
source-git-commit: 70cfad1a04d17e1007178f32af73988be503fe90
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 1%

---


# Reporting Activity Manager

>[!NOTE]
>
>Diese Funktion befindet sich derzeit im Beta-Test.

Mit dem Reporting Activity Manager können Sie die Berichtskapazität für jede Report Suite in Ihrer Organisation anzeigen. Als Administrator erhalten Sie detaillierte Einblicke in den Berichtsverbrauch und können mühelos Kapazitätsprobleme während Spitzenzeiten der Berichterstellung diagnostizieren und beheben. Wenn Ihr Unternehmen die Berichtsanforderungskapazität erreicht und die Berichtsleistung verschlechtert wird, können Sie jetzt Reporting-Probleme selbstdiagnostizieren, ohne dass dies vom Kundendienst oder vom Techniker der Adobe vorgenommen wird. Sie können einfach Berichtwarteschlangen in einer einzigen Oberfläche verwalten und sofort &#x200B; handeln, um das Benutzererlebnis zu verbessern. Dieses Tool:

* Informiert Sie über Ihre aktuelle Berichtskapazität in all Ihren Report Suites.
* Enthält detaillierte Berichtabfrageinformationen zu aktuellen Berichtsanforderungen, unabhängig davon, ob sie sich in der Warteschlange befinden oder in Bearbeitung sind.
* Ermöglicht Ihnen die Optimierung der Berichtswarteschlange durch Priorisierung einiger Anforderungen und Abbruch anderer Berichtsanforderungen, um die Kapazität freizugeben. Mit anderen Worten: Sie können in Echtzeit fragen: Ist dieser Bericht zu diesem Zeitpunkt notwendig oder kann ich ihn zugunsten dringender Berichte ablehnen?

## Zugriff auf den Reporting Activity Manager

In Adobe Analytics navigieren Administratoren zu **[!UICONTROL Admin]** > **[!UICONTROL Reporting Activity Manager]**.

## Berichtwarteschlange verwalten

Beim Öffnen des Reporting-Aktivitäts-Managers wird eine Liste der zugrunde liegenden Report Suites angezeigt. Virtual Report Suites sind in dieser Ansicht nicht enthalten.

![Berichtwarteschlange](assets/reporting-activity1.png)

Virtual Report Suites bieten Berichtsanforderungen aufgrund zusätzlicher angewendeter Filter- und Segmentierungsebenen zusätzliche Komplexität. Alle Anforderungen, die von Virtual Report Suites stammen, werden kombiniert und gelangen zur zugrunde liegenden Report Suite. Wenn Sie also 10 Anforderungen von 5 VRSs haben, sind dies 50 Anforderungen auf der Basis-Report Suite. Auf diese Weise können Sie die Kapazität sehr schnell erreichen.

Im Folgenden finden Sie eine Ansicht einer VRS, deren Berichtskapazität in Echtzeit angezeigt wird:

![Virtual Report Suites](assets/reporting-activity-vrs.png)

Aktualisieren Sie die Seite, um die Ergebnisse zu ändern.

## Auswirkungen von Workspace-Berichten





