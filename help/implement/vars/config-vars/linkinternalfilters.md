---
title: linkInternalFilters
description: Verwenden Sie die Variable "linkInternalFilters", um die automatische Verfolgung von Ausstiegslinks zu unterstützen.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# linkInternalFilters

AppMeasurement Angebot ermöglicht die automatische Verfolgung von Links, die auf eine Stelle außerhalb Ihrer Site verweisen. Wenn [`trackExternalLinks`](trackexternallinks.md) diese Option aktiviert ist, wird eine Bildanforderung an Adobe gesendet, wenn ein Besucher auf einen Link klickt, um Ihre Site zu verlassen. Die [`linkExternalFilters`](linkexternalfilters.md) und `linkInternalFilters` Variablen bestimmen, welche Links als intern/extern gelten.

Wenn diese Variable einen Wert enthält, verhält sich die automatische Ausstiegslink-Verfolgung wie eine Blacklist. Wenn ein Link-Klick keinen `linkInternalFilters` Werten entspricht, wird er als Ausstiegslink betrachtet. Die gesamte URL wird mit dieser Variablen verglichen. Wenn [`linkLeaveQueryString`](linkleavequerystring.md) diese Option aktiviert ist, wird auch die Abfrage-Zeichenfolge geprüft.

Wenn Sie sowohl `linkInternalFilters` als auch `linkExternalFilters` gleichzeitig verwenden, muss der angeklickte Link übereinstimmen `linkExternalFilters` und **nicht übereinstimmen, um als Exitlink betrachtet** `linkInternalFilters` zu werden. Wenn ein angeklickter Link sowohl den Kriterien für Ausstiegslinks als auch für Downloadlinks entspricht, hat der Linktyp Priorität.

> [!NOTE] Die Filter `linkInternalFilters` für [interne URLs](/help/admin/admin/internal-url-filter-admin.md) sind separate Funktionen, die unterschiedliche Zwecke erfüllen. Die `linkInternalFilters` Variable funktioniert speziell für die Verfolgung von Ausstiegslinks. Interne URL-Filter sind eine Admin-Einstellung, die bei Datenverkehrsquellen-Dimensionen wie der verweisenden Domäne hilfreich ist.

## Ausgehende Links - In Adobe Experience Platform Launch nie verfolgen

Das Feld &quot;Nie verfolgen&quot;ist eine kommagetrennte Liste von Filtern (in der Regel Domänen) unter dem [!UICONTROL Link Tracking] Akkordeon, wenn die Adobe Analytics-Erweiterung konfiguriert wird.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Extensions] Registerkarte und klicken Sie dann auf die [!UICONTROL Configure] Schaltfläche unter Adobe Analytics.
4. Erweitern Sie das [!UICONTROL Link Tracking] Akkordeon, das das [!UICONTROL Outbound Links - Never Track] Feld aufdeckt.

Platzieren Sie Filter, die Sie nie als Ausstiegslinks nachverfolgen möchten, in diesem Feld. Trennen Sie mehrere Domänen durch ein Komma ohne Leerzeichen.

## s.linkInternalFilters in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.linkInternalFilters` Variable ist eine Zeichenfolge mit Filtern (z. B. Domänen), die Sie für Ihre Site als intern betrachten. Trennen Sie mehrere Filter mithilfe eines Kommas ohne Leerzeichen.

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
