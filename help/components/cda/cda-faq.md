---
title: Häufig gestellte Fragen zur geräteübergreifenden Analyse
description: Häufig gestellte Fragen zur geräteübergreifenden Analyse
translation-type: tm+mt
source-git-commit: f7c2a366b409995c1fe790db97de5c708882ab3d
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 71%

---


# Häufig gestellte Fragen

**Wie kann ich die geräteübergreifende Analyse verwenden, um zu sehen, wie Benutzer von einem Gerätetyp zum anderen wechseln?**

Sie können eine Flussvisualisierung mit der Dimension „Mobilgerätetyp“ verwenden.

1. Melden Sie sich bei Adobe Analytics an und erstellen Sie ein neues leeres Workspace-Projekt.
2. Klicken Sie auf der linken Seite auf die Registerkarte „Visualisierungen“ und ziehen Sie eine Flussvisualisierung in die Arbeitsfläche auf der rechten Seite.
3. Klicken Sie auf die Registerkarte „Komponenten“ auf der linken Seite und ziehen Sie die Dimension „Mobilgerätetyp“ an die mittlere Position mit der Bezeichnung „Dimension oder Element“.
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

**Kann ich sehen, wie Benutzer zwischen verschiedenen Benutzererlebnissen wechseln (z. B. zwischen Desktop-Browser, mobilem Browser und mobiler App)?**

Wenn Sie den Mobilgerätetyp wie oben dargestellt verwenden, können Sie sehen, wie Personen zwischen Mobilgerätetypen und Desktop-Gerätetypen wechseln. Sie sollten jedoch zwischen Desktop-Browsern und mobilen Browsern unterscheiden. Eine Möglichkeit dazu besteht darin, eine eVar zu erstellen, die aufzeichnet, ob das Erlebnis über einen Desktop-Browser, einen mobilen Browser oder die mobile App aufgetreten ist. Erstellen Sie dann ein Flussdiagramm wie oben beschrieben, wobei Sie die eVar „Erlebnis“ anstelle der Dimension „Mobilgerätetyp“ verwenden. Dadurch erhalten Sie eine etwas andere Ansicht des geräteübergreifenden Verhaltens.

**Wie weit reicht die Zuordnung der geräteübergreifenden Analyse für Besucher zurück?**

* Adobe bewahrt Daten zur Gerätezuordnung etwa 30 Tage lang auf. Wenn ein Gerät ursprünglich nicht durch das Co-op-Diagramm oder das Private Diagramm identifiziert wird, aber später innerhalb von 30 Tagen identifiziert wird, legt die geräteübergreifende Analyse rückwirkend fest, dass das Gerät bis zu 30 Tage in der Vergangenheit zu einer identifizierten Person gehört. Wenn ein Teil des nicht identifizierten Verhaltens eines Benutzers außerhalb des 30-Tage-Lookback-Fensters liegt, wird dieser Teil der Journey des Benutzers nicht zugeordnet.
* Adobe bewahrt Gerätezuordnungen im Co-op-Diagramm und im privaten Diagramm für etwa 6 Monate auf. Eine ECID, die länger als sechs Monate keine Aktivität aufweist, wird aus dem Diagramm entfernt. Bereits in der geräteübergreifenden Analyse zugeordnete Daten sind nicht betroffen, aber nachfolgende Treffer für diese ECID werden als neuer Kontakt behandelt.

**Wie behandelt die geräteübergreifende Analyse Treffer mit Zeitstempel?**

Adobe behandelt Treffer mit Zeitstempel so, als wären sie zum Zeitpunkt des Zeitstempels eingegangen, nicht zum Zeitpunkt, zu dem Adobe den Treffer erhalten hat. Treffer mit Zeitstempel, die älter als 1 Monat sind, können nicht zugeordnet werden, da sie außerhalb des Bereichs liegen, in dem Adobe Daten zum Zuordnen aufbewahrt.

**Wie sieht CDA im Vergleich zu benutzerdefinierten Besucher-IDs aus?**

Die [benutzerspezifische Besucher-ID](/help/implement/vars/config-vars/visitorid.md) ist eine veraltete Methode, um [Benutzer geräteübergreifend zu verbinden](/help/implement/js/xdevice-visid/xdevice-connecting.md). Bei einer benutzerspezifischen Besucher-ID verwenden Sie die `s.visitorID`-Variable, um die für die Besucherlogik verwendete ID explizit festzulegen. Die `s.visitorID`-Variable setzt alle Cookie-basierten IDs außer Kraft, die vorhanden sind.

Benutzerspezifische Besucher-IDs haben mehrere unerwünschte Nebenwirkungen, die CDA überwindet oder minimiert. Beispielsweise verfügt die Methode der benutzerspezifischen Besucher-ID über keine Lookback-Funktionen. Wenn sich ein Benutzer während eines Besuchs authentifiziert, wird der erste Teil des Besuchs mit einer anderen Besucher-ID verknüpft als der letzte Teil des Besuchs. Die separaten Besucher-IDs führen zu Besuchs- und Besucherinflation. Das 30-Tage-Lookback-Fenster der geräteübergreifenden Analyse ermöglicht es, rückwirkend festzulegen, dass das bisherige Verhalten zu derselben Person gehört. Das bedeutet, dass unauthentifiziertes geräteübergreifendes Verhalten mit authentifiziertem geräteübergreifenden Verhalten bei keiner oder minimaler Inflation kombiniert wird.

**Kann ich von der benutzerspezifischen Besucher-ID auf die geräteübergreifende Analyse umsteigen?**

Kunden, die bereits eine benutzerspezifische Besucher-ID verwenden, können auf die geräteübergreifende Analyse umsteigen. Die zugrunde liegenden Cookie-basierten IDs in der Basis-Report Suite werden von `s.visitorID` weiterhin außer Kraft gesetzt. Innerhalb der Virtual Report Suite ignoriert die geräteübergreifende Analyse jedoch `s.visitorID` für Geräte, die vom Gerätediagramm identifiziert werden.

**Wie behandelt das Gerätediagramm gemeinsam genutzte Geräte?**

In einigen Situationen ist es möglich, dass sich mehrere Personen von demselben Gerät aus anmelden. Beispiele dafür sind freigegebene Geräte zu Hause, freigegebene PCs in einer Bibliothek oder ein Terminal in einem Einzelhandelsgeschäft. In diesen Fällen wird die ID mit dem Gerätediagramm von diesen gemeinsam genutzten Geräten synchronisiert, was bedeutet, dass mehrere Benutzer im Laufe der Zeit mit diesem Gerät verknüpft sind. Das Gerätediagramm (Co-op-Diagramm oder privates Diagramm) verknüpft die ECID auf diesem Gerät nicht mit einem dieser Benutzer. Stattdessen verknüpft das Diagramm die ECID mit einem „Cluster“, das alle verknüpften Benutzer enthält. Das Diagramm versucht, diesen Cluster so stabil wie möglich zu halten, anstatt die ECID im Laufe der Zeit kontinuierlich zwischen Clustern zu wechseln. Deshalb kann die geräteübergreifende Analyse nicht zwischen einzelnen Benutzern auf einem gemeinsam genutzten Gerät unterscheiden. Alle Benutzer des gemeinsam genutzten Geräts werden innerhalb der geräteübergreifenden Analyse als eine einzige „Person“ betrachtet.

**Wie behandelt das Gerätediagramm Situationen, in denen eine einzelne Person über VIELE Geräte/ECIDs verfügt?**

In bestimmten Situationen kann ein einzelner Benutzer mit einer großen Anzahl von ECIDs verknüpft sein. Dies kann vorkommen, wenn der Benutzer eine Vielzahl von Browsern oder Apps verwendet, vor allem dann, wenn er häufig Cookies löscht oder den privaten oder Inkognito-Modus des Browsers verwendet. Das Gerätediagramm begrenzt die Anzahl der ECIDs, die mit einer bestimmten Benutzer-ID verknüpft sind, auf 200. Wenn eine Benutzer-ID mit zu vielen ECIDs verknüpft ist, geht das Gerätediagramm davon aus, dass die Benutzer-ID ungültig ist, und entfernt den mit dieser Benutzer-ID verknüpften Cluster. Die Benutzer-ID wird dann zu einer Blocklist hinzugefügt, um zu verhindern, dass sie in Zukunft in einem Cluster zusammengefasst wird. Das Ergebnis in der geräteübergreifenden Analyse ist, dass das Verhalten der Benutzer-ID nicht geräteübergreifend zugeordnet wird.

**Was ist der Unterschied zwischen der Metrik &quot;Personen&quot;in CDA und der Metrik &quot;Individuelle Besucher&quot;außerhalb von CDA?**

Die Metrik &quot;Personen&quot;ähnelt der Metrik &quot;Individuelle Besucher&quot;insofern, als sie die Anzahl der Einzelpersonen angibt. Bei der Verwendung von geräteübergreifender Analyse werden individuelle Besucher jedoch kombiniert, wenn sie ansonsten als zwei separate eindeutige Besucher außerhalb von CDA aufgezeichnet werden. Die Metrik &quot;Personen&quot;ersetzt die Metrik &quot;Individuelle Besucher&quot;, wenn &quot;Geräteübergreifende Analyse&quot;aktiviert ist.

**Was ist der Unterschied zwischen der Metrik &quot;Unique Devices&quot;in CDA und der Metrik &quot;Unique Besuchers&quot;außerhalb von CDA?**

Diese beiden Metriken sind in etwa gleich.

**Kann ich CDA-Metriken mit der 2.0-API einbeziehen?**

Ja. Analyse Workspace verwendet die 2.0-API, um Daten von Adobe-Servern anzufordern, und Sie können API-Aufrufe Ansicht verwenden, um Ihre eigenen Berichte zu erstellen:

1. Wenn Sie sich bei Analyse Workspace angemeldet haben, öffnen Sie die Entwicklerwerkzeuge Ihres Browsers (F12 für die meisten Browser).
1. Geben Sie in die Browser-Konsole `adobeTools.showDebugger()`ein. Die Seite wird mit Debugging-Symbolen in der oberen rechten Ecke jedes Bedienfelds neu geladen.
1. Klicken Sie im gewünschten Bereich auf das Debugging-Symbol und wählen Sie dann die gewünschte Visualisierung und die Uhrzeit der Anforderung aus.
1. Suchen Sie die JSON-Anforderung, die Sie in Ihrem API-Aufruf an Adobe verwenden können.

**Geräteübergreifende Analysen können individuelle Besucher miteinander verbinden. Kann sie die Besuche zusammenhalten?**

Ja. Wenn eine Einzelperson Treffer von zwei verschiedenen Geräten innerhalb des Timeouts für Besuche Ihrer Virtual Report Suite sendet (standardmäßig 30 Minuten), werden diese in denselben Besuch eingefügt.

**Was ist die ultimative Besucher-ID, die CDA verwendet? Kann ich es aus Adobe Analytics exportieren?**

Geräteübergreifende Analysen berechnen geheftete Daten mit einer &quot;Cluster-ID&quot;. Diese Kennung wird von Adobe zum Zeitpunkt der Ausführung des Berichts berechnet, auch als Berichtszeitverarbeitung bezeichnet. Die Art der Berichtszeitverarbeitung bedeutet, dass diese nicht mit Data Warehouse, Data Feeds oder anderen Exportfunktionen von Adobe-Angeboten kompatibel ist.
