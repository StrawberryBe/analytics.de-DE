---
title: sa
description: Ändern Sie die Report Suite jederzeit in Ihrer Implementierung.
exl-id: 524857a7-c820-4985-86c7-fcf21a0809bd
translation-type: ht
source-git-commit: 4c726cc78e4d6c15db70ab04b0319b0602a51be6
workflow-type: ht
source-wordcount: '184'
ht-degree: 100%

---

# sa

Mit der `sa()`-Methode können Sie eine Report Suite jederzeit auf der Seite dynamisch ändern. Wenn Sie Daten ohne Seitenneuladung an andere Report Suites senden möchten, können Sie diese Methode verwenden.

## Verwenden der sa-Methode in Adobe Experience Platform Launch

Es gibt keine flexible Möglichkeit, die Report Suite in der Oberfläche zu ändern. Sie können die Report Suite bei der Konfiguration der Adobe Analytics-Erweiterung unter dem Akkordeon [!UICONTROL Bibliotheksverwaltung] festlegen. Sie können die Report Suite jedoch nicht mithilfe von Regeln ändern oder aktualisieren. Wenn Sie die Report Suite-Werte nach dem Festlegen aktualisieren möchten, verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.sa() in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Rufen Sie die `s.sa()`-Methode auf, um die Ziel-Report Suite zu ändern. Das einzige Argument ist eine Zeichenfolge, die eine Report Suite-ID oder mehrere durch ein Komma getrennte Report Suite-IDs enthält. Das Argument der Report Suite-ID ist erforderlich. Verwenden Sie keine Leerzeichen im Zeichenfolgenargument.

```js
s.sa("examplersid");
```

## Beispiel

Sie können die Report Suite ändern, wenn der Benutzer eine bestimmte Aktion auf Ihrer Website ausführt.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// If the visitor plays a video, you can add a video report suite
s.sa("examplersid,videorsid");

// Then send an image request
s.t();
```
