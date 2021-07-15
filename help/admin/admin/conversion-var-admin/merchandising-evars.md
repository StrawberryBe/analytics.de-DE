---
title: Merchandising-eVars und Methoden zur Produktsuche
description: Ein tiefer Einblick in die Konzepte hinter Merchandising-eVars und deren Verarbeitung und Zuordnung von Daten.
source-git-commit: e7bfb56b63a9134728360c91f3c835da1952fa5a
workflow-type: tm+mt
source-wordcount: '549'
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

Um zu demonstrieren, wie diese Variablen festgelegt werden, beginne ich mit einem Beispiel, in dem ein Besucher entscheidet, dass er die interne Keyword-Suche &quot;Sandals&quot;verwendet, um ein Produkt auf der Site zu finden.  Auf der Suchergebnisseite für Suchbegriffe müssen Sie Daten in mindestens zwei eVars erfassen:

* `eVar2` entspricht dem Suchbegriff, der in der Suche verwendet wurde (&quot;Sandals&quot;)
* `eVar1` entspricht der verwendeten Suchmethode für das Produkt (&quot;interne Keyword-Suche&quot;).

Wenn Sie diese beiden Variablen auf diese spezifischen Werte setzen, wissen Sie, dass der Besucher den internen Keyword-Suchbegriff &quot;Sandalen&quot;verwendet, um ein Produkt zu finden.
Gleichzeitig wissen Sie, dass der Besucher nicht die anderen Methoden zur Produktsuche verwendet, um Produkte zu finden (z. B. durchsucht er nicht die Produktkategorien, während er eine Suchbegriffsuche durchführt). Um sicherzustellen, dass eine ordnungsgemäße Zuordnung pro Produkt erfolgt, sollten diese nicht verwendeten Methoden nicht dafür angerechnet werden, ein Produkt zu finden, das über eine interne Keyword-Suche gefunden wurde.  Daher müssen Sie Logik in den Code einfügen (z. B. AppMeasurement, AEP Web SDK usw.) , wodurch die mit diesen anderen Suchmethoden verknüpften eVars automatisch auf einen Wert ohne Suchmethode gesetzt werden.

Wenn ein Benutzer beispielsweise mithilfe des Suchbegriffs &quot;sandals&quot;nach Produkten sucht, sollte die Logik des Analytics-Codes die Variablen auf der Seite mit den internen Suchergebnissen für Suchbegriffe auf die folgenden setzen:

* eVar2=&quot;sandals&quot;: das Keyword &quot;Sandals&quot;in der internen Keyword-Suche verwendet wurde
* eVar1=&quot;Interne Keyword-Suche&quot;: die Suchmethode &quot;Suche nach internen Keywords&quot;verwendet wurde
* eVar3=&quot;Nicht-interne Kampagne&quot;: Es wurde keine interne Kampagne für den Zugriff auf die Suchergebnisseite verwendet.
* eVar4=&quot;non-browse&quot;: Auf der Suchergebnisseite wurde keine Kategorie &quot;Durchsuchen&quot;aufgerufen.
* eVar5=&quot;non-cross-sell&quot;: Auf der Suchergebnisseite wurde kein Link zum Querverkauf angeklickt

