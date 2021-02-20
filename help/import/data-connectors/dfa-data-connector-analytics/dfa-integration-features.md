---
description: 'Bei Aktivierung stellt die Data Connectors-DFA-Integration folgende Metriken für Ihre Adobe Analytics-Berichte zur Verfügung '
keywords: DFA
title: Integrationsfunktionen
topic: Data connectors
uuid: 4ad8e6e8-3449-498a-8596-37c0ac1657cd
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 100%

---


# Integrationsfunktionen {#integration-features}

Bei Aktivierung stellt die Data Connectors-DFA-Integration folgende Metriken für Ihre Adobe Analytics-Berichte zur Verfügung:

* Durchsichten
* DFA-Klicks
* Impressionen
* (Optional) DFA-Kostendaten
* (Optional) DFA-Abfragefehler, Timeouts

>[!NOTE]
>
> In dieser Integration werden Klicktracker (zuvor Klickbefehle) nicht unterstützt. Mithilfe von Klicktrackern werden Klicks auf Textlinks, Links in E-Mails und andere hartcodierte Elemente auf Websites aufgezeichnet.

DFA-Trackingcodes werden von der Data Connectors-DFA-Integration automatisch aus den von DFA zurückgegebenen Daten erstellt. Durch diese Trackingcodes werden Anzeigen sowie die zugehörigen Platzierungen und kreativen Elemente eindeutig gekennzeichnet. Je nach Version der Integration wird im Folgenden die Zusammensetzung des Trackingcodes grob zusammengefasst. In Version 1.5 wird dieses Format verwendet:

![](assets/DFA_id_struct1_5.png)

In Version 2.0 dieses:

![](assets/DFA_id_struct2.png)

Diese IDs stellen einen gemeinsamen Schlüssel für Genesis und DFA dar, um die korrekten Classifications und Metriken zuzuordnen.

| Site-ID | Drittanbietersite, auf der die Anzeige gehostet wurde Die Sitenamen-Classification enthält einen beschreibenden Namen der Site-ID. |
|---|---|
| Anzeigen-ID | ID für die kommerzielle Botschaft, die an die Benutzer ausgeliefert wird In der Anzeigennamen-Classification ist der Name der Anzeige wie von Ihrer Organisation im DFA-System definiert enthalten. Beispiel: `Hybrid Coup Textlink - Build`. |
| Platzierungs-ID | Darstellung des von Ihnen erworbenen Anzeigenplatzes auf einer Website, eines Websiteteils oder einer Gruppe von Websites in Ihrem DFA-Konto |
| Creative-ID | Bild, Flash-SWF oder andere Ressource, das bzw. die Besuchern gezeigt wird Die Creative-Namen-Classification enthält den Namen, den Sie diesem kreativen Element in der DFA-Oberfläche gegebenen haben. |

Die anderen Classifications, das Bereitstellungswerkzeug (DoubleClick for Advertisers) und der Kanal (Banneranzeige) weisen für jede DFA-Kampagne dieselben Werte auf und tragen so zur Erkennung der importierten DFA-Daten bei.

## SearchCenter-Deduplizierung   {#section-f809b3bb5e5142aa8ff89bcd5f0d0e49}

Die DFA-Integration unterstützt nun Adobe SearchCenter. Wenn Sie die SearchCenter-Deduplizierung über den Data Connectors-Assistenten aktivieren, sorgen Besucher-Suchvorgänge nicht dafür, dass Daten vom DFA Floodlight-Server abgerufen werden. Zudem wird *`s.campaign`* nicht von DFA ausgefüllt, sodass SearchCenter diese ausfüllen kann. Außerdem werden die Variablen für jedes Produkt nun von DFA und SearchCenter durch Deduplizierungswerte ersetzt.

In der folgenden Liste wird die Logik zusammengefasst, die bei Aktivierung der SearchCenter-Deduplizierung zum Einsatz kommt:

Wenn Sie im Assistenten **[!UICONTROL DFA]** > **[!UICONTROL SearchCenter-Deduplizierung]** auswählen:

* Beim DFA-Clickthrough wird der die Zeichenfolge „DFA-Clickthrough“ von der Integration in die eingestellte SCM-eVar eingespeist.
* Im Falle einer DFA-Durchsicht wird die Zeichenfolge „DFA-Durchsicht“ von der Integration in die eingestellte SCM-eVar eingespeist.

Wenn Sie im Assistenten **[!UICONTROL SearchCenter]** > **[!UICONTROL DFA-Deduplizierung]** auswählen:

* Im Falle einer DFA-Durchsicht wird die Zeichenfolge „DFA-Durchsicht“ von der Integration in die eingestellte SCM-eVar eingespeist.

>[!NOTE]
>
>Bei aktivierter SearchCenter > DFA-Deduplizierung und eingestelltem SearchCenter-Abfragezeichenfolgenparameter wird der Besuch bei der DFA-Verarbeitung nicht beachtet. Der SearchCenter-Abfragestringparameter sollte sich also vom DFA-Clickthrough-Parameter unterscheiden und keine Display-Anzeigen sollten den SearchCenter-Abfragestringparameter bestimmen.

