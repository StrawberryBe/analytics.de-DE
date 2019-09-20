---
description: Wenn ein Bericht eine große Anzahl individueller Werte aufweist, stellt Adobe eine Funktion bereit, mit der sichergestellt wird, dass die wichtigsten Werte in Ihrem Bericht angezeigt werden.
seo-description: Wenn ein Bericht eine große Anzahl individueller Werte aufweist, stellt Adobe eine Funktion bereit, mit der sichergestellt wird, dass die wichtigsten Werte in Ihrem Bericht angezeigt werden.
seo-title: Niedriger Traffic-Wert in Adobe Analytics
solution: Analytics
title: Niedriger Traffic-Wert in Adobe Analytics
topic: Metriken
uuid: 56f723f8-94e8-478f-8ea3-16dad21dfa1f
translation-type: tm+mt
source-git-commit: 22fc459dae1a57a387511560e7039c7085e30551

---


# Niedriger Traffic-Wert in Adobe Analytics

Wenn ein Bericht eine große Anzahl individueller Werte aufweist, stellt Adobe eine Funktion bereit, mit der sichergestellt wird, dass die wichtigsten Werte in Ihrem Bericht angezeigt werden. Eindeutige Variablenwerte, die nach etwa 500.000 vorhandenen Werten gesammelt wurden, werden unter einem Zeileneintrag mit dem Titel **(geringer Traffic)** aufgeführt.

## Funktionsweise von geringem Traffic

* Die Berichterstellung ist nicht betroffen, wenn die Variable in einem bestimmten Monat nicht 500.000 individuelle Werte erreicht.
* Wenn eine Variable diesen ersten Schwellenwert von 500.000 erreicht, werden die Daten unter geringem Traffic erfasst. Jeder Wert, der über diesen Schwellenwert hinausgeht, durchläuft die folgende Logik:
   * Wenn ein Wert bereits in Berichten enthalten ist, fügen Sie ihn wie gewohnt hinzu.
   * Wenn ein Wert noch nicht in der Berichterstellung enthalten ist, überprüfen Sie, ob dieser Wert heute mehr als etwa zehnmal angezeigt wurde. Ist dies der Fall, fügen Sie diesen Wert der Berichterstellung hinzu. Wenn es nicht mehr als zehnmal gezählt wurde, lassen Sie es unter geringem Traffic.
* Wenn eine Report Suite mehr als 1.000.000 individuelle Werte erreicht, wird eine aggressivere Filterung angewendet:
   * Wenn ein Wert bereits in Berichten enthalten ist, fügen Sie ihn wie gewohnt hinzu.
   * Wenn ein Wert noch nicht in der Berichterstellung enthalten ist, überprüfen Sie, ob dieser Wert heute mehr als etwa 100 Mal angezeigt wurde. Ist dies der Fall, fügen Sie den Wert der Berichterstellung hinzu. Wenn nicht, lassen Sie es unter geringem Traffic.

> [!NOTE] Wenn ein Variablenwert ausreichend Traffic erhält, um den Bucket mit niedrigem Traffic zu verlassen, werden die ersten erfassten Werte nicht zu dem entsprechenden Zeilenelement verschoben. Diese ersten 10 bis 100 Instanzen bleiben unter geringem Traffic.

## Ändern der eindeutigen Grenzwerte

Die Schwellenwerte liegen standardmäßig bei 500.000 und einer Million individuellen Werten. Diese Beschränkungen können variablenweise geändert werden. Wenden Sie sich an den Kundenbetreuer Ihres Unternehmens, um diese Änderung anzufordern. Schließen Sie beim Anfordern einer Änderung Folgendes ein:

* Die Report Suite-ID
* Die Variable, für die Sie den Schwellenwert für
* Sowohl der erste als auch der zweite Schwellenwert wurden gewünscht

Änderungen an Schwellenwerten können sich auf die Berichtleistung auswirken. Adobe empfiehlt dringend, bei der Anforderung einer Erhöhung der eindeutigen Werte in einer Variablen ein gutes Urteilsvermögen zu verwenden.

Schwellenwerte für niedrigen Traffic sind in der Analytics-Benutzeroberfläche nicht sichtbar. Bitten Sie einen unterstützten Benutzer Ihres Unternehmens, sich an den Adobe-Kundendienst zu wenden, wenn Sie weitere Informationen zu den vorhandenen Schwellenwerten wünschen.

## Low-Traffic mit Komponenten und anderen Funktionen

Verschiedene Funktionen behandeln Werte mit geringem Traffic auf unterschiedliche Weise.

* **** Data Warehouse: Die Anzahl der eindeutigen Werte in Data Warehouse-Berichten ist unbegrenzt. Die einzigartige Architektur ermöglicht die Berichterstellung beliebiger individueller Werte.
   * In einigen eingeschränkten Szenarien können Werte mit niedrigem Traffic weiterhin angezeigt werden. Beispiele sind Listenvariablen, Listeneigenschaftsvariablen, Merchandising-eVars und Marketingkanal-Detaildimensionen.
* **** Segmentierung: Wenn die Segmentkriterien eine Variable mit einer hohen Anzahl individueller Werte enthalten, werden unter niedrigem Traffic erfasste Werte nicht berücksichtigt.
* **** Klassifizierungen: Classification-Berichte unterliegen auch eindeutigen Beschränkungen. Wenn der Wert der übergeordneten Variablen einer Klassifizierung unter geringer Traffic-Traffic-Aufkommen fällt, wird der Wert nicht klassifiziert.
   * Wenn Sie Werte klassifizieren, bevor sie in den Daten angezeigt werden, werden diese Werte für den eindeutigen Schwellenwert für diesen Monat angerechnet.
