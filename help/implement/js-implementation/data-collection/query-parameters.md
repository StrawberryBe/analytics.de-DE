---
description: In den folgenden Tabellen werden die Abfrageparameter aufgeführt, die den Wert für jede Analytics-Variable enthalten, die zur Datenerfassung gesendet werden.
keywords: Analytics-Implementierung
seo-description: In den folgenden Tabellen werden die Abfrageparameter aufgeführt, die den Wert für jede Analytics-Variable enthalten, die zur Datenerfassung gesendet werden.
seo-title: Datenerfassungs-Abfrageparameter
solution: Analytics
title: Datenerfassungs-Abfrageparameter
topic: Entwickler und Implementierung
uuid: 4d5af486-df27-42fe-bb9c-28938dddf2b2
translation-type: ht
source-git-commit: 5a30ea6ac47ddd8612728e488afda868491a1ddc

---


# Datenerfassungs-Abfrageparameter

In den folgenden Tabellen werden die Abfrageparameter aufgeführt, die den Wert für jede Analytics-Variable enthalten, die zur Datenerfassung gesendet werden.

Diese Informationen können für das Debugging mit [Packet-Analyzern](../../../implement/impl-testing/packet-monitor.md#concept_490DF35E06D44234A91B5FC57C0BF258), beim manuellen Erstellen von Bildanforderungen oder bei der Verwendung von [dynamischen Variablen](../../../implement/js-implementation/c-variables/dynvars-overview.md#concept_B016789733A94070A9EAB209EEC05262) genutzt werden.

<table id="table_5442E15BF0AE4BDA92DDADD1C08F7C13"> 
 <thead> 
  <tr> 
   <th class="entry"> Parameter </th> 
   <th class="entry"> Analytics-Variable </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> aamlh </td> 
   <td colname="col2"> – </td> 
   <td colname="col3"> – </td> 
   <td colname="col4"> Audience Manager-Standorthinweis (in Experience Cloud Shared Profile-Integration verwendet) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> aamb </td> 
   <td colname="col2"> – </td> 
   <td colname="col3"> – </td> 
   <td colname="col4"> Audience Manager-Blob (in Experience Cloud Shared Profile-Integration verwendet) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> aid </td> 
   <td colname="col2"> – </td> 
   <td colname="col3"> – </td> 
   <td colname="col4"> Analytics-Besucher-ID </td> 
  </tr> 
  <tr> 
   <td> AQB </td> 
   <td> – </td> 
   <td> – </td> 
   <td> Zeigt den Anfang einer Bildanforderung an. </td> 
  </tr> 
  <tr> 
   <td> AQE </td> 
   <td> – </td> 
   <td> – </td> 
   <td> Zeigt das Ende einer Bildanforderung an (was beutet, dass die Anforderung nicht abgeschnitten wurde) </td> 
  </tr> 
  <tr> 
   <td> bh </td> 
   <td> – </td> 
   <td> Besucherprofil | Technologie | Browser-Fensterhöhe </td> 
   <td> Browser-Fensterhöhe (in Pixel) </td> 
  </tr> 
  <tr> 
   <td> bw </td> 
   <td> – </td> 
   <td> Besucherprofil | Technologie | Browser-Fensterbreite </td> 
   <td> Browser-Fensterbreite (in Pixel) </td> 
  </tr> 
  <tr> 
   <td> c </td> 
   <td> – </td> 
   <td> Besucherprofil | Technologie | Bildschirmfarbtiefen </td> 
   <td> Farbqualität (in Bit) </td> 
  </tr> 
  <tr> 
   <td> <code> c. <span class="varname"> [key] </code> </span> </td> 
   <td> <p>s.contextData </p> </td> 
   <td> <p>– </p> </td> 
   <td> <p>Schlüsselwertpaare werden in einem der folgenden Formate angegeben: </p> <p> <code> &lt;my.a&gt;red&lt;/my.a&gt; </code> </p> <p>oder: </p> <p> <code> &lt;my&gt;&lt;a&gt;red&lt;/a&gt;&lt;/my&gt; </code> </p> <p>Jedes dieser Beispiele führt zu dem Kontextdatenwert <code>my.a = red </code>. Es können mehrere Schlüsselwertpaare festgelegt werden. </p> <p>In der Abfragezeichenfolge würde die Kontextdatenvariable als <code>c.&amp;my.a=red</code> angezeigt werden. </p> </td> 
  </tr> 
  <tr> 
   <td> c1 - c75 </td> 
   <td> s.prop1 - s.prop75 </td> 
   <td> Alle benutzerspezifischen Traffic-Berichte </td> 
   <td> In benutzerspezifischen Traffic-Berichten verwendete Traffic-Variablen </td> 
  </tr> 
  <tr> 
   <td> cc </td> 
   <td> s.currencyCode </td> 
   <td> – </td> 
   <td> Die auf der Site verwendete Währung </td> 
  </tr> 
  <tr> 
   <td> cdp </td> 
   <td> s.cookieDomainPeriods </td> 
   <td> – </td> 
   <td> Die Anzahl der Punkte in einer Domäne für die Cookie-Verfolgung (manuell festgelegt) </td> 
  </tr> 
  <tr> 
   <td> ce </td> 
   <td> s.charSet </td> 
   <td> – </td> 
   <td> Die Zeichencodierung der Bildanforderung </td> 
  </tr> 
  <tr> 
   <td> cl </td> 
   <td> s.cookieLifetime (Lebensdauer des s_vi-Cookies in Sekunden) </td> 
   <td> – </td> 
   <td> Die Lebensdauer des Besucher-Cookies. </td> 
  </tr> 
  <tr> 
   <td> ch </td> 
   <td> s.channel </td> 
   <td> Site-Content | Site-Abschnitte </td> 
   <td> Die in den Traffic-Berichten verwendete Site-Abschnitt-Variable </td> 
  </tr> 
  <tr> 
   <td> cp </td> 
   <td> Treffertyp </td> 
   <td> Treffertyp </td> 
   <td> Gibt an, ob das Verhalten das Ergebnis einer direkten Interaktion im Vordergrund ist oder auf Informationen basiert, die das Gerät ohne direkten Interaktionshintergrund sendet. </td> 
  </tr> 
  <tr> 
   <td> ct </td> 
   <td> – </td> 
   <td> Besucherprofil | Technologie | Verbindungstypen </td> 
   <td> Die Art der Verbindung (Modem, LAN usw.; wird nur in IE mit Daten gefüllt) </td> 
  </tr> 
  <tr> 
   <td> <code> D </code> </td> 
   <td> dynamicVariablePrefix </td> 
   <td> – </td> 
   <td> <p>Siehe <a href="../../../implement/js-implementation/c-variables/dynvars-overview.md#concept_B016789733A94070A9EAB209EEC05262" format="dita" scope="local">Dynamische Variablen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td> events oder ev </td> 
   <td> s.events </td> 
   <td> Site-Traffic | Einkäufe, Einkaufswagen, Benutzerspezifische Ereignisse </td> 
   <td> Die Verkaufsaktivitäten und benutzerspezifischen Ereignisse, die auf der Seite aufgetreten sind (für Konversionsberichte) </td> 
  </tr> 
  <tr> 
   <td> g </td> 
   <td> – </td> 
   <td> – </td> 
   <td> Die aktuelle URL der Seite, bis zu 255 Bytes. </td> 
  </tr> 
  <tr> 
   <td> -g </td> 
   <td> – </td> 
   <td> – </td> 
   <td> URLs, die länger als 255 Bytes sind, werden geteilt, wobei die ersten 255 Bytes im Parameter „g=“ und die verbleibenden Bytes später in der Abfragezeichenfolge im Suchparameter „-g=“ integriert werden. </td> 
  </tr> 
  <tr> 
   <td> h1 - h5 </td> 
   <td> s.hier1 - s.hier5 </td> 
   <td> Site-Content | Hierarchieberichte </td> 
   <td> In Traffic-Berichten verwendete Hierarchievariablen </td> 
  </tr> 
  <tr> 
   <td> hp </td> 
   <td> – </td> 
   <td> Besucherprofil | Homepage des Besuchers </td> 
   <td> Gibt an, ob die aktuelle Seite die Browser-Homepage ist (Y/N; nur in IE) </td> 
  </tr> 
  <tr> 
   <td> j </td> 
   <td> – </td> 
   <td> Besucherprofil | Technologie | JavaScript-Version </td> 
   <td> Die aktuell installierte JavaScript-Version (für gewöhnlich 1.x) </td> 
  </tr> 
  <tr> 
   <td> k </td> 
   <td> – </td> 
   <td> Besucherprofil | Technologie | Cookies </td> 
   <td> Gibt an, ob Cookies im Browser unterstützt werden (Y, N oder U) </td> 
  </tr> 
  <tr> 
   <td> l1 - l3 </td> 
   <td> s.list1 - s.list3 </td> 
   <td> Benutzerspezifische Konversion </td> 
   <td> Eine Liste getrennter Werte, die in eine Variable überführt und bei der Berichterstellung als einzelne Zeilenelemente behandelt werden. </td> 
  </tr> 
  <tr> 
   <td> mid </td> 
   <td> – </td> 
   <td> – </td> 
   <td> Experience Cloud-Besucher-ID </td> 
  </tr> 
  <tr> 
   <td> ndh </td> 
   <td> – </td> 
   <td> – </td> 
   <td> Gibt an, ob die Bildanforderung aus einer JS-Datei stammt (1 oder 0) </td> 
  </tr> 
  <tr> 
   <td> ns </td> 
   <td> s.visitorNameSpace </td> 
   <td> – </td> 
   <td> Gibt die Domäne an, in der die Cookies gesetzt werden </td> 
  </tr> 
  <tr> 
   <td> oid </td> 
   <td> s.objectID </td> 
   <td> Site-Content | Links | ClickMap </td> 
   <td> Objekt-ID für die letzte Seite (in ClickMap verwendet) </td> 
  </tr> 
  <tr> 
   <td> ot </td> 
   <td> – </td> 
   <td> Site-Content | Links | ClickMap </td> 
   <td> Objekt-Tagname für die letzte Seite (in ClickMap verwendet) </td> 
  </tr> 
  <tr> 
   <td> p </td> 
   <td> – </td> 
   <td> Besucherprofil | Technologie | Netscape-Plug-ins </td> 
   <td> Liste der Browser-Plug-ins (mit Semikolon getrennt) </td> 
  </tr> 
  <tr> 
   <td> pageName (oder gn) </td> 
   <td> s.pageName </td> 
   <td> Site-Content | Seiten </td> 
   <td> Der Name der Seite in Berichten </td> 
  </tr> 
  <tr> 
   <td> pageType (oder gt) </td> 
   <td> s.pageType </td> 
   <td> Site-Content | Seiten nicht gefunden </td> 
   <td> Gibt an, ob es sich um eine 404-Fehlerseite handelt („error“ oder leer) </td> 
  </tr> 
  <tr> 
   <td> pccr </td> 
   <td> – </td> 
   <td> – </td> 
   <td> Nur bei neuen Besuchern; verhindert endlose Weiterleitungen (ist immer „true“) </td> 
  </tr> 
  <tr> 
   <td> pe </td> 
   <td> s.linkType </td> 
   <td> Site-Content | Links | Exitlinks, Dateidownloads, Benutzerspezifische Links </td> 
   <td> Der Typ des ausgelösten benutzerspezifischen Link-Klicks </td> 
  </tr> 
  <tr> 
   <td> pev1 </td> 
   <td> – </td> 
   <td> Site-Content | Links | Exitlinks, Dateidownloads, Benutzerspezifische Links </td> 
   <td> Die URL der Seite, auf der auf den benutzerspezifischen Link geklickt wurde </td> 
  </tr> 
  <tr> 
   <td> pev2 </td> 
   <td> – </td> 
   <td> Site-Content | Links | Exitlinks, Dateidownloads, Benutzerspezifische Links </td> 
   <td> Anzeigename des benutzerspezifischen Links </td> 
  </tr> 
  <tr> 
   <td> pev3 </td> 
   <td> – </td> 
   <td> Alle Videoberichte </td> 
   <td> Zur Nachverfolgung von Meilensteinen in älteren Videoberichten, ist ab Version 15 veraltet </td> 
  </tr> 
  <tr> 
   <td> pf </td> 
   <td> – </td> 
   <td> – </td> 
   <td> Nur zur Verwendung durch Adobe. Nicht ändern. </td> 
  </tr> 
  <tr> 
   <td> pid </td> 
   <td> – </td> 
   <td> Site-Content | Links | ClickMap </td> 
   <td> Seiten-ID für die letzte Seite (in ClickMap verwendet) </td> 
  </tr> 
  <tr> 
   <td> pidt </td> 
   <td> – </td> 
   <td> Site-Content | Links | ClickMap </td> 
   <td> Seiten-ID-Typ für die letzte Seite (in ClickMap verwendet) </td> 
  </tr> 
  <tr> 
   <td> products (oder pl) </td> 
   <td> s.products </td> 
   <td> Produkte | Produkte </td> 
   <td> In Konversionsberichten verwendete „products“-Variable </td> 
  </tr> 
  <tr> 
   <td> purchaseID (oder pi) </td> 
   <td> s.purchaseID </td> 
   <td> – </td> 
   <td> Dient zur Vermeidung doppelt gezählter Einkäufe, wodurch die Umsätze unnötig ansteigen würden </td> 
  </tr> 
  <tr> 
   <td> r </td> 
   <td> s.referrer </td> 
   <td> Alle Berichte zu Traffic-Quellen </td> 
   <td> Verweisende URL </td> 
  </tr> 
  <tr> 
   <td> s </td> 
   <td> – </td> 
   <td> Besucherprofil | Technologie | Bildschirmauflösungen </td> 
   <td> Bildschirmauflösung (Breite x Höhe) </td> 
  </tr> 
  <tr> 
   <td> server (oder sv) </td> 
   <td> s.server </td> 
   <td> Site-Content | Server </td> 
   <td> Der Server der Seite (wird in Traffic-Berichten verwendet) </td> 
  </tr> 
  <tr> 
   <td> state </td> 
   <td> s.state </td> 
   <td> Besucherprofil | Bundesstaat des Besuchers </td> 
   <td> Gibt den Status wie von der Variablen definiert an. </td> 
  </tr> 
  <tr> 
   <td> t </td> 
   <td> (automatisch, wird mit jedem Treffer gesendet, der keinen benutzerspezifischen Zeitstempel aufweist) </td> 
   <td> – </td> 
   <td> <p>Der Parameter <code>t</code> weist folgendes Format auf: </p> 
    <code>
      dd/mm/yyyy&amp;nbsp;hh:mm:ss&amp;nbsp;D&amp;nbsp;OFFSET 
    </code> <p>Wobei es sich bei „D“ um eine Zahl von <code>0-6</code> handelt, die den Wochentag angibt, und <code>OFFSET</code> für Folgendes steht: </p> 
    <code>
      offset&amp;nbsp;from&amp;nbsp;GMT&amp;nbsp;in&amp;nbsp;hours&amp;nbsp;*&amp;nbsp;60&amp;nbsp;*&amp;nbsp;-&amp;nbsp;1 
    </code> <p> Beispiel: </p> 
    <code>
      23/09/2016&amp;nbsp;14:00:00&amp;nbsp;1&amp;nbsp;420 
    </code> </td> 
  </tr> 
  <tr> 
   <td> <code> ts </code> </td> 
   <td> <p>timestamp </p> </td> 
   <td> – </td> 
   <td> <p>Der benutzerspezifische Zeitstempel, der berechnet und mit dem Treffer gesendet wird. Wird normalerweise für die Offline-Verfolgung verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td> v </td> 
   <td> – </td> 
   <td> Besucherprofil | Technologie | Java </td> 
   <td> Java ist aktiviert (J oder N) </td> 
  </tr> 
  <tr> 
   <td> v0 </td> 
   <td> s.campaign </td> 
   <td> Kampagnen | Trackingcodes </td> 
   <td> Die in Konversionsberichten verwendete „campaign“-Variable </td> 
  </tr> 
  <tr> 
   <td> v1–v75 </td> 
   <td> s.eVar1–s.eVar75 </td> 
   <td> Alle benutzerspezifischen Konversionsberichte </td> 
   <td> In benutzerspezifischen Konversionsberichten verwendete Konversionsvariablen </td> 
  </tr> 
  <tr> 
   <td> vid </td> 
   <td> <p>s.visitorID </p> </td> 
   <td> – </td> 
   <td> Die eindeutige ID des Besuchers, wie in der Besucher-ID-Variable festgelegt. </td> 
  </tr> 
  <tr> 
   <td> vmk </td> 
   <td> s.vmk </td> 
   <td> – </td> 
   <td> Besucher-Migrationsschlüssel für die Migration von Dritt- zu Erstanbieter-Cookies. Herabgestuft. </td> 
  </tr> 
  <tr> 
   <td> vvp </td> 
   <td> s.variableProvider </td> 
   <td> – </td> 
   <td> Wird in Genesis-Integrationen verwendet </td> 
  </tr> 
  <tr> 
   <td> xact </td> 
   <td> s.transactionID </td> 
   <td> – </td> 
   <td> Die zur Verknüpfung von Online- und Offline-Daten verwendete Transaktions-ID </td> 
  </tr> 
  <tr> 
   <td> zip </td> 
   <td> s.zip </td> 
   <td> Besucherprofil | Postleitzahl des Besuchers </td> 
   <td> Die in der Variablen festgelegte Postleitzahl </td> 
  </tr> 
  <tr> 
   <td> /5/ (für Mobilfunkprotokoll) oder /1/ (für alle anderen Protokolle) in der Bildanforderungs-URL. </td> 
   <td> – </td> 
   <td> – </td> 
   <td> <p> Steuert, in welcher Reihenfolge Cookies und sonstige Methoden zum Identifizieren von Besuchern eingesetzt werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

