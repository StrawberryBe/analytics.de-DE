---
title: Merchandising-eVars und Methoden zur Produktsuche
description: Ein tiefer Einblick in die Konzepte hinter Merchandising-eVars und deren Verarbeitung und Zuordnung von Daten.
source-git-commit: 746c2cfd3236df7ec7498749015ddf75c1e558f5
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Merchandising-eVars und Methoden zur Produktsuche

In diesem Dokument werden die Konzepte hinter Merchandising-eVars erläutert, die Daten anders verarbeiten und zuordnen als normale eVars. Außerdem wird erläutert, wie Merchandising-eVars mit Produktsuchmethoden zusammenhängen.

Die meisten Websites für den Einzelhandel bieten zwar viele Möglichkeiten, Produkte zu finden, die Adobe betrachtet jedoch die folgenden grundlegenden Methoden zur Produktsuche, die jeder Einzelhandelskunden in Adobe Analytics verfolgen sollte:

* Interne Suchkeywords
* Interne Kampagnen-Trackingcodes
* Merchandising-/Browse-Kategorien
* Verknüpfungen zum Cross-Selling

Zuordnen von einigen eVars zu den Lösungen für die Zwecke dieses Dokuments sehen wir wie folgt aus:

* eVar2: Interne Suchkeywords
* eVar3: Interne Kampagnen-Trackingcodes
* eVar4: Merchandising-/Browse-Kategorien
* eVar5: Verknüpfungen zum Cross-Selling

Wir können eine zusätzliche eVar verwenden, um die Leistung aller Methoden zur Produktsuche untereinander zu messen. Zusätzlich zu den oben beschriebenen Suchmethoden umfasst das eVar weitere Suchmethoden, wie z. B. Links zu Produktdetailseiten von externen Websites.

* eVar1: Methoden zur Produktsuche

Sie sollten keine dieser Variablen so konfigurieren, dass sie Standard-eVars sind, sondern sie stattdessen so konfigurieren, dass sie Merchandising-eVars sind.  Durch die Verwendung von Merchandising-eVars können Sie den von eVars erfassten Werten eine beliebige erfolgreiche Aktivität auf *pro Produkt*-Ebene statt auf *pro Besuch/pro Bestellung*-Ebene zuweisen. Ich werde den Unterschied zwischen der Verteilung pro Produkt und pro Bestellung im Rest dieses Dokuments klären.

