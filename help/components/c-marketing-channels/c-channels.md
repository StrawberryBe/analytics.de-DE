---
description: Fügen Sie im Marketing-Kanal-Manager Marketingkanäle hinzu oder aktivieren Sie sie. Für Report Suites ohne Marketingkanäle können Sie mit einem automatischen Setup mehrere Kanäle und deren Regeln erstellen. Sie können die vordefinierten Kanäle an Ihren Bedarf anpassen oder neue erstellen (bis insgesamt 25).
subtopic: Marketing channels
title: Marketing-Kanäle verwalten
topic: Reports and analytics
uuid: 9d367bb6-a17b-49b8-9cd5-24fac35ae982
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Marketing-Kanäle verwalten

Fügen Sie im Marketing-Kanal-Manager Marketingkanäle hinzu oder aktivieren Sie sie. Für Report Suites ohne Marketingkanäle können Sie mit einem automatischen Setup mehrere Kanäle und deren Regeln erstellen. Sie können die vordefinierten Kanäle an Ihren Bedarf anpassen oder neue erstellen (bis insgesamt 25).

Beachten Sie bei der Erstellung von Kanälen die folgenden Richtlinien:

* Richten Sie in der Vorbereitung eine Liste aller Kanäle ein, so dass alle Besucherzugriffe in die richtigen Kanäle eingeordnet werden.
* Denken Sie daran, immer Kanäle in den Trefferkategorien [Intern](/help/components/c-marketing-channels/c-faq.md) und [Direkt](/help/components/c-marketing-channels/c-faq.md) in die Liste aufzunehmen.

Der Zusatz von Kanälen in der [!UICONTROL Marketingkanal]-Seite erfolgt separat von der Regelerstellung in der Seite der [Marketingkanal-Verarbeitungsregeln](/help/components/c-marketing-channels/c-rules.md). Bei der Regelerstellung verbinden Sie Regeln mit Kanälen.

## Hinzufügen von Marketingkanälen {#add-mktg-channels}

Fügen Sie im Marketingkanal-Manager Marketingkanäle hinzu.

>[!NOTE] Ein Kanal kann nicht gelöscht werden. Wenn Sie einen Kanal nicht verwenden möchten, können Sie ihn deaktivieren oder umbenennen oder ihn zur späteren Verwendung aufbewahren.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Wählen Sie im [!UICONTROL Report Suite Manager] die Report Suite aus.

   Wenn Sie mehrere Report Suites auswählen, wählen Sie eine Vorlage aus, die die Einstellungen aus der Vorlage in die jeweiligen Report Suites kopiert.

   Siehe [Übernehmen von Report Suite-Vorlageneinstellungen für mehrere Report Suites](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Marketingkanäle]** > **[!UICONTROL Marketingkanal-Manager]**.

   Wenn in Ihrer Report Suite keine Kanäle definiert wurden, wird die Seite [Automatisches Setup](/help/components/c-marketing-channels/c-getting-started-mchannel.md) angezeigt.

1. Klicken Sie auf der Seite [!UICONTROL Marketingkanal-Manager] auf **[!UICONTROL Kanal hinzufügen]**.

   Diese Option steht nicht zur Verfügung, wenn 25 Kanäle definiert wurden.

1. Klicken Sie auf **[!UICONTROL Speichern.]**
1. Klicken Sie zur Regelkonfiguration für den Kanal auf **[!UICONTROL Marketing-Kanal-Verarbeitungsregeln]**.

   Weitere Informationen finden Sie unter [Einrichten von Marketing-Kanal-Verarbeitungsregeln](/help/components/c-marketing-channels/c-rules.md).

## Marketing-Kanal-Manager – Benutzeroberflächendefinitionen {#mktg-channel-mgr}

Felddefinitionen für die Seite [!UICONTROL Marketingkanal-Manager].

| Feld | Definition |
|--- |--- |
| Aktiviert | Aktiviert oder deaktiviert den Marketingkanal. |
| Kanalname | Benutzerfreundlicher Name des Marketingkanals. |
| Last Touch-Kanal außer Kraft setzen | Ermöglicht Ihnen, je nach Bedarf einen vorhandenen, beständigen Last Touch-Kanal durch den gewählten Kanal außer Kraft zu setzen. Wenn Sie diese Option auswählen, könnte jeder beliebige Kanal (einschließlich Direkt und Intern) einen vorhandenen Last Touch-Kanal außer Kraft setzen. Dies führt dazu, dass Konversionen den falschen Kanälen gutgeschrieben werden. Diese Option kann beispielsweise sicherstellen, dass dem direkten Kanal keine Konversionen gutgeschrieben werden, wenn der Benutzer zuvor über den Kanal Kostenlose Suche angeworben wurde. |
| Kanalinseln | Ermöglicht die Unterteilung des Kanals nach diesem Wert. You can add possible channel breakdowns (subchannels) when creating [marketing channel classifications](/help/components/c-marketing-channels/classifictions-mchannel.md). |
| Typ | Zeigt an, wie der Benutzer zu Ihrer Site gelangt ist. Sie können Online oder Offline auswählen. Online-Kanäle lassen sich z. B. für Besucher einsetzen, die über eine Suchmaschine oder E-Mail-Kampagne zu Ihrer Site gelangten. Offline-Kanäle gelten beispielsweise für Besucher, die Ihre Site durch Anzeigen in Zeitungen oder Zeitschriften fanden. Offlinekanäle beinhalten in der Regel Daten, die über Berichterstellungs-Data Sources importiert wurden. Siehe [Data Sources](https://docs.adobe.com/content/help/de-DE/analytics/import/data-sources/datasrc-home.html). Weitere Informationen finden Sie unter [Hinzufügen von Offline-Daten](/help/components/c-marketing-channels/c-getting-started-mchannel.md). |
| Kanalfarbe | Die mit diesem Marketingkanal verbundene Farbe. Die Farbe stellt den Kanal im Marketingkanal bericht dar. |

## Kanal definieren

Bevor Kanäle und ihre Daten im Bericht angezeigt werden, müssen Sie die Kanäle und die zur Datenverarbeitung erforderlichen Regeln einrichten. Sie können auch Kosten- und Budgetbeträge für betreffende Kanälen einrichten und angeben, wie lange der Besucherinteraktionszeitraum dauern soll. Sie führen Berichtskonfigurationsaufgaben in „Admin Tools“ durch.

Ein Kanal ist im Grunde nichts anderes als ein Behälter für Besuche und die Regeln ordnen die Besuche in den richtigen Behälter ein.

![](assets/buckets_2.png)

Adobe stellt während des  [automatischen Setups](/help/components/c-marketing-channels/c-getting-started-mchannel.md) eine Reihe vordefinierter Kanäle bereit, die Sie an Ihre Anforderungen anpassen können.

>[!NOTE]
>
>Adobe empfiehlt, dass Sie Ihren Bericht in einer Report Suite einrichten, die Sie zu Testzwecken als Vorlage verwenden können. Verwenden Sie die Vorlage, um Kanal- und Regelsätze global auf eine oder mehrere Produktions-Report Suites anzuwenden.
>
>Siehe [Übernehmen von Report Suite-Vorlageneinstellungen für mehrere Report Suites](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

### Voraussetzungen {#prereqs}

Gegebenenfalls müssen Sie sich für Support zu den Voraussetzungen an die Kundenunterstützung wenden:

* Aktivieren Sie in den allgemeinen Kontoeinstellungen der Admin Console die Option **[!UICONTROL Konversionsstufe]** (E-Commerce) für die Report Suite.

   Weitere Informationen finden Sie unter [Allgemeine Kontoeinstellungen](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/general-acct-settings-admin.html) in der Hilfe zu Analytics.

* Richten Sie den Zugriff auf die Marketing Kanal-Dimensionen ein.

   See [Marketing Channels permissions](/help/components/c-marketing-channels/c-channel-report-access.md).

* Stellen Sie sicher, dass Ihr Kundenbetreuer die **[!UICONTROL Kanalberichte]** für Ihre Report Suite aktiviert hat.

### Wichtige Verarbeitungshinweise {#important-proc-rules}

* Das System verarbeitet die Regeln in der angegebenen Reihenfolge. Sobald eine Regel erfüllt ist, stoppt das System die Verarbeitung der verbleibenden Regeln.
* Regeln haben Zugriff auf Variablen, die von VISTA gesetzt wurden, können jedoch nicht auf Daten zugreifen, die von VISTA gelöscht wurden.
* Kanäle speichern nur Konversionsmetriken. Traffic-Metriken stehen nicht zur Verfügung.
* Dasselbe Ereignis kann niemals zwei Marketingkanälen gutgeschrieben werden (wie Käufe oder Klicks). In dieser Hinsicht unterscheiden sich Marketingkanäle von eVars (dasselbe Ereignis kann zwei eVars gutgeschrieben werden).
* Der Bericht kann bis zu 25 Kanäle gleichzeitig verarbeiten.

