---
title: Ereignis-Serialisierung
description: hilft Ihnen, Metriken auf Ihrer Site zu deduplizieren.
translation-type: tm+mt
source-git-commit: c5a60bc9756af2742740dbc6a26a081f55ee3235

---


# Ereignis-ID-Serialisierung

Bei der Ereignis-Serialisierung werden Maßnahmen implementiert, um zu verhindern, dass doppelte Ereignisse in die Analytics-Berichterstattung aufgenommen werden. Das Deduplizieren von Ereignissen ist wichtig, wenn Sie nicht möchten, dass die Metriken durch Besucher, die die Seite aktualisieren, überhöht werden.

> [!NOTE] Data Sources unterstützt keine Ereignis-Serialisierung oder -Deduplizierung.

## Ereignisreihenbildung einrichten

Sie müssen zuerst die [!UICONTROL einzigartige Ereignisaufzeichnung] eines Ereignisses so einstellen, dass die Ereignis-ID[!UICONTROL  in den Report Suite-Einstellungen ]verwendet wird. See [Success Events](../../../../admin/admin/c-success-events/success-event.md) in the Admin user guide.

Bei Verwendung von Ereignis-IDs erfolgt eine Deduplizierung auf folgenden Ebenen:

* Jede Variable verwendet ihre eigene Tabelle zur Deduplizierung. Zum Beispiel `event1:ABC` und `event2:ABC` werden beide in Berichten gezählt.
* Deduplizierung erfolgt global über alle Besucher hinweg. Wenn Besucher A sendet `event1:ABC` und Besucher B auch sendet, ignoriert Adobe `event1:ABC`die zweite Instanz von Besucher B.
* Die Deduplizierung läuft nicht ab. Wenn ein Besucher `event1:ABC` dann zwei Jahre später zurückkehrt und `event1:ABC` erneut sendet, ignoriert Adobe die zweite Instanz.

> [!TIP] Wenn Sie das `purchase` Ereignis deduplizieren möchten, verwenden Sie stattdessen die `purchaseID` Variable.

## Ereignis-IDs beim Start der Adobe Experience Platform verwenden

Sie können das Feld für die Ereignis-ID entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder als Aktion in einer Regel festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL Ereignisse] , in dem jedes Ereignis ein Feld mit einer [!UICONTROL Ereignis-ID] enthält.

Gültige Werte sind alphanumerische Zeichen mit einer Länge von bis zu 20 Byte.

## Ereignis-IDs in AppMeasurement verwenden und benutzerdefinierten Code-Editor starten

Die Ereignisreihenbildung ist Teil der `s.events` Variablen. Weisen Sie jedem Ereignis mithilfe eines Doppelpunkts in der Zeichenfolge eine ID zu.

```js
// Assign custom ID serialization to a single value
s.events = "event1:ABC123";

// Assign custom ID serialization to multiple values
s.events = "event1:ABC123,event2:ABC123";
```

Wenn für ein Ereignis die Serialisierung aktiviert ist, aber keine Serialisierungs-ID enthält, wird das Ereignis immer gezählt.
