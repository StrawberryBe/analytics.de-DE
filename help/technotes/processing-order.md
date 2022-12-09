---
title: Verarbeitungsreihenfolge für Daten in Adobe Analytics
description: Erfahren Sie mehr zur Reihenfolge der Komponenten und Services, die Daten in Adobe Analytics verarbeiten.
exl-id: a8dc9c12-07d3-4dc8-b2df-136f7a7a1e77
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 100%

---

# Verarbeitungsreihenfolge für Daten in Adobe Analytics

Adobe bietet viele Möglichkeiten, Daten zu verändern oder zu bearbeiten, bevor sie in Berichten angezeigt werden. Auf dieser Seite wird die Reihenfolge angezeigt, in der verschiedene Funktionen von Adobe Analytics Daten verarbeiten. Sie können diese Liste verwenden, um Dateninkonsistenzen zu beheben oder die beste Funktion zu bestimmen, die bei notwendigen Datenanpassungen verwendet werden sollte.

![Verarbeitungsreihenfolge](assets/processing-order.png)

## Daten vor ihrem Senden an Adobe

Bevor Daten an Adobe gesendet werden, werden sie normalerweise Client-seitig mit einer der folgenden Methoden kompiliert:

* **AppMeasurement**: Eine auf Ihrer Site gehostete und auf jeder Seite referenzierte JavaScript-Datei. Daten werden direkt an Adobe Analytics gesendet.
* **Adobe Experience Platform Web SDK**: Eine auf Ihrer Site gehostete und auf jeder Seite referenzierte JavaScript-Datei. Daten werden an Adobe Experience Edge gesendet.
* **Tags in der Adobe Experience Cloud-Datenerfassung**: Eine auf jeder Seite referenzierte JavaScript-Datei mit Regeln, die in der Datenerfassungs-Benutzeroberfläche erstellt wurden. Die Adobe Analytics-Erweiterung bietet eine einfachere Möglichkeit der Implementierung von AppMeasurement. Die Web SDK-Erweiterung bietet eine einfachere Möglichkeit, das Web SDK zu implementieren.

Wenn Sie Daten an Adobe Experience Edge senden, können Sie diese so konfigurieren, dass Daten an Adobe Analytics (sowie an viele andere Adobe Experience Cloud-Lösungen) weitergeleitet werden. Unabhängig von der Implementierungsmethode wird letztendlich eine Bildanforderung mit den gewünschten Variablen an die Datenerfassungs-Server von Adobe gesendet.

## Daten beim Empfang bei den Adobe Analytics-Datenerfassungs-Servern

Sobald Daten in Adobe Analytics eingehen, passen die folgenden Funktionen die Daten nach Bedarf an:

1. **Suchtabellen**: Dimensionen, die auf Adobe-internen Suchtabellen basieren (z. B. die Dimension [Browser](/help/components/dimensions/browser.md)) werden dem entsprechenden Wert zugeordnet.
2. [**Dynamische Variablen**](/help/implement/vars/page-vars/dynamic-variables.md): Wenn eine dynamische Variable in einem beliebigen Teil einer Bildanforderung angezeigt wird, wird der Wert kopiert und ab dann als unabhängiger Wert gehandhabt.
3. [**Bot-Regeln**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md): Verwenden Sie standardmäßige oder benutzerdefinierte Bot-Filter, um diese Daten aus dem Reporting auszuschließen.
4. [**Verarbeitungsregeln**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md): Benutzerdefinierte Regeln, die von Ihrer Organisation auf Ihre Daten angewendet werden. Umfasst die Zuordnung von [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) auf die entsprechende Variable.
5. **VISTA-Regeln**: Benutzerdefinierte flexible Regeln, die von einer Person des Adobe-Berater-Teams auf Ihre Daten angewendet werden. VISTA-Regeln können je nach den Anforderungen Ihres Unternehmens vor oder nach den Verarbeitungsregeln ausgeführt werden. VISTA-Regeln werden meist nach den Verarbeitungsregeln ausgeführt, aber jede Organisation ist anders eingerichtet. Wenden Sie sich an Ihren Adobe Account Manager, um weitere Informationen zu bestehenden VISTA-Regeln zu erhalten.
6. [**Marketing-Kanal-Verarbeitungsregeln**](/help/components/c-marketing-channels/c-rules.md): Sie können [Verarbeitungsregeln](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md) verwenden, um Daten für die Verwendung in Marketing-Kanal-Verarbeitungsregeln vorzubereiten.
7. **Geolokalisierungsdaten**: Dimensionen, die auf der Suche nach IP-Adressen basieren (z. B. die Dimension [Land](/help/components/dimensions/countries.md)), werden befüllt.
8. [**IP-Verschleierung**](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md): Wenn sich Ihr Unternehmen dafür entschieden hat, IP-Adressen in Rohdaten zu verschleiern, erfolgt dies, nachdem alle anderen Verarbeitungsfunktionen abgeschlossen sind.

Zu diesem Zeitpunkt wird der einzelne Treffer in den Report Suite-Datentabellen aufgezeichnet. Nach der standardmäßigen [Latenzzeit](latency.md) ist er in Berichten verfügbar.

## Ändern von Daten nach ihrer Verarbeitung

Die Daten in Adobe Analytics sind größtenteils unveränderlich. Es gibt jedoch einige Funktionen, die eine selektive Datenanpassung oder -löschung ermöglichen:

* [**Datenreparatur-API**](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/): Bearbeiten Sie bestimmte Spalten oder löschen Sie die gewünschten Datenzeilen.
* [**Data Governance**](/help/admin/c-data-governance/an-gdpr-workflow.md): Erfüllen Sie Datenschutzanfragen, um Daten dauerhaft zu löschen.
* [**Klassifizierungen**](/help/components/classifications/c-classifications.md): Erstellen Sie Dimensionen anhand von Regeln oder hochgeladenen Daten, um eine unterschiedliche Organisation der Daten zu ermöglichen. Die zugrunde liegenden Report Suite-Daten werden nicht geändert, sodass Sie Klassifizierungsdaten frei bearbeiten oder überschreiben können.
* [**Virtual Report Suites**](/help/components/vrs/vrs-about.md): Erstellen Sie eine alternative Report Suite-Ansicht, durch die die maximale Wartezeit bei einem Besuch geändert oder die [geräteübergreifende Analyse](/help/components/cda/overview.md) zugelassen werden kann.
