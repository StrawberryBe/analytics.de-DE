---
description: Berichte zu Traffic-Quellen verschaffen Ihnen einen umfassenden Einblick in die Interaktion der Besucher mit Ihrer Website.
seo-description: Berichte zu Traffic-Quellen verschaffen Ihnen einen umfassenden Einblick in die Interaktion der Besucher mit Ihrer Website.
seo-title: Berichte zu Traffic-Quellen
solution: Analytics
title: Berichte zu Traffic-Quellen
topic: Ad Hoc Analysis
uuid: 246 afbdc -9 f 7 b -4956-a 44 a-b 7 aad 948 f 392
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Berichte zu Traffic-Quellen

Berichte zu Traffic-Quellen verschaffen Ihnen einen umfassenden Einblick in die Interaktion der Besucher mit Ihrer Website.

## Traffic Sources reports {#concept_0F1772141E1345C5BCF63BE7C544C0CB}

Berichte zu Traffic-Quellen verschaffen Ihnen einen umfassenden Einblick in die Interaktion der Besucher mit Ihrer Website.

Anhand der Berichte zu Traffic-Quellen können Sie:

* kritische Aspekte des Besucherverhaltens analysieren
* Verkehrsmuster beobachten und verstehen
* bevorzugte Site-Inhalte bestimmen
* Besucher nach beliebigen messbaren Kriterien segmentieren

**Allgemeine Persistenz**

Alle Berichtwerte in [!UICONTROL Traffic-Quellen] sind persistent und erhalten die Zuschreibung, bis sie überschrieben werden oder bis der Besuch endet, je nachdem, was zuerst erfolgt. Zuvor waren nur Keywords und Referrerdomänen persistent. Wenn ein Besucher z. B. eine Google-Suche nach      „DVD“ durchführt, was ihn zu Ihrer Site mit einem Kauf von 100 US-Dollar bringt, schreibt der Bericht dem Keyword „DVD“ sowie der Suchmaschine Google 100 US-Dollar gut. This functionality is unalterable, regardless of [!DNL Admin Console] settings.

## Suchkeywords {#concept_071FDCBD0A3B4242BA00744786D1C59C}

Zeigt eine Aufschlüsselung der Keywords für alle, gebührenpflichtige und kostenlose Suchläufe an.

<!-- 

c_reports_search_keyword.xml

 -->

** [!UICONTROL Search Keywords - All] **: Displays a breakdown of each search keyword that has been used to find your site. Sie können die Liste nach Seitenansichten oder Keywords ordnen, indem Sie oberhalb der Auflistung auf die Spaltenüberschrift klicken. Klicken Sie auf die Lupe neben dem Keyword, um den Suchergebnisbildschirm Ihrer Site anzuzeigan.

** [!UICONTROL Search Keywords - Paid] **: Displays a breakdown of each paid search keyword that is used to find your site. Sie können die Liste nach Seitenansichten oder Keywords ordnen, indem Sie oberhalb der Auflistung auf die Spaltenüberschrift klicken. Klicken Sie auf die Lupe neben dem Keyword, um den Suchergebnisbildschirm Ihrer Site anzuzeigan.

** [!UICONTROL Search Keywords - Natural] **: Displays a breakdown of each natural search keyword that is used to find your site. Sie können die Liste nach Seitenansichten oder Keywords ordnen, indem Sie oberhalb der Auflistung auf die Spaltenüberschrift klicken. Klicken Sie auf die Lupe neben dem Keyword, um den Suchergebnisbildschirm Ihrer Site anzuzeigan.

## Suchmaschinen {#concept_351CDE4F5FC44371B6B657064E125134}

Zeigt, welche Suchmaschinen Besucher für alle, gebührenpflichtige oder kostenlose Suchen nutzen.

<!-- 

c_reports_search_engines.xml

 -->

** [!UICONTROL Search Engines - All] **: Displays which search engines that people are using to find your web page. Das Diagramm zeigt Ihnen die verwendeten Suchmaschinen in Prozentwerten an.

** [!UICONTROL Search Engines - Paid] **: Displays which paid-keyword search engines that people are using to find your web page. Das Diagramm zeigt Ihnen die verwendeten Suchmaschinen in Prozentwerten an.

** [!UICONTROL Search Engines - Natural] **: Displays which natural-keyword search engines people are using to find your web page. Das Diagramm zeigt Ihnen die verwendeten Suchmaschinen in Prozentwerten an.

## Referrerdomänen {#concept_804614DF21C14C9FB542451B30F92788}

<!-- 

c_reports_ref_domains.xml

 -->

Zeigt die Domänen an, die jene Kunden an Sie verwiesen, die die Erfolgsmetrik Ihrer Site am meisten beeinflusst haben. Referrer lassen sich zwei Hauptkategorien zuweisen: Domänen und URLs. Domänen verweisen auf den Domänenamen und werden als Ausgangsdomäne ohne Abfragezeichenfolge oder Unterverzeichnisse angezeigt. URLs enthalten den Ausgangsdomänenamen sowie eventuell vorhandene Abfragezeichenfolgen oder Unterverzeichnisse.

## Ursprüngliche Referrerdomänen {#concept_EB18251DF70343169B46BB59543A579A}

<!-- 

c_reports_original_ref_domains.xml

 -->

Zeigt die ursprünglich verweisenden Stellen an, die die Kunden zu Ihrer Site führten. Kunden können Ihre Site mehrmals besuchen und für jeden Besuch eine andere verweisende Stelle verwenden. Dieser Bericht zeigt an, von wo die Kunden beim ersten Besuch Ihrer Site verwiesen wurden. Auf diese Weise können Sie sehen, ob die Kunden weiterhin dieselbe verweisende Stelle verwenden, und Muster erkennen, wie Kunden zu Ihrer Site verwiesen werden. Sie können die Anzahl der Besucher anzeigen, die von einer ursprünglichen verweisenden Stelle generiert wurden, oder feststellen, für wie viel Umsatz jede ursprüngliche verweisende Stelle verantwortlich war. Berichte der verweisenden Stelle können jedes Mal ausgefüllt werden, wenn ein Besucher Ihre Site aufsucht, auch wenn der Besucher während einer Sitzung mehrmals zur Site kommt (bevor der Besuch abläuft).

## Verweisende Stellen {#concept_40CF9C2D10B94E82819BC65A232F05C3}

Zeigt an, wo Ihre Besucher herkommen, bevor sie zu Ihrer Site gelangten, welche Methoden Ihre Besucher zum Suchen Ihrer Website verwenden und wie viele Besuche Ihrer Site von diesen verweisenden Stellen stammen.

<!-- 

c_reports_referrers.xml

 -->

Wenn beispielsweise ein Besucher auf Site A auf einen Link klickt und zu Ihrer Seite gelangt, ist Site A der Referrer, falls diese nicht als Teil Ihrer Domäne definiert ist. Während der Implementierung von „Marketing Reports and Analytics“ kann Ihr Implementierungsberater Ihnen dabei helfen, die Domänen und URLs zu definieren, die Teil Ihrer Website sind. (Diese Änderung kann nach der Implementierung vorgenommen werden.)

Domänen oder URLs, die nicht Bestandteil der definierten Domänen und URLs sind, gelten als Verweisende Stellen. Beispiel: Webseite A und Webseite B werden zum internen URL-Filter hinzugefügt, aber Webseite C nicht. In diesem Fall gilt Webseite C als Referrer.

Weitere Informationen finden Sie in der Hilfe zur [ unter ](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=internal_URL_filter_admin)Interne URL-Filter[!DNL Admin Console].

>[!NOTE]
>
>Marketing reports and analytics records a referring domain as an email when visitors click an emailed message link containing the protocol [!DNL imap://] or [!DNL mail://] and arrive at your site. So würden beispielsweise alle Nachrichten, die von [!DNL https://mail.yahoo.com] kommen, nicht als verweisende E-Mail-Stelle gelten, weil das Protokoll [!DNL https://] :// lautet. E-Mails von Outlook sind in der Zeile „Eingegeben/Mit Lesezeichen versehen“ aufgeführt, während Referrer mit dem HTTP-Protokoll, deren Domäne eine bekannte Suchmaschine ist, in der Zeile „Suchmaschine“ aufgeführt sind.

## Typ der verweisenden Stelle {#concept_689E42D8F96C450DA41C7167C7388198}

Wenn Sie die Referrer bei jedem Besuch verfolgen und aufzeichnen, können Sie feststellen, wie Ihre Besucher bei jedem Besuch zu Ihrer Site gefunden haben.

<!-- 

c_reports_ref_types.xml

 -->

In der folgenden Liste sind die verschiedenen Arten von verweisenden Stellen definiert:

* *Andere verweisende Websites* werden aufgezeichnet, wenn Besucher auf einen Link auf einer Seite einer anderen Website klicken (die nicht Bestandteil Ihrer Website ist) und daraufhin zu Ihrer Website gelangen.
* *Verweisende Suchmaschinen* werden aufgezeichnet, wenn Besucher eine Suchmaschine verwenden, um auf Ihre Website zuzugreifen.
* Verweise des Typs *Eingegeben/Mit Lesezeichen versehen* werden aufgezeichnet

   * wenn ein Besucher über einen anderen als einen Browserlink auf Ihre Website gelangt (beispielsweise in einer E-Mail);
   * wenn ein Besucher die URL Ihrer Website direkt in den Browser eingibt;
   * wenn ein Besucher auf einen HTML-Link auf der eigenen Festplatte klickt;
   * wenn ein Besucher durch Auswahl eines Lesezeichens im Browser auf Ihre Website gelangt;

**Definitionen**

Die folgenden Zeilenelemente werden evtl. bei Ausführung dieses Berichts angezeigt:

**Innerhalb Ihrer Site**: Diese Elemente sind URLs, die von den internen URL-Filtern vergeben werden. Diese Elemente werden nicht als     Instanzen von Referrern gezählt, sind jedoch in den Berichten zu anderen Metriken ersichtlich.

** Kein Javascript**: Es gab kein javascript, sodass der Typ nicht identifiziert werden konnte (unbekannt). Das heißt, dass es keine Informationen zu Referrern von einem Client für einen Browser gibt, der keine Unterstützung von JavaScript meldet. Diese Elemente werden nicht als Instanzen von Referrern gezählt, sind jedoch in den Berichten zu anderen Metriken ersichtlich.

**USENET (Newsgroup)**: Das heißt, dass die URL eines Referrer mit [!DNL news://] :// eingeleitet wurde. Folglich wurde der Link des Referrer in einer USENET-Newsgroup und nicht auf einer Webseite veröffentlicht.

>[!NOTE]
>
>Referrer Type logic matches other traffic sources reports (such as [!UICONTROL Referrers] and [!UICONTROL Referring Domains]). Dadurch sollte das Auftreten der Zeileneinträge Innerhalb Ihrer Website und Kein JavaScript im Bericht zum [!UICONTROL Referrertyp] reduziert oder gänzlich ausgeräumt werden.

