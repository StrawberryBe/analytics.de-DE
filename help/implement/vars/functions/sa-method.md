---
title: sa
description: Ändern Sie die Report Suite jederzeit in Ihrer Implementierung.
translation-type: tm+mt
source-git-commit: f179292abae9cf7986d61da89a86e3e88111943e

---


# sa

Mit der `sa` Methode können Sie eine Report Suite jederzeit auf der Seite dynamisch ändern. Wenn Sie Daten ohne Seitenneuladung an andere Report Suites senden möchten, können Sie diese Methode verwenden.

## Verwenden der sa-Methode beim Starten der Adobe Experience Platform

Es gibt keine flexible Möglichkeit, Report Suite in der Oberfläche zu ändern. Sie können die Report Suite beim Konfigurieren der Adobe Analytics-Erweiterung im Akkordeon &quot; [!UICONTROL Bibliotheksverwaltung] &quot;festlegen. Sie können die Report Suite jedoch nicht mithilfe von Regeln ändern oder aktualisieren. Wenn Sie die Report Suite-Werte nach dem Festlegen aktualisieren möchten, verwenden Sie den benutzerdefinierten Code-Editor nach der AppMeasurement-Syntax.

## s.sa() in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Rufen Sie die `s.sa()` Methode auf, um die Ziel-Report Suite zu ändern. Das einzige Argument ist eine Zeichenfolge, die eine Report Suite-ID oder mehrere durch ein Komma getrennte Report Suite-IDs enthält. Das Argument der Report Suite-ID ist erforderlich. Verwenden Sie keine Leerzeichen im Zeichenfolgenargument.

```js
s.sa("examplersid");
```

## Beispiel

Sie können die Report Suite ändern, wenn der Benutzer eine bestimmte Aktion auf Ihrer Site ausführt.

```js
// Instantiate the tracking object
var s = s_gi("examplersid");

// If the visitor plays a video, you can add a video report suite
s.sa("examplersid,videorsid");

// Then send an image request
s.t();
```
