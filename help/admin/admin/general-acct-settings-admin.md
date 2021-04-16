---
description: Feldbeschreibungen für die Report Suite „Allgemeine Kontoeinstellungen“ in der Admin-Konsole.
title: Allgemeine Kontoeinstellungen
feature: Admin Tools
uuid: c1ab5c34-2c41-4d12-a706-0e760dff8a95
exl-id: f49babb2-8e26-4cc6-b264-b4d7be93f130
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 88%

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
| Letztes Oktett der IP-Adresse durch 0 ersetzen | Das letzte Oktett wird entfernt, bevor eine Verarbeitung für den Treffer durchgeführt wird, einschließlich vor der IP-Filterung/dem Ausschluss, bevor Bot-Regeln überprüft werden, bevor Geosegmentation-Suchen usw. durchgeführt werden. Dabei wird das letzte Oktett mit „0“ ersetzt und die Regeln für den IP-Ausschluss sollten angepasst werden, um IP-Adressen mit einer Null am Ende zu berücksichtigen. Übereinstimmung * sollte mit 0 übereinstimmen. Die IP-Adresse 11.22.33.44 wird beispielsweise auf 11.22.33.0 geändert. Die Geosegmentierungs-Daten sind dann nicht ganz so präzise wie bei Verwendung der vollständigen IP-Adresse. Insbesondere wird die Genauigkeit der Stadt stärker betroffen sein als die Genauigkeit von Land oder Region. Sowohl Bot-Regeln als auch VISTA-Regeln sind davon betroffen, da die vollständige IP-Adresse nicht mehr zur Verfügung steht. Außerdem wirkt sich diese Einstellung auf IP-basierte Verarbeitungsregeln aus, einschließlich der Marketingkanalregeln und der Verarbeitungsregeln für die Report Suite.  <br> **Hinweis**: Diese Einstellung ist standardmäßig für alle neuen Report Suites aktiviert, die ab Januar 2019 im London Data Center erstellt wurden – jedoch nur dann, wenn die Einstellungen für diese Report Suites aus einer Vorlage kopiert werden, die in der Admin Console aufgeführt ist. Report Suites mit Einstellungen, die aus anderen Report Suites dupliziert wurden, erben alle Einstellungen der ausgewählten Report Suite. |
| IP-Verschleierung | Verwandelt IP-Adressen in nicht erkennbare Zeichenketten, was sie letztendlich aus den Adobe Datenspeichern löscht. Wenn die IP-Verschleierung aktiviert ist, geht die ursprüngliche IP-Adresse dauerhaft verloren.   <br> **Hinweis**: Die IP-Adressen werden überall in Analytics verschleiert, auch im Data Warehouse. Die IP-Einstellung in Target wird jedoch separat gesteuert. Diese Einstellung hat also keine Auswirkung auf Target.<br> Wenn die IP-Verschleierung aktiviert ist, werden alle erforderlichen Verarbeitungen durchgeführt, einschließlich IP-Filterung/Ausschluss, Bot-Regeln und Geosegmentation-Suchen, bevor die IP-Adresse verschleiert wird. Sie müssen nichts ändern, wenn Sie IP-Verschleierung aktivieren.<ul><li>Wenn **Deaktiviert** ausgewählt wird, bleibt die IP-Adresse in den Daten.</li><li>Wenn Sie **IP-Adresse verschleiern** aktivieren, wird die IP in zwei Doppelpunkte gefolgt von einem Hash-Wert (z. B. `::1932023538`) geändert.</li><li>Wenn Sie **IP-Adresse entfernen**`::X.X.X.X` aktivieren, wird die IP-Adresse nach der Geo-Suche in den Daten durch ersetzt.</li></ul>**Hinweis**: Diese Einstellung erfordert möglicherweise Änderungen an benutzerdefinierten [Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md) oder [IP-Ausschlüssen](/help/admin/admin/exclude-ip.md). |
| Transaktions-ID-Speicher | Ermöglicht die Verwendung von [Transaktions-ID](/help/import/c-data-sources/c-datasrc-types/datasrc-transactionid.md)-Datenquellen. |
| Data Warehouse aktivieren | Aktiviert die Data Warehouse-Benutzeroberfläche unter „Analytics“ > „Tools“ > „Data Warehouse“. |
