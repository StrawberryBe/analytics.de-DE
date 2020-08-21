---
description: Tabellendaten, die die Spalten im Daten-Feed beschreiben.
keywords: Data Feed;columns
subtopic: data feeds
title: Datenspaltenreferenz
topic: Reports and analytics
uuid: 9042a274-7124-4323-8cd6-5c84ab3eef6d
translation-type: tm+mt
source-git-commit: ca9b77ebf8104a1937d87aba5021e2deeccd6f8b
workflow-type: tm+mt
source-wordcount: '3674'
ht-degree: 98%

---


# Datenspaltenreferenz

Auf dieser Seite erfahren Sie, welche Daten in den einzelnen Spalten enthalten sind. Bei den meisten Implementierungen wird nicht alle Spalten verwendet. Daher können Sie diese Seite konsultieren, wenn Sie entscheiden müssen, welche Spalten in einen Daten-Feed-Export einbezogen werden sollen.

>[!IMPORTANT]
>
>Für bestimmte Spalten (beispielsweise bei Definition als 255 Zeichen) kann ein Daten-Feed zusätzliche Zeichen senden, da Maskierungszeichenwerte in Zeichenfolgen hinzugefügt werden. Berücksichtigen Sie diese möglichen zusätzlichen Zeichen, wenn Ihre Implementierung regelmäßig Werte sendet, die die Zeichenbeschränkungen überschreiten.

## Spalten, Beschreibungen und Datentypen

>[!NOTE]
>
>Die meisten Spalten enthalten eine ähnliche Spalte mit dem Präfix `post_`. Post-Spalten enthalten Werte nach der serverseitigen Logik, den Verarbeitungsregeln und den VISTA-Regeln. Adobe empfiehlt in den meisten Fällen die Verwendung von Post-Spalten. Weitere Informationen finden Sie in den [häufig gestellten Fragen zu Daten-Feeds](../df-faq.md).

| Spaltenname | Spaltenbeschreibung | Datentyp |
| --- | --- | --- |
| `accept_language` | Führt alle unterstützten Sprachen, wie im HTTP-Header Accept-Language angegeben, in einer Bildanforderung auf. | char(20) |
| `aemassetid` | Eine mehrwertige Variable, die Asset-IDs (GUIDs) einer Reihe von Adobe Experience Manager Assets entspricht. Erhöht Impressionsereignisse. | text |
| `aemassetsource` | Identifiziert die Quelle des Asset-Ereignisses. Wird in Adobe Experience Manager verwendet. | varchar(255) |
| `aemclickedassetid` | Asset-ID eines Adobe Experience Manager-Assets. Erhöht Klickereignisse. | varchar(255) |
| `browser` | Numerische ID des Browsers. Verweist auf die Suchtabelle browser.tsv | int unsigniert |
| `browser_height` | Höhe des Browser-Fensters in Pixel. | smallint unsigniert |
| `browser_width` | Breite des Browser-Fensters in Pixel. | smallint unsigniert |
| `c_color` | Bit-Tiefe der Farbpalette. Wird im Rahmen der Berechnung der Dimension „Farbtiefe“ verwendet. Verwendet die JavaScript-Funktion screen.colorDepth() | char(20) |
| `campaign` | Variable, die in der Dimension „Trackingcode“ verwendet wird. | varchar(255) |
| `carrier` | Variable der Adobe Advertising Cloud-Integration. Gibt den Mobilnetzbetreiber an. Verweist auf die Suchtabelle des Mobilfunknetzbetreibers. | varchar(100) |
| `channel` | Variable, die in der Dimension „Sitebereiche“ verwendet wird. | varchar(100) |
| `click_action` | Wird nicht mehr verwendet. Adresse des Links, auf dem im veralteten ClickMap-Tool geklickt wurde. | varchar(100) |
| `click_action_type` | Wird nicht mehr verwendet. Link-Typ des veralteten ClickMap-Tools.<br>0: HREF-URL<br>1: Benutzerspezifische ID<br>2: JavaScript onClick-Ereignis<br>3: Formularelement | tinyint unsigniert |
| `click_context` | Wird nicht mehr verwendet. Name der Seite mit dem Link-Klick. Teil des veralteten ClickMap-Tools. | varchar(255) |
| `click_context_type` | Wird nicht mehr verwendet. Gibt an, ob es für click_context einen Seitennamen gibt oder standardmäßig die Seiten-URL gilt.<br>0: Seiten-URL<br>1: Seitenname | tinyint unsigniert |
| `click_sourceid` | Wird nicht mehr verwendet. Numerische ID der Linkposition auf der Seite. Teil des veralteten ClickMap-Tools. | int unsigniert |
| `click_tag` | Wird nicht mehr verwendet. HTML-Elementtyp, auf den geklickt wurde. | char(10) |
| `clickmaplink` | Activity Map-Link | varchar(255) |
| `clickmaplinkbyregion` | Activity Map-Link nach Region | varchar(255) |
| `clickmappage` | Activity Map-Seite | varchar(255) |
| `clickmapregion` | Activity Map-Region | varchar(255) |
| `code_ver` | Bibliotheksversion von AppMeasurement, die für das Kompilieren und Senden der Bildanforderung verwendet wird. | char(16) |
| `color` | Farbtiefen-ID basierend auf dem Wert der c_color-Spalte. Verweist auf die Suchtabelle color_depth.tsv | smallint unsigniert |
| `connection_type` | Numerische ID, die den Verbindungstyp darstellt. Die Variable, die in der Dimension „Verbindungstyp“ verwendet wurde. Verweist auf die Suchtabelle connection_type.tsv | tinyint unsigniert |
| `cookies` | Die Variable, die in der Dimension „Cookie-Unterstützung“ verwendet wurde.<br>Y: aktiviert<br>N: deaktiviert<br>U: unbekannt | char(1) |
| `country` | Numerische ID, die das Land angibt, aus dem der Treffer stammt. Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Ländern zuzuordnen. Verwendet die Suchtabelle country.tsv | smallint unsigniert |
| `ct_connect_type` | Bezieht sich auf die Spalte connection_type. Die häufigsten Werte sind LAN/WLAN, Mobilnetzbetreiber und Modem. | char(20) |
| `curr_factor` | Bestimmt die Dezimalstelle für die Währung und wird zur Währungsumrechnung verwendet. Für USD werden beispielsweise zwei Dezimalstellen verwendet, sodass der Spaltenwert 2 ist. | tinyint |
| `curr_rate` | Der Wechselkurs zum Zeitpunkt der Transaktion. Adobe arbeitet mit XE zusammen, um den aktuellen Wechselkurs zu bestimmen. | Dezimalzahl(24,12) |
| `currency` | Der während der Transaktion verwendete Währungscode. | char(8) |
| `cust_hit_time_gmt` | Nur für Report Suites mit aktiviertem Zeitstempel. Der mit dem Treffer gesendet Zeitstempel in Unix-Zeit. | int |
| `cust_visid` | Wurde eine benutzerdefinierte Besucher-ID festgelegt, wird sie in diese Spalte aufgenommen. | varchar(255) |
| `daily_visitor` | Flag zur Bestimmung, ob der Treffer ein neuer täglicher Besucher ist. | tinyint unsigniert |
| `date_time` | Die Uhrzeit des Treffers in lesbarem Format, basierend auf der Zeitzone der Report Suite. | datetime |
| `domain` | Variable, die in der Dimension „Domäne“ verwendet wurde. Basiert auf dem Internetdienstanbieter (ISP) des Benutzers. | varchar(100) |
| `duplicate_events` | Listet alle Ereignisse auf, die als Duplikat gezählt wurden. | varchar(255) |
| `duplicate_purchase` | Ein Flag, das anzeigt, dass das Kaufereignis für diesen Treffer ignoriert werden muss, da es ein Duplikat ist. | tinyint unsigniert |
| `duplicated_from` | Wird nur in Report Suites mit VISTA-Regeln zur Trefferkopie verwendet. Gibt an, von welcher Report Suite der Treffer kopiert wurde. | varchar(40) |
| `ef_id` | Die ef_id, die in Adobe Advertising Cloud-Integrationen verwendet wird. | varchar(255) |
| `evar1 - evar250` | Benutzerdefinierte Variablen 1–250. Jede Organisation verwendet eVars anders. Der beste Ort für weitere Informationen dazu, wie Ihre Organisation entsprechende eVars füllt, ist ein Dokument zum Lösungsentwurf, das für Ihre Organisation gilt. | varchar(255) |
| `event_list` | Kommagetrennte Liste numerischer IDs, die die durch den Treffer ausgelösten Ereignisse darstellen. Enthält sowohl die Standardereignisse als auch die benutzerdefinierten Ereignisse 1–1000. Verwendet die Suchtabelle event.tsv | text |
| `exclude_hit` | Ein Flag, das angibt, dass der Treffer nicht in die Berichterstellung einfließt. Die Spalte visit_num wird bei ausgeschlossenen Treffern nicht erhöht.<br>1: Nicht verwendet. Teil einer veralteten Funktion.<br>2: Nicht verwendet. Teil einer veralteten Funktion.<br>3: Wird nicht mehr verwendet. Benutzeragentenausschluss<br>4: Ausschluss basierend auf IP-Adresse<br>5: Wichtige Trefferinformationen fehlen, z. B. page_url, pagename, page_event oder event_list<br>6: JavaScript hat Treffer nicht korrekt verarbeitet<br>7: Kontospezifischer Ausschluss, z. B. in VISTA-Regeln<br>8: Nicht verwendet. Alternativer kontospezifischer Ausschluss.<br>9: Nicht verwendet. Teil einer veralteten Funktion.<br>10: Ungültiger Währungscode<br>11: Treffer, bei dem ein Zeitstempel für eine Report Suite mit Zeitstempel fehlt, oder ein Treffer, der einen Zeitstempel in einer Report Suite ohne Zeitstempel aufweist<br>12: Nicht verwendet. Teil einer veralteten Funktion.<br>13: Nicht verwendet. Teil einer veralteten Funktion.<br>14: Target-Treffer, der nicht mit einem Analytics-Treffer übereinstimmte<br>15: Derzeit nicht verwendet.<br>16: Advertising Cloud-Treffer, der nicht mit einem Analytics-Treffer übereinstimmte | tinyint unsigniert |
| `first_hit_page_url` | Die allererste URL des Besuchers. | varchar(255) |
| `first_hit_pagename` | Variable, die in der Dimension „Ursprüngliche Entrypage“ verwendet wird. Der Name der ursprünglichen Entrypage des Besuchers. | varchar(100) |
| `first_hit_ref_domain` | Variable, die in der Dimension „Ursprünglich verweisende Domäne“ verwendet wird. Basiert auf first_hit_referrer. Die allererste verweisende Domäne des Besuchers. | varchar(100) |
| `first_hit_ref_type` | Numerische ID des Typs der verweisenden Stelle der allerersten verweisenden Stelle des Besuchers. Verwendet die Suche referrer_type.tsv | tinyint unsigniert |
| `first_hit_referrer` | Die allererste verweisende URL des Besuchers. | varchar(255) |
| `first_hit_time_gmt` | Zeitstempel des allerersten Treffers des Besuchers in Unix-Zeit. | int |
| `geo_city` | Name der Stadt, aus der der Treffer stammt, basierend auf der IP. Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Städten zuzuordnen. | char(32) |
| `geo_country` | Abkürzung für das Land, aus dem der Treffer stammt, basierend auf der IP. Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Ländern zuzuordnen. | char(4) |
| `geo_dma` | Numerische ID des demografischen Bereichs, aus dem der Treffer stammt, basierend auf der IP. Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu demografischen Bereichen zuzuordnen. | int unsigniert |
| `geo_region` | Name des Bundeslands oder der Region, aus der der Treffer stammt, basierend auf der IP. Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Bundesländern bzw. Regionen zuzuordnen. | char(32) |
| `geo_zip` | Die Postleitzahl, von der der Treffer stammt, basierend auf der IP. Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Postleitzahlen zuzuordnen. | varchar(16) |
| `hier1 - hier5` | Wird von Hierarchievariablen verwendet. Enthält eine durch Trennzeichen getrennte Werteliste. Das in den Report Suite-Einstellungen gewählte Trennzeichen. | varchar(255) |
| `hit_source` | Gibt die Quelle an, aus der der Treffer stammt. Trefferquellen 1, 2 und 6 werden in Rechnung gestellt. <br>1: Standard-Bildanforderung ohne Zeitstempel <br>2: Standard-Bildanforderung mit Zeitstempel <br>3: Hochladen der Live-Datenquelle mit Zeitstempel <br>4: Nicht verwendet <br>5: Generischer Datenquellen-Upload <br>6: Datenquellen-Upload mit voller Verarbeitung <br>7: TransaktionsID-Datenquellenupload <br>8: nicht mehr verwendet; Frühere Versionen von Adobe Advertising Cloud-Datenquellen <br>9: nicht mehr verwendet; Metriken zur Adobe Social-Zusammenfassung <br>10: Serverseitige Weiterleitung des Audience Managers verwendet | tinyint unsigniert |
| `hit_time_gmt` | Der Zeitstempfel der Adobe-Datenerfassungsserver erhielt den Treffer, basierend auf der Unix-Zeit. | int |
| `hitid_high` | Wird zusammen mit hitid_low zur eindeutigen Identifizierung eines Treffers verwendet. | bigint unsigniert |
| `hitid_low` | Wird zusammen mit hitid_high zur eindeutigen Identifizierung eines Treffers verwendet. | bigint unsigniert |
| `homepage` | Wird nicht mehr verwendet. Wird angezeigt, wenn die aktuelle URL die Browser-Startseite ist. | char(1) |
| `hourly_visitor` | Flag zur Bestimmung, ob der Treffer ein neuer stündlicher Besucher ist. | tinyint unsigniert |
| `ip` | IP-Adresse basierend auf dem HTTP-Header der Bildanforderung. | char(20) |
| `ip2` | Nicht verwendet. Backend-Verweis-Variable für Report Suites mit VISTA-Regeln basierend auf IP-Adressen. | char(20) |
| `j_jscript` | Vom Browser unterstützte JavaScript-Version. | char(5) |
| `java_enabled` | Ein Flag, das angibt, ob Java aktiviert ist. <br>Y: Aktiviert <br>N: Deaktiviert <br>U: Unbekannt | char(1) |
| `javascript` | Such-ID der JavaScript-Version, basierend auf j_jscript. Verwendet eine Suchtabelle. | tinyint unsigniert |
| `language` | Numerische ID der Sprache. Verwendet die Suchtabelle languages.tsv | smallint unsigniert |
| `last_hit_time_gmt` | Zeitstempel (in Unix-Zeit) des vorherigen Treffers. Wird zur Berechnung der Dimension „Tage seit dem letzten Besuch“ verwendet. | int |
| `last_purchase_num` | Variable, die in der Dimension „Kundenloyalität“ verwendet wird. Gibt die Anzahl der vorherigen Käufe des Besuchers an. <br>0: Keine vorherigen Käufe (kein Kunde) <br>1: 1 vorheriger Kauf (neuer Kunde) <br>2: 2 vorherige Käufe (Bestandskunde) <br>3: 3 oder mehr vorherige Käufe (treuer Kunde) | int unsigniert |
| `last_purchase_time_gmt` | Variable, die in der Dimension „Tage seit letztem Kauf“ verwendet wird. Zeitstempel (in Unix-Zeit) des letzten Kaufs. Bei Erstkäufen und Besuchern, die zuvor noch nichts gekauft haben, ist dieser Wert 0. | int |
| `latlon1` | Standort (bis 10 km) | varchar(255) |
| `latlon23` | Standort (bis 100 m) | varchar(255) |
| `latlon45` | Standort (bis 1 m) | varchar(255) |
| `mc_audiences` | Liste der Audience Manager-Segment-IDs, zu denen der Besucher gehört. | text |
| `mcvisid` | Experience Cloud-Besucher-ID. 128-Bit-Zahl bestehend aus zwei verketteten 64-Bit-Zahlen verteilt auf 19 Ziffern. | varchar(255) |
| `mobile_id` | Die numerische Geräte-ID, wenn der Benutzer ein Mobilgerät verwendet. | int |
| `mobileaction` | Mobile Aktion. Wird automatisch erfasst, wenn trackAction in Mobile Services aufgerufen wird. Ermöglicht automatisches Action Pathing in der App. | varchar(100) |
| `mobileappid` | ID der mobilen App Speichert den Applikationsnamen und die Version im folgenden Format:[AppName] [BundleVersion] | varchar(255) |
| `mobileappperformanceappid` | Wird im Apteligent-Daten-Connector verwendet. Die in Apteligent verwendete App-ID. | varchar(255) |
| `mobileappperformancecrashid` | Wird im Apteligent-Daten-Connector verwendet. Die in Apteligent verwendete Absturz-ID. | varchar(255) |
| `mobileappstoreobjectid` | Wird im Appfigures-Daten-Connector verwendet. App Store-Objekt-ID | varchar(255) |
| `mobilebeaconmajor` | Mobile Services – Haupt-Beacon | varchar(100) |
| `mobilebeaconminor` | Mobile Services – Neben-Beacon | varchar(100) |
| `mobilebeaconproximity` | Mobile Services – Beacon-Nähe | varchar(255) |
| `mobilebeaconuuid` | Mobile Services-Beacon UUID | varchar(100) |
| `mobilecampaigncontent` | Der Name der ID des Inhalts, in dem der Link angezeigt wurde. Erfasst durch App-Akquise. | varchar(255) |
| `mobilecampaignmedium` | Marketingmedium, z. B. Banner oder E-Mail. Erfasst durch App-Akquise. | varchar(255) |
| `mobilecampaignname` | Name der Kampagne, ebenfalls gespeichert in der Kampagnenvariable. Erfasst durch App-Akquise. | varchar(255) |
| `mobilecampaignsource` | Ursprünglicher Referrer, wie z. B. Newsletter oder soziales Netzwerk. Erfasst durch App-Akquise. | varchar(255) |
| `mobilecampaignterm` | Bezahlte Keywords oder andere Begriffe, die Sie mit dieser Akquise verfolgen wollen. Erfasst durch App-Akquise. | varchar(255) |
| `mobiledayofweek` | Nummer des Wochentags, an dem die App gestartet wurde. | varchar(255) |
| `mobiledayssincefirstuse` | Anzahl der Tage, die seit dem ersten Ausführen der App vergangen sind. | varchar(255) |
| `mobiledayssincelastupgrade` | Wird mit der Kontextdatenvariablen a.DaysSinceLastUpgrade erfasst. Die Anzahl der Tage, die seit der vorherigen Sitzung vergangen sind. | varchar(255) |
| `mobiledayssincelastuse` | Anzahl der Tage, die vergangen sind, seitdem die App das letzte Mal ausgeführt wurde. | varchar(255) |
| `mobiledeeplinkid` | Wird mit der Kontextdatenvariablen a.<span>deeplink</span>.id erfasst. Wird in Akquise-Berichten als Identifikator für mobilen Akquise-Link verwendet. | varchar(255) |
| `mobiledevice` | Mobilgerätname. Unter iOS als kommagetrennte 2-Ziffern-Zeichenfolge gespeichert. Die erste Zahl gibt die Gerätegeneration an und die zweite die Gerätefamilie. | varchar(255) |
| `mobilehourofday` | Gibt die Stunde des Tages an, zu der die App gestartet wurde. Angaben im 24-Stunden-Format. | varchar(255) |
| `mobileinstalldate` | Installationsdatum der mobilen App. Stellt das Datum zur Verfügung, an dem ein Benutzer die Mobile App erstmalig geöffnet hat. | varchar(255) |
| `mobilelaunchessincelastupgrade` | Wird mit der Kontextdatenvariablen a.LaunchesSinceUpgrade erfasst. Gibt die Anzahl der Starts seit der letzten Aktualisierung an. | varchar(255) |
| `mobilelaunchnumber` | Wird immer dann erhöht, wenn die Mobile App gestartet wird. | varchar(255) |
| `mobileltv` | Wird nicht mehr verwendet. Erfasst durch trackLifetimeValue-Methoden. | varchar(255) |
| `mobilemessagebuttonname` | Wird mit der Kontextdatenvariablen a.<span>message</span>.button.id erfasst. Wird für In-App-Nachrichten verwendet, um die Schaltfläche zu identifizieren, mit der die Nachricht geschlossen wurde. | varchar(100) |
| `mobilemessageid` | In-App-Nachrichten-ID | varchar(255) |
| `mobilemessageonline` | In-App-Online-Nachricht | varchar(255) |
| `mobilemessagepushoptin` | Wird mit der Kontextdatenvariablen a.push.optin erfasst. Setzen Sie sie auf „true“, wenn sich der Benutzer für Push-Nachrichten anmeldet; andernfalls ist der Wert „false“. | varchar(255) |
| `mobilemessagepushpayloadid` | Wird mit der Kontextdatenvariablen a.push.payloadid erfasst. Wird in Push-Nachrichten als Payload-ID verwendet. | varchar(255) |
| `mobileosenvironment` | Wird mit der Kontextdatenvariablen a.OSEnvironment erfasst. Gibt das Betriebssystem an, z. B. Android oder iOS. | varchar(255) |
| `mobileosversion` | Betriebssystemversion der Mobile Services | varchar(255) |
| `mobileplaceaccuracy` | Erfasst mit der Kontextdatenvariablen a.loc.acc. Gibt die Genauigkeit des GPS in Metern zum Erfassungszeitpunkt an. | varchar(255) |
| `mobileplacecategory` | Wird mit der Kontextdatenvariablen a.loc.category erfasst. Beschreibt die Kategorie eines bestimmten Orts. | varchar(255) |
| `mobileplaceid` | Wird mit der Kontextdatenvariablen a.<span>loc</span>.id erfasst. Kennung für einen bestimmten Zielpunkt. | varchar(255) |
| `mobilerelaunchcampaigncontent` | Startinhalte für Mobile Services | varchar(255) |
| `mobilerelaunchcampaignmedium` | Startmedium für Mobile Services | varchar(255) |
| `mobilerelaunchcampaignsource` | Startquelle für Mobile Services | varchar(255) |
| `mobilerelaunchcampaignterm` | Startbedingung für Mobile Services | varchar(255) |
| `mobilerelaunchcampaigntrackingcode` | Wird mit der Kontextdatenvariablen a.launch.campaign.trackingcode erfasst. Wird bei der Akquise als Trackingcode für die Startkampagne verwendet. | varchar(255) |
| `mobileresolution` | Auflösung des Mobilgeräts. Breite x Höhe in Pixel. | varchar(255) |
| `monthly_visitor` | Flag, das angibt, dass der Benutzer im aktuellen Monat eindeutig ist. | tinyint unsigniert |
| `mvvar1` – `mvvar3` | Listenvariablenwerte. Enthält eine durch Trennzeichen getrennte Liste benutzerdefinierter Werte in Abhängigkeit von der Implementierung. | text |
| `namespace` | Nicht verwendet. Teil einer veralteten Funktion. | varchar(50) |
| `new_visit` | Ein Flag, das bestimmt, ob der aktuelle Treffer ein neuer Besuch ist. Wird von Adobe-Servern nach einer 30-minütigen Besuchsinaktivität festgelegt. | tinyint unsigniert |
| `os` | Numerische ID, die das Betriebssystem des Besuchers darstellt. Basiert auf der Spalte user_agent. Verwendet die os-Suche. | int unsigniert |
| `p_plugins` | Wird nicht mehr verwendet. Liste der für den Browser verfügbaren Plugins. Hat die JavaScript-Funktion navigator.plugins() verwendet | text |
| `page_event` | Die Art des Treffers, die in der Bildanforderung gesendet wird (Standardtreffer, Downloadlink, benutzerspezifischer Link, Exitlink). Siehe [Seitenereignissuche](datafeeds-page-event.md). | tinyint unsigniert |
| `page_event_var1` | Wird nur in Linktracking-Bildanforderungen verwendet. Die URL des angeklickten Downloadlinks, Exitlinks oder benutzerspezifischen Links. | text |
| `page_event_var2` | Wird nur in Linktracking-Bildanforderungen verwendet. Der benutzerdefinierte Name des Links, sofern angegeben. | varchar(100) |
| `page_event_var3` | Wird nicht mehr verwendet. Enthielt Umfrage- und Medienmoduldaten. Füllte verwaltete Videoberichte in vorherigen Versionen von Adobe Analytics. | text |
| `page_type` | Wird zum Füllen der Dimension „Seiten nicht gefunden“ verwendet; nur für 404-Seiten. Die Variable sollte entweder leer sein oder „ErrorPage“ enthalten. | char(20) |
| `page_url` | Die URL des Treffers. Wird nicht in Linktracking-Bildanforderungen verwendet. | varchar(255) |
| `pagename` | Wird zum Füllen der Dimension „Seiten“ verwendet. Wenn die Variable „pagename“ leer ist, verwendet Analytics stattdessen page_url. | varchar(100) |
| `paid_search` | Flag, das gesetzt wird, wenn der Treffer mit der gebührenpflichtigen Sucherkennung übereinstimmt. | tinyint unsigniert |
| `partner_plugins` | Nicht verwendet. Teil einer veralteten Funktion. | varchar(255) |
| `persistent_cookie` | Wird von der Dimension „Unterstützung beständiger Cookies“ verwendet. Gibt an, ob der Benutzer Cookies unterstützt, die nicht nach jedem Treffer gelöscht werden. | char(1) |
| `plugins` | Wird nicht mehr verwendet. Liste numerischer IDs, die den im Browser verfügbaren Plugins entsprechen. Verwendet die Suchtabelle plugins.tsv | varchar(180) |
| `pointofinterest` | Name des Mobile Services-Zielpunkts | varchar(255) |
| `pointofinterestdistance` | Entfernung der Mobile Services zur Zielpunktmitte | varchar(255) |
| `post_ columns` | Enthält den in diesen Berichten ultimativ verwendeten Wert. Jede Post-Spalte wird nach der serverseitigen Logik, den Verarbeitungsregeln und den VISTA-Regeln gefüllt. Adobe empfiehlt in den meisten Fällen die Verwendung von Post-Spalten. | Vgl. entsprechende non-post-Spalte |
| `prev_page` | Nicht verwendet. Proprietäre Adobe ID der vorherigen Spalte | int unsigniert |
| `product_list` | Produktliste, so wie sie von der Variable der Produkte übergeben wurde. Produkte sind durch Kommata voneinander getrennt und individuelle Produkteigenschaften durch Semikolons. | text |
| `product_merchandising` | Nicht verwendet. Verwenden Sie stattdessen product_list. | text |
| `prop1` – `prop75` | Benutzerdefinierte Traffic-Variablen 1 bis 75. | varchar(100) |
| `purchaseid` | Eindeutige ID für einen Kauf, so wie durch das Festlegen der Variable s_purchaseID bestimmt. Wird von der Spalte duplicate_purchase verwendet. | char(20) |
| `quarterly_visitor` | Flag zur Bestimmung, ob der Treffer ein neuer Quartals-Besucher ist. | tinyint unsigniert |
| `ref_domain` | Basiert auf der Referrer-Spalte. Die verweisende Domäne des Treffers. | varchar(100) |
| `ref_type` | Eine numerische ID, die den Typ des Verweises für den Treffer darstellt.<br>1: Auf Ihrer Site<br>2: Andere Websites <br>3: Suchmaschinen <br>4: Festplatte <br>5: USENET <br>6: Eingegeben/mit Lesezeichen versehen (kein Referrer) <br>7: E-Mail <br>8: Kein JavaScript <br>9: Soziale Netzwerke | tinyint unsigniert |
| `referrer` | Seiten-URL der vorherigen Seite. Beachten Sie, dass während `referrer` einen Datentyp von varchar(255) verwendet, `post_referrer` einen Datentyp von varchar(244) verwendet. | varchar(255) |
| `resolution` | Numerische ID, die die Auflösung des Bildschirms darstellt. Bestückt die Dimension „Bildschirmauflösung“. Verwendet die Suchtabelle resolution.tsv | smallint unsigniert |
| `s_kwcid` | Die Keyword-ID, die in Adobe Advertising Cloud-Integrationen verwendet wird. | varchar(255) |
| `s_resolution` | Rohwert der Bildschirmauflösung. Erfasst mit der JavaScript-Funktion screen.width x screen.height | char(20) |
| `sampled_hit` | Wird nicht mehr verwendet. Wurde zuvor für das Sampling in Ad Hoc Analysis verwendet. | char(1) |
| `search_engine` | Numerische ID, die die Suchmaschine darstellt, die den Besucher auf Ihre Site verwiesen hat. Verwendet die Suche search_engines.tsv | smallint unsigniert |
| `search_page_num` | Wird von der Dimension „Rangansicht aller Suchseiten“ verwendet. Gibt an, auf welcher Seite der Suchergebnisse Ihre Site angezeigt wurde, ehe der Benutzer sich zu Ihrer Site durchgeklickt hat. | smallint unsigniert |
| `secondary_hit` | Flag, das sekundäre Treffer verfolgt. Stammt ursprünglich vom Multi-Suite-Tagging und von VISTA-Regel, die Treffer kopieren. | tinyint unsigniert |
| `service` | Nicht verwendet. Verwenden Sie stattdessen page_event. | char(2) |
| `socialaccountandappids` | Wird nicht mehr verwendet. Social-Media-Konto und App-IDs | varchar(255) |
| `socialassettrackingcode` | Wird nicht mehr verwendet. Variable für Social-Media-Kampagnen | varchar(255) |
| `socialauthor` | Wird nicht mehr verwendet. Variable für Social-Media-Autoren | varchar(255) |
| `socialcontentprovider` | Wird nicht mehr verwendet. Soziale Plattformen/Eigenschaften | varchar(255) |
| `socialinteractiontype` | Wird nicht mehr verwendet. Art der sozialen Interaktion | varchar(255) |
| `sociallanguage` | Wird nicht mehr verwendet. Social-Media-Sprache | varchar(255) |
| `sociallatlong` | Wird nicht mehr verwendet. Social – Längen- und Breitengrad | varchar(255) |
| `socialowneddefinitioninsighttype` | Wird nicht mehr verwendet. Soziale eigene Definition Insight-Typ | varchar(255) |
| `socialowneddefinitioninsightvalue` | Wird nicht mehr verwendet. Soziale eigene Definition Insight-Wert | varchar(255) |
| `socialowneddefinitionmetric` | Wird nicht mehr verwendet. Soziale eigene Definition Metrik | varchar(255) |
| `socialowneddefinitionpropertyvspost` | Wird nicht mehr verwendet. Soziale eigene Definition Eigenschaft vs. Post | varchar(255) |
| `socialownedpostids` | Wird nicht mehr verwendet. Social – eigene Post-IDs | varchar(255) |
| `socialownedpropertyid` | Wird nicht mehr verwendet. Soziale eigene Eigenschafts-ID | varchar(255) |
| `socialownedpropertyname` | Wird nicht mehr verwendet. Sozialer eigener Eigenschaftsname | varchar(255) |
| `socialownedpropertypropertyvsapp` | Wird nicht mehr verwendet. Social – eigene Eigenschaft vs App | varchar(255) |
| `state` | Statusvariable. | varchar(50) |
| `stats_server` | Wird nicht verwendet. Interner Adobe-Server, der den Treffer verarbeitet hat. | char(30) |
| `t_time_info` | Lokale Zeit des Besuchers. Format wie folgt: T/M/JJJJ HH:MM:SS Monat (0-11, 0=Januar) Zeitzonenversatz (in Minuten) | varchar(100) |
| `tnt` | Wird in Adobe Target-Integrationen verwendet. | text |
| `tnt_action` | Wird in Adobe Target-Integrationen verwendet. | text |
| `tnt_post_vista` | Wird nicht mehr verwendet. Verwenden Sie stattdessen post_tnt. | text |
| `transactionid` | Eine eindeutige Kennung, bei der später verschiedene Datenpunkte via Datenquellen hochgeladen werden können. | text |
| `truncated_hit` | Ein Flag, das angibt, dass die Bildanforderung gekürzt wurde. Zeigt den Erhalt eines teilweisen Treffers an. <br>Y: Treffer abgeschnitten; Teiltreffer erhalten <br>N: Treffer nicht abgeschnitten; vollständigen Treffer erhalten | char(1) |
| `ua_color` | Wird nicht mehr verwendet. Wurde zuvor als Fallback für die Farbtiefe verwendet. | char(20) |
| `ua_os` | Wird nicht mehr verwendet. Wurde zuvor als Fallback für das Betriebssystem verwendet. | char(80) |
| `ua_pixels` | Wird nicht mehr verwendet. Wurde zuvor als Fallback für die Browserhöhe und -breite verwendet. | char(20) |
| `user_agent` | Im HTTP-Header der Bildanforderung gesendete Benutzeragenten-Zeichenfolge. | text |
| `user_hash` | Wird nicht verwendet. Doppelkreuz in der Report Suite-ID. Verwenden Sie stattdessen username. | int unsigniert |
| `user_server` | Variable, die in der Dimension „Server“ verwendet wurde. | varchar(100) |
| `userid` | Wird nicht verwendet. Die numerische ID für die Report Suite-ID. Verwenden Sie stattdessen username. | int unsigniert |
| `username` | Die Report Suite-ID für den Treffer. | char(40) |
| `va_closer_detail` | Die Variable, die in der Dimension „Letztkontaktdetail“ verwendet wird. | varchar(255) |
| `va_closer_id` | Numerische ID, anhand derer die Dimension „Letztkontaktdetails“ identifiziert wird. Die Suchtabelle für diese ID finden Sie im Marketingkanal-Manager. | tinyint unsigniert |
| `va_finder_detail` | Die Variable, die in der Dimension „Erstkontaktdetail“ verwendet wird. | varchar(255) |
| `va_finder_id` | Numerische ID, anhand derer die Dimension „Erstkontakt Kanal“ identifiziert wird. Die Suchtabelle für diese ID finden Sie im Marketingkanal-Manager. | tinyint unsigniert |
| `va_instance_event` | Flag zur Identifizierung von Marketingkanalinstanzen. Wird von der Metrik Marketingkanal Letztkontaktinstanzen verwendet. | tinyint unsigniert |
| `va_new_engagement` | Flag zur Identifizierung neuer Marketingkanal-Interaktionen. Wird von der Metrik „Neue Interaktionen“ verwendet. | tinyint unsigniert |
| `video` | Videoinhalt | varchar(255) |
| `videoad` | Name der Videoanzeige | varchar(255) |
| `videoadinpod` | Videoanzeigenposition innerhalb der Werbeunterbrechung | varchar(255) |
| `videoadlength` | Länge der Videoanzeige | varchar(255) |
| `videoadload` | Ladeaufforderungen der Videoanzeige | varchar(255) |
| `videoadname` | Name der Videoanzeige | varchar(255) |
| `videoadplayername` | Name des Videoanzeigen-Players | varchar(255) |
| `videoadpod` | Videoanzeigen-Pod | varchar(255) |
| `videoadvertiser` | Videoadvertiser | varchar(255) |
| `videoaudioalbum` | Video-Audio-Album | varchar(255) |
| `videoaudioartist` | Video-Audio-Interpret | varchar(255) |
| `videoaudioauthor` | Video-Audio-Autor | varchar(255) |
| `videoaudiolabel` | Video-Audio-Beschriftung | varchar(255) |
| `videoaudiopublisher` | Video-Audio-Publisher | varchar(255) |
| `videoaudiostation` | Video-Audio-Station | varchar(255) |
| `videocampaign` | Videokampagne | varchar(255) |
| `videochannel` | Video-Kanal | varchar(255) |
| `videochapter` | Video-Kapitelname | varchar(255) |
| `videocontenttype` | Video-Content-Typ Ist für alle Videoansichten automatisch auf „Video“ gesetzt | varchar(255) |
| `videodaypart` | Videotagesabschnitt | varchar(255) |
| `videoepisode` | Videoepisode | varchar(255) |
| `videofeedtype` | Video-Feed-Typ | varchar(255) |
| `videogenre` | Video-Genre | text |
| `videolength` | Videolänge | varchar(255) |
| `videomvpd` | Video-MVPD | varchar(255) |
| `videoname` | Videoname | varchar(255) |
| `videonetwork` | Videonetzwerk | varchar(255) |
| `videopath` | Videopfad | varchar(100) |
| `videoplayername` | Name des Videoplayers | varchar(255) |
| `videoqoebitrateaverageevar` | Videoqualität – Durchschnittliche Bitrate | varchar(255) |
| `videoqoebitratechangecountevar` | Videoqualität – Anzahl Änderungen | varchar(255) |
| `videoqoebuffercountevar` | Videoqualität – Anzahl Puffer | varchar(255) |
| `videoqoebuffertimeevar` | Videoqualitätspufferzeit | varchar(255) |
| `videoqoedroppedframecountevar` | Videoqualität – Anzahl Einzelbildverluste | varchar(255) |
| `videoqoeerrorcountevar` | Videoqualität – Anzahl Fehler | varchar(255) |
| `videoqoeextneralerrors` | Externe Fehler in Videoqualität | text |
| `videoqoeplayersdkerrors` | SDK-Fehler in Videoqualität | text |
| `videoqoetimetostartevar` | Videoqualität – Startzeitpunkt | varchar(255) |
| `videoseason` | Videostaffel | varchar(255) |
| `videosegment` | Videosegment | varchar(255) |
| `videoshow` | Videosendung | varchar(255) |
| `videoshowtype` | Typ der Videosendung | varchar(255) |
| `videostreamtype` | Typ des Videostreams | varchar(255) |
| `visid_high` | Wird zusammen mit visid_low zur eindeutigen Identifizierung eines Besuchers verwendet. | bigint unsigniert |
| `visid_low` | Wird zusammen mit visid_high zur eindeutigen Identifizierung eines Besuchers verwendet. | bigint unsigniert |
| `visid_new` | Flag, das anzeigt, ob der Treffer eine neu generierte Besucher-ID enthält. | char(1) |
| `visid_timestamp` | Wurde die Besucher-ID neu generiert, wird der Zeitstempel (in Unix-Zeit) der Generierung der Besucher-ID bereitgestellt. | int |
| `visid_type` | Nicht zur externen Verwendung; intern von Adobe für Verarbeitungsoptimierungen verwendet. Numerische ID, die die Methode angibt, die zur Identifizierung des Besuchers verwendet wurde.<br>0: Benutzerspezifische Besucher-ID oder unbekannt/nicht anwendbar<br>1: IP- und Benutzeragenten-Fallback <br>2: HTTP Mobile Subscriber Header <br>3: Alter Cookie-Wert (s_vi) <br>4: Fallback-Cookie-Wert (s_fid) <br>5: Identity Service | tinyint unsigniert |
| `visit_keywords` | Variable, die in der Dimension „Suchbegriff“ verwendet wird. Diese Spalte verwendet eine nicht standardmäßige Zeichenbeschränkung, um der von Adobe verwendeten Backend-Logik Rechnung zu tragen. | varchar(244) |
| `visit_num` | Variable, die in der Dimension „Besuchsnummer“ verwendet wird. Beginnt bei 1 und erhöht sich bei jedem neuen Besuch eines Besuchers. | int unsigniert |
| `visit_page_num` | Variable, die in Dimension „Treffertiefe“ verwendet wird. Wird für jeden vom Benutzer generierten Treffer um 1 erhöht. Setzt jeden Besuch zurück. | int unsigniert |
| `visit_ref_domain` | Basiert auf der Spalte visit_referrer. Die allererste verweisende Domäne des Besuchs. | varchar(100) |
| `visit_ref_type` | Numerische ID des Typs der verweisenden Stelle der ersten verweisenden Stelle des Besuchs. Verwendet die Suchtabelle referrer_type.tsv | tinyint unsigniert |
| `visit_referrer` | Die erste verweisende Stelle des Besuchs. | varchar(255) |
| `visit_search_engine` | Numerische ID der ersten Suchmaschine des Besuchs. Verwendet die Suchtabelle search_engines.tsv | smallint unsigniert |
| `visit_start_page_url` | Die erste URL des Besuchs. | varchar(255) |
| `visit_start_pagename` | Der erste Seitenname des Besuchs. | varchar(100) |
| `visit_start_time_gmt` | Zeitstempel (in Unix-Zeit) des ersten Treffers des Besuchs. | int |
| `weekly_visitor` | Flag zur Bestimmung, ob der Treffer ein neuer wöchentlicher Besucher ist. | tinyint unsigniert |
| `yearly_visitor` | Flag zur Bestimmung, ob der Treffer ein neuer jährlicher Besucher ist. | tinyint unsigniert |
| `zip` | Wird zum Füllen der Dimension „Postleitzahl“ verwendet. | varchar(50) |

## Leere Spalten

Die folgende Liste von Spalten wird nicht verwendet und enthält keine Daten:

* mobileacquisitionclicks
* mobileactioninapptime
* mobileactiontotaltime
* mobileappperformanceaffectedusers
* mobileappperformanceappid<span>.</span>app-perf-app-name
* mobileappperformanceappid<span>.</span>app-perf-platform
* mobileappperformancecrashes
* mobileappperformancecrashid<span>.</span>app-perf-crash-name
* mobileappperformanceloads
* mobileappstoreavgrating
* mobileappstoredownloads
* mobileappstoreinapprevenue
* mobileappstoreinapproyalties
* mobileappstoreobjectid<span>.</span>app-store-user
* mobileappstoreobjectid<span>.</span>application-name
* mobileappstoreobjectid<span>.</span>application-version
* mobileappstoreobjectid<span>.</span>appstore-name
* mobileappstoreobjectid<span>.</span>category-name
* mobileappstoreobjectid<span>.</span>country-name
* mobileappstoreobjectid<span>.</span>device-manufacturer
* mobileappstoreobjectid<span>.</span>device-name
* mobileappstoreobjectid<span>.</span>in-app-name
* mobileappstoreobjectid<span>.</span>platform-name-version
* mobileappstoreobjectid<span>.</span>rank-category-type
* mobileappstoreobjectid<span>.</span>region-name
* mobileappstoreobjectid<span>.</span>review-comment
* mobileappstoreobjectid<span>.</span>review-title
* mobileappstoreoneoffrevenue
* mobileappstoreoneoffroyalties
* mobileappstorepurchases
* mobileappstorerank
* mobileappstorerankdivisor
* mobileappstorerating
* mobileappstoreratingdivisor
* mobileavgprevsessionlength
* mobilecrashes
* mobilecrashrate
* mobiledailyengagedusers
* mobiledeeplinkid<span>.</span>name
* mobileinstalls
* mobilelaunches
* mobileltvtotal
* mobilemessageclicks
* mobilemessageid<span>.</span>dest
* mobilemessageid<span>.</span>name
* mobilemessageid<span>.</span>type
* mobilemessageimpressions
* mobilemessagepushpayloadid<span><span>.</span></span>name
* mobilemessageviews
* mobilemonthlyengagedusers
* mobileplacedwelltime
* mobileplaceentry
* mobileplaceexit
* mobileprevsessionlength
* mobilerelaunchcampaigntrackingcode<span><span>.</span></span>name
* mobileupgrades
* socialaveragesentiment
* socialaveragesentiment (deprecated)
* socialfbstories
* socialfbstorytellers
* socialinteractioncount
* sociallikeadds
* sociallink
* sociallink (nicht mehr unterstützt)
* socialmentions
* socialpageviews
* socialpostviews
* socialproperty
* socialproperty (nicht mehr unterstützt)
* socialpubcomments
* socialpubposts
* socialpubrecommends
* socialpubsubscribers
* socialterm
* socialtermslist
* socialtermslist (nicht mehr unterstützt)
* socialtotalsentiment
* sourceid
* videoauthorized
* videoaverageminuteaudience
* videochaptercomplete
* videochapterstart
* videochaptertime
* videopause
* videopausecount
* videopausetime
* videoplay
* videoprogress10
* videoprogress25
* videoprogress50
* videoprogress75
* videoprogress96
* videoqoebitrateaverage
* videoqoebitratechange
* videoqoebuffer
* videoqoedropbeforestart
* videoqoedroppedframes
* videoqoeerror
* videoresume
* videototaltime
* videouniquetimeplayed
