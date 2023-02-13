---
title: Importieren von Paid-Search-Metriken
description: Schritte zum Konfigurieren von Adobe Analytics zur Verfolgung Ihrer Paid Search-Metriken (z. B. Google AdWords, MSN, Yahoo usw.) unter Verwendung von Datenquellen.
exl-id: b25a2a26-d277-4a51-9194-973acb425095
source-git-commit: 68389772dec0420a66767bb0af9dea3122e1cb0f
workflow-type: ht
source-wordcount: '1210'
ht-degree: 100%

---

# Importieren von [!UICONTROL Paid Search]-Metriken mithilfe von [!UICONTROL Datenquellen]

Für viele Marketing-Unternehmen ist Paid Search eine der wertvollsten und zuverlässigsten Methoden, um sowohl neue Kunden zu erreichen als auch bestehende zu binden. Die Funktion [!UICONTROL Datenquellen] in Adobe Analytics erleichtert den Import von erweiterten Paid-Search-Daten von digitalen Werbeplattformen wie Google AdWords. Sie können sie zusammen mit den Verhaltensdaten und Kundenattributen auf der Site in den Rest Ihrer Marketing-Daten integrieren, um Ihnen bessere Einblicke in die Paid Search-Bemühungen Ihres Unternehmens zu ermöglichen.

Diese Schritte zeigen Ihnen, wie Sie eine Integration mit AdWords konfigurieren können, um Keyword-Daten sowie Metriken wie Impressionen, Klicks, Kosten pro Klick und mehr zu importieren.

In den Schritten wird beschrieben, wie Sie einen einmaligen Import von Pay-per-Click-Daten einrichten. Allerdings ermöglicht [!UICONTROL Datenquellen] den fortlaufenden Import von Daten unter Verwendung des hier beschriebenen Dateiformats. Abhängig von Ihrer Paid-Search-Plattform können Sie unter Umständen regelmäßige Exporte planen (täglich, monatlich usw.), automatisierte Prozesse einrichten, um diese Exporte in das von Adobe Analytics benötigte Dateiformat umzuwandeln, und diese Dateien in Adobe Analytics hochladen, um Berichte zur Paid-Search-Integration zu erstellen.

## Voraussetzungen

* Sie haben die Erkennung von Paid Search implementiert.
* Sie erfassen Trackingcode-Daten.
* Sie verfügen für jede Anzeigengruppe über eindeutige Trackingcodes.

## Konfigurieren von [!UICONTROL Erfolgsereignissen]

Unser erster Schritt besteht darin, Adobe Analytics auf den Empfang der Metriken vorzubereiten. Dazu müssen Sie einige Erfolgsereignisse einrichten.

[!UICONTROL Erfolgsereignisse] sind Aktionen, die verfolgt werden können. Sie legen fest, was ein [!UICONTROL Erfolgsereignis] ist. Zu unseren Zwecken der Nachverfolgung von [!UICONTROL Paid Search]-Metriken sollten wir [!UICONTROL Erfolgsereignisse] für [!UICONTROL Klicks], [!UICONTROL Impressionen], [!UICONTROL Gesamtkosten] und aktivierte [!UICONTROL Trackingcodes] einrichten.

1. Navigieren Sie zu **[!UICONTROL Adobe Analytics > Admin > Report Suites]**.
1. Wählen Sie eine Report Suite aus.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten > Konversion > Erfolgsereignisse]**.

   ![Erfolgsereignisse](assets/success-events.png)

1. Unter „Benutzerdefinierte Erfolgsereignisse“ können Sie mit **[!UICONTROL Neu hinzufügen]** drei benutzerdefinierte Erfolgsereignisse definieren: [!UICONTROL Klicks] (Zähler), [!UICONTROL Impressionen] (Zähler) und [!UICONTROL Gesamtkosten] (Währung).

   ![Neues Erfolgsereignis](assets/new-success-events.png)

1. Klicken Sie auf „Speichern“.
Sie sollten eine Meldung erhalten, dass Ihre Speichervorgänge genehmigt wurden.
1. Navigieren Sie zu **[!UICONTROL „Admin“ > „Report Suites“ > „Einstellungen bearbeiten“ > „Konversion“ > „Konversionsvariablen“]**.
1. Aktivieren Sie Trackingcodes, indem Sie das Kontrollkästchen neben **[!UICONTROL Trackingcode]** unter **[!UICONTROL Kampagne > Kampagnenvariable]** aktivieren.

   ![Kampagnenvariable](assets/campaign-variable.png)

## Einrichten von Datenquellen

[!UICONTROL Datenquellen] ermöglichen es Ihnen, Nicht-Clickstream-Daten für Adobe Analytics freizugeben. In diesem Fall verwenden wir Adobe Analytics zur Verfolgung von Paid Search-Metriken. Wir verwenden den Trackingcode als Schlüssel, um die beiden Datenelemente (Paid-Search-Metriken und Adobe Analytics-Metriken) miteinander zu verbinden.

1. Navigieren Sie zu **[!UICONTROL „Adobe Analytics“ > „Admin“ > „Alle Administratoren“ > „Datenquellen“]**.
1. Wählen Sie die Registerkarte **[!UICONTROL Erstellen]**, um mit der Aktivierung neuer Datenquellen zu beginnen.
1. Wählen Sie unter **[!UICONTROL Kategorie auswählen]** die Option **[!UICONTROL Anzeigenkampagne]**.

   ![Datenquellen](assets/data-sources.png)

1. Wählen Sie unter **[!UICONTROL Typ auswählen]** die Option **[!UICONTROL Generischer Pay-Per-Click-Service]**.
1. Klicken Sie auf **[!UICONTROL Aktivieren]**.
Der [!UICONTROL Datenquellenaktivierungs-Assistent] wird angezeigt:

   ![Aktivierungsassistent](assets/ds-activation-wizard.png)

1. Klicken Sie auf **[!UICONTROL Weiter]** und benennen Sie Ihre Datenquelle. Dieser Name erscheint im Datenquellen-Manager.
1. Akzeptieren Sie die Service-Vereinbarung und klicken Sie auf **[!UICONTROL Weiter]**.
1. Wählen Sie die drei Standardmetriken aus: [!UICONTROL Impressionen], [!UICONTROL Klicks] und [!UICONTROL Gesamtkosten], und klicken Sie dann auf **[!UICONTROL Weiter]**.
1. Ordnen Sie nun diese neue Datenquelle den benutzerdefinierten Ereignissen zu, die wir in [Konfigurieren von Erfolgsereignissen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/t-success-events.md) erstellt haben.

   ![Zuordnen](assets/data-source-mapping.png)

1. Auswählen der Datendimensionen 
Aktivieren Sie das Kontrollkästchen neben „Trackingcodes“ und klicken Sie auf **[!UICONTROL Weiter]**.
1. Zuordnen der Datendimensionen.
Ordnen Sie die importierte Datendimension (Attribut) dem Adobe Analytics-Attribut zu, in dem Sie sie speichern möchten. Dies kann eine Standarddimension oder eine eVar sein. Nachdem Sie auf **[!UICONTROL Weiter]** geklickt haben, werden die resultierenden Zuordnungen in der Zusammenfassung angezeigt:

   ![Zusammenfassung](assets/data-source-summary.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Klicken Sie auf **[!UICONTROL Herunterladen]**, um die Vorlagendatei für diese Datenquelle herunterzuladen.
Der Dateiname entspricht dem ursprünglich angegebenen Datenquellentyp – in diesem Fall „Generic Pay-Per-Click Service template.txt“.
1. Öffnen Sie die Vorlage in Ihrem bevorzugten Texteditor.
Die Datei enthält bereits die Metriken und Dimensionen sowie deren Zuordnungen.

## Exportieren der PPC-Daten und Hochladen in Analytics

Diese Schritte funktionieren für Google Adwords, MSN, Yahoo und andere PPC-Konten.

### Exportieren von Daten

1. Melden Sie sich bei Ihrem PPC-Konto an und erstellen Sie einen neuen Bericht oder Export.
Stellen Sie sicher, dass der Export die folgenden Felder enthält: Datum, Ziel-URL (Landingpage), Impressionen, Klicks und Kosten. Der Export kann andere Felder enthalten, diese werden jedoch wie unten beschrieben gelöscht.
1. Wenn möglich, speichern Sie den Bericht als `.csv` oder tabulatorgetrennte Datei. Dies erleichtert die Arbeit in den folgenden Schritten.
1. Öffnen Sie die Datei in Microsoft Excel.

### Bearbeiten der Datei in Microsoft Excel

1. Löschen Sie in Microsoft Excel alle anderen Spalten als die oben genannten.
1. Löschen Sie alle zusätzlichen Zeilen oben.
1. So isolieren Sie die Trackingcodes von den Ziel-URLs: 
a. Kopieren Sie Daten aus allen Spalten und fügen Sie sie ein.
b. Klicken Sie auf **[!UICONTROL Daten > Text in Spalten]**.
c. Stellen Sie in Schritt 1 des Assistenten sicher, dass **[!UICONTROL Getrennt]** ausgewählt ist, und klicken Sie auf **[!UICONTROL Weiter]**.
d. Geben Sie in Schritt 2 des Assistenten das Trennzeichen an, je nachdem, wie Sie Ihre URLs erstellt haben (entweder ? oder &amp;) und klicken Sie auf **[!UICONTROL Weiter]**.
e. Zeigen Sie in Schritt 3 des Assistenten Ihre Daten in der Vorschau an und stellen Sie sicher, dass eine der Spalten „trackingcodename=trackingcode“ lautet. Wenn Sie zusätzliche Variablen haben, wiederholen Sie diese Schritte (mithilfe von &amp; als Trennzeichen).
f. Löschen Sie alle Spalten außer Trackingcodes, Impressionen, Klicks und Kosten. Fügen Sie eine neue Spalte mit dem Namen Datum hinzu und organisieren Sie Ihre Spalten in der folgenden Reihenfolge: Datum :: Trackingcode :: Impressionen :: Klicks :: Kosten.
1. Fügen Sie diese Daten zu der Vorlage hinzu, die Sie oben im Abschnitt „Einrichten von Datenquellen“ heruntergeladen haben.
Jetzt können Sie die Datei hochladen.

### Hochladen der Datei über FTP in Adobe Analytics

Gehen Sie zurück zum Datenquellen-Assistenten, um Anweisungen zu erhalten und die Datei via FTP hochzuladen:

![Hochladen über FTP](assets/upload-ftp.png)

## Erstellen von berechneten Metriken

Das Hinzufügen berechneter Metriken ist bei Pay-per-Click-Entscheidungen hilfreich.

Sie können beispielsweise diese [berechnete Metriken](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html?lang=de#calculated-metrics) hinzufügen:

| Name | Formel | Metriktyp | Beschreibung |
| --- | --- | --- | --- |
| Seitenansichten pro Besuch | Seitenansichten/Besuche | Numerisch | Wenn auf Site-Ebene angewandt: Zeigt die durchschnittliche Anzahl von Seiten pro Besuch. Wenn im Bericht „Bevorzugte Seiten“ angewandt: Zeigt, wie oft eine bestimmte Seite im Durchschnitt pro Besuch angezeigt wird. |
| Durchschnittlicher Bestellwert | Umsatz/Bestellungen | Währung | Zeigt den durchschnittlichen Umsatz pro Bestellung. |
| Umsatz pro Besuch | Umsatz/Besuch | Währung | Zeigt den durchschnittlichen Umsatz pro Besuch. |
| Clickthrough-Rate (CTR) | Klicks/Impressionen | Numerisch | Misst das Verhältnis von Klicks zu Impressionen einer Online-Werbe- oder E-Mail-Marketing-Kampagne. |
| Gewinn | Umsatz - Kosten | Währung | Zeigt den Umsatz einer Kampagne abzüglich der Kosten an. |
| Profit per Impression (PPI) | (Umsatz - Kosten)/Impression | Währung | Zeigt, wie viel Umsatz jedes Mal generiert wurde, wenn eine Anzeige angezeigt wurde, abgeglichen mit den Kosten. |
| Rendite auf Werbeausgaben (Return on Ad Spend, ROAS) | Umsatzbetrag/Werbeausgaben | Währung | (ROI) Gibt an, wie viel Euro pro Euro, der für die entsprechende Werbung ausgegeben wurde, verdient wurden. |

## Konfigurieren und Ausführen von Berichten

Der letzte Schritt besteht darin, die Datenquellenmetriken und alle berechneten Metriken zum Trackingcode-Bericht hinzuzufügen und einen Drilldown in eine Kampagne durchzuführen, um einen sofortigen Überblick über die Leistung jeder Anzeigengruppe zu erhalten.

1. Wählen Sie in **[!UICONTROL Adobe Analytics > Berichte]** die Report Suite aus, in die Sie Datenquellen importiert haben.
1. Navigieren Sie zu **[!UICONTROL Berichte > Kampagnen > Trackingcode > Trackingcode]**.
1. Wählen Sie den Datumsbereich aus.
1. Klicken Sie auf **[!UICONTROL Metriken > Hinzufügen]** und fügen Sie Ihre Datenquellenmetriken (Klicks, Impressionen, Gesamtkosten) aus der Liste der Standardmetriken hinzu.
1. Gehen Sie für jede berechnete Metrik, die Sie hinzugefügt haben, genauso vor. Der Bericht wird aktualisiert, sobald Sie Metriken hinzufügen.
