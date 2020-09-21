---
description: Feldbeschreibungen für die Report Suite „Allgemeine Kontoeinstellungen“ in der Admin-Konsole.
title: Allgemeine Kontoeinstellungen
topic: Admin tools
uuid: c1ab5c34-2c41-4d12-a706-0e760dff8a95
translation-type: tm+mt
source-git-commit: dbcdabdfd53b9d65d72e6269fcd25ac7118586e7
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 100%

---


# Allgemeine Kontoeinstellungen

Feldbeschreibungen für die Report Suite „Allgemeine Kontoeinstellungen“ unter „Admin“.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Allgemeine Kontoeinstellungen]**

Diese Einstellungen umfassen Bearbeitungsoptionen für grundlegende Report Suite-Funktionen wie Name und Zeitzone.

| Option | Beschreibung |
|--- |--- |
| Website-Titel | Identifiziert die Website. Legen Sie für jede Report Suite einen eindeutigen Site-Titel fest. |
| Basis-URL | Gibt die Hauptwebsite der Report Suite an. Die Basis-URL hat keine Auswirkungen auf die Filterung des Referrers. Verwenden Sie stattdessen [interne URL-Filter](/help/admin/admin/internal-url-filter-admin.md). |
| Zeitzone | Dies wirkt sich auf das Datum und die Uhrzeit aus, die mit Ihren Berichtdaten verbunden werden.  Durch das Ändern der Zeitzone bei einer Live-Report Suite ergibt sich entweder eine Spitze oder Lücke in den Berichtdaten. Um die Auswirkungen so gering wie möglich zu halten und keine Daten zu verfälschen, empfiehlt Adobe, die Zeitzonen außerhalb der besonders datenintensiven Zeiten zu ändern.  Wenn Sie beispielsweise um 15 Uhr die Zeitzone von „Central Standard Time“ zu „Pacific Standard Time“ (US-Westküste) ändern, ändert sich die aktuelle Uhrzeit in 13 Uhr. Da die Berichterstellung bereits Daten für 13 Uhr gesammelt hat, kommt es für den Zeitraum zwischen 13 und 15 Uhr zu Traffic-Spitzen.  Wenn Sie umgekehrt um 15 Uhr die Zeitzone von „Central Standard Time“ zu „Eastern Standard Time“ (US-Ostküste) ändern, ändert sich die aktuelle Uhrzeit in 16 Uhr. In diesem Fall werden in den Berichten für den Zeitraum zwischen 15 und 16 Uhr am Tag der Zeitänderung keine Daten angezeigt. |
| Standardseite | Wenn der Bericht [!UICONTROL Bevorzugte Seiten] URL-Adressen statt Seitennamen enthält, verhindert diese Einstellung, dass für eine Webseite mehrere URL-Adressen angegeben werden. Beispielsweise sind die URLs `https://example.com` und `https://example.com/index.html` normalerweise dieselben Seiten. Sie können Standarddateinamen entfernen, damit beide URLs als `https://example.com` angezeigt werden.  Wenn Sie das Feld leer lassen, werden folgende Dateinamen aus den URLs entfernt: index.htm, index.html, index.cgi, index.asp, default.htm, default.html, default.cgi, default.asp, home.htm, home.html, home.cgi und home.asp.  Um das Entfernen von Dateinamen ganz zu deaktivieren, geben Sie einen Wert ein, der in Ihren URLs nicht vorkommt. |
| Letztes Oktett der IP-Adresse durch 0 ersetzen | Das letzte Oktett wird vor der IP-Filterung entfernt. Dabei wird das letzte Oktett mit „0“ ersetzt und die Regeln für den IP-Ausschluss sollten angepasst werden, um IP-Adressen mit einer Null am Ende zu berücksichtigen. Übereinstimmung * sollte mit 0 übereinstimmen. Wenn Sie diese Option auswählen, wird die IP-Adresse geändert, bevor sie verarbeitet wird. Die IP-Adresse 134.123.567.780 wird beispielsweise auf 134.123.567.0 geändert. Die Geosegmentierungs-Daten sind dann nicht ganz so präzise wie bei Verwendung der vollständigen IP-Adresse. Insbesondere wird die Genauigkeit der Stadt stärker betroffen sein als die Genauigkeit von Land oder Region. Sowohl Bot-Regeln als auch VISTA-Regeln sind davon betroffen, da die vollständige IP-Adresse nicht mehr zur Verfügung steht. Außerdem wirkt sich diese Einstellung auf IP-basierte Verarbeitungsregeln aus, einschließlich der Marketingkanalregeln und der Verarbeitungsregeln für die Report Suite.  <br> **Hinweis**: Diese Einstellung ist standardmäßig für alle neuen Report Suites aktiviert, die ab Januar 2019 im London Data Center erstellt wurden – jedoch nur dann, wenn die Einstellungen für diese Report Suites aus einer Vorlage kopiert werden, die in der Admin Console aufgeführt ist. Report Suites mit Einstellungen, die aus anderen Report Suites dupliziert wurden, erben alle Einstellungen der ausgewählten Report Suite. |
| IP-Verschleierung | Verwandelt IP-Adressen in nicht erkennbare Zeichenketten, was sie letztendlich aus den Adobe Datenspeichern löscht. Wenn die IP-Verschleierung aktiviert ist, geht die ursprüngliche IP-Adresse dauerhaft verloren.  <br> **Hinweis**: Die IP-Adressen werden überall in Analytics verschleiert, auch im Data Warehouse. Die IP-Einstellung in Target wird jedoch separat gesteuert. Diese Einstellung hat also keine Auswirkung auf Target.<br> Wenn die IP-Verschleierung aktiviert ist, wird der IP-Ausschluss durchgeführt, bevor die IP verschleiert wird. Kunden müssen also keine Änderungen vornehmen, wenn sie die IP-Verschleierung aktivieren. <br> Wenn **Deaktiviert** ausgewählt wird, bleibt die IP-Adresse in den Daten. <br> Wenn Sie **IP-Adresse verschleiern** aktivieren, wird die IP in einen Hash-Wert geändert (z. B. 234abc6493872038). <br> Wenn Sie **IP-Adresse entfernen** aktivieren, wird die IP-Adresse nach der Geo-Suche in den Daten durch x.x.x.x ersetzt. <br> **Hinweis**: Diese Einstellung erfordert möglicherweise Änderungen an benutzerdefinierten [Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md) oder [IP-Ausschlüssen](/help/admin/admin/exclude-ip.md). |
| Transaktions-ID-Speicher | Ermöglicht die Verwendung von [Transaktions-ID](/help/import/c-data-sources/c-datasrc-types/datasrc-transactionid.md)-Datenquellen. |
| Ad Hoc Analysis aktivieren | Gibt an, ob die betreffende Report Suite in Ad Hoc Analysis als verfügbare Report Suite angezeigt wird. Verwenden Sie diese Einstellung, um einzugrenzen, welche Report Suites als eine Option für Ad Hoc Analysis angezeigt werden. Sie können beispielsweise Ad Hoc Analysis für Entwicklungs- und QA-Report Suites deaktivieren. |
| Data Warehouse aktivieren | Aktiviert die Data Warehouse-Benutzeroberfläche unter „Analytics“ > „Tools“ > „Data Warehouse“. |
