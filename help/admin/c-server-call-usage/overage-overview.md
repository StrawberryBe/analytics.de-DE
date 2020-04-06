---
description: 'null'
title: Übersicht zur Nutzung von Server-Aufrufen
uuid: 6e014364-efc1-4769-a0b5-cf105c0ed9b1
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Übersicht zur Nutzung von Server-Aufrufen

## Warum sollte man die Nutzung der Server-Aufrufe überwachen und Warnhinweise einrichten? {#section_060C29BF1D00444B85892AD1FCF55290}

Mit der Nutzung der Server-Aufrufe von Adobe Analytics können Sie Einsicht in Daten über die Server-Aufrufe von Browsern und Mobilgeräten erhalten. Sie haben Zugriff auf:

* Ein Dashboard zur Nutzung von Server-Aufrufen, das Ihre Verbrauchsdaten bezüglich Server-Aufrufen verfolgt und mit Ihrem vertraglich festgelegten Limit vergleicht. (**[!UICONTROL Analytics > Admin > Server Call Usage]**)
* A Server Call Usage alert type in the Alert Builder that lets you set up alerts to prevent overages (**[!UICONTROL Analytics > Components >Alerts]**)

Die wichtigsten Vorteile der Verwendung von Server-Aufrufen sind:

* **Sichtbarkeit** der Daten zum Telefonkonsum und zur Bindung Ihrer Server-Daten, einschließlich des Mobilverbrauchs im Vergleich zu Ihrer vertraglichen Beschränkung der Serveraufrufe.
* **Warnungen** , die Sie über das Risiko oder das Auftreten einer Überlagerung informieren und sich auf die Möglichkeit einer Überschneidung vorbereiten/handeln.

Previously, while you could access monthly server call consumption data under  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Billing]** , this data was only updated 6 days after billing had closed for that month. Zusätzlich dazu enthielten die Daten keine Informationen über die mobile Nutzung. Diese Funktion ersetzt auch den aktuellen **[!UICONTROL Billing Information]** Bericht unter **[!UICONTROL Analytics]** > **[!UICONTROL Reports]** .

## Voraussetzungen {#section_49AE590FFC7C4E8A83C640C4AAA581AA}

* **Berechtigungen:** Um auf das Dashboard zur Nutzung von Server-Aufrufen und die Warnhinweiserstellung/-verwaltung zugreifen zu können, müssen Sie ein Adobe Analytics-Administrator sein.
* **Berechtigungen:** Administratoren können Zugriff auf Nicht-Administratoren gewähren: die Berechtigung aufgerufen wird **[!UICONTROL Server Call Usage]**. Siehe [Berechtigung zur Nutzung von Server-Aufrufen](/help/admin/c-server-call-usage/overage-overview.md#section_FCC58EB635954A32990D4E67B52B4369).

## Wichtige Begriffe {#section_CBA348A039F34563B097CD8890AB358D}

Im Folgenden finden Sie einen kurzen Leitfaden zur wichtigsten Terminologie für die Verwendung von Server-Aufrufen:

<table id="table_4E97F85F13344A2C962FA4FA5A51642E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Begriff </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Serveraufruf </p> </td> 
   <td colname="col2"> <p>Ein Server-Aufruf, auch als "Treffer"oder "Bildanforderung"bezeichnet, ist eine Instanz, in der Daten zur Verarbeitung an Adobe-Server gesendet werden. Der häufigste Serveraufruftyp ist eine page-Ansicht. Bei einem Seitenaufruf betrachtet der Besucher eine Seite Ihrer Website. Es wird dann ein Server-Aufruf an Adobe generiert, wobei Informationen erfasst, verarbeitet und in Ihre Berichtsmetriken aufgenommen werden. </p> <p>Weitere Typen von Server-Aufrufen sind Exitlinks und Dateidownloads, bei denen Daten für eine Verarbeitung an Adobe gesendet werden. Diese Daten werden aber nicht als neuer Seitenaufruf aufgezeichnet. Selbst "ausgeschlossene"Ansichten (z. B. aufgrund eines von Ihnen konfigurierten IP-Adressbereichs) sind Serveraufrufe, da sie von Adobe empfangen und verarbeitet werden, jedoch nie in Ihren Berichten angezeigt werden. </p> <p><b>Primärer Server-Aufruf</b>: Anforderungen, die direkt von den Browsern der Website-Besucher oder von der Dateneinfüge-API empfangen werden. Umfasst primäre Treffer (Seitenaufrufe), primäre benutzerspezifische Ereignis, Primär-Download-Ereignis und primäre Ausstiegs-Ereignis. </p> <p><b>Sekundärer Server-Aufruf</b>: Kopien der primären Serveraufrufe, die von Multi-Suite-Tags erstellt oder von einer VISTA-Regel kopiert/verschoben wurden. Wenn ein sekundärer Serveraufruf durch eine VISTA-Regel in eine andere Report Suite verschoben (nicht kopiert) wurde, werden die gesammelten sekundären Aufrufe von den primären Serveraufrufen abgezogen. </p> <p><b>Primärer Serveraufruf für Mobilgeräte </b> </p> <p>Anforderungen, die direkt von einem der Mobile-SDKs empfangen wurden. Beinhaltet trackAction, trackState, trackApp Crashes, trackActionFromBackground, trackLocation, trackBeacon, trackPushMessageClickThrough, trackTimedActionBacklog, trackLifetimeValueIncrease.</p> <p><b>Mobilgerät - sekundärer Serveraufruf</b> </p> <p>Kopien der primären Server-Aufrufe, die von Multi-Suite-Tags erstellt oder von einer VISTA-Regel kopiert/verschoben wurden. Wenn ein sekundärer Serveraufruf durch eine VISTA-Regel in eine andere Report Suite verschoben (nicht kopiert) wurde, werden die gesammelten sekundären Aufrufe von den primären Serveraufrufen abgezogen. </p> <p>Hinweis: Falls Ihr Unternehmen vertraglich nur zu mobilen Server-Aufrufen (primär oder sekundär) berechtigt ist, werden sowohl die Web- als auch die Mobilnutzung gegen Ihre Mobilzusage aufgerechnet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Firma der Rechnungsstellung (Rechnungsstellungs-ID) </p> </td> 
   <td colname="col2"> <p>Die rechtliche Organisation, der die Server-Aufrufe in Rechnung gestellt werden. Zum Beispiel adobe.com. Jede Abrechnungsunternehmen hat eine Abrechnungs-ID, die verwendet wird, um den Abrechnungskunden eindeutig zu identifizieren. Eine Abrechnungs-ID kann an mehrere Experience Cloud-Abläufe gebunden werden. Es gibt nicht immer eine 1:1-Beziehung zwischen einer Bestellung und einer Abrechnungs-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Firma der Anmeldung </p> </td> 
   <td colname="col2"> <p>Ein Abrechnungsunternehmen kann über <a href="https://helpx.adobe.com/de/analytics/kb/multiple-login-companies.html">mehrere Anmeldeunternehmen</a> verfügen. Eine Firma zur Anmeldung ist eine Sammlung von Report Suites, die von Ihrem Unternehmen verwendet werden. Einige Unternehmen verfügen über mehrere Firmen zur Anmeldung, die für verschiedene Unternehmensbereiche gelten. Dies ist besonders für große Unternehmen nützlich, die mit verschiedenen Geschäftsbereichen zu tun haben, bei denen viele Report Suites nicht für andere in der Firma gelten. </p> <p>Oft sind das regionale Niederlassungen eines Unternehmens. Dieses Beispiel zeigt die Firmen für die Anmeldung und die zugehörigen Report Suites: </p> 
    <ul id="ul_8C756C7972D04F5E89D6E32BB06D26C3"> 
     <li id="li_EA6257FED7854B6FAA071926D0F8A07C">adobe.world: RS1, RS2, RS3, RS4 </li> 
     <li id="li_3EAFB556849E4CCC9D96D5A3492EC898">adobe.us: RS1, RS2 </li> 
     <li id="li_572FFB3F4BF545BDB13102D82CE5E50C">adobe.in: RS3 </li> 
     <li id="li_B6ACBA35E18A427AA83F76BD38E502D7">adobe.de: RS4 </li> 
    </ul> <p>Hinweis: Die Nutzungsdaten von Server-Aufrufen für <u>alle</u> Report Suites innerhalb eines Abrechnungsunternehmens sind für alle Benutzer mit der entsprechenden <a href="/help/admin/c-server-call-usage/overage-overview.md#section_FCC58EB635954A32990D4E67B52B4369">Berechtigung</a> einsehbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud-Organisation </p> </td> 
   <td colname="col2"> <p>Eine --Organisation ist die Einheit, die es einem Administrator ermöglicht, Gruppen und Benutzer zu konfigurieren und das Single-Sign-on in der Experience Cloud zu steuern. Die Organisation agiert als zentrale Anmeldestelle, die sämtliche Experience Cloud-Produkte und -Lösungen umfasst. </p> <p>Meistens ist ein Unternehmen Ihr Name für die Firma. Eine Firma kann jedoch viele Organisationen haben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serveraufruf-Verpflichtung </p> </td> 
   <td colname="col2"> <p>Wenn Ihr Unternehmen einen Vertrag mit Adobe abschließt, dann stellt das Sales-Team von Adobe zusammen mit Ihnen, dem Kunden, fest, welche Arten (primär, sekundär, primär mobil, sekundär mobil) und schätzungsweise welche Menge an Server-Aufrufen von Ihnen über die Dauer des Vertrags zu erwarten sind. Dies ist Ihre gesamte Serveraufrufverpflichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nutzungszeitraum </p> </td> 
   <td colname="col2"> <p>Zur Überwachung der Verwendung von Server-Aufrufen wird diese gesamte Serveraufrufverpflichtung in kleinere Nutzungszeiträume (z. B. 3 Monate) unterteilt, um Jahresvergleiche zu erleichtern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertragszeitraum </p> </td> 
   <td colname="col2"> <p>Die Vertragsdauer kann mehrere Jahre betragen. Nehmen wir an, dass Ihr Unternehmen eine Zusage für Server-Aufrufe von 6 Millionen Aufrufen während einer Vertragsdauer von 3 Jahren erhalten hat. Um die Nutzung der Server-Aufrufe besser überwachen zu können, wird dieser Zeitraum von 3 Jahren in kleinere Nutzungsperioden aufgeteilt, um so einfacher Jahresvergleiche durchzuführen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Berechtigung zur Nutzung von Server-Aufrufen {#section_FCC58EB635954A32990D4E67B52B4369}

Analytics-Administratoren erhalten automatisch die Berechtigung zur Nutzung von Server-Aufrufen. Damit können Nutzer das Dashboard einsehen und Warnhinweise zu Server-Aufrufen erstellen. Administratoren können diese Berechtigung auch Nichtadministratoren erteilen.

>[!NOTE] Ihr Unternehmen kann entscheiden, welche Anmeldeunternehmen Zugriff auf die Nutzung der Server-Aufrufe haben.

<table id="table_86256AD8B4554F369439A8FDF2F545E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Berechtigungsname </th> 
   <th colname="col3" class="entry"> Erteilen Sie die Berechtigung, wenn Sie bei Adobe Analytics angemeldet sind (veraltete Anmeldung) </th> 
   <th colname="col4" class="entry"> Berechtigung erteilen, wenn Sie bei Adobe Experience Cloud angemeldet sind </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nutzung der Server-Aufrufe </p> </td> 
   <td colname="col3"> 
    <ol id="ol_13A984328D264488B7045DC7521A5F55"> 
     <li id="li_ACDA518C7D184084AC1DFA7B38C67314">Melden Sie sich über sc.omniture.com bei Analytics an. </li> 
     <li id="li_066D90AB071941C3869EDAFCE981707A">Gehen Sie zu <span class="ignoretag"> <span class="uicontrol">Admin</span> &gt; <span class="uicontrol">Benutzerverwaltung</span> &gt; <span class="uicontrol">Gruppen</span> &gt; <span class="uicontrol">Zugriff auf alle Berichte bearbeiten</span> &gt; <span class="uicontrol">Analytics-Tools</span> &gt; <span class="uicontrol">Anpassen</span> &gt; <span class="uicontrol">Nutzung der Server-Aufrufe</span> </span> </li> 
    </ol> </td> 
   <td colname="col4"> 
    <ol id="ol_518673ED323A4C5993A3B9F4BA09E405"> 
     <li id="li_56FF685A3B454ECEA5F16BB591A60034">Melden Sie sich bei login.experiencecloud.adobe.com an.</li> 
     <li id="li_FA1AE0F19DEF4AB2AA77B22CCA2995F9">Klicken Sie auf <span class="uicontrol">Analytics</span>. </li> 
     <li id="li_22A4CBB84B5A451780873BBE67E6E6EF">Navigieren Sie zu <span class="ignoretag"><span class="uicontrol">Produkte</span> &gt; <span class="uicontrol">Produktprofil</span> &gt; <span class="uicontrol">Berechtigungen</span> &gt; <span class="uicontrol">Analytics-Tools</span> &gt; <span class="uicontrol">Nutzung der Server-Aufrufe</span></span>. </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

