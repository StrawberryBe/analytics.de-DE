---
title: Last Touch-Kanal
description: Der neueste Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Last Touch-Kanal

Die Dimension &quot;Last Touch-Kanal&quot;zeigt den letzten Marketing-Kanal an, mit dem ein Besucher während der Interaktionszeit des Besuchers (standardmäßig 30 Tage) übereinstimmt. Diese Dimension ist nützlich, um zu verstehen, welche Marketing-Kanal Traffic zu Ihrer Site bringen, der zu Umrechnungen führt, sodass Sie die Marketingbemühungen auf Bereiche konzentrieren können, die am effektivsten sind.

## Diese Dimension mit Daten füllen

Diese Dimension verweist direkt auf die Kanal-Namen, die Sie im [Marketing Kanal-Manager](/help/admin/admin/marketing-channels-admin.md)definiert haben.

Jeder Hit, der an Adobe-Datenerfassungsserver gesendet wird, wird über die Verarbeitungsregeln für den Marketing Kanal Ihrer Report Suite ausgeführt. Es durchläuft jede Regel in numerischer Reihenfolge, bis eine Übereinstimmung gefunden wird, bei der der Marketing-Kanal mit dem Treffer verknüpft ist. Der Last Touch-Kanal bleibt beim Besucher bestehen, bis er die Site nicht länger als den Besucher-Interaktionszeitraum (standardmäßig 30 Tage) besucht.

Wenn Sie diese Dimension auf einen bestimmten Wert setzen möchten, sind die folgenden Schritte erforderlich:

* Legen Sie das gewünschte Dimensionselement als Kanal im Marketing Kanal-Manager unter Report Suite-Einstellungen fest.
* Legen Sie eine Verarbeitungsregel für den Marketing Kanal fest, die die gewünschten Kriterien für den Treffer enthält.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Verarbeitungsregel Marketing Kanal beschrieben sind.

## Dimensionselemente

Dimensionselemente enthalten einen beliebigen Kanal im Marketing Kanal-Manager. Standardmäßig umfassen die Werte `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"`und `"Referring domains"`. Sie können Kanal im Marketing Kanal-Manager hinzufügen oder löschen, die sich auf die Werte dieser Dimension auswirken.
