---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.linkLeaveQueryString

Standardmäßig sind Abfragezeichenfolgen in allen Berichten ausgeschlossen. 

Bei einigen Exitlinks und Downloadlinks befindet sich der wichtige Teil der URL möglicherweise in der Abfragezeichenfolge (wie in der folgenden Beispiel-URL):

```js
https://www.mycompany.com/download.asp?filename=myfile.exe
```

Der Name der Download-Datei kann in der Abfragezeichenfolge festgelegt sein, sodass die Abfragezeichenfolge erforderlich ist, damit der Bericht [!UICONTROL Dateidownloads] genauer ist.

Die Variable *`linkLeaveQueryString`* bestimmt, ob die Abfragezeichenfolge in den Berichten [!UICONTROL Exitlinks] und [!UICONTROL Dateidownload] enthalten sein soll.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|--- |--- |--- |--- |
| Keine | Keine | Exit Links File Downloads | false |

>[!NOTE]
>
>Setting `linkLeaveQueryString=true` includes all query string parameters for all exit links and download links.

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

* Setting `s.linkLeaveQueryString=true` includes all query string parameters for all exit links and download links.
* The `linkLeaveQueryString` variable does not affect recorded page URLs, visitor click map, or [!UICONTROL Path] reports.
