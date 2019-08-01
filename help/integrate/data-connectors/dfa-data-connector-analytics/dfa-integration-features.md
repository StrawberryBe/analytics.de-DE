---
description: 'Bei Aktivierung stellt die Data Connectors-DFA-Integration folgende Metriken für Ihre Adobe Analytics-Berichte zur Verfügung '
keywords: DFA
seo-description: 'Bei Aktivierung stellt die Data Connectors-DFA-Integration folgende Metriken für Ihre Adobe Analytics-Berichte zur Verfügung '
seo-title: Integrationsfunktionen
solution: Analytics
title: Integrationsfunktionen
topic: Data Connectors
uuid: 4 ad 8 e 6 e 8-4449-498 a -8596-37 c 0 ac 1657 cd
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Integrationsfunktionen{#integration-features}

Bei Aktivierung stellt die Data Connectors-DFA-Integration folgende Metriken für Ihre Adobe Analytics-Berichte zur Verfügung:

* Durchsichten
* DFA-Klicks
* Impressionen
* (Optional) DFA-Kostendaten
* (Optional) DFA-Abfragefehler, Timeouts

>[!NOTE]
>
>Diese Integration bietet keine Unterstützung für Klicktracker (zuvor Klickbefehle). Mithilfe von Klicktrackern werden Klicks auf Textlinks, Links in E-Mails und andere hartcodierte Elemente auf Websites aufgezeichnet.

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

## SearchCenter-Deduplizierung {#section-f809b3bb5e5142aa8ff89bcd5f0d0e49}

Die DFA-Integration unterstützt nun Adobe SearchCenter. Wenn Sie die SearchCenter-Deduplizierung im Data Connectors-Assistenten aktivieren, werden zu Besuchern, die von der Suche beeinflusst wurden, keine Daten vom DFA Floodlight-Server abgefragt und *`s.campaign`* nicht von DFA, sondern von SearchCenter ausgefüllt. Außerdem werden die Variablen für jedes Produkt nun von DFA und SearchCenter durch Deduplizierungswerte ersetzt.

In der folgenden Liste wird die Logik zusammengefasst, die bei Aktivierung der SearchCenter-Deduplizierung zum Einsatz kommt:

If **[!UICONTROL DFA]** &gt; **[!UICONTROL SearchCenter deduplication]** is selected in the wizard:

* Beim DFA-Clickthrough wird der String „DFA-Clickthrough“ von der Integration in die eingestellte SCM-eVar eingespeist.
* Bei einer DFA-Durchsicht wird der String „DFA-Durchsicht“ von der Integration in die eingestellte SCM-eVar eingespeist.

If **[!UICONTROL SearchCenter]** &gt; **[!UICONTROL DFA deduplication]** is selected in the wizard:

* Bei einer DFA-Durchsicht wird der String „DFA-Durchsicht“ von der Integration in die eingestellte SCM-eVar eingespeist.

>[!NOTE]
>
>Wenn searchcenter &gt; DFA Deduplizierung aktiviert ist und der searchcenter-Abfragezeichenfolgenparameter festgelegt ist, wird der Besuch für die DFA-Verarbeitung nicht berücksichtigt. Der SearchCenter-Abfragestringparameter sollte sich also vom DFA-Clickthrough-Parameter unterscheiden und keine Display-Anzeigen sollten den SearchCenter-Abfragestringparameter bestimmen.

