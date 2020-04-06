---
title: useLinkTrackSessionStorage
description: Speichern Sie Linkverfolgungsdaten in der Datenspeicherung der Sitzung statt in einem Cookie.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# useLinkTrackSessionStorage

Wenn Ihr Unternehmen die Linktracking verwendet, verwendet AppMeasurement das Cookie, um Informationen zwischen Treffern weiterzugeben `s_sq` . Einige Website-Konfigurationen stehen in Konflikt mit diesem Cookie. Wenn Sie die Datenspeicherung der Browsersitzung für die Linktracking- und Aktivität Map-Daten anstelle eines Cookies verwenden möchten, aktivieren Sie diese Variable.

Die Verwendung der Sitzungs-Datenspeicherung eines Browsers für die Linkverfolgung unterliegt einigen Einschränkungen:

* Die Datenspeicherung der Sitzung funktioniert nicht zwischen Protokollen. Beispielsweise wird eine Seite über HTTP und die nächste über HTTPS bereitgestellt. AppMeasurement kann aufgrund von Protokollunterschieden nicht auf Link-Verfolgungsdaten in der Datenspeicherung der Sitzung zugreifen.
* Die Datenspeicherung der Sitzung funktioniert nicht über Subdomänen hinweg. Beispielsweise navigiert ein Besucher zu `store.example.com`und navigiert dann zu `toys.example.com`. AppMeasurement kann aufgrund verschiedener Subdomänen nicht auf Linkverfolgungsdaten in der Datenspeicherung der Sitzung zugreifen.

>[!TIP] Die zuverlässigste Implementierung mithilfe der Sitzungs-Datenspeicherung zur Linkverfolgung stellt alle Inhalte über HTTPS in einer einzigen Subdomäne bereit.

AppMeasurement entfernt die Link-Verfolgungsdaten zur Datenspeicherung von Sitzungen, nachdem ein Treffer an Adobe gesendet wurde. Es läuft auch automatisch ab, wenn die Browser-Registerkarte geschlossen wird.

## Verwenden der Datenspeicherung der Linktracking-Sitzung in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerspezifischen Code-Editor entsprechend der AppMeasurement-Syntax.

## s.useLinkTrackSessionStorage in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.useLinkTrackSessionStorage` Variable ist ein boolescher Wert, der bestimmt, ob AppMeasurement Sitzungsdaten anstelle des `s_sq` Cookies zur Linktracking-Datenspeicherung verwendet. Der Standardwert lautet `false`. Legen Sie diese Variable so fest, `true` dass AppMeasurement bei der Linktracking- und Aktivität-Map die Sitzungs-Datenspeicherung anstelle des `s_sq` Cookies verwendet.

```js
s.useLinkTrackSessionStorage = true;
```
