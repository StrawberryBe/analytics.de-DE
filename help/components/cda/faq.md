---
title: Häufig gestellte Fragen zur geräteübergreifenden Analyse
description: Häufig gestellte Fragen zur geräteübergreifenden Analyse
exl-id: 7f5529f6-eee7-4bb9-9894-b47ca6c4e9be
source-git-commit: 7dc97ad5225baf56c829efc8c21b07154bdd8ff9
workflow-type: tm+mt
source-wordcount: '1937'
ht-degree: 98%

---

# Häufig gestellte Fragen

## Wie kann ich die geräteübergreifende Analyse verwenden, um zu sehen, wie Benutzer von einem Gerätetyp zum anderen wechseln?

Sie können eine [!UICONTROL Fluss]-Visualisierung mit der Dimension „Mobilgerätetyp“ verwenden.

1. Melden Sie sich bei Adobe Analytics an und erstellen Sie ein neues leeres Workspace-Projekt.
2. Klicken Sie auf der linken Seite auf die Registerkarte „Visualisierungen“ und ziehen Sie eine Flussvisualisierung in die Arbeitsfläche auf der rechten Seite.
3. Klicken Sie auf die Registerkarte „Komponenten“ auf der linken Seite und ziehen Sie die Dimension „Mobilgerätetyp“ an die mittlere Position mit der Bezeichnung „Dimension oder Element“.
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

## Kann ich sehen, wie Benutzer zwischen verschiedenen Benutzererlebnissen wechseln (z. B. zwischen Desktop-Browser, mobilem Browser und Mobile App)?

Anhand des Beispiels mit dem oben beschriebenen Mobilgerätetyp können Sie sehen, wie Personen zwischen Mobilgerätetypen und Desktop-Gerätetypen wechseln. Desktop-Browser können jedoch nicht von mobilen Browsern unterschieden werden. Wenn Sie diese Information wünschen, können Sie eine benutzerdefinierte Variable erstellen (z. B. eine Prop oder eVar), die aufzeichnet, ob das Erlebnis in einem Desktop-Browser, einem mobilen Browser oder einer Mobile App stattfand. Anschließend können Sie ein Flussdiagramm wie oben beschrieben erstellen, indem Sie die benutzerdefinierte Variable anstelle der Mobilgerätetyp-Dimension verwenden. Durch diese Methode erhalten Sie eine etwas andere Ansicht des geräteübergreifenden Verhaltens.

## Wie weit reicht die Zuordnung der geräteübergreifenden Analyse für Besucher zurück?

Die geräteübergreifende Zuordnung der Cross-Device-Analyse erfolgt in zwei gleichzeitigen Prozessen.

* Das erste Verfahren wird als „Live-Zuordnung“ bezeichnet und läuft ab, wenn die Daten in Adobe Analytics strömen. Während der Live-Zuordnung versucht die Cross-Device-Analyse, die Daten auf Personenebene neu darzustellen. Ist die Person zum Zeitpunkt der Live-Zuordnung jedoch unbekannt, nutzt die Cross-Device-Analyse zur Darstellung der Person die Besucher-ID.

* Der zweite Prozess ist die sogenannte „Wiederholung“. Während der Wiederholung geht die Cross-Device-Analyse in der Zeit zurück und ordnet soweit möglich historische Daten innerhalb eines bestimmten Rückblickfensters neu zu. Dieses Rückblickfenster dauert je nach Konfiguration der Cross-Device-Analyse entweder 1 Tag oder 7 Tage. Während der Wiederholung versucht die Cross-Device-Analyse, Treffer neu darzustellen, bei denen die Person vorher unbekannt war.

* **Bei Verwendung eines Gerätediagramms** bleiben Gerätezuordnungen im Co-op-Diagramm und im privaten Diagramm für ca. 6 Monate bei Adobe erhalten. Eine ECID, die länger als sechs Monate keine Aktivität aufweist, wird aus dem Diagramm entfernt. Bereits in der geräteübergreifenden Analyse zugeordnete Daten sind nicht betroffen, aber nachfolgende Treffer für diese ECID werden als neue Person behandelt.

## Wie behandelt die geräteübergreifende Analyse Treffer mit Zeitstempel?

Adobe behandelt Treffer mit Zeitstempel so, als wären sie zum Zeitpunkt des Zeitstempels eingegangen, nicht zum Zeitpunkt, zu dem Adobe den Treffer erhalten hat. Treffer mit Zeitstempel, die älter als 1 Monat sind, werden nie zugeordnet, da sie außerhalb des Bereichs liegen, den Adobe zum Stitching verwendet.

## Wie unterscheidet sich die geräteübergreifende Analyse von der benutzerspezifischen Besucher-ID?

Die Verwendung der benutzerspezifischen Besucher-ID ist eine veraltete Methode, um [Benutzer geräteübergreifend zu verbinden](/help/implement/js/xdevice-visid/xdevice-connecting.md). Bei einer benutzerspezifischen Besucher-ID verwenden Sie die [`visitorID`](/help/implement/vars/config-vars/visitorid.md)-Variable, um die für die Besucherlogik verwendete ID explizit festzulegen. Die `visitorID`-Variable setzt alle Cookie-basierten IDs außer Kraft, die vorhanden sind.

Benutzerspezifische Besucher-IDs haben mehrere unerwünschte Seiteneffekte, die durch CDA überwunden oder minimiert werden. Beispielsweise verfügt die Methode der benutzerspezifischen Besucher-ID über keine [Wiederholungsfunktionen](replay.md). Wenn sich ein Benutzer während eines Besuchs authentifiziert, wird der erste Teil des Besuchs mit einer anderen Besucher-ID verknüpft als der letzte Teil des Besuchs. Die separaten Besucher-IDs führen zu Besuchs- und Besucherinflation. Die geräteübergreifende Analyse stellt historische Daten erneut dar, sodass nicht authentifizierte Treffer zur richtigen Person gehören.

## Kann ich von der benutzerspezifischen Besucher-ID auf die geräteübergreifende Analyse umsteigen?

Kunden, die bereits eine benutzerdefinierte Besucher-ID verwenden, können auf CDA aktualisieren, ohne dass sich die Implementierung ändert. Die `visitorID`-Variable wird weiterhin in der Quell-Report Suite verwendet. Die geräteübergreifende Analyse ignoriert jedoch die `visitorID`-Variable in der Virtual Report Suite, wenn sich ein Benutzer authentifiziert.

## Wie behandelt das Gerätediagramm gemeinsam genutzte Geräte?

In einigen Situationen ist es möglich, dass sich mehrere Personen von demselben Gerät aus anmelden. Beispiele dafür sind freigegebene Geräte zu Hause, freigegebene PCs in einer Bibliothek oder ein Terminal in einem Einzelhandelsgeschäft.

* **Bei Verwendung eines Gerätediagramms** ist die Handhabung gemeinsam genutzter Geräte eingeschränkt. Das Gerätediagramm verwendet einen Algorithmus, um die Eigentümerschaft eines „Clusters“ zu bestimmen, und kann sich bei jeder Veröffentlichung dieses Clusters ändern. Benutzer des gemeinsam genutzten Geräts unterliegen dem Cluster, zu dem sie gehören.
* **Bei der Verwendung des feldbasierten Stitching** überschreibt die Prop oder eVar, die Sie zur Identifizierung der angemeldeten Benutzer verwenden, andere Kennungen. Gemeinsam genutzte Geräte werden als separate Personen betrachtet, auch wenn sie vom gleichen Gerät stammen.

## Wie behandelt die geräteübergreifende Analyse Situationen, in denen eine einzelne Person über VIELE Geräte/ECIDs verfügt?

In bestimmten Situationen kann ein einzelner Benutzer mit einer großen Anzahl von ECIDs verknüpft sein. Dies kann vorkommen, wenn der Benutzer eine Vielzahl von Browsern oder Apps verwendet, vor allem dann, wenn er häufig Cookies löscht oder den privaten oder Inkognito-Modus des Browsers verwendet.

* **Bei der Verwendung eines Gerätediagramms** wird die Anzahl der ECIDs, die mit einer bestimmten Benutzer-ID verknüpft sind, auf 50 begrenzt. Wenn eine Benutzer-ID mit zu vielen ECIDs verknüpft ist, geht das Gerätediagramm davon aus, dass die Benutzer-ID ungültig ist, und entfernt den mit dieser Benutzer-ID verknüpften Cluster. Die Benutzer-ID wird dann auf eine Blockierungsliste gesetzt, um zu verhindern, dass sie in Zukunft in ein Cluster aufgenommen wird. Das Ergebnis in der Berichterstellung ist, dass diese Benutzer-ID nicht geräteübergreifend zugeordnet wird.
* **Bei der Verwendung des feldbasierten Stitching** ist die Anzahl der Geräte für die Prop/eVar, die Sie zur Identifizierung der angemeldeten Benutzer verwenden, irrelevant. Ein einzelner Benutzer kann zu einer beliebigen Anzahl von Geräten gehören, ohne dass sich dies auf die Fähigkeit der CDA auswirkt, Geräte zuzuordnen.

## Was ist der Unterschied zwischen der Metrik „Personen“ in CDA und der Metrik „Unique Visitors“ außerhalb von CDA?

Die Metriken [Personen](/help/components/metrics/people.md) und [Unique Visitors](/help/components/metrics/unique-visitors.md) zählen einzelne Besucher (Einzelpersonen). Beachten Sie jedoch, dass zwei verschiedene Geräte derselben Person gehören können. Die geräteübergreifende Analyse ordnet die beiden Geräte derselben Person zu, während die zwei Geräte außerhalb der geräteübergreifenden Analyse als zwei separate „Unique Visitors“ erfasst werden.

## Was ist der Unterschied zwischen der Metrik „Eindeutige Geräte“ in CDA und der Metrik „Unique Visitors“ außerhalb von CDA?

Diese beiden Metriken sind in etwa gleich. Unterschiede zwischen diesen beiden Metriken treten auf, wenn:

* Ein gemeinsam genutztes Gerät mehreren Personen zugeordnet wird. In diesem Szenario werden 1 Unique Visitor und mehrere eindeutige Geräte gezählt.
* Ein Gerät sowohl nicht zugeordneten als auch zugeordneten Traffic vom gleichen Besucher aufweist. Beispiel: Ein Browser generiert identifizierten zugeordneten Traffic sowie anonymen historischen Traffic, der nicht zugeordnet wurde. In diesem Fall werden 1 Unique Visitor und 2 eindeutige Geräte gezählt.

Weitere Beispiele und Details zur Funktionsweise finden Sie unter [Eindeutige Geräte](/help/components/metrics/unique-devices.md).

## Kann ich CDA-Metriken über die 2.0 API einbinden?

Ja. Analysis Workspace verwendet die 2.0-API, um Daten von Adobe-Servern anzufordern. Außerdem können Sie API-Aufrufe anzeigen, die Adobe verwendet, um Ihre eigenen Berichte zu erstellen:

1. Wenn Sie sich bei Analysis Workspace angemeldet haben, gehen Sie zu [!UICONTROL Hilfe] > [!UICONTROL Debugger aktivieren].
2. Klicken Sie im gewünschten Bedienfeld auf das Debugging-Symbol und wählen Sie dann die gewünschte Visualisierung und die Uhrzeit der Anfrage aus.
3. Suchen Sie die JSON-Anfrage, die Sie in Ihrem API-Aufruf an Adobe verwenden können.

## Geräteübergreifende Analysen können Unique Visitors einander zuordnen. Können durch diese Metrik Besuche einander zugeordnet werden?

Ja. Wenn eine Person innerhalb des Besuchszeitlimits Ihrer Virtual Report Suite (standardmäßig 30 Minuten) Treffer von zwei verschiedenen Geräten sendet, werden sie demselben Besuch zugeordnet.

## Was ist die ultimative Besucher-ID, die CDA verwendet? Kann ich sie aus Adobe Analytics exportieren?

* **Bei Verwendung eines Gerätediagramms** ist eine benutzerdefinierte ID, die auf ihrem Cluster basiert, die primäre Kennung.
* **Bei Verwendung des feldbasierten Stitching** ist eine benutzerdefinierte ID, die auf der von Ihnen gewählten Eigenschaft/eVar basiert, die primäre Kennung.

Beide diese Kennungen werden von Adobe zum Zeitpunkt der Berichterstellung berechnet. Dies wird auch als [Berichtszeitverarbeitung](../vrs/vrs-report-time-processing.md) bezeichnet. Aufgrund der Art der Berichtszeitverarbeitung ist diese nicht mit Data Warehouse, Daten-Feeds oder anderen Exportfunktionen von Adobe kompatibel.

## Wie kann ich vom Gerätediagramm zum feldbasierten Stitching wechseln oder umgekehrt?

Der Wechsel vom Gerätediagramm zur feldbasierten Zuordnung oder umgekehrt kann über die Kundenunterstützung angefordert werden. Es kann jedoch einige Wochen oder länger dauern, bis ein solcher Wechsel abgeschlossen ist, und *historische zugeordnete Daten aus der vorherigen Methode gehen verloren*.

## Wie geht Adobe mit individuellen Einschränkungen für eine Prop oder eVar um, die beim feldbasierten Stitching verwendet wird?

Die geräteübergreifende Analyse ruft Identifizierungsvariablen-Dimensionselemente ab, bevor sie für das Reporting optimiert werden. Sie müssen sich bei der geräteübergreifenden Analyse keine Sorgen um individuelle Einschränkungen machen. Wenn Sie jedoch versucht haben, diese Prop/eVar in einem Workspace-Projekt zu verwenden, wird weiterhin das Dimensionselement [(Geringer Traffic)](/help/technotes/low-traffic.md) angezeigt.

## Wie viele Report Suites meines Unternehmens können für die geräteübergreifende Analyse aktiviert werden?

Ab dem 1. Mai 2022 ist jede neue Implementierung der geräteübergreifenden Analyse auf maximal drei Report Suite-IDs (RSIDs) pro Kunde beschränkt. Die geräteübergreifende Analyse führt Report Suites nicht zusammen. Jede für die geräteübergreifende Analyse aktivierte Report Suite muss geräteübergreifend sein (mit Daten von mehreren Oberflächen wie Desktop-Web, mobilem Web, App usw.)..

## Wenn meine Experience Cloud-Organisation (auch IMS-Organisation genannt) mehrere Unternehmen in verschiedenen Regionen hat, kann ich dann die geräteübergreifende Analyse für alle Unternehmen aktivieren?

Nein. Innerhalb einer Organisation kann die geräteübergreifende Analyse nur für eine Region aktiviert werden.

## Welche Vor- und Nachteile hat eine Wiederholung über sieben Tage gegenüber einer Wiederholung über einen Tag?

Der Vorteil des siebentägigen Wiederholungs-Lookback-Fensters besteht darin, dass die geräteübergreifende Analyse einen längeren Zeitraum nutzen kann, um zu versuchen, zuvor anonyme Ereignisse mit einer Person zu verknüpfen, die sich später innerhalb dieser sieben Tage angemeldet hat. Die Nachteile des 7-Tage-Lookback-Fensters sind: 1) Wiederholungen werden nur einmal pro Woche ausgeführt, und 2) die letzten sieben Tage können sich ändern.

Die Vorteile der Verwendung des eintägigen Wiederholungs-Lookback-Fensters sind: 1) tägliche Wiederholungsläufe und 2) nur gestern kann sich ändern. Der Nachteil des eintägigen Lookback-Fensters besteht darin, dass die geräteübergreifende Analyse nur einen Tag zurückgehen kann, um zuvor anonyme Ereignisse mit einer Person zu verknüpfen, die sich gestern angemeldet hat.

## Was passiert mit den zugeordneten Daten in meinen Virtual Report Suites für geräteübergreifende Analyse, wenn mein Unternehmen beschließt, ein Downgrade von Analytics Ultimate durchzuführen?

Wenn ein Kunde von Ultimate herabstuft, hat er keinen Zugriff mehr auf zugeordnete Daten. Alle zuvor zugeordneten Daten werden entfernt. Das bedeutet, dass die Virtual Report Suites für geräteübergreifende Analyse jetzt keine geräteübergreifende Zuordnung widerspiegeln. Die Daten ähneln der ursprünglich nicht zugeordneten Report Suite.

## Warum unterscheidet sich die Gesamtzahl der Treffer zwischen meiner ursprünglichen Report Suite und der Virtual Report Suite der geräteübergreifenden Analyse?

Die geräteübergreifende Analyse verwendet eine komplexe parallele Verarbeitungs-Pipeline mit mehreren abhängigen Komponenten. Es wird eine Datenabweichung von etwa 1 % für die Gesamtzahl der Treffer zwischen der ursprünglichen Report Suite und der Virtual Report Suite für die geräteübergreifende Analyse erwartet.

## Warum ist die Metrik „Identifizierte Personen“ überhöht?

Die Metrik „Identifizierte Personen“ kann etwas höher sein, wenn für die Prop//eVar der Kennung eine [Hash-Kollision](/help/implement/validate/hash-collisions.md) besteht.

Bei feldbasiertem Stitching wird bei der benutzerdefinierten Identifizierungsvariablen zwischen Groß- und Kleinschreibung unterschieden. Die Zahl der Metrik „Identifizierte Personen“ kann erheblich höher sein, wenn die Kennungswerte nicht mit der Groß-/Kleinschreibung übereinstimmen. Wenn beispielsweise `bob` und `Bob` gesendet und eigentlich dieselbe Person sind, interpretiert die geräteübergreifende Analyse diese beiden Werte als unterschiedlich.

## Warum sehe ich für die Metrik „Nicht identifizierte Personen“ bei der Anzeige der Prop/eVar der Kennung Werte ungleich null?

Diese Situation tritt normalerweise auf, wenn für einen Besucher im Berichtsfenster sowohl authentifizierte als auch nicht authentifizierte Treffer generiert werden. Der Besucher gehört in der Dimension [Identifikationsstatus](/help/components/dimensions/identified-state.md) sowohl zu „Nicht identifiziert“ als auch zu „Identifiziert“, weshalb nicht identifizierte Treffer einer Kennung zugeordnet werden. Dieses Szenario kann sich nach der Ausführung von [Wiederholen](replay.md) ändern, je nach der Wiederholungshäufigkeit und der Erfolgsrate.