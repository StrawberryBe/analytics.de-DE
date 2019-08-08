---
description: Der Data Connectors-Integrationsassistent führt Sie durch den Data Connectors-Integrationsprozess.
seo-description: Der Data Connectors-Integrationsassistent führt Sie durch den Data Connectors-Integrationsprozess.
seo-title: Silverpop-Integration
title: Silverpop-Integration
uuid: dc 5 e 6 a 09-3238-412 d -9980-4 a 105 ce 14819
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Silverpop-Integration{#silverpop-integration}

Der Data Connectors-Integrationsassistent führt Sie durch den Data Connectors-Integrationsprozess.

Konfigurieren der Integration:

1. Wählen Sie in der Adobe Marketing Cloud in der Dropdownliste "Produkte" die Option" Data Connectors™" aus.
1. Klicken **[!UICONTROL Sie auf "Neu]** hinzufügen" und wählen **[!UICONTROL Sie]** in der Dropdown-Liste **[!UICONTROL " Anzeigen]** " die Option "Nach Name" aus.
1. Suchen Sie das **Symbol Silverpop Connect 2.0** und ziehen Sie es in einen leeren Plugin-Slot in Ihrer Analytics-Report Suite, um den Data Connectors-Integrationsassistenten zu starten.
1. Überprüfen Sie auf der Einführungsseite der Silverpop-Integration den Text und aktivieren Sie dann das Kontrollkästchen, um die mit der Integration verbundenen Gebühren zu akzeptieren.
1. Wählen Sie die Report Suite aus, die Sie für diese Integration verwenden möchten.
1. Geben Sie einen benutzerfreundlichen Namen zur Identifizierung dieser Integration ein und klicken **[!UICONTROL Sie auf Diese Integration erstellen und konfigurieren]**.

   Auf dieser Seite erhalten Sie einen Überblick über die Integration sowie praktische Links für weitere Informationen. Dieser Integration sind sowohl Adobe- als auch Silverpop-Gebühren zugeordnet. Wenden Sie sich an die jeweiligen Verkaufsmitarbeiter der beiden Unternehmen und versichern Sie sich, dass Sie die Zusammensetzung der Gebühren verstehen.
1. Geben Sie auf jeder Seite des Data Connectors-Integrationsassistenten die erforderlichen Informationen ein, wie in der folgenden Tabelle beschrieben:

<table id="table_74EC1EEBE7A548AB878AA40187EBCD30"> 
 <thead> 
  <tr valign="top"> 
   <th colname="col2" class="entry"> <p> <b>Feld</b> </p> </th> 
   <th colname="col03" valign="top" align="left" class="entry"> <p> <b>Konfigurationsabschnitt</b> </p> </th> 
   <th colname="col3" class="entry"> <p> <b>Beschreibung</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col2" valign="top" align="left"> <p>Integrationsname </p> </td> 
   <td colname="col03"> <p>(1) Integrationseinstellungen </p> </td> 
   <td colname="col3"> <p>Geben Sie den Integrationsnamen an, den Data Connectors in der aktiven Integrationsliste der Report Suite anzeigt. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2" valign="top" align="left"> <p>Datei herunterladen </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p> Für die Verwendung mit Datei-Download-Remarketing. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p> Email Address </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Wird für das Remarketing für Besucher ohne bekannte Silverpop-ID verwendet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Konto-ID </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Geben Sie Ihre Silverpop-Konto-ID (die eindeutige ID Ihres Unternehmens von Silverpop) an und klicken Sie dann auf <b>Weiter</b> , um mit Schritt 3 des Assistenten fortzufahren. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Formularname </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Für das Remarketing des Formularabbruchs. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Versand von Ids </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Silverpop ID </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p> Absprünge </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, das die aus dem E-Email-System importierten Gesamt-Absprungdaten speichert. </p> <p>Das Ereignis "Total-Bounces" zeigt die Anzahl der E-Email-Nachrichten an, die aufgrund eines Problems mit der Auslieferung nicht an Empfänger übermittelt wurden. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Angeklickt </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, das die per E-Email angeklickten Daten aus dem E-Email-System speichert. </p> <p>Mit dem Ereignis "Angeklickt" können Sie erkennen, wie viele Besucher auf die E-Email geklickt haben. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> Datei heruntergeladen </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p> Für die Verwendung mit Datei-Download-Remarketing. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> Formular abgeschlossen </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Für das Remarketing des Formularabbruchs. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> Formular gestartet </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Für das Remarketing des Formularabbruchs. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Geöffnet </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, das die vom E-Email-System importierten Daten per E-Email speichert. </p> <p>Mit dem Ereignis "Geöffnet" können Sie erkennen, wie viele Besucher die E-Email geöffnet haben. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Gesendet </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, das die per E-Email gesendeten Daten speichert, die aus dem E-Email-System importiert wurden. </p> <p>Im Ereignisereignis können Sie die Anzahl der gesendeten E-Email-Nachrichten anzeigen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Abonnement </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, das die vom E-Email-System importierten Daten zum Abonnieren von Abonnements per E-Email speichert. </p> <p>Mit dem nicht abonnierten Ereignis können Sie die Anzahl der Besucher anzeigen, die die E-Email-Nachricht geöffnet haben, dann aber auf den Link Abonnieren klicken, um zukünftige E-Email-Nachrichten aus Ihrer Organisation abzuwählen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Segmente </p> </td> 
   <td colname="col03"> <p>(3) Dateneinstellungen </p> </td> 
   <td colname="col3"> <p>Mit dieser Integration werden die im Abschnitt Partner-Segmente angezeigten Partner-definierten Segmente erstellt. </p> <p>Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration einbezogen werden sollen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Zugriffsanforderungen </p> </td> 
   <td colname="col03"> <p>(3) Dateneinstellungen </p> </td> 
   <td colname="col3"> <p> (Erforderlich) Aktivieren Sie <span class="uicontrol"> Diese Integration zulassen, um die Produktdaten herunterzuladen</span>. </p> <p>Optional: Ermöglicht es dieser Integration, Umsatz, Bestellungen und Einheiten herunterzuladen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Datenerfassung </p> </td> 
   <td colname="col03"> <p>(3) Dateneinstellungen </p> </td> 
   <td colname="col3"> <p>Wählen Sie <b>javascript-Plug-in</b> , wenn Sie das Plug-in s_ code. js als Erfassungsmodell für diese Integration verwenden möchten (siehe <a href="../silverpop-overview/silverpop-analytics-code.md#concept-28e7c834a6804a949aa9306f8896b36e" format="dita" scope="local"> Analytics-Plug-In-Code)</a>. </p> <p>Wählen Sie <b>Automatisierte Lösung</b> , wenn Sie ein automatisiertes Collection-Modell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen ids für diese Integration an. </p> <p>Wenn Sie diese Option auswählen, geben Sie die eindeutigen ids für diese Integration an: </p> <p> <b>Nachrichten-ID Abfragezeichenfolgenparameter:</b>Dieser Wert stellt die Nachrichten-ID dar, die Ihr E-Email-Partner an die URL der Einstiegsseite angehängt hat. </p> <p> <b>Empfänger-ID Abfragezeichenfolgenparameter:</b> Dieser Wert stellt die Empfänger-ID dar, die Ihr E-Email-Partner an die URL der Einstiegsseite angehängt hat. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Dashboard- und Lesezeichenerstellung </p> </td> 
   <td colname="col03"> <p>(4) Berichtseinstellungen </p> </td> 
   <td colname="col3"> <p>Erstellen Sie automatisch ein Dashboard und Lesezeichen für die Integration. </p> </td> 
  </tr> 
 </tbody> 
</table>

