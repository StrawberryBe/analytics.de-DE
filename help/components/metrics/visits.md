---
title: Besuche
description: Eine Folge von Seitenansichten während einer Sitzung.
translation-type: tm+mt
source-git-commit: 0328de560185e716a3913080feda9cd078e0f206
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 5%

---


# Besuche

Die Metrik &quot;Besuche&quot;zeigt die Anzahl der Sitzungen für alle Besucher Ihrer Site an.

## Berechnung dieser Metrik

Ein Besuch hängt immer mit einem Zeitraum zusammen, sodass Sie wissen, ob ein neuer Besuch gezählt werden soll, wenn dieselbe Person zu Ihrer Site zurückkehrt. Ein Besuch Beginn, wenn der Benutzer zum ersten Mal auf Ihre Site gelangt. Ein Besuch endet, wenn eines der folgenden Kriterien erfüllt ist:

* **30 Minuten Inaktivität**: Fast alle Sitzungen enden auf diese Weise. Wenn mehr als 30 Minuten zwischen Treffern verstreichen, beginnt ein neuer Besuch.
* **12 Stunden Aktivität**: Wenn ein Benutzer Bildanforderungen über einen Zeitraum von 12 Stunden ohne 30-minütige Lücken auslöst, wird automatisch ein neuer Besuch Beginn.
* **2500 Treffer**: Wenn ein Benutzer eine große Anzahl von Treffern generiert, ohne eine neue Sitzung zu starten, wird ein neuer Besuch nach 2500 Bildanforderungen gezählt.
* **100 Hits in 100 Sekunden**: Wenn ein Besuch aus mehr als 100 Hits besteht, die in weniger als 100 Sekunden stattfinden, endet der Besuch automatisch. Dieses Verhalten gibt normalerweise eine Bot-Aktivität an. Diese Einschränkung wird erzwungen, um die Berichtleistung zu erhöhen.

Ein Besuch fällt aufgrund der oben genannten Kriterien nicht unbedingt mit einer Browsersitzung zusammen. Einer der häufigsten Unterschiede besteht darin, dass ein Besucher zu Ihrer Site navigiert, die Registerkarte mehr als 30 Minuten geöffnet lässt und dann das Browsen fortsetzt. Diese Aktion ist technisch gesehen Teil derselben Browsersitzung, Adobe betrachtet diese Aktion jedoch zwei separate Besuche.

## Definition eines Besuchs ändern

Sie können die Definition eines Besuchs auf einen anderen Zeitpunkt als 30 Minuten ändern.

* Bei [Virtual Report Suites](../vrs/vrs-about.md)können Sie den Timeout-Wert für Besuche mithilfe des [!UICONTROL Timeouts] für Besuche ändern. Sie können den Timeout-Wert für Besuche in einen beliebigen vernünftigen Wert ändern.
* Bei Standard-Report Suites wenden Sie sich an den Kundendienst, um eine Verkürzung der Besuchsdauer für eine bestimmte Report Suite anzufordern. Die Dauer der Besuche für Standard-Report Suites darf 30 Minuten nicht überschreiten, daher können Sie sie nur verkürzen.

## Verhalten, das sich auf Besuche auswirkt

Wenn ein Besucher eine der folgenden Aktionen ausführt, wird ein neuer Besuch Beginn:

* Löscht den Cache während der Sitzung und fährt mit dem Durchsuchen Ihrer Site fort
* Lässt Ihre Site länger als 30 Minuten in einer Registerkarte geöffnet und fährt dann mit dem Browsen fort
* Öffnet einen anderen Browser und navigiert auf demselben Computer zu Ihrer Site
* Derselbe Benutzer navigiert auf verschiedenen Geräten auf Ihrer Site

Wenn ein Besucher eine dieser Aktionen ausführt, wird ein neuer Besuch **nicht** Beginn, solange weniger als 30 Minuten zwischen aufeinander folgenden Treffern liegen:

* Schließt ihren Browser und navigiert dann erneut zu Ihrer Site
* Starten Sie den Computer neu, öffnen Sie denselben Browser und navigieren Sie erneut zu Ihrer Site
* Transitionen an ein anderes Netzwerk, z. B. das Trennen der Verbindung von einer Dockingstation mit einem kabelgebundenen Netzwerk zu einem Wireless-Netzwerk
* Durchsucht Ihre Site in mehreren Registerkarten. Wenn ein Besucher zwischen Registerkarten hin- und herschaltet, zählt jeder Treffer als Teil desselben Besuchs.

## Besuche, die eine Datumsgrenze überschreiten

Ein Besuch zählt für jeden involvierten Zeitraum. Wenn Sie beispielsweise einen Besucher haben, dass Beginn am Montag um 23:45 Uhr durch Ihre Site navigieren und dann am Dienstag um 12:10 Uhr ihre letzte Bildanforderung senden, sehen Sie einen Besuch, der Montag und Dienstag zugeordnet ist. Die Gesamtbesuchsmetrik wird jedoch dedupliziert und zeigt einen einzelnen Besuch für den Datumsbereich des Projekts an.
