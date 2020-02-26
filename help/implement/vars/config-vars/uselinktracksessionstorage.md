---
title: useLinkTrackSessionStorage
description: Speichern Sie Linkverfolgungsdaten im Sitzungsspeicher anstelle eines Cookies.
translation-type: tm+mt
source-git-commit: e1a08ecd3d5eb41bce7ca91027249871c3b5b22f

---


# useLinkTrackSessionStorage

Wenn Ihr Unternehmen die Linktracking verwendet, verwendet AppMeasurement das Cookie, um Informationen zwischen Treffern weiterzugeben `s_sq` . Einige Website-Konfigurationen stehen in Konflikt mit diesem Cookie. Wenn Sie die Speicherung der Browsersitzung für die Linktracking- und Activity Map-Daten anstelle eines Cookies verwenden möchten, aktivieren Sie diese Variable.

Die Verwendung des Sitzungsspeichers eines Browsers zur Linktracking unterliegt einigen Einschränkungen:

* Sitzungsspeicher funktioniert nicht zwischen Protokollen. Beispielsweise wird eine Seite über HTTP und die nächste über HTTPS bereitgestellt. AppMeasurement kann aufgrund von Protokollunterschieden nicht auf Link-Verfolgungsdaten im Sitzungsspeicher zugreifen.
* Sitzungsspeicher funktioniert nicht über Subdomänen hinweg. Beispielsweise navigiert ein Besucher zu `store.example.com`und navigiert dann zu `toys.example.com`. AppMeasurement kann aufgrund verschiedener Subdomänen nicht auf Linktracking-Daten im Sitzungsspeicher zugreifen.

> [!TIP] Die zuverlässigste Implementierung unter Verwendung des Sitzungsspeichers für die Linktracking stellt alle Inhalte über HTTPS in einer einzigen Subdomäne bereit.
AppMeasurement entfernt Link-Verfolgungsdaten zur Sitzungsspeicherung, nachdem ein Treffer an Adobe gesendet wurde. Es läuft auch automatisch ab, wenn die Browser-Registerkarte geschlossen wird.

## Verwenden der Linktracking-Sitzungsspeicherung in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s.useLinkTrackSessionStorage in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.useLinkTrackSessionStorage` Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement Sitzungsspeicher für Linkverfolgungsdaten anstelle des `s_sq` Cookies verwendet. Its default value is `false`. Legen Sie diese Variable so fest, `true` dass AppMeasurement Sitzungsspeicher anstelle des `s_sq` Cookies für die Linktracking und Activity Map verwendet.

```js
s.useLinkTrackSessionStorage = true;
```
