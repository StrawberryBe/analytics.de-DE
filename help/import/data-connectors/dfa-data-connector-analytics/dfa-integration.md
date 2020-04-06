---
description: 'Bei der Konfiguration der DFA-Integration sind folgende Aufgaben enthalten '
keywords: DFA
title: DFA-Integration
topic: Data connectors
uuid: 972a9d62-24fd-4463-a34c-5ec0b926e81e
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# DFA-Integration {#dfa-integration}

Bei der Konfiguration der DFA-Integration sind folgende Aufgaben enthalten:

## Konfigurieren der DFA-Integration {#configure-the-dfa-integration}

Führen Sie die DFA Data Connectors-Integration durch.

Die Konfigurationsseiten bieten einen Überblick über die Integration sowie hilfreiche Links für weitere Informationen. Für diese Integration fallen sowohl Adobe- als auch DoubleClick-Gebühren an. Wenden Sie sich an die jeweiligen Verkaufsmitarbeiter der beiden Unternehmen und versichern Sie sich, dass Sie die Zusammensetzung der Gebühren verstehen.

1. Melden Sie sich bei [!DNL Adobe Analytics] an.
1. Klicken Sie auf **[!UICONTROL Admin]** > **[!UICONTROL Data Connectors]**.

   ![](assets/data_connectors.png)

1. Suchen Sie **[!UICONTROL DoubleClick DFA]** und klicken Sie auf **[!UICONTROL Add New]**.

   ![Schritt Ergebnis](assets/wizard-01.png)

   Geben Sie auf jeder Seite des Integrationsassistenten die erforderlichen Informationen ein und klicken Sie auf **[!UICONTROL Next]**. In der folgenden Tabelle werden die Informationen erläutert, die Sie zum Abschluss der Integration mithilfe des Assistenten benötigen.

<table id="table_8F6F7F304C36431DA5FD6E5D54F60FC0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Assistentenseite Nr. </th> 
   <th colname="col2" class="entry"> Feld </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 1 </td> 
   <td colname="col2"> Integrationsname </td> 
   <td colname="col3"> Der Integrationsname, der von Genesis in der aktiven Integrationsliste der Report Suite angezeigt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 1 </td> 
   <td colname="col2"> Email-Adresse der Integration </td> 
   <td colname="col3"> Die E-Mail-Adresse, an die alle Benachrichtigungen im Zusammenhang mit dieser Integration gesendet werden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> Benutzername </td> 
   <td colname="col3"> Der für diese Integration zu verwendende DFA-API-Benutzername. Um einen Benutzer für die API-Anmeldung zu aktivieren, überprüfen Sie das API-Attribut in der DFA-Oberfläche. Nachdem Sie die API-Anmeldung aktiviert haben, wird ein Kennwortfeld angezeigt, um ein Kennwort für den Benutzer bereitzustellen. Dieses Kennwort wird zur Authentifizierung zusammen mit dem Benutzernamen in den Assistenten eingegeben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> Passwort </td> 
   <td colname="col3"> Das DFA-API-Passwort. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 2 </td> 
   <td colname="col2"> Advertiser-ID </td> 
   <td colname="col3"> <p>Die DFA-Advertiser-ID oder die übergeordnete Floodlight-Konfigurations-ID. Data Connectors verwendet diese ID zur Identifizierung des zu verfolgenden DFA-Advertisers (Version 1.5 der Integration). Diese Advertiser-ID wird in Version 2.0 der Integration nicht verwendet. Stattdessen wird die übergeordnete Floodlight-Konfigurations-ID abgerufen und verwendet. Anweisungen finden Sie in den Anweisungen auf dem Bildschirm </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 3 </td> 
   <td colname="col2"> DFA-Anzeigenvariable </td> 
   <td colname="col3"> Die Analytics-eVar, an die DFA-Kampagnen-Attribute, Impressionen und Klickdaten gesendet werden. Dabei handelt es sich im Normalfall um die Trackingcode-eVar (  <span class="varname"> s.campaign </span>), Sie können aber jede verfügbare eVar auswählen. Data Connectors fügt außerdem die folgenden DFA-bezogenen Classifications zur ausgewählten eVar hinzu: <p><b>Kampagnen</b>: Eine Sammlung von Anzeigen, die an mehrere Sites mit gemeinsamem Messaging gesendet werden. </p> <p><b>Site-Name</b>: Die Site, auf der die Anzeige bereitgestellt wurde. </p> <p><b>Anzeigenname</b>: Der Anzeigenname, wie in Ihrem DFA-Konto definiert. </p> <p><b>Site-Platzierungsname</b>: Die Website und Seite, auf der die Anzeige bereitgestellt wurde. </p> <p><b>Versand-Tool</b>: DoubleClick for Advertisers </p> <p><b>Kanal</b>: Banneranzeige </p> <p><b>Kostenstruktur</b>: CPM, CPC oder Fest, basierend auf der Kostenstruktur der Anzeige. </p> <p><b>Kreativer Name</b>: Der Name des kreativen Elements, das mit einer Anzeigen-/Platzierungs-/Kreativelement-ID verknüpft ist. </p> <p><b>DFA &gt; SearchCenter-Deduplizierung</b>: Legt fest, dass DFA Werte in SearchCenter-Variablen eingibt, wenn DFA-Clickthrough- oder Durchsichtsaktionen ausgeführt werden </a> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 </td> 
   <td colname="col2"> Impressionen </td> 
   <td colname="col3"> Das benutzerspezifische Ereignis, an das DFA-Impressionsmetrikdaten gesendet werden. Impressionen geben an, wie oft die Anzeige bereitgestellt wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 4 </td> 
   <td colname="col2"> Klicks </td> 
   <td colname="col3"> Wählen Sie das benutzerspezifische Ereignis aus, an das DFA-Klickmetrikdaten gesendet werden. Klicks stellen die Anzahl der wie durch die Weiterleitung von DFA gemessenen Klicks auf die Anzeige durch Besucher dar. Die Klickmetrik steht in Zusammenhang mit der Analytics-Clickthrough-Metrik. <p>Hinweis: DFA-Klicks und Analytics-Clickthroughs stimmen aufgrund von Unterschieden in der Erfassungsart der Daten unter Umständen nicht genau überein.  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> Ansicht-Through-Variable </td> 
   <td colname="col3"> <p>Die Analytics-eVar, an die DFA-Ansicht-Through-Daten gesendet werden. Die Variable "Ansicht-Through"hilft Ihnen dabei, zu sehen, wie Ansichten-Raten die Konversionsraten auf Ihrer Site beeinflussen. </p> <p>Data Connectors fügt dieser eVar dieselben DFA-bezogenen Classifications hinzu wie der DFA-Anzeigenvariablen (siehe oben). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> Zeit seit der letzten Ansicht (Ansicht-durch-Zeitbehälter-Variable) </td> 
   <td colname="col3"> Die Analytics-eVar, an die Daten zur DFA-Zeit seit der letzten Ansicht gesendet werden. Die Zeitangabe seit der letzten Ansicht gibt an, wie viel Zeit seit der letzten Ansicht vergangen ist. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 5 </td> 
   <td colname="col2"> Ansichten-Durchgänge </td> 
   <td colname="col3"> Das benutzerspezifische Ereignis, an das DFA-Ansicht-Durchlauf-Metrikdaten gesendet werden. Verwenden Sie das Durchsichtsereignis mit der Durchsichtsvariablen, um herauszufinden, welche Kampagnen keinen direkten Clickthrough veranlassen, aber unter Umständen eine Rolle bei der Erhöhung des Traffics auf der Site zu einem späteren Zeitpunkt gespielt haben. <p>Das ausgewählte benutzerspezifische Ereignis wird durch Data Connectors in „Durchklick-Ansichten“ umbenannt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 6 </td> 
   <td colname="col2"> Fehler bei der DFA-Abfrage </td> 
   <td colname="col3"> (Optional) Die Analytics-eVar, an die alle gemeldeten Fehlermeldungen zur DFA-Abfrage gesendet werden. Mögliche DFA-Nachrichtencodes sind: 
    <ul id="ul_85FC7FB19F7F4ADF83ABCA6DDB44CE19"> 
     <li id="li_0A3181DED5A149588A0D3F1584E2FE8B"><b>nc</b>: Kein DoubleClick-Cookie. </li> 
     <li id="li_D397AA73AD5E4086A18B87F271E4EC14"><b>oo</b>: Benutzer hat sich abgemeldet. </li> 
     <li id="li_5AC1D0C8049340B4AD857D88E275CBD6"><b>nh</b>: Keine Kampagne Geschichte. </li> 
     <li id="li_73A8C5E905C54E2BB531A1FCDBC6AA1A"><b>qe</b>: Fehler bei der Abfrage (Zeitüberschreitung, Serverausfall usw.) </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 6 </td> 
   <td colname="col2"> Timeout-Ereignis </td> 
   <td colname="col3"> <p>Das Analytics-Zählerereignis, dessen Wert bei jedem Ablauf von  <span class="varname"> s.maxDelay </span> steigt, wenn keine Reaktion von den DFA-Servern einging. Verwenden Sie dieses Ereignis zum Konfigurieren der <span class="varname"> s.maxDelay </span>-Variablen zum Abstimmen von s.maxDelay</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Websiteaktualisierungen für die DFA-Integration {#web-site-updates-for-the-dfa-integration}

Sobald Ihre Analytics-Report Suite für die DFA-Integration von Genesis konfiguriert wurde, müssen Sie Ihre Website und DFA-Umgebung anhand folgender Schritte konfigurieren, damit die Integration unterstützt wird:

### Verifizierung der Cookiekapazität auf der Domäne {#verify-cookie-space-on-the-domain}

Für die Data Connectors-Integration für DFA müssen Sie ein Cookie in der Domäne der Seite einrichten.

Obwohl dies selten der Fall ist, haben einige Domänen die maximale Cookie-Kapazität für einige Webbrowser erreicht. Um das Browsen der Besucher auf Ihrer Website nicht zu beeinträchtigen, versichern Sie sich bei Ihrem Netzwerkbetreiber, Ihrem Entwicklungsteam oder Ihrer Technikgruppe, dass das Hinzufügen eines weiteren Cookies zur Domäne der für die DFA-Integration verwendeten Seiten keinen Einfluss darauf hat. Sie müssen außerdem einen Namen für das Cookie festlegen.

### Aktualisierung Ihres DFA-Abfragestringparameters {#update-your-dfa-query-string-parameter}

Wenn Sie bereits vor der DFA-Integration Werbeanzeigen-Kampagnen mit Adobe Analytics verfolgt haben, ist es möglich, dass alle Kampagnen (E-Mail, Suche oder Banner) denselben Zeichenfolgenparameter für die Abfrage verwenden, um die verweisende Kampagnen-ID auf der Landingpage zu identifizieren.

Um zu verstehen, wann Ansichten- und Clickthrough-Daten aus DFA-Daten für Ihre DFA-Ad-Kampagnen angefordert werden sollen, muss Data Connectors ermitteln, wann ein Besucher auf eine DFA-Kampagne-Banneranzeige geklickt hat. Dazu müssen Sie einen differenzierten Abfragezeichenfolgenparameter zur Landingpage-URL der DFA-Anzeigenkampagne hinzufügen, sodass Data Connectors zwischen DFA-Anzeigenkampagnenseiten und anderen Anzeigenkampagnenseiten unterscheiden kann, die sich gegebenenfalls auf Ihrer Website befinden. Der `dfa_overrideParam` im JavaScript-Plug-in, das für DFA verwendet wird.

>[!CAUTION]
>
>Die Kampagnenvariable kann zwar für andere Kampagnen verwendet werden, sollte jedoch nicht für DFA-Kampagnen verwendet werden. Wenn Sie die Variable &quot;Kampagne&quot;auf eine DFA-Kampagne-Landingpage festlegen, kann Adobe Impressionen und Klicks nicht mit Durchklickraten für DFA-Kampagnen verknüpfen. Einmal pro Besuch prüfen die Adobe-Erfassungsserver die DFA-Server auf vorherige Clickthrough- oder Ansicht-Rate. Fügen Sie daher den DFA-Plug-in-Code nur auf allgemeinen Landingpages ein, um unnötige Umleitungen zu vermeiden, die insbesondere für Benutzer mit langsameren Internetverbindungen die Ladezeiten der Seiten verlangsamen können.

## Aktualisierung des Datenerfassungscodes Ihrer Website {#update-your-web-site-s-data-collection-code}

Für die Genesis-Integration für DFA wird die DFA Floodlight-Konfigurations-ID (dfa_SPOTID) verwendet, wodurch die Berichtskonsistenz zwischen DFA und dem Adobe-Datenerfassungssystem verbessert wird.

>[!NOTE] Die Bezeichnung „Spotlight“ wurde in einer neuen Version von Google DFA in „Floodlight“ geändert. Die Benennung des JavaScript-Parameters `dfa_SPOTID` basiert auf der Spotlight-Terminologie, wird aber für beide Versionen verwendet.

Um die DFA-Integration auf Ihrer Website zu aktivieren, müssen Sie Ihren JavaScript-Datenerfassungscode aktualisieren, indem Sie Folgendes hinzufügen:

* Integrate-Modul für DFA
* Zusatz zum Erfassungscode

### Integrate-Modul für DFA {#section-fa00e42a732a4e27a4ab3dfcfeae1a5b}

Für die DFA-Integration wird das Adobe Experience Cloud Integrate-Modul verwendet, wodurch zusätzliche Funktionen zu Ihrem JavaScript-Datenerfassungscode (`s_code.js`) hinzugefügt werden. Das Integrate-Modul ist Bestandteil der ZIP-Datei, wenn Sie den AppMeasurement für JavaScript-Code aus dem Code-Manager herunterladen. Wenden Sie sich an Ihren Adobe-Berater, wenn Sie weitere Hilfe benötigen, um ihn zu finden.

Fügen Sie den Integrate-Modulcode in den Abschnitt `Modules` der Datei `s_code.js` Ihrer Website ein.

### Zusatz zu Ihrem Erfassungscode {#section-8f98c727f1ba414fb8b4f02d696b8791}

Basierend auf Ihren Einstellungen bei der Aktivierung der DFA-Integration im Integrationsassistenten wird von Data Connectors ein benutzerdefinierter Zusatz zu Ihrem JavaScript-Datenerfassungscode erstellt, den Sie per E-Mail erhalten. Geben Sie diesen Code in den Hauptabschnitt der Datei `s_code.js` (nicht in die Funktion `doPlugins` oder andere Funktionen) ein.

Der folgende Beispielcode dient nur zur Veranschaulichung: Verwenden Sie den Code, der Ihnen nach Abschluss des Data Connectors-Integrationsassistenten per E-Mail zugesendet wurde.

Der Erfassungscode besteht aus den folgenden Komponenten:

* DFA-Integrationseinstellungen
* Für Integration erforderliche Plug-ins

**DFA-Integrationseinstellungen**

```
/************************** DFA VARIABLES **************************/ 
var dfaConfig = { 
   CSID:              "1234567", 
   SPOTID:            "29876543", 
   tEvar:             "eVar17", 
   errorEvar:         "eVar59", 
   timeoutEvent:      "event76", 
   requestURL:         "http://fls.doubleclick.net/ 
json?spot=[SPOTID]&src=[CSID]&var=[VAR]&host=integrate.112.2o7.net%2 
Fdfa_echo%3Fvar%3D[VAR]%26AQE%3D1%26A2S%3D1&ord=[RAND]", 
 
   maxDelay:          "1500", 
   visitCookie:       "s_dfa", 
   clickThroughParam: "CID", 
   searchCenterParam: "s_kwcid", 
   newRsidsProp:      undefined 
}; 
/************************ END DFA Variables ************************/ 
```

Der DFA Integrate-Einstellungsblock legt die für die DFA-Integration erforderlichen Variablen fest. Die Werte für jede dieser Variablen stammen aus den folgenden Quellen:

**CSID**: Clientseitige ID. Wird von DFA nach Abschluss des Integrationsassistenten erstellt. Data Connectors füllt diese Variable mit Ihrer DFA CS ID und sendet Ihnen diesen Wert auch in der Setup-E-Mail, nachdem Sie den Integrationsassistenten abgeschlossen haben. Diese Variable ist nicht erforderlich, wenn das erweiterte AdServing für Ihr Konto aktiviert ist.

**SPOTID**: Floodlight-Konfiguration (zuvor Spotlight-ID genannt). Data Connectors füllt diese Variable vorab mit Ihrer DFA Floodlight-Konfigurations-ID, basierend auf den DFA-Kontoinformationen, die Sie im Integrationsassistenten angegeben haben.

**tEvar**: Übertragungsvariable. Data Connectors füllt diese Variable mit dem Analytics-Variablennamen, den Sie im Integrationsassistenten für die Ansicht-Through-Variable angegeben haben. Ändern Sie diesen Wert nur nach sorgfältiger Abstimmung mit Adobe Engineering oder Engineering Services.

**errorEvar**: Fehlervariable. Data Connectors füllt diese Variable mit dem Analytics-Variablennamen, den Sie im Integrationsassistenten für die Variable &quot;DFA-Abfrage-Fehler&quot;angegeben haben.

**timeoutEvent**: Timeout-Ereignis. Data Connectors füllt diese Variable mit dem Analytics-Variablennamen, den Sie im Integrationsassistenten für die Variable &quot;Timeout Ereignis&quot;angegeben haben.

**requestURL**: Der Remote-DFA-Host zur Abfrage für Anzeigeninformationen. Ändern Sie diesen Wert nur, wenn Adobe dies anweist.

**maxDelay**: Gibt in Millisekunden an, wie lange der JavaScript-Datenerfassungscode auf eine Antwort vom DFA Floodlight-Server wartet. Adobe empfiehlt, mit diesem Wert etwas zu experimentieren, um die für den Traffic auf Ihrer Site optimale Einstellung zu ermitteln. Wenn Sie diesen Wert beispielsweise erhöhen, werden im Allgemeinen mehr DFA-Daten gesammelt, aber das Risiko, die Basisdaten des Besuchers zu verlieren, erhöht sich, wenn der Besucher die Site während der Verzögerung verlässt. Durch die Reduzierung dieses Werts sinkt das Risiko, Trefferdaten zu verlieren, kann jedoch die Menge der DFA-Daten, die mit den Adobe-Trefferdaten gesendet werden, reduziert werden.

**visitCookie**: Der Name des Cookies, mit dem DFA-Aufrufe auf ein Mal pro Besuch beschränkt werden.

**clickThroughParam**: Eine Abfrage-Zeichenfolge, die normalerweise in allen Anzeigen enthalten ist und dem Integrate-Modul mitteilt, dass gerade ein Klick stattgefunden hat. Wenn dieser Parameter in der Abfrage-Zeichenfolge vorhanden ist, wird die Anforderung an DFA Floodlight-Server gesendet, unabhängig davon, ob der Besucher in den letzten 30 Minuten bereits abgefragt wurde.

**newRsidsProp**: (Optional) Einer nicht verwendeten Traffic-Eigenschaftenvariablen zugeordnet. Die DFA-Integration erfasst und speichert diesen Wert im Besuchcookie, um die Report Suites zu identifizieren, die Daten für einen bestimmten Besucher erfasst haben. Diese Eigenschaft ist nur bei benutzerdefinierten Implementierungen mit Adobe Engineering Services erforderlich.

**Für die Integration erforderliche Plugins**

Der Erfassungscode-Zusatz enthält zusätzliche Plugins, die den Betrieb der DFA-Integration verbessern:

* Begrenzt DFA-Abfragen auf ein Mal pro Besuch
* Bietet Flexibilität bei Cookie-Namen. Obwohl die meisten Organisationen s_dfa verwenden, können Sie einen beliebigen gültigen Cookie-Namen für die DFA-Integration verwenden.
* Beseitigung unnötiger Umleitungen. Da Ansicht-through-Daten in Echtzeit erfasst werden, können Adobe-Erfassungsserver und DFA potenziell Daten auf jeder Ansicht austauschen. Das Plug-In blockiert diesen Datenaustausch, wenn die Informationen nicht erforderlich sind.

>[!CAUTION]
>
>Bei einem der Mechanismen, die vom Plug-in verwendet werden, um unnötige DFA-Abfragen zu verhindern, handelt es sich um ein domänenbasiertes Besuchscookie. Eine Integrations-Report Suite, die mehrere Domänen umfasst, erhöht die Clickthrough- und Durchsichtsdaten, wenn Besucher nach einer DFA-basierten Durchsichts- oder Clickthrough-Aktion die Domäne wechseln.

## Bestätigung einer erfolgreichen DFA-Integration befolgen {#confirming-a-successful-dfa-integration}

Nachdem Sie alle notwendigen Websiteaktualisierungen vorgenommen haben, können Sie einen Viewer für den Datenverkehr im Netzwerk wie Charles*, Chrome Developer Tools oder Firebug* verwenden, um zu überprüfen, ob DFA mit den Adobe-Erfassungsservern kommuniziert.

Verwenden Sie den Viewer für den Datenverkehr im Netzwerk, nachdem Sie die DFA-aktivierte `s_code.js`-Datei bereitgestellt haben, um die Anfragen zwischen DFA und den Adobe-Datenerfassungsservern anzuzeigen und nach Folgendem zu suchen:

* Anfrage an den DFA-Service `fls.doubleclick.net/json`. Dieser Dienst kann je nach verwendeter DFA-Version unterschiedlich reagieren. Mit DFA-Integration Version 1.5:

   * HTTP-302-Weiterleitung auf [!DNL ad.doubleclick.net]. Dadurch wird mit der Reaktion ein „Ort:“-Tag gesendet, in dem Informationen zum Anzeigenbesucher enthalten sind.
   * Durch dieses Tag erfolgt eine Weiterleitung auf [!DNL integrate.112.2o7.net/dfa_echo]. Dieser Dienst übersetzt die Informationen zum Besucher der Anzeige in eine JSON-kodierte Zeichenfolge (JavaScript Object Notation on). Diese Daten werden mit einer HTTP-Antwort von 200 OK zurückgegeben.

* Mit DFA-Integration Version 2.0 (erweitertes Ad-Serving aktiviert):

   * [!DNL fls.doubleclick.net] gibt direkt 200 „OK“ zurück.

In beiden Fällen führt eine erfolgreiche Anforderung zu einer Anforderung an die Adobe-Datenerfassungsserver, die den Parameter vX enthält, wobei X Ihre Ansicht-Through-eVar-Nummer ist. Dieser Parameterwert hat das folgende Format: DFA-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX Diese Zeichenfolge enthält Daten zum letzten Klick und zum letzten Impression für den aktuellen Besucher.

## Abstimmung von s.maxDelay {#tuning-s-maxdelay}

Zu einer erfolgreichen DFA-Implementierung gehört auch ein optimierter Wert für s.maxDelay auf Ihrer entsprechenden Site.

Im Allgemeinen beinhaltet die Entscheidung, *`s.maxDelay`* zu erhöhen oder zu senken, einen Kompromiss zwischen dem Abrufen von mehr DFA-Besucherdaten und der Gefährdung der Sammlung von Adobe-Besucherdaten. Durch die Erhöhung von *`s.maxDelay`* werden mehr DFA-Besucherdaten abgerufen. Bei einem zu hoch eingestellten Wert kann die Erfassung von Adobe-Besucherdaten jedoch beeinträchtigt werden. Senken Sie s.maxDelay, ist die Erfassung von Adobe-Besucherdaten gewährleistet, aber es können DFA-Besucherdaten verloren gehen.

*`s.maxDelay`* beinhaltet mehr als nur die Zeit für die Netzwerkkommunikation zur Kontaktaufnahme mit DFA. Dieser Wert stellt auch Browserverzögerungen dar, die das JavaScript auslösen und evaluieren, auf dem diese Kommunikation basiert. Dies liegt daran, dass das Integrate-Modul den *`s.maxDelay`*-Timer startet, nachdem es das HTML-Element in das DOM eingefügt hat, das die Daten vom DFA Floodlight-Server abruft. Die Zeitdauer, die der Browser benötigt, um die HTTP-Anforderung auf der Grundlage dieses neuen HTML-Elements zu starten, hängt von anderen Bildern oder JavaScript-Dateien ab, die gleichzeitig geladen werden, von der Geschwindigkeit des Besuchers und von bestimmten Browserimplementierungen. Wenn die JSON-Daten vom DFA Floodlight-Server abgerufen werden, muss JavaScript vom Browser ausgewertet werden. Dies wird wiederum vollständig vom Browser gesteuert und kann verzögert werden, wenn große Mengen von JavaScript-Code gleichzeitig ausgeführt werden oder viele asynchrone JavaScript-Anfragen ausgeführt werden.

Beachten Sie diese Informationen und legen Sie den Wert für  *`s.maxDelay`* also auf Grundlage der Komplexität der Landingpage und der Netzwerkverzögerungen bei DFA fest. Auf einigen Sites lässt sich die Komplexität unter anderem dadurch verringern, dass der Adobe-Erfassungscode frühzeitig beim Laden der Seite ausgelöst wird, sodass weniger im Browser ausgeführt wird, wenn der Floodlight-Server angefordert wird.

Die Timeoutvariable ist bei der Abstimmung von  *`s.maxDelay`* dringend erforderlich, da sie bei jedem Ablauf von s.maxDelay erhöht wird. Es wird empfohlen, sich an diesen Prozess zu halten, wenn Sie auswählen, ob *`s.maxDelay`* erhöht oder reduziert werden soll:

1. Erfassen Sie Daten aus mehreren Tagen, wobei Sie *`s.maxDelay`* auf einen bestimmten Wert festlegen.
1. Führen Sie einen [!DNL Daily Unique Visitors Report] für den Zeitraum aus.
1. Führen Sie einen [!DNL Timeout Event Report] aus, um zu überprüfen, wie viele Timeouts auftreten. Denken Sie daran, dass ein Timeout nur einmal pro Besucher erfasst wird.

Jetzt, da die Zahlen vorliegen, berechnen

```
Timeout Percentage = [Step 3] / [Step 2] * 100
```

Beachten Sie, dass der Timeout-Prozentsatz tatsächlich alle Besucher der Site berücksichtigt. Einige dieser Besucher wären überhaupt nicht an DFA gebunden gewesen, sodass der Timeout irreführend ist. Sie können diese Berechnung verbessern, indem Sie eine weitere Analyse nur für Unique Visitors auf Seiten ausführen, für die `clickThroughParam` eingestellt ist (zum Beispiel `?CID=1`). Dadurch wird die Genauigkeit erhöht.

Liegt der Timeoutprozentsatz sehr niedrig, sollten Sie  *`s.maxDelay`*. Liegt er sehr hoch, erhöhen Sie *`s.maxDelay`*. Wird *`s.maxDelay`* reduziert, sollten Sie den [!DNL Timeout Report] erneut durchführen, um zu gewährleisten, dass die Anzahl der Timeouts nicht stark gestiegen ist. Wenn Sie *`s.maxDelay`* erhöhen, sollten Sie einen [!DNL Page Views Report] ausführen, um sicherzustellen, dass Seitenansichten nicht aufgrund verlorener Daten fehlschlagen. Beobachten Sie bei jeder Änderung von *`s.maxDelay`* die Daten über mehrere Tage, um sicherzustellen, dass die Daten einen Trend und nicht nur eine tägliche Schwankung darstellen.

Die optimale Einstellung für *`s.maxDelay`* ist der Punkt, an dem der Timeout-Prozentsatz minimiert wird, während „Seitenansichten“ nicht zurückgeht.

Die Timeouts werden beim Wechsel zu Version 2.0 der Integration voraussichtlich verringert, da 302-Weiterleitungen entfernt werden. Erste Ergebnisse mit Beta-Kunden haben gezeigt, dass die Timeouts stetig reduziert werden und somit mehr DFA-Daten gesammelt werden
