---
title: Verarbeitungsregeln für Marketing-Kanäle
description: Die Marketingkanal-Verarbeitungsregeln bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt. Die Regeln verarbeiten jeden Treffer des Besuchers auf Ihrer Site. Wenn eine Regel die Kriterien des Kanals nicht erfüllt oder die Regeln nicht richtig konfiguriert sind, ordnet das System den Treffer unter „Kein Kanal identifiziert“ ein.
translation-type: tm+mt
source-git-commit: ea4d9e6c9396032fe323de594cb43eecbf97aa15

---


# Verarbeitungsregeln für Marketing-Kanäle

Die Marketingkanal-Verarbeitungsregeln bestimmen, ob der Besucherzugriff die dem Kanal zugewiesenen Kriterien erfüllt. Die Regeln verarbeiten jeden Treffer des Besuchers auf Ihrer Site. Wenn eine Regel die Kriterien des Kanals nicht erfüllt oder die Regeln nicht richtig konfiguriert sind, ordnet das System den Treffer unter „Kein Kanal identifiziert“ ein.

Beachten Sie bei der Regelerstellung diese wichtigen Richtlinien:

* Sortieren Sie die Regeln in der Reihenfolge, in der sie verarbeitet werden sollen.
* Setzen Sie an das Ende Ihrer Liste eine Sammelregel wie „Sonstige“. Diese Regel identifiziert externen Traffic, jedoch nicht den internen Traffic.

   Siehe [Kein Kanal identifiziert.](/help/components/c-marketing-channels/mc-faq/c-faq.md#no-channel-identified)

> [!NOTE] Auch wenn diese Regeln keine Auswirkungen auf die Berichterstellung außerhalb der Marketing-Kanäle haben, beeinflussen sie die Marketing-Kanal-Datenerfassung. Mit diesen Regeln erfasste Daten sind zu 100 % dauerhaft und nach der Datenerfassung geänderte Regeln sind nicht rückwirkend. It is strongly recommended to review and consider all circumstances before saving [!UICONTROL Marketing Channel Processing Rules] to mitigate data being collected in incorrect channels.

## Voraussetzungen

* Überprüfen Sie die Konzeptinformationen unter [Erste Schritte mit Marketingkanälen](/help/components/c-marketing-channels/getting-started/c-getting-started-mchannel.md).
* Erstellen Sie einen oder mehr Kanäle, um Regeln zuweisen zu können. See [Add marketing channels.](/help/components/c-marketing-channels/mark-channel-mgr/c-channels.md)
