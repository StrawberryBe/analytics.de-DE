---
description: Liste mit vordefinierten Ereignissen.
keywords: Analytics-Implementierung; Ereignis
seo-description: Liste mit vordefinierten Ereignissen.
seo-title: Was ist ein vordefiniertes Ereignis?
solution: Analytics
title: Was ist ein vordefiniertes Ereignis?
topic: Entwickler und Implementierung
uuid: 4 d 0799 ba -0 f 97-42 c 3-a 620-36 c 03 f 9995 da
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

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

