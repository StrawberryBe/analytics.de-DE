---
description: Mit „Bot-Regeln“ können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots verursacht wird. Die Entfernung von Bot-Traffic kann eine genauere Messung der Aktivität von Benutzern auf Ihrer Website ermöglichen.
subtopic: Bot rules
title: Übersicht über Bot-Regeln
topic: Admin tools
uuid: 3cb9e29d-1c37-43de-b7ac-34441093a60e
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Übersicht über Bot-Regeln

Mit Bot-Regeln können Sie Traffic aus Ihrer Report Suite entfernen, der von bekannten Spiders und Bots generiert wird. Die Entfernung von Bot-Traffic kann eine genauere Messung der Aktivität von Benutzern auf Ihrer Website ermöglichen.

Nach der Definition von Bot-Regeln wird aller eingehender Traffic mit den definierten Regeln abgeglichen. Traffic, der mit einer dieser Regeln übereinstimmt, wird nicht in der Report Suite erfasst und nicht in Traffic-Metriken eingeschlossen.

To update or upload bot rules, navigate to **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**. Wählen Sie die richtige Report Suite und gehen Sie dann zu **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Bot Rules]**.

Das Entfernen des Bot-Traffics verringert in der Regel das Traffic- und Konversionsvolumen. Viele Kunden stellen fest, dass die Entfernung von Bot-Traffic zu höheren Konversionsraten und zu höheren Benutzerfreundlichkeitsmetriken führt. Bevor Sie den Bot-Traffic entfernen, sollten Sie mit den Interessenträgern kommunizieren, um sicherzustellen, dass sie die aufgrund dieser Änderung erforderlichen Anpassungen an wichtigen Leistungsindikatoren vornehmen können. Wenn möglich, empfehlen wir, zunächst den Bot-Traffic aus einer kleinen Report Suite zu entfernen, um die potenziellen Auswirkungen abschätzen zu können.

Bot-Traffic-Daten werden in einem separaten Repository zur Anzeige in den Berichten „Bots“ und „Bot-Seiten“ gespeichert. Es gibt zwei Optionen zum Aktivieren der Bot-Filterung:

| Regeltyp | Beschreibung |
|--- |--- |
| Standard-IAB-Bot-Regeln | Selecting [!UICONTROL Enable IAB Bot Filtering Rules] uses the [IAB&#39;s](https://www.iab.com) (International Advertising Bureau&#39;s) International Spiders &amp; Bots List to remove bot traffic. Die meisten Kunden wählen mindestens diese Option aus. |
| Benutzerdefinierte Bot-Regeln | Sie können benutzerdefinierte Bot-Regeln festlegen und hinzufügen, die auf Benutzeragenten, IP-Adressen oder IP-Bereichen basieren. |

## Standard-IAB-Bot-Regeln

Standard-IAB-Bot-Regeln können durch Aktivieren des [!UICONTROL Enable IAB Bot Filtering Rules] Kontrollkästchens aktiviert werden. Diese Auswahl entfernt Bots in der Liste „International Spiders &amp; Bots List“ von IAB (International Advertising Bureau), um Bot-Traffic zu entfernen. IAB aktualisiert diese Liste monatlich.

![](assets/bot-iab-checkbox.png)

Adobe kann die detaillierte IAB-Bot-Liste nicht an Kunden weitergeben, aber Sie können den Bericht „Bots“ verwenden, um eine Liste der Bots anzuzeigen, die auf Ihre Website zugegriffen haben. Um einen Bot an die IAB-Liste zu senden, gehen Sie zu [IAB](https://www.iab.com).

## Benutzerdefinierte Bot-Regeln

>[!Note]: In der Benutzeroberfläche können 500 Regeln manuell definiert werden. Wenn diese Grenze erreicht wurde, müssen Regeln über die Optionen „Datei importieren“ und „Bot-Regeln exportieren“ stapelweise verwaltet werden.

Mit benutzerspezifischen Bot-Regeln können Sie Traffic-basierte Bedingungen filtern, die Sie definieren.

Benutzerspezifische Bot-Regeln werden mithilfe der folgenden Bedingungstypen definiert:

* Benutzeragent
* IP-Adresse
* IP-Bereich

Für eine einzelne Regel können mehrere Bedingungen definiert werden. Mehrere Bedingungen werden mit &quot;oder&quot;abgeglichen. Wenn Sie beispielsweise einen Wert für Benutzeragent und IP-Adresse angeben, wird der Traffic als Bot-Traffic gewertet, wenn eine der beiden Bedingungen erfüllt ist.

### Benutzeragent

A User Agent condition checks the user agent value to see if it **[!UICONTROL starts with]** or **[!UICONTROL contains]** the specified string. If **[!UICONTROL contains]** is selected, the substring is matched if it occurs anywhere in the user agent.

Optional values can be included in the **[!UICONTROL does not contain]** list to define values that the user agent must not contain for a successful match. Es können mehrere Werte angegeben werden, indem ein Wert pro Zeile eingefügt wird. Wenn der Benutzeragent die in der Übereinstimmungszeichenfolge angegebenen Kriterien erfüllt, aber auch eine Zeichenfolge auf der enthält keine Liste, wird er nicht als Übereinstimmung betrachtet.

The **[!UICONTROL contains]** field is limited to 100 characters. Die Zeile enthält keine Liste ist auf 255 Zeichen minus Trennzeichen für jede neue Zeile beschränkt. (Dies entspricht der Anzahl der Zeichenfolgen - 1. Wenn Sie 4 *enthält* keine Zeichenfolgen angeben, sind 3 Trennzeichen erforderlich.) Bei allen Zeichenfolgenübereinstimmungen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

### IP-Adresse (inklusive Wildcard-Übereinstimmungen)

Entspricht einer IP-Adresse oder mehreren Adressen im selben Block mit Platzhaltern (*). Geben Sie die numerischen Werte der IP-Adresse ein, die Sie abgleichen möchten. Ersetzen Sie * für alle Werte, die Sie mit einem Platzhalter abgleichen möchten. Die folgende Liste enthält Beispiele für eine IP-Adressen-Übereinstimmungszeichenfolge:

```
10.10.10.1
10.10.10.*
```

### IP-Adressbereich

Geben Sie den Beginn und die Endbereiche der IP-Adressen an, die übereinstimmen sollen. Ersetzen Sie * für alle Werte, die Sie mit einem Platzhalter abgleichen möchten.

### Definieren einer benutzerdefinierten Bot-Regel

1. Gehen Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]**, wählen Sie eine oder mehrere Report Suites aus und klicken Sie auf **[!UICONTROL General]** > **[!UICONTROL Bot Rules]**.
1. Click **[!UICONTROL Add Rule]** and define one or more match conditions.
1. Klicken Sie auf **[!UICONTROL Save]**. Die Änderung sollte binnen 30 Minuten in Kraft treten.

## Hochladen von Bot-Regeln

Um Bot-Regeln stapelweise zu importieren, können Sie eine CSV-Datei hochladen, die die Regeln definiert.

Erstellen Sie eine CSV-Datei mit den folgenden Spalten in der angegebenen Reihenfolge:

| Spalte 1 | Spalte 2 | Spalte 3 | Spalte 4 | Spalte 5 |
|--- |--- |---|---|---|
| Bot-Name | IP-Start | IP-Ende | Agent-Übereinstimmungsregel<br>(enthält oder beginnt mit)</br> | Agent ausschließlich<br>(maximal 255 Zeichen)</br> |

Sie können drei Arten von Bot-Regeln definieren:

* Benutzeragent enthält oder Beginn mit
* Einzelne IP-Adresse oder Wildcard-Übereinstimmung
* IP-Bereichsübereinstimmung

Jede Zeile in der Importdatei darf nur eine der folgenden Bot-Definitionen enthalten:

* **Benutzeragent enthält oder Beginn mit**: Geben Sie eine Zeichenfolge für einen einzelnen Benutzeragenten an, die in der Spalte Agent einschließlich übereinstimmen soll. Geben Sie den gewünschten Übereinstimmungstyp an, indem Sie im Feld Agent-Übereinstimmungsregel *enthält* oder *Beginn mit* platzieren. Ein optionaler Wert kann in die Spalte „Agent ausschließlich“ aufgenommen werden, der eine oder mehrere längsstrichgetrennte (`|`) Zeichenketten definiert, die der Agent nicht enthalten darf. Bei Zeichenfolgenübereinstimmungen wird nicht zwischen Groß- und Kleinschreibung unterschieden. Die Spalten IP-Beginn und IP-Ende müssen leer sein.

* **Einzelne IP-Adresse oder Wildcard-Übereinstimmung**: Um eine Übereinstimmung mit einer einzelnen IP-Adresse (`10.10.10.1`) oder einer Platzhalter-IP-Adresse (`10.10.*.*`) herzustellen, platzieren Sie denselben Wert in den Spalten „IP-Start“ und „IP-Ende“. „Übereinstimmungsregel“, „Agent einschließlich“ und „Agent ausschließlich“ müssen leer sein.

* **IP-Bereichsübereinstimmung**: Definieren Sie einen IP-Adressenbereich mithilfe der Spalten IP-Beginn und IP-Ende. Sie können Platzhalter nutzen, um Übereinstimmungen für IP-Bereiche zu finden, z. B. `10.10.10.*` bis `10.10.20.*`. „Übereinstimmungsregel“, „Agent einschließlich“ und „Agent ausschließlich“ müssen leer sein.

### Mehrere mit ODER kombinierte Regeln

Wenn Sie einen Bot mit einer Kombination von Regeln, die mit einem ODER verbunden sind (z. B. Benutzeragent oder IP-Adresse), abgleichen möchten, geben Sie einen identischen Namen für alle Regeln ein, die Sie im Feld Bot-Name kombinieren möchten. UND-Übereinstimmungen werden nicht unterstützt.

### Überschreiben aller Regeln mit einer hochgeladenen Datei

Select the **[!UICONTROL Overwrite existing rules]** checkbox to delete all existing rules and replace them with the rules defined in the upload file.

### Exportieren von Regeln

The **[!UICONTROL Export Uploaded Bot File]** button exports all rules defined in the UI in a CSV format.


## Auswirkung von Bot-Regeln auf die Datenerfassung {#section_F01A3130E7A04A9993371CF26F6586F2}

Bot-Regeln gelten für alle Analysedaten. Mithilfe von Bot-Regeln entfernte Daten sind nur in den Berichten „Bots“ und „Bot-Seiten“ sichtbar.

VISTA-Regeln werden nach den Bot-Regeln angewendet (siehe [Verarbeitungsreihenfolge).](/help/admin/admin/c-processing-rules/c-processing-rules-configuration/processing-rule-order.md)

**Verarbeitung von Hoch-Treffer-Besuchen:** Wenn bei einem Besuch mehr als 100 Treffer auftreten, bestimmt Berichte, ob die Besuchszeit in Sekunden kleiner oder gleich der Anzahl der Treffer beim Besuch ist. In diesem Fall gehen die Beginn aufgrund der Kosten für die Verarbeitung langer, intensiver Besuche mit einem neuen Besuch vorbei. Besuche mit hohen Treffern werden in der Regel durch Bot-Angriffe verursacht und gelten nicht als normales Browsen von Besuchern.

>[!NOTE] Treffer, die als *`bots`* markiert sind, werden als [-Serveraufrufe in Rechnung gestellt.](/help/admin/c-server-call-usage/overage-overview.md)

## Auswirkung der IP-Verschleierung auf die Bot-Filterung {#section_92E60B95BE8940D983F28C79E0CD6B12}

Die IAB-Bot-Liste basiert ausschließlich auf dem Benutzeragenten, sodass die Filterung auf der Grundlage dieser Liste nicht durch IP-Verschleierungseinstellungen beeinträchtigt wird. Bei Nicht-IAB-Bot-Filterung (benutzerdefinierte Regeln) kann die IP Teil der Filterkriterien sein. Wenn Bots mit IP gefiltert werden, erfolgt die Bot-Filterung, nachdem das letzte Oktett entfernt wurde, wenn diese Einstellung aktiviert ist, aber vor den anderen IP-Verschleierungsoptionen, wie dem Löschen der gesamten IP oder dem Ersetzen durch eine eindeutige ID.

Wenn die IP-Verschleierung aktiviert ist, wird der IP-Ausschluss durchgeführt, bevor die IP-Adresse verschleiert wird. Kunden müssen also nichts ändern, wenn sie die IP-Verschleierung aktivieren.

Wenn das letzte Oktett entfernt wird, erfolgt dies vor der IP-Filterung. Daher wird das letzte Oktett durch den Wert 0 ersetzt, und die Regeln zum IP-Ausschluss sollten aktualisiert werden, damit IP-Adressen mit einer Null am Ende übereinstimmen. Übereinstimmung * sollte mit 0 übereinstimmen.
