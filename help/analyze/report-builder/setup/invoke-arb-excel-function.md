---
description: Erfahren Sie, wie Sie Microsoft Excel mit Report Builder-Funktionen verwenden können, ohne auf die Report Builder-Benutzeroberfläche zuzugreifen.
title: Erfahren Sie, wie Sie Microsoft Excel mit Report Builder-Funktionen verwenden.
uuid: 5342cc4f-085d-4a2d-a498-38b00a3ef4d3
feature: Report Builder
role: User, Admin
exl-id: b412f2b5-affe-4297-af4b-85e8c6dfd257
source-git-commit: 66b7de0b008364e47253d319785c204ca479ab26
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 43%

---

# Verwenden von Report Builder-Funktionen mit Microsoft Excel

Sie können Report Builder-Funktionen verwenden, um auf Funktionen zuzugreifen, ohne auf die Benutzeroberfläche des Report Builders zuzugreifen.

Um beispielsweise Report Builder-Anforderungen automatisch mit Eingabefiltern zu aktualisieren, die auf Daten basieren, die aus anderen Quellen in Excel abgerufen werden, verwenden Sie die Zeichenfolge RefreshRequestsInCellsRange(..) durchführen. Alle Aufrufe sind asynchron und werden sofort zurückgegeben. Warten Sie nicht, bis die Ausführung vollständig abgeschlossen ist.

**Voraussetzungen**

* Report Builder 5.0 (oder höher) ist erforderlich.

In der folgenden Tabelle sind die angezeigten Funktionen aufgeführt.

| Name der Funktion | Typ | Beschreibung |
|:---| --- | ---|
| AsyncRefreshAll() | string | Aktualisiert alle in einer Arbeitsmappe vorhandenen Report Builder-Anforderungen. |
| AsyncRefreshRange(string rangeAddressInA1Format) | string | Aktualisiert alle Report Builder-Anforderungen in der angegebenen Zellenbereichsadresse (ein Zeichenfolgenausdruck, der einen Zellenbereich im A1-Format darstellt, z. B. „Sheet1!A2:A10“). |
| AsyncRefreshRangeAltTextParam() | string | Aktualisiert alle Report Builder-Anforderungen, die im angegebenen, über den Alternativtext des MS-Formularsteuerelements weitergeleiteten Zellenbereich vorhanden sind. |
| AsyncRefreshActiveWorksheet() | string | Aktualisiert alle im aktiven Arbeitsblatt vorhandenen Report Builder-Anforderungen. |
| AsyncRefreshWorksheet(string worksheetName) | string | Aktualisiert alle im angegebenen Arbeitsblatt vorhandenen Report Builder-Anforderungen (der Arbeitsblattname, wie er auf der Registerkarte angezeigt wird.) |
| AsyncRefreshWorksheetAltTextParam(); | string | Aktualisiert alle Report Builder-Anforderungen, die im angegebenen, über den Alternativtext des MS-Formularsteuerelements weitergeleiteten Arbeitsblattnamen vorhanden sind. |
| string GetLastRunStatus() | string | Gibt eine Zeichenfolge zurück, die den Status der letzten Ausführung beschreibt. |

Um auf die Report Builder-Funktionen zuzugreifen, navigieren Sie zu **[!UICONTROL Formeln]** > **[!UICONTROL Funktion einfügen]**. Verwenden Sie das Suchfeld, um nach einer Funktion zu suchen, oder wählen Sie eine Kategorie aus, um die Funktionen in dieser Kategorie aufzulisten.

![Screenshot mit dem Fenster Funktion einfügen mit erweiterter Kategorieliste.](assets/arb_functions.png)

## Beispiel {#section_034311081C8D4D7AA9275C1435A087CD}

Das folgende Beispiel zeigt *Wenn der Wert in Zelle P5 Text oder leer ist, aktualisieren Sie den Bereich in Zelle P9*.

```
=IF(OR(ISTEXT(P5),ISBLANK(P5)),AsyncRefreshRange("P9"),"")
```

## Verwenden von Report Builder-Funktionen mit „Steuerelement formatieren“  {#section_26123090B5BD49748C8D8ED7A1C5ED84}

Sie können einem von Ihnen erstellten Steuerelement ein Makro zuweisen. Dieses Steuerelement kann eine Funktion sein, die eine Arbeitsmappenanforderung aktualisiert. Beispielsweise werden mit der Funktion AsyncRefreshActiveWorksheet alle Anforderungen in einem Arbeitsblatt aktualisiert. Manchmal möchten Sie jedoch möglicherweise nur bestimmte Anforderungen aktualisieren.

1. Legen Sie den Makro-Parameter fest.
1. Klicken Sie mit der rechten Maustaste auf das Steuerelement und wählen Sie **[!UICONTROL Makro zuweisen]** aus.
1. Geben Sie den Funktionsnamen des Report Builders ein (keine Parameter oder Klammern).

![Screenshot mit dem Fenster &quot;Makro zuweisen&quot;.](assets/assign_macro.png)

## Übergeben von Parametern an Report Builder-Funktionen mithilfe der Formatsteuerung {#section_ECCA1F4990D244619DFD79138064CEF0}

Zwei Funktionen, die einen Parameter annehmen, können mit &quot;Steuerelement formatieren&quot;verwendet werden. Sie müssen die **Alternativtext:** -Feld:

* AsyncRefreshRange(string rangeAddressInA1Format)
* AsyncRefreshWorksheet(string worksheetName)

So übergeben Sie Parameter mithilfe der Formatsteuerung an Report Builder-Funktionen

1. Klicken Sie mit der rechten Maustaste auf das Steuerelement und wählen Sie **[!UICONTROL Steuerelement formatieren]** aus.

   ![Screenshot mit ausgewählter Formatsteuerung.](assets/format_control.png)

1. Klicken Sie auf die Registerkarte **[!UICONTROL Alt-Text]**.

   ![Screenshot mit der Registerkarte ALT-Text und dem Feld Alternativer Text:](assets/alt_text.png)

1. Geben Sie unter **[!UICONTROL Alternativtext]** den Zellenbereich ein, der aktualisiert werden soll.
1. Öffnen Sie die Liste der Report Builder-Parameter unter **[!UICONTROL Formeln]** > **[!UICONTROL Funktion einfügen]**> **[!UICONTROL Adobe.ReportBuilder.Bridge]**.

1. Wählen Sie eine der beiden Funktionen aus, die auf AltTextParam enden, und klicken Sie auf **[!UICONTROL OK]**.
