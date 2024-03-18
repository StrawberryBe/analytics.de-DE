---
title: zip
description: Füllen Sie die Dimension „Postleitzahl“ manuell, wenn die Report Suite-Einstellungen dies zulassen.
feature: Variables
exl-id: 1acf4bf7-3788-46bd-bcdb-9885c7b93b59
role: Admin, Developer
source-git-commit: 5ef92db2f5edb5fded497dddedd56abd49d8a019
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 75%

---

# zip

Mit der `zip`-Variablen können Sie die Dimension „Postleitzahl“ manuell füllen, wenn die [!UICONTROL Zip-Option] in den Report Suite-Einstellungen dies zulässt. In früheren Versionen von Adobe Analytics konnte diese Variable nur manuell eingestellt werden, üblicherweise bei Eingabe von Versandinformationen auf einer Retail-Website. Dank der Verbesserungen an Adobe Analytics kann diese Variable mithilfe von Standortdaten automatisch eingestellt werden. Diese Variable bleibt nicht über den Treffer hinaus bestehen, in dem sie gesetzt wurde.

>[!IMPORTANT]
>
>Stellen Sie sicher, dass die [!UICONTROL Postleitzahlenoption] in den Report Suite-Einstellungen auf den gewünschten Wert eingestellt ist. Diese Variable kann nicht verwendet werden, wenn [!UICONTROL Geo-Zip] wird immer verwendet. Weitere Informationen finden Sie im Admin-Benutzerhandbuch unter [Allgemeine Kontoeinstellungen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md).

## Postleitzahl mit dem Web SDK

Postleitzahl wird den folgenden Variablen zugeordnet:

* [XDM-Objekt](/help/implement/aep-edge/xdm-var-mapping.md): `xdm.placeContext.geo.postalCode`
* [Datenobjekt](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.zip`

## Postleitzahl mit der Adobe Analytics-Erweiterung

Sie können die Postleitzahl entweder beim Konfigurieren der Analytics-Erweiterung (globale Variablen) oder unter Regeln festlegen.

1. Melden Sie sich bei der [Adobe Experience Platform-Datenerfassung](https://experience.adobe.com/data-collection) mit Ihren Adobe ID-Anmeldeinformationen an.
2. Klicken Sie auf die gewünschte Tag-Eigenschaft.
3. Gehen Sie zur Registerkarte „[!UICONTROL Regeln]“ und klicken Sie dann auf die gewünschte Regel (oder erstellen Sie eine Regel).
4. Klicken Sie unter [!UICONTROL Aktionen] auf eine bestehende Aktion [!UICONTROL Adobe Analytics – Variablen festlegen] oder klicken Sie auf das Pluszeichen.
5. Legen Sie die [!UICONTROL Erweiterung] einer Dropdown-Liste zu Adobe Analytics und dem [!UICONTROL Aktionstyp] nach [!UICONTROL Variablen festlegen].
6. Suchen Sie den Abschnitt [!UICONTROL Postleitzahl].

Sie können die Postleitzahl auf einen beliebigen Zeichenfolgenwert einstellen, einschließlich Datenelementen.

## s.zip in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.zip`-Variable ist eine Zeichenfolge, die normalerweise eine Postleitzahl enthält, jedoch einen beliebigen Wert mit einer Länge von bis zu 50 Byte enthalten kann.

```js
s.zip = "84043";
```
