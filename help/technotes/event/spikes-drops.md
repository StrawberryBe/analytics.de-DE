---
title: Fehlerbehebung bei Spitzen und Datenabfällen
description: Erfahren Sie, aus welchen Gründen Sie in Trendberichten dramatische Steigerungen oder Rückgänge feststellen können.
translation-type: tm+mt
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 2%

---


# Fehlerbehebung bei Spitzen und Datenabfällen

Da Ihre Website Daten sammelt, kann es zahlreiche externe Faktoren geben, die sich auf die Datensammlung oder die Berichterstellung auswirken können. Im Folgenden finden Sie eine Liste potenzieller Erklärungen, warum bestimmte Variablen oder der Traffic insgesamt drastisch zunehmen oder abnehmen.

Wenn Sie die Ursache bestimmen und eine Auflösung anstreben, können Sie die Auswirkungen des Ereignisses auf Ihre Daten messen und bestimmen, wie Sie fortfahren möchten. See the [overview page](overview.md) for more information.

## Traffic-Drops

Traffic-Drops werden in zwei Abschnitte kategorisiert: partielle Daten und Nulldaten.

### Mögliche Ursachen für vollständig fehlende Daten (Berichte-Nullen)

* **Report Suite-Latenz**: Gelegentlich kann eine Report Suite aufgrund verschiedener Faktoren eine [Latenz](../latency.md) erleben. Viele Latenzprobleme können innerhalb von Stunden behoben werden. Wenden Sie sich bei Problemen mit einer bestimmten Report Suite an den Kundendienst der Adobe.
* **Implementierungsentfernung**: Manchmal wird die Neuimplementierung von Analytics übersehen, wenn eine Organisation Änderungen an der Implementierung vornimmt oder ihre Site umstrukturiert. Arbeiten Sie mit Entwicklern in Ihrem Unternehmen zusammen, um den Code auf Ihrer Site neu zu implementieren.
* **Problem** bei der Analytics-Oberfläche/Zwischenspeicherung: In seltenen Fällen enthält der Cache eines Browsers ungültige Daten, die dazu führen, dass alle Berichte Nullen zurückgeben. Löschen Sie die Cookies und den Cache des Browsers, um das Problem zu beheben. Wenn das Löschen Ihrer Cookies/des Cache nicht funktioniert, wenden Sie sich an den Kundendienst, wenn der Bericht &quot;Fehlende&quot;und der Datumsbereich fehlen. Sie können das Problem Duplikat geben und zusätzliche Informationen bereitstellen.
* **Analytics-Verfügbarkeit**: Überprüfen Sie [status.adobe.com](https://status.adobe.com/products/1173/) auf Probleme bei der Datenerfassung oder -verarbeitung.

### Potenzielle Ursachen für teilweise fehlende Daten oder verminderten Traffic

* **Implementierungsänderungen**: Überprüfen Sie mit dem [Debugger](/help/implement/validate/debugger.md) , ob die gewünschten Dimensionen funktionieren.
* **Verringerter verweisender Traffic**: Wenn eine beliebte Banneranzeige oder ein Hyperlink auf einer anderen Site entfernt wird, kann dies zu einer dramatischen Verringerung des Traffics führen. Trennen Sie die Dimension &quot; [Verweisende Domänen](/help/components/dimensions/referring-domain.md) &quot;von vor und nach dem Dropdown, um weiter zu forschen.
* **Site-Leistungsprobleme**: Eine fehlerhafte Verteilung des Traffics durch Lastenausgleich oder Serverprobleme, die Ihre Site hosten, können zu einer Verringerung des Analytics-Berichte beitragen. Arbeiten Sie mit dem Team in Ihrem Unternehmen zusammen, das die Integrität und Gesundheit Ihrer Site verwaltet, um mögliche Leistungsprobleme zu untersuchen.
* **Änderungen der Rangansicht** der kostenlosen Suche: Der Traffic kann potenziell abnehmen, wenn eine andere Site Ihre kostenlose Suchrangliste für einige Ihrer Suchbegriffe verlässt. Diese Verringerung kann besonders dann deutlich werden, wenn Ihre Site nicht mehr auf der ersten Seite der Suchergebnisse steht. Trennen Sie die [Suchmaschinen](/help/components/dimensions/search-engine.md) -Dimension, um weiter zu recherchieren.
* **Veränderungen bei der PPC-Werbung**: Eine Änderung der Anzeigentitel und -beschreibungen für vorhandene Kampagnen kann sich auf Ihre Qualitätsbewertung auswirken. Eine hohe Qualitätsbewertung bedeutet im Allgemeinen, dass Ihr Suchbegriff Anzeigen in einer höheren Position und zu geringeren Kosten pro Klick auslöst. Trennen Sie die [Suchbegriffe - die gebührenpflichtige](/help/components/dimensions/search-keyword.md) Dimension, um weiter zu forschen.

## Traffic-Spitzen

Traffic-Spitzen werden in zwei Abschnitte eingeteilt: Daten und andere Ursachen in der Nähe der Dublette.

### Mögliche Ursachen für die beinahe oder exakte Dublette der erwarteten Daten

* **Mehrere Bildanforderungen innerhalb einer Implementierung**: Wenn Ihre Implementierung mehr als einen [`t()`](/help/implement/vars/functions/t-method.md) Methodenaufruf pro Seite enthält, werden alle erfassten Daten effektiv Dublette. Verwenden Sie den Debugger auf Ihrer Site und achten Sie darauf, dass mehrere Bildanforderungen Duplikate abfangen.
* **Hochgeladene** Duplikat-Datenquellendateien: Wenn Ihr Unternehmen [Datenquellen](/help/import/c-data-sources/datasrc-home.md)verwendet, kann ein Benutzer in Ihrem Unternehmen dieselbe Datei zweimal nach Adobe Analytics hochladen. Durch das Hochladen dieses Duplikats werden Dubletten effektiv durchgeführt, die Daten in Berichte enthalten, was zu einer Traffic-Spitze führt.

### Andere potenzielle Ursachen für erhöhten Traffic

* **Spiders oder Bots**: Wenn Sie einen starken plötzlichen Anstieg des Traffics sehen, sollten Sie als Erstes die Möglichkeit einer Spider oder Bot suchen. Die Identifizierung von Bots kann manchmal schwierig sein, da jeder einzelne seine eigene Methode hat, Code auf Ihrer Site auszuführen. Erstellen Sie einen Data warehouse-Bericht mit IP als Dimension, um zu sehen, welche Adressen den meisten Traffic verursachen. Sie können dann entweder [Bot-Regeln](/help/admin/admin/bot-removal/bot-rules.md) oder eine VISTA-Regel verwenden, um Bot-Traffic aus zukünftigen Berichten zu eliminieren.
* **Kampagnen** gestartet: Marketingbemühungen wie E-Mail-Kampagnen oder Suchmaschinenoptimierung können möglicherweise zu einer Traffic-Spitze auf Ihrer Site führen. Trennen Sie die [Tracking-Code](/help/components/dimensions/tracking-code.md) -Dimension, um weiter zu forschen. Sie kann auch dazu beitragen, Ihr Marketingteam zu kontaktieren, um sicherzustellen, dass die Spitze beabsichtigt war.
* **Umwelt- oder Indiziengründe**: Wenn ein Ereignis im Urlaub oder in einem Umstand eingetreten ist (ein wichtiges Ereignis, bei dem Ihre Site eine bekannte Ressource ist, oder Restmarketingbemühungen anderer Organisationen), kann der Traffic auf Ihrer Site zunehmen. Die Fehlerbehebung für die genaue Ursache ist schwierig, da es eine nahezu unbegrenzte Anzahl von Umständen gibt, aus denen der Traffic steigen kann. Diese Ursachen sind jedoch besonders wichtig, damit Ihr Unternehmen sie nutzen und entsprechende Geschäftsentscheidungen treffen kann. Die Trendbildung der Dimension &quot; [Seite](/help/components/dimensions/page.md) &quot;oder &quot; [Werber](/help/components/dimensions/referrer.md) &quot;ist höchstwahrscheinlich der beste Ort für Beginn, um die Traffic-Quelle zu bestimmen.

Wenn keiner der oben genannten Gründe potenzielle Ursachen für erhöhten oder verminderten Traffic auf Ihrer Site ist, wenden Sie sich an die Kundenunterstützung der Adobe. Sie können dabei helfen, die Quelle der Traffic-Spitze oder des Abfalls zu finden. Weisen Sie den Kundendienstmitarbeiter beim Erstellen des Vorfalls an, einen bestimmten Bericht neu zu erstellen, der die Spitze bzw. den Absturz deutlich illustriert.
