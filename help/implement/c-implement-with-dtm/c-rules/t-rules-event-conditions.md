---
description: Die Bedingungen bestimmen, ob eine ereignisbasierte Regel ausgelöst wird.
keywords: Dynamisches Tag-Management;Regel;Regel erstellen;Neue Regel;ereignisbasierte Regel;Linkaktivierung verzögern;Ereignishandler direkt auf Element anwenden;Bubbling;Ereignisblasen
seo-description: Die Bedingungen bestimmen, ob eine ereignisbasierte Regel ausgelöst wird.
seo-title: Bedingungen für ereignisbasierte Regeln erstellen
solution: Experience Cloud, Analytics, Target, Dynamisches Tag-Management
title: Bedingungen für ereignisbasierte Regeln erstellen
uuid: a847391c-5aec-4d64-8a35-388587731598
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Bedingungen für ereignisbasierte Regeln erstellen

Die Bedingungen bestimmen, ob eine ereignisbasierte Regel ausgelöst wird.

1. Wählen Sie die Art der Interaktion aus, die Sie verfolgen möchten, z. B. Mausklicks oder Senden eines Formulars.  

   ![](assets/condition-event-based.png)

   Weitere Informationen finden Sie unter [Ereignistypen](https://marketing.adobe.com/resources/help/en_US/dtm/event_types.html) in der Produktdokumentation zum Dynamic Tag Management.

1. Aktivieren Sie nach Bedarf die folgenden Optionen:

   | Element | Beschreibung |
   |--- |--- |
   | Linkaktivierung verzögern | Aktivieren, wenn das Ereignis einen Link aktiviert und Sie wünschen, dass der Link verzögert wird, bis das Ereignis ausgelöst werden kann. |
   | Ereignishandler direkt auf Element anwenden | Der Ereignishandler wird direkt auf das spezifische Element angewendet, auf das die Ausrichtung erfolgt. Diese Einstellung ist mit dem Bubbling- und Ebenen-Konzept in einem Browser verknüpft. |

   For example, when you click an image inside an anchor tag like `<a href="abc.html"><img src="xyz.png"/></a>`, you might expect the click to be associated with the anchor tag, because the tag is in the bubble stream. However, when you inspect the click in the developer tools, the click may actually affect only the `<img>` tag. To ensure that the event is handled correctly, associate the click with the `<img>` tag and do not depend on the browser to bubble up the click to a parent element. An event like a click can potentially bubble up to `<body>`. Es ist daher wichtig zu verstehen, an welche Einstellung das Ereignis tatsächlich gebunden ist, und diese zielgerichtet anzusprechen, um sicherzugehen, dass die Regel korrekt ausgelöst wird.

   *Bubbling* bedeutet, dass das Ereignis zuerst von dem innersten Element erfasst und behandelt wird und anschließend an übergeordnete Elemente weitergegeben wird.

1. Geben Sie den Namen des Tags an, das Sie verfolgen möchten, sowie zusätzliche Eigenschaften, über die das Tag verfügt und die Sie abgleichen möchten.  

   ![](assets/condition-event-based2.png)

   Informationen zum Auffinden des richtigen Element-Tags finden Sie unter [Using the CSS Selector](https://marketing.adobe.com/resources/help/en_US/dtm/css-selector.html) (Verwenden des CSS-Selektors) in der Produktdokumentation für das Dynamic Tag Management.

1. Wählen Sie zusätzliche Kriterien oder Bedingungstypen aus, die Sie an die Regel binden möchten, oder richten Sie sie ein.

   ![](assets/condition-event-based3.png)

1. Legen Sie Ihre bevorzugte Eventbubbling-Einstellung fest.

   Eventbubbling ist eine Möglichkeit der Ereignisübergabe im HTML-DOM.

   | Wenn Sie ... | Option verwenden |
   |--- |--- |
   | Sie möchten zugehörige Interaktionen in untergeordneten Elementen des Regel-Selektors zulassen, den Sie als Auslöser der Regel angegeben haben. | Eventbubbling für untergeordnete Elementen zulassen. |
   | Sie möchten das Bubbling verhindern, wenn das untergeordnete Element bereits ein eigenes Ereignis auslöst. | Nicht zulassen, wenn untergeordnetes Element bereits ein Ereignis auslöst. |
   | Sie möchten nicht, dass die Ereignisse im ausgewählten Regel-Selektor in der Ereignishierarchie das Element selbst übersteigen. | Eventbubbling zu übergeordneten Elementen nicht zulassen. |
