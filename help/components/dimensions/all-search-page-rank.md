---
title: Rangansicht aller Suchseiten
description: Bestimmen Sie, welche Seite in einer Suchmaschine ein Besucher zu Ihrer Site durchgeklickt hat.
feature: Dimensions
exl-id: 58ce54c3-cc45-4e84-a14d-5fec0b70f50f
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 85%

---

# Rangansicht aller Suchseiten

Der &quot;Rangansicht aller Suchseiten&quot; [Dimension](overview.md) bietet Einblicke, auf welche Seite mit Suchergebnissen ein Besucher zu Ihrer Site durchgeklickt hat. Wenn Ihre Site beispielsweise auf der zweiten Seite der Suchergebnisse einer Suchmaschine erscheint, ist das Dimensionselement für diese Variable „Suchseite 2“.

## Füllen dieser Dimension mit Daten

Damit diese Dimension funktioniert, müssen die [internen URL-Filter](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) in Ihrer Report Suite korrekt eingerichtet sein. AppMeasurement füllt diese Dimension automatisch ohne Änderungen am Implementierungscode.

## Dimensionselemente

Wenn ein Besucher von einer Suchmaschine zu Ihrer Site durchklickt, lautet der Wert dieser Dimension „Suchseite“, gefolgt von der Seitenzahl, auf der er durchgeklickt hat. Wenn ein Treffer nicht von einer Suchmaschine stammt, lautet der Wert dieser Dimension „Nicht angegeben“.
