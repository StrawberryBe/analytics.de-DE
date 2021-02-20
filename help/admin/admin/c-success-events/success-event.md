---
description: 'Erfolgsereignisse sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Beispiel: Wenn ein Besucher einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden..'
keywords: event
title: Übersicht über Erfolgsereignisse
topic: Admin tools
uuid: 410eee44-8960-462c-a9c3-07b44d0b1df0
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 100%

---


# Übersicht über Erfolgsereignisse

Erfolgsereignisse sind Aktionen, die verfolgt werden können. Sie legen fest, was ein Erfolgsereignis ist. Beispiel: Wenn ein Besucher einen Artikel kauft, kann das Kaufereignis als Erfolgsereignis betrachtet werden..

Rufen Sie die Seite „Erfolgsereignisse“ in den Report Suite-Einstellungen auf:

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Klicken Sie oben auf die 9-Raster-Schaltfläche und dann auf [!UICONTROL Analytics].
3. Navigieren Sie zu [!UICONTROL Admin] > [!UICONTROL Report Suites]
4. Wählen Sie die gewünschte Report Suite aus und navigieren Sie dann zu [!UICONTROL Einstellungen bearbeiten] > [!UICONTROL Konversion] > [!UICONTROL Erfolgsergebnisse].
5. Suchen Sie nach dem gewünschten Ereignis und ändern Sie das Dropdown-Menü [!UICONTROL Eindeutige Ereignisaufzeichnung] in [!UICONTROL Einmal pro Besuch aufzeichnen] oder [!UICONTROL Ereignis-ID verwenden].

Es gibt, je nach Ihrem Websitetyp, viele Arten von Erfolgsereignissen. Zu diesen Arten zählen beispielsweise:

* **Einzelhandel**: Produktaufruf, Checkout, Kauf
* **Medien**: Abonnement, Wettbewerbsanmeldung, Seitenaufruf, Videoaufruf
* **Finanzen**: Applikationseinreichung, Anmeldung, Nutzung von Self-Service-Tools
* **Reisen**: Reservierung (Kauf), interne Kampagne (Clickthrough), Suche (Preisberechnung)
* **Telekommunikation**: Kauf, Leads, Nutzung von Self-Service-Tools
* **High Tech**: Download von White Papers, Gebotsanfragen, Formularausfüllung, Supportanfragen
* **Automotive**: Leadeinsendung, Preisanfrage, Download von Broschüren

Die Variable [s.events](https://docs.adobe.com/content/help/de-DE/analytics/implementation/vars/page-vars/events/event-serialization.html) definiert ein Erfolgsereignis.

## Seite „Erfolgsereignisse“ – Beschreibungen   {#section_681ECEC981694CABBDBF00E18165B447}

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Erfolgsereignisse]**

Auf der Seite „Erfolgsereignisse“ können Sie die auf der Site verwendeten Ereignisvariablen konfigurieren. Sie können bis zu 1.000 Erfolgsereignisse hinzufügen. Die Ereignisse 81–1.000 sind nur bei H22-Code oder höher verfügbar.

| Element | Beschreibung |
|--- |--- |
| Ereignis- | Der ursprüngliche Name des Ereignisses. |
| Name | Verwenden Sie aussagekräftige Namen für die auf Ihrer Website genutzten Erfolgsereignisse. Wenn beispielsweise Ereignis1 zur Nachverfolgung von Registrierungen verwendet wird, können Sie hier den Namen ändern, damit es in sämtlichen Konversionsberichten als „Registrierungen“ angezeigt wird. |
| Typ | Je nach ausgewähltem Typ handelt es sich um ein Zählerereignis (Standard), ein numerisches Ereignis oder ein Währungsereignis. Bei numerischen Ereignissen und Währungsereignissen können die Metriken um einen anderen Wert als 1 erhöht werden.  Zählerereignisse halten Ereignisse in der Zeit fest, Währungsereignisse dagegen eine Dezimalzahl (z. B. Steuern oder Versandkosten). Der in die Währungsereignisse einfließende Wert wird bei Eingang von der Seitenwährung in die Basiswährung der Report Suite konvertiert. Weitere Informationen zur Verwendung von Währungsereignissen erhalten Sie bei Ihrem Adobe-Support-Mitarbeiter. Numerische Ereignisse werden für Berichte zu anderen Zahlen als Währungsangaben verwendet, z. B. für die Zahl der bei einer Bestellung verwendeten Gutscheine. Währungsereignisse werden zur Nachverfolgung von Steuern und Versandkosten verwendet. Ereignisse im Standardtyp von „Data Sources“ müssen numerische oder Währungsereignisse sein. |
| Polarität | Anhand der Metrikpolarität können Sie festlegen, ob Adobe Analytics es als positiv oder negativ interpretieren soll, wenn ein benutzerdefiniertes Ereignis (Metrik) ansteigt. So kann Adobe Analytics Trendanzeigen (Pfeile) für verschiedene Metriken einbinden und mehr Kontext bieten (z. B. Vergleich über mehrere Wochen).  Beispiele: Wenn die Metrik „Übermittelte Bugs“ über mehrere Wochen ansteigt, soll Adobe Analytics dies als positiv oder negativ interpretieren? Ein Anstieg der E-Mail-Registrierungen ist wahrscheinlich positiv. Ein Anstieg bei den Übermittlungsfehlern für Formulare ist hingegen möglicherweise negativ.  In Analysis Workspace wird die Polarität angewendet auf: bedingte Formatierung der Freiformtabelle, Visualisierungen von Änderungen an der Zusammenfassung und das positive/negative Farbschema der Kartenvisualisierung. |
| Beschreibung | Eine kurze Beschreibung des Ereignisziels und dessen Nutzung. |
| Eindeutige Ereignisaufzeichnung | **Einmal pro Besuch aufzeichnen**: Verbindet das angegebene Ereignis mit der Sitzung des Besuchers. Nachfolgende Zählungen für ein bestimmtes Ereignis im selben Besuch werden ignoriert. Für diese Art der Ereignis-Serialisierung sind keine Implementierungsänderungen erforderlich.<br>**Ereignis-ID verwenden:** Verbindet das angegebene Ereignis mit einer benutzerdefinierten ID. Nachfolgende Zählungen für ein bestimmtes Ereignis mit derselben Ereignis-ID werden ignoriert. Für diese Art der Ereignis-Serialisierung ist eine benutzerdefinierte ID in Treffern erforderlich, um Werte zu deduplizieren. Siehe [Ereignis-ID-Serialisierung](../../../implement/vars/page-vars/events/event-serialization.md) im Benutzerhandbuch zu Implementierungen. |
| Beitrag | Ermöglicht die vollständige Attribution zu allen Dimensionselementen im Besuch. |
| Warnung (Währungsereignis) | Wenn Sie den Ereignistyp ändern, also von einem Währungsereignis zu einem anderen Ereignistyp wechseln oder umgekehrt, wird eine Meldung angezeigt, dass die historischen Daten nicht für die Berichterstellung verfügbar sind.  Die unterschiedlichen Ereignistypen verwenden separate Datentabellen, die nicht gleichzeitig genutzt werden können. Beim Wiederherstellen des bisherigen Ereignistyps kann ein Teil der historischen Daten unter Umständen wiederhergestellt werden. Alle Daten, die nach der ersten Änderung erfasst wurden, sind jedoch nicht mehr verfügbar. Gehen Sie beim Ändern des Ereignistyps mit Vorsicht vor. |

