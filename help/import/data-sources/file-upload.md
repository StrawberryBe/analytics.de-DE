---
title: Hochladen der Datenquellendatei in Adobe
description: Der Prozess zum Hochladen einer Datenquellendatei in Adobe Analytics zur Erfassung.
exl-id: 64e3cd70-b511-4c4e-abd0-94eb36bc3519
feature: Data Sources
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# Hochladen der Datenquellendatei in Adobe

Das Senden einer Datenquellendatei an Adobe umfasst einen typischen authentifizierten FTP-Workflow. Sie können Windows Explorer, Finder oder einen dedizierten FTP-Client verwenden, um die gewünschten Dateien zum FTP-Speicherort der Adobe hochzuladen.

Suchen Sie die FTP-Anmeldeinformationen im [Data Sources Manager](manage.md). Jede Datenquelle enthält einen Link zu **[!UICONTROL FTP-Info]**. Jeder FTP-Speicherort ist für diese spezifische Datenquelle vorgesehen. Sie können nicht denselben FTP-Speicherort für mehrere Datenquellen verwenden.

Aus Sicherheitsgründen sind FTP-Standorte ohne Aktivität für mehr als 30 Tage deaktiviert.

## Die `.fin` file

Ein wichtiger Teil der erfolgreichen Aufnahme einer Datenquellendatei ist die Einbeziehung eines `.fin` -Datei. Diese Datei zeigt der Adobe an, dass die Datendatei zur Verarbeitung bereit ist. Wenn Sie eine Datenquellendatei ohne entsprechende `.fin` -Datei, verarbeitet Adobe diese Daten nie.

Die `.fin` -Datei weist die folgenden Eigenschaften auf:

* Die Datei enthält eine `.fin` -Erweiterung. Stellen Sie sicher, dass Ihr Betriebssystem es Ihnen ermöglicht, Dateitypen anzuzeigen und zu bearbeiten.
* Die Datei ist leer. Speichern Sie keine Daten in der `.fin` -Datei.
* Die Datei hat genau den gleichen Namen wie die Datenquellendatei. Wenn Sie beispielsweise eine Datenquellendatei mit dem Namen `example.txt`, die `.fin` file **must** be name `example.fin`. Wenn sie nicht den gleichen Namen haben, verarbeitet Adobe die Datenquellendatei nie.

Einmal sowohl die Datenquellendatei als auch `.fin` auf die FTP-Site hochgeladen werden, verarbeitet Adobe die Datei. Laden Sie die `.fin` Datei, bis die Datenquellendatei vollständig hochgeladen wurde. Wenn die Variable `.fin` -Datei vorzeitig hochgeladen wird, ruft Adobe die teilweise hochgeladene Datei ab und erfasst sie, was zu Fehlern führt.

## Verarbeitungsreihenfolge

Wenn Sie mehrere Dateien gleichzeitig auf die FTP-Site hochladen, erfasst Adobe sie in alphanumerischer Reihenfolge. Wenn Ihre Organisation erfordert, dass Dateien in einer bestimmten Reihenfolge erfasst werden, stellen Sie sicher, dass ihre Dateinamen alphanumerisch benannt sind.

## Verarbeitungszeit

Um eine schnellste Dateiverarbeitung zu gewährleisten, empfiehlt Adobe, metrische Daten in einer einzigen Zeile pro Datum zu aggregieren. Diese Datenquellendatei wäre zwar gültig, würde jedoch langsamer verarbeitet:

| `date` | `eVar1` | `event1` | `event2` | `event3` |
| --- | --- | --- | --- | --- |
| `07/24/YYYY` | `red` | `1` | | |
| `07/24/YYYY` | `red` | `1` | | |
| `07/24/YYYY` | `red` | | `1` | |
| `07/24/YYYY` | `red` | | | `1` |

Diese Datei würde schneller verarbeitet werden, da sie dieselben Daten enthält:

| `date` | `eVar1` | `event1` | `event2` | `event3` |
| --- | --- | --- | --- | --- |
| `07/24/YYYY` | `red` | `2` | `1` | `1` |
