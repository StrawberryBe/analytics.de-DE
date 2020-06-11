---
title: Letztkontakt Kanal
description: Details zum letzten Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
translation-type: tm+mt
source-git-commit: 87d0c7e20594e2e39f55284e8d50d425cc1cdacf
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---


# Letztkontakt Kanal

Die Dimension &quot;Last Touch-Kanal&quot;enthält Details zum letzten Marketing-Kanal, mit dem ein Besucher während der Interaktionszeit des Besuchers (standardmäßig 30 Tage) übereinstimmt. Diese Dimension ist wertvoll, um zu verstehen, was zum Trefferabgleich eines Marketing-Kanals beigetragen hat. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal für gebührenpflichtige Suchen übereinstimmt, können Sie mithilfe der Angaben zum Kanal sehen, welche Suchmaschine verwendet wurde oder nach welchem Suchbegriff sie gesucht hat.

## Diese Dimension mit Daten füllen

Diese Dimension kopiert Werte aus anderen Variablen. Die verwendete Variable referenziert den Kanal-Wert in jeder [Marketing Kanal-Verarbeitungsregel](/help/admin/admin/marketing-channels-admin.md). Wenn ein Treffer mit einer Verarbeitungsregel des Marketing-Kanals übereinstimmt, wird die Dimension &quot; [Last Touch-Kanal](last-touch-channel.md) &quot;auf den Kanal-Namen festgelegt und diese Dimension auf den in der Regel festgelegten Kanal-Wert gesetzt.

Wenn Sie diese Dimension auf einen bestimmten Wert setzen möchten, sind die folgenden Schritte erforderlich:

* Achten Sie darauf, dass sich der gewünschte Dimensionswert in einem Trefferattribut oder einer benutzerspezifischen Variablen befindet.
* Legen Sie eine Verarbeitungsregel für den Marketing Kanal fest, die die gewünschten Kriterien für den Treffer enthält.
* Wählen Sie den gewünschten Dropdown-Wert unter [!UICONTROL Legen Sie den Wert] des Kanals in der Verarbeitungsregel Marketing Kanal fest.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Verarbeitungsregel Marketing Kanal beschrieben sind.

## Dimensionswerte

Dimensionswerte hängen vom Dropdown-Menü &quot;Kanal&quot;ab. Wenn Sie beispielsweise den Wert des Kanals auf &quot;Seiten-URL&quot;setzen, enthalten Dimensionswerte Seiten-URLs auf Ihrer Site. Wenn Sie den Wert des Kanals auf Verweisende Domäne einstellen, umfassen die Dimensionswerte Domänen, auf die Besucher geklickt haben, um zu Ihrer Site zu gelangen. Diese Dimension Aggregat alle Detail-Dimensionswerte, unabhängig davon, in welchem Kanal sie sich befinden.

Adobe empfiehlt die Festlegung von Kanal-Werten für den Marketing-Kanal, um Einblicke in Details zu Kanälen zu erhalten.
