---
description: Erfahren Sie mehr über Best Practices und Beispiele, wie Sie die verschiedenen Regeln füllen, die Sie ggf. für Ihre Marketingkanäle einrichten.
title: Häufig gestellte Fragen und Beispiele zu Marketing-Kanälen
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Häufig gestellte Fragen und Beispiele zu Marketing-Kanälen

See [Create Marketing Channel Processing Rules](/help/components/c-marketing-channels/c-rules.md) for definitions of fields displayed on the [!UICONTROL Marketing Channel Processing Rules] page.

## Häufig gestellte Fragen {#faq}

Jede Implementierung der Verarbeitungsregeln für Marketing Kanal kann je nach Rückverfolgungscodes unterschiedlich sein. Die Konfiguration von Regeln, die Ergebnisse liefern, nach denen Sie suchen, kann kreatives Denken erfordern, um Probleme zu lösen.

**Frage**: Meine Trackingcodes folgen keinem Muster und ich habe Tausende, die für meinen Affiliates-Kanal angegeben werden müssen.

* Sortieren Sie aus, was Sie nicht brauchen. Wenn Ihre E-Mail- und Affiliates-Kanal denselben Zeichenfolgenparameter für Abfragen verwenden, Sie jedoch nur über wenige E-Mail-Tracking-Codes verfügen, können Sie die E-Mail-Tracking-Codes in einem Regelsatz angeben, der E-Mail definiert. Klassifizieren Sie dann alle weiteren Trackingcodes als  *`affiliates.`*
* Fügen Sie allen Landingpage-URLs in Ihrem E-Mail-System einen Abfragezeichenfolgenparameter hinzu, z. B. *`&ch=eml`*. Erstellen Sie einen Regelsatz, der erkennt, ob der „ch“-Abfrageparameter gleich *`eml`*. Wenn er *`eml`* nicht enthält, ist er ein Affiliate.

**Frage**: Verweisende Domänen enthalten mehr Daten als erwartet.

* Verweisende Domänen sind in der Liste der Verarbeitungsregeln möglicherweise zu hoch. Es sollte sich um einen der letzten (oder letzten) Regelsätze handeln, da die Verarbeitungsreihenfolge wichtig ist.

**Frage**: Ich habe eine Regel erstellt, die mit einem Abfrage-String-Parameter übereinstimmt und nicht funktioniert.

* Stellen Sie sicher, dass der Parametername in den Parameterfeldern für die Abfrage (normalerweise ein alphanumerischer Wert) angegeben ist. Achten Sie außerdem darauf, dass der Parameterwert nach dem Operator angegeben wird, wie im folgenden Beispiel einer E-Mail-Regel dargestellt.

   ![](assets/example_email.png)

**Frage**: Warum wird mein gesamter Last Touch-Traffic einer internen Domäne zugeordnet?

* Sie haben eine Regel, die dem internen Traffic entspricht. Denken Sie daran, dass diese Regeln für jeden Treffer auf Ihrer Site verarbeitet werden, nicht nur beim Erstbesuch. Wenn Sie eine Regel wie  *`Page URL exists`* ohne weitere Kriterien verwenden, wird bei jedem nachfolgenden Treffer auf Ihrer Site eine Übereinstimmung mit dem betreffenden Kanal erfasst, da die Seiten-URL immer vorhanden ist.

**Frage**: Wie behebe ich Traffic-Fehler, der im Bericht unter Kein Kanal identifiziert angezeigt wird?

* Regeln werden in der richtigen Reihenfolge verarbeitet. Wenn keine bestimmten Kriterien erfüllt sind, fallen Treffer in eine von drei Kategorien:

1. Kein Verweis (ein Direktbesuch).

2. Interner Verweis, auf der ersten Seite des Besuchs.

3. Ein Verarbeitungsfehler auf der Seite.

Achten Sie darauf, dass Sie einen Kanal für diese drei Möglichkeiten haben. Erstellen Sie beispielsweise Regeln, die Folgendes angeben:

1. **[!UICONTROL Referrer]** und **[!UICONTROL Does Not Exist]** und **[!UICONTROL Is First Page of Visit]**. (Siehe [Direct.](/help/components/c-marketing-channels/c-faq.md))

2. **[!UICONTROL Referrer Matches Internal URL Filters]** und **[!UICONTROL Is First page of Visit]**. (Siehe [Internal](/help/components/c-marketing-channels/c-faq.md).)

3. **[!UICONTROL Referrer]** und **[!UICONTROL Exists]** und **[!UICONTROL Referrer Does Not Match Internal URL Filters]**.

Erstellen Sie abschließend einen Kanal *Other*, der die verbleibenden Treffer erfasst, wie in [Kein Kanal identifiziert](/help/components/c-marketing-channels/c-faq.md#no-channel-identified) beschrieben.

## Kein Kanal identifiziert  {#no-channel-identified}

When your rules do not capture data, or if rules are not configured correctly, the report displays the data in the [!UICONTROL No Channel Identified] row on the report. Sie können beispielsweise am Ende Ihrer Verarbeitungsreihenfolge einen Regelsatz mit dem Namen *Sonstige* erstellen, der auch internen Traffic identifiziert.

![](assets/example_other.png)

This kind of rule serves as a catch-all to ensure that channel traffic always matches external traffic, and typically does not end up in **[!UICONTROL No Channel Identified]**. Achten Sie darauf, keine Regel zu erstellen, die auch internen Traffic erkennt. Setting the channel&#39;s value to **[!UICONTROL Referring Domain]** or to **[!UICONTROL Page URL]** are the most common, useful ways to create an effective Other rule.

>[!NOTE] Es kann dennoch vorkommen, dass Kanal-Traffic teilweise in die Kategorie „Kein Kanal identifiziert“ fällt. Beispiel: Ein Besucher besucht die Site und markiert eine Seite mit Lesezeichen, und bei demselben Besuch wird die Seite über das Lesezeichen zurückgegeben. Da dies nicht die erste Seite des Besuchs ist, wird sie weder im direkten Kanal noch im anderen Kanal angezeigt, da keine verweisende Domäne vorhanden ist.

## Gebührenpflichtige Suche {#paid-search}

Eine gebührenpflichtige Suche ist ein Begriff oder eine Wortgruppe, die auf Bezahlung von der Suchmaschine in die Suchergebnisse gesetzt wird. Um die gebührenpflichtigen Sucherkennungsregeln einzuhalten, verwendet der Marketing-Kanal die auf der [!UICONTROL Paid Search Detection] Seite konfigurierten Einstellungen. ( **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Paid Search Detection]**). Die Ziel-URL stimmt mit der vorhandenen gebührenpflichtigen Sucherkennungsregel für diese Suchmaschine überein.

Für die Marketing Kanal-Regel gelten die [!UICONTROL Paid Search] folgenden Einstellungen:

![](assets/example_paid_search.png)

Weitere Informationen finden Sie unter [Gebührenpflichtige Sucherkennung](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) in Admin.

## Kostenlose Suche  {#natural-search}

Eine kostenlose Suche findet statt, wenn Besucher Ihre Website über eine Websuche finden, bei der die Suchmaschine Ihre Site aufführt, ohne dass Sie dafür Gebühren entrichten müssen. Sie können die Ziel-URL steuern, mit der die Suchmaschine eine Verknüpfung zu Ihrer Site herstellt. Mit dieser URL kann Analytics ermitteln, ob eine Suche kostenlos ist.

Es gibt keine Erkennung kostenloser Suchen in Analytics. Das System erkennt nach Einrichtung der gebührenpflichtigen Sucherkennung kostenlose Suchverweise durch Schlussfolgerung, wenn der Verweis nicht aus der gebührenpflichtigen Suche entstand. Bei einer kostenlosen Suche stimmt die Ziel-URL nicht mit der vorhandenen gebührenpflichtigen Sucherkennungsregel für diese Suchmaschine überein.

Für die Regel &quot;Marketing Kanal&quot;gelten die folgenden Einstellungen für die kostenlose Suche:

![](assets/example_natural_search.png)

Weitere Informationen finden Sie unter [Gebührenpflichtige Sucherkennung](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) in der Admin-Datei.

## Affiliates  {#afilliates}

Eine Affiliate-Regel identifiziert Besucher, die aus einem bestimmten Satz verweisender Domänen stammen. In der Regel werden die Domänen von Affiliates, die Sie verfolgen möchten, wie folgt Liste:

![](assets/example_affiliates.png)

## Sozialen Netzwerke  {#social-networks}

Diese Regel identifiziert Besucher, die aus sozialen Netzwerken wie Facebook* stammen. Folgende Einstellungen sind möglich:

![](assets/example_social.png)

## Anzeigen  {#display}

Diese Regel identifiziert Besucher, die von Banner-Werbung zu Ihnen gelangten. Sie wird durch einen Abfragezeichenfolgenparameter in der Ziel-URL bestimmt, in diesem Fall  *`Ad_01`*.

![](assets/example_display.png)

## Intern {#internal}

Diese Regel identifiziert Besucher, die über eine verweisende Stelle kamen, die mit den internen URL-Filtern der Report Suite übereinstimmt.

![](assets/example_internal.png)

## E-Mail  {#email}

Geben Sie zur Regeleinrichtung den Abfragezeichenfolgenparameter für Ihre E-Mail-Kampagne ein. In diesem Beispiel lautet der Parameter  *`eml`*:

![](assets/example_email.png)

Wenn Ihre Regel Rück-Trackingcodes enthält, geben Sie wie nachfolgend beschrieben einen Wert pro Zeile ein:

![](assets/tracking_code.png)

## Direkt  {#direct}

Diese Regel identifiziert Besucher, die keine verweisende Domäne haben. Diese Regel umfasst Besucher, die direkt zu Ihrer Site gelangen, z. B. über einen Favoriten-Link oder durch Einfügen eines Links in den Browser.

![](assets/example_direct.png)

