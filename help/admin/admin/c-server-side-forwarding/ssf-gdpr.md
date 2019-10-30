---
description: 'null'
seo-description: 'null'
seo-title: GDPR/ePrivacy Compliance und serverseitige Weiterleitung
title: GDPR/ePrivacy Compliance und serverseitige Weiterleitung
uuid: 1b90c567-3321-4dbd-a699-38c04e809fa4
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# GDPR/ePrivacy Compliance und serverseitige Weiterleitung

In diesem Abschnitt werden kürzlich erfolgte Optimierungen an der serverseitigen Weiterleitung erläutert, die durch die [EU-Cookie-Richtlinie](https://ec.europa.eu/ipg/basics/legal/cookies/index_en.htm) erforderlich wurden, die am 30. September 2017 in Kraft trat.

Server-side forwarding is used to share data from Adobe Analytics to other [!DNL Experience Cloud Solutions], such as Audience Manager, in real time. Bei entsprechender Aktivierung ermöglicht die serverseitige Weiterleitung während des Datenerfassungsprozesses Analytics das Übergeben von Daten an andere Experience Cloud-Lösungen und diesen Lösungen das Übergeben von Daten an Analytics.

Bis vor Kurzem gab es bei der serverseitigen Weiterleitung keine Möglichkeit zur Unterscheidung zwischen Ereignissen/Treffern vor und nach einer erfolgten Zustimmung. Ab dem 1. November 2018 hatten Sie als Datenverantwortlicher (Adobe Analytics-Kunde) die Möglichkeit, die vor einer erfolgten Zustimmung zugänglichen Daten auf Adobe Analytics zu beschränken sowie die serverseitige Weiterleitung an AAM zu unterbinden. Eine neue Variable im Implementierungskontext ermöglicht es, die Treffer zu kennzeichnen, bei denen noch keine Zustimmung erfolgt ist. Diese Variable, sofern festgelegt, verhindert, dass die Treffer vor einer Zustimmung an AAM weitergeleitet werden.

When this new context variable, `cm.ssf=1`, exists on a hit, this hit gets flagged and does not get server-side-forwarded to AAM. Taucht die Zeichenfolge hingegen nicht bei einem Treffer auf, wird der Treffer an AAM weitergeleitet.

Die serverseitige Weiterleitung ist bidirektional, d. h. wenn sie auf einen Treffer angewendet und dieser Treffer an AAM weitergeleitet wird, erhält Audience Analytics Segmentinformationen für diesen Treffer von AAM und sendet diese zurück an Analytics. Aus diesem Grund werden Treffer, die nicht serverseitig von Analytics an AAM weitergeleitet werden, nicht mit der Liste von Segment-IDs aus AAM versehen. Aus diesem Grund gibt es einen Teilsatz von Traffic/Treffern, die keine Segment-ID-Informationen von AAM erhalten.

## Implementierungsdetails {#section_FFA8B66085BF469FAB5365C944FE38F7}

Befolgen Sie abhängig von Ihrer Implementierungsmethode die folgenden Schritte.

| Implementierungsmethode | Schritte |
|--- |--- |
| Adobe Experience Platform Launch | Wenn Sie die Adobe Analytics-Erweiterung installiert haben, fügen Sie in der Aktionskonfiguration einer Regel die folgende Definition der Kontextdatenvariablen zum benutzerdefinierten Code-Editor hinzu: <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Hinweis:  Definieren Sie die contextData-Variable und setzen Sie sie auf 1, wenn ein Kunde dem zielgerichteten Marketing nicht zustimmt. Set the `contextdata` variable to *0* for customers who consented to targeted marketing. |
| DTM | Fügen Sie die Kontextdatenvariable im Editor für benutzerdefinierte Seiten-Codes hinzu: <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Hinweis: Definieren Sie die Kontextdatenvariable und legen Sie dafür den Wert „1“ fest, wenn ein Kunde gezieltem Marketing nicht zustimmt. Legen Sie für die Kontextdatenvariable den Wert „0“ für Kunden fest, die gezieltem Marketing zugestimmt haben. |
| AppMeasurement | Fügen Sie die Kontextdatenvariablendefinition zur Datei „AppMeasurement.js“ hinzu:  <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Hinweis: Definieren Sie die Kontextdatenvariable und legen Sie dafür den Wert „1“ fest, wenn ein Kunde gezieltem Marketing nicht zustimmt. Legen Sie für die Kontextdatenvariable den Wert „0“ für Kunden fest, die gezieltem Marketing zugestimmt haben. |

## Berichterstellung (Optional) {#section_6AD4028EC11C4DABA2A34469DDC99E89}

Sie können Adobe Analytics verwenden, um Berichte darüber zu erstellen, wie viel Traffic auf der Zustimmung basiert und infolgedessen serverseitig weitergeleitet wurde, im Gegensatz dazu, wie viel Traffic nicht auf der Zustimmung basiert und nicht an AAM weitergeleitet wurde.

Um diese Art der Berichterstellung zu konfigurieren, weisen Sie die neue Kontextvariable über Verarbeitungsregeln einer benutzerdefinierten Traffic-Variable (Eigenschaft) hinzu. Gehen Sie dazu wie folgt vor

1. Implementieren Sie die Variable "cm.ssf"(wie oben gezeigt).
1. [Aktivieren Sie die Eigenschaft.](/help/admin/admin/c-traffic-variables/traffic-var.md)
1. Weisen Sie die Kontextvariable über Verarbeitungsregeln der Eigenschaft hinzu.

   1. Go to  **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** , then select a report suite.
   1. Click  **[!UICONTROL Edit Report Suite]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Processing Rules]** .
   1. Klicken Sie auf **[!UICONTROL Regel hinzufügen.]**
   1. Under **[!UICONTROL Always Execute]**, overwrite the value of the prop you had enabled with the context variable "cm.ssf(Context Data)".
   1. Klicken Sie auf **[!UICONTROL Speichern]**.

