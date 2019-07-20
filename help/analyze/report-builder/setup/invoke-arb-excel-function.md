---
description: Dank dieser Funktion wird die ReportBuilder-Verwendung in den normalen Excel-Workflow integriert, ohne dass Sie auf die ReportBuilder-Benutzeroberfläche zugreifen müssen.
seo-description: Dank dieser Funktion wird die ReportBuilder-Verwendung in den normalen Excel-Workflow integriert, ohne dass Sie auf die ReportBuilder-Benutzeroberfläche zugreifen müssen.
seo-title: Reportbuilder-Funktionen aus Microsoft Excel-Funktionen aufrufen
solution: Analytics
title: Reportbuilder-Funktionen aus Microsoft Excel-Funktionen aufrufen
topic: ReportBuilder
uuid: 5342 cc 4 f -085 d -4 a 2 d-a 498-38 b 00 a 3 ef 4 d 3
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Reportbuilder-Funktionen aus Microsoft Excel-Funktionen aufrufen

Dank dieser Funktion wird die ReportBuilder-Verwendung in den normalen Excel-Workflow integriert, ohne dass Sie auf die ReportBuilder-Benutzeroberfläche zugreifen müssen.

Sie können beispielsweise ReportBuilder-Anforderungen automatisch aktualisieren, deren Eingabefilter auf Daten basieren, die in Excel aus anderen Quellen abgerufen wurden. Genau dies können Sie mithilfe der Zeichenfolgenfunktion RefreshRequestsInCellsRange(..) durchführen. Alle Aufrufe sind asynchron. Sie werden sofort zurückgegeben und warten nicht, bis ein Aufruf vollständig ausgeführt wird.

>[!NOTE]
>
>Für diese Funktionalität muss Reportbuilder 5.0 (oder höher) installiert sein.

In der nachfolgenden Tabelle sind alle exponierten Funktionen aufgelistet.

| Name der Funktion | Beschreibung |
|---|---|
| string AsyncRefreshAll() | Aktualisiert alle in einer Arbeitsmappe vorhandenen ReportBuilder-Anforderungen. |
| string AsyncRefreshRange(string rangeAddressInA1Format) | Aktualisiert alle ReportBuilder-Anforderungen in der angegebenen Zellenbereichsadresse (ein Zeichenfolgenausdruck, der einen Zellenbereich im A1-Format darstellt, z. B. „Sheet1!A2:A10“). |
| string AsyncRefreshRangeAltTextParam() | Aktualisiert alle ReportBuilder-Anforderungen, die im angegebenen, über den Alternativtext des MS-Formularsteuerelements weitergeleiteten Zellenbereich vorhanden sind. |
| string AsyncRefreshActiveWorksheet() | Aktualisiert alle im aktiven Arbeitsblatt vorhandenen ReportBuilder-Anforderungen. |
| string AsyncRefreshWorksheet(string worksheetName) | Aktualisiert alle im angegebenen Arbeitsblatt vorhandenen ReportBuilder-Anforderungen (der Arbeitsblattname, wie er auf der Registerkarte angezeigt wird.) |
| string AsyncRefreshWorksheetAltTextParam(); | Aktualisiert alle ReportBuilder-Anforderungen, die im angegebenen, über den Alternativtext des MS-Formularsteuerelements weitergeleiteten Arbeitsblattnamen vorhanden sind. |
| string GetLastRunStatus() | Gibt eine Zeichenfolge zurück, die den Status der letzten Ausführung beschreibt. |

Um auf diese Funktionen innerhalb von ReportBuilder zuzugreifen, wechseln Sie zu [!UICONTROL Formeln] &gt; [!UICONTROL Funktion einfügen]. Am Ende der Kategorienliste finden Sie Adobe.ReportBuilder.Bridge:

![](assets/arb_functions.png)

## Use these functions in a formula {#section_034311081C8D4D7AA9275C1435A087CD}

Beispiel: Die Formel

```
=IF(OR(ISTEXT(P5),ISBLANK(P5)),AsyncRefreshRange("P9"),"")
```

bedeutet: „Wenn die Zelle P5 Text enthält oder leer ist, aktualisieren Sie den Bereich der Zelle P9.“

## Use Report Builder functions with format control {#section_26123090B5BD49748C8D8ED7A1C5ED84}

Ab sofort können Sie einem Steuerelement, das Sie erstellt haben, ein Makro zuweisen. Dieses Steuerelement kann eine Funktion sein, die eine Arbeitsmappenanforderung aktualisiert. Beispielsweise werden mit der Funktion AsyncRefreshActiveWorksheet alle Anforderungen in einem Arbeitsblatt aktualisiert. Manchmal möchten Sie jedoch vielleicht nur bestimmte Anforderungen und nicht alle aktualisieren.

1. Legen Sie den Makro-Parameter fest.
1. Klicken Sie mit der rechten Maustaste auf das Steuerelement und wählen Sie **[!UICONTROL Makro zuweisen aus]**.
1. Geben Sie den ReportBuilder-Funktionsnamen ein (ohne Parameter und Klammern).

![](assets/assign_macro.png)

## Pass parameters to Report Builder functions via format control {#section_ECCA1F4990D244619DFD79138064CEF0}

Die beiden Funktionen, die einen Parameter annehmen, können mit „Steuerelement formatieren“ verwendet werden, jedoch nur über das Feld für Alternativtext:

* AsyncRefreshRange(string rangeAddressInA1Format)
* AsyncRefreshWorksheet(string worksheetName)

1. Klicken Sie mit der rechten Maustaste auf das Steuerelement und wählen Sie **[!UICONTROL Steuerelement formatieren aus]**.

   ![](assets/format_control.png)

1. Klicken Sie auf die Registerkarte [!UICONTROL Alt-Text].

   ![](assets/alt_text.png)

1. Geben Sie unter [!UICONTROL Alternativtext] den Zellenbereich ein, der aktualisiert werden soll.
1. Öffnen Sie unter [!UICONTROL Formeln] &gt; [!UICONTROL Funktion einfügen] &gt; [!UICONTROL Adobe.ReportBuilder.Bridge] die Liste der ReportBuilder-Parameter.

1. Wählen Sie eine der beiden Funktionen aus, die auf AltTextParam enden, und klicken Sie auf **[!UICONTROL OK]**.

