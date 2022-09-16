---
title: Verarbeitungsreihenfolge für Daten in Adobe Analytics
description: Erfahren Sie die Reihenfolge der Komponenten und Dienste, die Daten in Adobe Analytics verarbeiten.
source-git-commit: 65ee7ae6d838f34149eb60547d976856e4da3b17
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Verarbeitungsreihenfolge für Daten in Adobe Analytics

Adobe bietet viele Möglichkeiten, Daten zu ändern oder zu ändern, bevor sie in Berichten angezeigt werden. Auf dieser Seite wird die Reihenfolge angezeigt, in der verschiedene Adobe Analytics-Funktionen Daten verarbeiten. Sie können diese Liste verwenden, um Dateninkonsistenzen zu beheben oder die beste Funktion zu bestimmen, die bei Datenanpassungen verwendet werden sollte.

## Daten, bevor sie an Adobe gesendet werden

Bevor Daten an Adobe gesendet werden, werden sie normalerweise clientseitig mit einer der folgenden Methoden kompiliert:

* **AppMeasurement**: Eine auf Ihrer Site gehostete und auf jeder Seite referenzierte JavaScript-Datei. Daten werden direkt an Adobe Analytics gesendet.
* **Adobe Experience Platform Web SDK**: Eine auf Ihrer Site gehostete und auf jeder Seite referenzierte JavaScript-Datei. Daten werden an Adobe Experience Edge gesendet.
* **Tags in der Adobe Experience Cloud-Datenerfassung**: Ein JavaScript-Verweis auf jeder Seite mit Regeln, die in der Datenerfassungs-Benutzeroberfläche erstellt wurden. Die Adobe Analytics-Erweiterung bietet und erleichtert die Implementierung von AppMeasurement. Die Web SDK-Erweiterung bietet eine einfachere Möglichkeit, das Web SDK zu implementieren.

Wenn Sie Daten an Adobe Experience Edge senden, können Sie diese so konfigurieren, dass Daten an Adobe Analytics (sowie an viele andere Adobe Experience Cloud-Lösungen) weitergeleitet werden. Unabhängig von der Implementierungsmethode wird letztendlich eine Bildanforderung mit den gewünschten Variablen an die Datenerfassungsserver von Adobe gesendet.

## Daten beim Eingang zu den Adobe Analytics-Datenerfassungsservern

Sobald Daten in Adobe Analytics eingehen, passen die folgenden Funktionen die Daten nach Bedarf an:

1. **Suchtabellen**: Dimensionen, die auf Adobe-internen Suchtabellen basieren (z. B. die [Browser](/help/components/dimensions/browser.md) Dimension) mit dem entsprechenden Wert übereinstimmen.
2. [**Dynamische Variablen**](/help/implement/vars/page-vars/dynamic-variables.md): Wenn eine dynamische Variable in einem beliebigen Teil einer Bildanforderung angezeigt wird, wird der Wert kopiert und als unabhängiger Wert behandelt, der sich in Zukunft entwickelt.
3. [**Bot-Regeln**](/help/admin/admin/bot-removal/bot-rules.md): Verwenden Sie standardmäßige oder benutzerdefinierte Bot-Filter, um diese Daten aus der Berichterstellung auszuschließen.
4. [**Verarbeitungsregeln**](/help/admin/admin/c-processing-rules/processing-rules.md): Benutzerdefinierte Regeln, die von Ihrer Organisation auf Ihre Daten angewendet werden. Umfasst die Zuordnung von [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) auf die entsprechende Variable.
5. **VISTA-Regeln**: Benutzerdefinierte flexible Regeln, die von einem Adobe-Berater auf Ihre Daten angewendet werden. VISTA-Regeln können je nach den Anforderungen Ihres Unternehmens vor oder nach Verarbeitungsregeln ausgeführt werden. Die meisten VISTA-Regeln werden im Allgemeinen nach Verarbeitungsregeln ausgeführt, aber jede Organisation ist anders eingerichtet. Wenden Sie sich an Ihren Adobe Account Manager, um weitere Informationen zu bestehenden VISTA-Regeln zu erhalten.
6. [**Marketingkanal-Verarbeitungsregeln**](/help/components/c-marketing-channels/c-rules.md): Sie können [Verarbeitungsregeln](/help/admin/admin/c-processing-rules/processing-rules.md) , um Daten für die Verwendung in Marketingkanal-Verarbeitungsregeln vorzubereiten.
7. **Geolocation-Daten**: Dimensionen, die auf der Suche nach IP-Adressen basieren (z. B. die [Länder](/help/components/dimensions/countries.md) -Dimension) gefüllt werden.
8. [**IP-Verschleierung**](/help/admin/admin/general-acct-settings-admin.md): Wenn sich Ihr Unternehmen dafür entschieden hat, IP-Adressen in Rohdaten zu verschleiern, erfolgt dies nach Abschluss aller anderen Verarbeitungsfunktionen.

Zu diesem Zeitpunkt wird der einzelne Treffer in den Report Suite-Datentabellen aufgezeichnet. Nach dem Standard [Latenz](latency.md) -Intervall, ist es in Berichten verfügbar.

## Daten nach der Verarbeitung ändern

Die Daten in Adobe Analytics sind größtenteils dauerhaft. Es gibt jedoch einige Funktionen, die eine selektive Datenanpassung oder -löschung ermöglichen:

* [**Datenreparatur-API**](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/): Bearbeiten Sie bestimmte Spalten oder löschen Sie die gewünschten Datenzeilen.
* [**Data Governance**](/help/admin/c-data-governance/an-gdpr-workflow.md): Mit Datenschutzanfragen können Sie Daten dauerhaft löschen.
* [**Klassifizierungen**](/help/components/classifications/c-classifications.md): Erstellen Sie Dimensionen anhand von Regeln oder hochgeladenen Daten, die eine unterschiedliche Organisation der Daten ermöglichen. Die zugrunde liegenden Report Suite-Daten werden nicht geändert, sodass Sie Classification-Daten frei bearbeiten oder überschreiben können.
* [**Virtual Report Suites**](/help/components/vrs/vrs-about.md): Erstellen Sie eine alternative Report Suite-Ansicht, die das Besuchstimeout ändern oder zulassen kann, dass [Geräteübergreifende Analyse](/help/components/cda/overview.md).
