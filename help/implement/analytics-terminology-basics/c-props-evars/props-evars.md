---
description: Benutzerdefinierte Traffic-Variablen – auch als „props“ (s.prop) oder „Eigenschaftsvariablen“ bezeichnet – sind Zähler, die zählen, wie oft jeder Wert zu Analytics gesendet wird.
keywords: Analytics Implementation;Traffic prop;prop;conversion;evar;s.prop;custom conversion insight;traffic variable
title: Übersicht über Eigenschaften und eVars
topic: Developer and implementation
uuid: 522cab2b-1ef8-4f10-b216-c82b21431487
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Übersicht über Eigenschaften und eVars

Benutzerdefinierte Traffic-Variablen – auch als „props“ (s.prop) oder „Eigenschaftsvariablen“ bezeichnet – sind Zähler, die zählen, wie oft jeder Wert zu Analytics gesendet wird.

Wenn Sie sich mit der Zuweisung von Variablen beschäftigen, müssen Sie wissen, wie sich die Funktionen von Props und eVars unterscheiden. Wenn Ihre Organisation mit diesen Unterschieden vertraut ist, kann sie die optimale Verwendung dieser Variablen festlegen. Weitere Informationen finden Sie unter [Props und eVars im Vergleich](/help/implement/analytics-terminology-basics/c-props-evars/props-vs-evars.md).

Mithilfe von Eigenschaftsvariablen können Sie benutzerdefinierte Daten mit bestimmten Traffic-bezogenen Ereignissen in Verbindung setzen. Die Eigenschaftsvariablen sind im [!DNL Analytics]-Code auf jeder Seite Ihrer Website eingebettet. Über [!UICONTROL s.prop]-Variablen können Sie in [!DNL Analytics] benutzerdefinierte Berichte erstellen, die speziell auf Ihre Organisation, Branche und geschäftlichen Ziele ausgerichtet sind.

So kann ein Automobilhersteller zum Beispiel daran interessiert sein, dass in seinem „Seiten“-Bericht auch ein Punkt namens „Beliebtestes Automodell“ aufgeführt wird. Dies wird möglich, indem Sie eine unserer Traffic-Eigenschaften für die Darstellung des Automodells vorsehen. Anschließend implementieren Sie Code, der auf den entsprechenden Seiten das Automodell übergibt.

> [!NOTE] [!DNL Analytics] unterstützt maximal 75 [!UICONTROL s.prop]-Variablen.

Eigenschaftsvariablen werden in Pfadsetzungsberichten und Korrelationsberichten verwendet. So können [!UICONTROL Eigenschaftsvariablen] zum Beispiel eingesetzt werden, um den Content-Typ, Unterbereiche oder Vorlagennamen anzuzeigen. In den resultierenden Berichten zum [!UICONTROL Benutzerspezifischen Datenverkehr] wird dann angegeben, welcher Content-Typ, Unterabschnitt oder welche Vorlage am häufigsten angezeigt wird.

Je nachdem, was für Daten über benutzerspezifische Traffic-Variablen auf der Website erfasst werden, können die unterschiedlichsten geschäftlichen Fragen beantwortet werden. Dazu gehören zum Beispiel:

* Einblicke in die Navigation von Besuchern auf der Website
* Einblicke in das interne Suchverhalten von Benutzern
* Segmentierung des Datenverkehrs nach der Navigation oder der Kategorie
* Segmentierung des Besucherverhaltens nach demografischen Aspekten

Mithilfe von eVars (oder [!UICONTROL benutzerspezifischer Konversion Insight]-Variablen) können Sie erkennen, wie sehr bestimmte Attribute oder Aktionen zu Erfolgsereignissen auf Ihrer Site beitragen. So können eVars bei einer Medien-Website zum Beispiel verwendet werden, um festzustellen, wie viel interne Werbeaktionen dazu beitragen, dass sich Benutzer registrieren. Wenn ein Besucher auf die interne Werbeaktion klickt, kann ein eindeutiger Bezeichner für diese Werbeaktion in einer eVar gespeichert werden. Wenn dieser Besucher seine Registrierung abgeschlossen hat und ein Erfolgsereignis ausgelöst wird, erhält der eindeutige Bezeichner eine Gutschrift für das Registrierungsereignis.

In einer Konversions-Site kann mittels eVars verfolgt werden, wie sich angemeldete Besucher im Vergleich zu nicht angemeldeten Besuchern beim Tätigen von Einkäufen verhalten. Wenn sich ein Besucher anmeldet, wird in einer eVar der Wert „angemeldet“ festgelegt. Wenn der Besucher die Checkout-Seite erreicht, wird das Checkout-Ereignis dem „angemeldet“-Wert zugerechnet. Wenn einem Besucher nach einem Kauf die „Vielen Dank“-Seite angezeigt wird, werden die Produkte und Kaufbeträge dem „angemeldet“-Wert zugeschrieben. Im resultierenden [!UICONTROL Custom eVar]-Bericht wird die Gesamtanzahl der Checkouts und Bestellungen zu Besuchern vom Typ „angemeldet“ und „nicht angemeldet“ angezeigt.

Weitere Informationen finden Sie unter [Traffic-Variable](https://marketing.adobe.com/resources/help/en_US/reference/traffic_var.html) in der Analytics-Hilfe und -Referenz.

Informationen zum Einrichten von Eigenschaften in Digital Tag Management finden Sie unter [Webeigenschaft erstellen](/help/implement/c-implement-with-dtm/t-create-web-property.md).
