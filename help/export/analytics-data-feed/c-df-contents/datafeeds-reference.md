---
description: Tabellendaten, die die Spalten im Datenfeed beschreiben.
keywords: Data Feed;columns
subtopic: data feeds
title: Datenspaltenreferenz
topic: Reports and analytics
uuid: 9042a274-7124-4323-8cd6-5c84ab3eef6d
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Datenspaltenreferenz

Auf dieser Seite erfahren Sie, welche Daten in den einzelnen Spalten enthalten sind. Bei den meisten Implementierungen wird nicht jede Spalte verwendet. Daher kann auf diese Seite verwiesen werden, wenn bestimmt wird, welche Spalten in einen Datenfeed-Export einbezogen werden sollen.

> [!IMPORTANT] Für jede Spalte (z. B. eine Spalte, die als 255 Zeichen definiert ist) kann ein Datenfeed zusätzliche Zeichen senden, da Zeichen hinzugefügt werden, die Werte in einer Zeichenfolge Escapezeichen enthalten. Berücksichtigen Sie diese potenziellen zusätzlichen Zeichen, wenn Ihre Implementierung regelmäßig Werte sendet, die die Zeichenbeschränkungen überschreiten.

## Spalten, Beschreibungen und Datentypen

> [!NOTE] Die meisten Spalten enthalten eine ähnliche Spalte mit dem Präfix `post_`. Post-Spalten enthalten Werte nach der serverseitigen Logik, den Verarbeitungsregeln und den VISTA-Regeln. Adobe empfiehlt in den meisten Fällen die Verwendung von Post-Spalten. Weitere Informationen finden Sie unter Häufig gestellte Fragen zu [Datenfeeds](../df-faq.md) .

| Spaltenname | Spaltenbeschreibung | Datentyp |
| --- | --- | --- |
| accept_language | Führt alle unterstützten Sprachen, wie im HTTP-Header Accept-Language angegeben, in einer Bildanforderung auf | char(20) |
| aemassetid | Eine mehrwertige Variable, die Asset-IDs (GUIDs) einer Reihe von Adobe Experience Manager Assets entspricht Erhöht Impressionsereignisse | text |
| aemassetsource | Identifiziert die Quelle des Asset-Ereignisses Wird in Adobe Experience Manager verwendet | varchar(255) |
| aemclickedassetid | Asset-ID eines Adobe Experience Manager-Assets Erhöht Klickereignisse | varchar(255) |
| Browser | Numerische ID des Browsers Verweist auf die Suchtabelle browser.tsv | int unsigned |
| browser_height | Höhe des Browser-Fensters in Pixeln. | smallint unsigned |
| browser_width | Breite des Browser-Fensters in Pixeln. | smallint unsigned |
| c_color | Bit-Tiefe der Farbpalette Wird im Rahmen der Berechnung der Dimension „Farbtiefe“ verwendet Verwendet die JavaScript-Funktion screen.colorDepth() | char(20) |
| Kampagne | Variable, die in der Dimension „Trackingcode“ verwendet wird | varchar(255) |
| carrier | Variable der Adobe Advertising Cloud-Integration Gibt den Mobilfunknetzbetreiber an Verweist auf die Suchtabelle des Mobilfunknetzbetreibers | varchar(100) |
| kanal | Variable, die in der Dimension „Sitebereiche“ verwendet wird | varchar(100) |
| click_action | Wird nicht mehr länger verwendet. Adresse des Links, auf dem im veralteten ClickMap-Tool geklickt wurde | varchar(100) |
| click_action_type | Wird nicht mehr länger verwendet. Link-Typ des veralteten ClickMap-Tools.<br>0: HREF-URL<br>1: Benutzerspezifische ID<br>2: JavaScript onClick-Ereignis<br>3: Formularelement | tinyint unsigniert |
| click_context | Wird nicht mehr länger verwendet. Name der Seite mit dem Link-Klick Teil des veralteten ClickMap-Tools | varchar(255) |
| click_context_type | Wird nicht mehr länger verwendet. Gibt an, ob es für click_context einen Seitennamen gibt oder standardmäßig die Seiten-URL gilt<br>0: Seiten-URL<br>1: Seitenname | tinyint unsigniert |
| click_sourceid | Wird nicht mehr länger verwendet. Numerische ID der Linkposition auf der Seite Teil des veralteten ClickMap-Tools | int unsigned |
| click_tag | Wird nicht mehr länger verwendet. HTML-Elementtyp, auf den geklickt wurde | char(10) |
| clickmaplink | Activity Map-Link | varchar(255) |
| clickmaplinkbyregion | Activity Map-Link nach Region | varchar(255) |
| clickmappage | Activity Map-Seite | varchar(255) |
| clickmapregion | Activity Map-Region | varchar(255) |
| code_ver | Bibliotheksversion von AppMeasurement, die für das Kompilieren und Senden der Bildanforderung verwendet wird | char(16) |
| color | Farbtiefen-ID basierend auf dem Wert der c_color-Spalte Verweist auf die Suchtabelle color_depth.tsv | smallint unsigned |
| connection_type | Numerische ID, die den Verbindungstyp darstellt Die Variable, die in der Dimension „Verbindungstyp“ verwendet wurde Verweist auf die Suchtabelle connection_type.tsv | tinyint unsigniert |
| Cookies | Die Variable, die in der Dimension „Cookie-Unterstützung“ verwendet wurde<br>Y:<br>EnabledN:<br>DeaktiviertU: unbekannt | char(1) |
| country | Numerische ID, die das Land angibt, aus dem der Treffer stammt Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Ländern zuzuordnen. Verwendet die Suchtabelle country.tsv | smallint unsigned |
| ct_connect_type | Bezieht sich auf die Spalte connection_type Die häufigsten Werte sind LAN/WLAN, Mobilfunknetzbetreiber und Modem | char(20) |
| curr_factor | Bestimmt die Dezimalstelle für die Währung und wird zur Währungsumrechnung verwendet Für USD werden beispielsweise zwei Dezimalstellen verwendet, sodass der Spaltenwert 2 ist. | tinyint |
| curr_rate | Der Wechselkurs zum Zeitpunkt der Transaktion Adobe arbeitet mit XE zusammen, um den aktuellen Wechselkurs zu bestimmen. | Dezimalzahl(24,12) |
| currency | Der während der Transaktion verwendete Währungscode | char(8) |
| cust_hit_time_gmt | Nur für Report Suites mit aktiviertem Zeitstempel Der mit dem Treffer gesendet Zeitstempel in Unix-Zeit | int |
| cust_visid | Wurde eine benutzerdefinierte Besucher-ID festgelegt, wird sie in diese Spalte aufgenommen. | varchar(255) |
| daily_visitor | Flag zur Bestimmung, ob der Treffer ein neuer täglicher Besucher ist | tinyint unsigniert |
| date_time | Die Uhrzeit des Treffers in lesbarem Format, basierend auf der Zeitzone der Report Suite | datetime |
| domain | Variable, die in der Dimension „Domäne“ verwendet wurde Basiert auf dem Internetdienstanbieter (ISP) des Benutzers | varchar(100) |
| duplicate_events | Listet alle Ereignisse auf, die als Duplikat gezählt wurden. | varchar(255) |
| duplicate_purchase | Ein Flag, das anzeigt, dass das Kaufereignis für diesen Treffer ignoriert werden muss, da es ein Duplikat ist | tinyint unsigniert |
| duplicated_from | Wird nur in Report Suites mit VISTA-Regeln zur Trefferkopie verwendet Gibt an, von welcher Report Suite der Treffer kopiert wurde | varchar(40) |
| ef_id | Die ef_id, die in Adobe Advertising Cloud-Integrationen verwendet wird | varchar(255) |
| evar1-evar250 | Benutzerdefinierte Variablen 1–250 Jede Organisation verwendet eVars anders Der beste Ort für weitere Informationen dazu, wie Ihre Organisation entsprechende eVars füllt, ist ein Dokument zum Lösungsentwurf, das für Ihre Organisation gilt. | varchar(255) |
| event_list | Kommagetrennte Liste numerischer IDs, die die durch den Treffer ausgelösten Ereignisse darstellen Enthält sowohl die Standardereignisse als auch die benutzerdefinierten Ereignisse 1–1000 Verwendet die Suchtabelle event.tsv | text |
| exclude_hit | Ein Flag, das angibt, dass der Treffer nicht in die Berichterstellung einfließt Die Spalte visit_num wird bei ausgeschlossenen Treffern nicht inkrementiert.<br>1: Nicht verwendet. Teil einer übersprungenen Funktion.<br>2: Nicht verwendet. Teil einer übersprungenen Funktion.<br>3: Nicht mehr verwendet. Benutzeragentenausschluss<br>4: Ausschluss basierend auf IP-Adresse<br>5: Wichtige Trefferinformationen fehlen, z. B. page_url, pagename, page_event oder event_list<br>6: JavaScript hat Treffer<br>7 nicht korrekt verarbeitet: Kontospezifischer Ausschluss, z. B. in VISTA-Regeln<br>8: Nicht verwendet. Alternativer kontospezifischer Ausschluss.<br>9: Nicht verwendet. Teil einer übersprungenen Funktion.<br>10: Ungültiger Währungscode<br>11: Treffer, bei dem ein Zeitstempel für eine Report Suite mit nur Zeitstempel fehlt, oder ein Treffer mit einem Zeitstempel für eine Report Suite<br>12 ohne Zeitstempel: Nicht verwendet. Teil einer übersprungenen Funktion.<br>13: Nicht verwendet. Teil einer übersprungenen Funktion.<br>14: Target-Treffer, der nicht mit einem Analytics-Treffer<br>15 übereinstimmte: Nicht verwendet.<br>16: Advertising Cloud-Treffer, der nicht mit einem Analytics-Treffer übereinstimmte | tinyint unsigniert |
| first_hit_page_url | Die allererste URL des Besuchers | varchar(255) |
| first_hit_pagename | Variable, die in der Dimension „Ursprüngliche Entrypage“ verwendet wird Der Name der ursprünglichen Entrypage des Besuchers | varchar(100) |
| first_hit_ref_domain | Variable, die in der Dimension „Ursprünglich verweisende Domäne“ verwendet wird Basiert auf first_hit_referrer Die allererste verweisende Domäne des Besuchers | varchar(100) |
| first_hit_ref_type | Numerische ID des Typs der verweisenden Stelle der allerersten verweisenden Stelle des Besuchers Verwendet die Suche referrer_type.tsv | tinyint unsigniert |
| first_hit_referrer | Die allererste verweisende URL des Besuchers | varchar(255) |
| first_hit_time_gmt | Zeitstempel des allerersten Treffers des Besuchers in Unix-Zeit | int |
| geo_city | Name der Stadt, aus der der Treffer stammt, basierend auf der IP Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Städten zuzuordnen | char(32) |
| geo_country | Abkürzung für das Land, aus dem der Treffer stammt, basierend auf der IP Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Ländern zuzuordnen. | char(4) |
| geo_dma | Numerische ID des demografischen Bereichs, aus dem der Treffer stammt, basierend auf der IP Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu demografischen Bereichen zuzuordnen. | int unsigned |
| geo_region | Name des Bundeslands oder der Region, aus der der Treffer stammt, basierend auf der IP Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Bundesländern bzw. Regionen zuzuordnen. | char(32) |
| geo_zip | Die Postleitzahl, von der der Treffer kam, basierend auf IP. Adobe arbeitet mit Digital Envoy zusammen, um IP-Adressen zu Postleitzahlen zuzuordnen. | varchar(16) |
| hier1 – hier5 | Wird von Hierarchievariablen verwendet. Enthält eine durch Trennzeichen getrennte Werteliste Das in den Report Suite-Einstellungen gewählte Trennzeichen | varchar(255) |
| hit_source | Gibt die Quelle an, aus der der Treffer stammt <br>1: Standard-Bildanforderung ohne Zeitstempel <br>2: Standard-Bildanforderung mit Zeitstempel <br>3: Hochladen der Live-Datenquelle mit Zeitstempel <br>4: Nicht verwendet <br>5: Generischer Datenquellen-Upload <br>6: Datenquellen-Upload mit voller Verarbeitung <br>7: TransaktionsID-Datenquellenupload <br>8: nicht mehr verwendet; Frühere Versionen der Adobe Advertising Cloud-Datenquellen <br>9: nicht mehr verwendet; Metriken zur Zusammenfassung in Adobe Social | tinyint unsigniert |
| hit_time_gmt | Der Zeitstempel des Treffers Adobe-Datenerfassungsserver erhielt den Treffer, basierend auf der Unix-Zeit. | int |
| hitid_high | Wird zusammen mit hitid_low zur eindeutigen Identifizierung eines Treffers verwendet | bigint unsigned |
| hitid_low | Wird zusammen mit hitid_high zur eindeutigen Identifizierung eines Treffers verwendet | bigint unsigned |
| homepage | Wird nicht mehr länger verwendet. Wird angezeigt, wenn die aktuelle URL die Browser-Startseite ist | char(1) |
| hourly_visitor | Flag zur Bestimmung, ob der Treffer ein neuer stündlicher Besucher ist | tinyint unsigniert |
| ip | IP-Adresse basierend auf dem HTTP-Header der Bildanforderung | char(20) |
| ip2 | Nicht verwendet. Backend-Verweis-Variable für Report Suites mit VISTA-Regeln basierend auf IP-Adressen | char(20) |
| j_jscript | Vom Browser unterstützte JavaScript-Version | char(5) |
| java_enabled | Ein Flag, das angibt, ob Java aktiviert ist <br>Y: Aktiviert <br>N: Deaktiviert <br>U: unbekannt | char(1) |
| javascript | Such-ID der JavaScript-Version, basierend auf j_jscript Verwendet eine Suchtabelle | tinyint unsigniert |
| language | Numerische ID der Sprache Verwendet die Suchtabelle languages.tsv | smallint unsigned |
| last_hit_time_gmt | Zeitstempel (in Unix-Zeit) des vorherigen Treffers Wird zur Berechnung der Dimension „Tage seit dem letzten Besuch“ verwendet | int |
| last_purchase_num | Variable, die in der Dimension „Kundenloyalität“ verwendet wird Gibt die Anzahl der vorherigen Käufe des Besuchers an <br>0: Keine vorherigen Einkäufe (kein Kunde) <br>1: 1 vorheriger Kauf (neuer Kunde) <br>2: 2 vorherige Käufe (rückkehrender Kunde) <br>3: 3 oder mehr frühere Käufe (treuer Kunde) | int unsigned |
| last_purchase_time_gmt | Variable, die in der Dimension „Tage seit letztem Kauf“ verwendet wird Zeitstempel (in Unix-Zeit) des letzten Kaufs Bei Erstkäufen und Besuchern, die zuvor noch nichts gekauft haben, ist dieser Wert 0. | int |
| latlon1 | Standort (bis 10 km) | varchar(255) |
| latlon23 | Standort (bis 100 m) | varchar(255) |
| latlon45 | Standort (bis 1 m) | varchar(255) |
| mc_audiences | Liste der Audience Manager-Segment-IDs, zu denen der Besucher gehört | text |
| mcvisid | Experience Cloud-Besucher-ID. 128-Bit-Zahl bestehend aus zwei verketteten 64-Bit-Zahlen verteilt auf 19 Ziffern | varchar(255) |
| mobile_id | Wenn der Benutzer ein Mobilgerät verwendet, die numerische ID des Geräts. | int |
| mobileaction | Mobile Aktion Wird automatisch erfasst, wenn trackAction in Mobile Services aufgerufen wird. Ermöglicht automatische Handlungsvorgänge in der App. | varchar(100) |
| mobileappid | ID der mobilen App Speichert den Applikationsnamen und die Version im folgenden Format:[AppName] [BundleVersion] | varchar(255) |
| mobileappperformanceAppid | Wird im Apteligent Data Connector verwendet. Die in Apteligent verwendete App-ID. | varchar(255) |
| mobileappperformanceCrashid | Wird im Apteligent Data Connector verwendet. Die Absturz-ID, die in Apteligent verwendet wird. | varchar(255) |
| mobileappstoreobjectid | Wird im Data Connector von Appfigs verwendet. App Store-Objekt-ID | varchar(255) |
| mobilebeaconmajor | Mobile Services-Beacon-Hauptversion | varchar(100) |
| mobilebeaconminor | Mobile Services-Beacon-Moll | varchar(100) |
| mobilebeaconproximity | Nähe zum Mobile Services-Beacon | varchar(255) |
| mobilebeaconuuid | Mobile Services-Beacon UUID | varchar(100) |
| mobilecampaigncontent | Der Name der ID des Inhalts, in dem der Link angezeigt wurde. Erfasst durch App-Akquise. | varchar(255) |
| mobilecampaignmedium | Marketingmedium, z. B. Banner oder E-Mail. Erfasst durch App-Akquise. | varchar(255) |
| mobilecampaignname | Name der Kampagne, ebenfalls gespeichert in der Kampagnenvariable. Erfasst durch App-Akquise. | varchar(255) |
| mobilecampaignsource | Ursprünglicher Referrer, wie z. B. Newsletter oder soziales Netzwerk. Erfasst durch App-Akquise. | varchar(255) |
| mobilecampaignterm | Bezahlte Keywords oder andere Begriffe, die Sie mit dieser Akquise verfolgen wollen. Erfasst durch App-Akquise. | varchar(255) |
| mobiledayofweek | Nummer des Wochentags, an dem die App gestartet wurde | varchar(255) |
| mobiledayssincefirstuse | Anzahl der Tage, die seit dem ersten Ausführen der App vergangen sind | varchar(255) |
| mobiledayssincelastupgrade | Wird aus der Kontextdatenvariablen a.DaysSinceLastUpgrade erfasst. Die Anzahl der Tage, die seit der vorherigen Sitzung vergangen sind. | varchar(255) |
| mobiledayssincelastuse | Anzahl der Tage, die vergangen sind, seitdem die App das letzte Mal ausgeführt wurde | varchar(255) |
| mobiledeeplinkid | Wird aus der Kontextdatenvariablen a.<span>deeplink</span>.id erfasst. Wird in Akquise-Berichten als Identifikator für Link zur mobilen Akquise verwendet. | varchar(255) |
| mobiledevice | Mobilgerätname Unter iOS als kommagetrennte 2-Ziffern-Zeichenfolge gespeichert Die erste Zahl gibt die Gerätegeneration an und die zweite die Gerätefamilie. | varchar(255) |
| mobilehourofday | Gibt die Stunde des Tages an, zu der die App gestartet wurde Angaben im 24-Stunden-Format | varchar(255) |
| mobileinstalldate | Installationsdatum der mobilen App Stellt das Datum zur Verfügung, an dem ein Benutzer die mobile App erstmalig geöffnet hat | varchar(255) |
| mobilelaunchessincelastupgrade | Wird aus der Kontextdatenvariablen a.LaunchesSinceUpgrade erfasst. Gibt die Anzahl der Starts seit der letzten Aktualisierung an. | varchar(255) |
| mobilelaunchnumber | Wird immer dann erhöht, wenn die mobile App gestartet wird | varchar(255) |
| mobileltv | Wird nicht mehr länger verwendet. Erfasst durch trackLifetimeValue-Methoden. | varchar(255) |
| mobilemessagebuttonname | Wird aus der Kontextdatenvariablen a.<span>message</span>.button.id erfasst. Wird für In-App-Nachrichten verwendet, um die Schaltfläche zu identifizieren, mit der die Nachricht geschlossen wurde. | varchar(100) |
| mobilemessageid | In-App-Nachrichten-ID | varchar(255) |
| mobilemessageonline | In-App-Nachricht online | varchar(255) |
| mobilemessagepushoptin | Wird aus der Kontextdatenvariablen a.push.optin erfasst. auf "true"setzen, wenn der Benutzer sich für Push-Nachrichten entscheidet; andernfalls lautet der Wert "false". | varchar(255) |
| mobilemessagepushpayloadid | Wird aus der Kontextdatenvariablen a.push.payloadid erfasst. Wird in Push-Nachrichten als Nutzlastbezeichner verwendet. | varchar(255) |
| mobileosenvironment | Wird aus der Kontextdatenvariablen a.OSEnenvironment erfasst. Status-OS-Umgebung, z. B. Android oder iOS. | varchar(255) |
| mobileosversion | Mobile Services-Betriebssystemversion | varchar(255) |
| mobileplaceaccuracy | Erfasst aus der Kontextdatenvariablen a.loc.acc. Gibt die Genauigkeit des GPS zum Zeitpunkt der Erfassung in Metern an. | varchar(255) |
| mobileplacecategory | Wird aus der Kontextdatenvariablen a.loc.category erfasst. Beschreibt die Kategorie eines bestimmten Orts. | varchar(255) |
| mobileplaceid | Wird aus der Kontextdatenvariablen a.<span>loc</span>.id erfasst. Bezeichner für einen bestimmten Zielpunkt. | varchar(255) |
| mobilerelaunchampagneninhalt | Mobile Services - Startinhalte | varchar(255) |
| mobilerelaunchcampaign | Startmedium für Mobile Services | varchar(255) |
| mobilerelaunchcampaign source | Startquelle für Mobile Services | varchar(255) |
| mobilerelaunchcampaign | Mobile Services - Starttermin | varchar(255) |
| mobilerelaunchcampaign trackingcode | Wird aus der Kontextdatenvariablen a.launch.campaign.trackingcode erfasst. Wird bei der Akquise als Rückverfolgungscode für die Startkampagne verwendet. | varchar(255) |
| mobileresolution | Auflösung des Mobilgeräts Breite x Höhe in Pixel | varchar(255) |
| monthly_visitor | Flag, das angibt, dass der Benutzer im aktuellen Monat eindeutig ist | tinyint unsigniert |
| mvvar1 - mvvar3 | Listenvariablenwerte Enthält eine durch Trennzeichen getrennte Liste benutzerdefinierter Werte in Abhängigkeit von der Implementierung | text |
| namespace | Nicht verwendet. Teil einer veralteten Funktion | varchar(50) |
| new_visit | Ein Flag, das bestimmt, ob der aktuelle Treffer ein neuer Besuch ist. Wird von Adobe-Servern nach einer 30-minütigen Besuchsinaktivität festgelegt | tinyint unsigniert |
| os | Numerische ID, die das Betriebssystem des Besuchers darstellt Basiert auf der Spalte user_agent Verwendet die os-Suche | int unsigned |
| p_plugins | Wird nicht mehr länger verwendet. Liste der für den Browser verfügbaren Plugins. Hat die JavaScript-Funktion navigator.plugins() verwendet | text |
| page_event | Die Art des Treffers, die in der Bildanforderung gesendet wird (Standardtreffer, Downloadlink, benutzerspezifischer Link, Exitlink) See [Page event lookup](datafeeds-page-event.md). | tinyint unsigniert |
| page_event_var1 | Wird nur in Linktracking-Bildanforderungen verwendet Die URL des angeklickten Downloadlinks, Exitlinks oder benutzerspezifischen Links | text |
| page_event_var2 | Wird nur in Linktracking-Bildanforderungen verwendet Der benutzerdefinierte Name des Links, sofern angegeben | varchar(100) |
| page_event_var3 | Wird nicht mehr länger verwendet. Enthielt Umfrage- und Medienmoduldaten Füllte verwaltete Videoberichte in vorherigen Versionen von Adobe Analytics | text |
| page_type | Wird zum Füllen der Dimension „Seiten nicht gefunden“ verwendet; nur für 404-Seiten Die Variable sollte entweder leer sein oder „ErrorPage“ enthalten. | char(20) |
| page_url | Die URL des Treffers Wird nicht in Linktracking-Bildanforderungen verwendet | varchar(255) |
| pagename | Wird zum Füllen der Dimension „Seiten“ verwendet Wenn die Variable „pagename“ leer ist, verwendet Analytics stattdessen page_url. | varchar(100) |
| paid_search | Flag, das gesetzt wird, wenn der Treffer mit der gebührenpflichtigen Sucherkennung übereinstimmt | tinyint unsigniert |
| partner_plugins | Nicht verwendet. Teil einer veralteten Funktion | varchar(255) |
| persistent_cookie | Wird von der Dimension „Unterstützung beständiger Cookies“ verwendet Gibt an, ob der Benutzer Cookies unterstützt, die nicht nach jedem Treffer gelöscht werden | char(1) |
| plugins | Wird nicht mehr länger verwendet. Liste numerischer IDs, die den im Browser verfügbaren Plugins entsprechen Verwendet die Suchtabelle plugins.tsv | varchar(180) |
| pointofinterest | Name des Zielpunkts für Mobile Services | varchar(255) |
| pointofinterestdistance | Entfernung von Mobile Services zum Zielpunkt | varchar(255) |
| „post_“-Spalten | Enthält den in diesen Berichten ultimativ verwendeten Wert Jede Post-Spalte wird nach der serverseitigen Logik, den Verarbeitungsregeln und den VISTA-Regeln gefüllt. Adobe empfiehlt in den meisten Fällen die Verwendung von Post-Spalten. | Vgl. entsprechende non-post-Spalte |
| prev_page | Nicht verwendet. Proprietäre Adobe ID der vorherigen Spalte | int unsigned |
| product_list | Produktliste, so wie sie von der Variable der Produkte übergeben wurde Produkte sind durch Kommata voneinander getrennt und individuelle Produkteigenschaften durch Semikolons. | text |
| product_merchandising | Nicht verwendet. Verwenden Sie stattdessen product_list. | text |
| prop1 – prop75 | Benutzerdefinierte Traffic-Variablen 1–75. | varchar(100) |
| purchaseid | Eindeutige ID für einen Kauf, so wie durch das Festlegen der Variable s_purchaseID bestimmt Wird von der Spalte duplicate_purchase verwendet | char(20) |
| quarterly_visitor | Flag zur Bestimmung, ob der Treffer ein neuer Quartals-Besucher ist | tinyint unsigniert |
| ref_domain | Basiert auf der Referrer-Spalte Die verweisende Domäne des Treffers | varchar(100) |
| ref_type | Eine numerische ID, die den Typ des Verweises für den Treffer darstellt<br>1: Innerhalb Ihrer Site<br>2: Andere Websites <br>3: Suchmaschinen <br>4: Festplatte <br>5: USENET <br>6: Eingegeben/mit Lesezeichen versehen (keine verweisende Stelle) <br>7: E-Mail <br>8: Kein JavaScript <br>9: Soziale Netzwerke | tinyint unsigniert |
| referrer | Seiten-URL der vorherigen Seite | varchar(255) |
| resolution | Numerische ID, die die Auflösung des Bildschirms darstellt Bestückt die Dimension „Bildschirmauflösung“ Verwendet die Suchtabelle resolution.tsv | smallint unsigned |
| s_kwcid | In Adobe Advertising Cloud-Integrationen verwendete Suchbegriff-ID. | varchar(255) |
| s_resolution | Rohwert der Bildschirmauflösung Erfasst mit der JavaScript-Funktion screen.width x screen.height | char(20) |
| sampled_hit | Wird nicht mehr länger verwendet. Wurde zuvor für das Sampling in Ad Hoc Analysis verwendet | char(1) |
| search_engine | Numerische ID, die die Suchmaschine darstellt, die den Besucher auf Ihre Site verwiesen hat Verwendet die Suche search_engines.tsv | smallint unsigned |
| search_page_num | Wird von der Dimension „Rangansicht aller Suchseiten“ verwendet Gibt an, auf welcher Seite der Suchergebnisse Ihre Site angezeigt wurde, ehe der Benutzer sich zu Ihrer Site durchgeklickt hat | smallint unsigned |
| secondary_hit | Flag, das sekundäre Treffer verfolgt Stammt ursprünglich vom Multi-Suite-Tagging und von VISTA-Regel, die Treffer kopieren | tinyint unsigniert |
| service | Nicht verwendet. Verwenden Sie stattdessen page_event. | char(2) |
| socialaccountandappids | Wird nicht mehr länger verwendet. Social-Media-Konto und App-IDs | varchar(255) |
| socialassettrackingcode | Wird nicht mehr länger verwendet. Variable für Social-Media-Kampagnen | varchar(255) |
| socialauthor | Wird nicht mehr länger verwendet. Variable für Social-Media-Autoren | varchar(255) |
| socialcontentprovider | Wird nicht mehr länger verwendet. Soziale Plattformen/Eigenschaften | varchar(255) |
| socialinteractiontype | Wird nicht mehr länger verwendet. Art der sozialen Interaktion | varchar(255) |
| sociallanguage | Wird nicht mehr länger verwendet. Social-Media-Sprache | varchar(255) |
| sociallatlong | Wird nicht mehr länger verwendet. Social – Längen- und Breitengrad | varchar(255) |
| socialowneddefinitioninsighttype | Wird nicht mehr länger verwendet. Soziale eigene Definition Insight-Typ | varchar(255) |
| socialowneddefinitioninsightvalue | Wird nicht mehr länger verwendet. Soziale eigene Definition Insight-Wert | varchar(255) |
| socialowneddefinitionmetric | Wird nicht mehr länger verwendet. Soziale eigene Definition Metrik | varchar(255) |
| socialowneddefinitionpropertyvspost | Wird nicht mehr länger verwendet. Soziale eigene Definition Eigenschaft vs. Post | varchar(255) |
| socialownedpostids | Wird nicht mehr länger verwendet. Social – eigene Post-IDs | varchar(255) |
| socialownedpropertyid | Wird nicht mehr länger verwendet. Soziale eigene Eigenschafts-ID | varchar(255) |
| socialownedpropertyname | Wird nicht mehr länger verwendet. Sozialer eigener Eigenschaftsname | varchar(255) |
| socialownedpropertypropertyvsapp | Wird nicht mehr länger verwendet. Social – eigene Eigenschaft vs App | varchar(255) |
| state | Bundeslandvariable | varchar(50) |
| stats_server | Wird nicht verwendet. Interner Adobe-Server, der den Treffer verarbeitet hat | char(30) |
| t_time_info | Lokale Zeit des Besuchers. Format wie folgt: M/D/YYYY HH:MM:SS Monat (0-11, 0=Januar) Zeitzonenoffset (in Minuten) | varchar(100) |
| tnt | Wird in Adobe Target-Integrationen verwendet | text |
| tnt_action | Wird in Adobe Target-Integrationen verwendet | Text |
| tnt_post_vista | Wird nicht mehr länger verwendet. Verwenden Sie stattdessen post_tnt. | text |
| transactionid | Eine eindeutige Kennung, bei der später verschiedene Datenpunkte via Datenquellen hochgeladen werden können | text |
| truncated_hit | Ein Flag, das angibt, dass die Bildanforderung gekürzt wurde Zeigt den Erhalt eines teilweisen Treffers an <br>Y: Treffer abgeschnitten; Teiltreffer erhalten <br>N: Treffer nicht abgeschnitten; vollständigen Treffer erhalten | char(1) |
| ua_color | Wird nicht mehr länger verwendet. Wurde zuvor als Fallback für die Farbtiefe verwendet | char(20) |
| ua_os | Wird nicht mehr länger verwendet. Wurde zuvor als Fallback für das Betriebssystem verwendet | char(80) |
| ua_pixels | Wird nicht mehr länger verwendet. Wurde zuvor als Fallback für die Browserhöhe und -breite verwendet | char(20) |
| user_agent | Im HTTP-Header der Bildanforderung gesendete Benutzeragenten-Zeichenfolge | text |
| user_hash | Wird nicht verwendet. Doppelkreuz in der Report Suite-ID. Verwenden Sie stattdessen username. | int unsigned |
| user_server | Variable, die in der Dimension „Server“ verwendet wurde | varchar(100) |
| userid | Wird nicht verwendet. Die numerische ID für die Report Suite-ID Verwenden Sie stattdessen username. | int unsigned |
| username | Die Report Suite-ID für den Treffer. | char(40) |
| va_closer_detail | Die Variable, die in der Dimension „Letztkontaktdetail“ verwendet wird | varchar(255) |
| va_closer_id | Numerische ID, anhand derer die Dimension „Letztkontaktdetails“ identifiziert wird Die Suchtabelle für diese ID finden Sie im Marketingkanal-Manager. | tinyint unsigniert |
| va_finder_detail | Die Variable, die in der Dimension „Erstkontaktdetail“ verwendet wird | varchar(255) |
| va_finder_id | Numerische ID, anhand derer die Dimension „Erstkontakt Kanal“ identifiziert wird Die Suchtabelle für diese ID finden Sie im Marketingkanal-Manager. | tinyint unsigniert |
| va_instance_event | Flag zur Identifizierung von Marketingkanalinstanzen Wird von der Metrik Marketingkanal Letztkontaktinstanzen verwendet | tinyint unsigniert |
| va_new_engagement | Flag zur Identifizierung neuer Marketingkanal-Engagements Wird von der Metrik „Neue Interaktionen“ verwendet | tinyint unsigniert |
| video | Videoinhalt | varchar(255) |
| videoad | Name der Videoanzeige | varchar(255) |
| videoadinpod | Videoanzeige an der Position "Pod" | varchar(255) |
| videoadlength | Videoanzeigenlänge | varchar(255) |
| videoadload | Videoanzeigen laden | varchar(255) |
| videoadname | Name der Videoanzeige | varchar(255) |
| videoadplayername | Name der Videoanzeige | varchar(255) |
| videoadpod | Pod für Videoanzeigen | varchar(255) |
| videoadvertiser | Videoverwerter | varchar(255) |
| videoaudioalbum | Video-Audio-Album | varchar(255) |
| videoaudioartist | Video-Audio-Künstler | varchar(255) |
| videoaudioauthor | Video-Audio-Autor | varchar(255) |
| videoaudiolabel | Videoaudiobeschriftung | varchar(255) |
| videoaudiopublisher | Videoband-Herausgeber | varchar(255) |
| videoaudiostation | Audio-Station | varchar(255) |
| videocampaign | Videokampagne | varchar(255) |
| videochannel | Videokanal | varchar(255) |
| videochapter | Videokapitelname | varchar(255) |
| videocontenttype | Videoinhaltstyp. Ist für alle Videoansichten automatisch auf „Video“ gesetzt | varchar(255) |
| videodaypart | Videotagesabschnitt | varchar(255) |
| videoepisode | Videoepisode | varchar(255) |
| videofeedtype | Videofeed-Typ | varchar(255) |
| videogenre | Videogenre | text |
| videolength | Videolänge | varchar(255) |
| videomvpd | Video-MVPD | varchar(255) |
| videoname | Videoname | varchar(255) |
| videonetwork | Videonetzwerk | varchar(255) |
| videopath | Videopfad | varchar(100) |
| videoplayername | Name des Videoplayers | varchar(255) |
| videoqoebitrateaverageevar | Durchschnittliche Bitrate der Videoqualität | varchar(255) |
| videoqoebitratechangecountevar | Videoqualität – Anzahl Änderungen | varchar(255) |
| videoqoebuffercountevar | Videoqualität – Anzahl Puffer | varchar(255) |
| videoqoebuffertimeevar | Pufferzeit für Videoqualität | varchar(255) |
| videoqoedroppedframecountevar | Videoqualität – Anzahl Einzelbildverluste | varchar(255) |
| videoqoeerrorcountevar | Videoqualität – Anzahl Fehler | varchar(255) |
| videoqoeexternalerrors | Externe Fehler in Videoqualität | text |
| videoqoeplayersdkerrors | SDK-Fehler in Videoqualität | text |
| videoqoetimetostartevar | Videoqualität – Startzeitpunkt | varchar(255) |
| videoseason | Videosaison | varchar(255) |
| videosegment | Videosegment | varchar(255) |
| videoshow | Videoshow | varchar(255) |
| videoshowtype | Videoanzeigetyp | varchar(255) |
| videostreamtype | Videostream-Typ | varchar(255) |
| visid_high | Wird zusammen mit visid_low zur eindeutigen Identifizierung eines Besuchs verwendet | bigint unsigned |
| visid_low | Wird zusammen mit visid_high zur eindeutigen Identifizierung eines Besuchs verwendet | bigint unsigned |
| visid_new | Flag, das anzeigt, ob der Treffer eine neu generierte Besucher-ID enthält | char(1) |
| visid_timestamp | Wurde die Besucher-ID neu generiert, wird der Zeitstempel (in Unix-Zeit) der Generierung der Besucher-ID bereitgestellt. | int |
| visid_type | Numerische ID, die angibt, welche Methode zur Identifizierung des Besuchs verwendet wurde <br>0: Benutzerspezifische Besucher-ID <br>1: IP- und Benutzeragenten-Fallback <br>2: HTTP Mobile Subscriber Header <br>3: Alter Cookie-Wert (s_vi) <br>4: Ausweichcookie-Wert (s_fid) <br>5: Identitätsdienst | tinyint unsigniert |
| visit_keywords | Variable, die in der Dimension „Suchbegriff“ verwendet wird Diese Spalte verwendet eine nicht standardmäßige Zeichenbeschränkung, um der von Adobe verwendeten Back-End-Logik Rechnung zu tragen. | varchar(244) |
| visit_num | Variable, die in der Dimension „Besuchsnummer“ verwendet wird Beginnt bei 1 und erhöht sich bei jedem neuen Besuch eines Besuchers | int unsigned |
| visit_page_num | Variable, die in Dimension „Treffertiefe“ verwendet wird Wird für jeden vom Benutzer generierten Treffer um 1 erhöht Setzt jeden Besuch zurück | int unsigned |
| visit_ref_domain | Basiert auf der Spalte visit_referrer Die allererste verweisende Domäne des Besuchs | varchar(100) |
| visit_ref_type | Numerische ID des Typs der verweisenden Stelle der ersten verweisenden Stelle des Besuchs Verwendet die Suchtabelle referrer_type.tsv | tinyint unsigniert |
| visit_referrer | Die erste verweisende Stelle des Besuchs | varchar(255) |
| visit_search_engine | Numerische ID der ersten Suchmaschine des Besuchs Verwendet die Suchtabelle search_engines.tsv | smallint unsigned |
| visit_start_page_url | Die erste URL des Besuchs | varchar(255) |
| visit_start_pagename | Der Name der Seite, die zuerst besucht wurde. | varchar(100) |
| „visit_start_time_gmt“ | Zeitstempel (in Unix-Zeit) des ersten Treffers des Besuchs | int |
| weekly_visitor | Flag zur Bestimmung, ob der Treffer ein neuer wöchentlicher Besucher ist | tinyint unsigniert |
| yearly_visitor | Flag zur Bestimmung, ob der Treffer ein neuer jährlicher Besucher ist | tinyint unsigniert |
| zip | Wird zum Füllen der Dimension „Postleitzahl“ verwendet | varchar(50) |

## Leere Spalten

Die folgende Liste von Spalten wird nicht verwendet und enthält keine Daten:

* mobileacquisitionKlicks
* mobileactioninapptime
* mobileactiontotaltime
* mobileappperformance-betroffeneBenutzer
* mobileappperformanceAppid<span>.</span>app-perf-app-name
* mobileappperformanceAppid<span>.</span>app-perf-platform
* mobileappperformanceECRashes
* mobileappperformanceCrashid<span>.</span>app-perf-crash-name
* mobileappperformanceEloads
* mobileappstoreavgrating
* mobileappstoredownloads
* mobileappstoreinappRevenue
* mobileappstoreinheit
* mobileappstoreobjectid<span>.</span>app-store-user
* mobileappstoreobjectid<span>.</span>application-name
* mobileappstoreobjectid<span>.</span>application-version
* mobileappstoreobjectid<span>.</span>appstore-name
* mobileappstoreobjectid<span>.</span>category-name
* mobileappstoreobjectid<span>.</span>country-name
* mobileappstoreobjectid<span>.</span>Gerätehersteller
* mobileappstoreobjectid<span>.</span>device-name
* mobileappstoreobjectid<span>.</span>in-app-name
* mobileappstoreobjectid<span>.</span>platform-name-version
* mobileappstoreobjectid<span>.</span>rank-category-type
* mobileappstoreobjectid<span>.</span>region-name
* mobileappstoreobjectid<span>.</span>review-comment
* mobileappstoreobjectid<span>.</span>review-title
* mobileappstoreoneoffUmsatz
* mobileappstoreoneoffroyalties
* mobileappstorepurchases
* mobileappstorerank
* mobileappstorerankdivisor
* mobileappstore
* mobileappstoreratingdivisor
* mobileavgspräsessionlength
* mobilecrashes
* mobilecrashrate
* mobileyengagedusers
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
* mobilerelaunchcampaign trackingcode<span><span>.</span></span>name
* mobileupgrades
* socialaveragesentiment
* socialaveragesentiment (nicht mehr unterstützt)
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
* videoautorisiert
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
* videouniquetimeplay
