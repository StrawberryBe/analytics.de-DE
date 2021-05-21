---
description: Verschiedene Berichte in Adobe Analytics können abhängig vom aufgerufenen spezifischen Bericht „Nicht angegeben“, „Keine“, „Sonstige“ oder „Unbekannt“ anzeigen. Im Allgemeinen bedeutet dieser Zeileneintrag, dass die Variable nicht definiert wurde oder anderweitig nicht verfügbar war.
title: „Nicht angegeben“, „Keine“, „Sonstige“ und „Unbekannt“ in Berichten
exl-id: 35451239-91f3-400a-981e-8c3fbc0e4185
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '515'
ht-degree: 100%

---

# „Nicht angegeben“, „Keine“, „Sonstige“ und „Unbekannt“ in Berichten

Verschiedene Berichte in Adobe Analytics können abhängig vom aufgerufenen spezifischen Bericht „Nicht angegeben“, „Sonstige“ oder „Unbekannt“ anzeigen. Im Allgemeinen bedeutet dieser Zeileneintrag, dass die Variable nicht definiert wurde oder anderweitig nicht verfügbar war. Im Folgenden finden Sie eine vollständige Liste, die zeigt, wie die einzelnen Berichte eines dieser Zeilenelemente enthalten können.

## „Nicht angegeben“ (oder „Keine“) in Berichten

„Nicht angegeben“ ist ein relativ häufiger Zeileneintrag in Berichten. Er wird auch häufig als „Keine“ bezeichnet.

* **Ein Ereignis löst ohne Konversionsvariable aus:** Wenn z. B. ein Benutzer Ihre Website besucht und einen Kauf tätigt, ohne dass ein eVar1-Wert ausgelöst wird. Wenn Sie die Bestellungen mit der eVar1-Dimension anzeigen, ist kein Wert vorhanden, dem diese Bestellung zugeordnet wird. Daher wird ihm automatisch „Nicht angegeben“ zugeordnet.
* **Unklassifizierte Daten in Classification-Berichten:** Wenn Sie Classification-Daten anzeigen, wird für alle Werte, denen keine Daten mit dieser Classification zugeordnet sind, „Nicht angegeben“ aufgeführt. Um dieses Problem zu beheben, klassifizieren Sie den Wert der übergeordneten Variablen.
* **Detailberichte, bei denen nur eine Variable ausgelöst wurde:** Wenn Sie eine Aufschlüsselung auf eine Variable anwenden, muss jede Instanz dieser Variable berücksichtigt werden. Wenn die zweite Variable nicht angezeigt wurde oder sie von einem vorherigen Treffer beibehalten wurde, lautet das Dimensionselement „Nicht angegeben“.
* **Nicht mobile Treffer in Mobilgeräteberichten:** Alle nicht mobilen Treffer in Mobilgeräteberichten werden als „Nicht angegeben“ aufgeführt (in Reports &amp; Analytics als „Nicht mobil“).

## „Sonstige“ in Berichten

„Sonstige“ kommt zwar selten vor, kann aber unter verschiedenen Umständen in Berichten auftreten:

* **Seiten werden außerhalb der internen URL-Filter ausgelöst:** Dieser Wert dient zum Schutz vor Datenbetrug, z. B. wenn eine andere Organisation Ihren Quell-Code stiehlt und ihn auf ihrer eigenen Site implementiert. Um dieses Problem zu korrigieren, müssen Sie sicherstellen, dass alle URLs, auf denen die Implementierung Ihres Codes basiert, zu den internen URL-Filtern in Ihren Report Suite-Einstellungen passen.
* **Besucher, die einen selten verwendeten Browser nutzen:** Im Bericht zu den Browsertypen wird „Sonstige“ als Aufschlüsselung angegeben, wenn Benutzer einen wenig genutzten Browsertyp einsetzen. Es gibt eine Vielzahl an Organisationen, die Browser herstellen. Alle Browser, die nicht von größeren Anbietern entwickelt wurden, werden unter „Sonstige“ zusammengefasst, um die Übersichtlichkeit in Berichten zu gewährleisten.

## „Unbekannt“ in Berichten

„Unbekannt“ kann unter folgenden Umständen auftreten:

* **Nicht-Browser-Treffer bei Anzeige von Technologieberichten:** Wenn eine AppMeasurement-Bibliothek nicht ermitteln kann, ob eine Funktion unterstützt wird, wird im Reporting „Unbekannt“ angezeigt.
* **Verwendung von Segmenten, auf die keine Komponenten zugreifen können:** Stellen Sie sicher, dass die in einem Segment verwendeten Variablen aktiviert sind und dass Anwender darauf zugreifen können. Wenn ein Anwender keinen Zugriff auf eine Segmentkomponente hat oder eine Variable deaktiviert ist, wird „Unbekannt“ angezeigt.

## Filterung dieser Werte in Berichten {#section_5536E2B419D445D39C932E8F12C0070C}

In den meisten Fällen ist es sicherer, diese Zeilenelemente zu ignorieren. Mit dem Suchfilter können Sie sie bei Bedarf entfernen.

Einige Backend-Datenvariablen verwenden den Wert `::unspecified::` in Berichten, der jedoch nicht in der Benutzeroberfläche angezeigt wird. Wenn ein Suchfilter keine Daten ausschließt, versuchen Sie, diesen Wert (einschließlich der Doppelpunkte) zu verwenden.
