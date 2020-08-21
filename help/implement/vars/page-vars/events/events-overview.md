---
title: events
description: Legen Sie die Ereignisvariable fest, die die meisten Metriken auf Ihrer Website steuert.
translation-type: tm+mt
source-git-commit: 2fd6e3b561d02bdbdd77b0be982614e765c870e2
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 87%

---


# events

Dimensionen und Metriken sind wichtige Komponenten für Berichte. Die `events`-Variable ist für die Datenerfassung vieler Metriken auf Ihrer Website verantwortlich. Ereignis inkrementieren [Metriken](/help/components/metrics/overview.md) normalerweise in Berichten.

Bevor Sie Ereignis implementieren, stellen Sie sicher, dass Sie sie in den Report Suite-Einstellungen unter &quot; [Erfolgseinstellungen](/help/admin/admin/c-success-events/success-event.md) &quot;erstellen und konfigurieren. Wenn Sie planen, benutzerspezifische Ereignis bei Linktracking-Treffern zu verwenden, stellen Sie sicher, dass [`linkTrackVars`](../../config-vars/linktrackvars.md) und [`linkTrackEvents`](../../config-vars/linktrackevents.md) korrekt eingestellt sind.

## Ereignisse in Adobe Experience Platform Launch

Sie können Ereignisse entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Ereignisse].

Es stehen verschiedene Funktionen zur Verfügung:

* Mithilfe einer Dropdown-Liste können Sie das Ereignis auswählen, das eingeschlossen werden soll.
* Ein optionales Textfeld zur Serialisierung. Weitere Informationen finden Sie unter [Ereignis-Serialisierung](event-serialization.md).
* Ein optionales Textfeld für einen Ereigniswert. Sie können Währung für Währungsereignisse oder eine Ganzzahl für Ereignisse ohne Währungsangaben einschließen, um sie mehrmals zu erhöhen. Wenn Sie beispielsweise `event1` unter der Dropdown-Liste auswählen und `10` in dieses Feld einschließen, wird `event1` in der Berichterstellung um 10 inkrementiert.
* Eine Schaltfläche zum Hinzufügen eines weiteren Ereignisses. Die Anzahl der Ereignisse, die Sie in einen Treffer einbeziehen können, ist gewissermaßen unbegrenzt.

## s.events in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.events`-Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Ereignissen enthält, die in den Treffer einbezogen werden sollen. Für diese Variable gibt es keine Byte-Begrenzung, daher wird sie nicht abgeschnitten. Zu gültigen Werten gehören:

* `event1` - `event1000`: Benutzerdefinierte Ereignisse, die Sie nach Belieben einstellen können. Zeichnen Sie im [Lösungsdesigndokument](../../../prepare/solution-design.md) Ihres Unternehmens auf, wie Sie die einzelnen Ereignisse verwenden. Die Anzahl der verfügbaren Ereignisse hängt vom Analytics-Vertrag Ihres Unternehmens ab. In den meisten Unternehmen, die nicht über einen Altvertrag verfügen, stehen 1000 benutzerdefinierte Ereignisse zur Verfügung. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, wenn Sie nicht sicher sind, wie viele benutzerspezifische Ereignisse für Sie verfügbar sind.
* `purchase`: Erhöht die Metrik [Bestellungen](/help/components/metrics/orders.md) um 1 und berechnet anhand der in der `products`-Variable festgelegten Werte [Einheiten](/help/components/metrics/units.md) und [Umsatz](/help/components/metrics/revenue.md). Weitere Informationen finden Sie unter [Kaufereignis](event-purchase.md).
* `prodView`: Erhöht die Metrik [Produktansichten](/help/components/metrics/product-views.md).
* `scOpen`: Erhöht die Metrik [Warenkorb](/help/components/metrics/carts.md).
* `scAdd`: Erhöht die Metrik [Zusatz zum Warenkorb](/help/components/metrics/cart-additions.md).
* `scRemove`: Erhöht die Metrik [Entnahme aus Warenkorb](/help/components/metrics/cart-removals.md).
* `scView`: Erhöht die Metrik [Warenkorbansicht](/help/components/metrics/cart-views.md).
* `scCheckout`: Erhöht die Metrik [Checkouts](/help/components/metrics/checkouts.md).

>[!NOTE]
>
>Bei dieser Variable wird zwischen Groß- und Kleinschreibung unterschieden. Vermeiden Sie die falsche Großschreibung von Ereigniswerten, um eine genaue Datenerfassung sicherzustellen.

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

>[!NOTE]
>
>Zählerereignisse unterstützen keine Währungs- oder Dezimalwerte. Verwenden Sie Währungsereignisse für Währungswerte oder numerische Ereignisse für Dezimalwerte.

### Währungsereignisse verwenden

Sie können ein benutzerspezifisches Ereignis ändern, um anstelle von Ganzzahlen eine Währung zu verwenden. Währungsereignisse werden automatisch in die Währung der Report Suite konvertiert, wenn die Währung der Report Suite und die `currencyCode`-Variable nicht übereinstimmen. Sie sind hilfreich, um Versandkosten, Rabatte oder Erstattungen zu berechnen. Sie können Währungsereignisse in der `products`-Variablen festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

Stellen Sie vor der Implementierung von Währungseinstellungen sicher, dass Sie das gewünschte Ereignis unter [Erfolgseinstellungen in den Report Suite-Einstellungen auf &quot;Währung&quot;](/help/admin/admin/c-success-events/success-event.md) setzen.

```js
// Send $9.99 USD in event1 using the events variable. Make sure the event type for event1 is Currency in Report suite settings
s.currencyCode = "USD";
s.events = "event1=9.99";

// Send $9.99 USD in event1 using the products variable. Make sure the event type for event1 is Currency in Report suite settings
s.currencyCode = "USD";
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=9.99";
```

>[!NOTE]
>
>Wenn Sie einen Währungswert sowohl in der `events`-Variable als auch in der `products`-Variable festlegen, wird der Währungswert in `events` verwendet. Vermeiden Sie das Setzen von Währungswerten sowohl in der `events`- als auch in der `products`-Variablen.

### Numerische Ereignisse verwenden

Sie können ein benutzerspezifisches Ereignis ändern, um Dezimalwerte anstelle von Ganzzahlen zu akzeptieren. Numerische Ereignisse verhalten sich ähnlich wie Währungsereignisse, verwenden jedoch keine Währungsumrechnung. Sie können numerische Ereignisse in der `products`-Variablen festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

Stellen Sie vor der Implementierung numerischer Ereignis sicher, dass Sie das gewünschte Ereignis in den Report Suite-Einstellungen unter &quot; [Erfolgseinstellungen](/help/admin/admin/c-success-events/success-event.md) &quot;auf &quot;Nummerisch&quot;setzen.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in Report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

>[!NOTE]
>
>Wenn Sie einen numerischen Wert sowohl in der `events`-Variable als auch in der `products`-Variable festlegen, wird der numerische Wert in `events` verwendet. Vermeiden Sie das Setzen von numerischen Werten sowohl in der `events`- als auch in der `products`-Variable.
