---
description: Beschreibt, wie Sie Zielwährungs-Codes definieren, damit die Unterstützung mehrerer Währungen funktioniert.
title: Unterstützung mehrerer Währungen
feature: Analytics Basics
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
source-git-commit: f659d1bde361550928528c7f2a70531e3ac88047
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 10%

---

# Unterstützung mehrerer Währungen

Adobe bietet mehrere Stufen der Währungsumrechnung, sodass Ihr Unternehmen die gewünschte Währung in vielen Berichten erreichen kann. Die Konversion erfolgt auf drei Ebenen:

## Seitenebene

Sie können die [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) um die gewünschte Währung auf jeder Seite festzulegen. Wenn die Währung auf der Seite nicht mit der Währung der Ziel-Report Suite übereinstimmt, führt Adobe eine Währungsumrechnung in die Währung der Report Suite basierend auf dem aktuellen Tageswechselkurs durch. Die konvertierte Währung wird aufgezeichnet.

## Report Suite-Ebene

Jede Report Suite verfügt über eine **Basiswährung**. Diese Währung bestimmt den Kontext aller Währungsmetriken (z. B. [Umsatz](/help/components/metrics/revenue.md)). Alle gespeicherten Währungsdaten befinden sich in der Basiswährung der Report Suite.

## Benutzerebene

Für Reports &amp; Analytics können Benutzer unter eine andere Währung als die Basiswährung der Report Suite festlegen. [Berichtseinstellungen](/help/analyze/reports-analytics/report-settings.md). Diese Einstellung ist zerstörungsfrei, d. h., die zugrunde liegenden Daten werden nicht geändert. Stattdessen wird die grundlegende Währungsumrechnung auf alle angezeigten Berichte angewendet, die auf dem aktuellen Wechselkurs basieren. Wenn Sie denselben Bericht an unterschiedlichen Tagen anzeigen, können sich die Zahlen aufgrund unterschiedlicher Tageswechselkurse ändern.

Analysis Workspace bietet derzeit keine Währungsumrechnung auf Benutzerebene an.
