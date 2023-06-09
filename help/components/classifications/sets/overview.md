---
title: Übersicht über Klassifizierungssätze
description: Verwenden Sie Classification-Sets, um Classification-Daten zu verwalten.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
source-git-commit: 05243d37d252274d88650566de049327ff2bd439
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 26%

---

# Übersicht über Klassifizierungssätze

Klassifizierungssätze bieten eine einzige Oberfläche zur Verwaltung von Klassifizierungen und Regeln. Dieser Workflow kombiniert das Konzept der Erstellung von Classifications in den Report Suite-Einstellungen mit dem Konzept des Classification Importer, um eine intuitivere Oberfläche zum Erstellen und Verwalten von Classification-Daten zu bieten.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]**

Die mit Classification-Sets veröffentlichte Backend-Architektur enthält einige wichtige Verbesserungen:

* Geringere Verarbeitungszeit (72 Stunden → 24 Stunden)
* Die Verwendung der Benutzeroberfläche für Klassifizierungssätze
* Die Option, Klassifizierungsdaten in Adobe Experience Platform künftig über den [Adobe Analytics-Quell-Connector für Klassifizierungsdaten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html?lang=de) zu verwenden

Die Backend-Architektur, die mit Classification-Sets veröffentlicht wurde, enthält auch einige wichtige Änderungen:

* Bei Verwendung des Browsers oder des automatisierten Imports[!UICONTROL Bei Konflikt überschreiben]&quot; ist immer aktiviert.
* Bei Verwendung des Browsers oder des automatisierten Imports wird die Option zum sofortigen Export nach dem Import nicht mehr unterstützt. Exporte müssen separat initiiert werden.
* Die Analytics 2.0-API `GetDimensions`-Endpunkt gibt jetzt Zeichenfolgenkennungen für Klassifizierungen anstelle numerischer Kennungen zurück. Numerische Kennungen können zwar weiterhin verwendet werden, Adobe empfiehlt jedoch, nach Möglichkeit die neuen Zeichenfolgenkennungen zu verwenden. Numerische Kennungen können mithilfe der `?expansion=hidden` Abfragezeichenfolgen-Parameter abgerufen werden.

>[!IMPORTANT]
>
>Die Leistung von Classification-Sets hängt hauptsächlich von der Anzahl der eindeutigen Schlüsselwerte ab, die Daten enthalten. Adobe empfiehlt, bei Variablen mit einer großen Anzahl individueller Werte Vorsicht walten zu lassen. Diese Vorsicht gilt insbesondere bei der Kombination von Variablen aus mehreren Report Suites und Dimensionen zu einem einzigen Classification-Satz.

Klassifizierungssätze bestehen aus drei Hauptbereichen:

* [**[!UICONTROL Classification Sets Manager]**](manage/set-manager.md): Erstellen, bearbeiten und löschen Sie Classification-Sets.
* [**[!UICONTROL Auftrags-Manager für Klassifizierungssätze]**](job-manager.md): Zeigen Sie den Status der Classification-Set-Aufträge an und laden Sie die Exportdateien herunter.
* [**[!UICONTROL Klassifizierungssatz-Konsolidierung]**](consolidations/manage.md): Kombinieren Sie mehrere Classification-Sets zu einem einzigen Classification-Satz.
