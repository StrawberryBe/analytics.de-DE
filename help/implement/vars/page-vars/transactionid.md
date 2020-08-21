---
title: transactionID
description: Verwenden Sie diese Variable, um Online- und Offline-Daten miteinander zu verknüpfen.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '394'
ht-degree: 100%

---


# transactionID

Die `transactionID`-Variable identifiziert eine Transaktion eindeutig, sodass der Treffer mit Daten verknüpft werden kann, die über Data Sources hochgeladen wurden. Diese Variable ist nützlich, wenn Sie Daten aus anderen Kanälen verwenden und mit Daten verknüpfen möchten, die mit AppMeasurement erfasst werden.

>[!NOTE]
>
>Stellen Sie sicher, dass der [!UICONTROL Transaktions-ID-Speicher] in einer Report Suite aktiviert ist, bevor Sie diese Variable verwenden. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Allgemeine Kontoeinstellungen](/help/admin/admin/general-acct-settings-admin.md).

Wenn Sie `transactionID` für einen Treffer festlegen, erstellt Adobe einen „Schnappschuss“ aller zu diesem Zeitpunkt festgelegten oder beibehaltenen Analytics-Variablen. Daten, die über Data Sources mit einer übereinstimmenden Transaktions-ID hochgeladen wurden, sind dauerhaft mit diesen Variablenwerten verknüpft.

Adobe speichert standardmäßig alle (verknüpfte und nicht verknüpfte) Transaktions-ID-Werte bis zu 90 Tage lang. Wenn die Offline-Interaktion länger als 90 Tage dauert, lassen Sie diese Zeitspanne vom Kundendienst verlängern.

## Transaktions-ID in Adobe Experience Platform Launch

Sie können die Transaktions-ID entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Transaktions-ID].

Sie können die Transaktions-ID auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.transactionID in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.transactionID`-Variable ist eine Zeichenfolge, die eine eindeutige Kennung für eine Transaktion enthält. Gültige Werte sind alphanumerische Zeichen bis zu 100 Byte. Der Standardwert ist eine leere Zeichenfolge.

```js
s.transactionID = "ABC123";
```

Wenn Sie mehr als eine Transaktions-ID für einen Treffer haben, können Sie diese mit einem Komma trennen. Für mehrere Transaktions-IDs gilt weiterhin die 100-Byte-Grenze.

```js
s.transactionID = "ABC123,XYZ456";
```

>[!NOTE]
>
>Wenn Sie mit dieser Variablen mehrere Offline-Kanäle integrieren, stellen Sie sicher, dass sich die Transaktions-IDs nicht in verschiedenen Kanälen überschneiden. Wenn Sie beispielsweise eine Call-Center-Transaktions-ID mit dem Wert `1234` und eine Verkaufs-Lead-Transaktions-ID mit dem Wert `1234` haben, können sie miteinander in Konflikt geraten und unerwartete Ergebnisse verursachen. Stellen Sie sicher, dass Transaktions-IDs eindeutige Formate pro Offline-Kanal enthalten, und unterscheiden Sie diese bei Bedarf. Setzen Sie z. B. Ihre Call-Center-Transaktions-ID `call_1234` und Ihre Verkaufs-Lead-Transaktions-ID `lead_1234` sowohl in Data Sources als auch in AppMeasurement.
