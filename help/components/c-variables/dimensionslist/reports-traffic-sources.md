---
description: Zeigt Informationen zu den Stellen im Web an, die Traffic zu Ihrer Site lenken. Sie sehen, von welchen Suchmaschinen und Websites außerhalb Ihrer Domain Besucher zu Ihrer Website geleitet werden.
seo-description: Zeigt Informationen zu den Stellen im Web an, die Traffic zu Ihrer Site lenken. Sie sehen, von welchen Suchmaschinen und Websites außerhalb Ihrer Domain Besucher zu Ihrer Website geleitet werden.
seo-title: Traffic-Quellen
solution: Analytics
title: Traffic-Quellen
topic: Berichte
uuid: 34ab8797-7a3e-43fd-afb2-4335869661b8
translation-type: tm+mt
source-git-commit: debfeb513ec40de9323485006e9ed8459f75a586

---


# Traffic-Quellen

Zeigt Informationen zu den Stellen im Web an, die Traffic zu Ihrer Site lenken. Sie sehen, von welchen Suchmaschinen und Websites außerhalb Ihrer Domain Besucher zu Ihrer Website geleitet werden.

## Traffic-Quellen {#topic_6718F8EFD5984DC5839B9E8F6CC45EDA}

Zeigt Informationen zu den Stellen im Web an, die Traffic zu Ihrer Site lenken. Sie sehen, von welchen Suchmaschinen und Websites außerhalb Ihrer Domain Besucher zu Ihrer Website geleitet werden.

Diese Berichte lassen sich in drei Basiskategorien unterteilen:

* Suchkeywords
* Suchmaschinen
* Referrer und Referrerdomänen

### Suchbegriffe - Alle, Gebührenpflichtige oder Kostenlose

Zeigt eine Auflistung der einzelnen Keywords an, die bei der Suche nach Ihrer Site eingesetzt wurden. Sie können die Liste nach Seitenansichten oder Suchkeywords ordnen, indem Sie oberhalb der Auflistung auf die Spaltenüberschrift klicken. Klicken Sie auf die Lupe neben dem Keyword, um den Suchergebnisbildschirm Ihrer Site anzuzeigan.

### Suchmaschinen – alle, Gebührenpflichtig oder kostenlos

Zeigt, welche Suchmaschinen verwendet werden, um Ihre Webseite zu finden. Das Diagramm zeigt Ihnen die verwendeten Suchmaschinen in Prozentwerten an.

**Rangordnung aller Suchseiten**

Zeigt den Rang, den Ihre Site unter allen Ergebnissen der Suchvorgänge Ihres Besuchers einnimmt, einschließlich der Rangdaten für gebührenpflichtige und kostenlose Suchen.

Beispielsweise kann ein Benutzer, der von einer Suchmaschine zu Ihrer Site gelangte, Sie auf der dritten von hundert Ergebnisseiten gefunden haben. So können Sie Suchmaschineneinsätze schnell sehen und optimieren. Daten für diesen Bericht können für alle Zeiträume außer „stündlich“ angezeigt werden.

### Verweisende Domänen und verweisende Stellen

**Referrerdomänen**

Zeigt die Domänen an, die jene Kunden an Sie verwiesen, die die Erfolgsmetrik Ihrer Site am meisten beeinflusst haben. Referrer lassen sich zwei Hauptkategorien zuweisen: Domänen und URLs. Domänen verweisen auf den Domänenamen und werden als Ausgangsdomäne ohne Abfragezeichenfolge oder Unterverzeichnisse angezeigt. URLs enthalten den Ausgangsdomänenamen sowie eventuell vorhandene Abfragezeichenfolgen oder Unterverzeichnisse.

**Ursprünglich Referrerdomänen**

Zeigt die ursprünglich verweisenden Stellen an, die die Kunden zu Ihrer Site führten. Kunden können Ihre Site mehrmals besuchen und für jeden Besuch einen anderen Referrer verwenden.

Dieser Bericht ist sehr hilfreich, um zu erfahren, von wo die Kunden beim ersten Besuch Ihrer Site verwiesen wurden. Auf diese Weise können Sie sehen, ob die Kunden weiterhin dieselbe verweisende Stelle verwenden, und Muster erkennen, wie Kunden zu Ihrer Site verwiesen werden. Sie können die Anzahl der Besucher anzeigen, die von einer ursprünglichen verweisenden Stelle generiert wurden, oder feststellen, für wie viel Umsatz jede ursprüngliche verweisende Stelle verantwortlich war. Berichte der verweisenden Stelle können jedes Mal gefüllt werden, wenn ein Besucher Ihre Site aufsucht, auch wenn der Besucher während einer Sitzung mehrmals zur Site kommt (bevor der Besuch abläuft).

**Verweisende Stellen**

Zeigt an, wo Ihre Besucher herkommen, bevor sie zu Ihrer Site gelangten, welche Methoden Ihre Besucher zum Suchen Ihrer Website verwenden und wie viele Besuche Ihrer Site von diesen verweisenden Stellen stammen.

Wenn beispielsweise ein Besucher auf Site A auf einen Link klickt und zu Ihrer Seite gelangt, ist Site A der Referrer, falls diese nicht als Teil Ihrer Domäne definiert ist. Während der Implementierung hilft Ihnen Ihr Implementierungsberater bei der Definition der Domänen und URLs, die Teil Ihrer Website sind. (Dieser Vorgang kann auch nach der Implementierung durchgeführt werden.) Alle Domänen oder URLs, die nicht Bestandteil der definierten Domänen und URLs sind, gelten als Referrer.

Wenn Webseiten A und B dem Filter für interne URLs hinzugefügt werden, Webseite C jedoch nicht, gilt Webseite C als Referrer.

Siehe [Interne URL-Filter](/help/admin/admin/internal-URL-filter-admin.md)

>[!NOTE]
>
>Analytics records a referring domain as an email when visitors click an emailed message link containing the protocol `imap://` or `mail://` and arrive at your site.
>
>For example, anything coming from  https://mail.yahoo.com</code> is not counted as an email referrer because the protocol is `https://`. E-Mails von Outlook werden in der `Typed/ Bookmarked` Zeile aufgeführt. Jeder Referrer mit einem HTTP-Protokoll, bei dem die Domäne eine bekannte Suchmaschine ist, wird in der `Search Engine` Zeile gemeldet.

**Referrertypen**

Wenn Sie die Referrer bei jedem Besuch verfolgen und aufzeichnen, können Sie feststellen, wie Ihre Besucher bei jedem Besuch zu Ihrer Site gefunden haben. In der folgenden Liste sind die verschiedenen Arten von verweisenden Stellen definiert.

* Verweisende Festplatten werden aufgezeichnet, wenn Besucher auf einen Link in einem HTML-Dokument auf ihrer eigenen Festplatte klicken und daraufhin zu Ihrer Website gelangen.
* Andere verweisende Websites werden aufgezeichnet, wenn Besucher auf einen Link auf einer Seite einer anderen Website klicken (die nicht Bestandteil Ihrer Website ist) und daraufhin zu Ihrer Website gelangen.
* Verweisende Suchmaschinen werden aufgezeichnet, wenn Besucher eine Suchmaschine verwenden, um auf Ihre Website zuzugreifen. * Referrer in Form von Eingaben/Lesezeichen werden verzeichnet, wenn Besucher die URL Ihrer Website direkt in ihren Browser eingeben oder über Lesezeichen auf Ihre Site zugreifen.
