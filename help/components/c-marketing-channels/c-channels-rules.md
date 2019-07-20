---
description: Bevor Kanäle und ihre Daten im Bericht angezeigt werden, müssen Sie die Kanäle und die zur Datenverarbeitung erforderlichen Regeln einrichten. Sie können auch Kosten- und Budgetbeträge für betreffende Kanälen einrichten und angeben, wie lange der Besucherinteraktionszeitraum dauern soll. Sie führen Berichtskonfigurationsaufgaben in „Admin Tools“ durch.
seo-description: Bevor Kanäle und ihre Daten im Bericht angezeigt werden, müssen Sie die Kanäle und die zur Datenverarbeitung erforderlichen Regeln einrichten. Sie können auch Kosten- und Budgetbeträge für betreffende Kanälen einrichten und angeben, wie lange der Besucherinteraktionszeitraum dauern soll. Sie führen Berichtskonfigurationsaufgaben in „Admin Tools“ durch.
seo-title: Informationen zu Kanälen und Regeln
solution: Analytics
subtopic: Marketingkanäle
title: Informationen zu Kanälen und Regeln
topic: Reports and Analytics
uuid: 7 d 774790-4 d 0 d -419 d -8 fb 5-c 16 ec 5 a 4 a 387
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Informationen zu Kanälen und Regeln

Bevor Kanäle und ihre Daten im Bericht angezeigt werden, müssen Sie die Kanäle und die zur Datenverarbeitung erforderlichen Regeln einrichten. Sie können auch Kosten- und Budgetbeträge für betreffende Kanälen einrichten und angeben, wie lange der Besucherinteraktionszeitraum dauern soll. Sie führen Berichtskonfigurationsaufgaben in „Admin Tools“ durch.

Ein Kanal ist im Grunde nichts anderes als ein Behälter für Besuche und die Regeln ordnen die Besuche in den richtigen Behälter ein.

![](assets/buckets_2.png)

Adobe stellt während des [automatischen Setups](../../components/c-marketing-channels/c-channel-autosetup.md#topic_E9ABE9E9E71B4E40A4E7EA9AD2C0372B) eine Reihe vordefinierter Kanäle bereit, die Sie an Ihre Anforderungen anpassen können.

>[!NOTE]
>
>Adobe empfiehlt, dass Sie Ihren Bericht in einer Report Suite einrichten, die Sie zu Testzwecken als Vorlage verwenden können. Verwenden Sie die Vorlage, um Kanal- und Regelsätze global auf eine oder mehrere Produktions-Report Suites anzuwenden.
>
>Siehe [Übernehmen von Report Suite-Vorlageneinstellungen für mehrere Report Suites](../../components/c-marketing-channels/t-template.md#task_0DE0A320EDA94FC5A6E5912868B6E2DC).

Lesen Sie folgende Themen durch:

* [Voraussetzungen](../../components/c-marketing-channels/c-channels-rules.md#section_9913D2932E3140C099B7978CA95378B2)
* [Wichtige Verarbeitungshinweise](../../components/c-marketing-channels/c-channels-rules.md#section_DE372EEF02314F2395750CF2892DAAE1)

## Voraussetzungen {#section_9913D2932E3140C099B7978CA95378B2}

Gegebenenfalls müssen Sie sich für Support zu den Voraussetzungen an die Kundenunterstützung wenden:

* In the Administration Console (General Account Settings), enable the **[!UICONTROL Conversion Level]** (e-commerce) option for the report suite.

   See [General Account Settings](https://marketing.adobe.com/resources/help/en_US/reference/general_acct_settings_admin.html) in Analytics help for more information.

* Richten Sie den Benutzergruppenzugriff auf den **[!UICONTROL Marketingkanalbericht ein]**.

   See [Configure User Group Access](../../components/c-marketing-channels/t-user-groups.md#task_B156E7527FE94055A43A697338FE8C8C).

* Ensure that your account manager has enabled **[!UICONTROL Channel Reports]** for your report suite.

## Important processing notes {#section_DE372EEF02314F2395750CF2892DAAE1}

* Das System verarbeitet die Regeln in der angegebenen Reihenfolge. Sobald eine Regel erfüllt ist, stoppt das System die Verarbeitung der verbleibenden Regeln.
* Regeln haben Zugriff auf Variablen, die von VISTA gesetzt wurden, können jedoch nicht auf Daten zugreifen, die von VISTA gelöscht wurden.
* Kanäle speichern nur Konversionsmetriken. Traffic-Metriken stehen nicht zur Verfügung.
* Dasselbe Ereignis kann niemals zwei Marketingkanälen gutgeschrieben werden (wie Käufe oder Klicks). In dieser Hinsicht unterscheiden sich Marketingkanäle von eVars (dasselbe Ereignis kann zwei eVars gutgeschrieben werden).
* Der Bericht kann bis zu 25 Kanäle gleichzeitig verarbeiten.

