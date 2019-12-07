---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Listenvariable

Wird auch als „List Var“ bezeichnet. Ähnlich wie bei Listen-Props sind bei Listenvariablen mehrere Werte in derselben Bildanforderung möglich. Sie funktionieren auch ähnlich wie eVars, die über die Bildanforderung hinaus erhalten bleiben, für die sie definiert wurden. Sie können mit diesen Variablen bei vielen Elementen auf einer einzelnen Seite Ursache und Wirkung erkennen (z. B. bei Produktlisten, Wunschlisten, Listen mit Sucheinschränkungen oder Listen mit Display-Anzeigen).


<!-- 

listN.xml (bob edit)

 -->

**Zu beachten**

* Listenvariablen speichern ihre jeweiligen Werte durch Verweis auf das VisitorID-Cookie im Browser des Besuchers.
* Maximal 250 Werte werden gleichzeitig pro Besucher gespeichert. Wenn 250 Werte pro Besucher überschritten werden, so werden die letzten 250 Werte verwendet. Der Ablauf dieser Werte basiert auf dem für die Variable konfigurierten Ablauf.
* Jeder durch ein Trennzeichen begrenzte Wert kann maximal 255 Zeichen (bei Multibytezeichen weniger) enthalten. Dies ist die maximale Länge jedes Elements.
* Innerhalb dieser Variable gibt es keine Begrenzung für die Zeichenanzahl. Die einzige Ausnahme dabei gilt für ältere Versionen von Internet Explorer, in denen URL-Anforderungen maximal 2.083 Zeichen lang sein dürfen.
* Insgesamt sind pro Report Suite drei Listenvariablen verfügbar.
* Für Listenvariablen ist H23-Code oder höher erforderlich.
* Listenvariablen können klassifiziert werden.
* Wenn Werte in einer Bildanforderung doppelt definiert sind, deduplizieren Listenvariablen alle Instanzen dieser Werte.
* Die gröbste Segmentierung, die bei Listenvariablen möglich ist, erfolgt auf Hitebene (oder Seitenansichtsebene). Wenn in einer Bildanforderung eine Listenvariable mit drei Werten vorhanden ist und eine beliebige Segmentregel auf einen der Werte zutrifft, werden alle drei Werte in die Berichterstellung aufgenommen. Umgekehrt gilt, wenn eine Ausschlussregel definiert ist, die mit einem der Werte übereinstimmt, werden alle drei Werte ausgeschlossen.

**Konfiguration** {#section_8CADFF581D2447518BA3F7F79B2D80A9}

Sie können über die Admin Console auf die Konfiguration zugreifen und sie aktualisieren, ohne dabei die Hilfe des Adobe Kundendiensts in Anspruch zu nehmen:

1. Navigieren Sie zu: **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**
1. Wählen Sie die Report Suite aus.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** &gt; **[!UICONTROL Konversion]** &gt; **[!UICONTROL Listenvariablen]**.

* **Name**: Jeder durch ein Trennzeichen begrenzte Wert kann maximal 255 Zeichen (bei Multibytezeichen weniger) enthalten. Dies ist die maximale Länge jedes Elements.
* **Trennzeichen für Werte**: Das Zeichen, mit dem Werte in der Listenvariable voneinander getrennt werden. Häufig handelt es sich dabei um Zeichen wie Komma, Doppelpunkt, senkrechter Strich (Pipe) usw.

   >[!NOTE]
   >
   >Multi-Byte-Zeichen werden als Trennzeichen in Listenvariablen nicht unterstützt. Das Trennzeichen muss ein Single-Byte-Zeichen sein.

* **Ablauf**: Bestimmt, ähnlich wie beim eVar-Ablaufdatum, den Zeitraum, der zwischen der Listenvariable und dem zugehörigen Konversionsereignis liegen kann.

   * **Auf Seitenansichts- oder Besuchsebene**: Erfolgsereignisse außerhalb der Seitenansicht oder des Besuchs werden nicht wieder mit Werten in der Listenvariablen verknüpft.
   * **Auf Basis eines Zeitraums (Tag, Woche, Monat usw.)**: Erfolgsereignisse außerhalb des angegebenen Zeitraums werden nicht wieder mit Werten in der Listenvariablen verknüpft. Hier kann auch eine benutzerspezifische Anzahl von Tagen festgelegt werden.
   * **Bestimmte Konversionsereignisse**: Alle anderen Erfolgsereignisse, die nach dem angegebenen Ereignis ausgelöst werden, werden nicht wieder mit Werten in der Listenvariable verknüpft.
   * **Nie**: Zwischen der Listenvariablen und dem Erfolgsereignis kann ein beliebiger Zeitraum vergehen.

* **Zuordnung**: Diese Einstellung gibt vor, wie Erfolgsereignisse Gutschriften auf Werte aufteilen:

   * **Vollständig**: Erfolgsereignisse werden in allen Variablenwerten, die vor dem Ablauf der Variablen definiert sind, vollständig gutgeschrieben.
   * **Linear**: Konversionsereignisse werden in allen Variablenwerten, die vor dem Ablauf der Variablen definiert sind, aufgeteilt gutgeschrieben.
   * Variablenwerte werden niemals überschrieben, sondern die Gutschriften werden zu den Werten, in denen Erfolgsereignisse gutgeschrieben werden, hinzugefügt.

* **Höchstwerte**: Gibt die Anzahl der für diese Listenvariable zulässigen aktiven Werte an. Wenn dieser Wert z. B. auf „3“ gesetzt ist, werden nur die letzten drei erfassten Werte gespeichert, und alle vorhergehenden Werte werden verworfen. Beachten Sie, dass beim Senden von mehreren Werten innerhalb eines Treffers für dieselbe Listenvariable und wenn Sie einen Höchstwert festgelegt haben, jeder Wert mit demselben Zeitstempel versehen wird und nicht sicher ist, welcher Wert gespeichert wird.

   Maximal 250 Werte werden gleichzeitig pro Besucher gespeichert. Wenn 250 Werte pro Besucher überschritten werden, so werden die letzten 250 Werte verwendet. Der Ablauf dieser Werte basiert auf dem für die Variable konfigurierten Ablauf.

   Die Höchstwert-Einstellung kann dazu verwendet werden, die Attribuierung auf eine bestimmte Anzahl von Werten zu begrenzen. Wenn eine Listenvariable auf der ersten Seite eines Besuchs z. B. auf „A,B,C“ und auf der nächsten Seite auf „X,Y,Z“ gesetzt ist, wird die Attribuierung basierend auf der Zuordnung auf diese sechs Werte verteilt. Wenn Sie die Attribuierung nur auf „X,Y,Z“ begrenzen möchten, können Sie den Höchstwert auf „3“ setzen.

Um Listenvariablen einzurichten oder zu bearbeiten, navigieren Sie zu **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; **[!UICONTROL Einstellungen bearbeiten]** &gt; **[!UICONTROL Konversion]** &gt; **[!UICONTROL Listenvariablen]**.

**Implementierungsbeispiele** {#section_564AFE6A2F524BFEB372EC0F7FEBA656}

In den folgenden Beispielen wird ein Komma als Trennzeichen für Werte verwendet.

**Definieren eines einzelnen Werts in einer Listenvariable:**

```js
s.list1="Cat";
```

**Übergeben von mehreren Werten:**

```js
s.list2="Tabby,Persian,Siamese"; 
s.list1="Product 1,Product 2,Product 3";
```

**Zuweisung des Umsatzes zu einer Listenvariable:**

```js
//Define this code on the landing page: 
s.list3="Top Banner Ad,Side Bar Ad,Internal Campaign 1"; 
 
//Have these variables fire on the purchase confirmation page: 
s.products=";Kitten;1;50" 
s.events="purchase";
```

Dieses Ergebnis zeigt drei Zeileneinträge mit jeweils 50 USD Umsatz an (Top Banner Ad, Side Bar Ad und Internal Campaign 1). Beachten Sie, dass bei der Gesamtsumme dieses Berichts der Umsatz dedupliziert wird, daher würde die Gesamtsumme auch 50 USD betragen.

**Zuweisung des Umsatzes zu einer Listenvariable, die während eines Besuchs mehrmals festgelegt wurde:**

**Zuordnung**: Vollständig

**Ablauf**: Besuch

<table id="table_09E1879B44624A858555449E2DC74E69"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Seite </th> 
   <th colname="col2" class="entry"> s.list1 </th> 
   <th colname="col3" class="entry"> s.events/s.products </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Seite 1 </td> 
   <td colname="col2"> <code> s.list1="value1,value2,value3"; </code> </td> 
   <td colname="col3"> (Nicht festgelegt) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Seite 2 </td> 
   <td colname="col2"> <code> s.list1="value4,value5,value6"; </code> </td> 
   <td colname="col3"> <p> <code> s.events="purchase"; </code> </p> <p> <code> s.products=";product;1;200" </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ergebnis**: Der Einkauf wird in allen Werten in der Listenvariablen1, die während des Besuchs festgelegt wurden (value1, value2, value3, value4, value5, value6), vollständig gutgeschrieben.

