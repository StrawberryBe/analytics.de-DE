---
title: Merchandising-eVars und Methoden zur Produktsuche
description: Ein tiefer Einblick in die Konzepte hinter Merchandising-eVars und deren Verarbeitung und Zuordnung von Daten.
feature: Admin Tools
exl-id: 9e1a39aa-451f-49bb-8e39-797b6bbd5499
source-git-commit: 3d9b64bd28210732c7506dbf667c5d4d50e7fb07
workflow-type: tm+mt
source-wordcount: '5291'
ht-degree: 99%

---

# Merchandising-eVars und Methoden zur Produktsuche

In diesem detaillierten Dokument werden die Konzepte hinter Merchandising-eVars erläutert, da diese Daten anders verarbeiten und zuordnen als standardmäßige eVars. Außerdem wird erklärt, wie Merchandising-eVars mit Produktsuchmethoden zusammenhängen.

## Überblick

Durch die Verwendung von Merchandising-eVars können Sie den von eVars erfassten Werten eine beliebige erfolgreiche Aktivität auf einer *pro Produkt*- statt *pro Besuch/pro Bestellung*-Basis zuweisen.

Die meisten Websites für den Einzelhandel bieten zwar viele Möglichkeiten, Produkte zu finden, Adobe betrachtet jedoch die folgenden Methoden zur Produktsuche als unerlässlich, die jeder Einzelhandelskunde in Adobe Analytics verfolgen sollte:

* Interne Suchbegriffe
* Interne Kampagnen-Trackingcodes
* Kategorien von Merchandising/Suche
* Verknüpfungen zum Crossselling

Für die Zwecke dieses Dokuments wollen wir einige eVars den Lösungen wie folgt zuordnen:

* eVar2: Interne Suchbegriffe
* eVar3: Interne Kampagnen-Trackingcodes
* eVar4: Kategorien von Merchandising/Suche
* eVar5: Verknüpfungen zum Crossselling

Wir können eine zusätzliche eVar verwenden, um die Leistung aller Methoden zur Produktsuche untereinander zu messen. Zusätzlich zu den oben beschriebenen Suchmethoden umfasst die eVar weitere Suchmethoden, z. B. Links zu Produktdetailseiten von externen Websites.

* eVar1: Methoden zur Produktsuche

Konfigurieren Sie keine dieser Variablen als Standard-eVars, sondern als Merchandising-eVars.

Um zu demonstrieren, wie Sie diese Variablen festlegen können, ist hier ein Beispiel, bei dem ein Besucher beschließt, die interne Keyword-Suche „Sandalen“ zu verwenden, um ein Produkt auf der Site zu finden. Auf der Suchergebnisseite für Suchbegriffe müssen Sie Daten in mindestens zwei eVars erfassen:

* `eVar2` entspricht dem Suchbegriff, der in der Suche verwendet wurde („Sandalen“)
* `eVar1` entspricht der verwendeten Suchmethode für das Produkt („interne Keyword-Suche“).

Wenn Sie diese beiden Variablen auf diese spezifischen Werte setzen, wissen Sie, dass der Besucher den internen Keyword-Suchbegriff „Sandalen“ verwendet, um ein Produkt zu finden. Gleichzeitig wissen Sie, dass der Besucher nicht die anderen Produktsuchmethoden verwendet, um Produkte zu finden (z. B. durchsucht er nicht die Produktkategorien, während er eine Suchbegriffsuche durchführt). Um sicherzustellen, dass eine ordnungsgemäße Zuordnung pro Produkt erfolgt, sollten diese nicht verwendeten Methoden nicht für die Suche nach einem Produkt angerechnet werden, das über eine interne Keyword-Suche gefunden wurde. Daher müssen Sie eine Logik in den Code einfügen (z. B. AppMeasurement, AEP Web SDK usw.), der die mit diesen anderen Suchmethoden verknüpften eVars automatisch auf einen Wert einer „Nicht-Suchmethode“ setzt.

Wenn ein Benutzer beispielsweise mithilfe des Suchbegriffs „Sandalen“ nach Produkten sucht, sollte die Logik des Analytics-Codes die Variablen auf der Seite mit den internen Suchergebnissen für Suchbegriffe auf die folgenden Werte setzen:

* eVar2=„Sandalen“: das Keyword „Sandalen“ wurde in der internen Keyword-Suche verwendet
* eVar1=„internal keyword search“: die Suchmethode nach internen Keywords wurde verwendet
* eVar3=„non-internal campaign“: Es wurde keine interne Kampagne für den Zugriff auf die Suchergebnisseite verwendet.
* eVar4=„non-browse“: Auf der Suchergebnisseite wurde keine Kategorie „Durchsuchen“ aufgerufen.
* eVar5=„non-cross-sell“: Auf der Seite mit den Suchergebnissen wurde kein Crossselling-Link angeklickt

## Einstellungen für Merchandising-eVars

Im Folgenden finden Sie die verschiedenen Einstellungen, die Sie mit Ihren Merchandising-eVars verwenden können. Der folgende Screenshot stammt aus dem Report Suite Manager. Greifen Sie auf sie zu, indem Sie zu [!UICONTROL Analytics] > [!UICONTROL Admin] > [!UICONTROL Report Suites] > [!UICONTROL Einstellungen bearbeiten] > [!UICONTROL Konversion] > [!UICONTROL Konversionsvariablen] > [!UICONTROL Neu hinzufügen] > [!UICONTROL Merchandising aktivieren] navigieren.

![Merch eVars](assets/merch-evars1.png)

Weitere Informationen zu diesen Einstellungen finden Sie in den Abschnitten unter der Tabelle.

| Einstellung | Beschreibung |
|--- | --- |
| Name | Der Name oder die Berichtsdimension, mit der die Variable verknüpft werden soll. Wenn `eVar1` Produktsuchmethoden erfassen soll, sollte das Feld „Name“ für `eVar1` auf „Produktsuchmethoden“ gesetzt werden. |
| Merchandising | Die Syntax, die zum Erfassen der Merchandising-eVar verwendet wird |
| Zuordnung | Hilft bei der Bestimmung der Merchandising-eVar, der eine Gutschrift zugeschrieben werden soll, wenn ein erfolgreiches Ereignis stattfindet. |
| Läuft ab nach | Bestimmt, wann bestehende Bindungen mit Produkt- und Merchandising-eVars nicht mehr wirksam sein sollten. |
| Typ | Die Art der Daten, die in der Merchandising-eVar erfasst werden |
| Merchandising-Binding-Ereignis | Die Ereignisse, die bestimmen, wann ein Produkt an den Wert einer Merchandising-eVar gebunden werden soll |
| Zurücksetzen | Ein Trigger, der zu diesem Zeitpunkt alle Backend-Daten für die eVar zurücksetzt |
| Merchandising aktivieren | Eine Markierung, die auf „Aktiviert“ gesetzt werden muss, um die eVar von einer standardmäßigen eVar in eine Merchandising-eVar zu verwandeln |

### Merchandising aktivieren

Wenn die Einstellung „Merchandising aktivieren“ auf „Aktiviert“ gesetzt ist, werden alle unten beschriebenen Einstellungen im Report Suite Manager angezeigt. Wenn die Einstellung „Merchandising aktivieren“ auf „Deaktiviert“ gesetzt ist, sind nur die Standardeinstellungen für eVars verfügbar.

### Merchandising

Diese Option ist nicht für standardmäßige eVars verfügbar. Mit der Einstellung [!UICONTROL Merchandising] können Sie als Methode zur Erfassung der Merchandising-eVar entweder [!UICONTROL Konversionsvariablensyntax] oder [!UICONTROL Produktsyntax] auswählen.

**[!UICONTROL Konversionsvariablensyntax]** bedeutet, dass Sie den Wert der eVar in einer eigenen Variablen festlegen. Mit der Konversionsvariablensyntax wird beispielsweise der `eVar1`-Wert von „internal keyword search“ im Seiten-Code (oder im AppMeasurement-Code, AEP Web SDK-Code usw.) wie folgt festgelegt:

`s.eVar1="internal keyword search";`

Bei **[!UICONTROL Produktsyntax]** wird die eVar jedoch nur innerhalb der Adobe Analytics-Produktvariablen festgelegt. Die Analytics-Produktvariable ist in sechs verschiedene Teile pro Produkt unterteilt:

`s.products="[category];[name];[quantity];[revenue];[events];[eVars]"`

* [!UICONTROL Kategorie] und [!UICONTROL Name] das angegebene Produkt identifizieren.
* [!UICONTROL Menge] und [!UICONTROL Umsatz] sind nützlich, wenn ein Produktkauf verfolgt wird.
* [!UICONTROL Ereignisse] ist nützlich für die Aufzeichnung benutzerdefinierter inkrementeller oder Währungsereigniswerte, die nicht als Umsatz gezählt werden sollen (z. B. Versandkosten, Rabatte usw.)

Merchandising-eVars, die für die Verwendung der Produktsyntax konfiguriert sind, werden im letzten Teil der Variablen „products“ festgelegt. Angenommen, ein Besucher verwendet eine interne Keyword-Suche, um die Produkt-ID „12345“ zu finden. Die produktsyntaxbasierte Methode zum Festlegen von eVar1 in diesem Beispiel würde wie folgt aussehen:

`s.products=";12345;;;;eVar1=internal keyword search";`

Beachten Sie, dass wir weiterhin durch Semikolon getrennte Platzhalter für die Bereiche „Anzahl“, „Umsatz“ und „Ereignis“ der Produktvariablen haben. Ohne diese Platzhalter würde die `eVar1`-Einstellung der internen Keyword-Suche vollständig ignoriert.

### Zuordnung

Der Begriff „Zuordnung“ für Merchandising-eVars ist irreführend, insbesondere für Merchandising-eVars, die die Konversionsvariablensyntax verwenden. Alle Standard-eVars können über eine eigene individuelle Zuordnungseinstellung verfügen. Merchandising-eVars mit Konversionsvariablensyntax verwenden jedoch nur die Zuordnungseinstellung „Zuletzt (Letzte)“, unabhängig davon, was die Zuordnungseinstellungen im Report Suite Manager zeigen.

Um zu verstehen, was diese Einstellung bewirkt, müssen Sie den Unterschied zwischen der Zuordnung von eVars und der Bindung von Merchandising-eVars verstehen. Bei Merchandising-eVars ist „Bindung von Merchandising-eVars“ ein geeigneterer Name für diese Einstellung „Zuordnung“.

#### Standardeinstellung für die Zuordnung von eVars

Wenn eVars mit Standardsyntax aus einer Bildanforderung erfasst werden, fügen die Adobe Analytics-Verarbeitungs-Server Daten in eine andere Datenbankspalte ein, die Spalte `post_evar`. Da eVars persistent sein sollen – sie laufen in den meisten Fällen irgendwann nach dem aktuellen Treffer ab – legen die Server diese Spalte `post_evar` bei jeder nachfolgenden Bildanforderung fest. Sie wird auf den letzten Wert gesetzt, der an die entsprechende eVar übergeben wurde. Bei Standard-eVars verwendet Adobe Analytics bei einem Erfolgsereignis die Spalte `post_evar` anstelle der regulären eVar, um die eVar zu bestimmen, der das Ereignis gutgeschrieben werden soll.

Bei Standard-eVars bestimmt die Zuordnungseinstellung, ob die erste oder die letzte eVar, die während eines bestimmten Zeitraums erfasst wurde, in die Spalte `post_evar` eingefügt wird. Wenn die Zuordnungseinstellung für eine Standard-eVar gleich „Ausgangswert (Erste)“ ist, wird die erste vom Besucher erfasste eVar für alle nachfolgenden Bildanforderungen in die Spalte `post_evar` eingefügt. Dies gilt für alle zukünftigen Anfragen, die vom Browser dieses Besuchers gesendet werden, bis die eVar gemäß ihrer Einstellung „Läuft ab nach“ abläuft.

Wenn die Zuordnungseinstellung einer standardmäßigen eVar gleich „Zuletzt verwendet (Letzte)“ ist, wird die neueste vom Besucher erfasste eVar für alle nachfolgenden Bildanforderungen in die Spalte `post_evar` eingefügt. Die Zuordnung „Zuletzt verwendet (Letzte)“ bedeutet, dass sich der Wert `post_evar` jedes Mal ändert, wenn die zugehörige eVar in einer Bildanforderung auf einen neuen Wert gesetzt wird. Die Zuordnung „Ausgangswert (Erste)“ bedeutet, dass sich die Spalte `post_evar` nicht über Treffer hinweg ändert, obwohl die zugehörige eVar möglicherweise in einer zukünftigen Bildanforderung auf einen anderen Wert festgelegt wird.

#### Einstellung für die Zuordnung (Bindung) von Merchandising-eVars

Wie bereits erwähnt, wird allen Merchandising-eVars mit Konversionsvariablensyntax nur die Zuordnung „Zuletzt verwendet (Letzte)“ zugewiesen. Daher wird in der Zuordnungseinstellung für Merchandising-eVars nicht festgelegt, welche Werte in die Spalte „post_evar“ eingefügt werden, da ein Besucher die Site weiterhin verwendet. Stattdessen wird durch die Zuordnungseinstellung festgelegt, welcher eVar-Wert an ein Produkt gebunden ist und wie die Erfolgsereignisse dieser Produkte wieder den eVar-Werten zugeordnet werden, an die sie gebunden sind.

Folgendes geschieht, wenn die Einstellung für die Zuordnung (d. h. Bindung) einer Merchandising-eVar auf „Ausgangswert (Erste)“ gesetzt ist: Alle Produkte, die neben der Spalte „post_evar“ gesetzt wurden und noch nicht an die entsprechende „vorverarbeitete“ eVar der Spalte „post_evar“ gebunden waren, werden an den Wert in der Spalte „post_evar“ gebunden.  Diese Bindung zwischen eVar-Wert und Produkt ändert sich erst, wenn die eVar gemäß der Einstellung für „Läuft ab nach“ in den Report Suite-Einstellungen abläuft.

Jedes Mal, wenn eine Bildanforderung die Kriterien erfüllt, die ein bereits gebundenes Produkt ansonsten an den zuletzt festgelegten eVar-Wert binden würden, zwingt die Einstellung „Ausgangswert (Erste)“ die Adobe Analytics-Datenerfassungs-Server dazu, solche weiteren Versuche zu ignorieren. Das Gegenteil geschieht mit Merchandising-eVars, bei denen die Einstellung für die Zuordnung (Bindung) gleich „Zuletzt verwendet (Letzte)“ ist. Jedes Mal, wenn eine Bildanforderung die Kriterien erfüllt, die ein Produkt an eine Merchandising-eVar binden, bindet das Produkt sich selbst an den neuesten Wert, der an die eVar übergeben wurde, oder an den Wert, der (immer) in der Spalte `post_evar` enthalten ist.

Wie bereits erwähnt, können Sie mit Merchandising-eVars Erfolgsereignisse an eVar-Werte auf Produktbasis und nicht pro Besuch/pro Bestellung zuweisen. Wenn einem gebundenen Produkt also ein Erfolgsereignis zugeordnet ist (z. B. ein Hinzufügen zum Warenkorb oder ein Kauf), wird das Erfolgsereignis sowohl dem Produkt als auch den Werten der Merchandising-eVar gutgeschrieben, an die das Produkt zu diesem Zeitpunkt gebunden ist.

### Läuft ab nach

Die Ablaufeinstellung einer Merchandising-eVar ermöglicht die Auswahl von Folgendem:

* Wann die beiden Produkt-/eVar-Bindungen ablaufen sollen und

* Ab wann die Spalte „post_evar“ nicht mehr automatisch ausgefüllt werden soll, nachdem eine eVar an eine Bildanforderung übergeben wurde.

Eine eVar kann ablaufen, wenn entweder ein Erfolgsereignis aufgezeichnet wird oder ein bestimmter Zeitraum vergangen ist. Adobe Analytics ermöglicht nur eine einzige Ablaufeinstellung pro eVar zu einer gegebenen Zeit.

Für die Suchmethode für Produkte ist die Best Practice zum Festlegen des Ablaufs einer Merchandising-eVar, sie

* ENTWEDER auf die Dauer zu setzen, über die ein Produkt im Warenkorb einer Site aufbewahrt wird, bevor die Site es automatisch aus dem Warenkorb entfernt (z. B. 14 Tage, 30 Tage usw.),
* ODER auf den Zeitpunkt des Kaufereignisses.

Mit beiden Ablaufeinstellungen werden bei jedem von einem Besucher gekauften Produkt die Werte für Bestellung/Einheiten/Umsatz den Merchandising-eVar-Werten zugeordnet, mit denen die Produkte zu diesem Zeitpunkt verbunden waren.

### Typ

Die Einstellung des eVar-Typs bestimmt, welcher Datentyp in die eVar eingefügt wird. In den meisten Fällen sollte dieser Wert gleich „Text“ sein. Die Verwendung von „Zähler“ für eine Merchandising-eVar ist selten. „Zähler“ kann jedoch verwendet werden, um einer Zähler-eVar Erfolgswerte pro Produkt zuzuweisen. Die Erörterung von Lösungen mit dem Typ „Zähler“ liegt außerhalb des Rahmens dieses Dokuments.

### Merchandising-Binding-Ereignis

Mit der Einstellung „Merchandising-Binding-Ereignis“ können Sie die Bedingungen festlegen, unter denen ein Produkt an den Wert einer Merchandising-eVar gebunden wird. Diese Bedingungen sind auf das Auslösen bestimmter Erfolgsereignisse oder eVars beschränkt. Das Auslösen von Traffic-Variablen (z. B. Props) hat keine Auswirkungen auf Merchandising-Bindungen.

Beachten Sie, dass mit der Einstellung „Merchandising-Binding-Ereignis“ ein Produkt durch mehr als ein Ereignis an eine eVar gebunden werden kann. Beispiele:

* Über ein Produktansichtsereignis
* Über das Ereignis „Zum Warenkorb hinzufügen“
* Über ein Kaufereignis

Standardmäßig wird ein Produkt durch die Einstellung an einen Merchandising-eVar-Wert gebunden, wenn ein anderes Ereignis/eine andere eVar (Merchandising oder Standard) in derselben Bildanforderung wie das Produkt enthalten ist.

### Zurücksetzen

Mit der Einstellung „Zurücksetzen“ können Sie alle eVars für alle Besucher, die derzeit einen `post_evar`-Wert in der Adobe Analytics-Backend-Datenbank haben, sofort „ablaufen“ lassen. Außerdem werden alle aktuellen Produkt-/eVar-Bindungen entfernt.

>[!IMPORTANT]
>Es wird von Adobe nicht empfohlen, die Einstellung „Zurücksetzen“ zu verwenden, es sei denn, Sie möchten die eVar vollständig mit einem völlig „sauberen Neustart“ von Daten aus dem Zeitpunkt des Zurücksetzens beginnen lassen.

## Welche Einstellungen sollten Sie verwenden?

Unter den vielen verfügbaren Einstellungskombinationen könnten Sie sich fragen, welche Einstellungen empfehlenswert sind.

Wenn Sie die „interne Keyword-Suche“ an die Produkt-ID 12345 binden möchten, wird die Variable „products“ wie folgt festgelegt:

`s.products=";12345;;;;eVar1=internal keyword search";`

Alle Erfolgsereignisse (Hinzufügen zum Warenkorb, Käufe), die gleichzeitig mit der Produkt-ID 12345 erfasst werden, werden sowohl der Produkt-ID 12345 als auch dem eVar1-Wert „interne Keyword-Suche“ zugeschrieben. Ein anderer eVar1-Wert erhält nur dann die Zuordnung der mit der Produkt-ID 12345 verknüpften Erfolgsereignisse, wenn eVar1 später in der Variablen „products“ auf einen anderen Wert festgelegt wird (neben der Produkt-ID 12345).

Beispiel:

```js
s.products=";12345;;;;eVar1=internal campaign";
```

Diese Konfiguration ändert die Bindung der Produkt-ID 12345 vom eVar1-Wert „Interne Keyword-Suche“ in den eVar1-Wert „Interne Kampagne“. Diese Bindungsänderung erfolgt auch, wenn die eVar für die Verwendung der Produktsyntax und der Zuordnungseinstellung (Bindung) „Zuletzt verwendet (Letzte)“ konfiguriert wird. Wäre die Einstellung für die Zuordnung (Bindung) stattdessen auf „Ausgangswert (Erste)“ festgelegt worden, würde das Festlegen von eVar1 auf „Interne Kampagne“ neben der Produkt-ID 12345 die Produkt-ID 12345 nicht erneut an den eVar1-Wert „Interne Kampagne“ binden. Stattdessen bliebe die Bindung mit dem ursprünglich gebundenen Wert „Interne Keyword-Suche“ bestehen.

### Herausforderungen bei der Verwendung der Produktsyntax

Ohne sorgfältige Planung können bei der Verwendung der Produktsyntax mehrere Probleme auftreten. Nehmen wir beispielsweise die Verwendung mehrerer eVars zur Verfolgung von Produktsuchmethoden auf der Website. Hier muss jede einzelne eVar der Suchmethode gleichzeitig festgelegt werden, damit eine bestimmte Suchmethode einer eVar gutgeschrieben wird (und die eVars der anderen Suchmethoden keine Gutschrift erhalten). Produktsyntax kann in solchen Szenarien verwendet werden, der resultierende Code zur Bereitstellung ist jedoch komplizierter.

Wenn wir unser ursprüngliches Beispiel „Sandalen“ verwenden und es an die Verwendung der Produktsyntax anpassen (in der Annahme, der Besucher hat ein Produkt mit der ID „Sandale123“ unter Verwendung des Keywords „Sandalen“ gefunden), muss die resultierende Variable „products“ wie folgt festgelegt werden:

`s.products=";sandal123;;;;eVar2=sandals|eVar1=internal search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell";`

Während die Syntax der Variablen „products“ in diesem Beispiel lang ist, wird jede angezeigte eVar an die Produkt-ID „Sandale123“ gebunden. Ab diesem Zeitpunkt werden alle Erfolgsereignisse (z. B. Hinzufügungen zum Warenkorb, Käufe), die gleichzeitig mit dem Produkt „Sandale123“ erfasst werden, den eVar-Werten gutgeschrieben, die zuletzt an das Produkt gebunden waren.  Dieses Code-Beispiel zeigt, ob ein Kauf von 1 Einheit des Produkts „Sandale123“ (für 79,95 USD) stattfindet, nachdem die oben genannten eVars an das Produkt „Sandale123“ gebunden waren:

```js
s.products=";sandal123;1;79.95";
s.events="purchase";
```

Die folgenden Werte weisen alle 1 Bestellung, 1 Einheit und 79,95 USD Umsatz auf:

* eVar2-Wert von „Sandalen“
* eVar1-Wert von „internal keyword search“
* eVar3-Wert von „non-internal campaign“
* eVar4-Wert von „non-browse“
* eVar5-Wert von „non-cross-sell“

Dies ist eine korrekte Zuordnung, was kein Problem darstellt. Das Hauptproblem bei diesem Ansatz besteht vielmehr darin, zu bestimmen, wie und wann die eVars für die Produktsuchmethode festgelegt werden sollen.

In den meisten Fällen mit Produktsyntax müssten die eVars für die Suchmethode auf einer Produktdetailseite festgelegt werden und nicht auf der Seite, auf der die Suchmethode tatsächlich verwendet wurde (z. B. auf der Suchergebnisseite für Suchbegriffe, auf der Durchsuchen-Seite, auf der Landingpage für interne Kampagnen usw.). Es ist vernünftig anzunehmen, dass ein Produkt erst dann wirklich „gefunden“ wurde, wenn ein Besucher in gewissem Umfang mit einem Produkt interagiert. Daher sollten diese eVars (unter Verwendung der Produktsyntax) nicht auf der Seite der Suchmethode festgelegt werden, da (normalerweise) mehrere Produkte auf diesen Seiten angezeigt werden. Wir möchten den Wert der Suchmethode nur an die Produkte binden, mit denen der Besucher interagiert hat.

Darüber hinaus können Besucher beim Anzeigen einer Suchmethodenseite entweder auf einen Link klicken, der sie zu einer einzelnen Produktdetailseite führt, oder ein einzelnes Produkt direkt von der Suchmethodenseite zum Warenkorb hinzufügen. Wenn in unserem Beispiel der Suchbegriff „Sandalen“ verwendet wird und ein Besucher das Produkt „Sandale123“ direkt von einer Suchergebnisseite aus in den Warenkorb legt, müsste der Code zur Erfassung des Hinzufügens zum Warenkorb (über das onClick-Ereignis der Schaltfläche zum Hinzufügen zum Warenkorb usw.) entweder zum Zeitpunkt des Hinzufügens zum Warenkorb dynamisch generiert werden oder direkt über den Seiten-Code oder ein Tag-Management-System „hart-codiert“ werden.  Unabhängig davon würde der Code, der in solchen Fällen ausgelöst werden soll, etwa wie folgt aussehen:

```js
s.linkTrackVars="products,events";
s.linkTrackEvents=s.events="scAdd";
s.products=";sandal123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell";
s.tl(true,"o","Cart Add")
```

Dieser Code bindet die oben angezeigten eVar-Werte ordnungsgemäß an das Produkt „Sandale123“. Um diese Werte jedoch beim Eintreten des Klickereignisses angemessen festzulegen, muss der Entwickler:

* Zur Suchergebnisseite Server-seitige Logik hinzufügen, die die Werte bestimmt, die in die eVars der Produktsuchmethode eingefügt werden müssen, und
* Die gesamte oben gezeigte Variable „products“ ohne Syntaxfehler zusammensetzen.

Wenn ein Besucher das Produkt durch Klicken auf einen Link zur Produktdetailseite „finden“ möchte, muss der Entwickler außerdem:

* Die Details der Produktsuchmethode (wie oben gezeigt) von der Suchmethodenseite an die Produktdetailseite übergeben und
* Denselben Wert der Variablen „products“ aus den Elementen neu erstellen, die gerade von der vorherigen Seite übergeben wurden.

### Wo Produktsyntax nützlich ist

Die Produktsyntax ist weiterhin nützlich, wenn

* Mit mehreren Produkten mit denselben Produkt-IDs gleichzeitig interagiert wird und
* Die eVars, die an solche Produkte gebunden werden sollen, müssen unterschiedliche Werte pro Produkt-ID aufweisen.

Viele Bekleidungsprodukte verfügen beispielsweise über „untergeordnete SKUs“, die Größe, Farbe, Stil und andere Attribute angeben. Diese Attribute trennen ein einzelnes untergeordnetes Produkt von anderen Produkten, die zum selben übergeordneten Produkt gehören. Angenommen, Sie möchten ein mittelgroßes blaues T-Shirt plus ein großes rotes T-Shirt kaufen. Angenommen, beide T-Shirts haben die übergeordnete Produkt-ID „tshirt123“ und `eVar10` wurde so konfiguriert, dass untergeordnete SKUs erfasst werden. Die auf der Kaufbestätigungsseite festgelegten Variablen würden wie folgt festgelegt:

```js
s.events="purchase";
s.products=";tshirt123;1;20;;eVar10=tshirt123-m-blue,;tshirt123;1;20;;eVar10=tshirt123-l-red";
```

In diesem Fall werden die Werte `eVar10` (childSKU) von „tshirt123-M-blau“ und „tshirt123-L-rot“ für den Kauf der jeweiligen Instanzen der Produkt-ID „tshirt123“ gutgeschrieben.

### Herausforderungen bei der Zuordnung „Zuletzt verwendet“

Bei Verwenden der Einstellung „Zuletzt verwendet (Letzte)“ für die Zuordnung (Bindung) können zusätzliche Probleme auftreten. Beim Surfen im Web kommt es oft vor, dass Besucher ein Produkt, das sie bereits angesehen und/oder zum Warenkorb hinzugefügt haben, „erneut finden“. Dies geschieht normalerweise über einen nachfolgenden Besuch oder unmittelbar vor der Entscheidung, einen Kauf abzuschließen. Angenommen, ein Besucher findet bei einem Besuch der Website das Produkt „Sandale123“ über die Keyword-Suche von „Sandalen“. Er fügt es sofort von der Suchergebnisseite aus zum Warenkorb hinzu. Der Code, der das Hinzufügen zum Warenkorb erfasst, würde wie folgt festgelegt:

```js
s.linkTrackVars="products,events";
s.linkTrackEvents=s.events="scAdd";
s.products=";sandal123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross";
```

Daher sind alle in dieser Bildanforderung angezeigten eVars an das Produkt „Sandale123“ gebunden.

Stellen Sie sich nun vor, der Besucher kauft das Produkt während dieses Besuchs nicht, kehrt aber drei Tage später auf die Site zurück, wobei das Produkt „Sandale123“ noch im Warenkorb ist. Der Besucher möchte mehr über das Produkt erfahren, bevor er den Kauf tätigt. Aber anstatt eine Keyword-Suche zu verwenden, um das Produkt zu finden, durchsucht der Besucher die Website. Er landet im Merchandising-Abschnitt „Damen“ > „Schuhe“ > „Sandalen“, direkt bevor er das Produkt „erneut findet“. Wenn er schließlich die Produktdetailseite für das Produkt „Sandale123“ erneut findet, werden die Variablen wie folgt festgelegt (beim Laden der Seite):

```js
s.events="prodView";
s.products=";sandal123;;;;eVar4=womens > shoes > sandals|eVar1=browse|eVar3=non-internal campaign|eVar2=non-search|eVar5=non-cross-sell";
```

Mit der Einstellung „Zuletzt verwendet (Letzte)“ für die Zuordnung (Bindung) wird das Produkt „Sandale123“ an vollständig andere eVar-Werte neu gebunden als ursprünglich. Wenn der Besucher dann den Kauf von „Sandale123“ abschließt, wird der Kauf außerdem vollständig diesen neu gebundenen eVar-Werten anstatt den ursprünglich gebundenen Werten gutgeschrieben!

Die Frage lautet hier: Welche eVar-Werte sollten für den Kauf berücksichtigt werden? Beachten Sie, dass der Besucher das Produkt „Sandale123“ ursprünglich über eine interne Keyword-Suche gefunden hatte. Es wurde dann direkt von der Suchergebnisseite aus zum Warenkorb hinzugefügt. Daher sollte der eVar1-Wert „internal keyword search“ (und der eVar2-Wert „Sandalen“) den Kauf angerechnet bekommen. Die Einstellungen für die Zuordnung (Bindung) wurden jedoch auf „Zuletzt verwendet (Letzte)“ festgelegt. Daher erhält stattdessen der eVar1-Wert von „Durchsuchen“ (und der eVar4-Wert von „Frauen“ > „Schuhe“ > „Sandalen“) die Gutschrift aufgrund des Kaufs. Der Grund dafür ist, dass dies die letzten Werte waren, die an „Sandale123“ gebunden waren, bevor der Besucher den Kauf abgeschlossen hatte.

Eine Lösung für dieses Problem besteht darin, die Einstellung für die Zuordnung (Bindung) der Merchandising-eVar von „Zuletzt verwendet (Letzte)“ in „Ausgangswert (Erste)“ zu ändern. Auf diese Weise wird den ursprünglichen eVar-Werten, die an das Produkt „Sandale123“ gebunden sind, der Kauf gutgeschrieben, unabhängig davon, wie oft der Besucher das Produkt „erneut findet“.

Wenn der Besucher ein Produkt zum Warenkorb hinzufügt, es jedoch nie kauft, ermöglicht der Ablauf der eVar die Bindung eines neuen Suchmethodenwerts an das Produkt. Der Ablauf der eVar sollte der Zeitdauer entsprechen, während der eine Website es einem Produkt ermöglicht, im Warenkorb zu bleiben, bevor es automatisch entfernt wird.

### Verwenden von Konversionsvariablensyntax

Kehren wir zur Frage der „Produktsyntax“ im Vergleich zur „Konversionsvariablensyntax“ zurück. Adobe hat eine einfachere Methode gefunden, um sowohl die Merchandising-eVars der Produktsuchmethode zu erfassen als auch ihre Werte an Produkte zu binden, die Besucher gefunden haben: Die Verwendung der Konversionsvariablensyntax reduziert die Implementierungsarbeit, für die die Entwickler des Kunden verantwortlich sind. Sie bietet weiterhin die gleichen – oder besseren – Informationen wie die Methode der Produktsyntax. Entwickler müssen einfach die Implementierungsanweisungen befolgen, die ihnen gegeben wurden, und der Rest des Codes kann in die Adobe AppMeasurement/AEP Web SDK-Datei eingefügt werden.

Sehen wir uns beispielsweise die empfohlene Lösung zur Verfolgung der Suchleistung nach internen Keywords an. Sie besagt, dass der Code auf der Suchergebnisseite für den Suchbegriff das gesuchte Schlüsselwort über eine Prop (z. B. prop4) und eine andere Prop (z. B. prop5) erfasst. Diese Props verfolgen die Anzahl der Ergebnisse, die bei der Suche angezeigt werden. Immer wenn eine Adobe Analytics-Bildanforderung auf der Suchergebnisseite generiert wird, verwendete sie die Datenschichtobjekte (oder den Seiten-Code), die von den Entwicklern bereitgestellt wurden, um die oben genannten Variablen (die Props) auszufüllen.

Zusätzliche Logik in der AppMeasurement/AEP Web SDK-Datei kann die restlichen Variablen (die Merchandising-eVars/Dimensionen) ausfüllen, die gleichzeitig festgelegt werden müssen.\
Wenn beispielsweise ein neuer Besucher nach „Sandalen“ sucht und 25 Ergebnisse auf der Suchergebnisseite zurückgegeben wurden, würde der auszulösende Code (über den Seiten-Code ODER die Datenschichterfassung) wie folgt aussehen:

```js
s.prop4="sandals";
s.prop5="25";
```

Die Logik in der AppMeasurement/Analytics SDK-Datei könnte diesen Code-Ausschnitt dann automatisch in Folgendes umwandeln:

```js
s.prop4="sandals";
s.prop5="25";
s.eVar2="sandals";
s.eVar1="internal keyword search";
s.eVar3="non-internal campaign";
s.eVar4="non-browse";
s.eVar5="non-cross sell";
```

Es besteht kein Grund, sich Gedanken darüber zu machen, ob Daten von Seite zu Seite weitergegeben werden und versucht werden muss, eine recht große, unhandliche Zeichenfolge zu erstellen, die in die Produktvariable eingefügt wird. Stattdessen können Entwickler ihren Teil der Tracking-Lösungen implementieren – was in die Props eingefügt wird – und den Rest der Implementierung dem benutzerdefinierten Code überlassen, der von Adobe Consulting bereitgestellt wird.

Wie bereits erläutert, haben alle Merchandising-eVars, die die Konversionsvariablensyntax verwenden, die Zuordnungseinstellung „Zuletzt verwendet (Letzte)“. Sobald eine eVar auf einen beliebigen Wert gesetzt wurde, bleibt dieser Wert über alle nachfolgenden Treffer hinweg erhalten (über die Spalte „post_evar“). Er bleibt so lange bestehen, bis er auf einen anderen Wert gesetzt wird oder bis die eVar abläuft. Daher werden alle Produkte, mit denen Benutzer interagieren, nachdem die eVars festgelegt wurden, an die in den eVar übergebenen Werte „Zuletzt verwendet (Letzte)“ gebunden, sofern sie noch nicht an diese eVars gebunden waren.

Im obigen Beispiel bleiben der `eVar2`-Wert von „Sandalen“ und der eVar1-Wert von „internal keyword search“ usw. auf allen Seiten bestehen, die nach der Keyword-Suche angezeigt wurden. Sie bleiben so lange bestehen, bis die eVars mit anderen Werten überschrieben werden. Angenommen, ein Besucher klickt auf seiner Suchergebnisseite auf einen Link zur Produktdetailseite für die Produkt-ID „Sandale123“.  Anschließend wird die Produkt-ID „Sandale123“ (sofern noch nicht gebunden) an jeden der in den Spalten „post_evar“ enthaltenen Werte oder an die eVar-Werte gebunden, die von der vorherigen Seite (Suchergebnisse) erfasst wurden.

Es gibt noch eine Sache, die mit der Syntax der Konversionsvariablen überdacht werden muss. Binding-Ereignisse müssen so eingerichtet werden, dass sie eine eVar an ein Produkt binden. Wenn Sie in einer Adobe Analytics-Bildanforderung einfach eine Merchandising-eVar neben einem Produkt (in der Variablen „products“) festlegen, wird der eVar-Wert nicht notwendigerweise an das Produkt gebunden.  Stattdessen bestimmt die Einstellung „Merchandising-Binding-Ereignis“, die im Report Suite Manager festgelegt ist, die Kriterien, die einen eVar-Wert an ein Produkt binden

Da wir die eVar-Werte der Suchmethode immer dann an Produkte binden möchten, wenn eine Produktinteraktion stattfindet – was bedeutet, dass ein Produkt „gefunden“ wurde –, können Sie davon ausgehen, dass die häufigsten „Produkt gefunden“-Interaktionen entweder eine Produktansicht sind (wenn Besucher auf eine Produktdetailseite gehen) oder eine Hinzufügung zum Warenkorb (wenn Besucher ein Produkt direkt über eine Suchmethodenseite zum Warenkorb hinzufügen). 

Daher können wir diese beiden Ereignisse (prodView, scAdd) als „grundlegende“ Merchandising-Binding-Ereignisse auswählen.
Folgendes geschieht, wenn eines dieser Binding-Ereignisse in einer Bildanforderung enthalten ist. Alle Produkt-IDs, die in derselben Anforderung enthalten sind (innerhalb der Produktvariablen) und nicht an eine Merchandising-eVar gebunden wurden, werden an die neuesten Werte gebunden, die an die Merchandising-eVar übergeben wurden (Spalten „post_evar“). Jeder Versuch, diese Produkte nach dieser ursprünglichen Bindung erneut zu binden, wird ignoriert, wenn die Einstellung für die Zuordnung (Bindung) auf „Ausgangswert (Erste)“ festgelegt ist.

### Best-Practice-Einstellungen

Im Folgenden finden Sie die Best-Practice-Einstellungen. Damit wird die Produktsuchmethode einfach mit den besten Ergebnissen implementiert. Adobe empfiehlt, dass Kunden die einzelnen Merchandising-eVars ihrer Produktsuchmethode (allgemein) wie folgt konfigurieren:

* Merchandising aktiviert: Aktiviert
* Merchandising-[Syntax]: Syntax der Konversionsvariablen
* Zuordnung der [Bindung]: Ausgangswert (Erste)
* Läuft ab nach: Die Zeit, die ein Produkt in einem Warenkorb verbleibt, bevor es automatisch entfernt wird (z. B. 14 Tage, 30 Tage usw.). Wenn keine solche Zeit vorhanden ist, läuft sie nach dem „Kauf“-Ereignis ab
* Typ: Text
* Merchandising-Binding-Ereignisse: Produktansicht, Hinzufügen zum Warenkorb und Kauf

## Was machen Binding-Ereignisse eigentlich?

Wenn ein Binding-Ereignis im selben Server-Aufruf wie die Variable „products“ enthalten ist, werden die Merchandising-eVar-Werte (unter Verwendung der Konversionsvariablensyntax) in ihrer Post-Spalte an die Variable „products“ gebunden. Angenommen, ein Server-Aufruf enthält basierend auf dem vorherigen Beispiel die folgenden Merchandising-eVar-Werte:

```js
s.eVar2="sandals";
s.eVar1="internal keyword search";
s.eVar3="non-internal campaign";
s.eVar4="non-browse";
s.eVar5="non-cross sell";
```

Wie bereits erläutert, bleiben die oben genannten eVars durch ihre jeweilige Spalte „post_evar“ über den aktuellen Treffer hinaus bestehen. Daher wandeln die Server von Adobe die oben genannten eVars in Folgendes um:

```js
post_eVar2="sandals";
post_eVar1="internal keyword search";
post_eVar3="non-internal campaign";
post_eVar4="non-browse";
post_eVar5="non-cross sell";
```

Diese Post-Spalten werden in der Adobe-Datenbank gespeichert und bleiben über den aktuellen Treffer hinaus bestehen, bei dem sie ursprünglich festgelegt wurden. Dabei wird davon ausgegangen, dass kein Ablauf oder keine Zurücksetzung der Variablen erfolgt. Auf Adobe-Servern sind diese post_evar-Werte zum Zeitpunkt der Verarbeitung künftiger Server-Aufrufe, die sowohl das Binding-Ereignis als auch die Produktvariable enthalten, „verfügbar“.

Die Bindung erfolgt ausschließlich zwischen diesen post_evar-Werten und dem Inhalt der Variablen „products“. Das Binding-Ereignis „bindet“ nicht unbedingt an die eVars oder die Variable „products“. Es ist der „Katalysator“, der die Adobe-Server anweist, die post_evar-Werte an die Produkte zu binden.

Angenommen, bei einem zukünftigen Treffer werden die folgenden Variablen festgelegt:

```js
s.products=";sandals123"
s.events="prodView";
```

Die Verarbeitungs-Server von Adobe sehen diesen Treffer in den „post_evar“-Spalten wie folgt:

```js
s.products=";sandals123";
s.events="prodView";
post_eVar2="sandals";
post_eVar1="internal keyword search";
post_eVar3="non-internal campaign";
post_eVar4="non-browse";
post_eVar5="non-cross sell";
```

Angenommen, eVar1, eVar2, eVar3, eVar4 und eVar5 wurden so konfiguriert, dass `prodView` als Binding-Ereignis verwendet wird. Wenn eine dieser eVars nicht für die Verwendung von prodView als Binding-Ereignis konfiguriert ist, erfolgt keine Bindung zwischen dieser (falsch konfigurierten) eVar und der Variablen „products“.

Die Bindung erzeugt einige sehr interessante Ergebnisse, die im Wert der Spalte „post_products“ zu sehen sind. Durch die Bindung wird der obige Code umgewandelt und einige weitere Post-Spalten wie folgt festgelegt:

```js
post_events="prodView";
post_products=";sandals123;;;;eVar2=sandals|eVar1=internal keyword search|eVar3=non-internal campaign|eVar4=non-browse|eVar5=non-cross-sell";
```

Der in der Spalte „post_products“ enthaltene Wert ist Ihnen möglicherweise bekannt. Scrollen Sie in diesem Dokument nach oben und vergleichen Sie diesen post_products-Wert mit dem s.products-Wert, wie unter dargestellt. Beachten Sie, dass die Spalte „post_products“ mithilfe der Syntax der Produktvariablen festgelegt wurde!

Das bedeutet, dass durch die Bindung die eVar-Werte der Konversionsvariablensyntax über die Produktsyntax in die Variable „products“ kopiert werden. Diese Kopieraktion findet nur statt, wenn die Variable „products“ und ein Binding-Ereignis (über die eVar-Konfiguration festgelegt) in derselben Anforderung enthalten sind. Ab diesem Zeitpunkt sind die in den Spalten „post_eVar“ enthaltenen Werte an das Produkt gebunden. Diese Bindung wird über die Produktsyntax dargestellt, die in der Spalte „post_products“ gespeichert ist.

## Merchandising-eVars, Instanzmetrik und Attribution IQ

Wenn eine standardmäßige eVar in einem Analytics-Server-Aufruf gesendet wird, wird dem Wert in der Spalte „post_evar“ immer eine Instanz zugeordnet. Instanzen stellen die Häufigkeit dar, mit der eine eVar in einer Bildanforderung auf einen bestimmten Wert gesetzt wurde.

Angenommen, `eVar10` ist eine standardmäßige eVar mit der Attribution [!UICONTROL Letztkontakt]. Wenn Sie auf einer beliebigen Seite `s.eVar10="hello world"` festlegen, wird der Wert „hello world“ an die Spalte „post_evar10“ übergeben, wenn Adobe den Treffer verarbeitet. Für jede einzelne `eVar10`-Einstellung von `hello world` ist die Instanzmetrik „1“. Beachten Sie, dass eine Instanz nicht immer aufgezeichnet wird, wenn die Spalte „post_evar“ einen Wert aufweist. Stattdessen bestimmt die Spalte „post_evar“, welcher Wert die Instanz erhält, wenn eine Instanz aufgezeichnet wird.

Instanzen für eine Merchandising-eVar geben den Werten, die die eVar sammelt, eine Zuordnung. Dies geschieht jedoch nur, wenn gleichzeitig mit einem Produkt, das an den Wert der Merchandising-eVar gebunden ist, „interagiert“ wurde.

Wenn Sie beispielsweise `s.eVar1="Internal Keyword Search"` allein festlegen, werden dem eVar1-Wert „Interne Keyword-Suche“ keine Instanzmetriken zugewiesen. Es wird jedoch in diesem Moment eine Instanz aufgezeichnet. Wenn jedoch nicht gleichzeitig mit dem Festlegen von `eVar1` ein Produkt an den Wert „Interne Keyword-Suche“ gebunden ist, wird die Instanz dem Bereich „Nicht angegeben“ zugeordnet. Mit anderen Worten, der `eVar1`-Wert von „Interne Keyword-Suche“ kann eine Instanz erhalten. Dies geschieht jedoch nur, wenn ein Produkt, das an den Wert „Interne Keyword-Suche“ gebunden ist, in der Produktvariablen in derselben Bildanforderung angezeigt wird.

Zusammenfassend lässt sich sagen, dass die vorkonfigurierte Instanzmetrik für eine Merchandising-eVar ohne zusätzliche Konfiguration wenig nützlich ist. Deshalb hat Adobe [Attribution IQ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/overview.html?lang=de) herausgebracht. Damit können Sie mehrere Attributionsmodelle auf jede benutzerdefinierte Metrik anwenden, die von Adobe Analytics erfasst wird. Metriken, die diese Attributionsmodelle anwenden, verwenden nicht die Werte in den Spalten „post_evar“ oder die Werte, die an ein bestimmtes Produkt gebunden sind. Stattdessen verwenden diese Metriken nur die Werte, die über die Bildanforderungen selbst übergeben werden (oder Werte, die über Adobe Analytics-Verarbeitungsregeln erfasst werden). Sie können die Funktionen in Attribution IQ verwenden, um eine präzise zugeordnete Instanzmetrik für alle Merchandising-eVars zu erhalten, die die Konversionsvariablensyntax verwenden.

![Attributionsauswahl](assets/attribution-select.png)

Soll eine Instanzmetrik für eine Merchandising-eVar zu einem Bericht hinzugefügt werden, ist das richtige Attribution IQ-Modell das „Letztkontakt“-Modell. Die Einstellung „Lookback-Fenster“ für das Modell spielt in diesem Fall keine Rolle. Der Grund liegt darin, dass ein „erzwungenes“ Letztkontakt-Attributionsmodell jedem einzelnen Wert, der über eine Anfrage übergeben wird, immer Instanzzuordnungen zuweist. Dies ist unabhängig davon, ob die tatsächlichen Zuordnungs-/Bindungseinstellungen der eVar auf „Zuletzt verwendet (Letzte)“ oder auf „Ausgangswert (Erste)“ festgelegt sind.
