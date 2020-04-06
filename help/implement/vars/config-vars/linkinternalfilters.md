---
title: linkInternalFilters
description: Verwenden Sie die Variable „linkInternalFilters“, um das automatische Tracking von Exitlinks zu unterstützen.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# linkInternalFilters

AppMeasurement bietet die Möglichkeit, Links, die auf eine Stelle außerhalb Ihrer Website verweisen, automatisch zu verfolgen. If [`trackExternalLinks`](trackexternallinks.md) is enabled, an image request is sent to Adobe right as a visitor clicks a link to leave your site. Die Variablen [`linkExternalFilters`](linkexternalfilters.md) und `linkInternalFilters` bestimmen, welche Links als intern/extern betrachtet werden.

Wenn diese Variable einen Wert enthält, verhält sich das automatische Tracking von Exitlinks wie eine Blacklist-Variante. Wenn ein Link-Klick keinem `linkInternalFilters`-Wert entspricht, wird er als Exitlink betrachtet. Die gesamte URL wird mit dieser Variablen verglichen. If [`linkLeaveQueryString`](linkleavequerystring.md) is enabled, the query string is also examined.

Wenn Sie sowohl `linkInternalFilters` als auch `linkExternalFilters` gleichzeitig verwenden, muss der geklickte Link mit `linkExternalFilters`**übereinstimmen und** darf nicht mit `linkInternalFilters` überstimmen, um als Exitlink betrachtet zu werden. Wenn ein geklickter Link sowohl den Kriterien für Exitlinks als auch für Downloadlinks entspricht, hat der Downloadlink-Typ Priorität.

>[!NOTE] `linkInternalFilters`[](/help/admin/admin/internal-url-filter-admin.md) und interne URL-Filter sind separate Funktionen, die unterschiedliche Zwecke erfüllen. Die `linkInternalFilters`-Variable funktioniert speziell für das Tracking von Exitlinks. Interne URL-Filter sind eine Admin-Einstellung, die bei Traffic-Quellendimensionen (wie z. B. verweisende Domäne) hilfreich ist.

## Ausgehende Links – „Niemals verfolgen“ in Adobe Experience Platform Launch

The Never Track field is a comma-separated list of filters (usually domains) under the [!UICONTROL Link Tracking] accordion when configuring the Adobe Analytics extension.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Extensions] tab, then click the [!UICONTROL Configure] button under Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Link Tracking] Akkordeon, das das [!UICONTROL Outbound Links - Never Track] Feld aufdeckt.

Platzieren Sie Filter, die Sie nie als Exitlinks verfolgen möchten, in diesem Feld. Trennen Sie mehrere Domänen durch ein Komma ohne Leerzeichen.

## s.linkInternalFilters in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.linkInternalFilters`-Variable ist eine Zeichenfolge mit Filtern (z. B. Domänen), die Sie als intern für Ihre Website betrachten. Trennen Sie mehrere Filter durch ein Komma ohne Leerzeichen.

```js
s.linkInternalFilters = "example.com,example.net,example.org";
```

Betrachten Sie das folgende Implementierungsbeispiel, als ob es auf `adobe.com` wäre:

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.com">Example link 2</a>
```
