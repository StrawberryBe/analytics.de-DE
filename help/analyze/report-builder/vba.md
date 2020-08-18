---
title: Visual Basic-Makros in Report Builder
description: Erweitern Sie die Funktionalität von Excel-Arbeitsmappen und Report Builder mit VBA.
translation-type: tm+mt
source-git-commit: b569f87dde3b9a8b323e0664d6c4d1578d410bb7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Visual Basic-Makros in Report Builder

Mit VBA-Makros, auch Visual Basic-Makros genannt, können Sie Arbeitsmappen so bearbeiten, wie es Microsoft Excel allein nicht kann. Visual Basic hat Zugriff auf die Arbeitsmappe, Excel und sogar Windows.

Adobe unterstützt drei Report Builder-API-Methoden. Stellen Sie sicher, dass die neueste Version von ReportBuilder installiert ist, und melden Sie sich an, bevor Sie Makros ausführen.

>[!IMPORTANT]
>
>Aus Sicherheitsgründen ist es nicht möglich, eine Arbeitsmappe mit einem Makro zu planen.

## `RefreshAllReportBuilderRequests()`

The `RefreshAllReportBuilderRequests()` macro refreshes all Report Builder requests in the active workbook. Es Beginn durch Aufruf der Report Builder-COM-Hinzufügen über seine Produkt-ID und ruft dann den `RefreshAllRequests()` API-Befehl auf:

```vba
Sub RefreshAllReportBuilderRequests()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshAllRequests(ActiveWorkbook)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInActiveWorksheet()`

The `RefreshAllReportBuilderRequestsInActiveWorksheet()` macro refreshes all Report Builder requests in the active worksheet. Der `RefreshWorksheetRequests()` API-Aufruf verwendet ein Arbeitsblattobjekt als Argument. Sie können diesen Aufruf für jedes Arbeitsblatt verwenden, das Report Builder-Anforderungen enthält:

```vba
Sub RefreshAllReportBuilderRequestsInActiveWorksheet()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshWorksheetRequests(ActiveWorkbook.ActiveSheet)
 
End Sub
```

## `RefreshAllReportBuilderRequestsInCellsRange()`

The `RefreshAllReportBuilderRequestsInCellsRange()` macro refreshes all Report Builder requests whose cell outputs intersect the specified range of cells. Der in diesem Beispiel verwendete Zellbereich verweist auf den Bereich `B1:B54` des &quot;Data&quot;-Arbeitsblatts in der aktiven Arbeitsmappe. Der Bereichsbereich-Ausdruck unterstützt alle unterstützten Excel-Ausdruck:

```vba
Sub RefreshAllReportBuilderRequestsInCellsRange()
 
 Dim addIn As COMAddIn
 Dim automationObject As Object
 Dim success As String
 Set addIn = Application.COMAddIns("ReportBuilderAddIn.Connect")
 Set automationObject = addIn.Object
 success = automationObject.RefreshRequestsInCellsRange("'Data'!B1:B54")
  
End Sub
```
