---
title: Anzeigeneinwilligung
description: Weitere Informationen finden Sie in der Konfiguration für die Werbezustimmung für Drittanbieter.
feature: Dimensions
source-git-commit: b5aba8a42f524ef3367a779e6fb1a731de680750
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# Anzeigeneinwilligung

Die &quot;Anzeigeneinwilligung&quot; [Dimension](overview.md) zeigt an, ob die Zustimmung zum Senden von Daten an Drittanbieter für Werbung wie Google, Meta und andere erfasst wird.

Diese Dimension wird derzeit nur für Google verwendet. Aufgrund der europäischen Datenschutzbestimmungen, des Digital Markets Act (DMA), verlangt Google, dass Daten, die an ihre Server gesendet und in Europa erfasst werden, angeben müssen, ob die Einwilligung eingeholt wird. Einige Analytics-Kunden senden Ereignisdaten über Adobe Advertising als Konversionsereignisse an Google.

Künftig kann diese Dimension verwendet werden, um die Kodierung zusätzlicher Zustimmungsinformationen für andere Drittanbieter von Werbung zu unterstützen.

## Füllen dieser Dimension mit Daten

Diese Dimension erfasst Daten aus den folgenden [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md)

* `contextData.['adConsent']`

Sie füllen die Kontextdatenvariable mit relevanten Werten für die Google-Einwilligungsfelder.

* `ad_user_data` (1. Zeichen) und
* `ad_personalization` (2. Zeichen).

Siehe [Zustimmung in der Google Ads API-Referenz](https://developers.google.com/google-ads/api/reference/rpc/v15/Consent) für weitere Informationen.

Die möglichen Werte für jedes dieser Felder können sein:

| Wert | ad_user_data | ad_personalization |
|:-:|---|---|
| `Y` | Erteilen Sie Google eine Einwilligung zu Anzeigenbenutzerdaten. | Erteilen Sie Google eine Zustimmung zur Anzeigenpersonalisierung. |
| `N` | Verweigern Sie die Zustimmung zu Google für Anzeigenbenutzerdaten. | Einverständnis für die Anzeigenpersonalisierung mit Google. |
| `U` | Nicht angegeben. | Nicht angegeben. |

Im folgenden Beispiel wird Google für Anzeigenbenutzerdaten, jedoch nicht für die Anzeigenpersonalisierung genehmigt:

```
contextData.['adConsent'] = "YN..."
```

Zeichen, die über das erste und zweite Zeichen hinausgehen, werden derzeit ignoriert.

## Daten verwenden

Sie können die erfassten Daten der Anzeigenzustimmung verwenden:

* Daten-Feeds: Die Daten zur Anzeigenzustimmung sind mit der Variablen `dataprivacydmaconsent` [column](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md).
* Data Warehouse-Berichte: Die Daten zur Anzeigenzustimmung sind über die **[!UICONTROL Zustimmung zur Anzeigenplattform]** Dimension.


Ihr Unternehmen bestimmt die Logik zur Implementierung dieser Kontextdatenvariablen. Der Wert bleibt nicht über den Treffer hinaus erhalten, für den er festgelegt wurde. Daher müssen Sie die Kontextdatenvariable auf jeder Seite festlegen.

Wenn Sie Werbedaten von Adobe Analytics über Adobe Advertising als Konversionsereignisse an Google senden, wenden Sie sich an das Adobe Advertising-Team, um Hilfe bei der Integration zu erhalten.

Weitere Informationen finden Sie unter [Datenschutzberichte](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md).
