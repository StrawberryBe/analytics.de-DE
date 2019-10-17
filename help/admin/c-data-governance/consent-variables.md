---
description: Variablen für Datenschutzberichte in der Datenschutzrichtlinie.
seo-description: Variablen für Datenschutzberichte in der Datenschutzrichtlinie.
seo-title: Variablen für Datenschutzberichte
solution: Analytics
title: Variablen für Datenschutzberichte
topic: Admin Tools
translation-type: tm+mt
source-git-commit: 4d3577cc87b95da41275552efe7fc70bcc23e023

---


# Variablen für Datenschutzberichte

Um zusätzliche Unterstützung bei der Verwaltung von Datenschutzdaten zu bieten, stehen eine Reihe reservierter Variablen zur Verfügung, die zusammen mit bestimmten Kontextdatenvariablen verwendet werden können.
Diese Variablen für die Datenschutzberichterstellung bieten ein benutzerfreundliches Framework zur Erfassung des Datenschutzstatus bei jedem Treffer in der Analyse.

## Variablen

* Einwilligungsmanagement Opt-out
   * Reservierte Variable: Listen-Prop
   * Typ: Kommagetrennte Zeichenfolge
   * Enthält:
      * `contextData.['cm.ssf']=1` angezeigt als SSF
      * `contextData.['opt.dmp']=N` angezeigt als DMP
      * `contextData.['opt.sell']=N` als SELL angezeigt

* Einwilligungsmanagement Opt-in
   * Reservierte Variable: Listen-Prop
   * Typ: Kommagetrennte Zeichenfolge
   * Enthält:
      * `contextData.['opt.dmp']=Y` angezeigt als DMP
      * `contextData.['opt.sell']=Y` als SELL angezeigt

## Berichterstellung  

Sie können die Datenschutzberichtsvariablen über eine neue Datenschutzeinstellung aktivieren, die in der Analytics Admin-Konsole verfügbar ist.

Jede Report Suite kann wie folgt konfiguriert werden:
1. In Reports &amp; Analytics click **[!UICONTROL Admin &gt; Report Suites.]**
1. Select the report suite(s) where you are collecting media data and click **[!UICONTROL Edit Settings &gt; Privacy Management.]**

   ![](assets/rsm-privacy-select.png)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Datenschutzberichte]** aktivieren. **** Hinweis: Nach der Aktivierung können diese Variablen nicht deaktiviert werden.

   ![](assets/rsm-privacy-enable.png)

1. Nach der Aktivierung wird eine Bestätigungsmeldung angezeigt.

   ![](assets/rsm-privacy-config.png)

1. Die reservierten Variablen stehen jetzt für die Berichterstellung zur Verfügung.  Siehe Opt-out- und Zustimmungsverwaltung für die Verwaltung.

   ![](assets/rsm-privacy-reports.png)

## Implementierung

Drei Kontextdatenvariablen wurden vordefiniert, um mit den vom Datenschutzmanagement reservierten Variablen zu arbeiten.  Es ist Sache jedes Implementierungstechnikers, zu bestimmen, wie die Einstellung dieser Variablen verwaltet und beibehalten wird.

Allgemeine Anleitungen zur Implementierung von Kontextdatenvariablen finden Sie unter [Kontextdatenvariablen](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/context-data-variables.html) .

### SSF

* Kontextdaten: contextData.["cm.ssf"]
* Akzeptierte Werte:
   * 1 - Wenn der Wert "1"gesendet wird, bedeutet dies, dass die serverseitige Weiterleitung einen Ausschluss-Status aufweist. Der Wert "1"in Verbindung mit dieser Variablen blockiert die Freigabe dieses Treffers für Adobe Audience Manager. Siehe [AAM-Datenschutzbestimmungen.](https://docs.adobe.com/help/en/analytics/integration/audience-analytics/audience-analytics-workflow/ssf-gdpr.html)
   * Für diesen Parameter werden keine anderen Werte akzeptiert.

### DMP

* Kontextdaten: contextData.['opt.dmp']
* Akzeptierte Werte:
   * N - Wenn der Wert "N"gesendet wird, deutet dies darauf hin, dass der Verbraucher die Freigabe für Datenverwaltungsplattformen ablehnt. **** Hinweis: Wenn diese Variable auf "N"gesetzt wird, wird die Freigabe für AAM derzeit nicht blockiert. Anfang 2020 wird jedoch das Blockieren von AAM-Aufrufen hinzugefügt. Adobe empfiehlt zunächst, sowohl das Senden von Treffern an AAM festzulegen `c.cm.ssf=1` als auch `c.opt.dmp=N` zu verhindern.
   * Y - Wenn der Wert "Y"gesendet wird, deutet dies darauf hin, dass sich der Verbraucher für die Freigabe an Datenverwaltungsplattformen entscheidet.

### SELL

* Kontextdaten: contextData.['opt.sell']
* Akzeptierte Werte:
   * N - Wenn der Wert "N" gesendet wird, deutet dies darauf hin, dass der Verbraucher die Freigabe oder den Verkauf der Daten an Dritte ablehnt.
   * Y - Wenn der Wert "Y"gesendet wird, deutet dies darauf hin, dass der Verbraucher sich für die Freigabe oder den Verkauf der Daten an Dritte entscheidet.
