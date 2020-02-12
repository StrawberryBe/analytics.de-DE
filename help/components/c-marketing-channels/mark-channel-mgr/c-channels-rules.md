---
title: Kanäle definieren
description: Bevor Kanäle und ihre Daten im Bericht angezeigt werden, müssen Sie die Kanäle und die zur Datenverarbeitung erforderlichen Regeln einrichten. Sie können auch Kosten- und Budgetbeträge für betreffende Kanälen einrichten und angeben, wie lange der Besucherinteraktionszeitraum dauern soll. Sie führen Berichtskonfigurationsaufgaben in „Admin Tools“ durch.
translation-type: tm+mt
source-git-commit: e080c38e536f710490291aaca252cba36456b0f9

---


# Kanäle definieren

Bevor Kanäle und ihre Daten im Bericht angezeigt werden, müssen Sie die Kanäle und die zur Datenverarbeitung erforderlichen Regeln einrichten. Sie können auch Kosten- und Budgetbeträge für betreffende Kanälen einrichten und angeben, wie lange der Besucherinteraktionszeitraum dauern soll. Sie führen Berichtskonfigurationsaufgaben in „Admin Tools“ durch.

Ein Kanal ist im Grunde nichts anderes als ein Behälter für Besuche und die Regeln ordnen die Besuche in den richtigen Behälter ein.

![](assets/buckets_2.png)

Adobe stellt während des [automatischen Setups](/help/components/c-marketing-channels/getting-started/c-channel-autosetup.md) eine Reihe vordefinierter Kanäle bereit, die Sie an Ihre Anforderungen anpassen können.

>[!NOTE]
>
>Adobe empfiehlt, dass Sie Ihren Bericht in einer Report Suite einrichten, die Sie zu Testzwecken als Vorlage verwenden können. Verwenden Sie die Vorlage, um Kanal- und Regelsätze global auf eine oder mehrere Produktions-Report Suites anzuwenden.
>
>Siehe [Übernehmen von Report Suite-Vorlageneinstellungen für mehrere Report Suites](/help/components/c-marketing-channels/getting-started/t-template.md).

## Voraussetzungen {#prereqs}

Gegebenenfalls müssen Sie sich für Support zu den Voraussetzungen an die Kundenunterstützung wenden:

* In the Administration Console (General Account Settings), enable the **[!UICONTROL Conversion Level]** (e-commerce) option for the report suite.

   Weitere Informationen finden Sie unter [Allgemeine Kontoeinstellungen](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/general-acct-settings-admin.html) in der Hilfe zu Analytics.

* Richten Sie den Zugriff auf die Marketingkanal-Dimensionen ein.

   See [Marketing Channels permissions](/help/components/c-marketing-channels/mc-access/c-channel-report-access.md).

* Ensure that your account manager has enabled **[!UICONTROL Channel Reports]** for your report suite.

## Wichtige Verarbeitungshinweise {#important-proc-rules}

* Das System verarbeitet die Regeln in der angegebenen Reihenfolge. Sobald eine Regel erfüllt ist, stoppt das System die Verarbeitung der verbleibenden Regeln.
* Regeln haben Zugriff auf Variablen, die von VISTA gesetzt wurden, können jedoch nicht auf Daten zugreifen, die von VISTA gelöscht wurden.
* Kanäle speichern nur Konversionsmetriken. Traffic-Metriken stehen nicht zur Verfügung.
* Dasselbe Ereignis kann niemals zwei Marketingkanälen gutgeschrieben werden (wie Käufe oder Klicks). In dieser Hinsicht unterscheiden sich Marketingkanäle von eVars (dasselbe Ereignis kann zwei eVars gutgeschrieben werden).
* Der Bericht kann bis zu 25 Kanäle gleichzeitig verarbeiten.

