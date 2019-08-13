---
description: Mit „Bot Rules“ können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots verursacht wird. Mit der Entfernung von Bot-Traffic erhalten Sie eine präzisere Messung der Benutzeraktivität auf Ihrer Website.
seo-description: Mit „Bot Rules“ können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots verursacht wird. Mit der Entfernung von Bot-Traffic erhalten Sie eine präzisere Messung der Benutzeraktivität auf Ihrer Website.
seo-title: Bot-Regeln
solution: Analytics
subtopic: Bot Rules
title: Bot-Regeln
topic: Admin Tools
uuid: 3 cb 9 e 29 d -1 c 37-43 de-b 7 ac -44441093 a 60 e
translation-type: tm+mt
source-git-commit: 4a627e268994d0152a19fb44e9bc06ea7ebc64c6

---


# Bot-Regeln

Mit Bot-Regeln können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots generiert wird. Mit der Entfernung von Bot-Traffic erhalten Sie eine präzisere Messung der Benutzeraktivität auf Ihrer Website.

Nach der Definition von Bot Rules wird aller eingehender Traffic mit den definierten Regeln abgeglichen. Traffic, der mit einer dieser Regeln übereinstimmt, wird nicht in der Report Suite erfasst und nicht in Traffic-Metriken berücksichtigt.

To update or upload bot rules, navigate to **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**. Select the correct Report Suite, and then go to **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Bot Rules]**.

Mit der Entfernung von Bot-Traffic werden das Traffic-Volumen und die Konversionsmetriken vermindert. Viele Kunden haben die Erfahrung gemacht, dass die Entfernung von Bot-Traffic zu höheren Konversionsraten und Anstiegen in anderen Usability-Metriken führt. Bevor Sie den Bot-Traffic entfernen, machen Sie Stakeholder darauf aufmerksam, damit diese die im Zuge der Änderung notwendigen Anpassungen an wichtige Kennzahlen vornehmen können. Wenn möglich, wird empfohlen, zunächst den Bot-Traffic aus einer kleinen Report Suite zu entfernen, um die potenziellen Auswirkungen abschätzen zu können.

>[!NOTE] Es wird empfohlen, pro Report Suite nicht mehr als 500 Bot-Regeln zu definieren. In der Benutzeroberfläche können 500 Regeln manuell definiert werden. Nach dem Erreichen dieser Grenze müssen Regeln zusammen über die [Optionen „Datei importieren“](../../../admin/admin/bot-removal/t-upload-bot-rules.md#task_95868D8564564E6A996163335C119806) und „Bot-Regeln exportieren“ verwaltet werden.

Bot-Traffic-Daten werden in einem separaten Repository zur Anzeige der Berichte, [!UICONTROL Bots] und [!UICONTROL Bot Pages] gespeichert.

| Regeltyp | Beschreibung |
|--- |--- |
| IAB | Selecting [!UICONTROL Include IAB] uses the IAB's (International Advertising Bureau's) International Spiders &amp; Bots List to remove bot traffic. Diese Liste wird monatlich vom IAB aktualisiert. <br>Um einen Bot an die IAB-Liste zu senden, besuchen Sie [IAB](https://www.iab.net/sites/spiders/form.php). <br>Adobe kann Kunden leider keine detaillierte IAB-Bot-Liste zur Verfügung stellen. Sie können aber den Bots Report nutzen, um eine Liste der Bots zu sehen, die auf Ihre Website zugegriffen haben. |
| Benutzerspezifische Bot-Regeln | Siehe [Erstellen einer benutzerspezifischen Bot-Regel](../../../admin/admin/bot-removal/t-create-bot-rules.md). |

## Auswirkung von Bot-Regeln auf die Datenerfassung {#section_F01A3130E7A04A9993371CF26F6586F2}

Bot-Regeln gelten für alle Analysedaten. Mithilfe von Bot-Regeln entfernte Daten sind nur in den Berichten „Bots“ und „Bots Pages“ sichtbar.

VISTA rules are applied after Bot Rules (see [Processing Order](../../../admin/admin/c-processing-rules/c-processing-rules-configuration/processing-rule-order.md#concept_8A6BBEA7F50C40C8A8D8755D4F579B1E)).

**Verarbeitung von Besuchen mit hoher Hit-Zahl:** Wenn mehr als 100 Hits in einem Besuch auftreten, wird bei der Berichterstellung ermittelt, ob der Zeitraum des Besuchs (in Sekunden) kleiner oder gleich der Anzahl der Hits bei diesem Besuch ist. In dieser Situation beginnt die Berichterstellung mit dem nächsten Besuch neu, da die Verarbeitung langer, intensiver Besuche hohe Kosten verursacht. Besuche mit hoher Hit-Zahl werden in der Regel durch Bot-Angriffe verursacht und gelten nicht als normales Browsen von Besuchern.

>[!NOTE]
>
>Treffer, die als *`bots`*[Serveraufrufe gekennzeichnet werden](https://docs.adobe.com/content/help/en/analytics/admin/server-call-usage/overage-overview.html).

## Auswirkung von IP-Verschleierung auf Bot-Filterung {#section_92E60B95BE8940D983F28C79E0CD6B12}

Die IAB-Bot-Liste basiert lediglich auf dem Benutzeragenten, so dass das Filtern auf der Basis dieser Liste nicht durch die IP-Verschleierungseinstellungen beeinträchtigt wird. Bei Nicht-IAB-Bot-Filterung (benutzerdefinierte Regeln) kann die IP Bestandteil der Filterkriterien sein. Beim Filtern von Bots mithilfe von IP erfolgt die Bot-Filterung nach Entfernung des letzten Oktetts, sofern diese Einstellung aktiviert ist, jedoch vor den anderen IP-Verschleierungseinstellungen wie z. B. dem Löschen der gesamten IP oder dem Austausch durch eine eindeutige ID.

Wenn die IP-Verschleierung aktiviert ist, wird der IP-Ausschluss durchgeführt, bevor die IP verschleiert wird. Kunden müssen also keine Änderungen vornehmen, wenn sie die IP-Verschleierung aktivieren.

Wenn das letzte Oktett entfernt wird, geschieht dies vor der IP-Filterung. Dabei wird das letzte Oktett mit „0“ ersetzt und die Regeln für den IP-Ausschluss sollten angepasst werden, um IP-Adressen mit einer Null am Ende zu berücksichtigen. Übereinstimmung * sollte mit 0 übereinstimmen.
