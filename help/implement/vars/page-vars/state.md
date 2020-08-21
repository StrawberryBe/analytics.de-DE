---
title: state
description: Füllen Sie den Bericht „Bundesstaat des Besuchers“ in Reports and Analytics.
translation-type: ht
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: ht
source-wordcount: '215'
ht-degree: 100%

---


# state

>[!IMPORTANT]
>
>Diese Variable wurde eingestellt und ist keine verfügbare Dimension in Analysis Workspace. Verwenden Sie stattdessen die Dimension „US-Bundesstaaten“, die AppMeasurement automatisch basierend auf dem Standort des Besuchers erfasst.

In früheren Versionen von Adobe Analytics wurde die `state`-Variable verwendet, wenn Besucher Versandinformationen auf Retail-Websites ausfüllten. Sie ist funktionell mit einer Prop identisch, aber nicht in Analysis Workspace verfügbar.

## state in Adobe Experience Platform Launch

Sie können „state“ entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Bundesstaat].

Sie können „state“ auf einen beliebigen Zeichenfolgenwert oder ein beliebiges Datenelement einstellen.

## s.state in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.state`-Variable ist eine Zeichenfolge, die normalerweise das Bundesland oder den Bundesstaat des Besuchers enthält. Vollständige Namen oder Zweibuchstaben-Codes der Bundesstaaten sind gültig. Sie hat einen Maximalwert von 50 Byte. Längere Werte werden abgeschnitten. Der Standardwert ist eine leere Zeichenfolge.

```js
s.state = "Utah";
```
