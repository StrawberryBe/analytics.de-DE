---
description: Beschreibt die durch die Integration erzielten Marketing-Effizienzen.
title: Lyris-Data Connector für Adobe Analytics
uuid: db213865-1296-4a93-a0a2-781c026b2be5
translation-type: tm+mt
source-git-commit: 3850dc3503ca57ba4f13f0de63e8420e484db501
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 98%

---


# Lyris-Data Connector für Adobe Analytics {#lyris-data-connector-for-adobe-analytics}

>[!IMPORTANT]
>
>Am 1. August 2021 werden wir die Adobe Data Connector-Technologie beenden. [Weitere Informationen ...](/help/import/data-connectors/data-connectors-eol.md)

Bei der E-Mail-Integration von Adobe® Data Connectors™ werden verhaltensbezogene Informationen aus Adobe Analytics mit Lyris-E-Mail-Marketing kombiniert, um die Erfolgsmessung neu zu definieren und Zielgruppen mit relevanterem Messaging anzusprechen.

Die Bereitstellung relevanter E-Mail-Nachrichten für diese Marktsegmente kann zu völlig neuen Umsatzmöglichkeiten führen, wodurch die Konvertierung und der Umsatz neuer und vorhandener E-Mail-Kampagnen gesteigert werden. So hat zum Beispiel die Bereitstellung relevanter E-Mail-Nachrichten auf Grundlage von Produkten, die während eines Besuchs angesehen wurden, oder von Produkten, die in einem Warenkorb zurückgelassen wurden, nachweislich erhebliche Auswirkungen auf den Umsatz bei minimalen Auswirkungen auf die Kosten, weil dadurch lediglich die Daten Ihrer Websitebenutzer genutzt werden.

Diese Steigerung der Marketingeffizienz ist einer der wichtigsten Vorteile der Integration von Adobe Analytics in Lyris. Darüber hinaus synchronisiert diese Integration E-Mail-Metriken automatisch mit Adobe Analytics-Daten stündlich für Closed-Loop-Berichte.

## Hauptvorteile und Funktionen {#key-benefits-and-features}

Beschreibt die wichtigsten Vorteile der Integration von Lyris und Adobe Marketing Reports and Analytics.

Die Integration von Lyris und Adobe Analytics bietet die folgenden Hauptvorteile:

* Zusammenfassen von E-Mail-Marketing- und Analysedaten auf einer Berichtsoberfläche.
* Optimieren von E-Mail-Kampagnen nach Konversion und Beitrag zum Umsatz und zum Site-Erfolg.
* Auf dynamischen Marketingsegmenten basierendes Remarketing für wichtige Besucher und Marktsegmente.

### Dynamische Marketingsegmente

Die E-Mail-Integration unterstützt dynamische Marketingsegmente, die Sie bei der Förderung Ihres Unternehmens unterstützen. Diese Integration umfasst standardmäßig die folgenden Marketingsegmente:

* **Profil für Warenkorbabbruch**: Mit auf sie speziell abgestimmten Kampagnen können Sie Besucher, die zögern, ihren Einkaufswagen abzuschließen, in Kunden umwandeln.
* **Profile für Kauf**: Erhöhen Sie Nachbestellungen und den durchschnittlichen Bestellwert durch Kampagnen, die auf das Kaufverhalten der Besucher ausgerichtet sind.
* **Profil für das Verhalten der Produkt-/Inhaltsansicht**: Erreichen Sie potenzielle Kunden durch Marketingsegmente, die auf Produktansichten und Inhaltszugriffsprofilen basieren.
* Kunden können auch **benutzerspezifische Remarketing-Segmente** erstellen und planen, die speziell auf die Bedürfnisse ihrer Benutzer abgestimmt sind.

## Voraussetzungen für die Integration {#integration-prerequisites}

Beschreibt die Voraussetzungen für eine erfolgreiche Integration.

Bevor Sie diese Integration aktivieren, überprüfen Sie die folgenden Elemente anhand Ihrer Implementierungen von Adobe Analytics und Ihrer E-Mail-Software.

Dadurch wird sichergestellt, dass vor der Aktivierung die entsprechenden Best Practices und Voraussetzungen vorhanden sind, was zu einer optimalen und erfolgreichen Integration führt.

### Voraussetzungen für Adobe Analytics {#section-ddb9d4f3b283438ea33788f47f35e69a}

* **Report Suite-spezifisch**: Beachten Sie, dass diese Integration Report Suite-spezifisch ist. Stellen Sie sicher, dass Sie die gewünschte Report Suite ausgewählt haben, bevor Sie die Integration aktivieren
* **Verfügbare und konfigurierte Analytics-Variablen**: Für diese Integration sind benutzerspezifische Ereignisse und benutzerspezifische eVars sowie optional zusätzliche Ereignisse und zusätzliche eVars erforderlich.

* **Beauftragter Vertreter**: Achten Sie darauf, dass Ihrer Firma aufgrund der Aktivierung dieser Integration möglicherweise Gebühren gemäß Ihrer Servicevereinbarung mit Adobe, Inc. oder Ihrer Servicevereinbarung mit einem der vertrauenswürdigen Partner von Adobe entstehen. Durch Aktivierung dieser Integration bestätigen Sie hiermit, dass Sie ein beauftragter Vertreter Ihrer Firma sind. Dergestalt ist Ihre Firma bereit, die in der oben beschriebenen Servicevereinbarung ggf. festgelegten Gebühren zu zahlen.
* **Adobe Analytics Data Warehouse**: Für diese Integration muss Adobe Analytics Data Warehouse aktiviert sein, um Remarketing-Segmente zu generieren. Wenn Sie Data Warehouse nicht aktiviert haben, wenden Sie sich für weitere Informationen an Adobe.
* **Empfänger-ID**: Für die Integration muss eine „Besucher-ID“ in einer Analytics-Variablen (eVar) erfasst und gespeichert werden. Die Besucher-ID (häufig als „Empfänger-ID“ bezeichnet) ist eine kodierte oder numerische Darstellung einer E-Mail-Adresse aus dem Lyris-System. Diese „Empfänger-ID“ ist mit dem nachgelagerten Besucherverhalten auf der Site (Warenkorbabbrüche, Käufe usw.) verknüpft, wird wiederum in das Lyris-System übertragen und kann für Remarketing-Zwecke genutzt werden. Während des Einrichtungsvorgangs müssen Sie eine eVar für diesen Zweck identifizieren, wenn Sie vom Assistenten dazu aufgefordert werden.
* **Externes Tracking**: Zum Gewährleisten einer erfolgreichen Integration sollten Sie die Best Practice zur Aktivierung des externen Trackings für jede gesendete E-Mail-Kampagne befolgen. Weitere Informationen finden Sie unten im Abschnitt „Lyris“.
* **Datenschutz-Compliance**: Sie sollten sich darüber im Klaren sein, dass durch die Aktivierung des Empfänger- oder Besucher-ID-Trackings diese Funktion persönliche Informationen Ihrer Site-Besucher verfolgen kann. Dies wirkt sich auf den Datenschutz aus, sodass Ihre Organisation entsprechende Verfahren implementieren muss, z. B. die Benachrichtigung und Zustimmung Ihrer Site-Besucher.

### Voraussetzungen für Lyris EmailLabs {#section-84abae9401224a3699fed861f715ebde}

* **Gültiges Lyris-Konto**: Zur Verwendung dieser Data Connector-Integration benötigen Sie ein gültiges Lyris-Konto.
* **Kontoinformationen**: Sie benötigen während der Einrichtung dieser Integration die folgenden Informationen zu Ihrem Lyris-Konto:

   * *Lyris-API-Schlüssel*: Wird zur Datenpopulation verwendet.
   * *Abfragezeichenfolgeparameter*: Diese werden an die URL der Landingpage für Nachrichten-ID und Empfänger-ID (Besucher-ID) angehängt.
   * *Lyris Server/URL*: Der Serverwert, den Sie im Lyris-System verwenden.
   * *Lyris-Site-ID*: Dieser auch als „Kunden-ID“ bezeichnete eindeutige Wert für Ihre Instanz von Lyris HQ. Diese finden Sie im Abschnitt „Kontostartseite“ von EmailLabs unter „Kundeninfo“.

## Konfigurieren von Adobe Analytics-Variablen für Lyris {#configure-adobe-analytics-variables-for-lyris}

Beschreibt die eVars und Ereignisse, die für jede Report Suite-Implementierung reserviert werden sollen.

Für diese Integration müssen mindestens 2 eVars für jede Report Suite-Implementierung reserviert werden. Abgesehen von diesen eVars können einige Ereignisse reserviert werden, je nachdem, welche Lyris-Daten in Analytics angezeigt werden sollen. Diese eVars und Ereignisse sind in der folgenden Tabelle beschrieben:

<table id="table_43E32344E9E54FED8491F28047249329"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variablentyp </th> 
   <th colname="col2" class="entry"> Variablenname </th> 
   <th colname="col3" class="entry"> Verwenden der Variablen </th> 
   <th colname="col4" class="entry"> Einstellungen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> Nachrichten-ID </td> 
   <td colname="col3"> Erfassen der Identifizierung der einzelnen E-Mail-Nachrichten </td> 
   <td colname="col4"> <p>Status: Aktiviert </p> <p>Zuordnung: Zuletzt verwendet </p> <p>Läuft ab nach: „Geschäftsentscheidung“ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> eVar </td> 
   <td colname="col2"> E-Mail-Empfänger-ID </td> 
   <td colname="col3"> Erfassen der anonymen Identifizierung Ihres Kunden, der auf die E-Mail-Kampagne geklickt hat </td> 
   <td colname="col4"> <p>Status: Aktiviert </p> <p>Zuordnung: Zuletzt verwendet </p> <p>Läuft ab nach: „Geschäftsentscheidung“ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Lyris – Gesendete E-Mails </td> 
   <td colname="col3"> Zum Speichern der Anzahl der von Lyris gesendeten E-Mails </td> 
   <td colname="col4">Typ: Numerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Lyris – Geöffnete E-Mails </td> 
   <td colname="col3"> Zum Speichern der Anzahl der geöffneten E-Mails </td> 
   <td colname="col4">Typ: Numerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Lyris – Geöffnete einmalige E-Mails </td> 
   <td colname="col3"> Zum Speichern der Anzahl der geöffneten einmaligen E-Mails </td> 
   <td colname="col4">Typ: Numerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Lyris – E-Mail-Clickthroughs </td> 
   <td colname="col3"> Zum Speichern der Anzahl der Klicks auf eine E-Mail </td> 
   <td colname="col4">Typ: Numerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Lyris – Nicht zugestellte E-Mails </td> 
   <td colname="col3"> Zum Speichern der Anzahl der nicht zugestellten E-Mails </td> 
   <td colname="col4">Typ: Numerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ereignis </td> 
   <td colname="col2"> Lyris – Gekündigte E-Mail-Abonnements </td> 
   <td colname="col3"> Zum Speichern der Anzahl der deaktivierten E-Mail-Abonnements </td> 
   <td colname="col4">Typ: Numerisch <p>Beitrag: Aktiviert </p> </td> 
  </tr> 
 </tbody> 
</table>
