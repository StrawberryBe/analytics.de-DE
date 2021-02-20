---
description: Data Feeds sind Exporte von durch Adobe empfangene Clickstream-Daten. Verfügbar sind sowohl standardmäßige als auch benutzerdefinierte Daten-Feeds.
keywords: ftp;sftp
title: Daten-Feeds
uuid: 3c70eea3-ca59-4aa5-9b11-64e1bb677bfa
translation-type: tm+mt
source-git-commit: fc14751c810019c5257a23a8a598b16f42ed10ee
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 99%

---


# Daten-Feeds

Data Feeds sind Exporte von durch Adobe empfangene Clickstream-Daten. Verfügbar sind sowohl standardmäßige als auch benutzerdefinierte [Daten-Feeds](/help/export/analytics-data-feed/data-feed-overview.md).

Wenn Sie Adobe Data Warehouse und [!UICONTROL Standard Data Feeds] erworben haben, können Sie eigene Analytics-Daten-Feeds einrichten. Diese können an ein beliebiges FTP-Konto gesendet werden (entweder ein durch Adobe eingerichtetes oder ein externes FTP-Konto). Adobe Engineering Services bieten benutzerdefinierte [!UICONTROL Data Feeds], die auf nahezu jede Art gesendet werden können.

[!UICONTROL Daten-Feed]-FTP-Konten sind auf 10 GB beschränkt (standardmäßig). Für alle anderen Standard-FTP-Konten gilt eine Obergrenze von 50 MB. In Fällen, in denen Kunden das FTP-Konto bestimmungsgemäß verwenden, kann es bei Benutzern mit hohem Traffic-Aufkommen schnell passieren, dass die Konten voll sind. Wenn ein FTP-Konto voll ist, können keine weiteren Dateien in das Konto übertragen werden. An dieses FTP-Konto gelieferte Dateien ([!UICONTROL Daten-Feeds]-, Data Warehouse-Anforderungen usw.) werden daher nicht ausgeliefert. Dies ist einer Gründe, aus denen es wichtig ist, dass Sie Ihr Adobe FTP-Konto verwalten und empfangene Dateien nach dem Herunterladen entfernen.

Wenn ein FTP-Konto voll ist, müssen Sie die vorhandenen Dateien herunterladen und entfernen und Adobe mitteilen, dass der Speicher wieder frei ist. Adobe kann dann nicht ausgelieferte Dateien erneut senden. Einige Werkzeuge, z. B. Data Warehouse, erlauben dem Benutzer das erneute Senden der betroffenen Dateien. Hier ist für das erneute Senden kein Eingreifen von Adobe erforderlich. Falls Ihr FTP-Konto häufig voll ist, wenden Sie sich an die Adobe-Kundenunterstützung, um sich über Zustellungsalternativen zu informieren, wozu die Vergrößerung des FTP-Speichers und die Erhöhung der Dateigrenze für das Konto gehören.
