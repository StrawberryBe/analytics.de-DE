---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
solution: null
title: Dynamische Variablen
translation-type: ht
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# s.dynamicAccountMatch

Die Variable „“ ruft mithilfe des DOM-Objekts den Abschnitt der URL ab, auf den alle in „“ aufgeführten Regeln angewendet werden.

Diese Variable ist nur gültig, wenn *`dynamicAccountSelection`* auf „True“ festgelegt ist. Da der Standardwert [!DNL window.location.host] lautet, ist diese Variable nicht erforderlich, damit die [!UICONTROL dynamische Kontoauswahl] ordnungsgemäß funktioniert. Weitere Informationen finden Sie unter [dynamicAccountList](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html).

Die Regeln in `dynamicAccountList` werden auf den Wert von `dynamicAccountMatch` angewendet. Wenn `dynamicAccountMatch` nur [!DNL window.location.host] (Standard) enthält, gelten die Regeln in `dynamicAccountList` nur für die Domäne der Seite.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | nicht angegeben | nicht angegeben | window.location.host |

## Syntax und mögliche Werte

Die Variable `dynamicAccountMatch` wird für gewöhnlich von dem Adobe-Berater ausgefüllt, der die AppMeasurement für JavaScript-Datei zur Verfügung stellt. Jedoch können die nachfolgend aufgeführten Werte jederzeit übernommen werden.

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

Keine

## Probleme, Fragen und Tipps

* Die dynamische Kontoauswahl wird von [AppMeasurement für JavaScript](https://docs.adobe.com/content/help/de-DE/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html) nicht unterstützt.

* Bei auf einer Festplatte gespeicherten Seiten ist [!DNL window.location.host] leer, wodurch deren Seitenansichten an die standardmäßige Report Suite (in `s_account`).

* Bei über ein webbasiertes Tool übersetzten Seiten (wie z. B. Google) funktioniert die [!UICONTROL Dynamische Kontoauswahl] nicht richtig. Für eine präzisere Nachverfolgung müssen Sie die Variable [!UICONTROL s_account] serverseitig auffüllen.
