---
description: Erläutert Optimierungen der Server-seitigen Weiterleitung, die durch die EU-Cookie-Richtlinie veranlasst wurden.
title: DSGVO/ePrivacy – Einhaltung und serverseitige Weiterleitung
feature: Server-Side Forwarding
exl-id: 54e43a16-8f15-4ee8-9aa2-579af30be2c9
role: Admin
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 55%

---

# DSGVO/ePrivacy – Einhaltung und serverseitige Weiterleitung

In diesem Abschnitt werden Optimierungen an der Server-seitigen Weiterleitung erläutert, die durch die [EU-Cookie-Richtlinie](https://wikis.ec.europa.eu/display/WEBGUIDE/04.+Cookies+and+similar+technologies) erforderlich wurden, die am 30. September 2017 in Kraft trat.

Die serverseitige Weiterleitung wird verwendet, um Daten in Echtzeit von Adobe Analytics zu anderen [!DNL Experience Cloud Solutions] wie Audience Manager zu übertragen. Bei entsprechender Aktivierung ermöglicht die Server-seitige Weiterleitung während des Datenerfassungsprozesses Analytics das Übergeben von Daten an andere Experience Cloud-Lösungen und diesen Lösungen das Übergeben von Daten an Analytics.

Zuvor gab es bei der Server-seitigen Weiterleitung keine Möglichkeit zur Unterscheidung zwischen Ereignissen/Treffern vor und nach einer erfolgten Zustimmung. Ab dem 1. November 2018 haben Sie als Datenverantwortlicher (Adobe Analytics-Kunde) die Möglichkeit, Daten vor der Einwilligung auf Adobe Analytics zu beschränken und zu verhindern, dass sie an Adobe Audience Manager weitergeleitet werden. Eine neue Variable im Implementierungskontext ermöglicht es, die Treffer zu kennzeichnen, bei denen noch keine Zustimmung erfolgt ist. Wenn diese Variable festgelegt ist, verhindert sie, dass diese Treffer an Adobe Audience Manager gesendet werden, bis die Einwilligung eingeholt wurde.

Wenn diese neue Kontextvariable `cm.ssf=1`, bei einem Treffer vorhanden ist, wird dieser Treffer gekennzeichnet und nicht serverseitig an Adobe Audience Manager weitergeleitet. Wenn diese Zeichenfolge hingegen bei einem Treffer nicht angezeigt wird, wird der Treffer an Adobe Audience Manager weitergeleitet.

Die serverseitige Weiterleitung erfolgt bidirektional, d. h. wenn sie auf einen Treffer angewendet wird und dieser Treffer an Adobe Audience Manager weitergeleitet wird, erhält Audience Analytics Segmentinformationen für diesen Treffer von Adobe Audience Manager und sendet ihn zurück an Analytics. Daher werden Treffer, die nicht serverseitig von Analytics an Adobe Audience Manager weitergeleitet werden, nicht mit der Liste der Segment-IDs aus Adobe Audience Manager angereichert. Daher gibt es eine Untergruppe von Traffic/Treffern, die keine Segment-ID-Informationen von Adobe Audience Manager erhalten.

## Implementierungsdetails {#section_FFA8B66085BF469FAB5365C944FE38F7}

Befolgen Sie abhängig von Ihrer Implementierungsmethode die folgenden Schritte.

| Implementierungsmethode | Schritte |
|--- |--- |
| Tags in Adobe Experience Platform | Wenn Sie die Adobe Analytics-Erweiterung installiert haben, fügen Sie dem benutzerdefinierten Code-Editor innerhalb der Aktionskonfiguration einer Regel die folgende Definition für Kontextdatenvariablen hinzu: <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/> Hinweis: Definieren Sie die Kontextdatenvariable und legen Sie dafür den Wert „1“ fest, wenn ein Kunde gezieltem Marketing nicht zustimmt. Legen Sie für die `contextdata`-Variable den Wert *0* für Kunden fest, die gezieltem Marketing zugestimmt haben. |
| AppMeasurement | Fügen Sie der Datei &quot;AppMeasurement.js&quot;die Kontextdatenvariablendefinition hinzu:  <br/>`s.contextData['cm.ssf']&nbsp;=&nbsp;'1' ` <br/>Hinweis: Definieren Sie die Kontextdatenvariable und legen Sie dafür den Wert &quot;1&quot;fest, wenn ein Kunde gezieltem Marketing nicht zustimmt. Legen Sie für die Kontextdatenvariable den Wert „0“ für Kunden fest, die gezieltem Marketing zugestimmt haben. |

## Reporting (optional) {#section_6AD4028EC11C4DABA2A34469DDC99E89}

Sie können Adobe Analytics verwenden, um Berichte dazu zu erstellen, wie viel Ihres Traffics auf der Zustimmung basiert und somit serverseitig weitergeleitet wurde, im Vergleich dazu, wie viel Ihres Traffics nicht auf der Zustimmung basiert und nicht an Adobe Audience Manager weitergeleitet wurde.

Um diese Art der Berichterstellung zu konfigurieren, weisen Sie die neue Kontextvariable über Verarbeitungsregeln einer benutzerdefinierten Traffic-Variable (Eigenschaft) hinzu. Gehen Sie dazu wie folgt vor

1. Implementieren Sie die Variable „cm.ssf“ (wie oben dargestellt.)
1. [Aktivieren Sie die Eigenschaft.](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md)
1. Weisen Sie die Kontextvariable über Verarbeitungsregeln der Eigenschaft hinzu.

   1. Gehen Sie zu **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**. Wählen Sie dann eine Report Suite aus.
   1. Klicken Sie auf **[!UICONTROL Report Suite bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Verarbeitungsregeln]**.
   1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]**.
   1. Überschreiben Sie unter **[!UICONTROL Immer ausführen]** den Wert der über die Kontextvariable „cm.ssf(Context Data)“ aktivierten Kontextvariable.
   1. Klicken Sie auf **[!UICONTROL Speichern]**.
