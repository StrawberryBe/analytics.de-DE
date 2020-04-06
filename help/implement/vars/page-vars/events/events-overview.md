---
title: events
description: Legen Sie die Ereignisvariable fest, die die meisten Metriken auf Ihrer Website steuert.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# events

Dimensionen und Metriken sind wichtige Komponenten für Berichte. Die `events`-Variable ist für die Datenerfassung vieler Metriken auf Ihrer Website verantwortlich.

## Ereignisse in Adobe Experience Platform Launch

Sie können Ereignisse entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Rules] tab, then click the desired rule (or create a rule).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Locate the [!UICONTROL Events] section.

Es stehen verschiedene Funktionen zur Verfügung:

* Mithilfe einer Dropdown-Liste können Sie das Ereignis auswählen, das eingeschlossen werden soll.
* Ein optionales Textfeld zur Serialisierung. Weitere Informationen finden Sie unter [Ereignis-Serialisierung](event-serialization.md).
* Ein optionales Textfeld für einen Ereigniswert. Sie können Währung für Währungsereignisse oder eine Ganzzahl für Ereignisse ohne Währungsangaben einschließen, um sie mehrmals zu erhöhen. Wenn Sie beispielsweise `event1` unter der Dropdown-Liste auswählen und `10` in dieses Feld einschließen, wird `event1` in der Berichterstellung um 10 inkrementiert.
* Eine Schaltfläche zum Hinzufügen eines weiteren Ereignisses. Die Anzahl der Ereignisse, die Sie in einen Treffer einbeziehen können, ist gewissermaßen unbegrenzt.

## s.events in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.events`-Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Ereignissen enthält, die in den Treffer einbezogen werden sollen. Für diese Variable gibt es keine Byte-Begrenzung, daher wird sie nicht abgeschnitten. Zu gültigen Werten gehören:

* `event1` - `event1000`: Benutzerdefinierte Ereignisse, die Sie nach Belieben einstellen können. Zeichnen Sie im [Lösungsdesigndokument](../../../prepare/solution-design.md) Ihres Unternehmens auf, wie Sie die einzelnen Ereignisse verwenden. Die Anzahl der verfügbaren Ereignisse hängt vom Analytics-Vertrag Ihres Unternehmens ab. In den meisten Unternehmen, die nicht über einen Altvertrag verfügen, stehen 1000 benutzerdefinierte Ereignisse zur Verfügung. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, wenn Sie nicht sicher sind, wie viele benutzerspezifische Ereignisse für Sie verfügbar sind.
* `purchase`: Erhöht die Metrik „Bestellungen“ um 1 und berechnet anhand der in der `products`-Variablen festgelegten Werte „Einheiten“ und „Umsatz“. Weitere Informationen finden Sie unter [Kaufereignis](event-purchase.md).
* `prodView`: Erhöht die Metrik „Produktansichten“.
* `scOpen`: Erhöht die Metrik „Warenkorb“.
* `scAdd`: Erhöht die Metrik „Zusätze zum Warenkorb“.
* `scRemove`: Erhöht die Metrik „Entnahmen aus Warenkorb“.
* `scView`: Erhöht die Metrik „Warenkorbansichten“.
* `scCheckout`: Erhöht die Metrik „Checkouts“.

>[!NOTE] Bei dieser Variablen wird zwischen Groß- und Kleinschreibung unterschieden. Vermeiden Sie die falsche Großschreibung von Ereigniswerten, um eine genaue Datenerfassung sicherzustellen.

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

>[!NOTE] Zählerereignisse unterstützen keine Währungs- oder Dezimalwerte. Verwenden Sie Währungsereignisse für Währungswerte oder numerische Ereignisse für Dezimalwerte.

### Währungsereignisse verwenden

Sie können ein benutzerspezifisches Ereignis ändern, um anstelle von Ganzzahlen eine Währung zu verwenden. Währungsereignisse werden automatisch in die Währung der Report Suite konvertiert, wenn die Währung der Report Suite und die `currencyCode`-Variable nicht übereinstimmen. Sie sind hilfreich, um Versandkosten, Rabatte oder Erstattungen zu berechnen. Sie können Währungsereignisse in der `products`-Variablen festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

```js
// Send $9.99 USD in event1 using the events variable. Make sure the event type for event1 is Currency in report suite settings
s.currencyCode = "USD";
s.events = "event1=9.99";

// Send $9.99 USD in event1 using the products variable. Make sure the event type for event1 is Currency in report suite settings
s.currencyCode = "USD";
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=9.99";
```

>[!NOTE] Wenn Sie einen Währungswert sowohl in der `events`-Variablen als auch in der `products`-Variablen festlegen, wird der Währungswert in `events` verwendet. Vermeiden Sie das Setzen von Währungswerten sowohl in der `events`- als auch in der `products`-Variablen.

### Numerische Ereignisse verwenden

Sie können ein benutzerspezifisches Ereignis ändern, um Dezimalwerte anstelle von Ganzzahlen zu akzeptieren. Numerische Ereignisse verhalten sich ähnlich wie Währungsereignisse, verwenden jedoch keine Währungsumrechnung. Sie können numerische Ereignisse in der `products`-Variablen festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

>[!NOTE] Wenn Sie einen numerischen Wert sowohl in der `events`-Variablen als auch in der `products`-Variablen festlegen, wird der numerische Wert in `events` verwendet. Vermeiden Sie das Setzen von numerischen Werten sowohl in der `events`- als auch in der `products`-Variablen.
