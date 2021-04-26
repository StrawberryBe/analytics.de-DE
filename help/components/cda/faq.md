---
title: Häufig gestellte Fragen zur geräteübergreifenden Analyse
description: Häufig gestellte Fragen zur geräteübergreifenden Analyse
exl-id: 7f5529f6-eee7-4bb9-9894-b47ca6c4e9be
translation-type: tm+mt
source-git-commit: 60856c2c410d7b45ba54d1ae7bdd659d181965ff
workflow-type: tm+mt
source-wordcount: '1672'
ht-degree: 81%

---

# Häufig gestellte Fragen

## Wie kann ich die geräteübergreifende Analyse verwenden, um zu sehen, wie Benutzer von einem Gerätetyp zum anderen wechseln?

Sie können eine Visualisierung [!UICONTROL Fluss] mit der Dimension Mobilgerätetyp verwenden.

1. Melden Sie sich bei Adobe Analytics an und erstellen Sie ein neues leeres Workspace-Projekt.
2. Klicken Sie auf der linken Seite auf die Registerkarte „Visualisierungen“ und ziehen Sie eine Flussvisualisierung in die Arbeitsfläche auf der rechten Seite.
3. Klicken Sie auf die Registerkarte „Komponenten“ auf der linken Seite und ziehen Sie die Dimension „Mobilgerätetyp“ an die mittlere Position mit der Bezeichnung „Dimension oder Element“.
4. Dieser Flussbericht ist interaktiv. Klicken Sie auf einen der Werte, um den Fluss auf nachfolgende oder vorherige Seiten zu erweitern. Verwenden Sie das Kontextmenü, um Spalten zu erweitern oder zu reduzieren. Im selben Flussbericht können auch verschiedene Dimensionen verwendet werden.

## Kann ich sehen, wie Benutzer zwischen verschiedenen Benutzererlebnissen wechseln (z. B. zwischen Desktop-Browser, mobilem Browser und mobiler App)?

Wenn Sie den Mobilgerätetyp wie oben dargestellt verwenden, können Sie sehen, wie Personen zwischen Mobilgerätetypen und Desktop-Gerätetypen wechseln. Sie sollten jedoch zwischen Desktop-Browsern und mobilen Browsern unterscheiden. Eine Möglichkeit dazu besteht darin, eine eVar zu erstellen, die aufzeichnet, ob das Erlebnis über einen Desktop-Browser, einen mobilen Browser oder die Mobile App aufgetreten ist. Erstellen Sie dann ein Flussdiagramm wie oben beschrieben, wobei Sie die eVar „Erlebnis“ anstelle der Dimension „Mobilgerätetyp“ verwenden. Dadurch erhalten Sie eine etwas andere Ansicht des geräteübergreifenden Verhaltens.

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
* **Bei der Verwendung des feldbasierten Stitching** überschreibt die Eigenschaft oder eVar, die Sie zur Identifizierung der angemeldeten Benutzer verwenden, andere Kennungen. Gemeinsam genutzte Geräte werden als separate Personen betrachtet, auch wenn sie vom gleichen Gerät stammen.

## Wie behandelt die geräteübergreifende Analyse Situationen, in denen eine einzelne Person über VIELE Geräte/ECIDs verfügt?

In bestimmten Situationen kann ein einzelner Benutzer mit einer großen Anzahl von ECIDs verknüpft sein. Dies kann vorkommen, wenn der Benutzer eine Vielzahl von Browsern oder Apps verwendet, vor allem dann, wenn er häufig Cookies löscht oder den privaten oder Inkognito-Modus des Browsers verwendet.

* **Bei der Verwendung eines Gerätediagramms** wird die Anzahl der ECIDs, die mit einer bestimmten Benutzer-ID verknüpft sind, auf 50 begrenzt. Wenn eine Benutzer-ID mit zu vielen ECIDs verknüpft ist, geht das Gerätediagramm davon aus, dass die Benutzer-ID ungültig ist, und entfernt den mit dieser Benutzer-ID verknüpften Cluster. Die Benutzer-ID wird dann auf eine Blockierungsliste gesetzt, um zu verhindern, dass sie in Zukunft in ein Cluster aufgenommen wird. Das Ergebnis in der Berichterstellung ist, dass diese Benutzer-ID nicht geräteübergreifend zugeordnet wird.
* **Bei der Verwendung des feldbasierten Stitching** ist die Anzahl der Geräte für die Prop/eVar, die Sie zur Identifizierung der angemeldeten Benutzer verwenden, irrelevant. Ein einzelner Benutzer kann zu einer beliebigen Anzahl von Geräten gehören, ohne dass sich dies auf die Fähigkeit der CDA auswirkt, Geräte zuzuordnen.

## Was ist der Unterschied zwischen der Metrik „Personen“ in CDA und der Metrik „Unique Visitors“ außerhalb von CDA?

Die Metrik [Personen](/help/components/metrics/people.md) ähnelt der Metrik [Unique Visitors](/help/components/metrics/unique-visitors.md) insofern, als sie die Anzahl der eindeutigen Einzelpersonen angibt. Bei der Verwendung der geräteübergreifenden Analyse werden Unique Visitors jedoch kombiniert, wenn sie ansonsten als zwei separate Unique Visitors außerhalb von CDA aufgezeichnet werden. Die Metrik „Personen“ ersetzt die Metrik „Unique Visitors“, wenn Cross-Device Analytics aktiviert ist. Es steht eine neue Metrik ([Individuelle Geräte](/help/components/metrics/unique-devices.md)) zur Verfügung, die außerhalb von Cross-Device Analytics ungefähr „Unique Visitors“ gleicht.

## Was ist der Unterschied zwischen der Metrik „Unique Devices“ in CDA und der Metrik „Unique Visitors“ außerhalb von CDA?

Diese beiden Metriken sind in etwa gleich.

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

Wenden Sie sich an den Account Manager Ihres Unternehmens, wenn Sie zwischen den Identifizierungsmethoden der CDA wechseln möchten. Der Account Manager kann Ihre Report Suite mit der gewünschten Methode zur Identifizierung von Personen bereitstellen. *Historische zugeordnete Daten aus der vorherigen Methode gehen verloren.*

## Wie geht Adobe mit individuellen Einschränkungen für eine eVar um, die beim feldbasierten Stitching verwendet wird?

Die geräteübergreifende Analyse ruft Dimensionselemente ab, bevor sie für die Berichterstellung optimiert werden. Sie müssen sich bei der geräteübergreifenden Analyse keine Sorgen um individuelle Einschränkungen machen. Wenn Sie jedoch versucht haben, diese Eigenschaft/eVar in einem Workspace-Projekt zu verwenden, können Sie weiterhin das Dimensionselement [(Geringer Traffic)](/help/technotes/low-traffic.md) anzeigen.

## Wie viele Report Suites meiner Firma können für CDA aktiviert werden?

Es können mehrere Report Suites aktiviert werden. Jede zusätzliche Report Suite erhöht jedoch die Gesamtbereitstellungszeit, wenn mehrere Report Suites gleichzeitig angefordert werden. CDA führt keine Report Suites zusammen. Jede für CDA aktivierte Report Suite muss geräteübergreifend sein (Daten aus mehreren Oberflächen wie Desktop-Web, mobiles Web, mobile App usw.).

## Wenn mein Experience Cloud-Org (auch IMS-Org genannt) mehrere Firmen in verschiedenen Regionen hat, kann ich dann CDA für alle aktivieren?

Nein. Für dieselbe Organisation kann CDA nur für eine Region aktiviert sein.

## Was sind die Vor- und Nachteile einer 7-tägigen Wiederholung im Vergleich zu einer 1-tägigen Wiederholung?

Der Vorteil des 7-Tage-Lookback-Fensters besteht darin, dass CDA in der Lage ist, mit der Zeit weiter zurückzugehen und zu versuchen, zuvor anonyme Ereignis mit einigen Personen zu verbinden, die sich später innerhalb dieser 7 Tage angemeldet haben. Die Nachteile des 7-Tage-Lookback-Fensters sind 1) Replay wird nur einmal pro Woche ausgeführt und 2) die letzten 7 Tage können sich ändern.

Die Vorteile der Verwendung des 1-Tage-Lookback-Fensters sind 1) Replay-Läufe jeden Tag und 2) nur gestern kann geändert werden. Der Nachteil des 1-tägigen Lookback-Fensters besteht darin, dass CDA nur noch einen Tag zurückgehen kann, um zu versuchen, zuvor anonyme Ereignis mit einer Person zu verbinden, die sich gestern angemeldet hat.

## Was passiert mit den gehefteten Daten in meinen Virtual Report Suites von CDA, wenn meine Firma beschließt, Analytics Ultimate herunterzustufen?

Wenn ein Kunde von Ultimate herabgestuft wird, hat er keinen Zugriff mehr auf zugewiesene Daten. Alle zuvor zugewiesenen Daten werden entfernt. Das bedeutet, dass die Virtual Report Suites von CDA jetzt keine geräteübergreifende Verknüpfung widerspiegeln. Die Daten sehen ähnlich aus wie die ursprünglich nicht zugewiesene Report Suite.
