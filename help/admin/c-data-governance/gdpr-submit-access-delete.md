---
description: So fordern Sie Datenzugriff und -löschung in Adobe Analytics an.
title: Zugriffs- und Löschanfragen einreichen
uuid: d006cd5c-e3cd-4385-8683-acaf73cb681b
translation-type: ht
source-git-commit: b3ea538d0d6e6ebbbbd17871aacaed7527cf3976
workflow-type: ht
source-wordcount: '1312'
ht-degree: 100%

---


# Zugriffs- und Löschanfragen einreichen


## Überblick {#section_BD70882995894C1CA19C205C49FEC23C}

Wenn Ihre Kunden (Verbraucher/Datensubjekte) wissen möchten, welche Daten Sie über sie besitzen, oder verlangen, dass ihre Daten aus Ihren Analytics-Datensätzen gelöscht werden, sind Sie als Datenverantwortlicher für die Beantwortung solcher Anfragen verantwortlich. Der Datenverantwortliche legt fest, wie die Organisation mit betroffenen Personen interagiert (z. B. über ein entsprechendes Benutzerportal), und managt die Interaktion mit ihnen. Es unterliegt darüber hinaus der Verantwortung des Datenverantwortlichen, die Kommunikation mit dem Datensubjekt abzuschließen, nachdem die Anfrage bearbeitet wurde. Als Auftragsverarbeiter akzeptiert Adobe Experience Cloud also keine Anfragen direkt von betroffenen Personen und gibt keine Daten direkt an diese zurück. Stattdessen erhält Adobe Anfragen nur von Ihnen als Datenverantwortlicher und gibt Daten auch nur an Sie zurück.

Sie sollten in Erwägung ziehen, Ihren Apps und Websites Hinweise hinzuzufügen, über die Sie betroffene Personen über ihre Rechte zu direkt oder indirekt identifizierbaren sowie über andere von Ihnen erfasste Daten informieren.

## Kundeneinwilligung verwalten  {#section_3012015E7E8942519FB9279CF7057EAB}

Als Datenverantwortlicher sind Sie dafür zuständig, die ausdrückliche Einwilligung von Ihren Datensubjekten einzuholen, bevor Sie Daten über sie erfassen (möglicherweise auch Adobe Analytics-Daten). Zudem liegt es in Ihrer Verantwortung, auf Ihrer Website einen [Abmeldemechanismus zu implementieren](https://docs.adobe.com/content/help/de-DE/dtm/using/tools/opt-in.html). Über einen solchen Mechanismus können Datensubjekte zu einem späteren Zeitpunkt der Datenerfassung durch Adobe Experience Cloud widersprechen.

## Benutzer und ihre Daten validieren  {#section_AFB2CC225AA94AF6A3CE9F24EF788358}

Sie als Datenverantwortlicher müssen sicherstellen, dass das Datensubjekt die Person ist, für die sie sich ausgibt, und zum Zugriff auf die angeforderten Daten berechtigt ist. Darüber hinaus müssen Sie sicherstellen, dass dem Datensubjekt die richtigen Daten bereitgestellt werden und dass es nicht unumkehrbar Daten zu anderen Datensubjekten erhält.

Hierzu müssen Sie auch die im Rahmen der Datenschutz-Zugriffsanfrage von Adobe Analytics zurückgegebenen Daten überprüfen, bevor Sie sie an das Datensubjekt senden. Besonders vorsichtig sollten Sie sein, wenn Sie Personen-IDs verwenden und nicht nur Daten zurückgeben, in denen diese ID enthalten ist, sondern auch Daten für andere Hits auf gemeinsam genutzten Geräten, auf denen die entsprechende ID manchmal genutzt wurde. Siehe [ID-Erweiterung.](/help/admin/c-data-governance/gdpr-id-expansion.md)

Jede Datei kombiniert Daten von all Ihren Report Suites und entfernt automatisch zusätzliche Kopien replizierter Hits. Sie können entscheiden, welche dieser Dateien Sie an die betroffene Person zurückgeben. Sie können auch Daten extrahieren oder mit Daten aus anderen Systemen kombinieren, bevor Sie sie an das Datensubjekt zurücksenden.

## Anfragen einreichen  {#submit-requests}

Sie können Datenschutz-Zugriffs- und -Löschanfragen über unser [Datenschutz-UI-Portal](https://docs.adobe.com/content/help/de-DE/experience-platform/privacy/home.html#!api-specification/markdown/narrative/tutorials/privacy_service_tutorial/privacy_service_ui_tutorial.md) oder unsere [Datenschutz-API](https://www.adobe.io/apis/experienceplatform/gdpr.html) senden.

>[!NOTE]
>
>Die Datenschutz-API unterstützt die Batch-Einsendung für mehrere Benutzer in einer einzelnen Anfrage. Die Unterstützungsgrenze liegt momentan bei 1000 separaten Benutzern (pro Benutzer können mehrere IDs vorliegen) in einer einzelnen JSON-Anfragedatei.

## JSON-Beispielanfrage  {#sample-json-request}

Hier sehen Sie den JSON-Abschnitt, der über die Datenschutz-API oder -UI eingereicht werden kann und mit dem die Datenschutzverarbeitung für drei Benutzer angefragt wird.

```
{ 
    "companyContexts": [ 
        { 
            "namespace": "imsOrgID", 
            "value": "5D7236525AA6D9580A495C6C@AdobeOrg" 
        } 
    ], 
    "users": [ 
        { 
            "key": "Data Privacy-1234", 
            "action": ["access"], 
            "userIDs": [ 
                { 
                    "namespace": "AAID", 
                    "namespaceId", 10, 
                    "type": "standard", 
                    "description": "Legacy Visitor ID", 
                    "value": "2D783E5885312539-4000010360000181", 
                } 
            ] 
        }, 
        { 
            "key": "Data Privacy-1235", 
            "action": ["access"], 
            "userIDs": [ 
                { 
                    "namespace": "ECID", 
                    "namespaceId": 4, 
                    "type": "standard", 
                    "description": "This is the ID generated by the Adobe ID service.", 
                    "value": "22470866493385587460528148368265592748", 
                } 
            ] 
        }, 
        { 
            "key": "Data Privacy-1236", 
            "action": ["access","delete"], 
            "userIDs": [ 
                { 
                    "namespace": "CRM-ID", 
                    "type": "analytics", 
                    "description": "namespace defined on eVar17 in some report suites", 
                    "value": "ACME-12345678"
                }, 
                { 
                    "namespace": "email address", 
                    "type": "analytics", 
                    "description": "namespace defined on eVar23 in some report suites", 
                    "value": "john@mail.com" 
                } 
            ] 
        } 
    ], 
    "expandIds": true 
} 
```

Beachten Sie, dass der Benutzerabschnitt drei Blöcke enthält, die drei separate Anfragen für vermutlich drei verschiedene Datensubjekte darstellen.

* Bei der ersten Anfrage handelt es sich um eine Zugriffsanfrage, in der eine herkömmliche Adobe Analytics-Cookie-ID (AAID) verwendet wird.
* Die zweite Anfrage ist ebenfalls eine Zugriffsanfrage, in der jedoch ein MCID-/ECID-Cookie verwendet wird.
* Die dritte Anfrage dient sowohl dem Zugriff als auch dem Löschen für die angegebenen IDs. Obwohl für alle Anfragen eine ID-Erweiterung angegeben ist, wird sie die größte Auswirkung auf die dritte Anfrage haben, weil dies die einzige Anfrage ist, für die Nicht-Cookie-IDs verwendet werden. Infolgedessen erkennt diese Anfrage auch Cookie-IDs, die beliebigen Geräten mit der angegebenen CRM-ID oder E-Mail-Adresse zugeordnet sind. Zudem wird die Anfrage erweitert, sodass sie auch diese IDs beinhaltet.

Bedenken Sie Folgendes

* Der Wert „5D7236525AA6D9580A495C6C@AdobeOrg“ im Abschnitt „companyContexts“ muss mit dem Wert Ihrer eigenen Experience Cloud-Organisation aktualisiert werden.
* Die Felder „type“ und „namespace“ werden im Abschnitt [Namespaces](/help/admin/c-data-governance/gdpr-namespaces.md) beschrieben.
* Die Felder „description“ werden ignoriert.
* Die Felder „key“ können beliebige Werte enthalten. Wenn Sie über eine interne ID zum Verfolgen von Datenschutzanfragen verfügen, können Sie hier den Wert ablegen, um die Zuordnung von Anfragen im Adobe-System zu denen in Ihren eigenen Systemen zu vereinfachen.

## Reaktionsdetails  {#section_93F554F65DBB48A18B75EB5784056C96}

Diese Abschnitte enthalten Reaktionsdetails zum Zugriff und zum Löschen.

**Reaktionsdetails zum Zugriff**

Die auf Zugriffsanfragen zurückgegebenen Daten enthalten eine URL, über die Sie als Datenverantwortlicher eine ZIP-Datei herunterladen können, die ein Verzeichnis für jedes Ihrer Adobe-Produkte enthält. Im Analytics-Ordner können sich folgende Elemente befinden:

* Personendateien, abgeleitet aus Hits, die mit ID-PERSON übereinstimmen

   * Eine CSV-Datei mit einer Zeile für jeden passenden Treffer und einer Spalte für jedes Feld mit der Beschriftung ACC-ALL oder ACC-PERSON, sortiert nach Zeitstempel.
   * Eine HTML-Zusammenfassungsdatei mit einem Eintrag für jede ACC-ALL- oder ACC-PERSON-Beschriftung. Jeder Eintrag enthält alle eindeutigen Werte für das Feld sowie die Anzahl der jeweiligen Vorkommen. Felder mit Zeitstempeln werden gerundet, sodass nur eindeutige Tage angegeben werden.

* Gerätedateien, abgeleitet aus Treffern, in denen eines der Felder mit einer bestimmten ID-DEVICE, jedoch keines mit einer bestimmten ID-PERSON übereinstimmte

   * Eine CSV-Datei mit nur einer Zeile für jeden passenden Treffer und einer Spalte für jedes Feld mit der Beschriftung ACC-ALL, sortiert nach Zeitstempel.
   * HTML-Zusammenfassungsdatei mit einem Eintrag für jede ACC-ALL-Beschriftung. Jeder Eintrag enthält alle eindeutigen Werte für das Feld sowie die Anzahl der jeweiligen Vorkommen. Felder mit Zeitstempeln werden gerundet, sodass nur eindeutige Tage angegeben werden.

Jede Datei kombiniert Daten von all Ihren Report Suites und entfernt automatisch zusätzliche Kopien replizierter Hits.

Sie können entscheiden, welche dieser Daten Sie an das Datensubjekt zurückgeben. Sie können auch Daten extrahieren oder mit Daten aus anderen Systemen kombinieren, bevor Sie sie an das Datensubjekt zurücksenden.

**Reaktionsdetails zum Löschen**

Bei Löschanfragen werden keine Daten zurückgegeben. Stattdessen wird ein Status an die Datenschutz-API übermittelt, der die erfolgreiche Bearbeitung der Anfrage angibt.

## Testen der Datenschutzverarbeitung Ihrer Daten {#section_FBA843DBFAE64D979D8DB8A3C56784D7}

In der Regel richten Analytics-Kunden einige Test-Report Suites ein, um die Funktionalität zu überprüfen, bevor sie Ressourcen der Öffentlichkeit zur Verfügung stellen. Bevor echter Traffic an die Produktions-Report Suites gesendet wird, senden Staging-Websites und -Apps die Daten an die entsprechenden Test-, Entwicklungs- oder QS-Report Suites, um zu überprüfen, wie sie nach Veröffentlichung des Codes funktionieren werden.

Mit einer normalen Konfiguration kann die Verarbeitung von DSGVO-Anfragen jedoch nicht erst an diesen Test-Report Suites getestet werden, bevor sie auf die Produktions-Report Suites angewendet wird. Grund hierfür ist, dass eine Datenschutzanfrage automatisch auf alle Report Suites in der Experience Cloud-Organisation angewendet wird, was häufig allen Report Suites für Ihr Unternehmen entspricht.

Es gibt jedoch einige Möglichkeiten, wie Sie Ihre Datenschutzverarbeitung vor der Anwendung auf all Ihre Report Suites testen können:

* Eine Option ist die Einrichtung einer separaten Experience Cloud-Organisation, die nur Test-Report Suites enthält. Verwenden Sie dann diese Experience Cloud-Organisation für Ihren Datenschutztest und Ihre normale Experience Cloud-Organisation für die eigentliche Datenschutzverarbeitung.
* Eine weitere Option ist es, den IDs in Ihren Test-Report-Suites andere Namespaces zuzuweisen als in den Produktions-Report-Suites.

   Sie können beispielsweise jedem Namespace in Ihren Test-Report Suites „qs-“ voranstellen. Wenn Sie Datenschutzanfragen senden, die nur Namespaces mit dem Präfix „qs-“ enthalten, werden diese Anfragen nur im Rahmen Ihrer Test-Report Suites ausgeführt. Wenn Sie die Anfragen später ohne das Präfix senden, werden sie auf Ihre Produktions-Report Suites angewendet. **Wir empfehlen diesen Ansatz, sofern Sie nicht die visitorId-, AAID-, ECID- oder customVisitorId-Namespaces verwenden, da diese fest codiert sind und Sie keine alternativen Namen in Ihren Test-Report Suites festlegen können**.
