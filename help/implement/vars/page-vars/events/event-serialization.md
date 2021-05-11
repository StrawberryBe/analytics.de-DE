---
title: Ereignis-Serialisierung
description: Hilft Ihnen, Metriken auf Ihrer Website zu deduplizieren.
exl-id: 54de0fd7-9056-44af-bd59-b8eb55fc816e
translation-type: tm+mt
source-git-commit: 71581f49eb7ef13577a05c05daee737eeb9e6218
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 94%

---

# Ereignis-ID-Serialisierung

Bei der Ereignis-Serialisierung werden Maßnahmen implementiert, um zu verhindern, dass doppelte Ereignisse in das Analytics-Reporting aufgenommen werden. Das Deduplizieren von Ereignissen ist wichtig, wenn Sie nicht möchten, dass die Metriken durch Besucher, die die Seite aktualisieren, überhöht werden.

>[!NOTE]
>
>Data Sources unterstützt keine Ereignisserialisierung oder -Deduplizierung.

## Einrichten der Ereignis-Serialisierung

Sie müssen [!UICONTROL Eindeutige Ereignisaufzeichnung] eines Ereignisses zuerst in den Report Suite-Einstellungen auf [!UICONTROL Ereignis-ID verwenden] setzen. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Erfolgsereignisse](/help/admin/admin/c-success-events/success-event.md).

Bei Verwendung von Ereignis-IDs erfolgt eine Deduplizierung auf folgenden Ebenen:

* Jede Variable verwendet ihre eigene Tabelle zur Deduplizierung. Zum Beispiel werden `event1:ABC` und `event2:ABC` beide in Berichten gezählt.
* Deduplizierung erfolgt global über alle Besucher hinweg. Wenn Besucher A `event1:ABC` sendet und dann Besucher B auch `event1:ABC` sendet, ignoriert Adobe die zweite Instanz von Besucher B.
* Die Deduplizierung läuft nicht ab. Wenn ein Besucher `event1:ABC` sendet und dann zwei Jahre später zurückkehrt und `event1:ABC` erneut sendet, ignoriert Adobe die zweite Instanz.

>[!TIP]
>
>Wenn Sie das [`purchase`](event-purchase.md)-Ereignis deduplizieren möchten, verwenden Sie stattdessen die [`purchaseID`](../purchaseid.md)-Variable.

## Verwenden der Ereignis-IDs in Adobe Experience Platform Launch

Sie können das Feld für die Ereignis-ID entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder als Aktion in einer Regel festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Ereignisse], in dem jedes Ereignis ein Feld [!UICONTROL Ereignis-ID] enthält.

Gültige Werte sind alphanumerische Zeichen bis zu 20 Byte. Wenn Sie einen Wert eingeben, der länger als 20 Byte ist, wird er vom System auf die ersten 20 Byte abgeschnitten.

## Ereignis-IDs in AppMeasurement und im benutzerdefinierten Code-Editor in Launch verwenden

Die Ereignis-Serialisierung ist Teil der `s.events`-Variablen. Weisen Sie jedem Ereignis mithilfe eines Doppelpunkts in der Zeichenfolge eine ID zu.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

Wenn ein Ereignis die Serialisierung aktiviert hat, aber keine Serialisierungs-ID enthält, wird das Ereignis immer gezählt.
