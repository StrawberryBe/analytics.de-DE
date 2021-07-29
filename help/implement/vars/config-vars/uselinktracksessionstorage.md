---
title: useLinkTrackSessionStorage
description: Speichern von Linktracking-Daten im Sitzungsspeicher statt in einem Cookie.
exl-id: 3295195d-bfd6-4af9-9487-dc1ea6c3da23
source-git-commit: 1a49c2a6d90fc670bd0646d6d40738a87b74b8eb
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 87%

---

# useLinkTrackSessionStorage

Wenn Ihr Unternehmen Linktracking verwendet, nutzt AppMeasurement das Cookie `s_sq`, um Informationen zwischen Treffern weiterzugeben. Manche Website-Konfigurationen stehen in Konflikt mit diesem Cookie. Wenn Sie zum Linktracking die Browser-Sitzungsspeicherung und Activity Map-Daten anstelle eines Cookies verwenden möchten, aktivieren Sie diese Variable.

Die Verwendung der Sitzungsspeicherung eines Browsers für Linktracking unterliegt einigen Einschränkungen:

* Die Sitzungsspeicherung funktioniert nicht zwischen unterschiedlichen Protokollen. Dies ist der Fall, wenn beispielsweise eine Seite über HTTP und die nächste über HTTPS bereitgestellt wird. AppMeasurement kann aufgrund von unterschiedlichen Protokollen nicht auf Linktracking-Daten in der Sitzungsspeicherung zugreifen.
* Die Sitzungsspeicherung funktioniert nicht Subdomain-übergreifend. Beispielsweise könnte ein Besucher zu `store.example.com` und dann zu `toys.example.com` navigieren. AppMeasurement kann aufgrund verschiedener Subdomains nicht auf Linktracking-Daten in der Sitzungsspeicherung zugreifen.

>[!TIP]
>
>Die zuverlässigste Implementierung ist die, die mithilfe der Sitzungsspeicherung zum Linktracking alle Inhalte über HTTPS in einer einzigen Subdomain bereitstellt.

AppMeasurement entfernt die Sitzungsspeicherungs-Linktracking-Daten, nachdem ein Treffer an Adobe gesendet wurde. Die Speicherung wird auch automatisch eingestellt, wenn die Browser-Registerkarte geschlossen wird.

## Verwenden der Linktracking-Sitzungsspeicherung mithilfe von Tags in Adobe Experience Platform

In der Datenerfassungs-Benutzeroberfläche gibt es kein dediziertes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.useLinkTrackSessionStorage in AppMeasurement und im benutzerdefinierten Code-Editor

Die Variable `s.useLinkTrackSessionStorage` ist ein boolescher Wert, der bestimmt, ob AppMeasurement die Sitzungsspeicherung anstelle des `s_sq`-Cookies für die Linktracking-Daten verwendet. Der Standardwert lautet `false`. Legen Sie diese Variable auf `true` fest, wenn Sie möchten, dass AppMeasurement die Sitzungsspeicherung anstelle des `s_sq`-Cookies für Linktracking und Activity Map verwendet.

```js
s.useLinkTrackSessionStorage = true;
```
