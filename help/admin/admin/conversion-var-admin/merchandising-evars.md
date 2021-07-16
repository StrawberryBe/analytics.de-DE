---
title: Merchandising-eVars und Methoden zur Produktsuche
description: Ein tiefer Einblick in die Konzepte hinter Merchandising-eVars und deren Verarbeitung und Zuordnung von Daten.
source-git-commit: eb508167930019c51823e652fc16122e9e416d07
workflow-type: tm+mt
source-wordcount: '4949'
ht-degree: 0%

---

# Merchandising-eVars und Methoden zur Produktsuche

In diesem detaillierten Dokument werden die Konzepte hinter Merchandising-eVars erläutert, die Daten anders verarbeiten und zuordnen als normale eVars. Außerdem wird erläutert, wie Merchandising-eVars mit Produktsuchmethoden zusammenhängen.

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

Wir können eine zusätzliche eVar verwenden, um die Leistung aller Methoden zur Produktsuche untereinander zu messen. Zusätzlich zu den oben beschriebenen Suchmethoden umfasst das eVar weitere Suchmethoden, z. B. Links zu Produktdetailseiten von externen Websites.

* eVar1: Methoden zur Produktsuche

Konfigurieren Sie keine dieser Variablen als Standard-eVars, sondern als Merchandising-eVars. Durch die Verwendung von Merchandising-eVars können Sie den von eVars erfassten Werten eine beliebige erfolgreiche Aktivität auf *pro Produkt*-Ebene statt auf *pro Besuch/pro Bestellung*-Ebene zuweisen. In diesem Dokument wird der Unterschied zwischen der Zuordnung pro Produkt und pro Bestellung erläutert.

Um zu demonstrieren, wie Sie diese Variablen festlegen, hier ist ein Beispiel, bei dem ein Besucher beschließt, die interne Keyword-Suche &quot;Sandals&quot;zu verwenden, um ein Produkt auf der Site zu finden. Auf der Suchergebnisseite für Suchbegriffe müssen Sie Daten in mindestens zwei eVars erfassen:

* `eVar2` entspricht dem Suchbegriff, der in der Suche verwendet wurde (&quot;Sandals&quot;)
* `eVar1` entspricht der verwendeten Suchmethode für das Produkt (&quot;interne Keyword-Suche&quot;).

Wenn Sie diese beiden Variablen auf diese spezifischen Werte setzen, wissen Sie, dass der Besucher den internen Keyword-Suchbegriff &quot;Sandalen&quot;verwendet, um ein Produkt zu finden. Gleichzeitig wissen Sie, dass der Besucher nicht die anderen Produktsuchmethoden verwendet, um Produkte zu finden (z. B. durchsucht er nicht die Produktkategorien, während er eine Suchbegriffsuche durchführt). Um sicherzustellen, dass eine ordnungsgemäße Zuordnung pro Produkt erfolgt, sollten diese nicht verwendeten Methoden nicht für die Suche nach einem Produkt angerechnet werden, das über eine interne Keyword-Suche gefunden wurde. Daher müssen Sie eine Logik in den Code einfügen (z. B. AppMeasurement, AEP Web SDK usw.), der die mit diesen anderen Suchmethoden verknüpften eVars automatisch auf einen Wert der &quot;Nicht-Suchmethode&quot;setzt.

Wenn ein Benutzer beispielsweise mithilfe des Suchbegriffs &quot;sandals&quot;nach Produkten sucht, sollte die Logik des Analytics-Codes die Variablen auf der Seite mit den internen Suchergebnissen für Suchbegriffe auf die folgenden setzen:

* eVar2=&quot;sandals&quot;: das Keyword &quot;Sandals&quot;in der internen Keyword-Suche verwendet wurde
* eVar1=&quot;Interne Keyword-Suche&quot;: die Suchmethode &quot;Suche nach internen Keywords&quot;verwendet wurde
* eVar3=&quot;Nicht-interne Kampagne&quot;: Es wurde keine interne Kampagne für den Zugriff auf die Suchergebnisseite verwendet.
* eVar4=&quot;non-browse&quot;: Auf der Suchergebnisseite wurde keine Kategorie &quot;Durchsuchen&quot;aufgerufen.
* eVar5=&quot;non-cross-sell&quot;: Auf der Seite Suchergebnisse wurde kein Querverkaufslink angeklickt

## Merchandising-eVars-Einstellungen

Bevor Sie mit dem Beispiel &quot;Sandalen&quot;fortfahren, finden Sie hier die verschiedenen Einstellungen, die Sie mit Ihren Merchandising-eVars verwenden können.  Der folgende Screenshot stammt aus dem Report Suite Manager. Rufen Sie sie auf, indem Sie zu Analytics > Admin > Report Suites > Einstellungen bearbeiten > Konversion > Konversionsvariablen > Neu hinzufügen > Merchandising aktivieren navigieren.

![](assets/merch-evars1.png)

Die Abschnitte unter der Tabelle enthalten weitere Details zu diesen Einstellungen.

| Einstellung | Beschreibung |
|--- | --- |
| Name | Der Name oder die Berichtsdimension, mit der die Variable verknüpft werden soll. Wenn `eVar1` Produktsuchmethoden erfassen soll, sollte das Feld Name für `eVar1` auf &quot;Produktsuchmethoden&quot;gesetzt werden. |
| Merchandising | Die Syntax, die zum Erfassen der Merchandising-eVar verwendet wird |
| Zuordnung | Hilft bei der Bestimmung des Merchandising-eVar, dem eine Gutschrift zugeschrieben werden soll, wenn ein erfolgreiches Ereignis stattfindet. |
| Läuft ab nach | Bestimmt, wann bestehende eVar- und Merchandising-Bindungen nicht mehr wirksam sein sollten. |
| Typ | Die Art der Daten, die im Merchandising-eVar erfasst werden |
| Merchandising-Binding-Ereignis | Die Ereignisse, die bestimmen, wann ein eVar an einen Merchandising-Wert gebunden werden soll |
| Zurücksetzen | Ein Trigger, der zu diesem Zeitpunkt alle Backend-Daten für die eVar zurücksetzt |
| Merchandising aktivieren | Eine Markierung, die auf &quot;Aktiviert&quot;gesetzt werden muss, um den eVar von einem standardmäßigen eVar in ein Merchandising-eVar zu verwandeln |

### Merchandising aktivieren

Wenn die Einstellung &quot;Merchandising aktivieren&quot;auf &quot;Aktiviert&quot;gesetzt ist, werden alle unten beschriebenen Einstellungen im Report Suite Manager angezeigt. Wenn die Einstellung &quot;Merchandising aktivieren&quot;auf &quot;Deaktiviert&quot;gesetzt ist, sind nur die Standardeinstellungen für eVar verfügbar.

### Merchandising

Diese Option ist nicht für reguläre eVars verfügbar. Mit der Einstellung [!UICONTROL Merchandising] können Sie entweder [!UICONTROL Konversionsvariablensyntax] oder [!UICONTROL Produktsyntax] als Methode zur Erfassung des Merchandising-eVar auswählen.

**[!UICONTROL Konversionsvariablensyntax]** bedeutet, dass Sie den eVar in einer eigenen Variablen festlegen. Mit der Konversionsvariablensyntax wird beispielsweise der `eVar1`-Wert von &quot;Interne Keyword-Suche&quot;im Seiten-Code (oder im AppMeasurement-Code, AEP Web SDK-Code usw.) wie folgt festgelegt:

`s.eVar1="internal keyword search";`

Bei **[!UICONTROL Produktsyntax]** wird der eVar jedoch nur innerhalb der Adobe Analytics-Produktvariablen festgelegt. Die Analytics-Produktvariable ist in sechs verschiedene Teile pro Produkt unterteilt:

`s.products="[category];[productID];[quantity];[revenue];[events];[eVars]"`

*  Kategorie ist eine veraltete Funktion und wird nicht mehr als praktikable Option zur Nachverfolgung der Produktkategorieleistung empfohlen.  Die bloße Existenz zeigt, warum bei den meisten Implementierungen der Variablen &quot;products&quot;ein einzelnes Semikolon dem productID-Teil des Variablenwerts vorangeht.
*  Menge und   Umsatz sind nützlich, wenn ein Produktkauf verfolgt wird.
*  Ereignisse sind nützlich für die Aufzeichnung benutzerdefinierter inkrementeller oder Währungsereigniswerte, die nicht als Umsatz gezählt werden sollen (z. B. Versand, Rabatte usw.)

Merchandising-eVars, die für die Verwendung der Produktsyntax konfiguriert sind, werden im letzten Teil der Variablen &quot;products&quot;festgelegt. Angenommen, ein Besucher verwendet eine interne Keyword-Suche, um die Produkt-ID &quot;12345&quot;zu finden. Die produktsyntaxbasierte Methode zum Festlegen von eVar1 in diesem Beispiel würde wie folgt aussehen:

`s.products=";12345;;;;eVar1=internal keyword search";`

Beachten Sie, dass wir weiterhin durch Semikolon getrennte Platzhalter für die Menge, den Umsatz und die Ereignisbereiche der Produktvariablen haben.  Ohne diese Platzhalter würde die Einstellung `eVar1` der internen Keyword-Suche vollständig ignoriert.

### Zuordnung

Der Begriff &quot;Zuordnung&quot;für Merchandising-eVars ist irreführend, insbesondere für Merchandising-eVars, die die Konversionsvariablensyntax verwenden. Alle Standard-eVars können über eine eigene individuelle Zuordnungseinstellung verfügen. Merchandising-eVars mit Konversionsvariablensyntax verwenden jedoch nur die Zuordnungseinstellung &quot;Zuletzt (Letzter)&quot;, unabhängig davon, was die Zuordnungseinstellungen im Report Suite Manager zeigen.

Zu verstehen, was diese Einstellung bewirkt, bedeutet, den Unterschied zwischen der Zuordnung von eVar und der Bindung von Merchandising-eVar zu verstehen. Bei Merchandising-eVars ist &quot;Merchandising-eVar-Bindung&quot;ein geeigneterer Name für diese Einstellung &quot;Zuordnung&quot;.

**Standardeinstellung für die Zuordnung von eVar**

Wenn eVar mit Standardsyntax aus einer Bildanforderung erfasst werden, fügen die Adobe Analytics-Verarbeitungsserver Daten in eine andere Datenbankspalte ein, die so genannte `post_evar` -Spalte. Da eVars persistent sein sollen - sie laufen in den meisten Fällen nach dem aktuellen Treffer irgendwann ab - setzen die Server diese `post_evar` -Spalte bei jeder nachfolgenden Bildanforderung ein. Sie wird auf den letzten Wert gesetzt, der an die entsprechende eVar übergeben wird. Bei Standard-eVars verwendet Adobe Analytics bei einem Erfolgsereignis die Spalte `post_evar` anstelle der regulären eVar, um den eVar zu bestimmen, dem das Ereignis gutgeschrieben werden soll.

Bei Standard-eVars bestimmt die Zuordnungseinstellung, ob der erste oder der letzte eVar, der während eines bestimmten Zeitraums erfasst wurde, in die Spalte `post_evar` eingefügt wird. Wenn die Zuordnungseinstellung für einen Standard-eVar gleich &quot;Ausgangswert (Erster)&quot;ist, wird der erste vom Besucher erfasste eVar für alle nachfolgenden Bildanforderungen in die Spalte `post_evar` eingefügt. Dies gilt für alle zukünftigen Anfragen, die vom Browser dieses Besuchers gesendet werden, bis der eVar gemäß seiner Einstellung &quot;Läuft ab nach&quot;abläuft.

Wenn die Zuordnungseinstellung eines standardmäßigen eVar gleich &quot;Zuletzt verwendet (Letzter)&quot;ist, wird der neueste vom Besucher erfasste eVar für alle nachfolgenden Bildanforderungen in die Spalte `post_evar` eingefügt. Die Zuordnung &quot;Zuletzt verwendet (Letzter)&quot;bedeutet, dass sich der Wert `post_evar` jedes Mal ändert, wenn der zugehörige eVar in einer Bildanforderung auf einen neuen Wert gesetzt wird. Die Zuordnung &quot;Ausgangswert (Erster)&quot;bedeutet, dass sich die Spalte `post_evar` nicht über Treffer hinweg ändert, obwohl die zugehörige eVar in einer zukünftigen Bildanforderung möglicherweise auf einen anderen Wert festgelegt ist.

**Zuweisungseinstellung für Merchandising-eVar (Bindung)**

Wie bereits erwähnt, wird allen Merchandising-eVars mit Konversionsvariablensyntax nur die Zuordnung &quot;Zuletzt (Letzter)&quot;zugewiesen.  Dies bedeutet die Einstellung &quot;Zuordnung&quot;tatsächlich für Merchandising-eVars: Wie bereits erwähnt, bestimmt diese Einstellung nicht, welche Werte in die Spalte `post_evar` eingefügt werden, da ein Besucher die Site weiterhin verwendet. Stattdessen bestimmt die Zuordnungseinstellung für Merchandising-eVars, welcher eVar an ein Produkt gebunden ist und wie diese  ihre Erfolgsereignisse wieder den eVar zuordnen, an die sie gebunden sind.

Lassen Sie uns besprechen, was passiert, wenn die Einstellung für die Zuordnung (d. h. Bindung) eines Merchandising-eVar auf &quot;Ausgangswert (Erster)&quot;gesetzt ist. Alle Produkte, die neben der Spalte `post_evar` gesetzt wurden und noch nicht an die entsprechende &quot;vorverarbeitete&quot;eVar der Spalte &quot;post_evar&quot;gebunden waren, sind an den Wert in der Spalte `post_evar` gebunden. Diese Bindung zwischen eVar und Produkt ändert sich erst, wenn die eVar gemäß den Einstellungen für &quot;Läuft ab nach&quot;in den Report Suite-Einstellungen ablaufen.

Jedes Mal, wenn eine Bildanforderung die Kriterien erfüllt, die ein bereits gebundenes eVar ansonsten an den zuletzt festgelegten Wert binden würden, zwingt die Einstellung &quot;Ausgangswert (Erster)&quot;die Adobe Analytics-Datenerfassungsserver dazu, solche weiteren Versuche zu ignorieren. Das Gegenteil geschieht mit Merchandising-eVars, bei denen die Einstellung Zuordnung (Bindung) gleich &quot;Zuletzt verwendet (Letzter)&quot;ist. Jedes Mal, wenn eine Bildanforderung die Kriterien erfüllt, die ein Produkt an ein Merchandising-eVar binden, bindet das Produkt sich selbst an den neuesten Wert, der an die eVar übergeben wird, oder an den Wert, der (immer) in der Spalte `post_evar` enthalten ist.

Wie bereits erwähnt, können Sie mit Merchandising-eVars Erfolgsereignisse eVar auf Produktbasis und nicht pro Besuch/pro Bestellung zuweisen. Wenn einem gebundenen Produkt also ein Erfolgsereignis zugeordnet ist (z. B. ein Zusatz zum Warenkorb oder ein Kauf), schreibt das Erfolgsereignis sowohl dem eVar als auch den Merchandising-Werten gut, an die das Produkt zu diesem Zeitpunkt gebunden ist.

### Läuft ab nach

Mit der Ablaufeinstellung eines Merchandising-eVar können Sie festlegen, wann die Produkt-/eVar-Bindungen ablaufen sollen und wann die Spalte post_evar nicht mehr automatisch ausgefüllt werden soll, nachdem eine eVar an eine Bildanforderung übergeben wurde. Der Ablauf eines eVar kann stattfinden, wenn entweder ein Erfolgsereignis (Ihrer Wahl) aufgezeichnet wird oder ein bestimmter Zeitraum - erneut, Ihrer Wahl - vergeht. Adobe Analytics ermöglicht jeweils nur eine Ablaufeinstellung pro eVar.

Für die Lösung zur Produktsuchmethode sollte die Best Practice für die Festlegung des Ablaufs eines Merchandising-eVar darin bestehen, sie entweder auf die Zeit festzulegen, die ein Produkt im Warenkorb einer Site verbleibt, bevor die Site es automatisch aus dem Warenkorb entfernt ODER wenn das Kaufereignis stattfindet. Mit beiden Ablaufeinstellungen wird jedem eVar, das ein Besucher kauft, die Bestell-/Einheitsgutschrift zugewiesen, die den Merchandising-Werten zugeordnet wird, an die die Produkte zu diesem Zeitpunkt gebunden waren.

### Typ

Die Einstellung eVar bestimmt, welcher Datentyp in die eVar eingefügt wird. In den meisten - wenn nicht in allen - Fällen sollte dieser Wert beim Einrichten einer Merchandising-eVar &quot;Text&quot;entsprechen. Die Verwendung des Typs &quot;Zähler&quot;für Merchandising-eVar ist selten, kann jedoch je nach Tracking-Anforderungen effektiv genutzt werden, um den Zählerwerten eVar pro Produkt zuzuordnen.  Die Erörterung von Lösungen mit dem Typ &quot;Zähler&quot;fällt nicht in den Anwendungsbereich dieses Dokuments.

### Merchandising-Binding-Ereignis

Mit der Einstellung &quot;Merchandising-Binding-Ereignis&quot;können Sie die Bedingungen festlegen, unter denen ein Produkt an den Wert eines Merchandising-eVar gebunden wird. Diese Bedingungen sind auf das Auslösen bestimmter Erfolgsereignisse oder eVars beschränkt. Das Auslösen von Traffic-Variablen (z. B. Props) hat keine Auswirkungen auf Merchandising-Bindungen.

Eine der nützlichsten Funktionen bei der Einstellung &quot;Merchandising-Binding-Ereignis&quot;ist die Möglichkeit, ein Produkt über mehrere Ereignisse an einen eVar zu binden. Beispielsweise könnte die Einstellung ermöglichen, dass eVar entweder über ein Produktansichtsereignis, ein Warenkorbereignis oder ein Kaufereignis an einen Merchandising-Wert gebunden werden. Die Einstellung kann sogar - standardmäßig - ein eVar an einen Merchandising-Wert binden, wenn ein anderes Ereignis/jede andere eVar - Merchandising oder anderweitig - in derselben Bildanforderung wie das Produkt enthalten ist.

### Zurücksetzen

Mit der Einstellung Zurücksetzen können Sie alle eVar für alle Besucher, die derzeit einen `post_evar` -Wert in der Adobe Analytics-Backend-Datenbank haben, sofort &quot;ablaufen&quot;lassen. Außerdem werden alle aktuellen Produkt-/eVar-Bindungen entfernt.

>[!IMPORTANT]
>Es wird von Adobe nicht empfohlen, die Einstellung &quot;Zurücksetzen&quot;zu verwenden, es sei denn, Sie möchten den eVar vollständig mit einer vollständig &quot;leeren Verzögerung&quot;von Daten aus dem Zeitpunkt des Zurücksetzens beginnen lassen.

## Welche Einstellungen sollten Sie verwenden?

Unter den vielen verfügbaren Einstellungskombinationen könnten Sie sich fragen, welche Einstellungen &quot;Best Practice&quot;sind.

Wenn Sie die &quot;interne Keyword-Suche&quot;an die Produkt-ID 12345 binden möchten, wird die Variable &quot;products&quot;wie folgt festgelegt:

`s.products=";12345;;;;eVar1=internal keyword search";`

Erfolgsereignisse (Hinzufügung des Warenkorbs, Käufe), die gleichzeitig mit der Produkt-ID 12345 erfasst werden, werden sowohl der Produkt-ID 12345 als auch dem `eVar1`-Wert der &quot;internen Keyword-Suche&quot;gutgeschrieben. Ein anderer `eVar1`-Wert erhält nur dann die Gutschrift für Erfolgsereignisse, die mit der Produkt-ID 12345 verknüpft sind, wenn `eVar1` später in der Variablen &quot;products&quot;auf einen **anderen**-Wert gesetzt wurde (neben der Produkt-ID 12345). Beispiel:

`s.products=";12345;;;;eVar1=internal campaign";`

Diese Konfiguration ändert die Bindung der Produkt-ID 12345 vom `eVar1`-Wert von &quot;Interne Keyword-Suche&quot;in den `eVar1`-Wert von &quot;Interne Kampagne&quot;. Diese Neubindung erfolgt jedes Mal, wenn die Produktsyntax verwendet wird und die Einstellung Zuordnung (Bindung) für die eVar auf &quot;Zuletzt verwendet (Letzter)&quot;festgelegt ist. Was passiert, wenn die Einstellung &quot;Zuordnung (Bindung)&quot;stattdessen auf &quot;Ausgangswert (Erster)&quot;festgelegt ist? Wenn Sie dann eVar1 neben der Produkt-ID 12345 auf &quot;Interne Kampagne&quot;setzen, wird die Produkt-ID 12345 nicht erneut an den eVar1-Wert &quot;Interne Kampagne&quot;gebunden. Die Bindung bleibt mit dem ursprünglich gebundenen Wert - &quot;Interne Keyword-Suche&quot;.

### Herausforderungen bei der Verwendung der Produktsyntax

Ohne sorgfältige Planung können bei der Verwendung der Produktsyntax mehrere Probleme auftreten. Nehmen wir beispielsweise die Verwendung mehrerer eVars zur Verfolgung von Produktsuchmethoden auf der Website. Hier muss jede einzelne eVar der Suchmethode gleichzeitig festgelegt werden, damit eine bestimmte Suchmethode einer eVar gutgeschrieben wird (und die andere Suchmethode eVars keine Gutschrift). Produktsyntax kann in solchen Szenarien verwendet werden, der resultierende Code zur Bereitstellung ist jedoch komplizierter.

Wenn wir unser ursprüngliches Beispiel &quot;Sandals&quot;verwenden und es an die Verwendung der Produktsyntax anpassen (vorausgesetzt der Besucher hat ein Produkt mit der ID &quot;sandal123&quot;unter Verwendung des Keyword &quot;sandals&quot;gefunden), muss die resultierende Variable &quot;products&quot;wie folgt festgelegt werden:

`s.products=";sandal123;;;;eVar2=sandals|eVar1=internal search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell";`

Während die Syntax der Variablen &quot;products&quot;in diesem Beispiel lang ist, wird jeder angezeigte eVar an die Produkt-ID &quot;sandal123&quot;gebunden. Ab diesem Zeitpunkt werden alle Erfolgsereignisse (z. B. Hinzufügungen zum Warenkorb, Käufe), die gleichzeitig mit dem Produkt &quot;sandal123&quot;erfasst werden, den eVar gutgeschrieben, die zuletzt an das Produkt gebunden waren.  Dieses Codebeispiel zeigt, ob ein Kauf von 1 Einheit des Produkts &quot;sandal123&quot;(für 79,95 USD) stattfindet, nachdem die oben genannten eVars an das Produkt &quot;sandal123&quot;gebunden waren:

```
s.products=";sandal123;1;79.95";
s.events="purchase";
```

Die folgenden Werte weisen alle 1 Bestellung, 1 Einheit und 79,95 USD Umsatz auf:

* eVar2-Wert von &quot;sandals&quot;
* eVar 1 von &quot;internal keyword search&quot;
* eVar &quot;Nicht-interne Kampagne&quot;
* eVar 4 von &quot;non-browse&quot;

Dies ist die korrekte Zuordnung, was kein Problem darstellt. Das Hauptproblem bei diesem Ansatz besteht vielmehr darin, zu bestimmen, wie und wann die eVars für die Produktsuchmethode festgelegt werden.

In den meisten Fällen mit Produktsyntax müssten die eVars für die Suchmethode auf einer Produktdetailseite festgelegt werden und nicht auf der Seite, auf der die Suchmethode tatsächlich verwendet wurde (z. B. auf der Suchergebnisseite für Suchbegriffe, auf der Durchsuchen-Seite, auf der Landingpage für interne Kampagnen usw.). Es ist vernünftig anzunehmen, dass ein Produkt erst dann wirklich &quot;gefunden&quot;wurde, wenn ein Besucher in gewissem Umfang mit einem Produkt interagiert. Daher sollten diese eVars (unter Verwendung der Produktsyntax) nicht auf der Suchmethodeseite festgelegt werden, da (normalerweise) mehrere Produkte auf diesen Seiten angezeigt werden. Wir möchten den Wert der Suchmethode nur an die Produkte binden, mit denen der Besucher interagiert hat.

Darüber hinaus können Besucher beim Anzeigen einer Suchmethodeseite entweder auf einen Link klicken, der sie zu einer einzelnen Produktdetailseite führt, oder ein einzelnes Produkt direkt von der Suchmethodeseite zum Warenkorb hinzufügen. Wenn ein Besucher das Produkt &quot;sandal123&quot;direkt von einer Suchergebnisseite zum Warenkorb hinzufügt, verwenden Sie unser Suchbegriffbeispiel &quot;sandal123&quot;, den Code zur Erfassung des hinzugefügten Warenkorbs (über das onClick-Ereignis der Schaltfläche zum Hinzufügen zum Warenkorb usw.) zum Zeitpunkt des Hinzufügen zum Warenkorb dynamisch generiert werden oder direkt über den Seiten-Code oder ein Tag-Management-System &quot;hartcodiert&quot;werden.  Unabhängig davon würde der Code, der in solchen Fällen ausgelöst werden soll, etwa wie folgt aussehen:

```
s.linkTrackVars="products,events";
s.linkTrackEvents=s.events="scAdd";
s.products=";sandal123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell";
s.tl(true,"o","Cart Add")
```

Dieser Code bindet die oben angezeigten eVar ordnungsgemäß an das Produkt &quot;sandal123&quot;. Um diese Werte jedoch beim Eintreten des Klickereignisses angemessen festzulegen, muss der Entwickler:

* Fügen Sie der Suchergebnisseite eine serverseitige Logik hinzu, die die Werte bestimmt, die in die eVars der Produktsuchmethode eingefügt werden müssen, und
* Stellen Sie die gesamte Variable &quot;products&quot;ohne Syntaxfehler zusammen.

Wenn ein Besucher das Produkt durch Klicken auf einen Link zur Produktdetailseite &quot;finden&quot;möchte, muss der Entwickler außerdem:

* Übergeben Sie die Details der Produktsuchmethode (wie oben gezeigt) von der Suchmethodenseite zur Produktdetailseite und * * * Stellen Sie denselben Produktvariablenwert aus den Elementen zusammen, die gerade von der vorherigen Seite übergeben wurden.

Diese Lösung erfordert eine hohe Komplexität, die möglicherweise nicht machbar ist.

### Wo Produktsyntax nützlich ist

Die Produktsyntax ist weiterhin nützlich, wenn

* Mehrere Produkte mit denselben Produkt-IDs werden gleichzeitig mit interagiert und
* Die eVars, die an solche Produkte gebunden werden sollen, müssen unterschiedliche Werte pro Produkt-ID aufweisen.

Viele Bekleidungsprodukte verfügen beispielsweise über &quot;untergeordnete SKUs&quot;, die Größe, Farbe, Stil und andere Attribute angeben. Diese Attribute trennen ein einzelnes untergeordnetes Produkt von anderen gleichrangigen Produkten, die zum selben übergeordneten Produkt gehören. Angenommen, Sie möchten ein mittelblaues T-Shirt plus ein großes rotes T-Shirt kaufen. Angenommen, beide Hemden haben die übergeordnete Produkt-ID &quot;tshirt123&quot;und eVar10 wurde so konfiguriert, dass untergeordnete SKUs erfasst werden. Die auf der Kaufbestätigungsseite festgelegten Variablen werden wie folgt festgelegt:

```
s.events='purchase';
s.products=';tshirt123;1;20;;eVar10=tshirt123-m-blue,;tshirt123;1;20;;eVar10=tshirt123-l-red"
```

In diesem Fall werden die Werte `eVar10` (childSKU) von &quot;tshirt123-m-blue&quot;und &quot;tshirt123-l-red&quot;für den Kauf der jeweiligen Instanzen der Produkt-ID &quot;tshirt123&quot;gutgeschrieben.

### Herausforderungen bei der Zuordnung &quot;Zuletzt verwendet&quot;

Mithilfe der Einstellung &quot;Zuletzt verwendet (Letzter)&quot;für die Zuordnung (Bindung) können zusätzliche Probleme auftreten. In vielen Web-Browsing-Erlebnissen &quot;suchen&quot;Besucher ein Produkt, das sie bereits angesehen und/oder zum Warenkorb hinzugefügt haben. Dies geschieht normalerweise über einen nachfolgenden Besuch oder unmittelbar vor der Entscheidung, einen Kauf abzuschließen. Angenommen, sie haben während ihres ersten Besuchs der Site das Produkt &quot;sandal123&quot;über die Keyword-Suche von &quot;Sandalen&quot;gefunden. Sie haben es sofort auf der Suchergebnisseite zum Warenkorb hinzugefügt. Der Code, der den Zusatz zum Warenkorb erfasst, würde wie folgt festgelegt:

```
s.linkTrackVars="products,events";
s.linkTrackEvents=s.events="scAdd";
s.products=";sandal123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross
```

Daher sind alle in dieser Bildanforderung angezeigten eVar an das Produkt &quot;sandal123&quot;gebunden.

Stellen Sie sich vor, der Besucher kauft das Produkt während dieses Besuchs nicht, kehrt aber drei Tage später zur Site zurück. Sie wissen, dass sie bereits das Produkt &quot;sandals123&quot;zum Warenkorb hinzugefügt haben. Aber sie wollen noch mehr darüber erfahren, bevor sie den Kauf tätigen. Anstatt eine Suchbegriffsuche zu verwenden, um das Produkt zu finden, durchsucht der Besucher die Site. Sie landen im Merchandising-Abschnitt &quot;Damen > Schuhe > Sandalen&quot;direkt vor dem &quot;erneuten Auffinden&quot;des Produkts. Wenn sie schließlich die Produktdetailseite für das Produkt &quot;sandal123&quot;erneut finden, werden die Variablen wie folgt festgelegt (beim Laden der Seite):

```
s.events="prodView";
s.products=";sandal123;;;;eVar4=womens > shoes > sandals|eVar1=browse|eVar3=non-internal campaign|eVar2=non-search|eVar5=non-cross-sell";
```

Mit der Einstellung &quot;Zuletzt verwendet (Letzter)&quot;für die Zuordnung (Bindung) wird das Produkt &quot;sandal123&quot;an vollständig andere eVar als ursprünglich gebunden gebunden erneut gebunden. Wenn der Besucher dann den Kauf von &quot;sandal123&quot;abschließt, werden diese neu gebundenen eVar zusätzlich zu den ursprünglich gebundenen Werten vollständig dem Kauf gutgeschrieben!

Die Frage lautet hier: Welche eVar sollten für den Kauf berücksichtigt werden?&quot; Beachten Sie, dass der Besucher das Produkt &quot;sandal123&quot;ursprünglich über eine interne Keyword-Suche gefunden hat. Er wurde dann direkt auf der Suchergebnisseite zum Warenkorb hinzugefügt. Daher sollte der eVar 1-Wert von &quot;Interne Keyword-Suche&quot;(und der eVar2-Wert von &quot;Sandals&quot;) für den Kauf gutgeschrieben werden. Die Zuordnungseinstellungen (Bindung) wurden jedoch auf &quot;Zuletzt verwendet (Letzter)&quot;festgelegt. Daher erhält der eVar1-Wert von &quot;Durchsuchen&quot;(und der eVar4-Wert von &quot;womens > shoes > sandals&quot;) stattdessen die Kaufgutschrift. Der Grund dafür ist, dass sie die letzten Werte waren, die an &quot;sandal123&quot;gebunden waren, bevor der Besucher den Kauf abgeschlossen hatte.

Eine Lösung für dieses Problem besteht darin, die Einstellung für die Zuordnung (Bindung) des Merchandising-eVar von &quot;Zuletzt verwendet (Letzter)&quot;in &quot;Ausgangswert (Erster)&quot;zu ändern. Auf diese Weise werden die ursprünglichen Produktwerte, die an das Produkt &quot;sandal123&quot;gebunden sind, beim Kauf gutgeschrieben, unabhängig davon, wie oft der eVar das  &quot;erneut findet&quot;.

Wenn der Besucher ein Produkt zum Warenkorb hinzufügt, es jedoch nie kauft, ermöglicht der Ablauf der eVar die Bindung eines neuen Suchmethodenwerts an das Produkt. Der eVar sollte der Zeit entsprechen, die eine Website einem Produkt ermöglicht, im Warenkorb zu bleiben, bevor es automatisch entfernt wird.

### Verwenden der Syntax von Konversionsvariablen

Kehren wir zur &quot;Produktsyntax&quot;im Vergleich zu zurück. Frage zur Syntax der Konversionsvariablen. Adobe hat eine einfachere Methode gefunden, um sowohl die Merchandising-eVars der Produktsuchmethode zu erfassen als auch ihre Werte an Produkte zu binden, die Besucher gefunden haben: Die Verwendung der Konversionsvariablensyntax reduziert die Implementierungsarbeit, für die die Entwickler des Clients verantwortlich sind. Sie bietet weiterhin die gleichen - oder besseren - Informationen als die Methode der Produktsyntax. Entwickler müssen einfach die Bereitstellungsanweisungen befolgen, die ihnen gegeben wurden, und der Rest des Codes kann in die Adobe AppMeasurement/AEP Web SDK-Datei eingefügt werden.

Sehen wir uns beispielsweise die empfohlene Lösung zur Verfolgung der Suchleistung interner Keywords an. Auf der Suchergebnisseite für Suchbegriffe wird angegeben, dass der Code den Suchbegriff erfasst, nach dem über eine Prop (z. B. prop4) und eine andere Prop (z. B. prop5) gesucht wird. Diese Eigenschaften verfolgen die Anzahl der Ergebnisse, die bei der Suche angezeigt werden. Immer wenn eine Adobe Analytics-Bildanforderung auf der Suchergebnisseite generiert wird, verwendete sie die Datenschichtobjekte (oder den Seitencode), die von den Entwicklern bereitgestellt wurden, um die oben genannten Variablen (die Props) auszufüllen.

Zusätzliche Logik in der AppMeasurement/AEP Web SDK-Datei kann die restlichen Variablen (die Merchandising-eVars/Dimensionen) ausfüllen, die gleichzeitig festgelegt werden müssen.\
Wenn beispielsweise ein neuer Besucher nach &quot;Sandalen&quot;sucht, die 25 Ergebnisse auf der Suchergebnisseite zurückgaben, würde der auszulösende Code (über den Seiten-Code ODER die Datenschichterfassung) wie folgt aussehen:

```
s.prop4="sandals";
s.prop5="25";
```

Die Logik in der AppMeasurement/Analytics SDK-Datei könnte diesen Codeausschnitt dann automatisch in Folgendes umwandeln:

```
s.prop4="sandals";
s.prop5="25";
s.eVar2="sandals";
s.eVar1="internal keyword search";
s.eVar3="non-internal campaign";
s.eVar4="non-browse";
s.eVar5="non-cross sell";
```

Es besteht kein Grund, sich Gedanken darüber zu machen, ob Daten von Seite zu Seite weitergegeben und versucht werden, eine recht große, unhandliche Zeichenfolge zu erstellen, die in die Produktvariable eingefügt wird. Stattdessen können Entwickler ihren Teil der Tracking-Lösungen implementieren - was in die Props eingefügt wird - und den Rest der Implementierung dem benutzerdefinierten Code überlassen, der von Adobe Consulting bereitgestellt wird.

Wie bereits erläutert, haben alle Merchandising-eVars, die die Konversionsvariablensyntax verwenden, die Zuordnungseinstellung &quot;Zuletzt verwendet (Letzter)&quot;. Sobald ein eVar auf einen beliebigen Wert gesetzt wurde, bleibt dieser Wert über alle nachfolgenden Treffer hinweg erhalten (über die Spalte post_evar ). Er bleibt bestehen, bis er auf einen anderen Wert gesetzt wird oder bis der eVar abläuft. Daher werden alle Produkte, mit denen Benutzer interagieren, nachdem die eVars festgelegt wurden, an die &quot;Zuletzt verwendet (Letzter)&quot;Werte gebunden, sofern sie noch nicht an diese eVars gebunden waren.

Unter Verwendung des obigen Beispiels werden der `eVar2`-Wert von &quot;sandals&quot;und der eVar 1-Wert von &quot;internal keyword search&quot; usw. verwendet. auf allen Seiten bestehen, die nach der Keyword-Suche angezeigt wurden. Sie bleiben bestehen, bis die eVars mit anderen Werten überschrieben werden. Angenommen, ein Besucher klickt auf einen Link zur Produktdetailseite für die Produkt-ID &quot;sandal123&quot;auf der Suchergebnisseite für Suchbegriffe.  Anschließend wird die Produkt-ID &quot;sandal123&quot;(sofern noch nicht gebunden) an jeden der in den Spalten post_evar enthaltenen Werte oder an die eVar gebunden, die von der vorherigen Seite (Suchergebnisse) erfasst wurden.

Es gibt noch eine Sache, die mit der Syntax der Konversionsvariablen überdacht werden muss. Binding-Ereignisse müssen eingerichtet werden, um einen eVar an ein Produkt zu binden. Wenn Sie in einer Adobe Analytics-Bildanforderung einfach ein Merchandising-eVar (in der eigenen -Variablen) neben einem Produkt (in der Produktvariablen) festlegen, wird der eVar nicht notwendigerweise an das Produkt gebunden.  Stattdessen bestimmt die Einstellung &quot;Merchandising-Binding-Ereignis&quot;, die im Report Suite Manager festgelegt ist, die Kriterien, die einen eVar an ein Produkt binden

Da wir die eVar der Suchmethode immer dann an Produkte binden möchten, wenn eine Produktinteraktion stattfindet - was bedeutet, dass ein Produkt &quot;gefunden&quot;wurde -, können Sie davon ausgehen, dass die häufigsten &quot;gefundenen&quot;Interaktionen entweder eine Produktansicht (wenn Besucher auf eine Produktdetailseite gehen) oder ein Zusatz zum Warenkorb (wenn Besucher ein  direkt über eine Produktermittlungsseite zum Warenkorb hinzufügen) sind.  Daher können wir diese beiden Ereignisse (prodView, scAdd) als &quot;grundlegende&quot;Merchandising-Binding-Ereignisse auswählen.
Wenn eines dieser Binding-Ereignisse in einer Bildanforderung enthalten ist, binden alle Produkt-IDs, die in derselben Anforderung enthalten sind (innerhalb der Produktvariablen) und noch nicht an ein Merchandising-eVar gebunden waren, an die neuesten Werte, die an die Merchandising-eVar übergeben wurden (wie in den Spalten post_evar enthalten). Jeder Versuch, diese Produkte nach dieser ursprünglichen Bindung erneut zu binden, wird ignoriert, wenn die Einstellung Zuordnung (Bindung) auf &quot;Ausgangswert (Erster)&quot;gesetzt ist.

### Best Practice-Einstellungen

Im Folgenden finden Sie die Best Practice-Einstellungen. Sie implementieren die Produktsuchmethode so einfach wie möglich mit den leistungsstärksten Ergebnissen. Adobe empfiehlt, dass Clients die einzelnen Merchandising-eVars ihrer Produktsuchmethode (allgemein) wie folgt konfigurieren:

* Merchandising aktiviert: Aktiviert
* Merchandising [Syntax]: Syntax der Konversionsvariablen
* Zuordnung [binding]: Ausgangswert (Erster)
* Läuft ab nach: Die Zeit, die ein Produkt in einem Warenkorb verbleibt, bevor es automatisch entfernt wird (z. B. 14 Tage, 30 Tage usw.).  Wenn keine solche Zeit vorhanden ist, laufen Sie nach dem &quot;Kauf&quot;-Ereignis ab
* Typ: Text
* Merchandising-Binding-Ereignisse:  Produktansicht, Hinzufügen zum Warenkorb und Kauf

## Was machen Binding-Ereignisse eigentlich?

Wenn ein Binding-Ereignis im selben Server-Aufruf wie die Variable &quot;products&quot;enthalten ist, werden die Merchandising-eVar-Werte (unter Verwendung der Konversionsvariablensyntax) in ihrer Post-Spalte an die Variable &quot;products&quot;gebunden. Angenommen, ein Server-Aufruf enthält basierend auf dem vorherigen Beispiel die folgenden Merchandising-eVar:

```
s.eVar2="sandals";
s.eVar1="internal keyword search";
s.eVar3="non-internal campaign";
s.eVar4="non-browse";
s.eVar5="non-cross sell";
```

Wie bereits erläutert, bleiben die oben genannten eVars über ihre Spalte post_evar über den aktuellen Treffer hinaus bestehen. Daher wandeln die Server der Adobe die oben genannten eVars in Folgendes um:

```
post_eVar2="sandals";
post_eVar1="internal keyword search";
post_eVar3="non-internal campaign";
post_eVar4="non-browse";
post_eVar5="non-cross sell";
```

Diese Post-Spalten werden in der Adobe gespeichert und bleiben über den aktuellen Treffer hinaus erhalten, in dem sie ursprünglich festgelegt wurden. Dabei wird davon ausgegangen, dass kein Ablauf oder keine Zurücksetzung der Variablen erfolgt.  Auf Servern der Adobe sind diese post_evar-Werte zum Zeitpunkt der Verarbeitung künftiger Serveraufrufe, die sowohl das Binding-Ereignis als auch die Produktvariable enthalten, &quot;verfügbar&quot;.

Die Bindung erfolgt ausschließlich zwischen diesen post_evar -Werten und dem Inhalt der Variablen &quot;products&quot;. Das Binding-Ereignis &quot;bindet&quot;nicht unbedingt an die eVars- oder die Produktvariable. Es ist der &quot;Katalysator&quot;, der die Adobe-Server anweist, die post_evar -Werte an die Produkte zu binden.

Angenommen, bei einem zukünftigen Treffer werden die folgenden Variablen festgelegt:

```
s.products=";sandals123"
s.events="prodView";
```

In Anbetracht der Spalten post_evar sehen die Adobe-Verarbeitungsserver diesen Treffer wie folgt:

```
s.products=";sandals123"
s.events="prodView";
post_eVar2="sandals";
post_eVar1="internal keyword search";
post_eVar3="non-internal campaign";
post_eVar4="non-browse";
post_eVar5="non-cross sell";
```

Angenommen, eVar1, eVar2, eVar3, eVar4 und eVar5 wurden so konfiguriert, dass `prodView` als Binding-Ereignis verwendet wird. Wenn eine dieser eVars nicht für die Verwendung von prodView als Binding-Ereignis konfiguriert ist, erfolgt keine Bindung zwischen dieser (falsch konfigurierten) eVar und der Variablen &quot;products&quot;.

Die Bindung erzeugt einige sehr interessante Ergebnisse, die im Wert der Spalte post_products zu sehen sind. Durch die Bindung wird der obige Code umgewandelt und einige weitere Post-Spalten wie folgt festgelegt:

```
post_events="prodView"
post_products=";sandals123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell"
```

Der in der Spalte &quot;post_products&quot;enthaltene Wert ist Ihnen möglicherweise bekannt. Scrollen Sie in diesem Dokument nach oben und vergleichen Sie diesen post_products -Wert mit dem s.products -Wert, wie unter dargestellt.  Sie werden feststellen, dass die Spalte post_products mithilfe der Syntax der Produktvariablen festgelegt ist! Das bedeutet, dass durch die Bindung die eVar der Konversionsvariablensyntax über die Produktsyntax in die Variable &quot;products&quot;kopiert werden. Diese Kopieraktion findet nur statt, wenn die Variable &quot;products&quot;und ein Binding-Ereignis (über die eVar-Konfiguration festgelegt) in derselben Anforderung enthalten sind. Ab diesem Zeitpunkt sind die in der Spalte &quot;post_eVar&quot;enthaltenen Werte an das Produkt gebunden. Diese Bindung wird über die Produktsyntax dargestellt, die in der Spalte post_products gespeichert ist.
