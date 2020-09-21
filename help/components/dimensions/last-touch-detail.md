---
title: Letztkontakt-Kanaldetail
description: Details zum neuesten Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '313'
ht-degree: 100%

---


# Letztkontakt-Kanaldetail

Die Dimension „Letztkontakt-Kanaldetail“ enthält Details zum letzten Marketing-Kanal, mit dem ein Besucher während der Interaktionszeit des Besuchers (standardmäßig 30 Tage) übereinstimmt. Diese Dimension ist nützlich, um zu verstehen, was dazu beigetragen hat, dass der Treffer einem Marketing-Kanal entsprach. Wenn beispielsweise ein Besucher zu Ihrer Site gelangt ist und mit dem Marketing-Kanal „Paid Search“ übereinstimmt, können Sie anhand des Kanaldetails sehen, welche Suchmaschine verwendet wurde oder nach welchem Schlüsselwort er gesucht hat.

## Füllen dieser Dimension mit Daten

Diese Dimension kopiert Werte aus anderen Variablen. Die verwendete Variable referenziert den Kanalwert in jeder [Marketing-Kanalverarbeitungsregel](/help/admin/admin/marketing-channels-admin.md). Wenn ein Treffer mit einer Marketing-Kanalverarbeitungsregel übereinstimmt, wird die Dimension [Letztkontakt-Kanal](last-touch-channel.md) auf den Kanalnamen festgelegt und diese Dimension auf den in der Regel festgelegten Kanalwert gesetzt.

Führen Sie die folgenden Schritte aus, um diese Dimension auf einen bestimmten Wert zu setzen:

* Achten Sie darauf, dass sich das gewünschte Dimensionselement in einem Trefferattribut oder einer benutzerdefinierten Variable befindet.
* Legen Sie eine Marketing-Kanalverarbeitungsregel fest, die die gewünschten Kriterien für den Treffer enthält.
* Wählen Sie den gewünschten Dropdown-Wert in der Marketing-Kanalverarbeitungsregel unter [!UICONTROL Kanalwert setzen].
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Marketing-Kanalverarbeitungsregel beschrieben sind.

## Dimensionselemente

Die Dimensionselemente hängen vom Dropdown-Menü „Kanalwert“ ab. Wenn Sie beispielsweise den Wert des Kanals auf „Seiten-URL“ setzen, umfassen die Dimensionselemente die Seiten-URLs auf Ihrer Site. Wenn Sie den Wert des Kanals auf „Referrer-Domäne“ setzen, umfassen die Dimensionselemente die Domänen, auf die Besucher geklickt haben, um zu Ihrer Site zu gelangen. Diese Dimension aggregiert alle Detaildimensionselemente, unabhängig davon, auf welchem Kanal sie sich befinden.

Adobe empfiehlt, Kanalwerte für den Marketing-Kanal festzulegen, um Einblick in die Kanaldetails zu erhalten.
