---
title: zip
description: Füllen Sie die Dimension „Postleitzahl“ manuell, wenn die Report Suite-Einstellungen dies zulassen.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 100%

---


# zip

Mit der `zip`-Variablen können Sie die Dimension „Postleitzahl“ manuell füllen, wenn die [!UICONTROL Zip-Option] in den Report Suite-Einstellungen dies zulässt. In früheren Versionen von Adobe Analytics konnte diese Variable nur manuell eingestellt werden, üblicherweise bei Eingabe von Versandinformationen auf einer Retail-Website. Dank der Verbesserungen an Adobe Analytics kann diese Variable mithilfe von Standortdaten automatisch eingestellt werden. Diese Variable bleibt nicht über den Treffer hinaus bestehen, in dem sie gesetzt wurde.

>[!IMPORTANT]
>
>Stellen Sie sicher, dass die [!UICONTROL Postleitzahlenoption] in den Report Suite-Einstellungen auf den gewünschten Wert eingestellt ist. Sie können diese Variable nicht verwenden, wenn immer [!UICONTROL geo-zip] verwendet wird. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Allgemeine Kontoeinstellungen](/help/admin/admin/general-acct-settings-admin.md).

## zip In Adobe Experience Platform Launch

Sie können die Postleitzahl entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
2. Klicken Sie auf die gewünschte Eigenschaft.
3. Gehen Sie zur Registerkarte [!UICONTROL Regeln] und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Wählen Sie im Dropdown-Menü [!UICONTROL Erweiterung] die Option „Adobe Analytics“ aus und setzen Sie den [!UICONTROL Aktionstyp] auf [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Postleitzahl].

Sie können die Postleitzahl auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.zip in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s.zip`-Variable ist eine Zeichenfolge, die normalerweise eine Postleitzahl enthält, jedoch einen beliebigen Wert mit einer Länge von bis zu 50 Byte enthalten kann.

```js
s.zip = "84043";
```
