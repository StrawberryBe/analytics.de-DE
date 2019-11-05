---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 8c4c368a84ba5499d85f0b7512c99de47ddb14c2

---


# s.trackDownLoadLinks

Legen Sie „“ auf „true“ fest, wenn Sie Links für herunterladbare Dateien auf Ihrer Site verfolgen möchten.

Wenn „True“ für *`trackDownloadLinks`* angegeben ist, wird *`linkDownloadFileTypes`* verwendet, um zu bestimmen, welche Links herunterladbare Dateien sind.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | True |

Die Variable *`trackDownloadLinks`* ist nur dann auf „false“ zu setzen, wenn die Site keine herunterladbaren Dateien enthält oder wenn Sie nicht daran interessiert sind, dass die Anzahl der Klicks auf herunterladbare Dateien verfolgt wird. Wenn *`trackDownloadLinks`* auf „True“ gesetzt ist und ein Link für einen Datei-Download angeklickt wird, werden die Daten unverzüglich an [!DNL Analytics] übermittelt. Zu den gesendeten Daten gehören die Download-URL des Links sowie Daten zur Besucherklickzuordnung für diesen Link. Wenn *`trackDownloadLinks`* auf „False“ gesetzt ist, sind die Daten zur Besucherklickzuordnung für Exitlinks, die zu herunterladbaren Dateien gehören, wahrscheinlich in Berichten enthalten.

## Syntax und mögliche Werte

Die Variable *`trackDownloadLinks`* kann entweder „true“ oder „false“ sein.

## Beispiele

```
js
s.trackDownloadLinks=true 
```

```
js
s.trackDownloadLinks=false
```

## Konfigurationseinstellungen

Keine

## Probleme, Fragen und Tipps

* den *`trackDownloadLinks`* Wert „false“ hat, sind Links, die zu herunterladbaren Dateien auf Ihrer Site gehören, wahrscheinlich in Berichten zur Besucherklickzuordnung enthalten.

* Wenn *`trackDownloadLinks`* „true“ ist, werden, sobald ein Besucher auf einen Link für einen Datei-Download klickt, Daten gesendet.
