---
description: Beschreibt, wie Sie Zielwährungs-Codes definieren, damit die Unterstützung mehrerer Währungen funktioniert.
title: Unterstützung mehrerer Währungen
feature: Analytics Basics
exl-id: b67f459c-0636-4eac-af52-51846bb583b5
source-git-commit: 99156dd9d898ce0abf214561cb0040c647d7e6ab
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 16%

---

# Unterstützung mehrerer Währungen

Adobe bietet mehrere Stufen der Währungsumrechnung, sodass Ihr Unternehmen die gewünschte Währung in vielen Berichten erreichen kann. Die Konversion erfolgt auf drei Ebenen:

## Seitenebene

Sie können die [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) um die gewünschte Währung auf jeder Seite festzulegen. Wenn die Währung auf der Seite nicht mit der Währung der Ziel-Report Suite übereinstimmt, führt Adobe eine Währungsumrechnung in die Währung der Report Suite basierend auf dem aktuellen Tageswechselkurs durch. Die konvertierte Währung wird aufgezeichnet.

## Report Suite-Ebene

Jede Report Suite verfügt über eine **Basiswährung**. Diese Währung bestimmt den Kontext aller Währungsmetriken (z. B. [Umsatz](/help/components/metrics/revenue.md)). Alle gespeicherten Währungsdaten befinden sich in der Basiswährung der Report Suite.

