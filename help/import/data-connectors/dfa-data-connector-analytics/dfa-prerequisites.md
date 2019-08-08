---
description: 'null '
keywords: DFA
seo-description: 'null '
seo-title: Voraussetzungen
solution: Analytics
title: Voraussetzungen
topic: Data Connectors
uuid: b 5 f 5 e 30 c-e 269-41 a 4-9236-5 ddc 404 bfd 94
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Voraussetzungen{#prerequisites}

Führen Sie vor dem Start der Adobe Data Connectors-Integration für DFA folgende Schritte durch:

* Entscheiden Sie, ob Sie die Integration mit Version 1.5 durchführen oder auf Version 2.0 warten möchten. Das hängt davon ab, welche Funktionen in Ihrem DFA-Konto verwendet werden und in welchem Zeitrahmen Sie die Integration durchführen möchten. Weitere Informationen finden Sie unter [Info zu Version 2.0](../dfa-data-connector-analytics/dfa-version-differences.md#concept-2c7d6a6ab8524dccad96ea0c17228664).
* Entscheiden Sie, wie DFA-Advertiser Zuordnungen zu Adobe Analytics-Report Suites durchführen sollen. Wenn Sie beispielsweise über mehrere DFA-Advertiser und mehrere Report Suites verfügen, müssen Sie entscheiden, welche Advertiser welchen Report Suites zugeordnet werden.
* Verwenden Sie Version H.22 oder neuer des Adobe-Datenerfassungscodes auf allen Seiten, die getrackt werden sollen.
* Informieren Sie sich über die Advertiser-ID eines DFA-Kontos, das Teil der zu integrierenden Floodlight-Konfiguration ist. Durch die Integration werden alle Advertiser innerhalb der Floodlight-Konfiguration automatisch importiert.
* Informieren Sie sich über Benutzernamen und Passwort Ihres DFA-Kontos.
* Teilen Sie jeden DFA-Advertiser nur einer Adobe Analytics-Report Suite zu. Tagging mit mehreren Report Suites ist in der Genesis-Standardintegration für DFA nicht möglich.
* Fügen Sie jeder Landingpage einen Clickthrough-Abfragestringparameter für jede DFA-Platzierung hinzu, die Teil der Integration ist. Dieser Abfragestringparameter ist für die korrekte Zählung der Clickthroughs erforderlich.
* Konfigurieren Sie Ihre DFA-Platzierungen, sodass Besucher nicht durch mehrere Domänen weitergeleitet werden. Besucher sollten also durch eine Platzierung nicht auf eine Microsite unter www.xyz.com weitergeleitet werden, wenn sie von dort anschließend auf eine andere Site, zum Beispiel www.fgh.com, weitergeleitet werden. Enthält die Kampagnenreaktion also mehrere Domänen, können Clickthrough- und Durchsichtsdaten erhöht und verfälscht werden.
* Legen Sie in Reports &amp; Analysen eine benutzerdefinierte Variable fest, in der Ihre Kampagneninformationen enthalten sind.
* Identifizieren Sie eine Reports &amp; Analysen-eVar, um DFA-Durchsichtsinformationen zu speichern. Verwenden Sie diese eVar ausschließlich für diese DFA-Integration.
* Bestimmen Sie die Reports &amp; Analysen-Ereignisse, in denen Sie Impressions- und Klickdaten speichern möchten. Möglicherweise empfiehlt es sich, die Ereignisse entsprechend umzubenennen.
* (Optional) Legen Sie die Reports &amp; Analysen-Ereignisse zum Speichern von DFA-Kostendaten fest. Möglicherweise empfiehlt es sich, die Ereignisse entsprechend umzubenennen.
* (Optional) Bestimmen Sie eine benutzerdefinierte Reports &amp; Analysen-Variable sowie ein Erfolgsereignis zum Speichern von DFA-Fehlern und Timeouts. Mithilfe dieser Variablen können Sie Probleme erkennen, die bei der Integration auftreten können.
* (Optional) Legen Sie ein gesondertes E-Mail-Konto für Informationen und Benachrichtigungen zur Data Connectors DFA-Integration an.

