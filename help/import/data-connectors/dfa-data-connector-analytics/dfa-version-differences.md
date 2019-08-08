---
description: 'Momentan stehen drei Versionen der DFA-Integration zur Verfügung: 1.0, 1.5 und 2.0.'
keywords: DFA
seo-description: 'Momentan stehen drei Versionen der DFA-Integration zur Verfügung: 1.0, 1.5 und 2.0.'
seo-title: Versionsunterschiede
solution: Analytics
title: Versionsunterschiede
topic: Data Connectors
uuid: e 0 ae 70 f 0-369 d -451 a -9752-02660 d 270660
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Versionsunterschiede{#version-differences}

Momentan stehen drei Versionen der DFA-Integration zur Verfügung: 1.0, 1.5 und 2.0.

In der folgenden Tabelle sind die Funktionen jeder Version der Integration zusammengefasst.

| Funktion | Version 1.0 | Version 1.5 | Version 2.0 |
|---|---|---|---|
| Nächtliche DFA-Klick- und Impressionsmetriken | Ja | Ja | Ja |
| Clickthrough- und Durchsichtstracking | Ja | Ja | Ja |
| Eingang von Daten bei der Integration auf Advertiser-Ebene | Nein | Ja | Ja |
| Eingang von Daten bei der Integration auf Floodlight-Konfigurationsebene | Nein | Nein | Ja |
| Kostenmetriken | Nein | Nein | Ja |
| Creative-Metriken | Nein | Nein | Ja |
| Abfragestrings über 2.000 Bytes | Nein | Ja | Ja |
| Verwendung des Integrate-Moduls für optimale Drittanbieterdatenerfassung | Nein | Ja | Ja |
| Timeout- und Fehlertracking | Nein | Ja | Ja |
| Keine ausgehandelte Client-Site-ID erforderlich | Nein | Nein | Ja |

## Info zu Version 1.5 {#section-b5a3e967cfa141ea8f740612336181be}

In Version 1.5 der Integration wird das Integrate-Modul für Landingpage-JavaScript eingeführt. Das Integrate-Modul ermöglicht Abfragen des DFA-Anzeigenservers (ad.doubleclick.net) mit fester Größe. Dadurch wird die Abfragenbeschränkung auf 2.000 Bytes der Vorgängerversion umgangen. Außerdem wird mit ihr der verstellbare Timeoutwert *`s.maxDelay`*, um weiterhin Adobe-Besucherdaten zu erfassen, wenn Netzwerkausfälle auftreten. Fehler und Timeouts können auch in Analytics-Variablen erfasst werden.

Auf der folgenden Abbildung sehen Sie Netzwerkinteraktionen auf der Landingpage in Version 1.5.

![](assets/DFA_About_1_5.png)

Das Integrate-Modul (2) fragt in Version 1.5 Daten vom Floodlight-Server (3) ab. Der Floodlight-Server veranlasst eine Weiterleitung auf den DFA-Anzeigenserver, von dem aus Besucherdaten auf dieselbe Weise zurückgegeben werden wie in Version 1.0. Es erfolgt eine 302-Weiterleitung (4) zu einem speziellen Übersetzungsservice auf integrate.112.2o7.net, durch den die Reaktionsstruktur in ein JSON-Objekt übertragen wird. Das Integrate-Modul nimmt dieses JSON-Objekt auf und gibt die Information an das Adobe-Tracking (5) weiter.

Bei einem Wechsel von Version 1.0 der Integration auf Version 1.5 gibt es eine JavaScript-Änderung. Sie können dieses JavaScipt aufrufen, indem Sie sich bei Ihrem Adobe Online Marketing Suite-Konto anmelden, das Genesis-Produkt auswählen, in Ihrer DFA-Integration auf „Bearbeiten“ klicken und mit dem Assistenten fortfahren. Wenn zuvor eine Client-Site-ID zugewiesen wurde, erhalten Sie sofort einen neuen JavaScript-Code per E-Mail, sobald Sie die Integration speichern. Wenn Sie diesen Code erhalten haben, benötigen Sie außerdem eine neue Version des Kern-„s_code“ mit dem Integrate-Modul. Sie erhalten diesen Code von Ihrem Kundenbetreuer oder Implementationsberater.

Ein wichtiger Aspekt des neuen JavaScript-Codes ist, dass zwischen Version 1.5 und 2.0 keine Implementationsänderungen notwendig sind.

## Info zu Version 2.0 {#section-afd56de0c56c4489bb5ddc5798d6709a}

Durch die neueste Version der DFA-Integration gelangen Daten einer ganzen Floodlight-Konfiguration in die Integration. Vor Version 2.0 waren einzelne Integrationen an einzelne DFA-Advertiser gebunden. Durch diese Änderungen werden Klicks, Impressionen und Kostenmetriken für die gesamte Floodlight-Konfiguration in die Integrations-Report Suite eingebunden. Sie können außerdem siteübergreifende Durchsichten tracken, wenn sich die beiden Sites innerhalb derselben Floodlight-Konfiguration befinden. 

Ab Version 2.0 der Integration sind des Weiteren auch Metriken zu Medienkosten verfügbar. Sie müssen im Genesis-Assistenten ein Reports &amp; Analysen-Ereignis für Medienkosten wählen und die Währung für die Metrikangaben in der DFA-Oberfläche festlegen, um Metriken zu Medienkosten für eine Integration zu aktivieren.

Unter Version 2.0 der Integration wird die Anzahl der Timeouts voraussichtlich abnehmen, da die 302-Weiterleitungen wegfallen. Durch den Wegfall dieser Sprünge sollten weniger Timeouts auftreten und die Anzahl der DFA-Daten, die Sie integrieren können, sollte zunehmen.

Wenn es sich bei einer Floodlight-Konfiguration um eine in DFA freigegebene Konfiguration handelt, werden durch ein Upgrade von Version 1. 5 auf 2.0 Konversionsdaten aller freigegebenen Advertiser in der Floodlight-Konfiguration in die Report Suite eingeschlossen.

## Upgrade auf Version 2.0 {#section-f0bf90b9a7a1434ab1540b6c0999f4c7}

In der folgenden Tabelle sind die Inhaber der Migration auf neue Versionen der Integration zusammengefasst:

| Migration | Inhaber | Aufgaben |
|---|---|---|
| Version 1.0 auf 1.5 | Client | Implementierung von JavaScript für Version 1.5 in das Integrate-Modul |
| Version 1.5 auf 2.0 | Client | Beginn der Kommunikation des Clients mit Google zu Zeitrahmen für das Upgrade Aktivierung des erweiterten AdServings durch Google nach Genehmigung |

