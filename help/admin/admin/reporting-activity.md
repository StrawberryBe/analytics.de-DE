---
description: Erfahren Sie, wie Sie mit dem Reporting Activity Manager Kapazitätsprobleme während Spitzenzeiten der Berichterstellung diagnostizieren und beheben können.
title: Reporting Activity Manager
feature: Admin Tools
hide: true
hidefromtoc: true
source-git-commit: 6ab2f39bdfc3a50c2b91f020c98b0e81da8b2b8e
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 3%

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

## Berichtwarteschlange anzeigen

Beim Öffnen der Übersichtsseite &quot;Reporting Activity Manager&quot;wird eine Liste Ihrer aktivierten Basis-Report Suites angezeigt.

![Berichtwarteschlange](assets/reporting-activity1.png)

| UI-Element | Beschreibung |
| --- | --- |
| **[!UICONTROL Report Suite]** | Die zugrunde liegende Report Suite |
| **[!UICONTROL Virtual Report Suite]** | Alle Virtual Report Suites, die in diese zugrunde liegende Report Suite einfließen. Virtual Report Suites bieten Berichtsanforderungen aufgrund zusätzlicher angewendeter Filter- und Segmentierungsebenen zusätzliche Komplexität. Alle Anforderungen, die von Virtual Report Suites stammen, werden kombiniert und gelangen zur zugrunde liegenden Report Suite.<p>Wenn Sie 10 Anforderungen von 5 VRSs haben, sind dies 50 Anforderungen auf der Basis-Report Suite. Auf diese Weise können Sie die Kapazität sehr schnell erreichen. |
| **[!UICONTROL Nutzungskapazität]** | Prozentualer Anteil, wie viel der Berichterstellungskapazität der Report Suite in Echtzeit verwendet wird. |
| **[!UICONTROL Status]** | Vier mögliche Statusindikatoren: <ul><li>**Rot - Kapazität**: Die Report Suite wird in Bezug auf die Berichtskapazität festgelegt.</li><li>**Gelb - Nahtfähigkeit**: Diese Report Suite läuft Gefahr, ihre maximale Kapazität zu erreichen.</li><li>**Grün - verfügbar**: Die Berichtskapazität ist reichlich.</li><li>**Grau - nicht verfügbar**: Die Report Suite ist nicht für die Berichtskapazität konfiguriert.</li></ul> |

Aktualisieren Sie die Seite, um die Ergebnisse zu ändern.

## Report Suites filtern

Sie können die Report Suites nach