---
title: Verarbeitungsregeln für Marketing-Kanäle
description: Die Marketingkanal-Verarbeitungsregeln bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt. Die Regeln verarbeiten jeden Treffer des Besuchers auf Ihrer Site. Wenn eine Regel die Kriterien des Kanals nicht erfüllt oder die Regeln nicht richtig konfiguriert sind, ordnet das System den Treffer unter „Kein Kanal identifiziert“ ein.
translation-type: tm+mt
source-git-commit: acdaebf3c96d7cf1f0e5fed4a459968a83c89fbd
workflow-type: tm+mt
source-wordcount: '2048'
ht-degree: 71%

---


# Verarbeitungsregeln für Marketing-Kanäle

Die Verarbeitungsregeln des Marketing-Kanals bestimmen, ob ein Treffer des Besuchers die einem Kanal zugewiesenen Kriterien erfüllt, indem jeder Treffer verarbeitet wird, den ein Besucher auf Ihrer Site ausführt. Die Regeln werden in der von Ihnen angegebenen Reihenfolge verarbeitet. Wenn eine Regel erfüllt ist, stoppt das System die Verarbeitung der verbleibenden Regeln.

![](assets/buckets_2.png)

Weitere Hinweise zur Verarbeitung:
* Mit diesen Regeln erfasste Daten sind zu 100 % dauerhaft und nach der Datenerfassung geänderte Regeln sind nicht rückwirkend. Es wird dringend empfohlen, alle Umstände zu prüfen und in Erwägung zu ziehen, bevor [!UICONTROL Marketingkanal-Verarbeitungsregeln] gespeichert werden, um zu verhindern, dass Daten in falschen Kanälen erfasst werden.
* Der Bericht kann bis zu 25 Kanäle gleichzeitig verarbeiten.
* Regeln haben Zugriff auf Variablen, die von VISTA gesetzt wurden, können jedoch nicht auf Daten zugreifen, die von VISTA gelöscht wurden.
* Dasselbe Ereignis kann niemals zwei Marketingkanälen gutgeschrieben werden (wie Käufe oder Klicks). In dieser Hinsicht unterscheiden sich Marketingkanäle von eVars (dasselbe Ereignis kann zwei eVars gutgeschrieben werden).
* Wenn Ihre Regeln lückenhaft abgedeckt sind, sehen Sie möglicherweise [Kein Kanal identifiziert.](/help/components/c-marketing-channels/c-faq.md)

## Voraussetzungen

* Überprüfen Sie die Konzeptinformationen unter [Erste Schritte mit Marketing-Kanälen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
* Erstellen Sie einen oder mehr Kanäle, um Regeln zuweisen zu können. See [Add marketing channels.](/help/components/c-marketing-channels/c-channels.md)

## Einrichten von Marketingkanal-Verarbeitungsregeln

Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.

Dieser Vorgang verwendet eine E-Mail-Regel als Beispiel. Es wird davon ausgegangen, dass Sie Ihrer Kanalliste auf der Seite „Marketingkanal-Manager“ einen E-Mail-Kanal hinzugefügt haben.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
2. Wählen Sie eine Report Suite aus.

   Wenn in Ihrer Report Suite keine Kanäle definiert wurden, wird die Seite [!UICONTROL Marketingkanäle: Automatisches Setup] angezeigt.

   Siehe [Ausführen des automatischen Setups](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

3. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Marketingkanäle]** > **[!UICONTROL Marketingkanal-Verarbeitungsregeln]**.

   ![Schritt Ergebnis](assets/marketing_channel_rules.png)

4. Wählen Sie im Menü **[!UICONTROL Neuen Regelsatz hinzufügen:]** die Option **[!UICONTROL E-Mail]**.

   Hier wählen Sie keinen Kanal sondern eine Vorlage aus, die die Regel mit einigen der erforderlichen Parameter füllt. Sie können diese Vorlage nach Bedarf ändern.

   ![Schritt Ergebnis](assets/example_email.png)

5. Klicken Sie auf **[!UICONTROL Regel hinzufügen]**, um die Regelerstellung fortzusetzen.
6. Ziehen Sie die Regeln zur Priorisierung an die gewünschte Position.
7. Klicken Sie auf **[!UICONTROL Speichern.]**

Fahren Sie auf dieser Seite fort, um Empfehlungen für die Regelreihenfolge von Kanälen sowie weitere Definitionsbeispiele anzuzeigen.

### Festlegen des Kanal-Werts für Marketing

**[!UICONTROL Hinzufügen ]**RegelLegt den Wert des Kanals fest]**definiert die Detail-Dimension des Marketing-Kanals, die für diesen Kanal verfügbar ist. Auf diese Weise können Sie die Dimensionen des Marketing-Kanals unterteilen und detailliertere Informationen zum Kanal anzeigen.

Es wird empfohlen, den Kanal-Wert auf dieselben Kriterien festzulegen, die zur Definition des Kanals selbst verwendet werden. Wenn beispielsweise der Zeichenfolgenparameter &quot;Abfrage&quot;zum Definieren des Kanals verwendet wird, legen Sie den Abfrage-Zeichenfolgenparameter auch als Kanal-Wert fest.

### Regelkriterien

In dieser Referenztabelle werden die Felder, Optionen und Trefferattribute definiert, die Sie zum Definieren der Verarbeitungsregeln für Marketing Kanal verwenden können.

| Begriff | Definition |
|--- |--- |
| Alle | Aktiviert diesen Kanal nur, wenn alle Regeln in der nummerierten Regel „true“ sind. |
| Alle | Aktiviert diesen Kanal, wenn eine der Regeln im Regelsatz „true“ ist. Diese Option steht nur zur Verfügung, wenn mehr als eine Regel in der nummerierten Regel vorhanden ist. |
| AMO-ID | Der primäre Trackingcode, der von den Advertising Cloud- und Advertising Analytics-Integrationen verwendet wird. Wenn eine dieser Integrationen aktiviert ist, kann das Trackingcode-Präfix verwendet werden, um Advertising Cloud-spezifische Kanäle zu identifizieren. Die Verwendung von „AMO-ID“ beginnt mit „AL“ für die Suche, „AC“ für die Anzeige oder „AO“ für Social. Wenn die AMO-ID in Marketing-Kanälen verwendet wird, können die Klick-/Kosten-/Impressionsmetriken dem richtigen Kanal zugeordnet werden (wenn diese nicht konfiguriert sind, gehen diese Metriken zu „Direkt“ oder „Keine“). |
| AMO-EF-ID | Der von Advertising Cloud verwendete sekundäre Trackingcode. Der Hauptzweck dieses Trackingcodes besteht darin, als Schlüssel zum Zurücksenden von Daten an Ad Cloud zu dienen. Sie kann jedoch auch zur Identifizierung von Anzeige-Clickthrough oder Anzeige-Viewthroughs verwendet werden, wenn Sie diese als zwei separate Marketing-Kanäle betrachten möchten. Dazu können Sie die Marketing-Kanal-Logik so festlegen, dass „AMO EF ID“ für Anzeige-Clickthroughs auf „:d“ oder „AMO EF ID“ für Anzeige-Viewthroughs auf „:i“ endet. Wenn Sie die Anzeige nicht in zwei Kanäle aufteilen möchten, verwenden Sie stattdessen die „AMO-ID“-Dimension. |
| Konversionsvariablen | Setzt sich aus eVars zusammen, die für diese Report Suite aktiviert wurden, und gilt nur, wenn diese Variablen über den Adobe-Code auf der Seite gesetzt wurden.  Siehe Implementierungshandbuch . |
| Vorhanden | Mehrere Auswahlmöglichkeiten sind verfügbar, einschließlich:<ul><li>**Nicht vorhanden**: Gibt an, dass das Trefferattribut nicht in der Anfrage vorhanden ist. Beispiel: Wenn der Benutzer in einer verweisenden Domäne eine URL eingibt oder auf ein Lesezeichen klickt, ist das Attribut für die verweisende Domäne nicht vorhanden.</li><li>**Ist leer**: Gibt an, dass ein Trefferattribut vorhanden ist. In der Regel handelt es sich dabei um eine eVar oder einen Abfragezeichenfolgenparameter, doch dem Trefferattribut ist kein Wert zugeordnet.</li><li>**Enthält nicht**: Hiermit können Sie beispielsweise angeben, dass eine verweisende Domäne einen bestimmten Wert nicht enthält (anders als bei Auswahl von &quot;Enthält&quot;.)</li></ul> |
| Den Kanal identifizieren als | Verbindet die Regel mit dem Marketingkanal, den Sie der Seite Marketingkanal-Manager hinzugefügt haben.  Weitere Informationen finden Sie unter Hinzufügen von Marketing-Kanälen. |
| Stimmt mit Erkennungsregeln gebührenpflichtiger Suchvorgänge überein | Eine von Adobe erkannte, gebührenpflichtige Suche. Gebührenpflichtige Suchvorgänge treten ein, wenn Firmen Gebühren an die Suchmaschine zahlen, damit diese deren Site auflistet. Gebührenpflichtige Suchergebnisse tauchen gewöhnlich oben oder rechts von den Suchergebnissen auf. |
| Stimmt mit Erkennungsregeln kostenloser Suchvorgänge überein | Eine von Adobe erkannte, kostenlose Suche. |
| Verweisende Stelle stimmt mit internen URL-Filtern überein | Ein Besuch, dessen Seiten-URL laut der Definition für die Report Suite in „Admin Tools“ mit dem internen URL-Filter übereinstimmt. |
| Verweisende Stelle stimmt nicht mit internen URL-Filtern überein | Die verweisende URL stimmt laut Definition für die Report Suite in „Admin Tools“ nicht mit dem internen URL-Filter überein. Sie können diese Einstellung mit   Seiten-URL und Existiert einsetzen, um eine Sammelregel zu erstellen, sodass keine Besuche im Berichtabschnitt Kein Kanal identifiziert landen. |
| Treffer ignorieren, die mit internen URL-Filtern übereinstimmen | (Für verweisende Stellen) Verfolgt nur Treffer, die von extern verweisenden Stellen stammen. Normalerweise wird diese Option nicht aktiviert, es sei denn, Sie möchten internen Traffic einbeziehen. |
| Ist erste Seite des Besuchs | Die erste Seite eines Besuchs, die in der Adobe Berichterstellung erkannt wurde. |
| Seite | Der Seitenname einer Web-Seite auf Ihrer Site, die unter Verwendung des Adobe Webbeacons mit Tags versehen wurde. Dieser Wert entspricht  s.pageName . Examples include `Home Page` and `About Us`. |
| Seitendomäne | Die Domäne der Seite, auf der der Besucher landet, z. B. `products.example.co.uk`. |
| Seitendomäne und Pfad | The domain and path, such as `products.example.co.uk/mens/pants/overview.html` . |
| Stammdomäne der Seite (TLD+1) | Die Stammdomäne der Seite, auf der der Besucher landet, z. B. example.co.uk . |
| „Seiten-URL“ | Die URL einer Webseite auf Ihrer Site. |
| Verweisende Domäne | Die Domäne, von der Ihre Besucher kamen, als sie Ihre Site aufriefen; verweisende Stellen können z. B. `abcsite.com` oder `xyzsite.com` sein. |
| Abfragezeichenfolgenparameter | If a page URL on your site looks like `https://example.com/?page=12345&cat=1`, then page and cat are both query string parameters. (Siehe `https://en.wikipedia.org/wiki/Query_string`.)  Sie können pro Regelsatz nur einen Abfragezeichenfolgenparameter angeben. To add additional query string parameters, use `ANY` as your operator, then add new query string parameters to the rule. |
| Verweisende Stelle | Die Webseite (volle URL), auf der sich Besucher befanden, bevor sie zu Ihrer Site kamen. Die verweisende Stelle befindet sich außerhalb Ihrer definierten Domäne. |
| Verweisende Domäne und Pfad | Eine Verkettung aus verweisender Domäne und URL-Pfad. Beispiele:    `www.example.com/products/id/12345` oder `ad.example.com/foo` |
| Verweisender Parameter | Abfragezeichenfolgenparameter der verweisenden URL. Wenn Ihre Besucher z. B. von `example.com/?page=12345&cat=1` kommen, sind „page“ und „cat“ die verweisenden Parameter. |
| Verweisende Stammdomäne | Die Stammdomäne der verweisenden Stelle. Die verweisende Stelle befindet sich außerhalb Ihrer definierten Domäne. |
| Suchmaschine | Eine Suchmaschine wie Google oder Yahoo!, über die Besucher zu Ihrer Site gelangten. |
| Suchkeywords | Ein Wort, mit dem in einer Suchmaschine gesucht wird. |
| Suchmaschine + Keywords | Eine Verkettung aus Keyword und Suchmaschine, um die Suchmaschine eindeutig zu kennzeichnen. Wenn Sie z. B. nach dem Begriff „computer“ suchen, werden die Suchmaschine und Keyword wie folgt identifiziert: `Search Tracking Code = "<search_type>:<search engine>:<search keyword>" where    search_type = "n" or "p", search_engine = "Google", and search_keyword = "computer"`**Hinweis:**„n“ = kostenlos; „p“ = gebührenpflichtig |
| Den Kanalwert setzen auf | Neben der Erkenntnis, welche Marketing-Kanäle einen Besucher zu Ihrer Site führen, ist es auch von Interesse, welche Bannerwerbung, welches Keyword und welche E-Mail-Kampagne in dem Kanal die Gutschrift für die Site-Aktivität des Besuchers erhält. Diese ID ist ein Kanalwert, der mit dem Kanal gespeichert wird. Häufig handelt es sich dabei um eine Kampagnen-ID, die in die Landingpage oder die verweisende URL integriert ist. In anderen Fällen ist es eine Kombination aus Suchmaschine und Keyword oder die verweisende URL, die den Besucher aus einem bestimmten Kanal am genauesten identifiziert. |

## Regelreihenfolge und Definitionen für Marketing Kanal {#channel-rules}

Kanal-Regeln werden in der angegebenen Reihenfolge verarbeitet. Eine empfohlene Vorgehensweise bei der Bestellung von Kanälen besteht darin, gebührenpflichtige oder verwaltete Kanal zuerst zu bestellen (z.B. gebührenpflichtige Suche, kostenlose Suche, Anzeige, E-Mail), sodass sie eine Gutschrift erhalten, gefolgt von kostenlosen Kanälen (z.B. direkt, intern, verweisende Domänen).

Nachfolgend finden Sie die empfohlene Reihenfolge für Kanal-Regeln und Beispieldefinitionen:

### Gebührenpflichtige Suche {#paid-search}

Die gebührenpflichtige Suche ist ein Wort oder eine Wortgruppe, mit der Sie eine Suchmaschine für die Platzierung in Suchergebnissen bezahlen. Dieser Kanal wird in der Regel auf der Grundlage von Abfragen-Zeichenfolgenparametern (siehe Beispiel Kanal anzeigen) oder gebührenpflichtigen Sucherkennungsregeln definiert. Die Entscheidung hängt von den Details des Marketing-Kanals ab, den Sie aufzeichnen möchten.

#### Erkennung von Paid Search

Zum Erfüllen der Erkennungsregeln der bezahlten Suche verwendet der Marketingkanal die auf der Seite [!UICONTROL Gebührenpflichtige Sucherkennung] konfigurierten Einstellungen. (**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Gebührenpflichtige Sucherkennung]**). Die Ziel-URL stimmt mit der vorhandenen gebührenpflichtigen Sucherkennungsregel für die betreffende Suchmaschine überein.

Die [!UICONTROL gebührenpflichtigen Sucheinstellungen] für die Marketingkanalregel lauten wie folgt:

![](assets/example_paid_search.png)

Weitere Informationen finden Sie unter [Gebührenpflichtige Sucherkennung](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) in „Admin“.

### Kostenlose Suche  {#natural-search}

Eine Suche ist „kostenlos“, wenn Besucher Ihre Website durch eine Websuche finden, bei der die Suchmaschine Ihre Website aufführt, ohne dass Sie dafür Gebühren entrichten müssen.

Es gibt keine Erkennung kostenloser Suchen in Analytics. Das System erkennt nach Einrichtung der gebührenpflichtigen Sucherkennung kostenlose Suchverweise durch Schlussfolgerung, wenn der Verweis nicht aus der gebührenpflichtigen Suche entstand. Weitere Informationen finden Sie unter [Gebührenpflichtige Sucherkennung](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) in „Admin“.

Die kostenlosen Sucheinstellungen für die Marketingkanalregel lauten wie folgt:

![](assets/example_natural_search.png)

### Anzeigen  {#display}

Diese Regel identifiziert Besucher, die von Banner-Werbung zu Ihnen gelangten. Sie wird durch einen Abfragezeichenfolgenparameter in der Ziel-URL bestimmt, in diesem Fall  *`Ad_01`*.

![](assets/example_display.png)

### E-Mail  {#email}

Diese Regel identifiziert Besucher, die von E-Mail-Kampagnen stammen. Sie wird durch einen Abfragezeichenfolgenparameter in der Ziel-URL bestimmt, in diesem Fall *`eml`*:

![](assets/example_email.png)

### Affiliates  {#afilliates}

Diese Regel identifiziert Besucher, die aus einem bestimmten Satz verweisender Domänen stammen. Listen Sie in der Regel die Affiliate-Domänen, die verfolgt werden sollen, so auf:

![](assets/example_affiliates.png)

### Andere Kampagnen {#other-campaigns}

Eine bewährte Methode besteht darin, einen Kanal &quot;Sonstige Kampagnen&quot;einzubeziehen, der allen Regeln für gebührenpflichtige Kanal entspricht. Dieser Kanal dient als Auffangbehälter für nicht kategorisierten gebührenpflichtigen Traffic.

### Sozialen Netzwerke  {#social-networks}

Diese Regel identifiziert Besucher, die aus sozialen Netzwerken wie Facebook* stammen. Der Kanal wird oft in &quot;Organisch Social&quot;umbenannt. Die Einstellungen können wie folgt lauten:

![](assets/example_social.png)

### Kanal „Intern“ (Sitzungsaktualisierung){#internal}

Diese Regel gilt für Besucher, in denen die verweisende URL mit der URL-Adresse übereinstimmt, die in der Admin-Konsole eingerichtet wurde. Das bedeutet, dass der Besucher von der Site kam, um seinen Besuch Beginn. Dieser Kanal wird oft in &quot;Sitzungsaktualisierung&quot;umbenannt.

![](assets/int-channel1.png)

Weitere Informationen dazu, warum dieser Kanal auftritt, finden Sie unter [Gründe für die Aktualisierung der Sitzung](https://docs.adobe.com/content/help/en/analytics/components/marketing-channels/c-faq.html) .

### Direkt  {#direct}

Diese Regel identifiziert Besucher ohne Referrerdomäne. Dazu gehören Besucher, die direkt zu Ihrer Site gelangen, z. B. über einen Favoritenlink oder durch Einfügen eines Links in den Browser. Dieser Kanal wird oft in &quot;Direkte Eingabe/Lesezeichen&quot;umbenannt.

![](assets/example_direct.png)

### Kanal &quot;Verweisende Domänen&quot; {#referring-domains}

Der Kanal &quot;Verweisende Domänen&quot;identifiziert Besucher mit einer verweisenden Domäne. Die Kanal &quot;Interne&quot;, &quot;Direkte&quot;und &quot;Verweisende Domänen&quot;fungieren gemeinsam als Auffanglösung für alle verbleibenden Treffer, die noch nicht in einen Kanal kategorisiert wurden.

