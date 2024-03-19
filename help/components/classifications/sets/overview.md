---
title: Klassifizierungssätze – Überblick
description: Verwenden Sie Klassifizierungssätze zum Verwalten von Klassifizierungsdaten.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
feature: Classifications
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: ht
source-wordcount: '290'
ht-degree: 100%

---

# Klassifizierungssätze – Überblick

Klassifizierungssätze bieten eine einzige Oberfläche zum Verwalten von Klassifizierungen und Regeln. Dieser Workflow kombiniert das Konzept der Erstellung von Klassifizierungen in den Report Suite-Einstellungen mit dem Konzept des Klassifizierungsimports, um eine intuitivere Benutzeroberfläche zum Erstellen und Verwalten von Klassifizierungsdaten zu bieten.

**[!UICONTROL Komponenten]** > **[!UICONTROL Klassifizierungssätze]**

Die Backend-Architektur, die mit Klassifizierungssätzen veröffentlicht wurde, enthält einige wichtige Verbesserungen:

* Verkürzte Verarbeitungszeit (72 Stunden → 24 Stunden)
* Die Möglichkeit, die Benutzeroberfläche für Klassifizierungssätze zu verwenden
* Die Option, Klassifizierungsdaten in Adobe Experience Platform künftig über den [Adobe Analytics-Quell-Connector für Klassifizierungsdaten](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html?lang=de) zu verwenden

Die Backend-Architektur, die mit Klassifizierungssätzen veröffentlicht wurde, enthält auch einige wichtige Änderungen:

* Bei Verwendung des Browsers oder automatischen Imports ist [!UICONTROL Bei Konflikt überschreiben] immer aktiviert.
* Bei Verwendung des Browser- oder automatischen Imports wird die Option zum sofortigen Export nach dem Import nicht mehr unterstützt. Exporte müssen separat initiiert werden.
* Die Analytics 2.0-API `GetDimensions`-Endpunkt gibt jetzt Zeichenfolgenkennungen für Klassifizierungen anstelle numerischer Kennungen zurück. Numerische Kennungen können zwar weiterhin verwendet werden, Adobe empfiehlt jedoch, nach Möglichkeit die neuen Zeichenfolgenkennungen zu verwenden. Numerische Kennungen können mithilfe der `?expansion=hidden` Abfragezeichenfolgen-Parameter abgerufen werden.

>[!IMPORTANT]
>
>Die Leistung von Klassifizierungssätzen hängt hauptsächlich von der Anzahl der eindeutigen Schlüsselwerte ab, die Daten enthalten. Adobe empfiehlt, bei Variablen, die eine große Anzahl eindeutiger Werte enthalten, mit Sorgfalt vorzugehen. Diese Vorsicht gilt insbesondere bei der Kombination von Variablen aus mehreren Report Suites und Dimensionen zu einem einzigen Klassifizierungssatz.

Klassifizierungssätze bestehen aus zwei Hauptbereichen:

* [**[!UICONTROL Manager für Klassifizierungssätze]**](manage/set-manager.md): Erstellen, bearbeiten und löschen Sie Klassifizierungssätze.
* [**[!UICONTROL Auftrags-Manager für Klassifizierungssätze]**](job-manager.md): Zeigt den Status der Klassifizierungssatz-Aufträge an und ermöglicht es, die Exportdateien herunterzuladen.
* [**[!UICONTROL Klassifizierungssatz-Konsolidieruneng]**](consolidations/manage.md): Kombinieren Sie mehrere Klassifizierungssätze zu einem einzigen Klassifizierungssatz.
