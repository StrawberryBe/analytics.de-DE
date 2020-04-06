---
title: Ereignis-Serialisierung
description: Hilft Ihnen, Metriken auf Ihrer Website zu deduplizieren.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Ereignis-ID-Serialisierung

Bei der Ereignis-Serialisierung werden Maßnahmen implementiert, um zu verhindern, dass doppelte Ereignisse in das Analytics-Reporting aufgenommen werden. Das Deduplizieren von Ereignissen ist wichtig, wenn Sie nicht möchten, dass die Metriken durch Besucher, die die Seite aktualisieren, überhöht werden.

>[!NOTE] Data Sources unterstützt keine Ereignis-Serialisierung oder -Deduplizierung.

## Einrichten der Ereignis-Serialisierung

Sie müssen zuerst die Einstellung eines Ereignisses [!UICONTROL Unique Event Recording] in den Report Suite-Einstellungen [!UICONTROL Use Event ID] festlegen. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Erfolgsereignisse](/help/admin/admin/c-success-events/success-event.md).

Bei Verwendung von Ereignis-IDs erfolgt eine Deduplizierung auf folgenden Ebenen:

* Jede Variable verwendet ihre eigene Tabelle zur Deduplizierung. Zum Beispiel werden `event1:ABC` und `event2:ABC` beide in Berichten gezählt.
* Deduplizierung erfolgt global über alle Besucher hinweg. Wenn Besucher A `event1:ABC` sendet und dann Besucher B auch `event1:ABC` sendet, ignoriert Adobe die zweite Instanz von Besucher B.
* Die Deduplizierung läuft nicht ab. Wenn ein Besucher `event1:ABC` sendet und dann zwei Jahre später zurückkehrt und `event1:ABC` erneut sendet, ignoriert Adobe die zweite Instanz.

>[!TIP] Wenn Sie das [`purchase`](event-purchase.md)-Ereignis deduplizieren möchten, verwenden Sie stattdessen die [`purchaseID`](../purchaseid.md)-Variable.

## Verwenden der Ereignis-IDs in Adobe Experience Platform Launch

Sie können das Feld für die Ereignis-ID entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder als Aktion in einer Regel festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Go to the [!UICONTROL Rules] tab, then click the desired rule (or create a rule).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Suchen Sie den [!UICONTROL Events] Abschnitt, in dem jedes Ereignis ein [!UICONTROL Event ID] Feld enthält.

Gültige Werte sind alphanumerische Zeichen bis zu 20 Byte.

## Ereignis-IDs in AppMeasurement und im benutzerdefinierten Code-Editor in Launch verwenden

Die Ereignis-Serialisierung ist Teil der `s.events`-Variablen. Weisen Sie jedem Ereignis mithilfe eines Doppelpunkts in der Zeichenfolge eine ID zu.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

Wenn ein Ereignis die Serialisierung aktiviert hat, aber keine Serialisierungs-ID enthält, wird das Ereignis immer gezählt.
