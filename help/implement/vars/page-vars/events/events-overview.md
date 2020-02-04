---
title: events
description: Legen Sie die Ereignisvariable fest, die die meisten Metriken auf Ihrer Site steuert.
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# events

Dimensionen und Metriken sind entscheidende Komponenten für Berichte. Die `events` Variable ist für die Datenerfassung vieler Metriken auf Ihrer Site verantwortlich.

## Ereignisse beim Start der Adobe Experience Platform

Sie können Ereignisse entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL Ereignisse] .

Es stehen verschiedene Funktionen zur Verfügung:

* Mithilfe einer Dropdown-Liste können Sie das Ereignis auswählen, das eingeschlossen werden soll
* Ein optionales Textfeld zur Serialisierung. See [event serialization](event-serialization.md) for more information.
* Ein optionales Textfeld für einen Ereigniswert. Sie können Währung für Währungsereignisse oder eine Ganzzahl für Ereignisse ohne Währungsangaben einschließen, um sie mehrmals zu erhöhen. Wenn Sie beispielsweise `event1` unter der Dropdown-Liste auswählen und `10` `event1` in dieses Feld einschließen, wird der Bericht um 10 inkrementiert.
* Eine Schaltfläche zum Hinzufügen eines weiteren Ereignisses. Die Anzahl der Ereignisse, die Sie in einen Treffer einbeziehen können, ist nicht angemessen begrenzt.

## s.events in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.events` Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Ereignissen enthält, die in den Treffer einbezogen werden sollen. Für diese Variable gibt es keine Bytegrenze, daher wird sie nicht abgeschnitten. Zu gültigen Werten gehören:

* `event1` - `event1000`: Benutzerspezifische Ereignisse festlegen, wie Sie möchten. Zeichnen Sie auf, wie Sie die einzelnen Ereignisse im [Lösungsdesigndokument](../../../prepare/solution-design.md)Ihres Unternehmens verwenden. Die Anzahl der verfügbaren Ereignisse hängt vom Analytics-Vertrag Ihres Unternehmens ab. Bei den meisten Organisationen mit Verträgen ohne Legacy stehen 1000 benutzerspezifische Ereignisse zur Verfügung. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, wenn Sie nicht sicher sind, wie viele benutzerspezifische Ereignisse für Sie verfügbar sind.
* `purchase`: Erhöht die Metrik &quot;Bestellungen&quot;um 1 und berechnet anhand der in der `products` Variablen festgelegten Werte &quot;Einheiten&quot;und &quot;Umsatz&quot;. Weitere Informationen finden Sie unter [Kaufereignis](event-purchase.md) .
* `prodView`: Erhöht die Metrik &quot;Produktansichten&quot;.
* `scOpen`: Erhöht die Metrik &quot;Einkaufswagen&quot;.
* `scAdd`: Erhöht die Metrik &quot;Zusatz zum Einkaufswagen&quot;.
* `scRemove`: Erhöht die Metrik &quot;Entnahme aus Warenkorb&quot;.
* `scView`: Erhöht die Metrik &quot;Einkaufswagenansichten&quot;.
* `scCheckout`: Erhöht die Metrik &quot;Kassengänge&quot;.

> [!TIP] Bei dieser Variablen wird zwischen Groß- und Kleinschreibung unterschieden. Vermeiden Sie die mangelnde Großschreibung von Ereigniswerten, um eine genaue Datenerfassung sicherzustellen.

```js
// Set the events variable to a single value
s.events = "event1";

// Set the events variable to multiple values
s.events = "event1,event13,purchase";
```

### Zählerereignisse mehrmals erhöhen

Sie können benutzerspezifische Ereignisse bei Bedarf mehrmals zählen. Weisen Sie dem gewünschten Ereignis in der Zeichenfolge eine Ganzzahl zu. In den Report Suite-Einstellungen erstellte Ereignisse sind standardmäßig Zählerereignisse.

```js
// Count event1 ten times
s.events = "event1=10";

// Count event1 twice and event2 once
s.events = "event1=2,event2";
```

> [!NOTE] Zählerereignisse unterstützen keine Währungs- oder Dezimalwerte. Verwenden Sie Währungsereignisse für Währungsereignisse oder numerische Ereignisse für Dezimalwerte.

### Währungsereignisse verwenden

Sie können ein benutzerspezifisches Ereignis ändern, um anstelle von Ganzzahlen eine Währung zu verwenden. Währungsereignisse werden automatisch in die Währung der Report Suite konvertiert, wenn die Währung der Report Suite und die `currencyCode` Variable nicht übereinstimmen. Sie sind hilfreich, um Versandkosten, Rabatte oder Erstattungen zu berechnen. Sie können Währungsereignisse in der `products` Variablen festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

```js
// Send $9.99 USD in event1 using the events variable. Make sure the event type for event1 is Currency in report suite settings
s.currencyCode = "USD";
s.events = "event1=9.99";

// Send $9.99 USD in event1 using the products variable. Make sure the event type for event1 is Currency in report suite settings
s.currencyCode = "USD";
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=9.99";
```

> [!NOTE] Wenn Sie einen Währungswert sowohl in der `events` Variablen als auch in der `products` Variablen festlegen, wird der Währungswert in verwendet `events` . Vermeiden Sie es, Währungswerte sowohl in den Variablen `events` als auch in den `products` Variablen festzulegen.

### Numerische Ereignisse verwenden

Sie können ein benutzerdefiniertes Ereignis ändern, um Dezimalwerte anstelle von Ganzzahlen zu akzeptieren. Numerische Ereignisse verhalten sich ähnlich wie Währungsereignisse, es sei denn, sie verwenden keine Währungsumrechnung. Sie können numerische Ereignisse in der `products` Variablen festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

> [!NOTE] Wenn Sie einen numerischen Wert sowohl in der `events` Variablen als auch in der `products` Variablen festlegen, wird der numerische Wert in verwendet `events` . Legen Sie keine numerischen Werte sowohl in den Variablen `events` als auch in den `products` Variablen fest.
