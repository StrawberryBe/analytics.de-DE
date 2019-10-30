---
description: Liste mit vordefinierten Ereignissen.
keywords: Analytics-Implementierung;Ereignis
seo-description: Liste mit vordefinierten Ereignissen.
seo-title: Was ist ein vordefiniertes Ereignis?
solution: Analytics
title: Was ist ein vordefiniertes Ereignis?
topic: Entwickler und Implementierung
uuid: 4d0799ba-0f97-42c3-a620-36c03f9995da
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Was ist ein vordefiniertes Ereignis?

Liste mit vordefinierten Ereignissen.

| prodView | Das Erfolgsereignis tritt auf, wenn ein Besucher ein Produkt anzeigt. |
|---|---|
| scView | Das Erfolgsereignis tritt auf, wenn ein Warenkorb angezeigt wird. |
| scOpen | Das Erfolgsereignis tritt auf, wenn ein Besucher den Warenkorb zum ersten Mal öffnet. |
| scAdd | Das Erfolgsereignis tritt auf, wenn dem Warenkorb ein Produkt hinzugefügt wird. |
| scRemove | Das Erfolgsereignis tritt auf, wenn einem Warenkorb ein Artikel entnommen wird. |
| scCheckout | Das Erfolgsereignis tritt auf der ersten Seite eines Checkout auf. |
| purchase | Das Erfolgsereignis tritt auf der letzten Seite eines Checkout-Vorgangs auf (enthält „Umsatz“, „Bestellungen“ und „Einheiten“). |

Wenn eines der oben genannten vordefinierten Ereignisse auftritt, wird eine Instanz des Ereignisses inkrementiert. Sie können die Konversionsmetriken zu dem Ereignis in verschiedenen Berichten anzeigen. Das folgende Beispiel zeigt Code, mit dem vordefinierte Ereignisse konfiguriert werden.

```js
s.events="scAdd"
```

```js
s.events="scOpen,scAdd"
```

* Im Beispiel oben ist *`scAdd`* der Wert des Ereignisses. Sobald ein Artikel dem Warenkorb hinzugefügt wird, wird das Ereignis inkrementiert.
* Im zweiten Beispiel werden zwei Werte gleichzeitig erfasst. Treten auf einer Seite mehrere Erfolgsereignisse auf, wird jedes Ereignis inkrementiert.

