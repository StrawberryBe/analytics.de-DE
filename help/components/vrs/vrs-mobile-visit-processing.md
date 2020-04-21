---
description: Kontextbezogene Sitzungen in Virtual Report Suites ändern, wie Adobe Analytics mobile Besuche berechnet. In diesem Artikel wird die Verarbeitung von Implikationen von Hintergrundtreffern und App-Startereignissen (beides wird vom mobilen SDK festgelegt) bezüglich der Definition mobiler Besuche beschrieben.
title: Kontextbezogene Sitzungen
uuid: d354864a-9163-4970-a3a0-f2e9729bdbe3
translation-type: tm+mt
source-git-commit: 3997889ae72920d719203edbb159b55b983158e7

---


# Kontextbezogene Sitzungen

Kontextsensitive Sitzungen in Virtual Report Suites ändern, wie Adobe Analytics Besuche von jedem Gerät berechnet. In diesem Artikel werden auch die Verarbeitungsauswirkungen von Hintergrundbesuchen und App-Start-Ereignissen (beide vom mobilen SDK festgelegt) auf die Definition von Mobilbesuchen beschrieben.

Sie können einen Besuch beliebig definieren, ohne die zugrunde liegenden Daten zu verändern, um der Interaktion Ihrer Besucher mit Ihren digitalen Erlebnissen zu entsprechen.

## URL-Parameter für Kundenperspektive 

Mit dem Datenerfassungsprozess von Adobe Analytics können Sie einen Abfragen-Zeichenfolgenparameter festlegen, der die Kundenperspektive (als Zeichenfolgenparameter &quot;cp&quot; bezeichnet) angibt. Dieses Feld gibt den Status der digitalen Anwendung des Endbenutzers an. Auf diese Weise können Sie erkennen, ob ein Treffer generiert wurde, während sich eine mobile App im Hintergrund befand.

## Verarbeitung von Treffern im Hintergrund 

Ein Hintergrundschlag ist ein Treffer, der von Adobe Mobile SDK Version 4.13.6 und höher an Analytics gesendet wird, wenn die App eine Verfolgungsanfrage im Hintergrund durchführt. Zu den typischen Beispielen zählen:

* Daten, die während eines Geo-Zauns gesendet werden
* Push-Benachrichtigungsinteraktion

In den folgenden Beispielen wird die Logik erläutert, die verwendet wird, um zu bestimmen, wann ein Besuch-Beginn endet und wann die Einstellung &quot;Hintergrundtreffer am Starten eines neuen Besuchs verhindern&quot;für eine Virtual Report Suite aktiviert ist oder nicht aktiviert ist.

**Wenn „Starten neuer Besuche durch Hintergrundtreffer verhindern“ nicht aktiviert ist:**

Wenn diese Funktion für eine Virtual Report Suite nicht aktiviert ist, werden Hintergrundtreffer genauso behandelt wie jeder andere Treffer, d. h. sie werden für neue Besuche Beginn und verhalten sich genauso wie Vordergrundtreffer. Beispiel: Wenn ein Hintergrundschlag weniger als 30 Minuten vor einer Reihe von Vordergrundtreffer (der Standard-Sitzungs-Timeout für eine Report Suite) eintritt, ist der Hintergrundtreffer Teil der Sitzung.

![](assets/nogood1.jpg)

Tritt der Hintergrundschlag mehr als 30 Minuten vor einem Treffer im Vordergrund auf, erstellt der Hintergrundschlag einen eigenen Besuch, bei einem Gesamtbesuch von 2.

![](assets/nogood2.jpg)

**Wenn „Starten neuer Besuche durch Hintergrundtreffer verhindern“ aktiviert ist:**

Die folgenden Beispiele veranschaulichen das Verhalten von Hintergrundtreffern, wenn diese Funktion aktiviert ist.

Beispiel 1: Ein Hintergrundtreffer tritt eine gewisse Zeitspanne (t) vor einer Reihe von Vordergrundtreffern auf.

![](assets/nogoodexample1.jpg)

Wenn in diesem Beispiel der *Wert* größer ist als der von der Virtual Report Suite konfigurierte Timeout für Besuche, wird der Hintergrundtreffer aus dem Besuch ausgeschlossen, der durch die Vordergrundtreffer gebildet wird. Wenn beispielsweise der Timeout für den Besuch der Virtual Report Suite auf 15 Minuten festgelegt wurde und ** er 20 Minuten betrug, würde der Besuch, der aus dieser Trefferreihe (die durch die grüne Gliederung angezeigt wird) gebildet wurde, den Hintergrundschlag ausschließen. Das bedeutet, dass eVars, die mit einem &quot;Besuch&quot;-Ablauf beim Hintergrundschlag festgelegt wurden, **nicht** beim folgenden Besuch beibehalten werden und ein Container für Besuchersegment nur die Vordergrundtreffer in der grünen Umrisslinie enthalten würde.

![](assets/nogoodexample1-2.jpg)

Wenn *t* dagegen unter dem konfigurierten Timeout der Besuchszeit der Virtual Report Suite liegt, wird der Hintergrundtreffer als Teil des Besuchs einbezogen, als wäre er ein Vordergrundtreffer (wird durch die grüne Umrisslinie angezeigt):

![](assets/nogoodexample1-3.jpg)

Das bedeutet:

* Alle eVars, die mit dem Ablauf &quot;Besuch&quot;beim Hintergrundschlag festgelegt wurden, bleiben bei den anderen Treffern dieses Besuchs unverändert.
* Alle Werte, die im Hintergrund-Treffer festgelegt werden, werden in die Logikbewertung der Segmentlogik auf Besuchsebene einbezogen.

In beiden Fällen beträgt die Gesamtanzahl der Besuche 1.

Beispiel 2: Wenn ein Hintergrundtreffer nach einer Reihe von Vordergrundtreffern auftritt, ist das Verhalten ähnlich:

![](assets/nogoodexample2.jpg)

Wenn der Hintergrundschlag nach dem konfigurierten Timeout der Virtual Report Suite erfolgt, ist der Hintergrundschlag nicht Teil einer Sitzung (grün dargestellt):

![](assets/nogoodexample2-1.jpg)

Genauso wird der Hintergrundschlag in den Besuch aufgenommen, der durch die vorherigen Vordergrundtreffer gebildet wurde, wenn der Zeitraum *t* niedriger war als der konfigurierte Timeout der Virtual Report Suite:

![](assets/nogoodexample2-2.jpg)

Das bedeutet:

* Alle eVars, die bei den vorherigen Treffern im Vordergrund mit dem Ablauf &quot;Besuch&quot;festgelegt wurden, bleiben beim Hintergrundschlag dieses Besuchs mit ihren Werten erhalten.
* Alle Werte, die im Hintergrund-Treffer festgelegt werden, werden in die Logikbewertung der Segmentlogik auf Besuchsebene einbezogen.

Wie zuvor wäre die Gesamtzahl der Besuche in beiden Fällen 1.

Beispiel 3: Unter bestimmten Umständen kann ein Hintergrundtreffer dazu führen, dass zwei separate Besuche in einem einzelnen Besuch kombiniert werden. Im folgenden Szenario wird einem Hintergrundschlag eine Reihe von Vordergrundtreffer vorangestellt und gefolgt:

![](assets/nogoodexample3.jpg)

Wenn in diesem Beispiel *t1* und *t2* beide kleiner als die für die Virtual Report Suite konfigurierte Timeout-Werte für den Besuch sind, würden all diese Treffer zu einem einzigen Besuch zusammengefasst, selbst wenn *t1* und *t2* zusammen größer als der Timeout für den Besuch sind:

![](assets/nogoodexample3-1.jpg)

Wenn jedoch *t1* und *t2* größer als der für die Virtual Report Suite konfigurierte Timeout sind, werden diese Treffer in zwei unterschiedliche Besuche aufgeteilt:

![](assets/nogoodexample3-2.jpg)

Genauso (wie in unseren vorherigen Beispielen) würde, wenn *t1* kleiner als der Timeout und *t2* kleiner als der Timeout ist, der Hintergrundhit im ersten Besuch eingeschlossen werden:

![](assets/nogoodexample3-3.jpg)

Wenn *t1* größer als der Timeout und *t2* kleiner als der Timeout ist, wird der Hintergrundtreffer beim zweiten Besuch eingeschlossen:

![](assets/nogoodexample3-4.jpg)

Beispiel 4: In Szenarien mit einer Reihe von Hintergrundtreffern im Zeitraum des Besuchstimeouts der Virtual Report Suite bilden die Treffer einen nicht sichtbaren „Hintergrundbesuch“, der nicht zu der Besuchsanzahl zählt und der nicht mithilfe eines Besuchssegmentierungscontainers zugänglich ist.

![](assets/nogoodexample4.jpg)

Obwohl dies nicht als Besuch gilt, behalten festgelegte eVars mit Besuchsablauf ihre Werte für die anderen Hintergrundtreffer in diesem „Hintergrundbesuch“.

Beispiel 5: In Szenarien, in denen mehrere Hintergrundtreffer nacheinander im Anschluss an eine Reihe von Vordergrundtreffern auftreten, ist es möglich (je nach Timeouteinstellung), dass die Hintergrundtreffer einen Besuch länger aufrecht erhalten als für die Zeitspanne des Besuchstimeouts. Wenn zum Beispiel *t1* und *t2* zusammen größer als der Timeout für den Besuch der Virtual Report Suite, aber einzeln kleiner als der Timeout waren, würde der Besuch weiterhin beide Hintergrundtreffer umfassen:

![](assets/nogoodexample5.jpg)

Wenn eine Reihe von Hintergrundtreffern vor einer Reihe von Ereignissen im Vordergrund auftreten, tritt ein ähnliches Verhalten auf:

![](assets/nogoodexample5-1.jpg)

Hintergrundtreffer verhalten sich auf diese Weise, um alle Zuordnungseffekte von eVars oder anderen Variablen zu erhalten, die während Hintergrundtreffer festgelegt wurden. Auf diese Weise können nachgelagerte Ereignis zur Vordergrundkonvertierung auf Aktionen zurückgeführt werden, die während der Ausführung einer App im Hintergrund ausgeführt wurden. Sie ermöglicht es auch einem Besuchssegment-Container, Hintergrundtreffer einzuschließen, die zu einer nachgelagerten Vordergrundsitzung führten, was zur Messung der Effektivität von Push-Nachrichten nützlich ist.

## Besuchsmetrikverhalten 

Die Besuchszahl basiert ausschließlich auf der Anzahl der Besuche, die mindestens einen Treffer im Vordergrund enthalten. Das bedeutet, dass verwaiste Hintergrundbesuche oder &quot;Hintergrundbesuche&quot;nicht in die Besuchsmetrik einbezogen werden.

## Zeit pro Besuch – Metrikverhalten 

Die Besuchszeit wird immer noch analog zur Zeit zwischen Treffern ohne Hintergrundtreffer berechnet. Wenn ein Besuch Hintergrundtreffer enthält (weil diese Treffer nahe genug an die Treffer im Vordergrund gingen), werden diese Treffer in die Berechnung der Besuchszeit pro Besuch eingeschlossen, als ob sie ein Treffer im Vordergrund wären.

## Einstellungen zur Verarbeitung von Treffern im Hintergrund 

Weil die Hintergrundtrefferverarbeitung nur für Virtual Report Suites mit Berichtszeitverarbeitung verfügbar ist, unterstützt Adobe Analytics zwei Methoden zur Verarbeitung von Hintergrundtreffern, um die Anzahl der Besuche in der zugrunde liegenden Report Suite beizubehalten, wobei die Funktion „Berichtszeitverarbeitung“ nicht verwendet wird. Um auf diese Einstellung zuzugreifen, navigieren Sie zur Adobe Analytics Admin Console, gehen Sie zu den Einstellungen der jeweiligen Basis-Report Suite, navigieren Sie dann zum Menü &quot;Mobile Management&quot;und zum Untermenü &quot;Mobile Application Berichte&quot;.

1. &quot;Veraltete Verarbeitung am&quot;: Dies ist die Standardeinstellung für alle Report Suites. Die Verarbeitung von älterer Verarbeitung bei Prozesshintergrund-Treffern als normale Treffer in unserer Verarbeitungspipeline zu belassen, soweit es die Report Suite ohne Berichtszeitzuordnung betrifft. Das bedeutet, dass alle Hintergrundtreffer, die in der Basis-Report Suite angezeigt werden, die Besuche als normalen Treffer inkrementieren. Wenn in Ihrer Basis-Report Suite keine Hintergrundtreffer angezeigt werden sollen, ändern Sie diese Einstellung in &quot;Aus&quot;.
1. „Legacy-Verarbeitung Aus“: Wenn die Legacy-Verarbeitung für Hintergrundtreffer aus ist, werden an die zugrunde liegende Report Suite gesendete Hintergrundtreffer von der zugrunde liegenden Report Suite ignoriert, und sie sind nur zugänglich, wenn eine in dieser zugrunde liegenden Report Suite erstellte Virtual Report Suite für die Verwendung der Funktion „Berichtszeitverarbeitung“ konfiguriert ist. Demnach werden von den Hintergrundtreffern erfasste Daten, die an diese zugrunde liegende Report Suite gesendet werden, nur in einer Virtual Report Suite mit aktivierter Funktion „Berichtszeitverarbeitung“ angezeigt.

   Diese Einstellung ist für Kunden gedacht, die die neue Verarbeitung von Hintergrundschlägen nutzen möchten, ohne die Anzahl der Besuche ihrer Basis-Report Suite zu ändern.

In beiden Fällen werden Hintergrundtreffer mit denselben Kosten berechnet wie jeder andere Treffer, der an Analytics gesendet wird.

## Starten neuer Besuche bei allen App-Starts 

Neben der Verarbeitung von Hintergrundtreffervorgängen können Virtual Report Suites einen neuen Besuch von Beginn erzwingen, sobald das mobile SDK ein App-Start-Ereignis sendet. Wenn diese Einstellung aktiviert ist, erzwingt sie jedes Mal, wenn ein App-Start-Ereignis vom SDK gesendet wird, einen neuen Besuch bei Beginn, unabhängig davon, ob ein offener Besuch seinen Timeout erreicht hat. Der Treffer mit dem App-Start-Ereignis wird als erster Treffer beim nächsten Besuch eingeschlossen und inkrementiert die Besuchszahl und erstellt einen eindeutigen Container für die Segmentierung.
