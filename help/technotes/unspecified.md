---
description: Je nach angezeigtem Bericht können in verschiedenen Berichten in Adobe Analytics "Nicht angegeben", "Sonstige"oder "Unbekannt"angezeigt werden. Im Allgemeinen bedeutet dieser Zeileneintrag, dass die Variable nicht definiert wurde oder anderweitig nicht verfügbar war.
title: Nicht angegeben, Sonstige und Unbekannt in Berichten
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# "Nicht angegeben", "Sonstige"und "Unbekannt"in Berichten

Je nach angezeigtem Bericht können in verschiedenen Berichten in Adobe Analytics "Nicht angegeben", "Sonstige"oder "Unbekannt"angezeigt werden. Im Allgemeinen bedeutet dieser Zeileneintrag, dass die Variable nicht definiert wurde oder anderweitig nicht verfügbar war. Im Folgenden finden Sie eine vollständige Liste, die zeigt, wie die einzelnen Berichte eines dieser Zeilenelemente enthalten können.

## „Nicht angegeben“ in Berichten

"Nicht angegeben"ist ein relativ häufiger Zeileneintrag in Berichten.

* **** Ein Ereignis wird ohne Konversionsvariable ausgelöst: Ein Benutzer ruft beispielsweise Ihre Site auf und tätigt einen Kauf ohne eVar1-Wert. Wenn Sie Bestellungen mit der eVar1-Dimension anzeigen, gibt es keinen Wert, dem diese Reihenfolge zugeordnet werden kann. Daher wird sie automatisch "Nicht angegeben"zugeordnet.
* **** Nicht klassifizierte Daten in Classification-Berichten: Beim Anzeigen von Classification-Daten gibt jeder Wert, dem keine Daten mit dieser Classification zugeordnet sind, "Nicht angegeben"zurück. Um dieses Problem zu beheben, klassifizieren Sie den Wert der übergeordneten Variablen.
* **** Aufschlüsselungsberichte, bei denen nur eine Variable ausgelöst wurde: Wenn Sie eine Aufschlüsselung auf eine Variable anwenden, muss jede Instanz dieser Variable berücksichtigt werden. Wenn die zweite Variable nicht angezeigt wurde oder sie von einem vorherigen Treffer beibehalten wurde, lautet der Dimensionswert "Nicht angegeben".
* **** Nicht-mobile Treffer in Mobilberichten: Alle nicht-mobilen Treffer in Mobilberichten werden als "Nicht angegeben"aufgeführt ("Nicht mobil"in Reports &amp; Analysen).

## „Sonstige“ in Berichten

"Sonstige"kann in Berichten zwar selten vorkommen, jedoch unter verschiedenen Umständen:

* **** Seiten werden außerhalb der internen URL-Filter ausgelöst: Dieser Wert dient zum Schutz vor Datenbetrug, z. B. wenn eine andere Organisation Ihren Quellcode stiehlt und ihn auf ihrer eigenen Site implementiert. Um dieses Problem zu beheben, vergewissern Sie sich, dass alle URLs, die Ihr Code implementiert hat, mit den internen URL-Filtern in den Report Suite-Einstellungen übereinstimmen.
* **Besucher, die einen selten verwendeten Browser nutzen:** Im Bericht zu den Browsertypen wird „Sonstige“ als Aufschlüsselung angegeben, wenn Benutzer einen wenig genutzten Browsertyp einsetzen. Es gibt eine Vielzahl an Organisationen, die Browser herstellen. Alle Browser, die von größeren Organisationen nicht erstellt wurden, werden in "Sonstige"zusammengefasst, um eine Übersichtlichkeit in Berichten zu vermeiden.

## „Unbekannt“ in Berichten

„Unbekannt“ kann unter folgenden Umständen auftreten:

* **** Nicht-Browser-Treffer bei Ansicht von Technologieberichten: Wenn eine AppMeasurement-Bibliothek nicht ermitteln kann, ob eine Funktion unterstützt wird, wird in der Berichterstellung "Unbekannt"angezeigt.
* **** Verwenden von Segmenten, auf die keine Komponenten zugreifen können: Stellen Sie sicher, dass die in einem Segment verwendeten Variablen aktiviert sind und dass Benutzer darauf zugreifen können. Wenn ein Benutzer keinen Zugriff auf eine Segmentkomponente hat oder eine Variable deaktiviert ist, wird "Unbekannt"angezeigt.

## Filterung dieser Werte in Berichten {#section_5536E2B419D445D39C932E8F12C0070C}

In den meisten Fällen ist es sicherer, diese Zeilenelemente zu ignorieren. Mit dem Suchfilter können Sie sie bei Bedarf entfernen.

Some backend data variables use the value `::unspecified::` in reporting, though it is not shown in the interface. Wenn ein Suchfilter keine Daten ausschließt, versuchen Sie, diesen Wert (einschließlich der Doppelpunkte) zu verwenden.
