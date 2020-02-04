---
title: zip
description: Füllen Sie manuell die Dimension "Postleitzahl", wenn die Report Suite-Einstellungen dies zulassen.
translation-type: tm+mt
source-git-commit: f75c6759feb6576017733f1aac5bff2e21d4b0af

---


# zip

Mit der `zip` Variablen können Sie die Dimension &quot;Postleitzahl&quot;manuell füllen, wenn die Option &quot; [!UICONTROL PLZ&quot;in den Report Suite-Einstellungen dies zulässt] . In früheren Versionen von Adobe Analytics konnte diese Variable nur manuell eingestellt werden, üblicherweise bei Eingabe von Versandinformationen auf einer für den Handel bestimmten Site. Dank der Verbesserungen an Adobe Analytics kann diese Variable automatisch mithilfe von geografischen Standortdaten eingestellt werden. Diese Variable bleibt nicht über den festgelegten Treffer hinaus bestehen.

> [!IMPORTANT] Stellen Sie sicher, dass die [!UICONTROL ZIP-Option] in den Report Suite-Einstellungen auf den gewünschten Wert eingestellt ist. Sie können diese Variable nicht verwenden, wenn immer [!UICONTROL Geo-ZIP] verwendet wird. See [General Account Settings](/help/admin/admin/general-acct-settings-admin.md) in the Admin user guide for more information.

## In Adobe Experience Platform Launch zitieren

Sie können Postleitzahlen entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Log in to [launch.adobe.com](https://launch.adobe.com) using your AdobeID credentials.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen]auf eine bestehende Aktion [!UICONTROL Adobe Analytics - Set Variables] , oder klicken Sie auf das Pluszeichen.
5. Legen Sie das [!UICONTROL Erweiterungs] -Dropdownmenü auf Adobe Analytics und den [!UICONTROL Aktionstyp] auf Variablen [!UICONTROL festlegen]fest.
6. Suchen Sie den Abschnitt [!UICONTROL ZIP] .

Sie können Postleitzahl auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.zip in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s.zip` Variable ist eine Zeichenfolge, die normalerweise einen Postleitzahl enthält, jedoch einen beliebigen Wert von bis zu 50 Byte Länge enthalten kann.

```js
s.zip = "84043";
```
