---
description: 'null'
title: Advertising Analytics-Übersicht
uuid: 00e461ff-3e17-4071-818b-93fd1e4b36f1
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Advertising Analytics-Übersicht

Mit Advertising Analytics können Sie alle Paid Search-Daten aus Google und Bing zentral in Adobe Analytics anzeigen. Zuvor mussten Sie Daten zu Google AdWords/DFA oder Microsoft Bing Ads in Adobe Advertising Cloud (AMO) oder in Google/Bing anzeigen. Sie erhalten in Adobe Analytics folgende Daten: Impressionen, Klicks, Kosten, Qualitätsbewertung und durchschnittliche Position direkt aus Suchmaschinen sowie AMO-ID-Instanzen (Klickinstanzen).

>[!NOTE] Yahoo Gemini wurde am 31. März 2019 von Microsoft Bing übernommen. Daher ist die Anzeigen-Kontenoption „Yahoo Gemini“ nicht mehr verfügbar.

Indem Sie die Daten aus diesen Suchmaschinen in Adobe Analytics zusammenführen, können Sie dieselben Daten mithilfe von Analyse Workspace analysieren. A new [Paid Search Performance](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-report-ad-data-an.md) template in Workspace facilitates this analysis.

![](assets/aa_aw.png)

Diese Integration zielt auf folgende Audiencen ab:

* Der **Analyst** , der Leistungsberichte für den gebührenpflichtigen Suchmarketer erfassen muss.
* Der **Marketer** für gebührenpflichtige Suchen beantwortet folgende Fragen: Wie viel Traffic sende ich zu unserer Site und rechnen Kunden um? Was sind meine kosteneffizienten Anzeigen-Kampagnen?

## Voraussetzungen {#section_C25E0CA3474C4EDEAEAA9A5B8AAC9299}

* Advertising Analytics is available for Adobe Analytics [Select](https://www.adobe.com/data-analytics-cloud/analytics/select.html), [Prime](https://www.adobe.com/data-analytics-cloud/analytics/prime.html), and [Ultimate](https://www.adobe.com/data-analytics-cloud/analytics/ultimate.html) SKUs only.

* Diese Funktion ist für Nicht-Advertising Cloud- und Nicht-AMO-Kunden verfügbar.
* Sie müssen Adobe Analytics-Administrator sein, um Zugriff auf Advertising Analytics zu haben. Anschließend können Sie Nicht-Administratoren Zugriffsberechtigungen [gewähren](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369) .
* Sämtliche Analytics Report Suites, in denen Sie Google- oder Bing-Suchdaten anzeigen möchten, müssen [Ihrer Experience Cloud-Organisation zugeordnet](https://marketing.adobe.com/resources/help/de_DE/mcloud/report-suite-mapping.html) sein.
* For any report suite where you want to view Google/Bing search data, you must [enable those report suite/s for Advertising Analytics](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-provision-rs.md) ( **[!UICONTROL Admin]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Advertising Analytics Configuration]**).

* Sie benötigen Anmeldeinformationen für einen Benutzer mit Bearbeitungsberechtigungen für das/die Suchkonto/s, das/die Sie in Adobe Analytics integrieren möchten, z. B. eine Google-Konto-ID und ein Kennwort.
* Bei Bing-Anzeigen benötigen Sie auch die Bing-Kunden-ID.
* If you use Internet Explorer 11 (or earlier), you will not be able to successfully [set up an advertising account](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md) for any of the three search engines. Verwenden Sie stattdessen andere Webbrowser.

## Advertising Analytics-Berechtigungen {#section_FCC58EB635954A32990D4E67B52B4369}

Analytics verfügt über zwei Berechtigungen, die Analytics-Administratoren automatisch zugewiesen werden. Administratoren können diese Berechtigungen dann auch Nichtadministratoren gewähren.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Berechtigung </th> 
   <th colname="col2" class="entry"> Definition </th> 
   <th colname="col3" class="entry"> Berechtigung in Adobe Analytics erteilen </th> 
   <th colname="col4" class="entry"> Berechtigung erteilen, wenn Sie bei Adobe Experience Cloud angemeldet sind </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Advertising Analytics-Verwaltung </p> </td> 
   <td colname="col2"> <p>Ermöglicht Benutzern das Einrichten/Bearbeiten/Ansicht von Anzeigen-Suchkonten. </p> </td> 
   <td colname="col3"><span class="ignoretag"><span class="uicontrol"> Admin</span> &gt; <span class="uicontrol">Benutzerverwaltung</span> &gt; <span class="uicontrol">Gruppen</span> &gt; <span class="uicontrol">Zugriff auf alle Report Suites bearbeiten</span> &gt; <span class="uicontrol">Analytics-Tools anpassen</span> &gt; <span class="uicontrol">Advertising Analytics-Verwaltung</span></span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> Anmeldung bei adminconsole.adobe.com</span> &gt; <span class="uicontrol">Produkte</span> &gt; <span class="uicontrol">Produktprofil</span> &gt; <span class="uicontrol">Registerkarte „Berechtigungen“</span> &gt; <span class="uicontrol">Analytics-Tools</span> &gt; <span class="uicontrol">Advertising Analytics-Verwaltung</span></span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Advertising Analytics-Konfiguration </p> </td> 
   <td colname="col2"> <p>Ermöglicht Benutzern die Konfiguration von Report Suites zur Bereitstellung für Advertising Analytics. </p> </td> 
   <td colname="col3"><span class="ignoretag"><span class="uicontrol"> Admin</span> &gt; <span class="uicontrol">Benutzerverwaltung</span> &gt; <span class="uicontrol">Gruppen</span> &gt; <span class="uicontrol">Zugriff auf alle Report Suites bearbeiten</span> &gt; <span class="uicontrol">Report Suite-Tools anpassen</span> &gt; <span class="uicontrol">Advertising Analytics-Konfiguration</span></span> </td> 
   <td colname="col4"><span class="ignoretag"><span class="uicontrol"> Anmeldung bei adminconsole.adobe.com</span> &gt; <span class="uicontrol">Produkte</span> &gt; <span class="uicontrol">Produktprofil</span> &gt; <span class="uicontrol">Registerkarte „Berechtigungen“</span> &gt; <span class="uicontrol">Report Suite-Tools</span> &gt; <span class="uicontrol">Advertising Analytics-Konfiguration</span></span> </td> 
  </tr> 
 </tbody> 
</table>

## Advertising Analytics-Dimensionen und -Metriken {#section_C0DF4A08EA9E46ADABE9E465AFC11E32}

Advertising Analytics fügt die folgenden Dimensionen und Metriken zum Arbeitsbereich für Analysen, Reports &amp; Analysen, ReportBuilder und der Analytics Berichte-API hinzu.

**Dimensionen**

>[!IMPORTANT]
>
>Diese Integration erstellt eine neue Gruppe von Dimensionen mithilfe der Klassifizierungen der AMO-ID-Variablen. Diese neuen Dimensionen wirken sich nicht auf Ihre vorhandenen Marketing-Kanal oder die Dimensionen der Kampagne-Tracking-Variablen aus oder ändern sie nicht. Die AMO-ID ist mit dem Profil eines Besuchers verbunden, wenn ein Besucher über eine gebührenpflichtige Suchanzeige auf die Site gelangt. Daher können die AMO-Dimensionen verwendet werden, um sowohl die AMO-Metriken, die von dieser Integration bereitgestellt werden, als auch alle Daten, die vom Besucher nachgelagert erfasst werden (Besuche, Besucher, Ansichten der Seite, Absprungrate, Bestellungen, Umsatz, benutzerspezifische Ereignis usw.), aufzuschlüsseln. Sie können auch durch andere Dimensionen aufgeschlüsselt werden, wenn Berichte mit anderen Onsite-Metriken ausgeführt werden.
>
>Die Klassifizierungen für diese Metriken werden täglich aktualisiert. Wenn Sie also Änderungen an den Metadaten in einer Suchmaschine vornehmen, werden diese Änderungen möglicherweise erst am folgenden Tag angezeigt, an dem die Klassifizierungen aktualisiert werden.

| Name der Klassifizierung (Dimension) | Definition |
|--- |--- |
| Suchbegriffsübereinstimmungstyp (AMO-ID) | Der Suchbegriffübereinstimmungstyp. Werte sind normalerweise breit, Wortgruppe, exakt oder gar kein Wert, wenn der Anzeigentyp keinen Übereinstimmungstyp aufweist. |
| Anzeigenplattform (AMO-ID) | Der Name der Suchmaschine. Die Werte können Google AdWords oder Microsoft Bing Ads enthalten. |
| Konto (AMO-ID) | Der Name des Suchmaschinenkontos, das verfolgt wird. |
| Kampagne (AMO-ID) | Der Name der Kampagne in Ihrem Suchmaschinenkonto. |
| Anzeigengruppe (AMO-ID) | Der Name der Anzeigengruppe in den Kampagnen Ihrer Suchmaschine. |
| Anzeige (AMO-ID) | Der für Ihre Anzeige verwendete Titel und die Beschreibung |
| Suchbegriff (AMO-ID) | Der Keyword-Wert aus Ihrem Suchmaschinenkonto |
| Übereinstimmungstyp (AMO-ID) | Der Ihrem Keyword zugewiesene Keyword-Zuordnungstyp. Die Werte lauten normalerweise „umfassend“, „Phrase“, „exakt“ oder „kein Wert“, wenn für die Anzeigenart kein Zuordnungstyp vorhanden ist. |
| Anzeigenart (AMO-ID) | Der Typ der verarbeiteten Anzeige, normalerweise „Textanzeige“. |
| Anzeigentitel (AMO-ID) | Das in Ihrer Anzeige verwendete Titelobjekt. |
| Anzeigenbeschreibung (AMO-ID) | Das in Ihrer Anzeige verwendete Anzeigenbeschreibungsobjekt. |
| Anzeigen-URL (AMO-ID) | Das in Ihrer Anzeige verwendete URL-Objekt für die Darstellung der Anzeige. |
| Anzeigenziel-URL (AMO-ID) | Die Landingpage-URL oder finale URL, die Ihrer Anzeige zugewiesen ist. |
| Netzwerk (AMO-ID) | Das Netzwerk, auf dem die Anzeige bereitgestellt wird. Bei Advertising Analytics lautet dieser Wert immer „Suche“. |
| Platzierung (AMO-ID) | Die Website für verwaltete Platzierungen (für Inhaltsnetzwerke). Diese Dimension wird nur von verwalteten Platzierungen verwendet. |
| Produkt-Zielgruppe (AMO-ID) | Der Name des in PLA-Anzeigen verwendeten Produktziels (nicht das tatsächlich gekaufte Produkt). |
| Optimierung (AMO-ID) | Dies wird nicht von Advertising Analytics verwendet. Es wird nur von Advertising Cloud-Kunden verwendet. |
| Gerät (AMO-ID) | Wird momentan nicht verwendet. Platzhalter für potenzielle künftige Produkterweiterung auf das angegebene Zielgerät (z. B. Mobiltelefon, Desktop) für die Anzeige (nicht das tatsächliche Gerät des Besuchers). |

**Metriken**

>[!IMPORTANT]
>
>Bei den von Advertising Analytics bereitgestellten Metriken (siehe unten) handelt es sich um Zusammenfassungsdaten aus den Suchmaschinen. Sie sind nicht mit den Analytics Besucher-Profilen verbunden. Sie sind nur mit der AMO-ID-Variablen und den zugehörigen Classification-Dimensionen verknüpft. Daher sollten sie nicht von anderen Dimensionen/Segmenten als den Dimensionen der AMO-ID gemeldet werden. Dies führt dazu, dass Analytics Nullen für die Daten anzeigt. Sie können sie in errechnete Metriken mit anderen Metriken einbeziehen, aber diese errechnete Metrik sollte auch nur durch die AMO-ID-Dimensionen aufgeschlüsselt werden.
>
>Diese Metriken werden täglich aus Daten bezogen, sodass sie keine Daten für den aktuellen Tag haben. Sie sollten auch nicht mit einer Granularität von weniger als täglich gemeldet werden.
>
>Es gibt eine Metrik für AMO-ID-Instanzen, die festgelegt wird, wenn die AMO-ID für eine Landingpage festgelegt wird (d. h. eine Clickthrough-Rate). Diese Metrik wird in Echtzeit mit dem Treffer der Landingpage erfasst und steht für Aufschlüsselungen zur Verfügung, bei denen auch andere Dimensionen auf der Landingpage festgelegt wurden.

| Name der Metrik | Definition |
|--- |--- |
| AMO Impressionen | Die Anzahl der Anzeigenimpressionen, die von der Suchmaschine gemeldet werden. |
| AMO Klicks | Die Anzahl der Klicks auf Anzeigen, die von der Suchmaschine gemeldet werden. |
| AMO Kosten | Die für jeden Suchbegriff/jede Anzeige gezahlten Kosten, wie von der Suchmaschine gemeldet. |
| Durchschn. Pos. | Eine berechnete Metrik, die die durchschnittliche Position der Anzeigen, wie von der Suchmaschine gemeldet, widerspiegelt. |
| Durchschnittl. Qualitätsbewertung | Eine berechnete Metrik, die den durchschnittlichen Qualitätswert der Suchmaschine widerspiegelt. |
