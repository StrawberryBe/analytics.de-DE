---
title: hier
description: Implementieren Sie Hierarchievariablen in Adobe Analytics.
feature: Variables
exl-id: 72bdab8f-a001-4ada-b5e2-453a8e3f24a6
source-git-commit: a71db2fac9333b70a55da91fe9a94b0cc8434b42
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 93%

---

# hier

Hierarchievariablen sind benutzerdefinierte Variablen, mit denen Sie die Struktur einer Website sehen können.

>[!TIP]
>
>Diese Variable wurde in früheren Versionen von Adobe Analytics häufiger verwendet. Adobe empfiehlt stattdessen die Verwendung von [eVars](evar.md) und Klassifizierungen.

>[!IMPORTANT]
>
>Hierarchie wird bei der Datenerfassung mit XDM für Experience Edge nicht unterstützt.

Diese Variable ist nützlich bei Sites mit mehr als drei Ebenen in der Site-Struktur. Eine Medien-Site kann beispielsweise vier Ebenen zum Abschnitt „Sport“ haben: `Sports`, `Local Sports`, `Baseball` und `Team name`. Wenn ein Besucher die Fußballseite aufruft, wird dieser Besuch in den Ebenen „Sport“, „Lokaler Sport“ und „Fußball“ wiedergegeben.

Adobe unterstützt bis zu fünf Hierarchievariablen in Ihrer Implementierung. Legen Sie bei Aktivierung der Hierarchievariablen fest, welches Trennzeichen verwendet werden soll und über wie viele Ebenen die Hierarchie maximal verfügen soll. Wenn das Trennzeichen beispielsweise ein Komma ist, würde die Hierarchie wie folgt aussehen:

```js
s.hier1 = "Sports,Local Sports,Baseball";
```

Achten Sie darauf, dass keiner Ihrer Abschnittsnamen das Trennzeichen enthält. Wenn beispielsweise einer Ihrer Abschnitte `Coach Griffin, Jim` heißt, wählen Sie ein anderes Trennzeichen als ein Komma. Die maximale Variablenanzahl beträgt 255 Byte. Trennzeichen können aus mehreren Zeichen bestehen, z. B. `||` oder `/|\`, die in Variablenwerten mit geringerer Wahrscheinlichkeit auftreten.

## Beispiele

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub";
```

```js
s.hier4="Sports/Local Sports/Baseball";
```
