---
description: Dank dieser Funktion wird die Report Builder-Verwendung in den normalen Excel-Workflow integriert, ohne dass Sie auf die Report Builder-Benutzeroberfläche zugreifen müssen.
title: Report Builder-Funktionen über Microsoft Excel-Funktionen aufrufen
topic: Report builder
uuid: 5342cc4f-085d-4a2d-a498-38b00a3ef4d3
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Report Builder-Funktionen über Microsoft Excel-Funktionen aufrufen

Dank dieser Funktion wird die Report Builder-Verwendung in den normalen Excel-Workflow integriert, ohne dass Sie auf die Report Builder-Benutzeroberfläche zugreifen müssen.

Sie können beispielsweise Report Builder-Anforderungen automatisch aktualisieren, deren Eingabefilter auf Daten basieren, die in Excel aus anderen Quellen abgerufen wurden. Sie können dies jetzt mit der Zeichenfolge RefreshRequestsInCellsRange(..) tun. durchführen. Alle Aufrufe sind asynchron. Sie kehren sofort zurück und warten nicht, bis ein Aufruf vollständig ausgeführt wird.

>[!NOTE] Damit dies funktioniert, muss Report Builder 5.0 (oder höher) installiert sein.

Die folgende Tabelle zeigt die Liste der freigegebenen Funktionen:

| Funktionsname | Beschreibung |
|---|---|
| string AsyncRefreshAll() | Aktualisiert alle in einer Arbeitsmappe vorhandenen Report Builder-Anforderungen. |
| string AsyncRefreshRange(string rangeAddressInA1Format) | Aktualisiert alle Report Builder-Anforderungen in der angegebenen Zellenbereichsadresse (ein Zeichenfolgenausdruck, der einen Zellenbereich im A1-Format darstellt, z. B. „Sheet1!A2:A10“). |
| string AsyncRefreshRangeAltTextParam() | Aktualisiert alle Report Builder-Anforderungen, die im angegebenen, über den Alternativtext des MS-Formularsteuerelements weitergeleiteten Zellenbereich vorhanden sind. |
| string AsyncRefreshActiveWorksheet() | Aktualisiert alle im aktiven Arbeitsblatt vorhandenen Report Builder-Anforderungen. |
| string AsyncRefreshWorksheet(string worksheetName) | Aktualisiert alle im angegebenen Arbeitsblatt vorhandenen Report Builder-Anforderungen (der Arbeitsblattname, wie er auf der Registerkarte angezeigt wird.) |
| string AsyncRefreshWorksheetAltTextParam(); | Aktualisiert alle Report Builder-Anforderungen, die im angegebenen, über den Alternativtext des MS-Formularsteuerelements weitergeleiteten Arbeitsblattnamen vorhanden sind. |
| string GetLastRunStatus() | Gibt eine Zeichenfolge zurück, die den Status der letzten Ausführung beschreibt. |

Um auf diese Funktionen in ReportBuilder zuzugreifen, gehen Sie zu [!UICONTROL Formulas] > [!UICONTROL Insert Function]. Am Ende der Liste der Kategorien finden Sie Adobe.ReportBuilder.Bridge:

![](assets/arb_functions.png)

## Verwenden dieser Funktionen in einer Formel {#section_034311081C8D4D7AA9275C1435A087CD}

Beispiel: Die Formel

```
=IF(OR(ISTEXT(P5),ISBLANK(P5)),AsyncRefreshRange("P9"),"")
```

&quot;Wenn der Wert in Zelle P5 Text oder leer ist, aktualisieren Sie den Bereich in Zelle P9.&quot;

## Verwenden von Report Builder-Funktionen mit „Steuerelement formatieren“ {#section_26123090B5BD49748C8D8ED7A1C5ED84}

Sie können einem erstellten Steuerelement nun ein Makro zuweisen. Bei diesem Steuerelement kann es sich um eine Funktion handeln, die eine Arbeitsmappenanforderung aktualisiert. Beispielsweise aktualisiert die Funktion AsyncRefreshActiveWorksheet alle Anforderungen in einem Arbeitsblatt. Manchmal möchten Sie jedoch möglicherweise nur bestimmte Anforderungen aktualisieren, nicht alle.

1. Legen Sie den Makroparameter fest.
1. Klicken Sie mit der rechten Maustaste auf das Steuerelement und wählen Sie **[!UICONTROL Assign Macro]**.
1. Geben Sie den Funktionsnamen ReportBuilder ein (keine Parameter oder Klammern).

![](assets/assign_macro.png)

## Weiterleiten von Parametern zu Report Builder-Funktionen über „Steuerelement formatieren“ {#section_ECCA1F4990D244619DFD79138064CEF0}

Die beiden Funktionen, die einen Parameter annehmen, können mit &quot;Steuerelement formatieren&quot;verwendet werden, jedoch nur über das Feld &quot;ALT-Text&quot;:

* AsyncRefreshRange(string rangeAddressInA1Format)
* AsyncRefreshWorksheet(string worksheetName)

1. Klicken Sie mit der rechten Maustaste auf das Steuerelement und wählen Sie **[!UICONTROL Format Control]**.

   ![](assets/format_control.png)

1. Click the [!UICONTROL Alt Text] tab.

   ![](assets/alt_text.png)

1. Geben Sie [!UICONTROL Alternative text]unter den Zellbereich ein, der aktualisiert werden soll.
1. Öffnen Sie die Liste der ReportBuilder-Parameter unter [!UICONTROL Formulas] > [!UICONTROL Insert Function]> [!UICONTROL Adobe.ReportBuilder.Bridge].

1. Wählen Sie eine der beiden Funktionen aus, die auf AltTextParam enden, und klicken Sie auf **[!UICONTROL OK]**.

