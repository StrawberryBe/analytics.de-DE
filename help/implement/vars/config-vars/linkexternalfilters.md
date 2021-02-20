---
title: linkExternalFilters
description: Verwenden Sie die Variable „linkExternalFilters“, um das automatische Tracking von Exitlinks zu unterstützen.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 95%

---


# linkExternalFilters

AppMeasurement bietet die Möglichkeit, Links, die auf eine Stelle außerhalb Ihrer Website verweisen, automatisch zu verfolgen. Wenn [`trackExternalLinks`](trackexternallinks.md) aktiviert ist, wird eine Bildanfrage an Adobe geschickt, wenn ein Besucher auf einen Link klickt, um Ihre Website zu verlassen. Die Variablen `linkExternalFilters` und [`linkInternalFilters`](linkinternalfilters.md) bestimmen, welche Links als intern/extern betrachtet werden.

Wenn diese Variable einen Wert enthält, verhält sich die automatische Verfolgung von Ausstiegslinks wie eine Zulassungsliste. Wenn ein Link-Klick keinem `linkExternalFilters`-Wert entspricht, wird er nicht als Exitlink betrachtet. Die gesamte URL wird mit dieser Variablen verglichen. Wenn [`linkLeaveQueryString`](linkleavequerystring.md) aktiviert ist, wird auch die Abfragezeichenfolge geprüft.

>[!TIP]
>
>Verwenden Sie diese Variable nur, wenn Sie genau wissen, welche Domänen Sie als Exitlinks betrachten möchten. Viele Unternehmen stellen fest, dass die Verwendung von `linkInternalFilters` für das Tracking von Exitlinks ausreicht, und verwenden `linkExternalFilters` nicht.

Wenn Sie sowohl `linkInternalFilters` als auch `linkExternalFilters` gleichzeitig verwenden, muss der geklickte Link mit `linkExternalFilters`**übereinstimmen und** darf nicht mit `linkInternalFilters` überstimmen, um als Exitlink betrachtet zu werden. Wenn ein geklickter Link sowohl den Kriterien für Exitlinks als auch für Downloadlinks entspricht, hat der Downloadlink-Typ Priorität.

## Ausgehende Links – Verfolgen in Adobe Experience Platform Launch

Das Feld „Verfolgen“ ist eine kommagetrennte Liste von Filtern (üblicherweise Domänen) unter dem Akkordeon [!UICONTROL Linktracking] bei der Konfiguration der Adobe Analytics-Erweiterung.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
4. Erweitern Sie das Akkordeon [!UICONTROL Linktracking], wodurch das Feld [!UICONTROL Ausgehende Links – Verfolgen] angezeigt wird.

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

<!-- The following link is an exit link because it matches the linkExternalFilters allowlist -->
<a href = "example.com">Example link 2</a>
```
