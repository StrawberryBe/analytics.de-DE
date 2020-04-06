---
title: linkExternalFilters
description: Verwenden Sie die Variable „linkExternalFilters“, um das automatische Tracking von Exitlinks zu unterstützen.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkExternalFilters

AppMeasurement bietet die Möglichkeit, Links, die auf eine Stelle außerhalb Ihrer Website verweisen, automatisch zu verfolgen. If [`trackExternalLinks`](trackexternallinks.md) is enabled, an image request is sent to Adobe right as a visitor clicks a link to leave your site. Die Variablen `linkExternalFilters` und [`linkInternalFilters`](linkinternalfilters.md) bestimmen, welche Links als intern/extern betrachtet werden.

Wenn diese Variable einen Wert enthält, verhält sich das automatische Tracking von Exitlinks wie eine Whitelist-Variante. Wenn ein Link-Klick keinem `linkExternalFilters`-Wert entspricht, wird er nicht als Exitlink betrachtet. Die gesamte URL wird mit dieser Variablen verglichen. If [`linkLeaveQueryString`](linkleavequerystring.md) is enabled, the query string is also examined.

>[!TIP] Verwenden Sie diese Variable nur, wenn Sie genau wissen, welche Domänen Sie als Exitlinks betrachten möchten. Viele Unternehmen stellen fest, dass die Verwendung von `linkInternalFilters` für das Tracking von Exitlinks ausreicht, und verwenden `linkExternalFilters` nicht.

Wenn Sie sowohl `linkInternalFilters` als auch `linkExternalFilters` gleichzeitig verwenden, muss der geklickte Link mit `linkExternalFilters`**übereinstimmen und** darf nicht mit `linkInternalFilters` überstimmen, um als Exitlink betrachtet zu werden. Wenn ein geklickter Link sowohl den Kriterien für Exitlinks als auch für Downloadlinks entspricht, hat der Downloadlink-Typ Priorität.

## Ausgehende Links – Verfolgen in Adobe Experience Platform Launch

The Track field is a comma-separated list of filters (usually domains) under the [!UICONTROL Link Tracking] accordion when configuring the Adobe Analytics extension.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Link Tracking] Akkordeon, das das [!UICONTROL Outbound Links - Track] Feld aufdeckt.

Platzieren Sie Filter, die Sie immer als extern betrachten wollen, in diesem Feld. Trennen Sie mehrere Domänen durch ein Komma ohne Leerzeichen.

## s.linkExternalFilters in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.linkExternalFilters`-Variable ist eine Zeichenfolge mit Filtern (z. B. Domänen), die Sie als Exitlinks betrachten. Trennen Sie mehrere Domänen durch ein Komma ohne Leerzeichen.

```js
s.linkExternalFilters = "example.com,example.net,example.org";
```

Betrachten Sie das folgende Implementierungsbeispiel, als ob es auf `adobe.com` wäre:

```html
<script>
  s.trackExternalLinks = true;
  s.linkExternalFilters = "example.com,example.net";
</script>

<!-- The following link is NOT considered an exit link, even though the link is outside adobe.com -->
<a href = "example.org">Example link 1</a>

<!-- The following link is an exit link because it matches the linkExternalFilters whitelist -->
<a href = "example.com">Example link 2</a>
```
