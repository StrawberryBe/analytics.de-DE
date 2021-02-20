---
title: Fehlerbehebung bei Datenspitzen und Datenrückgängen
description: Informieren Sie sich über mögliche Gründe, warum Sie in Trend-Berichten dramatische Zu- oder Abnahmen feststellen können.
translation-type: tm+mt
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 100%

---


# Fehlerbehebung bei Datenspitzen und Datenrückgängen

Da Ihre Website Daten sammelt, kann es zahlreiche externe Faktoren geben, die sich auf die Datensammlung oder die Berichterstellung auswirken können. Im Folgenden finden Sie eine Liste potenzieller Erklärungen, weshalb bestimmte Variablen oder der allgemeine Traffic deutlich zu- oder abnimmt.

Während Sie die Ursache ermitteln und sich auf eine Lösung zubewegen, können Sie die Auswirkungen des Ereignisses auf Ihre Daten abschätzen und bestimmen, wie Sie vorgehen möchten. Weitere Informationen finden Sie auf der [Übersichtsseite](overview.md).

## Traffic-Rückgänge

Traffic-Rückgänge werden in zwei Abschnitte kategorisiert: Teil der Daten und keine Daten.

### Mögliche Ursachen für vollständig fehlende Daten (Nullen in Berichten)

* **Report Suite-Latenz**: Gelegentlich kann es bei einer Report Suite aufgrund einer Reihe von Faktoren zu einer [Latenz](../latency.md) kommen. Viele Latenzprobleme können innerhalb von Stunden behoben werden. Wenden Sie sich bei Problemen mit einer bestimmten Report Suite an die Adobe-Kundenunterstützung.
* **Entfernung der Implementierung**: Manchmal wird die Neuimplementierung von Analytics übersehen, wenn eine Organisation Änderungen an der Implementierung vornimmt oder ihre Site neu strukturiert. Arbeiten Sie mit Entwicklern in Ihrem Unternehmen zusammen, um den Code auf Ihrer Site neu zu implementieren.
* **Problem mit der Analytics-Oberfläche/dem Caching**: In seltenen Fällen enthält der Cache eines Browsers ungültige Daten, die dazu führen, dass alle Berichte Nullen zurückgeben. Löschen Sie die Cookies und den Cache des Browsers, um das Problem zu beheben. Wenn das Löschen Ihrer Cookies/des Cache nicht funktioniert, wenden Sie sich mit dem fehlenden Bericht und dem Datumsbereich an die Kundenunterstützung. Diese kann das Problem duplizieren und zusätzliche Informationen bereitstellen.
* **Verfügbarkeit von Analytics**: Überprüfen Sie [status.adobe.com](https://status.adobe.com/products/1173/de) auf Probleme bei der Datenerfassung oder -verarbeitung.

### Mögliche Ursachen für teilweise fehlende Daten oder verringerten Traffic

* **Änderungen bei der Implementierung**: Überprüfen Sie mit dem [Debugger](/help/implement/validate/debugger.md), ob die gewünschten Dimensionen funktionieren.
* **Verringerter verweisender Traffic**: Wenn eine beliebte Banneranzeige oder ein Hyperlink auf einer anderen Site entfernt wird, kann dies zu einer dramatischen Verringerung des Traffics führen. Zeigen Sie die Dimension [Referrer-Domänen](/help/components/dimensions/referring-domain.md) von bevor bis nach dem Rückgang in der Trend-Ansicht an, um weiter zu recherchieren.
* **Probleme mit der Site-Performance**: Eine fehlerhafte Verteilung des Traffics durch den Lastenausgleich oder Server-Probleme beim Hosten Ihrer Site können zu einem Rückgang in der Analytics-Berichterstellung beitragen. Arbeiten Sie mit dem Team in Ihrem Unternehmen zusammen, das die Integrität und Gesundheit Ihrer Site verwaltet, um mögliche Leistungsprobleme zu untersuchen.
* **Änderungen in der Rangfolge der kostenlosen Suche**: Der Traffic kann potenziell abnehmen, wenn Sie durch eine andere Site bei einigen Keywords in der Rangliste der kostenlosen Suche verdrängt werden. Dieser Rückgang kann besonders deutlich werden, wenn sich Ihre Site nicht mehr auf der ersten Seite der Suchergebnisse befindet. Zeigen Sie die Dimension [Suchmaschinen](/help/components/dimensions/search-engine.md) in der Trend-Ansicht an, um weiter zu recherchieren.
* **Veränderungen bei der PPC-Werbung**: Eine Änderung der Anzeigentitel und -beschreibungen für vorhandene Kampagnen kann sich auf Ihre Qualitätsbewertung auswirken. Eine hohe Qualitätsbewertung bedeutet im Allgemeinen, dass Ihr Suchbegriff Anzeigen in einer höheren Position und zu geringeren Kosten pro Klick auslöst. Zeigen Sie die Dimension [Suchbegriffe - Gebührenpflichtig](/help/components/dimensions/search-keyword.md) in der Trend-Ansicht an, um weiter zu recherchieren.

## Traffic-Spitzen

Traffic-Spitzen werden in zwei Kategorien eingeteilt: nahezu doppelte Daten und andere Ursachen.

### Mögliche Ursachen dafür, dass die erwarteten Daten nahezu oder genau doppelt so hoch sind

* **Mehrere Bildanforderungen innerhalb einer Implementierung**: Wenn Ihre Implementierung mehr als einen [`t()`](/help/implement/vars/functions/t-method.md)-Methodenaufruf pro Seite enthält, werden alle erfassten Daten effektiv verdoppelt. Verwenden Sie den Debugger auf Ihrer Site und achten Sie auf mehrere Bildanforderungen, um Duplikate abzufangen.
* **Doppelte Datenquelldateien hochgeladen**: Wenn Ihr Unternehmen [Datenquellen](/help/import/c-data-sources/datasrc-home.md) verwendet, kann ein Benutzer in Ihrem Unternehmen dieselbe Datei zweimal in Adobe Analytics hochladen. Wenn Sie diesen doppelten Upload durchführen, verdoppeln sich die Daten in der Berichterstellung, was zu einer Traffic-Spitze führt.

### Andere mögliche Ursachen für erhöhten Traffic

* **Spiders oder Bots**: Wenn Sie einen starken plötzlichen Anstieg des Traffics sehen, sollten Sie als Erstes nach einer möglichen Spider oder einem Bot suchen. Die Identifizierung von Bots kann manchmal schwierig sein, da jeder einzelne seine eigene Methode hat, Code auf Ihrer Site auszuführen. Erstellen Sie einen Data Warehouse-Bericht mit IP als Dimension, um festzustellen, welche Adressen den meisten Datenverkehr verursachen. Sie können dann entweder [Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md) oder eine VISTA-Regel verwenden, um Bot-Traffic aus zukünftigen Berichten zu eliminieren.
* **Gestartete Kampagnen**: Marketing-Bemühungen wie E-Mail-Kampagnen oder Suchmaschinenoptimierung können möglicherweise zu einer Traffic-Spitze auf Ihrer Site führen. Zeigen Sie die Dimension [Trackingcode](/help/components/dimensions/tracking-code.md) in der Trend-Ansicht an, um weiter zu recherchieren. Es kann auch hilfreich sein, Ihr Marketing-Team zu kontaktieren, um sicherzustellen, dass die Spitze beabsichtigt war.
* **Umwelt- oder situationsbedingte Gründe**: Wenn ein Feiertag oder ein situationsbedingtes Ereignis aufgetreten ist (ein wichtiges Ereignis, bei dem Ihre Site eine bekannte Ressource ist, oder verbleibende Marketing-Anstrengungen anderer Organisationen), kann der Traffic auf Ihrer Website zunehmen. Es ist schwierig, die genaue Ursache zu ermitteln, da es eine nahezu unbegrenzte Anzahl von situationsbedingten Gründen gibt, aus denen der Traffic zunehmen kann. Diese Ursachen sind jedoch besonders wichtig, damit Ihr Unternehmen sie nutzen und entsprechende Geschäftsentscheidungen treffen kann. Die Dimension [Seite](/help/components/dimensions/page.md) oder [Referrer](/help/components/dimensions/referrer.md) in der Trendansicht anzuzeigen,ist höchstwahrscheinlich der beste Ausgangspunkt für die Ermittlung der Traffic-Quelle.

Wenn keiner der oben genannten Gründe ein potenzieller Grund für einen Anstieg oder Rückgang der Besucherzahlen auf Ihrer Site ist, wenden Sie sich an die Adobe-Kundenunterstützung. Sie kann dabei helfen, die Quelle der Traffic-Spitze oder des Rückgangs zu finden. Weisen Sie den Kundendienstmitarbeiter beim Erstellen des Vorfalls an, wie ein spezieller Bericht erstellt werden kann, der die Traffic-Spitze oder den Rückgang deutlich illustriert.
