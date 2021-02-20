---
description: Sie werden vom Data Connectors-Integrationsassistenten durch den Data Connectors-Integrationsprozess geführt.
title: Ausführen des Data Connectors-Integrationsassistenten
uuid: 714417f7-c1df-4e61-a07f-d319f6581c9c
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 100%

---


# Ausführen des Data Connectors-Integrationsassistenten {#running-the-data-connectors-integration-wizard}

Sie werden vom Data Connectors-Integrationsassistenten durch den Data Connectors-Integrationsprozess geführt.

Konfigurieren der Integration:

1. Melden Sie sich bei Experience Cloud an.
1. Klicken Sie auf der Startseite von Adobe Analytics auf der Windrad- oder Werkzeugleiste auf das Data Connectors™-Symbol.
1. Wählen Sie auf der Seite „Data Connectors“ die Report Suite aus, in der Sie die Integration konfigurieren möchten.

   >[!NOTE]
   >
   >Wählen Sie die gewünschte Report Suite auf der Seite „Data Connectors“ in der links oben befindlichen Dropdown-Liste **Report Suite** aus.

1. Klicken Sie links auf der Data Connectors-Benutzeroberfläche im oberen Bereich der **Partner-Liste** auf die Registerkarte **Alphabetisch** und suchen Sie dann nach dem **Datran**-Symbol.
1. Ziehen Sie das **Datran**-Symbol in einen leeren Plug-in-Slot in Ihrer Adobe Analytics Report Suite, um den Data Connectors-Integrationsassistenten zu starten.

1. Überprüfen Sie auf der Einführungsseite für die Datran-Integration den Text. Aktivieren Sie das Kontrollkästchen, um die mit der Integration verbundenen Gebühren zu akzeptieren, und klicken Sie dann auf **Weiter**.

   Auf dieser Seite erhalten Sie einen Überblick über die Integration sowie praktische Links für weitere Informationen. Für diese Integration fallen sowohl Adobe- als auch Datran-Gebühren an. Wenden Sie sich an die jeweiligen Verkaufsmitarbeiter der beiden Unternehmen und versichern Sie sich, dass Sie die Zusammensetzung der Gebühren verstehen.
1. Geben Sie auf jeder Seite des Data Connectors-Integrationsassistenten die erforderlichen Informationen ein, wie in der folgenden Tabelle beschrieben:

<table id="table_74EC1EEBE7A548AB878AA40187EBCD30"> 
 <thead> 
  <tr valign="top"> 
   <th colname="col1" valign="top" align="left" class="entry"> <p><b>ASSISTENTENSEITE NR.</b> </p> </th> 
   <th colname="col2" class="entry"> <p><b>FELD</b> </p> </th> 
   <th colname="col3" class="entry"> <p><b>BESCHREIBUNG</b> </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2" valign="top" align="left"> <p>Integrationsname </p> </td> 
   <td colname="col3"> <p>Geben Sie den Integrationsnamen an, den Data Connectors in „Aktive Integrationsliste“ der Report Suite anzeigt. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Integrations-E-Mail-Adresse </p> </td> 
   <td colname="col3"> <p>Geben Sie die E-Mail-Adresse an, an die alle Benachrichtigungen zu dieser Integration gesendet werden, und klicken Sie dann auf <b>Weiter</b>, um mit Schritt 2 des Assistenten fortzufahren. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Konto-ID </p> </td> 
   <td colname="col3"> <p>Geben Sie Ihre Datran-Konto-ID ein (die eindeutige Kennung, die Datran Ihrer Organisation zugewiesen hat). Klicken Sie dann auf <b>Weiter</b>, um mit Schritt 3 des Assistenten fortzufahren. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Nachrichten-ID </p> </td> 
   <td colname="col3"> <p>Identifizieren Sie die Adobe Analytics-eVar, die zur Verfolgung der E-Mail-Nachrichten-ID verwendet wird. </p> <p>Die Nachrichten-ID wird für Marketing-/Remarketing-Kampagnen verwendet. Die Nachrichten-ID wird häufig als „Trackingcode“ bezeichnet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Empfänger-ID </p> </td> 
   <td colname="col3"> <p>Identifizieren Sie die Adobe Analytics-eVar, die zur Verfolgung der E-Mail-Empfänger-ID verwendet wird. </p> <p>Die Empfänger-ID wird für Marketing-/Remarketing-Kampagnen verwendet. Die Nachrichten-ID wird häufig als „Besuchercode“ bezeichnet. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Kontrollkästchen für die Annahme </p> </td> 
   <td colname="col3"> <p>Überprüfen Sie die Informationen, die neben dem Kontrollkästchen „Annahme“ angezeigt werden: </p> <p><i>Ich bestätige, dass durch Aktivierung der „Empfänger-ID“-Verfolgung persönlich identifizierbare Angaben zu unseren Site-Besuchern verfolgt werden können. Daraus ergeben sich Datenschutzsachverhalte, die die Implementierung angemessener Vorgehensweisen seitens meiner Organisation erfordern, so z. B. die rechtzeitige Inkenntnissetzung und das Einverständnis der Site-Besucher. </i> </p> <p>Wenn Sie der Annahmeerklärung zustimmen, aktivieren Sie das Kontrollkästchen und klicken Sie dann auf <b>Weiter</b>, um mit Schritt 4 des Assistenten fortzufahren. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Kundendefinierte Segmente auf Report Suite-Ebene </p> </td> 
   <td colname="col3"> <p>Diese Integration erstellt die von den Partnern definierten Segmente, die links auf der Seite „Integrationssegmente“ des Integrationsassistenten angezeigt werden. </p> <p>Darüber hinaus können Sie vorhandene Segmente auf Report Suite-Ebene auswählen, die in die Integration aufgenommen werden sollen. </p> <p>Wählen Sie die gewünschten Segmente auf der rechten Seite aus und klicken Sie dann auf <b>Weiter</b>, um mit Schritt 5 des Assistenten fortzufahren. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Angeklickt </p> </td> 
   <td colname="col3"> <p>Geben Sie das Adobe Analytics-Ereignis an, mit dem die vom E-Mail-System importierten per E-Mail angeklickten Daten gespeichert werden. </p> <p>Das angeklickte Ereignis zeigt die Anzahl der Besucher an, die auf die E-Mail-Nachricht geklickt haben. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Geöffnet </p> </td> 
   <td colname="col3"> <p>Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Mail-System importierten, geöffneten E-Mail-Daten speichert. </p> <p>Das Ereignis „Geöffnet“ zeigt die Anzahl der Besucher an, welche die E-Mail geöffnet haben. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Gesendet </p> </td> 
   <td colname="col3"> <p>Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Mail-System importierten, gesendeten E-Mail-Daten speichert. </p> <p>Das Ereignis „Angeklickt“ zeigt die Anzahl der gesendeten E-Mail-Nachrichten an. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Rücksendungen insgesamt </p> </td> 
   <td colname="col3"> <p>Geben Sie das Adobe Analytics-Ereignis an, in dem die vom E-Mail-System importierten Daten zu „Rücksendungen insgesamt“ gespeichert werden. </p> <p>Das Ereignis „Rücksendungen insgesamt“ zeigt die Anzahl der E-Mail-Nachrichten an, die aufgrund eines Bereitstellungsproblems nicht an Empfänger gesendet wurden. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>Abo storniert </p> </td> 
   <td colname="col3"> <p>Geben Sie das Adobe Analytics-Ereignis an, das die aus dem E-Mail-System importierten E-Mail-Daten zur Kündigung des Abonnements speichert. </p> <p>Mit dem Ereignis „Abo storniert“ können Sie die Anzahl der Besucher anzeigen, welche die E-Mail-Nachricht geöffnet, aber dann auf den Link „Abonnement kündigen“ geklickt haben, um zukünftige E-Mail-Nachrichten aus Ihrer Organisation abzuwählen. </p> <p>Klicken Sie auf „Weiter“, um mit Schritt 6 des Assistenten fortzufahren. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p>Datenerfassung: „JavaScript-Plugin“ </p> </td> 
   <td colname="col3"> <p>Wählen Sie <b>JavaScript-Plug-in</b> aus, wenn Sie das Plug-in als Erfassungsmodell für diese Integration verwenden möchten, und klicken Sie dann auf <b>Weiter</b>, um mit Schritt 7 des Assistenten fortzufahren. </p> <p> <p>Hinweis: „Automatisierte Lösung“ ist die Standardauswahl. </p> </p> <p>Wenden Sie sich für eine Kopie des für diese Integration verwendeten JavaScript-Plug-ins an Ihren Adobe-Berater. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p>Datenerfassung: „Automatisierte Lösung“ </p> </td> 
   <td colname="col3"> <p>Wählen Sie <b>Automatisierte Lösung</b> aus, wenn Sie ein automatisiertes Erfassungsmodell für diese Integration verwenden möchten, und geben Sie dann die eindeutigen Kennungen für diese Integration an. </p> <p> <p>Hinweis: „Automatisierte Lösung“ ist die Standardauswahl. </p> </p> <p>Wenn Sie diese Option auswählen, geben Sie die eindeutigen Kennungen an, die für diese Integration verwendet werden: </p> <p><b>Abfragezeichenfolgenparameter der Nachrichten-ID:</b> Dieser Wert steht für die Nachrichten-ID, die Ihr E-Mail-Partner an die URL der Landingpage angehängt hat. </p> <p><b>Abfragezeichenfolgenparameter der Empfänger-ID:</b> Dieser Wert steht für die Empfänger-ID, die Ihr E-Mail-Partner an die URL der Landingpage angehängt hat. </p> <p>Klicken Sie auf <b>Weiter</b>, um mit Schritt 7 des Assistenten fortzufahren. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>Integrationszusammenfassung </p> </td> 
   <td colname="col3"> <p>Überprüfen Sie die Integrationsparameter, indem Sie auf das Pluszeichen (+) neben jeder Kategorie klicken und dann auf <b>Speichern</b> klicken, um mit Schritt 8 des Assistenten fortzufahren. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p>Integration abgeschlossen </p> </td> 
   <td colname="col3"> <p>Klicken Sie auf <b>Fertigstellen</b>, um die Integration abzuschließen. </p> <p><b>WICHTIG:</b> Adobe Analytics speichert die Integrationseinstellungen erst, wenn Sie auf <b>Fertigstellen</b> klicken. </p> </td> 
  </tr> 
 </tbody> 
</table>
