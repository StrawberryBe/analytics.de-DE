---
description: Die Zeileneinstellungen variieren je nachdem, welche Komponente Sie in die Tabelle gezogen haben.
title: Zeileneinstellungen
uuid: f30c31d5-1fd4-4b93-94c3-ca441099fe2e
translation-type: tm+mt
source-git-commit: a9dc84cbfcbdffc427155b1d4d44c94d7fa50a64
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 17%

---


# Zeileneinstellungen

Die Zeileneinstellungen variieren je nachdem, welche Komponente Sie in die Tabelle gezogen haben. Um auf die Tabellenzeileneinstellungen zuzugreifen, klicken Sie auf das Einstellungs-Symbol neben einer Dimension, einem Segment, einer Metrik, einem Zeitraum oder einer Aufschlüsselung im jeweiligen Element:

![](assets/row-settings.png)

| Einstellung | Beschreibung |
|--- |--- |
| Datumsausrichtung | Bei dieser Einstellung auf Tabellenebene werden Datumsangaben aus den einzelnen Spalten an allen Beginn in derselben Zeile ausgerichtet. Die Datumsausrichtung ist standardmäßig aktiviert, wenn eine Zeitdimension in den Tabellenzeilen verwendet wird und unterschiedliche Datumsbereiche in den Spalten angewendet werden. In einer Tabelle mit Tagespauschale, bei der Oktober und September auf die Spalten angewendet werden, werden die Beginn mit der linken Spalte mit dem 1. Oktober und die Beginn mit der rechten Spalte mit dem 1. September angezeigt. |
| Aufschlüsselung nach Position | Standardmäßig ist diese Einstellung deaktiviert und die Aufschlüsselungen sind auf statische Zeilenelemente fixiert. Nehmen wir beispielsweise an, Sie unterteilen die drei wichtigsten Dimensionselemente der Seite (Homepage, Suchergebnisse, Kasse) nach Marketing-Kanal. Dann verlassen Sie das Projekt und kehren zwei Wochen später zurück. Nach dem erneuten Öffnen des Projekts haben sich die drei wichtigsten Seiten geändert. Jetzt sind Homepage, Suchergebnisse und Kasse die Top-4-6-Seiten. Standardmäßig werden Ihre Marketing-Kanal-Aufschlüsselungen weiterhin unter Homepage, Suchergebnisse und Checkout angezeigt, auch wenn sie sich jetzt in den Zeilen 4-6 befinden. <br> Im Gegensatz dazu werden bei einer **Aufschlüsselung nach Position** immer die drei wichtigsten Elemente unterteilt, unabhängig davon, was sie sind. Wenn Sie auf unser Beispiel zurückgreifen, werden die Marketing Kanal-Aufschlüsselungen beim erneuten Öffnen des Projekts an die drei obersten Tabellenseiten gebunden, nicht an Homepage, Suchergebnisse und Checkout, die sich nun in den Zeilen 4 bis 6 befinden. |
| Prozentsatz | **Die Standardeinstellung ist die Berechnung der Prozentsätze nach Spalte** . die in einer Spalte sichtbaren Prozentsätze werden auf Basis der Spaltensumme berechnet. <br>**Die Berechnung der Prozentsätze nach Zeile **zwingt die Freiform-Tabelle, die Zellprozentsätze in der Zeile zu berechnen, anstatt in der Spalte, wobei die Gesamtsumme als Nenner dient. Dies ist besonders nützlich für die Trend-Darstellung von Prozentangaben. Diese Einstellung ist bei Verwendung des Visualize-Symbols standardmäßig aktiviert. |
| Spaltensummen | Diese Einstellungen sind nur für [statische Zeilen](manual-vs-dynamic-rows.md)verfügbar. <br> **Die Summe der aktuellen Zeilen** zeigt eine clientseitige Summe der Zeilen in der Tabelle an. Dies bedeutet, dass die Gesamtsumme die Metriken zum Duplikat wie Besuche oder Besucher *nicht* entfernt. <br> **Die Gesamtsumme** anzeigen zeigt eine serverseitige Summe an, was bedeutet, dass die Metriken zum Entfernen des Duplikats insgesamt gelöscht werden. |
