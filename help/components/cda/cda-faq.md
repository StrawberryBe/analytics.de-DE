---
title: Häufig gestellte Fragen zur geräteübergreifenden Analyse
description: Häufig gestellte Fragen zu geräteübergreifenden Analysen
translation-type: tm+mt
source-git-commit: e7a78c2ac21042f57487c1c230e1c96318810429

---


# Häufig gestellte Fragen

> [!NOTE] Die Dokumentation zu geräteübergreifenden Analysen kann sich ändern, wenn die Funktion weiterentwickelt wird. Suchen Sie regelmäßig nach Updates.

**Wie kann ich CDA verwenden, um zu sehen, wie Menschen von einem Gerätetyp zum anderen wechseln?**

Sie können eine Flussvisualisierung mit der Dimension "Mobilgerätetyp"verwenden.

1. Melden Sie sich bei Adobe Analytics an und erstellen Sie ein neues leeres Workspace-Projekt.
2. Klicken Sie auf der linken Seite auf die Registerkarte Visualisierungen und ziehen Sie eine Flussvisualisierung auf die Arbeitsfläche auf der rechten Seite.
3. Klicken Sie auf die Registerkarte Komponenten auf der linken Seite und ziehen Sie die Dimension "Mobilgerätetyp"an die mittlere Position mit der Bezeichnung "Dimension oder Element".
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

**Kann ich sehen, wie sich die Benutzer zwischen verschiedenen Benutzererlebnissen bewegen (z. B. Desktop-Browser im Vergleich zum mobilen Browser oder zur mobilen App)?**

Wenn Sie den Mobilgerätetyp wie oben dargestellt verwenden, können Sie sehen, wie sich Personen zwischen Mobilgerätetypen und Desktop-Gerätetypen bewegen. Sie sollten jedoch Desktop-Browser und mobile Browser unterscheiden. Eine Möglichkeit dazu besteht darin, eine eVar zu erstellen, die aufzeichnet, ob das Erlebnis in einem Desktop-Browser, mobilen Browser oder mobilen App aufgetreten ist. Erstellen Sie dann ein Flussdiagramm wie oben beschrieben, wobei Sie die eVar "Erlebnis"anstelle der Dimension "Mobilgerätetyp"verwenden. Dies bietet eine etwas andere Ansicht zum geräteübergreifenden Verhalten.

**Wie weit führt CDA Besucher zurück?**

* Adobe bewahrt Daten zur Gerätezuordnung etwa 30 Tage lang auf. Wenn ein Gerät ursprünglich nicht durch das Co-op-Diagramm oder das Private Diagramm identifiziert wird, aber später innerhalb von 30 Tagen identifiziert wird, geht CDA zurück und weist darauf hin, dass das Gerät bis zu 30 Tage in der Vergangenheit zu einer identifizierten Person gehört. Wenn ein Teil des nicht identifizierten Verhaltens eines Benutzers außerhalb des 30-Tage-Lookback-Fensters liegt, wird dieser Teil der Reise des Benutzers nicht verknüpft.
* Adobe bewahrt Gerätezuordnungen im Co-op-Diagramm und im privaten Diagramm für etwa 6 Monate auf. Eine ECID, die länger als sechs Monate keine Aktivität hat, wird aus dem Diagramm entfernt. Bereits in CDA erfasste Daten sind nicht betroffen, aber nachfolgende Zugriffe auf diese ECID werden als neue Person behandelt.

**Wie behandelt CDA Treffer mit Zeitstempel?**

Adobe behandelt Treffer mit Zeitstempel so, als wären sie zum Zeitpunkt des Zeitstempels eingegangen, nicht zum Zeitpunkt, zu dem Adobe den Treffer erhalten hat. Treffer mit Zeitstempel, die älter als 1 Monat sind, können nicht zugeordnet werden, da sie außerhalb des Bereichs liegen, in dem Adobe Daten zum Verbinden verwendet.

**Wie sieht CDA im Vergleich zur benutzerdefinierten Besucher-ID aus?**

[Die benutzerspezifische Besucher-ID](../../implement/js-implementation/c-unique-visitors/visid-custom.md) ist eine alte Methode, um Benutzer geräteübergreifend zu [verbinden](../../implement/js-implementation/xdevice-visid/xdevice-connecting.md). Bei einer benutzerdefinierten Besucher-ID verwenden Sie die `s.visitorID` Variable, um die für die Besucherlogik verwendete ID explizit festzulegen. Die `s.visitorID` Variable setzt alle Cookie-basierten IDs außer Kraft, die vorhanden sind. Weitere Informationen finden Sie unter [Identifizieren Sie individuelle Besucher](../../implement/js-implementation/c-unique-visitors/visid-overview.md) im Implementierungs-Benutzerhandbuch.

Benutzerspezifische Besucher-IDs haben eine Reihe unerwünschter Nebenwirkungen, die CDA vermeiden oder minimieren soll. Beispielsweise verfügt die Methode der benutzerdefinierten Besucher-ID über keine Lookback-Funktionen. Wenn sich ein Benutzer während eines Besuchs authentifiziert, verknüpft der erste Teil des Besuchs mit einer anderen Besucher-ID als der letzte Teil des Besuchs. Die separaten Besucher-IDs führen zu Besuchs- und Besucherinflation. Das 30-Tage-Lookback-Fenster von CDA ermöglicht es, das bisherige Verhalten als zu derselben Person gehörend zu vergleichen und das Verhalten von nicht authentifiziertem geräteübergreifendem Verhalten mit authentifiziertem geräteübergreifendem Verhalten mit einer Nullrate oder einer minimalen Inflation zu verbinden.

**Kann ich von der benutzerdefinierten Besucher-ID auf die CDA aktualisieren?**

Kunden, die bereits eine benutzerdefinierte Besucher-ID verwenden, können auf CDA aktualisieren. Die zugrunde liegenden Cookie-basierten IDs in der Basis-Report Suite werden `s.visitorID` weiterhin außer Kraft gesetzt. Innerhalb der Virtual Report Suite wird CDA jedoch `s.visitorID` für Geräte ignoriert, die vom Gerätediagramm identifiziert werden.

**Wie behandelt das Gerätediagramm freigegebene Geräte?**

In einigen Situationen ist es möglich, dass sich mehrere Personen von demselben Gerät aus anmelden. Beispiele sind ein freigegebenes Gerät zu Hause, freigegebene PCs in einer Bibliothek oder ein Kiosk in einer Verkaufsstelle. In diesen Fällen zeigt die ID an, dass mit dem Gerätediagramm von diesen freigegebenen Geräten mehrere Benutzer mit der Zeit verknüpft sind. Das Gerätediagramm (Co-op oder Private Graph) verknüpft die ECID auf diesem Gerät nicht mit einem dieser Benutzer. Stattdessen verknüpft das Diagramm die ECID mit einem "Cluster", das alle zugehörigen Benutzer enthält. Das Diagramm versucht, diesen Cluster so stabil wie möglich zu halten, anstatt die ECID im Laufe der Zeit kontinuierlich zwischen Clustern zu wechseln. Deshalb kann CDA nicht zwischen einzelnen Benutzern auf einem freigegebenen Gerät unterscheiden. Alle Benutzer des freigegebenen Geräts werden innerhalb der CDA als eine einzige "Person"betrachtet.

**Wie behandelt das Gerätediagramm Situationen, in denen eine einzelne Person über VIELE Geräte/ECIDs verfügt?**

In bestimmten Situationen kann ein einzelner Benutzer eine große Anzahl von ECIDs verknüpfen. Dies kann vorkommen, wenn der Benutzer eine Vielzahl von Browsern oder Apps verwendet, und sich verschärfen, wenn er häufig Cookies löscht oder den privaten oder inkognito-Browsing-Modus des Browsers verwendet. Das Gerätediagramm zeichnet die Anzahl der ECIDs auf, die mit einer bestimmten Benutzer-ID mit 200 verknüpft sind. Wenn eine Benutzer-ID zu vielen ECIDs zugeordnet ist, geht das Gerätediagramm davon aus, dass die Benutzer-ID ungültig ist, und entfernt den mit dieser Benutzer-ID verknüpften Cluster. Die Benutzer-ID wird dann auf der schwarzen Liste aufgeführt, sodass sie künftig nicht mehr in den Cluster aufgenommen werden kann. Das Ergebnis bei CDA ist, dass das Verhalten der Benutzer-ID nicht geräteübergreifend verknüpft ist.
