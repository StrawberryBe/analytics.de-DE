---
title: Verwenden von Visual Basic-Makros in Report Builder
description: Erfahren Sie, wie Sie die Funktionalität von Excel-Arbeitsmappen und Report Builder mithilfe von VBA-Makros erweitern.
feature: Report Builder
role: User, Admin
exl-id: 0d92bce2-22ae-4b0c-af1d-3d12f2041ddf
source-git-commit: 66b7de0b008364e47253d319785c204ca479ab26
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 68%

---

# Visual Basic-Makros in Report Builder

Visual Basic (VBA)-Makros bieten Funktionen, mit denen Sie Excel-Arbeitsmappen aktualisieren können. Visual Basic hat Zugriff auf die Arbeitsmappe, Excel und Windows.

Sie müssen die neueste Version von Report Builder ausführen und sich anmelden, bevor Sie VBA-Makros ausführen.

>[!IMPORTANT]
>
>Aus Sicherheitsgründen ist es nicht möglich, eine Arbeitsmappe mit einem Makro zu planen.

Adobe unterstützt drei Report Builder-API-Methoden.

## `RefreshAllReportBuilderRequests()`

Das `RefreshAllReportBuilderRequests()`-Makro aktualisiert alle Report Builder-Anforderungen in der aktiven Arbeitsmappe. Zunächst wird das COM-Add-In von Report Builder über seine Produkt-ID und anschließend der `RefreshAllRequests()`-API-Befehl aufgerufen:

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

Das `RefreshAllReportBuilderRequestsInActiveWorksheet()`-Makro aktualisiert alle Report Builder-Anforderungen im aktiven Arbeitsblatt. Der `RefreshWorksheetRequests()`-API-Aufruf verwendet ein Arbeitsblattobjekt als Argument. Sie können diesen Aufruf für jedes Arbeitsblatt verwenden, das Report Builder-Anforderungen enthält:

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

Das `RefreshAllReportBuilderRequestsInCellsRange()`-Makro aktualisiert alle Report Builder-Anforderungen, deren Zellenausgabe den angegebenen Zellbereich überschneidet. Der in diesem Beispiel verwendete Zellbereich verweist auf den Bereich `B1:B54` des „Data“-Arbeitsblatts in der aktiven Arbeitsmappe. Der Bereichsausdruck unterstützt alle unterstützten Bereichsausdrücke in Excel:

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
