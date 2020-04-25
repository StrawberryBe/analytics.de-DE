---
description: Erfahren Sie mehr über Best Practices und Beispiele, wie Sie die verschiedenen Regeln füllen, die Sie ggf. für Ihre Marketingkanäle einrichten.
title: Häufig gestellte Fragen und Beispiele zu Marketing-Kanälen
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Häufig gestellte Fragen und Beispiele zu Marketing-Kanälen

Unter [Einrichten von Marketing-Kanal-Verarbeitungsregeln](/help/components/c-marketing-channels/c-rules.md) finden Sie eine Definition der angezeigten Felder auf der Seite der [!UICONTROL Verarbeitungsregeln des Marketing-Kanals].

## Häufig gestellte Fragen {#faq}

Die Implementierungen der Marketingkanal-Verarbeitungsregeln unterscheiden sich je nach verwendetem Trackingcode. Die Konfiguration der Regeln, die die gewünschten Ergebnisse erzielen, will gut durchdacht sein, um Probleme zu vermeiden.

**Frage**: Meine Trackingcodes sind alle verschieden, und für meinen Affiliates-Kanal muss ich Tausende dieser Codes angeben.

* Sortieren Sie aus, was Sie nicht brauchen. Wenn Ihre E-Mail- und Affiliates-Kanäle denselben Abfragezeichenfolgenparameter verwenden, aber nur wenig E-Mail-Trackingcodes vorliegen, können Sie die E-Mail-Trackingcodes in einem Regelsatz zu „email“ angeben. Klassifizieren Sie dann alle weiteren Trackingcodes als  *`affiliates.`*
* Fügen Sie allen Landingpage-URLs in Ihrem E-Mail-System einen Abfragezeichenfolgenparameter hinzu, z. B. *`&ch=eml`*. Erstellen Sie einen Regelsatz, der erkennt, ob der „ch“-Abfrageparameter gleich *`eml`*. Wenn er *`eml`* nicht enthält, ist er ein Affiliate.

**Frage**: Verweisende Domänen enthalten mehr Daten als erwartet.

* Verweisende Domänen stehen in der Liste der Verarbeitungsregeln eventuell zu weit oben. Da die Verarbeitungsreihenfolge wichtig ist, sollte dies einer der letzten bzw. der letzte Regelsatz sein.

**Frage**: Ich habe eine Regel erstellt, die mit einem Abfragezeichenfolgenparameter übereinstimmt aber nicht funktioniert.

* Vergewissern Sie sich, dass der Parametername in den Feldern des Abfragenzeichenfolgenparameters angegeben ist (gewöhnlich ein alphanummerischer Wert). Vergewissern Sie sich zudem, dass der Parameterwert nach dem Operator steht, wie in folgendem Beispiel einer E-Mail-Regel dargestellt.

   ![](assets/example_email.png)

**Frage**: Warum wird der gesamte Last Touch-Traffic einer internen Domäne zugeschrieben?

* Sie verwenden eine Regel, die internem Traffic entspricht. Denken Sie daran, dass diese Regeln für jeden Treffer auf Ihrer Site verarbeitet werden, nicht nur beim Erstbesuch. Wenn Sie eine Regel wie  *`Page URL exists`* ohne weitere Kriterien verwenden, wird bei jedem nachfolgenden Treffer auf Ihrer Site eine Übereinstimmung mit dem betreffenden Kanal erfasst, da die Seiten-URL immer vorhanden ist.

**Frage**: Wie behebe ich Traffic-Fehler, die im Bericht als „Kein Kanal identifiziert“ auftreten?

* Regeln werden der Reihe nach verarbeitet. Wenn keine Übereinstimmung mit den spezifischen Kriterien vorliegt, fallen die Treffer in eine von drei Kategorien:

1. Kein Verweis (ein Direktbesuch).

2. Interner Verweis, auf der ersten Seite des Besuchs.

3. Ein Verarbeitungsfehler auf der Seite.

Stellen Sie sicher, dass Sie einen Kanal für diese drei Möglichkeiten haben. Erstellen Sie beispielsweise diese Regeln:

1. **[!UICONTROL Verweisende Stelle]** und **[!UICONTROL Nicht vorhanden]** und **[!UICONTROL Ist erste Seite des Besuchs]**. (Siehe [Direct.](/help/components/c-marketing-channels/c-faq.md))

2. **[!UICONTROL Referrer entspricht internen URL-Filtern]** und **[!UICONTROL Ist erste Seite des Besuchs]**. (Siehe [Internal](/help/components/c-marketing-channels/c-faq.md).)

3. **[!UICONTROL Verweisende Domäne]** und **[!UICONTROL Vorhanden]** und **[!UICONTROL Verweis stimmt nicht mit internen URL-Filtern überein]**.

Erstellen Sie abschließend einen Kanal *Other*, der die verbleibenden Treffer erfasst, wie in [Kein Kanal identifiziert](/help/components/c-marketing-channels/c-faq.md#no-channel-identified) beschrieben.

## Kein Kanal identifiziert  {#no-channel-identified}

Wenn Ihre Regeln keine Daten erfassen oder die Regeln nicht korrekt konfiguriert sind, zeigt der Bericht die Daten in der Zeile [!UICONTROL Kein Kanal identifiziert] im Bericht an. Sie können beispielsweise am Ende der Verarbeitungsreihenfolge einen Regelsatz mit dem Namen *Sonstige* einrichten, der internen Traffic auch wie folgt identifiziert:

![](assets/example_other.png)

Diese Art von Regel dient als Auffangbehälter, um zu gewährleisten, dass Kanal-Traffic stets externem Traffic entspricht und in der Regel nicht **[!UICONTROL Kein Kanal identifiziert zugeordnet wird]**. Achten Sie darauf, keine Regel zu erstellen, die auch internen Traffic erkennt. Zur Erstellung einer wirksamen Regel „Sonstige“ ist es häufig am sinnvollsten, den Kanalwert auf **[!UICONTROL Verweisende Domäne]** oder **[!UICONTROL Seiten-URL]** zu setzen.

>[!NOTE] Es kann dennoch vorkommen, dass Kanal-Traffic teilweise in die Kategorie „Kein Kanal identifiziert“ fällt. Beispiel: Ein Besucher öffnet die Site und versieht eine Seite mit einem Lesezeichen. Beim gleichen Besuch kehrt dieser Besucher über das Lesezeichen zur Seite zurück. Da es sich dabei nicht um die erste Seite des Besuchs handelt, wird es weder dem direkten Kanal noch einem anderen Kanal zugeordnet, da keine Referrer-Domäne vorliegt.

## Gebührenpflichtige Suche {#paid-search}

Eine gebührenpflichtige Suche ist ein Begriff oder eine Wortgruppe, die auf Bezahlung von der Suchmaschine in die Suchergebnisse gesetzt wird. Zum Erfüllen der Erkennungsregeln der bezahlten Suche verwendet der Marketingkanal die auf der Seite [!UICONTROL Gebührenpflichtige Sucherkennung] konfigurierten Einstellungen. (**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Gebührenpflichtige Sucherkennung]**). Die Ziel-URL stimmt mit der vorhandenen gebührenpflichtigen Sucherkennungsregel für die betreffende Suchmaschine überein.

Die [!UICONTROL gebührenpflichtigen Sucheinstellungen] für die Marketingkanalregel lauten wie folgt:

![](assets/example_paid_search.png)

Weitere Informationen finden Sie unter [Gebührenpflichtige Sucherkennung](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) in „Admin“.

## Kostenlose Suche  {#natural-search}

Eine Suche ist „kostenlos“, wenn Besucher Ihre Website durch eine Websuche finden, bei der die Suchmaschine Ihre Website aufführt, ohne dass Sie dafür Gebühren entrichten müssen. Sie können die von der Suchmaschine für die Verlinkung zu Ihrer Website verwendete Ziel-URL steuern. Diese URL ermöglicht Analytics die Bestimmung, ob eine Suche kostenlos ist.

Es gibt keine Erkennung kostenloser Suchen in Analytics. Das System erkennt nach Einrichtung der gebührenpflichtigen Sucherkennung kostenlose Suchverweise durch Schlussfolgerung, wenn der Verweis nicht aus der gebührenpflichtigen Suche entstand. Bei der kostenlosen Suche stimmt die Ziel-URL nicht mit der vorhandenen gebührenpflichtigen Sucherkennungsregel für die betreffende Suchmaschine überein.

Die kostenlosen Sucheinstellungen für die Marketingkanalregel lauten wie folgt:

![](assets/example_natural_search.png)

Weitere Informationen finden Sie unter [Gebührenpflichtige Sucherkennung](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) in „Admin“.

## Affiliates  {#afilliates}

Eine Affiliate-Regel identifiziert Besucher, die aus einem bestimmten Satz verweisender Domänen stammen. Listen Sie in der Regel die Affiliate-Domänen, die verfolgt werden sollen, so auf:

![](assets/example_affiliates.png)

## Sozialen Netzwerke  {#social-networks}

Diese Regel identifiziert Besucher, die aus sozialen Netzwerken wie Facebook* stammen. Die Einstellungen können wie folgt lauten:

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

Diese Regel identifiziert Besucher, die keine verweisende Domäne haben. Dazu zählen Besucher, die direkt zu Ihrer Site gelangten, z. B. über einen Favoriten-Link oder durch Kopieren des Links in den Browser.

![](assets/example_direct.png)

