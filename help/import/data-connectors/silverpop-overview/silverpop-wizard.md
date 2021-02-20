---
description: Sie werden vom Data Connectors-Integrationsassistenten durch den Data Connectors-Integrationsprozess geführt.
title: Silverpop-Integration
uuid: dc5e6a09-3238-412d-9980-4a105ce14819
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 100%

---


# Silverpop-Integration {#silverpop-integration}

Sie werden vom Data Connectors-Integrationsassistenten durch den Data Connectors-Integrationsprozess geführt.

Konfigurieren der Integration:

1. Wählen Sie in der Adobe Experience Cloud in der Dropdown-Liste für Produkte den Eintrag „Data Connectors™“ aus.
1. Klicken Sie auf **[!UICONTROL Neu hinzufügen]** und wählen Sie **[!UICONTROL Nach Name]** in der Dropdown-Liste **[!UICONTROL Anzeigen]** aus.
1. Suchen Sie das Symbol **Silverpop Engage 2.0** und ziehen Sie es in einen leeren Plug-in-Slot in Ihrer Analytics Report Suite, um den Data Connectors-Integrationsassistenten zu starten.
1. Überprüfen Sie auf der Einführungsseite für die Silverpop-Integration den Text und aktivieren Sie dann das Kontrollkästchen, um die mit der Integration verbundenen Gebühren zu akzeptieren.
1. Wählen Sie die Report Suite aus, die Sie für diese Integration verwenden möchten.
1. Geben Sie einen benutzerfreundlichen Namen zur Identifizierung dieser Integration ein und klicken Sie dann auf **[!UICONTROL Diese Integration erstellen und konfigurieren]**.

   Auf dieser Seite erhalten Sie einen Überblick über die Integration sowie praktische Links für weitere Informationen. Für diese Integration fallen sowohl Adobe- als auch Silverpop-Gebühren an. Wenden Sie sich an die jeweiligen Verkaufsmitarbeiter der beiden Unternehmen und versichern Sie sich, dass Sie die Zusammensetzung der Gebühren verstehen.
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
   <td colname="col3"> <p>Geben Sie den Integrationsnamen an, den Data Connectors in „Aktive Integrationsliste“ der Report Suite anzeigt. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2" valign="top" align="left"> <p>Datei herunterladen </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p> Dient zum Remarketing bei Dateidownloads. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p> E-Mail-Adresse </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Dient zum Remarketing an Besucher ohne bekannte Silverpop-ID. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Konto-ID </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Geben Sie Ihre Silverpop-Konto-ID ein (die eindeutige Kennung, die Silverpop Ihrer Organisation zugewiesen hat). Klicken Sie dann auf <b>Weiter</b>, um mit Schritt 3 des Assistenten fortzufahren. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Name des Formulars </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Dient zum Remarketing bei Formularabbrüchen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Versand-ID </p> </td> 
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
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, in dem die vom E-Mail-System importierten Daten zu „Rücksendungen insgesamt“ gespeichert werden. </p> <p>Das Ereignis „Rücksendungen insgesamt“ zeigt die Anzahl der E-Mail-Nachrichten an, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Angeklickt </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, mit dem die vom E-Mail-System importierten per E-Mail angeklickten Daten gespeichert werden. </p> <p>Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> Datei heruntergeladen </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p> Dient zum Remarketing bei Dateidownloads. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> Ausgefülltes Formular </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Dient zum Remarketing bei Formularabbrüchen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> Formulare gestartet </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>Dient zum Remarketing bei Formularabbrüchen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Geöffnet </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, mit dem die vom E-Mail-System importierten per E-Mail geöffneten Daten gespeichert werden. </p> <p>Das Ereignis „Geöffnet“ zeigt die Anzahl der Besucher an, welche die E-Mail geöffnet haben. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Gesendet </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, mit dem die vom E-Mail-System importierten per E-Mail gesendeten Daten gespeichert werden. </p> <p>Das Ereignis „Gesendet“ zeigt die Anzahl der gesendeten E-Mail-Nachrichten an. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Abo storniert </p> </td> 
   <td colname="col03"> <p>(2) Variablenzuordnungen </p> </td> 
   <td colname="col3"> <p>(Erforderlich) Geben Sie das Analytics-Ereignis an, das die aus dem E-Mail-System importierten E-Mail-Daten zur Kündigung des Abonnements speichert. </p> <p>Mit dem Ereignis „Abo storniert“ können Sie die Anzahl der Besucher anzeigen, welche die E-Mail-Nachricht geöffnet, aber dann auf den Link „Abonnement kündigen“ geklickt haben, um zukünftige E-Mail-Nachrichten aus Ihrer Organisation abzuwählen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Segmente </p> </td> 
   <td colname="col03"> <p>(3) Dateneinstellungen </p> </td> 
   <td colname="col3"> <p>Diese Integration erstellt die von Partnern definierten Segmente, die im Abschnitt „Partnersegmente“ angezeigt werden. </p> <p>Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration aufgenommen werden sollen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Zugriffsanforderungen </p> </td> 
   <td colname="col03"> <p>(3) Dateneinstellungen </p> </td> 
   <td colname="col3"> <p> (Erforderlich) Aktivieren Sie <span class="uicontrol">Genehmigen Sie dieser Integration, Produktdaten herunterzuladen</span>. </p> <p> Optional: Erlauben Sie dieser Integration, Daten zu Umsätzen, Bestellungen und Einheiten herunterzuladen. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Datenerfassung </p> </td> 
   <td colname="col03"> <p>(3) Dateneinstellungen </p> </td> 
   <td colname="col3"> <p>Wählen Sie das <b>JavaScript-Plug-in</b> aus, wenn Sie das Plug-in „s_code.js“ als Erfassungsmodell für diese Integration verwenden möchten (siehe <a href="../silverpop-overview/silverpop-analytics-code.md">Analytics-Plug-in-Code</a>). </p> <p>Wählen Sie <b>Automatisierte Lösung</b> aus, wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Kennungen für diese Integration an. </p> <p>Wenn Sie diese Option auswählen, geben Sie die eindeutigen Kennungen an, die für diese Integration verwendet werden: </p> <p> <b>Abfragezeichenfolgenparameter der Nachrichten-ID:</b> Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Landingpage angehängt hat. </p> <p> <b>Abfragezeichenfolgenparameter der Empfänger-ID:</b> Dieser Wert steht für die Empfänger-ID, die Ihr E-Mail-Partner an die URL der Landingpage angehängt hat. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col2"> <p>Dashboard- und Lesezeichenerstellung </p> </td> 
   <td colname="col03"> <p>(4) Berichtseinstellungen </p> </td> 
   <td colname="col3"> <p>Generieren Sie automatisch ein Dashboard und Lesezeichen für die Integration. </p> </td> 
  </tr> 
 </tbody> 
</table>

