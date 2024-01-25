---
title: Verarbeitungsregeln für Marketing-Kanäle
description: Die Marketingkanal-Verarbeitungsregeln bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt. Die Regeln verarbeiten jeden Treffer des Besuchers auf Ihrer Site. Wenn eine Regel die Kriterien des Kanals nicht erfüllt oder die Regeln nicht richtig konfiguriert sind, ordnet das System den Treffer unter „Kein Kanal identifiziert“ ein.
feature: Marketing Channels
exl-id: 825f70a5-cce3-4b1c-bb42-828388348216
role: Admin
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '1884'
ht-degree: 67%

---

# Verarbeitungsregeln für Marketing-Kanäle

Die Verarbeitungsregeln für Marketing-Kanäle bestimmen, ob der Besucherzugriff die einem Kanal zugewiesenen Kriterien erfüllt, indem jeder Treffer eines Besuchers auf Ihrer Site verarbeitet wird. Die Regeln werden in der angegebenen Reihenfolge verarbeitet. Wenn eine Regel erfüllt ist, stoppt das System die Verarbeitung der verbleibenden Regeln.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Marketing-Kanäle]** > **[!UICONTROL Marketing-Kanal-Verarbeitungsregeln]**.

![](assets/buckets_2.png)

Weitere Hinweise zur Verarbeitung:

* Mit diesen Regeln erfasste Daten sind dauerhaft. Nach der Datenerfassung geänderte Regeln sind nicht rückwirkend. Adobe empfiehlt dringend, dass Sie alle Umstände vor dem Speichern überprüfen und berücksichtigen [!UICONTROL Marketingkanal-Verarbeitungsregeln] um zu verhindern, dass Daten in falschen Kanälen erfasst werden.
* Sie können bis zu 25 separate Marketing-Kanäle konfigurieren.
* Regeln haben Zugriff auf Variablen, die von VISTA gesetzt wurden, können jedoch nicht auf Daten zugreifen, die von VISTA gelöscht wurden.
* Dasselbe Ereignis kann niemals zwei Marketingkanälen gutgeschrieben werden (wie Käufe oder Klicks). In dieser Hinsicht unterscheiden sich Marketingkanäle von eVars (dasselbe Ereignis kann zwei eVars gutgeschrieben werden).
* Wenn die Abdeckung Ihrer Regeln lückenhaft ist, sehen Sie möglicherweise [Kein Kanal erkannt](/help/components/c-marketing-channels/c-faq.md).

## Voraussetzungen

* Sehen Sie sich die Konzeptinformationen unter [Erste Schritte mit Marketing-Kanälen](/help/components/c-marketing-channels/c-getting-started-mchannel.md) an.
* Erstellen Sie einen oder mehr Kanäle, um Regeln zuweisen zu können. Siehe [Hinzufügen von Marketingkanälen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md).
* Best Practices für die Verwendung von [!UICONTROL Marketingkanäle] mit [!UICONTROL Attribution].

## Einrichten von Marketingkanal-Verarbeitungsregeln

Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
2. Wählen Sie eine Report Suite aus.

   Wenn in Ihrer Report Suite keine Kanäle definiert wurden, wird die Seite [!UICONTROL Marketingkanäle: Automatisches Setup] angezeigt.

   Siehe [Ausführen des automatischen Setups](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

3. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Marketing-Kanäle]** > **[!UICONTROL Marketingkanal-Verarbeitungsregeln]**. Wenn Sie das automatische Setup ausgeführt haben, wurde automatisch ein Kanal- und Regelsatz definiert.

   ![Ergebnis des Schritts](assets/marketing_channel_rules.png)

4. Wenn Sie eine Regel hinzufügen möchten, wählen Sie aus der **[!UICONTROL Neuen Regelsatz hinzufügen]** Menü. Wenn Sie einen Kanal auswählen, erhalten Sie eine Regelvorlage. Wenn Sie „Benutzerdefiniert“ auswählen, fangen Sie mit einer komplett leeren Vorlage an. Bei beiden Optionen können Sie den Regelsatz nach Bedarf ändern.

   ![Ergebnis des Schritts](assets/example_email.png)

5. Klicken Sie auf **[!UICONTROL Neuen Regelsatz hinzufügen]**, um die Regelerstellung fortzusetzen.
6. Ziehen Sie die Regeln zur Priorisierung an die gewünschte Position.
7. Klicken Sie auf **[!UICONTROL Speichern]**.

### Festlegen des Marketing-Kanalwerts

**[!UICONTROL Den Kanalwert festlegen]** definiert die Dimension Marketing-Kanaldetail , die für diesen Kanal verfügbar ist.

### Regelkriterien

Diese Referenztabelle definiert die Trefferattribute, die Sie zum Festlegen von Verarbeitungsregeln für Marketing-Kanäle verwenden können.

>[!NOTE]
>
>Jedes von Ihnen definierte Textfeld, z. B. Abfragezeichenfolgenparameter oder Listen mit Werten, die abgeglichen werden sollen, wird als **nicht von Schreibweise abhängig** -Werte. Wenn Sie beispielsweise eine Regel haben, bei der der Abfragezeichenfolgenparameter `cmp = abc123`, alle Varianten in Großbuchstaben und Kleinbuchstaben `cmp` und `abc123` übereinstimmen.

| Begriff | Definition |
|--- |--- |
| Alle | Aktiviert diesen Kanal nur, wenn alle Kriterien in der Regel wahr sind. |
| Eines | Aktiviert diesen Kanal, wenn eines der Kriterien in der Regel wahr ist. Diese Option ist nur verfügbar, wenn die Regel mehr als ein Kriterium enthält. |
| AMO-ID | Der primäre Trackingcode, der von den Advertising Cloud- und Advertising Analytics-Integrationen verwendet wird. Wenn eine dieser Integrationen aktiviert ist, kann das Trackingcode-Präfix verwendet werden, um Advertising Cloud-spezifische Kanäle zu identifizieren. Die Verwendung von „AMO-ID“ beginnt mit „AL“ für die Suche, „AC“ für die Anzeige oder „AO“ für Social. Wenn die AMO-ID in Marketing-Kanälen verwendet wird, können die Klick-/Kosten-/Impressionsmetriken dem richtigen Kanal zugeordnet werden (wenn diese nicht konfiguriert sind, gehen diese Metriken zu &quot;Direkt&quot;oder &quot;Keine&quot;). |
| AMO-EF-ID | Der von Advertising Cloud verwendete sekundäre Trackingcode. Der Hauptzweck dieses Trackingcodes besteht darin, als Schlüssel zum Zurücksenden von Daten an Ad Cloud zu dienen. Sie kann jedoch auch zur Identifizierung von Anzeige-Clickthroughs oder Anzeige-Viewthroughs verwendet werden, wenn Sie diese als zwei separate Marketing-Kanäle betrachten möchten. Dies kann durch Festlegen der Marketing-Kanal-Logik für &quot;AMO EF ID&quot;erreicht werden, die mit `:d` für Anzeige-Clickthroughs oder &quot;AMO EF ID&quot;endet mit `:i` für Display ViewThroughs. Wenn Sie die Anzeige nicht in zwei Kanäle aufteilen möchten, verwenden Sie stattdessen die „AMO-ID“-Dimension. |
| Konversionsvariablen | Setzt sich aus eVars zusammen, die für diese Report Suite aktiviert wurden, und gilt nur, wenn diese Variablen über den Adobe-Code auf der Seite gesetzt wurden. |
| Vorhanden | Mehrere Auswahlmöglichkeiten sind verfügbar, einschließlich:<ul><li>**Nicht vorhanden**: Gibt an, dass das Trefferattribut nicht in der Anfrage vorhanden ist. Beispiel: Wenn der Benutzer in einer Referrer-Domäne eine URL eingibt oder auf ein Lesezeichen klickt, ist das Attribut für die Referrer-Domäne nicht vorhanden.</li><li>**Ist leer**: Gibt an, dass ein Trefferattribut vorhanden ist. In der Regel handelt es sich dabei um eine eVar oder einen Abfragezeichenfolgenparameter, doch dem Trefferattribut ist kein Wert zugeordnet.</li><li>**Enthält nicht**: Hiermit können Sie beispielsweise angeben, dass eine verweisende Domäne einen bestimmten Wert nicht enthält (im Gegensatz zur Auswahl von &quot;Enthält&quot;).</li></ul> |
| Den Kanal identifizieren als | Verbindet die Regel mit einem Marketingkanal, den Sie der Seite Marketingkanal-Manager hinzugefügt haben. |
| Stimmt mit Erkennungsregeln gebührenpflichtiger Suchvorgänge überein | Eine von Adobe erkannte, gebührenpflichtige Suche. Gebührenpflichtige Suchvorgänge treten ein, wenn Firmen Gebühren an die Suchmaschine zahlen, damit diese deren Site auflistet. Gebührenpflichtige Suchergebnisse tauchen gewöhnlich oben oder rechts von den Suchergebnissen auf. |
| Stimmt mit Erkennungsregeln kostenloser Suchvorgänge überein | Eine von Adobe erkannte, kostenlose Suche. |
| Verweisende Stelle stimmt mit internen URL-Filtern überein | Ein Besuch, dessen Seiten-URL laut der Definition für die Report Suite in „Admin Tools“ mit dem internen URL-Filter übereinstimmt. |
| Verweisende Stelle stimmt nicht mit internen URL-Filtern überein | Die verweisende URL stimmt laut Definition für die Report Suite in „Admin Tools“ nicht mit dem internen URL-Filter überein. Sie können diese Einstellung mit Seiten-URL und Existiert verwenden, um eine Sammelregel einzurichten, sodass keine Besuche im Berichtabschnitt Kein Kanal identifiziert landen. |
| Treffer ignorieren, die mit internen URL-Filtern übereinstimmen | (Für verweisende Stellen) Verfolgt nur Treffer, die von extern verweisenden Stellen stammen. Normalerweise wird diese Option nicht aktiviert, es sei denn, Sie möchten internen Traffic einbeziehen. |
| Ist erste Seite des Besuchs | Die erste Seite eines Besuchs, die in der Adobe Berichterstellung erkannt wurde. |
| Seite | Die Dimension [Seite](/help/components/dimensions/page.md). |
| Seitendomäne | Die Domain der Seite, auf der der Besucher landet, z. B. `products.example.com`. |
| Seitendomäne und Pfad | Die Domain und der Pfad, z. B. `products.example.com/mens/pants/overview.html`. |
| Stammdomäne der Seite (TLD+1) | Die Stammdomäne der Seite, auf der der Besucher landet, z. B. example.co.uk. |
| Seiten-URL | Die URL einer Webseite auf Ihrer Site. |
| Referrer-Domain | Die [Verweisende Domäne](/help/components/dimensions/referring-domain.md) Dimension |
| Abfragezeichenfolgenparameter | Verwenden Sie einen einzelnen Abfragezeichenfolgenparameter. Pro Kriterium können Sie nur einen Abfragezeichenfolgenparameter angeben. Verwenden Sie zum Hinzufügen zusätzlicher Abfragezeichenfolgenparameter `ANY` als Ihren Operator, und fügen Sie dann Abfragezeichenfolgenparameter zur Regel hinzu. |
| Referrer | Die Webseite (volle URL), auf der sich Besucher befanden, bevor sie zu Ihrer Site kamen. Die verweisende Stelle befindet sich außerhalb Ihrer definierten Domain. |
| Verweisende Domain und Pfad | Eine Verkettung aus verweisender Domain und URL-Pfad. Beispiele sind: `www.example.com/products/id/12345` oder `ad.example.com/foo` |
| Verweisender Parameter | Abfragezeichenfolgenparameter der verweisenden URL. Wenn Ihre Besucher z. B. von `example.com/?page=12345&cat=1` kommen, sind „page“ und „cat“ die verweisenden Parameter. |
| Verweisende Stammdomäne | Die Stammdomäne der verweisenden Stelle. Die verweisende Stelle befindet sich außerhalb Ihrer definierten Domain. |
| Suchmaschine | Eine Suchmaschine wie Google oder Yahoo!, über die Besucher zu Ihrer Site gelangten. |
| Suchkeywords | Ein Wort, mit dem in einer Suchmaschine gesucht wird. |
| Suchmaschine + Keywords | Eine Verkettung aus Keyword und Suchmaschine, um die Suchmaschine eindeutig zu kennzeichnen. Wenn Sie beispielsweise nach dem Begriff &quot;computer&quot;suchen, werden die Suchmaschine und der Suchbegriff wie folgt identifiziert: `Search Tracking Code = "<search_type>:<search engine>:<search keyword>" where    search_type = "n" or "p", search_engine = "Google", and search_keyword = "computer"`**Hinweis:** n = kostenlos; p = bezahlt |
| Den Kanalwert setzen auf | Legt die [Marketingkanaldetails](/help/components/dimensions/marketing-detail.md) Dimension. Sie bestimmen, welcher Wert im Kontext der Regel am besten ist. Beispiele sind Banneranzeigen-ID, Suchbegriff oder E-Mail-Kampagne. |

## Reihenfolge der Regeln und Definitionen für Marketing-Kanäle {#channel-rules}

Kanalregeln werden in der angegebenen Reihenfolge verarbeitet. Adobe empfiehlt, dass Sie gebührenpflichtige oder verwaltete Kanäle zuerst platzieren (z. B. gebührenpflichtige Suche, kostenlose Suche, Anzeige oder E-Mail), damit sie Guthaben über organische Kanäle (z. B. direkte, interne, verweisende Domänen) erhalten.

Nachfolgend finden Sie die empfohlene Reihenfolge für Kanalregeln und Beispieldefinitionen:

### Paid Search {#paid-search}

Paid Search ist ein Begriff oder eine Wortgruppe, die auf Bezahlung von der Suchmaschine in die Suchergebnisse gesetzt wird. Dieser Kanal wird in der Regel basierend auf Abfragezeichenfolgenparametern (siehe Beispiel für einen Anzeigenkanal) oder Erkennungsregeln für Paid Search definiert.

#### Paid-Search-Erkennung

Zum Erfüllen der Erkennungsregeln von Paid Search verwendet der Marketing-Kanal die auf der Seite [!UICONTROL Gebührenpflichtige Sucherkennung] konfigurierten Einstellungen. (**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Gebührenpflichtige Sucherkennung]**). Die Ziel-URL stimmt mit der vorhandenen gebührenpflichtigen Sucherkennungsregel für die betreffende Suchmaschine überein.

Die [!UICONTROL gebührenpflichtigen Sucheinstellungen] für die Marketingkanalregel lauten wie folgt:

![](assets/example_paid_search.png)

Siehe [Erkennung von Paid Search](../general/paid-search-detection/paid-search-detection.md) für weitere Informationen.

### Kostenlose Suche  {#natural-search}

Eine kostenlose Suche ist der Fall, wenn Besucher Ihre Website über eine Suchmaschine finden und die Suchmaschine Ihre Site in einer Rangfolge aufführt, ohne dass Sie für die Auflistung bezahlen müssen.

Adobe ermittelt den Suchtraffic basierend auf einer internen Suche nach Suchmaschinen. Wenn eine verweisende Stelle Kriterien für eine Suchmaschine erfüllt, bestimmt sie anhand von [Erkennung von Paid Search](../general/paid-search-detection/paid-search-detection.md) Regeln, die Sie konfiguriert haben. Ein Treffer gilt als kostenlose Suche, wenn er mit keiner der gebührenpflichtigen Sucherkennungsregeln übereinstimmt.

Die kostenlosen Sucheinstellungen für die Marketing-Kanalregel lauten wie folgt:

![](assets/example_natural_search.png)

### Anzeigen {#display}

Diese Regel identifiziert Besucher, die von Banner-Werbung zu Ihnen gelangten. Sie wird durch einen Abfragezeichenfolgenparameter in der Ziel-URL identifiziert, in diesem Fall *`Ad_01`*. Der Parameter der Abfragezeichenfolge und die gesuchten Werte werden ohne Unterscheidung der Groß-/Kleinschreibung ausgewertet.

![](assets/example_display.png)

### E-Mail {#email}

Diese Regel identifiziert Besucher, die von E-Mail-Kampagnen zu Ihnen gelangten. Sie wird durch einen Abfragezeichenfolgenparameter in der Ziel-URL bestimmt, in diesem Fall *`eml`*:

![](assets/example_email.png)

### Affiliates {#afilliates}

Diese Regel identifiziert Besucher, die aus einem bestimmten Satz von Referrer-Domänen stammen. Führen Sie in der Regel die Affiliate-Domänen, die verfolgt werden sollen, so auf:

![](assets/example_affiliates.png)

### Andere Kampagnen {#other-campaigns}

Eine Best Practice besteht darin, einen Kanal „Andere Kampagnen“ einzubeziehen, der allen Regeln für gebührenpflichtige Kanäle entspricht. Dieser Kanal dient als Sammelstelle für nicht kategorisierten gebührenpflichtigen Traffic.

![](assets/other-campaigns.png)

### Soziale Netzwerke  {#social-networks}

Diese Regel identifiziert Besucher, die aus einem sozialen Netzwerk wie Facebook stammen. Der Kanal wird oft in „Organic Social“ umbenannt. Die Einstellungen können wie folgt lauten:

![](assets/example_social.png)

### Kanal „Intern“ (Sitzungsaktualisierung) {#internal}

Diese Regel gilt für Besucher, bei denen die Referrer-URL mit den in der Admin Console eingerichteten internen URL-Filtern übereinstimmt, d. h. der Besucher kam von innerhalb der Site, um seinen Besuch zu beginnen. Der Kanal wird oft in „Sitzungsaktualisierung“ umbenannt.

![](assets/int-channel1.png)

Weitere Informationen zum Auftreten dieses Kanals finden Sie unter [Gründe für „Intern“ (Sitzungsaktualisierung)](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-faq.html?lang=de#internal).

### Direkt {#direct}

Diese Regel identifiziert Besucher, die über keine Referrer-Domäne verfügen. Dazu zählen Besucher, die direkt zu Ihrer Site gelangten, z. B. über einen Favoriten-Link oder durch Kopieren des Links in den Browser. Dieser Kanal wird oft in „Direkte Eingabe/Lesezeichen“ umbenannt.

![](assets/example_direct.png)

### Kanal „Referrer Domains“  {#referring-domains}

Der Kanal „Referrer-Domänen“ identifiziert Besucher mit einer Referrer-Domäne. Gemeinsam fungieren die Kanäle „Intern“, „Direkt“ und „Referrer-Domänen“ als Sammelstelle für alle verbleibenden Treffer, die noch nicht in einen Kanal kategorisiert wurden.

![](assets/referring-domains.png)
