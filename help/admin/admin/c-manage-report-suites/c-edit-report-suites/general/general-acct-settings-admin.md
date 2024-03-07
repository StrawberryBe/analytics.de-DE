---
description: Feldbeschreibungen für die Report Suite „Allgemeine Kontoeinstellungen“ in der Admin-Konsole.
title: Allgemeine Kontoeinstellungen
feature: Admin Tools
uuid: c1ab5c34-2c41-4d12-a706-0e760dff8a95
exl-id: f49babb2-8e26-4cc6-b264-b4d7be93f130
source-git-commit: 914b822aae659d1d0f0b8a98480090ead99e102a
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 82%

---

# Allgemeine Kontoeinstellungen

Feldbeschreibungen für die Report Suite „Allgemeine Kontoeinstellungen“ unter „Admin“.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Allgemeine Kontoeinstellungen]**

Diese Einstellungen umfassen Bearbeitungsoptionen für grundlegende Report-Suite-Funktionen wie Name und Zeitzone.

Im Folgenden finden Sie ein Video zum Konfigurieren der allgemeinen Kontoeinstellungen:

>[!VIDEO](https://video.tv.adobe.com/v/332330/?quality=12)

| Option | Beschreibung |
|--- |--- |
| Website-Titel | Identifiziert die Website. Legen Sie für jede Report Suite einen eindeutigen Site-Titel fest. |
| Basis-URL | Gibt die Hauptwebsite der Report Suite an. Die Basis-URL hat keine Auswirkungen auf die Filterung des Referrers. Verwendung [interne URL-Filter](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md) anstatt. |
| Zeitzone | Dies wirkt sich auf das Datum und die Uhrzeit aus, die mit Ihren Berichtdaten verbunden werden.  Durch das Ändern der Zeitzone bei einer Live-Report Suite ergibt sich entweder eine Spitze oder Lücke in den Berichtdaten. Um die Auswirkungen so gering wie möglich zu halten und keine Daten zu verfälschen, empfiehlt Adobe, die Zeitzonen außerhalb der besonders datenintensiven Zeiten zu ändern.  Wenn Sie beispielsweise um 15 Uhr die Zeitzone von „Central Standard Time“ zu „Pacific Standard Time“ (US-Westküste) ändern, ändert sich die aktuelle Uhrzeit in 13 Uhr. Da die Berichterstellung bereits Daten für 13 Uhr gesammelt hat, kommt es für den Zeitraum zwischen 13 und 15 Uhr zu Traffic-Spitzen.  Wenn Sie umgekehrt um 15 Uhr die Zeitzone von „Central Standard Time“ zu „Eastern Standard Time“ (US-Ostküste) ändern, ändert sich die aktuelle Uhrzeit in 16 Uhr. In diesem Fall werden in den Berichten für den Zeitraum zwischen 15 und 16 Uhr am Tag der Zeitänderung keine Daten angezeigt. |
| Standardseite | Wenn der Bericht [!UICONTROL Bevorzugte Seiten] URL-Adressen statt Seitennamen enthält, verhindert diese Einstellung, dass für eine Webseite mehrere URL-Adressen angegeben werden. Beispielsweise sind die URLs `https://example.com` und `https://example.com/index.html` normalerweise dieselben Seiten. Sie können Standarddateinamen entfernen, damit beide URLs als `https://example.com` angezeigt werden.  Wenn Sie das Feld leer lassen, werden folgende Dateinamen aus den URLs entfernt: index.htm, index.html, index.cgi, index.asp, default.htm, default.html, default.cgi, default.asp, home.htm, home.html, home.cgi und home.asp.  Um das Entfernen von Dateinamen ganz zu deaktivieren, geben Sie einen Wert ein, der in Ihren URLs nicht vorkommt. |
| Letztes Oktett der IP-Adresse durch 0 ersetzen | Wenn diese Option aktiviert ist, wird das letzte Oktett der IP-Adresse durch eine Null ersetzt. Dies geschieht, bevor geo-bezogene Berichte ausgefüllt werden und kann daher die Genauigkeit dieser Berichte beeinträchtigen. |
| IP-Verschleierung | Verwandelt IP-Adressen in nicht erkennbare Zeichenketten, was sie letztendlich aus den Adobe Datenspeichern löscht. Wenn die IP-Verschleierung aktiviert ist, gehen die ursprünglichen IP-Adressen dauerhaft verloren. <br> **Hinweis**: Die IP-Adressen werden überall in Analytics verschleiert, auch im Data Warehouse. Die IP-Einstellung in Target wird jedoch separat gesteuert. Diese Einstellung hat also keine Auswirkung auf Target.<br> Wenn die IP-Verschleierung aktiviert ist, erfolgt die gesamte erforderliche Verarbeitung, also auch die IP-Filterung bzw. der IP-Ausschluss, die Überprüfung von Bot-Regeln und Geosegmentierungssuchen, bevor die IP-Adresse verschleiert wird. Wenn Sie die IP-Verschleierung aktivieren, müssen Sie keine Änderungen vornehmen.<ul><li>Wenn **Deaktiviert** ausgewählt wird, bleibt die IP-Adresse in den Daten.</li><li>Wird **IP-Adresse verschleiern** markiert, wird die IP in zwei Doppelpunkte geändert, gefolgt von einem Hash-Wert (z. B. `::1932023538`).</li><li>Wenn Sie **IP-Adresse entfernen** aktivieren, wird die IP-Adresse nach der Geo-Suche durch `::X.X.X.X` in den Daten ersetzt.</li></ul>**Hinweis**: Diese Einstellung erfordert möglicherweise Änderungen an benutzerdefinierten [Bot-Regeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md) oder [IP-Ausschlüsse](/help/admin/admin/exclude-ip.md).<br> **Hinweis**: Mit dem Web SDK erfasste Daten können IP-Verschleierungen auf das Edge-Netzwerk angewendet werden, über die [Datenstrom-Konfiguration](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#@advanced-options). Wenn die IP-Verschleierung im Edge-Netzwerk angewendet wird, ist sie bereits verschleiert, wenn Analytics erreicht wird. Diese Verschleierung wirkt sich auf Bot-Regeln und Geo-Suchen aus. |
| Transaktions-ID-Speicher | Ermöglicht die Verwendung von [Transaktions-ID](/help/import/data-sources/transactionid.md)-Datenquellen. |
| Data Warehouse aktivieren | Aktiviert die Data Warehouse-Benutzeroberfläche unter „Analytics“ > „Tools“ > „Data Warehouse“. |
| Postleitzahl-Option | Hier können Sie die Postleitzahl angeben, anstatt die von unserer Geo-IP-Suche erzeugten Elemente zu verwenden. |
| Unterstützung von Multi-Byte-Zeichen | Bei der Multi-Byte-Zeichenunterstützung werden Zeichen der Report Suite als UTF-8 gespeichert. Beim Empfang der Daten konvertiert das System die Daten aus dem Zeichensatz der Web-Seite in den UTF-8-Zeichensatz, damit Sie in Ihren Marketing-Berichten eine beliebige Sprache verwenden können. Wenden Sie sich an Ihr Adobe Account Team oder an die Kundenunterstützung, um die Multibytezeichenunterstützung für eine bestehende Report Suite zu ändern. |
| Aktiviert | Gibt an, ob diese Report Suite aktiviert ist oder nicht. |
| Basiswährung | Hier können Sie die [Basiswährung](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/currencycode.html?lang=de) für diese Report Suite angeben. |
| Organisations-ID | Die ID, die Ihrem bereitgestellten Experience Cloud-Unternehmen zugeordnet ist. Diese ID besteht aus einer 24-stelligen alphanumerischen Zeichenfolge gefolgt von @AdobeOrg (erforderlich). |
