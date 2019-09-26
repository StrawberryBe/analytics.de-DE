---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: b38ba4222951d957c607cd764224028527835c7e

---


# s.dynamicAccountMatch

Die Variable „“ ruft mithilfe des DOM-Objekts den Abschnitt der URL ab, auf den alle in „“ aufgeführten Regeln angewendet werden.

This variable is only valid when *`dynamicAccountSelection`* is set to 'True.' Da der Standardwert [!DNL window.location.host] lautet, ist diese Variable nicht erforderlich, damit die [!UICONTROL dynamische Kontoauswahl] ordnungsgemäß funktioniert. For additional information, see [dynamicAccountList](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).

Die Regeln in `dynamicAccountList` werden auf den Wert von angewendet `dynamicAccountMatch`. Wenn `dynamicAccountMatch` nur [!DNL window.location.host] (Standard) enthalten ist, `dynamicAccountList` gelten die Regeln nur für die Domäne der Seite.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | window.location.host |

## Syntax und mögliche Werte

Die Variable `dynamicAccountMatch`wird für gewöhnlich von dem Adobe-Berater ausgefüllt, der die AppMeasurement für JavaScript-Datei zur Verfügung stellt. Jedoch können die nachfolgend aufgeführten Werte jederzeit übernommen werden.

```js
s.dynamicAccountMatch=[DOM object]
```

| Beschreibung | Wert |
|---|---|
| Domäne (Standard) | window.location.host |
| Pfad | window.location.pathname |
| Abfragezeichenfolge | (window.location.search?window.location.search:"?") |
| Domäne und Pfad | window.location.host+window.location.pathname |
| Pfad und Abfragezeichenfolge | window.location.pathname+(window.location.search?window.location.search:"?") |
| Vollständige URL | window.location.href |

## Beispiele

```js
s.dynamicAccountMatch=window.location.pathname
```

```js
s.dynamicAccountMatch=window.location.host+window.location.pathname
```

## Konfigurationseinstellungen

–

## Probleme, Fragen und Tipps

* Die dynamische Kontoauswahl wird nicht von [AppMeasurement für JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).

* Bei auf einer Festplatte gespeicherten Seiten ist [!DNL window.location.host] leer, wodurch deren Seitenansichten an die standardmäßige Report Suite (in `s_account`).

* Bei über ein webbasiertes Tool übersetzten Seiten (wie z. B. Google) funktioniert die [!UICONTROL Dynamische Kontoauswahl] nicht richtig. Für eine präzisere Nachverfolgung müssen Sie die Variable [!UICONTROL s_account] serverseitig auffüllen.
