---
title: Häufig gestellte Fragen zur geräteübergreifenden Analyse
description: Häufig gestellte Fragen zur geräteübergreifenden Analyse
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '1301'
ht-degree: 52%

---


# Häufig gestellte Fragen

## Wie kann ich die geräteübergreifende Analyse verwenden, um zu sehen, wie Benutzer von einem Gerätetyp zum anderen wechseln?

Sie können eine Flussvisualisierung mit der Dimension „Mobilgerätetyp“ verwenden.

1. Melden Sie sich bei Adobe Analytics an und erstellen Sie ein neues leeres Workspace-Projekt.
2. Klicken Sie auf der linken Seite auf die Registerkarte „Visualisierungen“ und ziehen Sie eine Flussvisualisierung in die Arbeitsfläche auf der rechten Seite.
3. Klicken Sie auf die Registerkarte „Komponenten“ auf der linken Seite und ziehen Sie die Dimension „Mobilgerätetyp“ an die mittlere Position mit der Bezeichnung „Dimension oder Element“.
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

## Kann ich sehen, wie Benutzer zwischen verschiedenen Benutzererlebnissen wechseln (z. B. zwischen Desktop-Browser, mobilem Browser und mobiler App)?

Wenn Sie den Mobilgerätetyp wie oben dargestellt verwenden, können Sie sehen, wie Personen zwischen Mobilgerätetypen und Desktop-Gerätetypen wechseln. Sie sollten jedoch zwischen Desktop-Browsern und mobilen Browsern unterscheiden. Eine Möglichkeit dazu besteht darin, eine eVar zu erstellen, die aufzeichnet, ob das Erlebnis über einen Desktop-Browser, einen mobilen Browser oder die mobile App aufgetreten ist. Erstellen Sie dann ein Flussdiagramm wie oben beschrieben, wobei Sie die eVar „Erlebnis“ anstelle der Dimension „Mobilgerätetyp“ verwenden. Dadurch erhalten Sie eine etwas andere Ansicht des geräteübergreifenden Verhaltens.

## Wie weit reicht die Zuordnung der geräteübergreifenden Analyse für Besucher zurück?

Adobe bewahrt Daten zur Gerätezuordnung etwa 30 Tage lang auf. Wird ein Gerät ursprünglich nicht identifiziert, wird es später jedoch innerhalb von 30 Tagen identifiziert, geht die CDA zurück und weist darauf hin, dass das Gerät bis zu 30 Tage in der Vergangenheit zu einer identifizierten Person gehört. Wenn ein Teil des nicht identifizierten Verhaltens eines Benutzers außerhalb des 30-Tage-Lookback-Fensters liegt, wird dieser Teil der Journey des Benutzers nicht zugeordnet.

* **Bei Verwendung eines Gerätediagramms** behält Adobe Gerätezuordnungen im Co-op-Diagramm und im privaten Diagramm für etwa 6 Monate bei. Eine ECID, die länger als sechs Monate keine Aktivität aufweist, wird aus dem Diagramm entfernt. Daten, die bereits in CDA zusammengefügt wurden, sind davon nicht betroffen, aber nachfolgende Zugriffe auf diese ECID werden als neue Person behandelt.

## Wie behandelt die geräteübergreifende Analyse Treffer mit Zeitstempel?

Adobe behandelt Treffer mit Zeitstempel so, als wären sie zum Zeitpunkt des Zeitstempels eingegangen, nicht zum Zeitpunkt, zu dem Adobe den Treffer erhalten hat. Treffer mit Zeitstempel, die älter als 1 Monat sind, werden nie zugeschnitten, da sie außerhalb des von Adobe für das Heften verwendeten Bereichs liegen.

## Wie unterscheidet sich die geräteübergreifende Analyse von der benutzerspezifischen Besucher-ID?

Using a custom visitor ID is a legacy method to [connect users across devices](/help/implement/js/xdevice-visid/xdevice-connecting.md). Bei einer benutzerspezifischen Besucher-ID verwenden Sie die [`visitorID`](/help/implement/vars/config-vars/visitorid.md)-Variable, um die für die Besucherlogik verwendete ID explizit festzulegen. Die `visitorID`-Variable setzt alle Cookie-basierten IDs außer Kraft, die vorhanden sind.

Benutzerspezifische Besucher-IDs haben mehrere unerwünschte Seiteneffekte, die durch CDA überwunden oder minimiert werden. For example, the custom visitor ID methodology has no [replay](replay.md) capabilities. Wenn sich ein Benutzer während eines Besuchs authentifiziert, wird der erste Teil des Besuchs mit einer anderen Besucher-ID verknüpft als der letzte Teil des Besuchs. Die separaten Besucher-IDs führen zu Besuchs- und Besucherinflation. CDA stellt historische Daten wieder her, sodass nicht authentifizierte Treffer zur richtigen Person gehören.

## Kann ich von der benutzerspezifischen Besucher-ID auf die geräteübergreifende Analyse umsteigen?

Kunden, die bereits benutzerdefinierte Besucher-ID verwenden, können auf CDA aktualisieren, ohne dass sich die Implementierung ändert. Die `visitorID` Variable wird weiterhin in der Quell-Report Suite verwendet. CDA ignoriert jedoch die `visitorID` Variable in der Virtual Report Suite, wenn sich ein Benutzer authentifiziert.

## Wie behandelt das Gerätediagramm gemeinsam genutzte Geräte?

In einigen Situationen ist es möglich, dass sich mehrere Personen von demselben Gerät aus anmelden. Beispiele dafür sind freigegebene Geräte zu Hause, freigegebene PCs in einer Bibliothek oder ein Terminal in einem Einzelhandelsgeschäft.

* **Bei Verwendung eines Gerätediagramms** ist die Handhabung freigegebener Geräte eingeschränkt. Das Gerätediagramm verwendet einen Algorithmus, um das Eigentum an einem &quot;Cluster&quot;zu bestimmen, und kann sich bei jeder Veröffentlichung dieses Clusters ändern. Benutzer des freigegebenen Geräts unterliegen dem Cluster, zu dem sie gehören.
* **Bei der Verwendung der feldbasierten Suche**&#x200B;überschreibt die Eigenschaft oder eVar, die Sie zur Identifizierung der angemeldeten Benutzer verwenden, andere Bezeichner. Freigegebene Geräte werden als separate Personen betrachtet, auch wenn sie vom gleichen Gerät stammen.

## Wie behandelt CDA Situationen, in denen eine einzelne Person über viele Geräte/ECIDs verfügt?

In bestimmten Situationen kann ein einzelner Benutzer mit einer großen Anzahl von ECIDs verknüpft sein. Dies kann vorkommen, wenn der Benutzer eine Vielzahl von Browsern oder Apps verwendet, vor allem dann, wenn er häufig Cookies löscht oder den privaten oder Inkognito-Modus des Browsers verwendet.

* **Bei Verwendung eines Gerätediagramms** wird bei CDA die Anzahl der ECIDs, die mit einer bestimmten Benutzer-ID verknüpft sind, auf 50 begrenzt. Wenn eine Benutzer-ID zu vielen ECIDs zugeordnet ist, geht das Gerätediagramm davon aus, dass die Benutzer-ID ungültig ist, und entfernt den mit dieser Benutzer-ID verknüpften Cluster. Die Benutzer-ID wird dann einer Blockierungsliste hinzugefügt, um zu verhindern, dass sie in Zukunft zu Clustern hinzugefügt wird. Das führt zum Berichte, dass die Benutzer-ID nicht geräteübergreifend verknüpft ist.
* **Bei der Verwendung der feldbasierten Suche** ist die Anzahl der Geräte für die Eigenschaftsvariable/eVar, die Sie zur Identifizierung der angemeldeten Benutzer verwenden, irrelevant. Ein einzelner Benutzer kann zu einer beliebigen Anzahl von Geräten gehören, ohne dass sich dies auf die Fähigkeit von CDA auswirkt, Geräte anzuheften.

## Was ist der Unterschied zwischen der Metrik &quot;Personen&quot;in CDA und der Metrik &quot;Individuelle Besucher&quot;außerhalb von CDA?

The [People](/help/components/metrics/people.md) metric is similar to the [Unique Visitors](/help/components/metrics/unique-visitors.md) metric in that it reports on the number of unique individuals. Bei der Verwendung der geräteübergreifenden Analyse werden Unique Visitors jedoch kombiniert, wenn sie ansonsten als zwei separate Unique Visitors außerhalb von CDA aufgezeichnet werden. Die Metrik „Personen“ ersetzt die Metrik „Unique Visitors“, wenn geräteübergreifende Analyse aktiviert ist.

## Was ist der Unterschied zwischen der Metrik „Eindeutige Geräte“ in CDA und der Metrik „Unique Visitors“ außerhalb von CDA?

Diese beiden Metriken sind in etwa gleich.

## Kann ich CDA-Metriken über die 2.0 API einbinden?

Ja. Analysis Workspace verwendet die 2.0-API, um Daten von Adobe-Servern anzufordern. Außerdem können Sie API-Aufrufe anzeigen, die Adobe verwendet, um Ihre eigenen Berichte zu erstellen:

1. Wenn Sie sich bei Analysis Workspace angemeldet haben, gehen Sie zu [!UICONTROL Hilfe] > Debugger [!UICONTROL aktivieren].
2. Klicken Sie im gewünschten Bedienfeld auf das Debugging-Symbol und wählen Sie dann die gewünschte Visualisierung und die Uhrzeit der Anfrage aus.
3. Suchen Sie die JSON-Anfrage, die Sie in Ihrem API-Aufruf an Adobe verwenden können.

## Geräteübergreifende Analysen können Unique Visitors einander zuordnen. Können Besuche einander zugeordnet werden?

Ja. Wenn eine Person innerhalb des Besuchszeitlimits Ihrer Virtual Report Suite (standardmäßig 30 Minuten) Treffer von zwei verschiedenen Geräten sendet, werden sie demselben Besuch zugeordnet.

## Was ist die ultimative Besucher-ID, die CDA verwendet? Kann ich sie aus Adobe Analytics exportieren?

* **Bei Verwendung eines Gerätediagramms** ist eine benutzerdefinierte ID, die auf ihrem Cluster basiert, der primäre Bezeichner.
* **Bei Verwendung der feldbasierten Suche** ist eine benutzerdefinierte ID, die auf der von Ihnen gewählten prop/eVar basiert, der primäre Bezeichner.

Beide Bezeichner werden von Adobe zum Zeitpunkt der Ausführung des Berichts berechnet, auch als [Berichtszeitverarbeitung](../vrs/vrs-report-time-processing.md)bezeichnet. Die Art der Berichtszeitverarbeitung bedeutet, dass sie nicht mit Data warehouse, Datenfeeds oder anderen Exportfunktionen kompatibel ist, die von Adobe Angebot ausgeführt werden.

## Wie kann ich vom Gerätediagramm zum field-basierten Stiching wechseln oder umgekehrt?

Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, wenn Sie zwischen den CDA-Identifizierungsmethoden wechseln möchten. Der Kundenbetreuer kann Ihre Report Suite nach der gewünschten Methode zur Identifizierung von Personen bereitstellen. *Historische Daten aus der vorherigen Methode gehen verloren.*

## Wie geht Adobe mit eindeutigen Beschränkungen für eine eVar um, die bei der field-basierten Suche verwendet wird?

CDA ruft eVar-Dimensionselemente ab, bevor sie für den Berichte optimiert werden. Sie müssen sich keine Sorgen um eindeutige Beschränkungen für CDA machen. Wenn Sie jedoch versucht haben, diese prop/eVar in einem Workspace-Projekt zu verwenden, können Sie weiterhin das Dimensionselement [(geringer Traffic)](/help/technotes/low-traffic.md) sehen.
