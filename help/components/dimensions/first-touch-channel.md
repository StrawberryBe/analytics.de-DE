---
title: Erstkontakt-Kanal
description: Der erste Marketing-Kanal innerhalb des Interaktionsablaufs des Besuchers.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 100%

---


# Erstkontakt-Kanal

Die Dimension „Erstkontakt-Kanal“ enthält den ersten Marketing-Kanal, mit dem ein Besucher während der Interaktionszeit des Besuchers (standardmäßig 30 Tage) übereinstimmt. Diese Dimension ist nützlich, um zu verstehen, welche Marketing-Kanäle den anfänglichen Traffic zu Ihrer Site leiten, sodass Sie Ihre Marketing-Bemühungen auf Bereiche konzentrieren können, die am effektivsten sind.

## Füllen dieser Dimension mit Daten

Diese Dimension verweist direkt auf die Kanalnamen, die Sie im [Marketing-Kanal-Manager](/help/admin/admin/marketing-channels-admin.md) definiert haben.

Jeder an die Datenerfassungs-Server von Adobe gesendete Treffer durchläuft die Verarbeitungsregeln für den Marketing-Kanal Ihrer Report Suite. Jede Regel wird in numerischer Reihenfolge durchlaufen, bis eine Übereinstimmung gefunden wird, in der dieser Marketing-Kanal mit dem Treffer verknüpft ist. Der Erstkontakt-Kanal bleibt so lange bestehen, bis der Besucher die Website länger als den Besucherinteraktionszeitraum (standardmäßig 30 Tage) nicht mehr besucht hat.

Führen Sie die folgenden Schritte aus, um diese Dimension auf einen bestimmten Wert zu setzen:

* Legen Sie das gewünschte Dimensionselement als Kanal im Marketing-Kanal-Manager unter den Report Suite-Einstellungen fest.
* Legen Sie eine Marketing-Kanalverarbeitungsregel fest, die die gewünschten Kriterien für den Treffer enthält.
* Der Treffer des Besuchers auf Ihrer Site muss den Kriterien entsprechen, die in der Marketing-Kanalverarbeitungsregel beschrieben sind, _und_ der erste Marketing-Kanalwert sein, auf den dies im Interaktionszeitraum des Besuchers zutrifft.

Wenn ein nachfolgender Treffer Kriterien unter einem anderen Marketing-Kanal erfüllt, wird diese Dimension nicht mit dem neuen Marketing-Kanal überschrieben.

## Dimensionselemente

Die Dimensionenselemente umfassen alle Kanalnamen im Marketing-Kanal-Manager. Standardmäßig umfassen die Werte `"Paid search"`, `"Natural search"`, `"Display"`, `"Email"`, `"Affiliate"`, `"Direct"`, `"Internal"`, `"Social networks"` und `"Referring domains"`. Sie können Kanäle im Marketing-Kanal-Manager hinzufügen oder löschen, die sich auf die Werte dieser Dimension auswirken.
