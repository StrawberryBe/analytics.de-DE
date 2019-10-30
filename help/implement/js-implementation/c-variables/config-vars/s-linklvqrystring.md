---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# s.linkLeaveQueryString

Standardmäßig sind Abfragezeichenfolgen in allen Berichten ausgeschlossen.

Bei einigen Exitlinks und Downloadlinks befindet sich der wichtige Teil der URL möglicherweise in der Abfragezeichenfolge (wie in der folgenden Beispiel-URL):

```js
https://www.mycompany.com/download.asp?filename=myfile.exe
```

Der Name der Download-Datei kann in der Abfragezeichenfolge festgelegt sein, sodass die Abfragezeichenfolge erforderlich ist, damit der Bericht [!UICONTROL Dateidownloads] genauer ist.

Die Variable *`linkLeaveQueryString`* bestimmt, ob die Abfragezeichenfolge in den Berichten [!UICONTROL Exitlinks] und [!UICONTROL Datei-Download] enthalten sein soll.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| Keine | Keine | Datei-Downloads für Exitlinks | false |

> [!NOTE] Wenn `linkLeaveQueryString=true` eingestellt wird, werden alle Abfragezeichenfolgen-Parameter für alle Exitlinks und Downloadlinks mit aufgenommen.

## Syntax

```js
s.linkLeaveQueryString=[false/true]
```

## Beispiele

```js
s.linkLeaveQueryString=false
```

## Mögliche Werte

```js
s.linkLeaveQueryString=false
```

```js
s.linkLeaveQueryString=true
```

## Konfigurationseinstellungen

Bei dieser Variablen sind keine Konfigurationen erforderlich.

## Probleme, Fragen und Tipps

* Wenn `s.linkLeaveQueryString=true` eingestellt wird, werden alle Abfragezeichenfolgen-Parameter für alle Exitlinks und Downloadlinks mit aufgenommen.
* Die `linkLeaveQueryString`-Variable hat keine Auswirkungen auf aufgezeichnete Seiten-URLs, Besucherklickzuordnungen oder [!UICONTROL Pfadberichte].
