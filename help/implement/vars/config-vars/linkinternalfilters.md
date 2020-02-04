---
title: linkInternalFilters
description: Verwenden Sie die Variable "linkInternalFilters", um die automatische Verfolgung von Ausstiegslinks zu unterstützen.
translation-type: tm+mt
source-git-commit: 8f7baa770f800ffe800e760f1eca59911d3db348

---


# linkInternalFilters

AppMeasurement bietet die Möglichkeit, Links, die auf eine Stelle außerhalb Ihrer Site verweisen, automatisch zu verfolgen. Falls `trackExternalLinks` dies `true`der Fall ist, wird eine Bildanforderung direkt an Adobe gesendet, wenn ein Besucher auf einen Link klickt, um Ihre Site zu verlassen. Die `linkTrackExternalFilters` und `linkTrackInternalFilters` Variablen bestimmen, welche Links als intern/extern gelten.

Wenn diese Variable einen Wert enthält, verhält sich die automatische Ausstiegslink-Verfolgung wie eine Blacklist. Wenn ein Link-Klick keinen `linkInternalFilters` Werten entspricht, wird er als Ausstiegslink betrachtet. Die gesamte URL wird mit dieser Variablen verglichen. Ist `linkLeaveQueryString` dies `true`der Fall, wird auch die Abfragezeichenfolge geprüft.

Wenn Sie sowohl `linkInternalFilters` als auch `linkExternalFilters` gleichzeitig verwenden, muss der angeklickte Link übereinstimmen `linkExternalFilters` und **nicht übereinstimmen, um als Exitlink betrachtet** `linkInternalFilters`zu werden. Wenn ein angeklickter Link sowohl den Kriterien für Ausstiegslinks als auch für Downloadlinks entspricht, hat der Linktyp Priorität.

> [!NOTE] Filter für interne `linkInternalFilters` URLs sind separate Funktionen, die unterschiedliche Zwecke erfüllen. Die `linkInternalFilters` Variable funktioniert speziell für die Verfolgung von Ausstiegslinks. Interne URL-Filter sind eine Admin-Einstellung, die bei Datenverkehrsquellen-Dimensionen wie der verweisenden Domäne hilfreich ist. See [Internal URL filters](/help/admin/admin/internal-url-filter-admin.md) in the Admin user guide.

## Ausgehende Links - In Adobe Experience Platform Launch nie verfolgen

Das Feld &quot;Nie verfolgen&quot;ist eine kommagetrennte Liste von Filtern (üblicherweise Domänen) unter dem Akkordeon &quot; [!UICONTROL Linktracking] &quot;beim Konfigurieren der Adobe Analytics-Erweiterung.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter Adobe Analytics auf die Schaltfläche [!UICONTROL Konfigurieren] .
4. Erweitern Sie das Akkordeon &quot; [!UICONTROL Linktracking] &quot;, in dem das Feld &quot; [!UICONTROL Ausgehende Links - Nie verfolgen] &quot;angezeigt wird.

Platzieren Sie Filter, die Sie nie als Ausstiegslinks nachverfolgen möchten, in diesem Feld. Trennen Sie mehrere Domänen durch ein Komma ohne Leerzeichen.

## s.linkInternalFilters in AppMeasurement und Starten des benutzerdefinierten Codeeditors

Die `s.linkInternalFilters` Variable ist eine Zeichenfolge mit Filtern (z. B. Domänen), die Sie für Ihre Site als intern betrachten. Trennen Sie mehrere Filter mit einem Komma ohne Leerzeichen.

```js
s.linkInternalFilters = "example.com,example.net,example.org";
```

Betrachten Sie das folgende Implementierungsbeispiel, als wäre es auf `adobe.com`:

```html
<script>
  s.trackExternalLinks = true;
  s.linkInternalFilters = "adobe.com";
</script>

<!-- The following link is an exit link because it does not match the anything under linkInternalFilters -->
<a href = "example.com">Example link 2</a>
```
