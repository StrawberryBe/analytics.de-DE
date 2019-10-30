---
description: Die Marketingkanal-Verarbeitungsregeln bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt. Die Regeln verarbeiten jeden Treffer des Besuchers auf Ihrer Site. Wenn eine Regel die Kriterien des Kanals nicht erfüllt oder die Regeln nicht richtig konfiguriert sind, ordnet das System den Treffer unter „Kein Kanal identifiziert“ ein.
seo-description: Die Marketingkanal-Verarbeitungsregeln bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt. Die Regeln verarbeiten jeden Treffer des Besuchers auf Ihrer Site. Wenn eine Regel die Kriterien des Kanals nicht erfüllt oder die Regeln nicht richtig konfiguriert sind, ordnet das System den Treffer unter „Kein Kanal identifiziert“ ein.
seo-title: Verarbeitungsregeln für Marketing-Kanäle
solution: Analytics
subtopic: Marketingkanäle
title: Verarbeitungsregeln für Marketing-Kanäle
topic: Reports and Analytics
uuid: f6394f4b-a244-48e9-9892-7dfbfceb5fc9
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Verarbeitungsregeln für Marketing-Kanäle

Die Marketingkanal-Verarbeitungsregeln bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt. Die Regeln verarbeiten jeden Treffer des Besuchers auf Ihrer Site. Wenn eine Regel die Kriterien des Kanals nicht erfüllt oder die Regeln nicht richtig konfiguriert sind, ordnet das System den Treffer unter „Kein Kanal identifiziert“ ein.

Beachten Sie bei der Regelerstellung diese wichtigen Richtlinien:

* Sortieren Sie die Regeln in der Reihenfolge, in der sie verarbeitet werden sollen.
* Setzen Sie an das Ende Ihrer Liste eine Sammelregel wie „Sonstige“. Diese Regel identifiziert externen Traffic, jedoch nicht den internen Traffic.

   Siehe [Kein Kanal identifiziert](../../components/c-marketing-channels/c-faq.md#section_451E42994DA247A8A7B8559C715A5EE7).

> [!NOTE] Diese Regeln wirken sich zwar nicht auf Berichte außerhalb von Marketingkanälen aus, wirken sich jedoch auf die Datenerfassung über Marketingkanäle aus. Mit diesen Regeln erfasste Daten sind zu 100 % dauerhaft und nach der Datenerfassung geänderte Regeln sind nicht rückwirkend. Es wird dringend empfohlen, alle Umstände zu prüfen und in Erwägung zu ziehen, bevor [!UICONTROL Marketingkanal-Verarbeitungsregeln] gespeichert werden, um zu verhindern, dass Daten in falschen Kanälen erfasst werden.

**Voraussetzungen**

* Überprüfen Sie erneut die konzeptbezogenen Informationen unter Erste [Schritte mit Marketingkanälen](../../components/c-marketing-channels/c-getting-started-mchannel.md#concept_0C28C1592F564E53BB467E6EBC168E8C) und [Marketingkanalberichten](../../components/c-marketing-channels/c-overview.md#concept_77BE50D20BAA402CB292026436A39068).

* Erstellen Sie einen oder mehr Kanäle, um Regeln zuweisen zu können.

   Siehe [Hinzufügen von Marketingkanälen](../../components/c-marketing-channels/c-channels.md#task_98C9D3F5DBBC4B198E0A9ED4D3891E03).

