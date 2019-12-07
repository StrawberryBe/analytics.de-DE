---
description: Beschreibt die durch die Integration erzielten Marketing-Effizienzen.
title: Lyris Data Connector for Adobe Analytics
uuid: db213865-1296-4a93-a0a2-781c026b2be5
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Lyris Data Connector for Adobe Analytics{#lyris-data-connector-for-adobe-analytics}

Beschreibt die durch die Integration erzielten Marketing-Effizienzen.

Bei der E-Mail-Integration von Adobe® Data Connectors™ werden verhaltensbezogene Informationen aus Adobe Analytics mit Lyris E-Mail-Marketing kombiniert, um die Erfolgsmessung neu zu definieren und Zielgruppen mit relevanterem Messaging anzusprechen.

Die Bereitstellung relevanter E-Mail-Nachrichten für diese Marktsegmente kann zu völlig neuen Umsatzmöglichkeiten führen, wodurch die Konvertierung und der Umsatz neuer und vorhandener E-Mail-Kampagnen gesteigert werden. So hat sich zum Beispiel die Bereitstellung relevanter E-Mail-Nachrichten auf der Grundlage von Produkten, die während eines Besuchs angesehen wurden, oder von Produkten, die in einem Warenkorb zurückgelassen wurden, als dramatisch auf den Umsatz ausgewirkt, mit minimalen Auswirkungen auf die Kosten, da dadurch lediglich Besucher genutzt werden, die Ihre Site bereits erhält.

Diese Steigerung der Marketingeffizienz ist einer der wichtigsten Vorteile der Integration von Adobe Analytics in Lyris. Darüber hinaus synchronisiert diese Integration E-Mail-Metriken automatisch mit Adobe Analytics-Daten so häufig wie stündlich für Berichte mit geschlossener Schleife.

## Hauptvorteile und Funktionen{#key-benefits-and-features}

Beschreibt die wichtigsten Vorteile der Integration von Lyris und Adobe Marketing Reports &amp; Analysen.

Die Integration von Lyris und Adobe Analytics bietet die folgenden Hauptvorteile:

* Zusammenfassen von E-Mail-Marketing- und Analysedaten in einer Berichtsschnittstelle
* Optimieren Sie E-Mail-Kampagnen nach Konversion und Beitrag zum Umsatz und zum Site-Erfolg.
* Remarketing zu wichtigen Besuchern und Marktsegmenten basierend auf dynamischen Marketingsegmenten

### Dynamische Marketingsegmente

Die E-Mail-Integration unterstützt dynamische Marketingsegmente, die Sie bei der Förderung Ihres Unternehmens unterstützen. Diese Integration umfasst die folgenden Marketingsegmente standardmäßig:

* **Einkaufswagenabbruchprofil**: hilft Besuchern durch feinabgestimmte Kampagnen, die speziell für diejenigen konzipiert wurden, die zögern, Einkaufswagen abzuschließen, zu Kunden umzuwandeln.
* **Kaufprofile**: Erhöhen Sie Wiederholungsbestellungen und den durchschnittlichen Bestellwert durch Kampagnen, die auf die Kaufmuster der Besucher ausgerichtet sind.
* **Verhaltensprofil**"Produkt-/Inhaltsansicht": Interessenten über Marketingsegmente auf Basis von Produktansichten und Inhaltsprofil erreichen
* Kunden können auch **benutzerdefinierte Remarketing-Segmente** erstellen und planen, die speziell auf die Bedürfnisse ihrer Benutzer abgestimmt sind.

## Voraussetzungen für die Integration{#integration-prerequisites}

Beschreibt die Voraussetzungen für eine erfolgreiche Integration.

Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Elemente anhand Ihrer Implementierungen von Adobe Analytics und Ihrer E-Mail-Software.

Dadurch wird sichergestellt, dass vor der Aktivierung die entsprechenden Best Practices und Voraussetzungen vorhanden sind, was zu einer optimalen und erfolgreichen Integration führt.

### Voraussetzungen für Adobe Analytics {#section-ddb9d4f3b283438ea33788f47f35e69a}

* **Report Suite-spezifisch**:Beachten Sie, dass diese Integration spezifisch für Report Suites ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren
* **Verfügbare und konfigurierte Analytics-Variablen**:Für diese Integration sind benutzerdefinierte Ereignisse und benutzerdefinierte eVars sowie optional zusätzliche Ereignisse und eVars erforderlich.

* **Bevollmächtigter**:Achten Sie darauf, dass Ihre Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe erhebt. Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein Bevollmächtigter Ihres Unternehmens sind. und somit ist Ihr Unternehmen bereit, die in der oben beschriebenen Servicevereinbarung genannten Gebühren zu zahlen, sofern vorhanden.
* **Adobe Analytics Data Warehouse**: Für diese Integration muss Adobe Analytics Data Warehouse aktiviert sein, um Remarketing-Segmente zu generieren. Wenn Sie Data Warehouse nicht aktiviert haben, wenden Sie sich für weitere Informationen an Adobe.
* **Empfänger-ID**: Die Integration erfordert, dass wir eine "Besucher-ID"in einer Analytics-Variablen (eVar) erfassen und speichern. Die Besucher-ID (häufig als "Empfänger-ID"bezeichnet) ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse aus dem Lyris-System. Diese "Empfänger-ID"ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft. die in das Lyris-System zurückgezogen werden und zu Wiederverkaufszwecken genutzt werden können. Während des Setupprozesses müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **Externe Verfolgung**: Wenn Sie derzeit die Best Practice zur Aktivierung der externen Verfolgung für jede gesendete E-Mail-Kampagne nicht befolgen, müssen Sie dies tun, um eine erfolgreiche Integration sicherzustellen. Weitere Informationen finden Sie im Abschnitt "Lyris"
* **Datenschutzbestimmungen**:Sie sollten sich bewusst sein, dass diese Funktion durch Aktivierung der Empfänger- oder Besucher-ID-Verfolgung persönlich identifizierbare Informationen über Ihre Site-Besucher verfolgen kann. Dies hat Auswirkungen auf die Privatsphäre, sodass Ihre Organisation entsprechende Verfahren implementieren muss, z. B. die Benachrichtigung und Zustimmung Ihrer Site-Besucher.

### Voraussetzungen für Lyris EmailLabs {#section-84abae9401224a3699fed861f715ebde}

* **Gültiges Lyris-Konto**: Zur Verwendung dieser Data Connector-Integration benötigen Sie ein gültiges Lyris-Konto.
* **Kontoinformationen**: Sie benötigen während der Integration die folgenden Informationen zu Ihrem Lyris-Konto:

   * *Lyris API-Schlüssel*: Für Datenpopulation verwendet
   * *Abfragezeichenfolgenparameter*: Diese werden an die URL der Einstiegsseite für Nachrichten-ID und Empfänger-ID (Besucher-ID) angehängt.
   * *Lyris Server/URL*: Der Serverwert, den Sie im Lyris-System verwenden
   * *Lyris-Site-ID*: Auch als "Kunden-ID"bezeichnet, ist dies der einzigartige Wert für Ihre Instanz von Lyris HQ. Diese Informationen finden Sie unter "Kundeninformationen"im Bereich "Kontostartseite"von EmailLabs.

## Adobe Analytics-Variablen für Lyris konfigurieren{#configure-adobe-analytics-variables-for-lyris}

Beschreibt die eVars und Ereignisse, die für jede Report Suite-Implementierung reserviert werden sollen.

Für diese Integration müssen mindestens 2 eVars für jede Report Suite-Implementierung reserviert werden. Abgesehen von diesen eVars können einige Ereignisse reserviert werden, je nachdem, welche Lyris-Daten in Analytics angezeigt werden sollen. Diese eVars und Ereignisse werden in der folgenden Tabelle beschrieben:

<table id="table_43E32344E9E54FED8491F28047249329"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variablentyp </th> 
   <th colname="col2" class="entry"> Variablenname </th> 
   <th colname="col3" class="entry"> Verwendung der Variablen </th> 
   <th colname="col4" class="entry"> Einstellungen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Nachrichten-ID </td> 
   <td colname="col3"> So erfassen Sie die Identifizierung der einzelnen E-Mail-Nachrichten </td> 
   <td colname="col4"> <p>Status: Aktiviert </p> <p>Zuordnung: Zuletzt verwendet </p> <p>Läuft ab nach: "Geschäftsentscheidung" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Email Recipient ID </td> 
   <td colname="col3"> So erfassen Sie die anonyme Identifizierung Ihres Kunden, der auf die E-Mail-Kampagne geklickt hat </td> 
   <td colname="col4"> <p>Status: Aktiviert </p> <p>Zuordnung: Zuletzt verwendet </p> <p>Läuft ab nach: "Geschäftsentscheidung" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - Gesendete E-Mails </td> 
   <td colname="col3"> Um nein zu speichern. von E-Mails von Lyris </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - E-Mails geöffnet </td> 
   <td colname="col3"> Um nein zu speichern. der geöffneten E-Mails </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - Eindeutige geöffnete E-Mails </td> 
   <td colname="col3"> Um nein zu speichern. der geöffneten E-Mails </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - E-Mail-Clickthroughs </td> 
   <td colname="col3"> Um nein zu speichern. des Zeitpunkts, zu dem eine E-Mail angeklickt wurde </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - E-Mail-Absprünge </td> 
   <td colname="col3"> So speichern Sie die Nummer. von E-Mails, die abgeschnitten wurden </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis- </td> 
   <td colname="col2"> Lyris - Email Unsubscribe </td> 
   <td colname="col3"> So speichern Sie die Nummer. von deaktivierten E-Mail-Abonnements </td> 
   <td colname="col4">Typ: Nummerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
 </tbody> 
</table>
