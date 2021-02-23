---
description: Entdecken Sie alles, was Sie mit Advertising Analytics tun können, in dieser Anleitung, einschließlich der erforderlichen Berechtigungen und verfügbaren Dimensionen und Metriken.
title: Ein Leitfaden für Advertising Analytics
translation-type: tm+mt
source-git-commit: c588087b949093152435967f62e43758e9e86208
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 97%

---


# Ein Leitfaden zu Advertising Analytics

Mit Advertising Analytics können Sie alle Paid Search-Daten aus Google und Bing zentral in Adobe Analytics anzeigen. Zuvor mussten Sie Daten zu Google AdWords/DFA oder Microsoft Bing Ads in Adobe Advertising Cloud (AMO) oder in Google/Bing anzeigen. Sie erhalten in Adobe Analytics folgende Daten: Impressionen, Klicks, Kosten, Qualitätsbewertung und durchschnittliche Position direkt aus Suchmaschinen sowie AMO-ID-Instanzen (Klickinstanzen).

>[!NOTE]
>
>Yahoo Gemini wurde am 31. März 2019 von Microsoft Bing übernommen. Daher ist die Anzeigen-Kontenoption „Yahoo Gemini“ nicht mehr verfügbar.

Indem Sie die Daten aus diesen Suchmaschinen in Adobe Analytics zusammenführen, können Sie sie mit Analysis Workspace zentral analysieren. Neu: [Paid Search-Performance](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-report-ad-data-an.md)-Vorlage in Analysis Workspace vereinfacht die Analyse.

![](assets/aa_aw.png)

Diese Integration zielt auf folgende Zielgruppen ab:

* **Analysten**, die Performance-Berichte für den Paid Search-Marketer erfassen müssen.
* **Paid Search-Marketer**, die folgende Fragen beantworten müssen: Wie viel Traffic sende ich an unsere Site bzw. konvertieren unsere Kunden? Welche meiner Werbekampagnen sind kosteneffektiv?

## Voraussetzungen {#section_C25E0CA3474C4EDEAEAA9A5B8AAC9299}

* Advertising Analytics steht nur für die Adobe Analytics-SKUs [Select](https://www.adobe.com/de/data-analytics-cloud/analytics/select.html), [Prime](https://www.adobe.com/de/data-analytics-cloud/analytics/prime.html) und [Ultimate](https://www.adobe.com/de/data-analytics-cloud/analytics/ultimate.html) zur Verfügung.

* Diese Funktion steht auch Kunden ohne Advertising Cloud und AMO zur Verfügung.
* Sie müssen Adobe Analytics-Administrator sein, um auf Advertising Analytics zugreifen zu können. Daraufhin können Sie auch Nicht-Administratoren [Zugriffsberechtigungen erteilen](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369).
* Sämtliche Analytics Report Suites, in denen Sie Google- oder Bing-Suchdaten anzeigen möchten, müssen [Ihrer Experience Cloud-Organisation zugeordnet](https://docs.adobe.com/content/help/de-DE/core-services/interface/about-core-services/report-suite-mapping.html) sein.
* Für jede Report Suite, in der Sie Google- oder Bing-Suchdaten anzeigen möchten, müssen Sie [die betreffenden Report Suites für Advertising Analytics aktivieren](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md) (**[!UICONTROL Admin]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Advertising Analytics-Konfiguration]**).

* Sie benötigen die Anmeldedaten eines Benutzers mit Bearbeitungsberechtigungen für die Suchkonten, die Sie in Adobe Analytics integrieren möchten wie z. B. Google-Konto-ID und -Passwort.
* Bei Bing Ads benötigen Sie darüber hinaus die Bing-Kunden-ID.
* Wenn Sie Internet Explorer 11 (oder niedriger) verwenden, können Sie für keine der drei Suchmaschinen [ein Werbekonto einrichten](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md). Verwenden Sie stattdessen einen anderen Webbrowser.

## Advertising Analytics-Berechtigungen {#section_FCC58EB635954A32990D4E67B52B4369}

Analytics umfasst zwei Berechtigungen, die Analytics-Administratoren automatisch zugewiesen werden. Administratoren können diese Berechtigungen dann an andere Benutzer weitergeben.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Berechtigung </th> 
   <th colname="col2" class="entry"> Definition </th> 
   <th colname="col3" class="entry"> Berechtigung in Adobe Analytics gewähren </th> 
   <th colname="col4" class="entry"> Berechtigung bei Anmeldung in Adobe Experience Cloud gewähren </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Advertising Analytics-Verwaltung </p> </td> 
   <td colname="col2"> <p>Ermöglicht Nutzern die Einrichtung, Bearbeitung und Anzeige von Werbesuchkonten. </p> </td> 
   <td colname="col3"><span class="ignoretag"><span class="uicontrol"> Admin</span> &gt; <span class="uicontrol">Benutzerverwaltung</span> &gt; <span class="uicontrol">Gruppen</span> &gt; <span class="uicontrol">Zugriff auf alle Report Suites bearbeiten</span> &gt; <span class="uicontrol">Analytics-Tools anpassen</span> &gt; <span class="uicontrol">Advertising Analytics-Verwaltung</span></span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> Anmeldung bei adminconsole.adobe.com</span> &gt; <span class="uicontrol">Produkte</span> &gt; <span class="uicontrol">Produktprofil</span> &gt; <span class="uicontrol">Registerkarte „Berechtigungen“</span> &gt; <span class="uicontrol">Analytics-Tools</span> &gt; <span class="uicontrol">Advertising Analytics-Verwaltung</span></span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Advertising Analytics-Konfiguration </p> </td> 
   <td colname="col2"> <p>Ermöglicht Benutzern die Konfiguration von Report Suites, die für Advertising Analytics bereitgestellt werden sollen. </p> </td> 
   <td colname="col3"><span class="ignoretag"><span class="uicontrol"> Admin</span> &gt; <span class="uicontrol">Benutzerverwaltung</span> &gt; <span class="uicontrol">Gruppen</span> &gt; <span class="uicontrol">Zugriff auf alle Report Suites bearbeiten</span> &gt; <span class="uicontrol">Report Suite-Tools anpassen</span> &gt; <span class="uicontrol">Advertising Analytics-Konfiguration</span></span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> Anmeldung bei adminconsole.adobe.com</span> &gt; <span class="uicontrol">Produkte</span> &gt; <span class="uicontrol">Produktprofil</span> &gt; <span class="uicontrol">Registerkarte „Berechtigungen“</span> &gt; <span class="uicontrol">Report Suite-Tools</span> &gt; <span class="uicontrol">Advertising Analytics-Konfiguration</span></span> </td> 
  </tr> 
 </tbody> 
</table>

## Advertising Analytics-Dimensionen und -Metriken {#section_C0DF4A08EA9E46ADABE9E465AFC11E32}

Advertising Analytics fügt folgende Dimensionen und Metriken zu Analysis Workspace, Reports &amp; Analytics, Report Builder und Analytics-Reporting-API hinzu.

**Dimensionen**

>[!IMPORTANT]
>
>Diese Integration erstellt eine neue Gruppe von Dimensionen mithilfe der Klassifizierungen der AMO-ID-Variablen. Diese neuen Dimensionen wirken sich nicht auf bestehende Marketingkanäle oder Dimensionen von Kampagnen-Tracking-Variablen aus. Die AMO-ID wird mit einem Besucherprofil verknüpft, wenn der Besucher über eine Paid Search-Werbeanzeige zur Site gelangt. Deshalb können Sie die AMO-Dimensionen nutzen, um sowohl die von dieser Integration bereitgestellten AMO-Metriken als auch vom Benutzer erfasste Daten (Besuche, Besucher, Seitenaufrufe, Absprungrate, Bestellungen, Umsatz, Kundenereignisse usw.) aufzuschlüsseln. Beim Reporting zu anderen lokalen Metriken können sie auch nach anderen Dimensionen aufgeschlüsselt werden.
>
>Die Klassifizierungen für diese Metriken werden täglich aktualisiert. Wenn Sie also Änderungen an Metadaten in einer Suchmaschine vornehmen, treten diese möglicherweise erst am folgenden Tag in Kraft, nachdem die Klassifizierungen aktualisiert wurden.

| Name der Classification (Dimension) | Definition |
|--- |--- |
| Keywordübereinstimmungstyp (AMO-ID) | Der Keyword-Übereinstimmungstyp. Mögliche Werte lauten in der Regel „Weit gefasst“, „Wortgruppe“, „Exakt“ bzw. kein Wert, wenn die Anzeigenart nicht über einen Übereinstimmungstyp verfügt. |
| Anzeigenplattform (AMO-ID) | Der Name der Suchmaschine. Die Werte können Google AdWords oder Microsoft Bing Ads enthalten. |
| Konto (AMO-ID) | Der Name des Suchmaschinenkontos, das verfolgt wird. |
| Kampagne (AMO-ID) | Der Name der Kampagne in Ihrem Suchmaschinenkonto. |
| Anzeigengruppe (AMO-ID) | Der Name der Anzeigengruppe in Ihren Suchmaschinen-Kampagnen. |
| Anzeige (AMO-ID) | Der Anzeigentitel und die Anzeigenbeschreibung Ihrer Werbeanzeige. |
| Keyword (AMO-ID) | Der Keywordwert aus Ihrem Suchmaschinenkonto. |
| Übereinstimmungstyp (AMO-ID) | Der Ihrem Keyword zugewiesene Keyword-Übereinstimmungstyp. Mögliche Werte lauten in der Regel „Weit gefasst“, „Wortgruppe“, „Exakt“ bzw. kein Wert, wenn die Anzeigenart nicht über einen Übereinstimmungstyp verfügt. |
| Anzeigenart (AMO-ID) | Der Typ der verarbeiteten Anzeige, normalerweise „Textanzeige“. |
| Anzeigentitel (AMO-ID) | Das in Ihrer Werbeanzeige verwendete Titelobjekt. |
| Anzeigenbeschreibung (AMO-ID) | Die in Ihrer Werbeanzeige verwendete Anzeigenbeschreibung. |
| Werbeanzeigen-URL (AMO-ID) | Die in Ihrer Werbeanzeige verwendete Werbeanzeigen-URL. |
| Anzeigenziel-URL (AMO-ID) | Die Ihrer Werbeanzeige zugewiesene Landingpage-URL oder endgültige URL. |
| Netzwerk (AMO-ID) | Das Netzwerk, auf dem die Werbeanzeige ausgeliefert wird. Bei Advertising Analytics lautet dieser Wert immer „Suche“. |
| Platzierung (AMO-ID) | Die Website der verwalteten Platzierung (bei Content-Netzwerken). Diese Dimension wird nur bei verwalteten Platzierungen verwendet. |
| Produktziel (AMO-ID) | Der bei PLA-Anzeigen verwendete Name des Produktziels (nicht das tatsächlich erworbene Produkt). |
| Optimierung (AMO-ID) | Dies wird von Advertising Analytics nicht verwendet. Es wird nur von Advertising Cloud-Kunden verwendet. |
| Gerät (AMO-ID) | Derzeit nicht verwendet. Platzhalter für potenzielle zukünftige Produktoptimierungen am jeweiligen Zielgerätetyp (z. B. Mobilgerät, Desktop) einer Werbeanzeige (nicht das tatsächliche Gerät des Besuchers). |

**Metriken**

>[!IMPORTANT]
>
>Bei den von Advertising Analytics bereitgestellten Metriken (siehe unten) handelt es sich um Zusammenfassungsdaten aus den Suchmaschinen. Sie sind nicht mit den Analytics-Besucherprofilen verbunden. Sie sind nur mit der AMO-ID-Variablen und den zugehörigen Classification-Dimensionen verknüpft. Deshalb sollten sie nicht zu Berichten abseits der Dimensionen/Segmente hinzugefügt werden, die auf den AMO-ID-Dimensionen basieren. In einem solchen Fall zeigt Analytics nur Nullen für die Daten an. Sie können sie mit anderen Metriken zu berechneten Metriken hinzufügen, jedoch sollte die entsprechende berechnete Metrik nur nach den AMO-ID-Dimensionen aufgeschlüsselt werden.
>
>Bei diesen Metriken handelt es sich um täglich abgerufene Daten. Für den aktuellen Tag liegen also keine Daten vor. Sie sollten nicht mit einem Zeitabstand von unter einem Tag zu Berichten hinzugefügt werden.
>
>Es gibt eine Metrik zu AMO-ID-Instanzen, die festgelegt wird, wenn die AMO-ID auf einer Landingpage festgelegt wird (also bei einem Clickthrough). Diese Metrik wird in Echtzeit mit dem Landingpage-Aufruf erfasst und ist für Aufschlüsselungen mit anderen auf der Landingpage festgelegten Dimensionen verfügbar.

| Kennzahlname | Definition |
|--- |--- |
| AMO-Impressionen | Die Anzahl der Werbeimpressionen gemäß den Daten der Suchmaschine. |
| AMO-Klicks | Die Anzahl der Klicks gemäß den Daten der Suchmaschine. |
| AMO-Kosten | Die Kosten pro Keyword/Werbeanzeige gemäß den Daten der Suchmaschine. |
| Durchschn. Pos. | Eine berechnete Metrik, die die durchschnittliche Position der Werbeanzeigen gemäß den Daten der Suchmaschine angibt. |
| Durchschnittl. Qualitätsbewertung | Eine berechnete Metrik, die die durchschnittliche Qualitätsbewertung gemäß den Daten der Suchmaschine angibt. |
