---
title: transactionID
description: Verwenden Sie diese Variable, um Online- und Offlinedaten miteinander zu verknüpfen.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# transactionID

Die `transactionID` Variable identifiziert eine Transaktion eindeutig, sodass der Treffer mit Daten verknüpft werden kann, die über Data Sources hochgeladen wurden. Diese Variable ist nützlich, wenn Sie Daten aus anderen Kanälen verwenden und mit mit AppMeasurement erfassten Daten verknüpfen möchten.

> [!NOTE] Stellen Sie sicher, dass der [!UICONTROL Transaktions-ID-Speicher] in einer Report Suite aktiviert ist, bevor Sie diese Variable verwenden. See [General Account Settings](/help/admin/admin/general-acct-settings-admin.md) in the Admin user guide for more information.

Wenn Sie `transactionID` bei einem Treffer festlegen, erstellt Adobe einen &quot;Schnappschuss&quot;aller zu diesem Zeitpunkt festgelegten oder beständigen Analytics-Variablen. Daten, die über Data Sources mit einer übereinstimmenden Transaktions-ID hochgeladen wurden, sind dauerhaft mit diesen Variablenwerten verknüpft.

Adobe speichert standardmäßig alle Transaktions-ID-Werte (verknüpft und nicht verknüpft) bis zu 90 Tage lang. Wenn Ihr Offline-Interaktionsprozess länger als 90 Tage ist, wenden Sie sich an den Kundendienst, um diese Beschränkung zu verlängern.

## Transaktions-ID beim Starten der Adobe Experience Platform

Sie können die Transaktions-ID entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL Transaktions-ID] .

Sie können die Transaktions-ID auf einen beliebigen Zeichenfolgenwert, einschließlich Datenelementen, setzen.

## s.transactionID in AppMeasurement und Benutzerdefinierter Code-Editor starten

Die `s.transactionID` Variable ist eine Zeichenfolge, die einen eindeutigen Bezeichner für eine Transaktion enthält. Gültige Werte sind alphanumerische Zeichen mit einer Länge von bis zu 100 Byte. Der Standardwert ist eine leere Zeichenfolge.

```js
s.transactionID = "ABC123";
```

Wenn Sie mehr als eine Transaktions-ID für einen Treffer haben, können Sie jede durch ein Komma trennen. Für mehrere Transaktions-IDs gilt weiterhin der Grenzwert von 100 Byte.

```js
s.transactionID = "ABC123,XYZ456";
```

> [!NOTE] Wenn Sie mit dieser Variablen mehrere Offlinekanäle integrieren, stellen Sie sicher, dass sich die Transaktions-IDs nicht in verschiedenen Kanälen überschneiden. Wenn Sie z. B. einen Transaktions-ID-Wert für Call-Center `1234` und einen Wert für die Transaktions-ID für Verkaufsgespräche `1234`haben, kann dies zu Konflikten und unerwarteten Ergebnissen führen. Stellen Sie sicher, dass Transaktions-IDs eindeutige Formate pro Offlinekanal enthalten, und unterscheiden Sie diese bei Bedarf. Legen Sie z. B. Ihre Call-Center-Transaktions-ID und Ihre Verkaufs-Interessenten-Transaktions-ID `call_1234` `lead_1234` in Data Sources und AppMeasurement fest.
