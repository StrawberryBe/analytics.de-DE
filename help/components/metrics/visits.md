---
title: Besuche
description: Eine Folge von Seitenansichten während einer Sitzung.
translation-type: tm+mt
source-git-commit: ee9868b53b93c1ffabdd48e83e38d3cafc9a4c2a
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 89%

---


# Besuche

Die Metrik „Besuche“ gibt die Anzahl der Sitzungen für alle Besucher Ihrer Site an.

## Berechnung dieser Metrik

Ein Besuch ist immer mit einem Zeitraum verknüpft. So wissen Sie, ob es sich um einen neuen Besuch handelt, wenn dieselbe Person zu Ihrer Site zurückkehrt. Ein Besuch beginnt, wenn der Benutzer zum ersten Mal auf Ihrer Site ankommt. Ein Besuch endet, wenn eines der folgenden Kriterien erfüllt ist:

* **30 Minuten Inaktivität**: Fast alle Sitzungen enden auf diese Weise. Wenn mehr als 30 Minuten zwischen Treffern vergangen sind, beginnt ein neuer Besuch.
* **12 Stunden Aktivität**: Wenn ein Benutzer über einen Zeitraum von 12 Stunden Bildanforderungen ohne 30-minütige Pausen auslöst, beginnt automatisch ein neuer Besuch.
* **2500 Treffer**: Wenn ein Benutzer zahlreiche Treffer generiert, ohne eine neue Sitzung zu starten, wird nach 2500 Bildanforderungen ein neuer Besuch gezählt.
* **100 Treffer in 100 Sekunden**: Wenn ein Besuch aus mehr als 100 Treffer besteht, die in weniger als 100 Sekunden stattfinden, endet der Besuch automatisch. Dieses Verhalten deutet typischerweise auf Bot-Aktivität hin. Diese Einschränkung wird durchgesetzt, um die Berichtsleistung zu verbessern.

Ein Besuch fällt aufgrund der oben genannten Kriterien nicht unbedingt mit einer Browser-Sitzung zusammen. Einer der häufigsten Unterschiede besteht darin, dass ein Besucher zu Ihrer Site navigiert, den Tab mehr als 30 Minuten geöffnet lässt und dann das Surfen fortsetzt. Diese Aktion ist technisch gesehen Teil derselben Browser-Sitzung. Adobe betrachtet diese Aktion jedoch als zwei separate Besuche.

## Verhalten, das sich auf Besuche auswirkt

Wenn ein Besucher eine dieser Aktionen ausführt, beginnt ein neuer Besuch:

* Löscht den Cache während der Sitzung und setzt den Besuch Ihrer Site fort.
* Lässt Ihre Site länger als 30 Minuten in einem Tab geöffnet und fährt dann mit dem Surfen fort.
* Öffnet einen anderen Browser und navigiert auf demselben Computer zu Ihrer Site.
* Derselbe Benutzer surft auf verschiedenen Geräten auf Ihrer Site.

Wenn ein Besucher eine dieser Aktionen ausführt, wird ein neuer Besuch **nicht** gestartet, solange zwischen aufeinanderfolgenden Treffern weniger als 30 Minuten liegen:

* Schließt seinen Browser und navigiert dann erneut zu Ihrer Site.
* Startet den Computer neu, öffnet denselben Browser und navigiert erneut zu Ihrer Site.
* Wechselt zu einem anderen Netzwerk, z. B. trennt die Verbindung der Docking-Station mit einem kabelgebundenen Netzwerk und wechselt zu einem drahtlosen Netzwerk.
* Besucht Ihre Site in mehreren Tabs. Wenn ein Besucher zwischen Tabs hin und her wechselt, zählt jeder Treffer als Teil desselben Besuchs.

## Ändern der Definition eines Besuchs

Sie können die Definition eines Besuchs auf eine andere Zeit als 30 Minuten ändern.

* Bei [Virtual Report Suites](../vrs/vrs-about.md) können Sie das Besuchszeitlimit mithilfe des Dropdown-Menüs [!UICONTROL Besuchszeitlimit] ändern. Sie können das Besuchszeitlimit auf einen angemessenen Wert ändern.
* Wenden Sie sich bei Standard-Report Suites an die Kundenunterstützung, um eine Verkürzung der Besuchsdauer für eine bestimmte Report Suite anzufordern. Die Besuchslänge für Standard-Report Suites darf 30 Minuten nicht überschreiten, daher können Sie sie nur verkürzen.

## Besuche, die eine Datumsgrenze überschreiten

Es wird für jeden betroffenen Zeitraum ein Besuch gezählt. Wenn Sie beispielsweise einen Besucher haben, der am Montag um 23.45 Uhr mit dem Navigieren auf Ihrer Site beginnt und am Dienstag um 00.10 Uhr seine letzte Bildanforderung sendet, wird ein Besuch angezeigt, der sowohl Montag als auch Dienstag zugeordnet ist. Die Gesamtbesuchsmetrik wird jedoch dedupliziert und zeigt einen einzelnen Besuch für den Datumsbereich des Projekts an.

## Besuche innerhalb einer Dimension im Vergleich zur Gesamtanzahl der Besuche

Besuche im Kontext einer Dimension (z. B. [Marketing-Kanal](../dimensions/marketing-channel.md)) zeigen die Anzahl der Besuche, die zu einem bestimmten Zeitpunkt ein bestimmtes Dimensionselement enthielten. Häufig gibt es mehrere Dimensionselemente bei verschiedenen Treffern im selben Besuch. Der Versuch, Besuche zu summieren, die über Dimensionselemente berichten, ist in der Regel nicht sinnvoll.

## Alle Besucher in Data Warehouse besuchen

Die Metrik &quot;Besuche - Alle Besucher&quot;steht zusätzlich zur Metrik &quot;Besuche&quot;in Data Warehouse zur Verfügung. Die Metrik &quot;Besuche - Alle Besucher&quot;ist mit der Metrik &quot;Besuche&quot;in anderen Analytics-Werkzeugen vergleichbar. Die Metrik &quot;Besuche&quot;in der Data Warehouse schließt Besucher ohne beständige Cookies aus. Adobe empfiehlt die Verwendung von &quot;Besuche - Alle Besucher&quot;in Anfragen zur Data Warehouse, bei denen Besuche als Metrik gewünscht werden.
