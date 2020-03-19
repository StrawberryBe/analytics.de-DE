---
title: Ereignis-Serialisierung
description: hilft Ihnen, Metriken auf Ihrer Site zu deduplizieren.
translation-type: tm+mt
source-git-commit: 468f97ee61f5d573d07475836df8d2c313b29fb3

---


# Serialisierung von Ereignis-IDs

Bei der Ereignis-Serialisierung werden Maßnahmen implementiert, um zu verhindern, dass doppelte Ereignisse in die Analytics-Berichterstattung aufgenommen werden. Die Deduplizierung von Ereignissen ist wichtig, wenn Sie nicht möchten, dass Metriken durch Besucher, die die Seite aktualisieren, überhöht werden.

> [!NOTE] Data Sources unterstützt keine Ereignis-Serialisierung oder -Deduplizierung.

## Einrichten der Serialisierung von Ereignissen

Sie müssen zuerst die Einstellung eines Ereignisses [!UICONTROL Unique Event Recording] in den Report Suite-Einstellungen [!UICONTROL Use Event ID] festlegen. See [Success Events](/help/admin/admin/c-success-events/success-event.md) in the Admin user guide.

Bei Verwendung von Ereignis-IDs erfolgt eine Deduplizierung auf folgenden Ebenen:

* Jede Variable verwendet ihre eigene Tabelle zur Deduplizierung. So werden zum Beispiel `event1:ABC` und `event2:ABC` beide in Berichte gezählt.
* Deduplizierung findet global in allen Besuchern statt. Wenn Besucher A sendet, `event1:ABC` dann sendet Besucher B auch `event1:ABC`die zweite Instanz von Besucher B.
* Die Deduplizierung läuft nicht ab. Wenn ein Besucher sendet `event1:ABC` dann zwei Jahre später zurück kommt und `event1:ABC` erneut sendet, ignoriert Adobe die zweite Instanz.

> [!TIP] Wenn Sie das Duplikat des [`purchase`](event-purchase.md) Ereignisses löschen möchten, verwenden Sie stattdessen die [`purchaseID`](../purchaseid.md) Variable.

## Ereignis-IDs beim Start der Adobe Experience Platform verwenden

Sie können das Feld für die Ereignis-ID entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder als Regelaktion festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur [!UICONTROL Rules] Registerkarte und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie [!UICONTROL Actions]unter &quot;auf eine bestehende [!UICONTROL Adobe Analytics - Set Variables] Aktion&quot;oder auf das Symbol &quot;+&quot;.
5. Legen Sie das [!UICONTROL Extension] Dropdown-Menü auf Adobe Analytics und [!UICONTROL Action Type] auf [!UICONTROL Set Variables].
6. Suchen Sie den [!UICONTROL Events] Abschnitt, in dem jedes Ereignis ein [!UICONTROL Event ID] Feld enthält.

Gültige Werte sind alphanumerische Zeichen mit einer Länge von bis zu 20 Byte.

## Ereignis-IDs in AppMeasurement verwenden und benutzerdefinierten Code-Editor starten

Die Serialisierung von Ereignissen ist Teil der `s.events` Variablen. Weisen Sie jedem Ereignis mithilfe eines Doppelpunkts in der Zeichenfolge eine ID zu.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

Wenn für ein Ereignis die Serialisierung aktiviert ist, aber keine Serialisierungs-ID enthält, wird das Ereignis immer gezählt.
