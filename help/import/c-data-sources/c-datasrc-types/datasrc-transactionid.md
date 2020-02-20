---
title: Transaktions-ID-Datenquellen
description: Erfahren Sie mehr über den allgemeinen Arbeitsablauf bei der Verwendung von Transaktions-ID-Datenquellen.
translation-type: tm+mt
source-git-commit: a5c3d9b2cd02dc7e89abb469e2e0e44985a17638

---


# Transaktions-ID-Datenquellen

Transaktions-ID-Datenquellen ermöglichen es Ihnen, nicht nur Online- und Offlinedaten nebeneinander anzuzeigen, sondern die Daten miteinander zu verbinden. Es erfordert die Verwendung der [`transactionID`](/help/implement/vars/page-vars/transactionid.md) Variablen in Ihrer Analytics-Implementierung.

Wenn Sie einen Online-Treffer senden, der einen `transactionID` Wert enthält, erstellt Adobe einen &quot;Schnappschuss&quot;aller Variablen, die zu diesem Zeitpunkt festgelegt wurden oder beibehalten wurden. Wenn eine übereinstimmende Transaktions-ID gefunden wird, die über Data Sources hochgeladen wurde, werden die Offline- und Onlinedaten miteinander verknüpft. Es spielt keine Rolle, welche Datenquelle zuerst gesehen wird.

## Gesamtarbeitsablauf für Transaktions-ID-Datenquellen

Verwenden Sie den folgenden generischen Arbeitsablauf, um mit der Verwendung von Transaktions-ID-Datenquellen zu beginnen:

1. Erstellen Sie eine Datenquelle (&quot;Generisch&quot;und &quot;Generische Datenquelle (Transaktions-ID)&quot;).
1. Folgen Sie dem Setup-Assistenten für Datenfeeds, um einen FTP-Speicherort zum Hochladen von Daten und Herunterladen einer Vorlagendatei für Datenquellen abzurufen.
1. Aktualisieren Sie Ihre Implementierung, um die `transactionID` Variable einzuschließen.
1. Laden Sie eine Datenquellen-Datei mit einer `.fin` Datei auf die FTP-Site hoch.
