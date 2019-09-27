---
description: Fügen Sie Marketingkanalberichten Offlinedaten hinzu.
seo-description: Fügen Sie Marketingkanalberichten Offlinedaten hinzu.
seo-title: Hinzufügen von Offline-Daten
solution: Analytics
subtopic: Marketingkanäle
title: Hinzufügen von Offline-Daten
topic: Reports and Analytics
uuid: bbf4661a-b6b1-4a89-a3cf-ae8dd785d37d
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# Hinzufügen von Offline-Daten

Fügen Sie Marketingkanalberichten Offlinedaten hinzu.

Online-Kanäle ermöglichen die Datenkategorisierung zu Besuchern, die über Suchmaschinen, Internet-Werbung, verweisende Domänen oder E-Mail-Kampagnen zu Ihnen gelangen. Offline-Kanäle gelten für Besucher, die Ihre Site durch TV-Werbung oder Anzeigen in Zeitungen und Zeitschriften fanden.

**Datenquellen in Marketingkanalberichte integrieren**

Wenn Sie [datenbezogene Daten](https://marketing.adobe.com/resources/help/en_US/sc/datasources/c_faq.html) in Marketingkanalberichte integrieren möchten, sollten Sie Folgendes beachten:

* Sämtliche standardmäßigen Treffer, die an Analyseberichte mit einer [transactionID](https://marketing.adobe.com/resources/help/en_US/sc/datasources/c_Transaction_ID.html) geleitet werden, werden durch Marketingkanal-Verarbeitungsregeln als normal verarbeitet.
* Sämtliche in Analysen geleitete `transactionID`-Datenquellen sind automatisch mit demselben Marketingkanal verbunden, auf dem der standardmäßige Treffer verarbeitet wurde.
* Sämtliche andere datenbezogenen Daten werden nicht durch Marketingkanal-Verarbeitungsregeln geleitet.

Weitere Informationen über Data Sources finden Sie in der Hilfe zu [Data Sources](https://marketing.adobe.com/resources/help/en_US/sc/datasources/index.html).

Zur Klassifizierung von Offline-Kanaldaten müssen Sie die Daten in Data Sources aktivieren, dann herunterladen und die Vorlage bearbeiten.

Siehe „Mit Data Sources arbeiten“ im [Data Sources-Benutzerhandbuch](https://marketing.adobe.com/resources/help/en_US/sc/datasources/index.html).

**Hinzufügen von Offline-Daten**

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Data Sources]**.
1. Klicken Sie auf der Seite „Datenquellen“ auf **[!UICONTROL Erstellen.]**
1. Under **[!UICONTROL 1. Kategorie auswählen]** die Option **[!UICONTROL Offline-Kanaldaten aus]**.
1. Under **[!UICONTROL 2. Typ auswählen]** die Option **[!UICONTROL Offline-Kanaldaten]**.
1. Click **[!UICONTROL Activate.]**
1. Ordnen Sie den Berichterstellungsmetriken die Offline-Metriken zu, indem Sie den Eingabeaufforderungen im Datenquellen-Aktivierungsassistenten folgen.
1. Laden und bearbeiten Sie die Vorlagendatei in einem Texteditor wie z. B. Excel.

   Siehe „Data Sources-Datei erstellen“ im [Data Sources-Benutzerhandbuch](https://marketing.adobe.com/resources/help/en_US/sc/datasources/index.html).

1. Laden Sie die Datei hoch wie in „Hochladen einer Data Sources-Datei“ im [Data Sources-Benutzerhandbuch beschrieben](https://marketing.adobe.com/resources/help/en_US/sc/datasources/index.html).
