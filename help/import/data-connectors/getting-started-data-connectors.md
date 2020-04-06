---
description: Import von Tracking-Daten aus Drittanbieteranwendungen in Analytics
title: Erste Schritte mit Analytics Data Connectors
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Übersicht über Data Connectors

Adobe bietet Organisationen umsetzbare Echtzeit-Informationen zu ihren digitalen Strategien und Marketinginitiativen. Mit Data Connectors können Sie Verfolgungsdaten aus Drittanbieteranwendungen in Analytics importieren, um Daten von einem zentralen Standort zu erfassen und zu verwenden. Wenn Sie eines der Partnerprodukte verwenden, können Sie eine Integration erstellen, die die Anwendungsdaten in Marketing-Berichte importiert. Nach der Integration können Sie Berichte erstellen, die Daten aus Ihrer Anwendung enthalten.

Für eine E-Mail-Integration möchten Sie z. B. vielleicht einen E-Mail-Partner nutzen, der für die Verteilung einer E-Mail-Kampagne sorgt. Wenn Besucher Ihre Website besuchen, möchten Sie wissen, wer aufgrund der E-Mail-Kampagne auf der Seite gelandet ist. Data Connectors integrieren Daten von Ihrem E-Mail-Partner in Marketingberichte, damit Sie diese Informationen zur Messung der Effektivität Ihrer E-Mail-Kampagne bestimmen können.

**Systemanforderungen**

Data Connectors sollten in die gängigsten Browser ordnungsgemäß integriert werden. Die beste Darstellung und Funktion von Berichten auf Systemen, die die folgenden Empfehlungen erfüllen:

* Browser: Microsoft Internet Explorer Version 6 und höher
* Cookies: Erforderlich
* JavaScript: Aktiviert
* Betriebssystem: Windows-basiert
* Macromedia Flash Player: Version 6 oder höher
* Bildschirmauflösung: 1024 x 768 (800 x 600 funktioniert)
* Farbtiefe: 16-Bit oder höher

Zusätzlich wird die Datenerfassung verbessert, wenn für die Webbrowser der Benutzer JavaScript aktiviert wurde.

**Voraussetzungen**

Bevor Sie eine Data Connectors-Integration für Ihr Produkt konfigurieren, führen Sie die folgenden Schritte aus:

* Sie haben die erforderlichen Zugangsdaten für das Partnerprodukt-Konto mit Zugriffsrechten auf alle Daten, die Sie in Marketing-Berichte integrieren möchten. Möglicherweise möchten Sie ein spezielles E-Mail-Konto für Berichtverteiler und für Benachrichtigungen über die integrierten Vorgänge erstellen.
* Identifizieren Sie die benutzerspezifischen Variablen, die die Informationen zu Ihrer Kampagne enthalten. Diese werden in der Regel als Kampagnen-Trackingcode bezeichnet, möglicherweise wird in Ihrer Organisation aber auch eine andere Terminologie verwendet.
* Bestimmen Sie die Ereignis, die Impressionen erhalten sollen, und klicken Sie auf Daten. Möglicherweise möchten Sie die Ereignis entsprechend umbenennen.
* Platzieren Sie den entsprechenden Code auf Ihrer Landingpage, damit Analytics eine geeignete Modellierung mit den Daten des Partnerprodukts durchführen kann. Spezifische Anweisungen für die jeweiligen Partnerprodukte finden Sie im Data Connectors-Showcase unter der Registerkarte Ressourcen.

## Eine Integration hinzufügen

Sie benötigen ein aktuelles Konto, um auf die [!UICONTROL Data Connectors]-Landingpage (Konsole) zugreifen zu können. Darüber hinaus wird empfohlen, dass Sie mit Adobe Analytics vertraut sind.

1. Melden Sie sich bei Adobe Experience Cloud an.
1. Klicken Sie auf **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Data Connectors]**.
1. Klicken Sie auf **[!UICONTROL Add New]**.
1. Gehen Sie durch die **[!UICONTROL Add Integration]** Oberfläche.

   Abhängig von der jeweiligen Produktintegration müssen Sie im Zuge des Integrationsprozesses eventuell spezifische Konfigurationsinformationen bereitstellen.

   Nach Abschluss der Integration wird das Partnerproduktsymbol auf der Seite „Data Connectors-Netzwerk“ angezeigt und steht in den Menüs zur Verfügung.

## Data Connectors-Konsole

Nachdem Sie eine Integration aktiviert haben, wird sie auf der Seite [!UICONTROL Data Connectors] angezeigt. Sie können Details anzeigen und Konfigurationsänderungen in der Konsole vornehmen. Sie können aktive Integrationen und Integrationen für alle Report Suites in Ihrer Firma anzeigen. Sie können auch ein Integrationsprotokoll Ansicht vornehmen, eine Aktivität als Dashboard festlegen, eine Integration konfigurieren und Hilfe suchen.

![Data Connectors-Konsole](assets/data-connectors-console.png)

## Remarketing-Segmente in Data Connectors

Remarketing-Segmente sind Datendateien, die auf der Grundlage der in einer Data Connectors-Integration verwendeten Variablen erstellt werden.

Adobe Analytics sendet diese täglich in separaten Dateien über Data Warehouse an ein durch Adobe für den Drittanbieter erstelltes FTP-Konto. Der Drittanbieter verteilt diese Dateien dann an den Client. Firmen nutzen dies in der Regel für ein Remarketing für Besucher, die die Site besucht und sich ein Produkt angesehen, dieses aber nicht gekauft haben. (Sie wenden sich z. B. an einen Kunden, der einen Rabatt für ein Produkt anbietet, das er angesehen hat, aber am Ende nicht gekauft hat).

**Segmente**

* [!UICONTROL Cart Abandonment]: Der Prozentsatz der Besucher, die einen Artikel zum Einkaufswagen hinzugefügt, ihn aber nicht gekauft haben. Technisch gesehen handelt es sich um eine berechnete Metrik, die aus Bestellungen besteht, geteilt durch Zusätze zum Warenkorb.
* [!UICONTROL Purchases]: Die Empfänger-IDs (oder Besucher-IDs), die Käufe auf der Grundlage der Nachrichten-ID in einem bestimmten Produkt getätigt haben.
* [!UICONTROL Product Views]: Ähnlich [!UICONTROL Cart Abandonment]ist dies auch eine berechnete Metrik. It reports [!UICONTROL Product Views] divided by Orders, because customers&#39; viewing the product shows some interest.

**Implementierungsbeispiele**

Um Remarketing-Segmente erfolgreich implementieren zu können, müssen die folgenden Bedingungen erfüllt sein:

* Es wurde ein Data Connectors-Vertrag abgeschlossen, und Ihre Organisation hat die Implementierungsphase mit einem Adobe-Berater abgeschlossen.
* Das entsprechende Ereignis wird gleichzeitig mit der Produktvariablen ausgelöst:
   * Warenkorbabbruch: `scAdd`-Ereignis
   * Einkäufe: `purchase`-Ereignis
   * Produktansichten: `prodView`-Ereignis

>[!NOTE] Wenn das Produkt ohne verknüpftes Ereignis definiert ist, wird das prodView-Ereignis automatisch ausgelöst.
Falls die obigen Voraussetzungen nicht erfüllt sind, werden die entsprechenden Remarketing-Segmente nicht korrekt berichtet.

[!UICONTROL Cart Abandonment]: wird ausgelöst, nachdem der Benutzer ein Produkt zum Warenkorb hinzugefügt hat:

```
s.products=";cat";
s.events="scAdd";
```

[!UICONTROL Purchases]: wird auf der Kaufbestätigungsseite ausgelöst:

```
s.products=";
cat;1;50";
s.events="purchase";
//Note: Though optional, adding the purchaseID variable increases accuracy by preventing duplicate purchases
```

**Häufige Probleme**

| Problem | Beschreibung |
| -----------| ---------- |  
| In der Remarketing-Segmentdatei werden keine Produkt-ID-Informationen angezeigt. | Dies passiert, wenn das richtige Ereignis ausgelöst wird, für dieselbe Bildanforderung jedoch keine Produktvariable vorhanden ist. Um dies zu korrigieren, vergewissern Sie sich, dass die Produktvariable und das zugehörige Ereignis auf derselben Seite ausgelöst werden, wie in den Implementierungsbeispielen oben dargestellt. |
| Remarketing-Segmentdateien werden nicht empfangen. | Wenn Sie Ihre Dateien nicht erhalten, bitten Sie einen unterstützten Benutzer Ihrer Organisation, sich an ClientCare zu wenden, um zu untersuchen, warum Berichte nicht erfolgreich empfangen wurden. |


>[!IMPORTANT] In der Regel richten Berater zusätzlich zu Ihrer standardmäßigen Remarketing Segment-Datei aus der Data Connectors-Integration auch eine Data Warehouse-Anforderung als terminierten täglichen Bericht ein. Diese Data Warehouse-Anforderung umfasst sowohl Data Connectors-Variablen als auch Nicht-Data Connectors-Variablen. Die Anforderung kann nur auf Basis der spezifischen Anforderung Ihres Unternehmens geplant werden. Um Verwirrung bei der Fehlerbehebung zu vermeiden, geben Sie an, ob es sich bei der betreffenden Datei um die eigentliche Remarketing-Segmentdatei oder um eine Data Warehouse-Anforderung mit Nicht-Genesis-Variablen handelt.
