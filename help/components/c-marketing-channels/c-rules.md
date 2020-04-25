---
title: Verarbeitungsregeln für Marketing-Kanäle
description: Die Marketingkanal-Verarbeitungsregeln bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt. Die Regeln verarbeiten jeden Treffer des Besuchers auf Ihrer Site. Wenn eine Regel die Kriterien des Kanals nicht erfüllt oder die Regeln nicht richtig konfiguriert sind, ordnet das System den Treffer unter „Kein Kanal identifiziert“ ein.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Verarbeitungsregeln für Marketing-Kanäle

Die Marketingkanal-Verarbeitungsregeln bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt. Die Regeln verarbeiten jeden Treffer des Besuchers auf Ihrer Site. Wenn eine Regel die Kriterien des Kanals nicht erfüllt oder die Regeln nicht richtig konfiguriert sind, ordnet das System den Treffer unter „Kein Kanal identifiziert“ ein.

Beachten Sie bei der Regelerstellung diese wichtigen Richtlinien:

* Sortieren Sie die Regeln in der Reihenfolge, in der sie verarbeitet werden sollen.
* Setzen Sie an das Ende Ihrer Liste eine Sammelregel wie „Sonstige“. Diese Regel identifiziert externen Traffic, jedoch nicht den internen Traffic.

   Siehe [Kein Kanal identifiziert.](/help/components/c-marketing-channels/c-faq.md)

>[!NOTE] Auch wenn diese Regeln keine Auswirkungen auf die Berichterstellung außerhalb der Marketing-Kanäle haben, beeinflussen sie die Marketing-Kanal-Datenerfassung. Mit diesen Regeln erfasste Daten sind zu 100 % dauerhaft und nach der Datenerfassung geänderte Regeln sind nicht rückwirkend. Es wird dringend empfohlen, alle Umstände zu prüfen und in Erwägung zu ziehen, bevor [!UICONTROL Marketingkanal-Verarbeitungsregeln] gespeichert werden, um zu verhindern, dass Daten in falschen Kanälen erfasst werden.

## Voraussetzungen

* Überprüfen Sie die Konzeptinformationen unter [Erste Schritte mit Marketing-Kanälen](/help/components/c-marketing-channels/c-getting-started-mchannel.md).
* Erstellen Sie einen oder mehr Kanäle, um Regeln zuweisen zu können. See [Add marketing channels.](/help/components/c-marketing-channels/c-channels.md)

## Einrichten von Marketingkanal-Verarbeitungsregeln

Richten Sie Marketingkanal-Verarbeitungsregeln ein, die bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt.

Dieser Vorgang verwendet eine E-Mail-Regel als Beispiel. Es wird davon ausgegangen, dass Sie Ihrer Kanalliste auf der Seite „Marketingkanal-Manager“ einen E-Mail-Kanal hinzugefügt haben.

1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Wählen Sie eine Report Suite aus.

   Wenn in Ihrer Report Suite keine Kanäle definiert wurden, wird die Seite [!UICONTROL Marketingkanäle: Automatisches Setup] angezeigt.

   Siehe [Ausführen des automatischen Setups](/help/components/c-marketing-channels/c-getting-started-mchannel.md).

1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Marketingkanäle]** > **[!UICONTROL Marketingkanal-Verarbeitungsregeln]**.

   ![Schritt Ergebnis](assets/marketing_channel_rules.png)

1. Wählen Sie im Menü **[!UICONTROL Neuen Regelsatz hinzufügen:]** die Option **[!UICONTROL E-Mail]**.

   Hier wählen Sie keinen Kanal sondern eine Vorlage aus, die die Regel mit einigen der erforderlichen Parameter füllt.

   ![Schritt Ergebnis](assets/example_email.png)

   Verwenden Sie zur Regelkonfiguration die Boolesche Logik (if/then (wenn/dann) Aussagen). In einer E-Mail-Kanalregel geben Sie z. B. die Einstellungen oder Informationen ein, die in der folgenden Regelaussage hervorgehoben sind:

   `"If **[!UICONTROL All]** or **[!UICONTROL Any]** of the following are true:  **[!UICONTROL Query String Parameter]** *<value>* **[!UICONTROL exists]**...`

   `"Then identify the channel as **[!UICONTROL Email]**...`

   `"Then set the channel's value to **[!UICONTROL Query String Parameter]** *<value>*."`

   In diesem Beispiel ist *`<value>`* der Abfragezeichenfolgenparameter, den Sie für Ihre E-Mail-Kampagne verwenden, wie z. B. *`eml`*.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]**, um die Regelerstellung fortzusetzen.
1. Ziehen Sie die Regeln zur Priorisierung an die gewünschte Position.
1. Klicken Sie auf **[!UICONTROL Speichern.]**

>[!MORELIKETHIS]
>
>* [Häufig gestellte Fragen und Beispiele](/help/components/c-marketing-channels/c-faq.md)


## Regelkriterien für Marketing-Kanal

Diese Referenztabelle definiert die Trefferattribute, die Sie auf der Seite „Marketingkanalregeln“ auswählen können.

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

## Kanal „Intern“ (Sitzungsaktualisierung)

Der Kanal „Intern“ (häufig in „Sitzungsaktualisierung“ umbenannt) besteht aus Besuchen auf der Site, bei denen die verweisende URL mit der Einrichtung von internen URL-Filtern in der Admin Console übereinstimmt. Das bedeutet, dass der Besucher seinen Besuch innerhalb der Site gestartet hat.

![](assets/int-channel1.png)

### Überschreiben von Best Practices

Es empfiehlt sich, die Option zum Außerkraftsetzen des Letztkontakts für die Kanäle „Direkt“ und „Intern“ zu deaktivieren, damit sie keine Gutschriften von anderen persistenten Letztkontakt-Kanälen (oder voneinander) erhalten.

>[!NOTE]In diesem Dokument wird davon ausgegangen, dass die Einstellungen zum Außerkraftsetzen für Direkt- und Sitzungsaktualisierung deaktiviert sind.

![](assets/int-channel2.png)

### Interaktionszeitraum

Sowohl die Erstkontakt- als auch die Letztkontakt-Kanäle eines Besuchers werden nach 30 Tagen Inaktivität in diesem Browser zurückgesetzt.

>[!NOTE] 30 Tage sind die Standardeinstellung, die bei Bedarf über die Admin-Einstellungen geändert werden kann.

Wenn der Besucher die Site häufig nutzt, passt sich das Interaktionsfenster daran an. Der Besucher muss 30 Tage lang inaktiv sein, damit der Zeitraum abläuft und die Kanäle zurückgesetzt werden.
Beispiel:

* Tag 1: Der Benutzer gelangt per Anzeige zur Site. Erstkontakt- und Letztkontakt-Kanäle werden auf „Anzeige“ eingestellt.

* Tag 2: Der Benutzer gelangt per natürlicher Suche zur Site. Erstkontakt bleibt „Anzeige“, Letztkontakt wird auf „Natürliche Suche“ eingestellt.

* Tag 35: Der Benutzer war seit 33 Tagen nicht mehr auf der Site und kehrt über die Registerkarte zurück, die er in seinem Browser geöffnet hatte. Bei einem Interaktionsfenster von 30 Tagen wäre das Fenster geschlossen, und die Marketingkanal-Cookies wären abgelaufen. Die Erstkontakt- und Letztkontakt-Kanäle werden zurückgesetzt und auf „Sitzungsaktualisierung“ eingestellt, da der Benutzer von einer internen URL kam.

### Beziehung zwischen Erstkontakt und Letztkontakt

Um die Interaktion zwischen Erstkontakt und Letztkontakt zu verstehen und zu bestätigen, dass Außerkraftsetzungen erwartungsgemäß funktionieren, können Sie einen Erstkontakt-Kanalbericht abrufen, der sich auf einen Letztkontakt-Kanalbericht bezieht, wobei Ihre wichtigste Erfolgsmetrik hinzugefügt wird (siehe Beispiel unten). Das Beispiel zeigt die Interaktion zwischen Erstkontakt- und Letztkontakt-Kanälen.

![](assets/int-channel3.png)

Die Schnittmenge, bei der Erstkontakt mit Letztkontakt übereinstimmt, ist orange hervorgehoben. Sowohl „Direkt“ als auch „Sitzungsaktualisierung“ erhalten nur dann eine Letztkontakt-Gutschrift, wenn sie auch der Erstkontakt-Kanal sind, da sie keine Gutschrift von anderen persistenten Kanälen erhalten können (grau hervorgehobene Zeilen).

### Warum kommt es zu einer Sitzungsaktualisierung?

Da wir wissen, dass eine Letztkontakt-Sitzungsaktualisierung nur erfolgen kann, wenn es sich gleichzeitig um den Erstkontakt handelt, wird in den Szenarien unten erläutert, wie die Sitzungsaktualisierung ein Erstkontakt-Kanal sein kann.

**Szenario 1: Sitzungstimeout**

Ein Besucher ruft die Website auf und lässt die Registerkarte dann in seinem Browser geöffnet, um sie später erneut zu verwenden. Der Interaktionszeitraum des Besuchers läuft ab (oder er löscht seine Cookies freiwillig), und er verwendet die geöffnete Registerkarte, um die Website erneut zu besuchen. Da die verweisende URL eine interne Domäne ist, wird der Besuch als Sitzungsaktualisierung klassifiziert.

**Szenario 2: Nicht alle Seiten der Site sind mit Tags versehen**

Ein Besucher landet auf Seite A, die nicht mit Tags versehen ist, und wechselt dann zu Seite B, die mit Tags versehen ist. Seite A wird als interner Referrer angesehen, und der Besuch wird als Sitzungsaktualisierung klassifiziert.

**Szenario 3: Umleitungen**

Wenn eine Umleitung nicht so eingerichtet ist, dass Referrer-Daten an die neue Landingpage weitergegeben werden, gehen die Referrer-Daten verloren, und die Umleitungsseite (wahrscheinlich eine interne Seite) erscheint als Referrer-Domäne. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

**Szenario 4: Domänenübergreifender Traffic**

Ein Besucher wechselt von einer Domäne, die zu Suite A führt, zu einer zweiten Domäne, die zu Suite B führt wird. Wenn in Suite B die internen URL-Filter die erste Domäne enthalten, wird der Besuch in Suite B als intern aufgezeichnet, da Marketingkanäle ihn als neuen Besuch in der zweiten Suite sehen. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

**Szenario 5: Lange Ladezeiten der Entrypage**

Ein Besucher landet auf Seite A mit viel Inhalt, und der Adobe Analytics-Code befindet sich unten auf der Seite. Bevor der gesamte Inhalt (einschließlich Adobe Analytics-Bildanforderungen) geladen werden kann, klickt der Besucher auf Seite B. Seite B löst ihre Adobe Analytics-Bildanforderung aus. Da die Bildanforderung von Seite A nie geladen wurde, wird die zweite Seite als erster Treffer des Besuchs in Adobe Analytics angezeigt, wobei Seite A als Referrer dient. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

**Szenario 6: Löschen von Cookies mitten auf der Site**

Ein Besucher besucht die Site und löscht seine Cookies während der Sitzung. Die Erstkontakt- und Letztkontakt-Kanäle werden zurückgesetzt, und der Besuch wird als Sitzungsaktualisierung klassifiziert (weil der Referrer intern ist).
