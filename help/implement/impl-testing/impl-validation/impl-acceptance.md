---
description: Vorgehensweise bei der Implementierung
keywords: Analytics-Implementierung
seo-description: Vorgehensweise bei der Implementierung
seo-title: Annahme der Implementierung
solution: Analytics
title: Annahme der Implementierung
topic: Entwickler und Implementierung
uuid: 6 f 7 ec 56 e -9 e 4 f -4 dc 8-b 534-92 b 1580 b 5 b 47
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Annahme der Implementierung

Vorgehensweise bei der Implementierung

Die Implementierung wird auf die folgende Weise durchgeführt.

1. Der Adobe-Berater stellt die Anforderungen hinsichtlich der Berichterstellung zusammen und erstellt auf dieser Grundlage einen Datenerfassungsplan.

   Der Datenerfassungsplan enthält die Variablendefinitionen, die erforderlichen VISTA-Regeln, benutzerdefinierte JavaScript-Elemente, die Zusammenhänge zwischen den Daten und alle Einstellungen für die einzelnen Report Suites. Der Kunde füllt den Implementierungsfragebogen aus.
1. Technische Mitarbeiter implementieren clientseitig den Code, sitespezifisches JavaScript und serverseitige Variablen.
1. Der Adobe-Berater kümmert sich um technische Probleme während der Implementierung und hilft ggf. bei der Ausarbeitung von Lösungen.
1. Technische Mitarbeiter führen die clientseitige Endprüfung der Implementierung durch.

   Testers log in to [!DNL Analytics] and verifying all variables ( *`page name`*, *`channel`*, *`server`*, *`events`*, *`campaign`*, econversion variables, custom traffic variables, *`products`*, and all other variables).
1. Der Kunde teilt Adobe den Abschluss der Implementierung mit.

   Der Kunde übergibt dem Adobe-Berater eine Validierungsstichprobe (Datenstichprobe) zum Überprüfen der Datengenauigkeit. (VISTA-generierte Report Suites werden durch Vergleich der entsprechenden Metriken überprüft. Welche Metriken überprüft werden sollen, müssen der Kunde und Adobe zuvor während der Erstellung der VISTA-Regeln vereinbaren.)
1. Der Kunde übermittelt eine Abnahmebestätigung für die Implementierung per Fax (oder unterschreibt diese online) für die entsprechende(n) Site(s).
1. Nach Erhalt der Abnahmebestätigung aktiviert der Adobe-Berater die Adobe Best Practices – Implementierungsbestätigung in der Schnittstelle.
1. Optional kann der Kunde auch Überwachungsdienste für Schlüsselseiten der implementierten Site mit Adobe vereinbaren (diese sind für gewöhnlich die primären Vorlagen, Homepage und wichtige Entrypages).

   Diese Überwachungssoftware – die in einem separaten Dokument beschrieben wird – verfolgt Seiten, indem sie die Seite lädt, ausführt und dann die Bildanforderung mit einer Grundlage vergleicht, die in einer Datenbank gespeichert ist. Wenn Unterschiede festgestellt werden, benachrichtigt die Software dafür vorgesehene Mitarbeiter von Adobe (AM/IE) und vom Kunden per E-Mail.

Mithilfe der folgenden Punkte lässt sich eine erfolgreiche Implementierung sicherstellen:

* Ein Dokument mit Best Practices für den Kunden, in dem die Vorgänge detailliert beschrieben sind
* Das Validierungsdokument, das der Kunde bei der Endprüfung der Implementierung verwendet
* Ein Abnahmeformular, das der Kunde unterschreibt
* Eine Überwachungsanwendung, die die Tags durchgehend validiert
* Eine Partnerschaft mit Accenture zur Hilfe beim Testen der Implementierung
* Hilfsprogramme/Tools für den Vergleich von Seitenansichten und/oder Bestellungen. Diese Vergleiche können sich ziemlich komplex gestalten.
* Eine Methode oder Vorgehensweise zum schnellen Erhalt des Debugprotokolls für einen bestimmten Tag und bestimmte Report Suite-IDs

