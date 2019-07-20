---
description: 'Erfolgsereignisse sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Beispiel: Wenn ein Besucher einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden..'
keywords: event
seo-description: 'Erfolgsereignisse sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Beispiel: Wenn ein Besucher einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden..'
seo-title: Übersicht über Erfolgsereignisse
solution: Analytics
title: Übersicht über Erfolgsereignisse
topic: Admin Tools
uuid: 410 eee 44-8960-462 c-a 9 c 3-7 b 44 d 0 b 1 b 0 df
translation-type: tm+mt
source-git-commit: a1213919de61a72c06ec5518e72a714c76c6859f

---


# Übersicht über Erfolgsereignisse

Erfolgsereignisse sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Beispiel: Wenn ein Besucher einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden..

Es gibt, je nach Ihrem Websitetyp, viele Arten von Erfolgsereignissen. Zu diesen Arten zählen beispielsweise:

* **Einzelhandel**: Produktaufruf, Checkout, Kauf
* **Medien**: Abonnement, Wettbewerbsanmeldung, Seitenaufruf, Videoaufruf
* **Finanzen**: Applikationseinreichung, Anmeldung, Nutzung von Self-Service-Tools
* **Reisen**: Reservierung (Kauf), interne Kampagne (Clickthrough), Suche (Preisberechnung)
* **Telekommunikation**: Kauf, Leads, Nutzung von Self-Service-Tools
* **High Tech**: Download von White Papers, Gebotsanfragen, Formularausfüllung, Supportanfragen
* **Automotive**: Leadeinsendung, Preisanfrage, Download von Broschüren

Die Variable [s.events](https://marketing.adobe.com/resources/help/en_US/sc/implement/events.html) definiert ein Erfolgsereignis.

## Seite „Erfolgsereignisse“ – Beschreibungen {#section_681ECEC981694CABBDBF00E18165B447}

**[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; **[!UICONTROL Einstellungen bearbeiten]** &gt; **[!UICONTROL Konversion]** &gt; **[!UICONTROL Erfolgsereignisse]**

Auf der Seite „Erfolgsereignisse“ können Sie die auf der Site verwendeten Ereignisvariablen konfigurieren. Sie können bis zu 1.000 Erfolgsereignisse hinzufügen. Die Ereignisse 81–1.000 sind nur bei H22-Code oder höher verfügbar.

| Element | Beschreibung |
|--- |--- |
| Ereignis | Der ursprüngliche Name des Ereignisses. |
| Name | Verwenden Sie aussagekräftige Namen für die auf Ihrer Website genutzten Erfolgsereignisse. Wenn beispielsweise Ereignis1 zur Nachverfolgung von Registrierungen verwendet wird, können Sie hier den Namen ändern, damit es in sämtlichen Konversionsberichten als „Registrierungen“ angezeigt wird. |
| Typ | Je nach ausgewähltem Typ handelt es sich um ein Zählerereignis (Standard), ein numerisches Ereignis oder ein Währungsereignis. Bei numerischen Ereignissen und Währungsereignissen können die Metriken um einen anderen Wert als 1 erhöht werden.  Zählerereignisse halten Ereignisse in der Zeit fest, Währungsereignisse dagegen eine Dezimalzahl (z. B. Steuern oder Versandkosten). Der in die Währungsereignisse einfließende Wert wird bei Eingang von der Seitenwährung in die Basiswährung der Report Suite konvertiert. Weitere Informationen zur Verwendung von Währungsereignissen erhalten Sie bei Ihrem Adobe-Support-Mitarbeiter. Numerische Ereignisse werden für Berichte zu anderen Zahlen als Währungsangaben verwendet, z. B. für die Zahl der bei einer Bestellung verwendeten Gutscheine. Währungsereignisse werden zur Nachverfolgung von Steuern und Versandkosten verwendet. Ereignisse im Standardtyp von „Data Sources“ müssen numerische oder Währungsereignisse sein. |
| Polarität | Anhand der Metrikpolarität können Sie festlegen, ob Adobe Analytics es als positiv oder negativ interpretieren soll, wenn ein benutzerspezifisches Ereignis (Metrik) ansteigt. So kann Adobe Analytics Trendanzeigen (Pfeile) für verschiedene Metriken einbinden und mehr Kontext bieten (z. B. Vergleich über mehrere Wochen).  Beispiele: Wenn die Metrik „Übermittelte Bugs“ über mehrere Wochen ansteigt, soll Adobe Analytics dies als positiv oder negativ interpretieren? Ein Anstieg der E-Mail-Registrierungen ist wahrscheinlich positiv. Ein Anstieg bei den Übermittlungsfehlern für Formulare ist hingegen möglicherweise negativ.  In Analysis Workspace wird die Polarität angewendet auf: bedingte Formatierung der Freiformtabelle, Visualisierungen von Änderungen an der Zusammenfassung und das positive/negative Farbschema der Kartenvisualisierung. |
| Beschreibung | Eine kurze Beschreibung des Ereignisziels und dessen Nutzung. |
| Eindeutige Ereignisaufzeichnung | Siehe [Ereignis-Serialisierung](/help/implement/js-implementation/event-serialization.md). |
| Beitrag | See [Metrics Participation](/help/components/c-variables/c-metrics/metrics-participation.md). |
| Warnung (Währungsereignis) | Wenn Sie den Ereignistyp ändern, also von einem Währungsereignis zu einem anderen Ereignistyp wechseln oder umgekehrt, wird eine Meldung angezeigt, dass die historischen Daten nicht für die Berichterstellung verfügbar sind.  Die unterschiedlichen Ereignistypen verwenden separate Datentabellen, die nicht gleichzeitig genutzt werden können. Beim Wiederherstellen des bisherigen Ereignistyps kann ein Teil der historischen Daten unter Umständen wiederhergestellt werden. Alle Daten, die nach der ersten Änderung erfasst wurden, sind jedoch nicht mehr verfügbar. Gehen Sie beim Ändern des Ereignistyps mit Vorsicht vor. |

