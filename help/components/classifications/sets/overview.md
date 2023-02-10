---
title: Klassifizierungssätze – Übersicht
description: Verwenden Sie Klassifizierungssätze zum Verwalten von Klassifizierungsdaten.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
source-git-commit: 2ba6ffc7f632975ca16fa02ee79d467d4d53f076
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 45%

---

# Klassifizierungssätze – Übersicht

Klassifizierungssätze bieten eine einzige Oberfläche zum Verwalten von Klassifizierungen und Regeln. Dieser Workflow kombiniert das Konzept der Erstellung von Klassifizierungen in den Report Suite-Einstellungen mit dem Konzept des Classification Importer, um eine intuitivere Benutzeroberfläche zum Erstellen und Verwalten von Klassifizierungsdaten zu bieten.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]**

>[!NOTE]
>
>Klassifizierungssätze stehen allen Kunden zur Verfügung, deren Report Suites in die neue Klassifizierungsarchitektur migriert wurden. Weitere Informationen erhalten Sie bei der Kundenunterstützung von Adobe oder Ihrem Account Manager.

Die Backend-Architektur, die mit Classification Sets veröffentlicht wurde, enthält einige wichtige Verbesserungen:

* Deutlich verkürzte Verarbeitungszeit (72 Stunden → 24 Stunden)
* Möglichkeit zur Verwendung der Benutzeroberfläche für Klassifizierungssets
* Die Option, Classification-Daten in Adobe Experience Platform künftig über die [Adobe Analytics-Quell-Connector für Classification-Daten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html)

Die Backend-Architektur, die mit Classification Sets veröffentlicht wurde, enthält auch einige wichtige Änderungen:

* Bei Verwendung des Browsers oder FTP-Imports wird[!UICONTROL Bei Konflikt überschreiben]&quot; ist immer aktiviert.
* Bei Verwendung des Browsers oder FTP-Imports wird die Option zum sofortigen Export nach dem Import nicht mehr unterstützt. Exporte müssen separat initiiert werden.
* Die Analytics 2.0-API `GetDimensions` -Endpunkt gibt jetzt Zeichenfolgenkennungen für Classifications anstelle numerischer Kennungen zurück. Numerische IDs können weiterhin verwendet werden. Adobe empfiehlt jedoch, nach Möglichkeit die neuen Zeichenfolgen-IDs zu verwenden. Numerische IDs können mithilfe der `?expansion=hidden` Abfragezeichenfolgen-Parameter.


Klassifizierungssätze bestehen aus zwei Hauptbereichen:

* [**[!UICONTROL Classification Sets Manager]**](set-manager.md): Erstellen, bearbeiten und löschen von Klassifizierungssätze.
* [**[!UICONTROL Auftrags-Manager für Klassifizierungssätze]**](job-manager.md): Zeigt den Status der Klassifizierungssatz-Aufträge an und ermöglicht, die Exportdateien herunterzuladen.
