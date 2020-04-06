---
description: Fügen Sie im Marketing-Kanal-Manager Marketingkanäle hinzu oder aktivieren Sie sie. Bei Report Suites ohne Marketing-Kanal können Sie mit einem automatischen Setup mehrere Kanal zusammen mit den zugehörigen Regeln erstellen. Sie können vordefinierte Kanal entsprechend Ihren Anforderungen bearbeiten oder eigene erstellen (bis zu insgesamt 25).
subtopic: Marketing channels
title: Marketing-Kanäle verwalten
topic: Reports and analytics
uuid: 9d367bb6-a17b-49b8-9cd5-24fac35ae982
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Marketing-Kanäle verwalten

Fügen Sie im Marketing-Kanal-Manager Marketingkanäle hinzu oder aktivieren Sie sie. Bei Report Suites ohne Marketing-Kanal können Sie mit einem automatischen Setup mehrere Kanal zusammen mit den zugehörigen Regeln erstellen. Sie können vordefinierte Kanal entsprechend Ihren Anforderungen bearbeiten oder eigene erstellen (bis zu insgesamt 25).

Hier sind die Richtlinien zum Erstellen von Kanälen:

* Planen Sie voraus, indem Sie eine Liste aller Kanal erstellen, sodass alle Ihre Besucher-Treffer in den richtigen Kanal kategorisiert werden.
* Schließen Sie immer Kanal für die Kategorien von [internen](/help/components/c-marketing-channels/c-faq.md) und [direkten](/help/components/c-marketing-channels/c-faq.md) Treffern ein.

Das Hinzufügen von Kanälen zur [!UICONTROL Marketing Channels] Seite erfolgt unabhängig von der Regelerstellung auf der Seite &quot;Verarbeitungsregeln für [Marketing-Kanal](/help/components/c-marketing-channels/c-rules.md) &quot;. Beim Erstellen der Regel verknüpfen Sie Regeln mit Kanälen.

## Hinzufügen von Marketingkanälen {#add-mktg-channels}

Fügen Sie im Marketingkanal-Manager Marketingkanäle hinzu.

>[!NOTE] Ein Kanal kann nicht gelöscht werden. Wenn Sie einen Kanal nicht verwenden möchten, können Sie ihn deaktivieren oder umbenennen oder ihn zur späteren Verwendung aufbewahren.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. On the [!UICONTROL Report Suite Manager] page, select a report suite.

   Wenn Sie mehrere Report Suites auswählen, wählen Sie eine Vorlage aus, mit der die Einstellungen aus der Vorlage in die ausgewählten Report Suites kopiert werden.

   See [Apply template report suite settings to multiple report suites](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

1. Klicken Sie auf **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   Wenn in Ihrer Report Suite keine Kanäle definiert wurden, wird die Seite [Automatisches Setup](/help/components/c-marketing-channels/c-getting-started-mchannel.md) angezeigt.

1. Klicken Sie auf der [!UICONTROL Marketing Channel Manager] Seite auf **[!UICONTROL Add Channel]**.

   Diese Option steht nicht zur Verfügung, wenn 25 Kanäle definiert wurden.

1. Klicken Sie auf **[!UICONTROL Save.]**
1. Klicken Sie zum Konfigurieren der Regeln für den Kanal auf **[!UICONTROL Marketing Channel Processing Rules]**.

   Weitere Informationen finden Sie unter [Einrichten von Marketing-Kanal-Verarbeitungsregeln](/help/components/c-marketing-channels/c-rules.md).

## Marketing-Kanal-Manager – Benutzeroberflächendefinitionen {#mktg-channel-mgr}

Felddefinitionen für die [!UICONTROL Marketing Channel Manager] Seite.

| Feld | Definition |
|--- |--- |
| Aktiviert | Aktiviert oder deaktiviert diesen Marketing-Kanal. |
| Kanalname | Der Anzeigename des Marketing-Kanals. |
| Last Touch-Kanal außer Kraft setzen | Hiermit können Sie festlegen, ob ein vorhandener, beständiger Last Touch-Kanal mit dem ausgewählten Kanal außer Kraft gesetzt werden soll. Wenn Sie dieses Kontrollkästchen aktivieren, setzt jeder Kanal (einschließlich Direkt und Intern) einen vorhandenen Last Touch-Kanal außer Kraft. Dies führt dazu, dass Konversionen den falschen Kanälen gutgeschrieben werden. Beispielsweise kann mit dieser Option sichergestellt werden, dass dem Direct-Kanal keine Konvertierung gutgeschrieben wird, wenn der Benutzer zuvor über den Kanal Kostenlose Suche erworben wurde. |
| Kanalinseln | Hiermit können Sie einen Kanal nach diesem Wert unterteilen. Sie können beim Erstellen von [Marketing Kanal-Classifications](/help/components/c-marketing-channels/classifictions-mchannel.md)mögliche Kanal-Aufschlüsselungen (Unterkanäle) hinzufügen. |
| Typ | Gibt an, wie der Benutzer zu Ihrer Site gelangt ist. Sie können Online oder Offline auswählen. Verwenden Sie Online-Kanal für Besucher, die über eine Suchmaschine oder E-Mail-Kampagne gelangen. Offline-Kanal gelten für Besucher, die Ihre Site über Zeitungsgutscheine oder Zeitschriftenanzeigen gefunden haben. Offline-Kanal enthalten in der Regel Daten, die über Berichte Data Sources importiert wurden. Siehe [Data Sources](https://docs.adobe.com/content/help/de-DE/analytics/import/data-sources/datasrc-home.html). Weitere Informationen finden Sie unter [Hinzufügen von Offline-Daten](/help/components/c-marketing-channels/c-getting-started-mchannel.md). |
| Farbe | Die mit diesem Marketing-Kanal verknüpfte Farbe. Die Farbe stellt den Kanal im Marketingkanal bericht dar. |

## Kanal definieren

Bevor Kanals- und Kanal-Daten im Bericht angezeigt werden können, erstellen Sie die Kanal und die zugrunde liegenden Regeln, die Daten verarbeiten. Sie können auch Kosten- und Budgetbeträge für verbundene Kanal erstellen und angeben, wie lange der Interaktionszeitraum des Besuchers dauern soll. Sie führen Aufgaben zur Berichtskonfiguration in den Admin Tools durch.

Stellen Sie sich einen Kanal als Container für Besuche vor. Die Regeln weisen dem richtigen Container Besuche zu.

![](assets/buckets_2.png)

Adobe stellt während des  [automatischen Setups](/help/components/c-marketing-channels/c-getting-started-mchannel.md) eine Reihe vordefinierter Kanäle bereit, die Sie an Ihre Anforderungen anpassen können.

>[!NOTE]
>
>Adobe empfiehlt, dass Sie Ihren Bericht in einer Report Suite einrichten, die Sie zu Testzwecken als Vorlage verwenden können. Sie können die Vorlage verwenden, um Kanal- und Regelsätze global auf eine oder mehrere Produktions-Report Suites anzuwenden.
>
>See [Apply Template Report Suite Settings to Multiple Report Suites](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

### Voraussetzungen {#prereqs}

Gegebenenfalls müssen Sie sich für Support zu den Voraussetzungen an die Kundenunterstützung wenden:

* In the Administration Console (General Account Settings), enable the **[!UICONTROL Conversion Level]** (e-commerce) option for the report suite.

   Weitere Informationen finden Sie unter [Allgemeine Kontoeinstellungen](https://docs.adobe.com/content/help/de-DE/analytics/admin/admin-tools/general-acct-settings-admin.html) in der Hilfe zu Analytics.

* Richten Sie den Zugriff auf die Marketing Kanal-Dimensionen ein.

   See [Marketing Channels permissions](/help/components/c-marketing-channels/c-channel-report-access.md).

* Ensure that your account manager has enabled **[!UICONTROL Channel Reports]** for your report suite.

### Wichtige Verarbeitungshinweise {#important-proc-rules}

* Das System verarbeitet die Regeln in der von Ihnen angegebenen Reihenfolge. Wenn eine Regel erfüllt ist, stoppt das System die Verarbeitung der verbleibenden Regeln.
* Regeln können auf Variablen zugreifen, die von VISTA festgelegt wurden, jedoch nicht auf Daten zugreifen, die von VISTA gelöscht wurden.
* Kanal speichern nur Konversionsmetriken. Traffic-Metriken sind nicht verfügbar.
* Zwei Marketing-Kanal erhalten nie eine Gutschrift für dasselbe Ereignis (z. B. Einkäufe oder Klicks). Auf diese Weise unterscheiden sich Marketing-Kanal von eVars (wobei zwei eVars für dasselbe Ereignis gutgeschrieben werden können).
* Der Bericht kann bis zu 25 Kanäle gleichzeitig verarbeiten.

