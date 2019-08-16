---
description: Verschiedene Berichte in Adobe Analytics können abhängig vom angezeigten spezifischen Bericht Nicht angegeben, Sonstige oder Unbekannt angezeigt werden. Im Allgemeinen bedeutet dieses Zeilenelement, dass die Variable nicht definiert oder anderweitig nicht verfügbar war.
seo-description: Verschiedene Berichte in Adobe Analytics können abhängig vom angezeigten spezifischen Bericht Nicht angegeben, Sonstige oder Unbekannt angezeigt werden. Im Allgemeinen bedeutet dieses Zeilenelement, dass die Variable nicht definiert oder anderweitig nicht verfügbar war.
seo-title: Nicht angegeben, Sonstige und Unbekannt in Berichten
solution: Analytics
title: Nicht angegeben, Sonstige und Unbekannt in Berichten
translation-type: tm+mt
source-git-commit: 5776b478580fea10a3a954f2e53048c3f0e1f9da

---


# Nicht angegeben, Sonstige und Unbekannt in Berichten

Verschiedene Berichte in Adobe Analytics können abhängig vom angezeigten spezifischen Bericht Nicht angegeben, Sonstige oder Unbekannt angezeigt werden. Im Allgemeinen bedeutet dieses Zeilenelement, dass die Variable nicht definiert oder anderweitig nicht verfügbar war. Im Folgenden finden Sie eine vollständige Liste, die zeigt, wie die einzelnen Berichte eines dieser Zeilenelemente enthalten können.

## "Nicht angegeben" in Berichten

"Nicht angegeben" ist ein ziemlich allgemeiner Zeileneintrag in Berichten.

* **Ein Ereignis wird ohne Konversionsvariable ausgelöst:** Beispiel: Ein Benutzer besucht Ihre Site und kauft einen Kauf ohne evar 1-Wert ein. Wenn Sie Bestellungen mit der evar 1-Dimension anzeigen, gibt es keinen Wert, dem diese Bestellung zugeordnet wird. Daher wird es automatisch "Nicht angegeben" zugeordnet.
* **Unklassifizierte Daten in Classification-Berichten:** Wenn Sie Classification-Daten anzeigen, wird für alle Werte, denen keine Daten mit dieser Classification zugeordnet sind, „Nicht angegeben“ aufgeführt. Um dieses Problem zu beheben, klassifizieren Sie den Wert der übergeordneten Variablen.
* **Unterteilungsberichte, bei denen nur eine Variable ausgelöst wurde:** Wenn Sie eine Aufschlüsselung auf eine Variable anwenden, muss jede Instanz dieser Variablen berücksichtigt werden. Wenn die zweite Variable nicht gesehen wurde oder wenn sie von einem vorherigen Treffer beibehalten wurde, lautet der Dimensionswert "Nicht angegeben" .
* **Nicht-Mobiltreffer in Mobilberichten:** Alle Nicht mobilen Treffer in Mobilberichten werden als "Nicht angegeben" ("Nicht angegeben" in Reports &amp; Analysen) aufgeführt.

## "Sonstige" in Berichten

Obwohl die Berichte in der Berichterstellung etwas seltener sind, kann sie unter verschiedenen Umständen auftreten:

* **Seiten lösen außerhalb interner URL-Filter aus:** Dieser Wert dient zur Verhinderung von Datenbetrug, z. B. wenn eine andere Organisation Ihren Quellcode stehst und ihn auf ihrer eigenen Site implementiert. Um dieses Problem zu beheben, stellen Sie sicher, dass alle urls, auf denen Ihr Code implementiert ist, den internen URL-Filtern in Ihren Report Suite-Einstellungen entsprechen.
* **Besucher, die einen selten verwendeten Browser nutzen:** Im Bericht zu den Browsertypen wird „Sonstige“ als Aufschlüsselung angegeben, wenn Benutzer einen wenig genutzten Browsertyp einsetzen. Es gibt eine Vielzahl an Organisationen, die Browser herstellen. Alle Browser, die größere Organisationen nicht erstellen, werden in "Sonstige" zusammengefasst, um zu verhindern, dass Berichte übersichtlicher werden.

## "Unbekannt" in Berichten

"Unbekannt" kann unter verschiedenen Umständen auftreten:

* **Nicht-Browser-Treffer beim Anzeigen von Technologieberichten:** Wenn eine appmeasurement-Bibliothek nicht feststellen kann, ob eine Funktion unterstützt wird, wird "Unbekannt" in den Berichten angezeigt.
* **Verwenden von Segmenten, auf die Komponenten nicht zugreifen können:** Stellen Sie sicher, dass in einem Segment verwendete Variablen aktiviert sind und dass Benutzer darauf zugreifen können. Wenn ein Benutzer keinen Zugriff auf eine Segmentkomponente hat oder wenn eine Variable deaktiviert ist, wird "Unbekannt" angezeigt.

## Filterung dieser Werte in Berichten {#section_5536E2B419D445D39C932E8F12C0070C}

In den meisten Fällen ist es sicherer, diese Zeilenelemente zu ignorieren. Der Suchfilter kann nach Wunsch entfernt werden.

Some backend data variables use the value `::unspecified::` in reporting, though it is not shown in the interface. Wenn ein Suchfilter keine Daten ausschließen kann, versuchen Sie es mit diesem Wert (einschließlich der Doppelpunkte).
