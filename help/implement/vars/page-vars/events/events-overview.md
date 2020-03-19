---
title: events
description: Legen Sie die Variable "Ereignis"fest, die die meisten Metriken auf Ihrer Site steuert.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# events

Dimensionen und Metriken sind entscheidende Komponenten für Berichte. Die `events` Variable ist für die Datenerfassung vieler Metriken auf Ihrer Site verantwortlich.

## Ereignis beim Starten der Adobe Experience Platform

Sie können Ereignis entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Locate the [!UICONTROL Events] section.

Es stehen verschiedene Funktionen zur Verfügung:

* Mithilfe einer Dropdown-Liste können Sie das Ereignis auswählen, das einbezogen werden soll
* Ein optionales Textfeld zur Serialisierung. See [event serialization](event-serialization.md) for more information.
* Ein optionales Textfeld für einen Ereignis-Wert. Sie können für Währungseinheiten Ereignisse oder für Ereignis ohne Währung eine Ganzzahl angeben, um sie mehrmals zu erhöhen. Wenn Sie beispielsweise `event1` unter der Dropdown-Liste auswählen und `10` `event1` in dieses Feld einschließen, wird der Berichte um 10 erhöht.
* Eine Schaltfläche zum Hinzufügen eines weiteren Ereignisses. Die Anzahl der Ereignis, die Sie in einen Treffer einbeziehen können, ist nicht angemessen begrenzt.

## s.Ereignis in AppMeasurement und Starten des benutzerdefinierten Codeeditors

Die `s.events` Variable ist eine Zeichenfolge, die eine kommagetrennte Liste von Ereignissen enthält, die in den Treffer einbezogen werden sollen. Für diese Variable gibt es keine Bytegrenze, daher wird sie nicht abgeschnitten. Zu gültigen Werten gehören:

* `event1` - `event1000`: Benutzerdefinierte Ereignis, die Sie nach Belieben festlegen möchten. Zeichnen Sie auf, wie Sie die einzelnen Ereignis im [Lösungsdesign-Dokument](../../../prepare/solution-design.md)Ihres Unternehmens verwenden. Die Anzahl der verfügbaren Ereignis hängt vom Analytics-Vertrag Ihres Unternehmens ab. Die meisten Organisationen mit Verträgen ohne Legacy-Vertrag verfügen über 1000 benutzerdefinierte Ereignis. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, wenn Sie nicht sicher sind, wie viele benutzerspezifische Ereignis für Sie verfügbar sind.
* `purchase`: Erhöht die Metrik &quot;Bestellungen&quot;um 1 und berechnet anhand der in der `products` Variablen festgelegten Werte &quot;Einheiten&quot;und &quot;Umsatz&quot;. Weitere Informationen finden Sie unter [Ereignis](event-purchase.md) erwerben.
* `prodView`: Erhöht die Metrik &quot;Ansichten des Produkts&quot;.
* `scOpen`: Erhöht die Metrik &quot;Einkaufswagen&quot;.
* `scAdd`: Erhöht die Metrik &quot;Zusatz zum Einkaufswagen&quot;.
* `scRemove`: Erhöht die Metrik &quot;Entnahme aus Warenkorb&quot;.
* `scView`: Erhöht die Metrik &quot;Ansichten aus Warenkorb&quot;.
* `scCheckout`: Erhöht die Metrik &quot;Kassengänge&quot;.

> [!NOTE] Bei dieser Variablen wird zwischen Groß- und Kleinschreibung unterschieden. Vermeiden Sie die mangelnde Großschreibung von Ereignis-Werten, um eine genaue Datenerfassung sicherzustellen.

```js
// Set the events variable to a single value
s.events = "event1";

// Set the events variable to multiple values
s.events = "event1,event13,purchase";
```

### Zähler-Ereignis mehrmals erhöhen

Sie können benutzerspezifische Ereignis bei Bedarf mehrmals zählen. Weisen Sie dem gewünschten Ereignis innerhalb der Zeichenfolge eine Ganzzahl zu. In den Report Suite-Einstellungen erstellte Ereignis sind standardmäßig Zähler-Ereignis.

```js
// Count event1 ten times
s.events = "event1=10";

// Count event1 twice and event2 once
s.events = "event1=2,event2";
```

> [!NOTE] Zähler-Ereignis unterstützen keine Währungs- oder Dezimalwerte. Verwenden Sie Währungswerte oder numerische Ereignis für Dezimalwerte.

### Währungs-Ereignis verwenden

Sie können ein benutzerdefiniertes Ereignis ändern, um anstelle von Ganzzahlen eine Währung zu verwenden. Währungs-Ereignis werden automatisch in die Währung der Report Suite konvertiert, wenn die Report Suite und die `currencyCode` Variable nicht übereinstimmen. Sie sind hilfreich, um Versandkosten, Rabatte oder Rückerstattungen zu berechnen. Sie können in der `products` Variablen Währungswerte festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

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

### Numerische Ereignis verwenden

Sie können ein benutzerdefiniertes Ereignis ändern, das anstelle von Ganzzahlen Dezimalwerte akzeptiert. Numerische Ereignis verhalten sich ähnlich wie Währungs-Ereignis, es sei denn, sie verwenden keine Währungsumrechnung. Sie können numerische Ereignis in der `products` Variablen festlegen, wenn Sie das Ereignis nur diesem Produkt zuordnen möchten.

```js
// Send 4.5 in event1 using the events variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1=4.5";

// Send 4.5 in event1 using the products variable. Make sure the event type for event1 is Numeric in report suite settings
s.events = "event1";
s.products = "Example category;Example product;1;0;event1=4.5";
```

> [!NOTE] Wenn Sie einen numerischen Wert sowohl in der `events` Variablen als auch in der `products` Variablen festlegen, wird der numerische Wert in verwendet `events` . Legen Sie keine numerischen Werte sowohl in den Variablen `events` als auch in den `products` Variablen fest.
