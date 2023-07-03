---
title: doubleEncodeLinkParameters
description: Aktivieren oder deaktivieren Sie die AppMeasurement-Doppelkodierung von Linktracking-Variablen.
exl-id: 7a4cea23-5ae6-4a8b-82a6-c68f9a1f9c49
feature: Variables
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 8%

---

# doubleEncodeLinkParameters

Die `doubleEncodeLinkParameters` ist ein boolescher Wert, der bestimmt, ob Linktracking-Variablen einmal kodiert werden (bei `false`) oder zweimal (wenn auf `true`). Es betrifft nur `linkName` (Teil der [`tl()`](../functions/tl-method.md) Methode) und [`linkURL`](linkurl.md). Es ist AppMeasurement 2.23.1 oder höher erforderlich. Der Standardwert dieser Variablen ist `true`.

In früheren Versionen von AppMeasurement waren Linktracking-Variablen immer zweimal URL-kodiert. Bei Implementierungen, die normalerweise auf Einzelbyte-Zeichen angewiesen sind, stellt die Doppelkodierung zwar kein Problem dar, sie hat aber falsch kodierte Werte für Multibytezeichen in Berichten erstellt. Diese Variable auf setzen `false` kodiert die Linktracking-Werte einmal, was normalerweise das gewünschte Verhalten ist.

* Wenn Ihre Implementierung Multi-Byte-Zeichen verwendet und Linktracking-Variablen URL-dekodiert sind, um die doppelte AppMeasurement zu versetzen, setzen Sie diese Variable auf . `true`. Dieser Wert behält bestehende AppMeasurement-Funktionen bei.
* Wenn Ihre Implementierung Multibyte-Zeichen verwendet und Sie keine URL-Dekodierung von Linktracking-Werten vornehmen, empfiehlt Adobe, diese Variable auf `false`.
* Wenn Ihre Implementierung keine Multibytezeichen verwendet, ist diese Variable nicht erforderlich. Adobe empfiehlt jedoch, diese Variable auf `false` in Fällen, in denen Multi-Byte-Zeichen möglicherweise gesendet werden.

## Doppelkodieren von Link-Parametern mit dem Web SDK

Diese Variable ist spezifisch für AppMeasurement und wird in keiner Web SDK-Implementierung benötigt.

## Doppelkodieren von Link-Parametern mit der Adobe Analytics-Erweiterung

In der Adobe Analytics-Erweiterung gibt es kein eigenes Feld, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s.doubleEncodeLinkParameters in AppMeasurement und im benutzerdefinierten Code-Editor der Analytics-Erweiterung

Die `s.doubleEncodeLinkParameters` ist ein boolescher Wert, der bestimmt, ob Linktracking-Werte doppelt kodiert werden. Wenn diese Variable nicht definiert ist, lautet der Standardwert `true` , um die Funktionalität für vorhandene Implementierungen beizubehalten. Adobe empfiehlt, diesen Wert auf `false` für alle neuen Implementierungen, insbesondere wenn in Linktracking-Berichten URL-kodierte Werte angezeigt werden.

```js
s.doubleEncodeLinkParameters = false;
```
