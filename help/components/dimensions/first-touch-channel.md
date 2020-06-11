---
title: First Touch-Kanal
description: Der erste Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
translation-type: tm+mt
source-git-commit: 2c262e5345c39a71a6a54062c607273528294b24
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---


# First Touch-Kanal

Die Dimension &quot;First Touch-Kanal&quot;berichtet über den ersten Marketing-Kanal, mit dem ein Besucher während der Interaktionszeit dieses Besuchers (standardmäßig 30 Tage) übereinstimmt. Diese Dimension ist nützlich, um zu verstehen, welche Marketing-Kanal den anfänglichen Traffic zu Ihrer Site leiten, sodass Sie die Marketingbemühungen auf Bereiche konzentrieren können, die am effektivsten sind.

## Diese Dimension mit Daten füllen

Diese Dimension verweist direkt auf die Kanal-Namen, die Sie im [Marketing Kanal-Manager](/help/admin/admin/marketing-channels-admin.md)definiert haben.

Jeder Hit, der an Adobe-Datenerfassungsserver gesendet wird, wird über die Verarbeitungsregeln für den Marketing Kanal Ihrer Report Suite ausgeführt. Es durchläuft jede Regel in numerischer Reihenfolge, bis eine Übereinstimmung gefunden wird, bei der der Marketing-Kanal mit dem Treffer verknüpft ist. Der First Touch-Kanal bleibt beim Besucher bestehen, bis er die Site nicht länger als den Besucher-Interaktionszeitraum (standardmäßig 30 Tage) besucht.

Wenn Sie diese Dimension auf einen bestimmten Wert setzen möchten, sind die folgenden Schritte erforderlich:

* Legen Sie den gewünschten Dimensionswert als Kanal im Marketing Kanal-Manager unter Report Suite-Einstellungen fest.
* Legen Sie eine Verarbeitungsregel für den Marketing Kanal fest, die die gewünschten Kriterien für den Treffer enthält.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Verarbeitungsregel für den Marketing-Kanal beschrieben sind, _und_ muss der erste Marketingwert sein, der dies im Interaktionszeitraum des Besuchers tut.

Wenn ein nachfolgender Treffer Kriterien unter einem anderen Marketing-Kanal erfüllt, wird diese Dimension nicht mit dem neuen Marketing-Kanal überschrieben.

## Dimensionswerte

Dimensionswerte enthalten einen beliebigen Kanal im Marketing Kanal-Manager. Standardmäßig umfassen die Werte `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"`und `"Referring domains"`. Sie können Kanal im Marketing Kanal-Manager hinzufügen oder löschen, die sich auf die Werte dieser Dimension auswirken.
