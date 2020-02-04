---
title: linkExternalFilters
description: Verwenden Sie die Variable "linkExternalFilters", um die automatische Verfolgung von Ausstiegslinks zu unterstützen.
translation-type: tm+mt
source-git-commit: 8f7baa770f800ffe800e760f1eca59911d3db348

---


# linkExternalFilters

AppMeasurement bietet die Möglichkeit, Links, die auf eine Stelle außerhalb Ihrer Site verweisen, automatisch zu verfolgen. Falls `trackExternalLinks` dies `true`der Fall ist, wird eine Bildanforderung direkt an Adobe gesendet, wenn ein Besucher auf einen Link klickt, um Ihre Site zu verlassen. Die `linkTrackExternalFilters` und `linkTrackInternalFilters` Variablen bestimmen, welche Links als intern/extern gelten.

Wenn diese Variable einen Wert enthält, verhält sich die automatische Ausstiegslink-Verfolgung auf eine weiße Listenform. Wenn ein Link-Klick keinen `linkExternalFilters` Werten entspricht, wird er nicht als Ausstiegslink betrachtet. Die gesamte URL wird mit dieser Variablen verglichen. Ist `linkLeaveQueryString` dies `true`der Fall, wird auch die Abfragezeichenfolge geprüft.

> [!TIP] Verwenden Sie diese Variable nur, wenn Sie genau wissen, welche Domänen Sie als Ausstiegslinks betrachten möchten. Viele Unternehmen stellen fest, dass die Verwendung `linkInternalFilters` `linkExternalFilters`für die Verfolgung von Ausstiegslinks ausreicht und nicht verwendet wird.

Wenn Sie sowohl `linkInternalFilters` als auch `linkExternalFilters` gleichzeitig verwenden, muss der angeklickte Link übereinstimmen `linkExternalFilters` und **nicht übereinstimmen, um als Exitlink betrachtet** `linkInternalFilters`zu werden. Wenn ein angeklickter Link sowohl den Kriterien für Ausstiegslinks als auch für Downloadlinks entspricht, hat der Linktyp Priorität.

## Ausgehende Links - In Adobe Experience Platform Launch verfolgen

Das Feld &quot;Verfolgen&quot;ist eine kommagetrennte Liste von Filtern (üblicherweise Domänen) unter dem Akkordeon &quot; [!UICONTROL Linktracking] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Linktracking] &quot;, in dem das Feld &quot; [!UICONTROL Ausgehende Links - Track] &quot;angezeigt wird.

Platzieren Sie Filter, die Sie in diesem Feld immer als extern betrachten möchten. Trennen Sie mehrere Domänen durch ein Komma ohne Leerzeichen.

## s.linkExternalFilters in AppMeasurement und benutzerdefinierten Codeeditor starten

Die `s.linkExternalFilters` Variable ist eine Zeichenfolge mit Filtern (z. B. Domänen), die Sie als Ausstiegslinks betrachten. Trennen Sie mehrere Domänen mit einem Komma ohne Leerzeichen.

```js
s.linkExternalFilters = "example.com,example.net,example.org";
```

Betrachten Sie das folgende Implementierungsbeispiel, als wäre es auf `adobe.com`:

```html
<script>
  s.trackExternalLinks = true;
  s.linkExternalFilters = "example.com,example.net";
</script>

<!-- The following link is not considered an exit link, even though the link is outside adobe.com -->
<a href = "example.org">Example link 1</a>

<!-- The following link is an exit link because it matches the linkExternalFilters whitelist -->
<a href = "example.com">Example link 2</a>
```
