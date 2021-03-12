---
title: Feldbasiertes Stitching
description: Machen Sie sich mit den Voraussetzungen und Einschränkungen der Datenzuordnung mithilfe von feldbasiertem Stitching vertraut.
translation-type: tm+mt
source-git-commit: beed7ffcc39b9b2628b1487b5e2eac42fa3a94d0
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 35%

---


# Feldbasiertes Stitching

Cross-Device Analytics bietet zwei verschiedene Methoden der Datenzuordnung. Bei dieser Methode stützt sich auf eine Analytics-Variable, z. B. eine [Prop](/help/implement/vars/page-vars/prop.md) oder eine [eVar](/help/implement/vars/page-vars/evar.md), verwendet, die eine Personenkennung enthält. Diese Variable wird als Grundlage für die Verknüpfung von Geräten verwendet.

## Spezifische Voraussetzungen für feldbasiertes Stitching

Wenn Sie die geräteübergreifende Analyse mithilfe von feldbasiertem Stitching implementieren möchten, ist Folgendes erforderlich. Arbeiten Sie mit Teams in Ihrer Organisation und Ihrem Adobe-Kundenbetreuer zusammen, um sicherzustellen, dass Sie alle folgenden Kriterien erfüllen.

>[!IMPORTANT]
>
>Wenn nicht alle Voraussetzungen erfüllt sind, ist die Aktivierung der geräteübergreifenden Analyse unter Umständen nicht möglich oder die Ergebnisse bei der Datenzuordnung sind schlecht.

* Alle auf der [Übersichtsseite](overview.md) aufgeführten Voraussetzungen.
* Ihre Implementierung muss eine Prop oder eVar festlegen, die eine Person eindeutig identifiziert, wann immer dies möglich ist, z. B. wenn ein Benutzer sich anmeldet oder eine E-Mail öffnet. Diese Anforderung gilt für alle Plattformen, einschließlich mobiler Apps, wenn sie verwendet werden. Teilen Sie Ihrem Kundenbetreuer die gewünschte Identifizierungsvariable mit, wenn diese für feldbasiertes Stitching bereitgestellt wird.

## Spezifische Einschränkungen für feldbasiertes Stitching

* Die feldbasierte Suche funktioniert am besten bei Report Suites mit einer hohen Identifizierungs-/Authentifizierungsrate.
* Obwohl Props und eVars jeweils Regeln für die Behandlung von Groß- und Kleinbuchstaben für Berichte haben, transformiert die feldbasierte Suche die Eigenschaft oder das eVar, die für das Zuordnen verwendet wird, in keiner Weise. Bei der feldbasierten Suche wird der Wert im angegebenen Feld verwendet, da es Post VISTA-Regeln und Nachbearbeitungsregeln gibt. Beim Heften wird zwischen Groß- und Kleinschreibung unterschieden. Wenn beispielsweise in der Eigenschaftsvariablen/eVar manchmal das Wort &quot;Bob&quot;erscheint und manchmal das Wort &quot;BOB&quot;erscheint, werden diese beim Sticken als zwei separate Personen behandelt.
* Da bei der feldbasierten Suche die Groß-/Kleinschreibung beachtet werden muss, empfiehlt Adobe die Überprüfung aller VISTA-Regeln oder Verarbeitungsregeln, die für die prop oder eVar gelten, die für die feldbasierte Suche verwendet wird. Sie müssen überprüft werden, um sicherzustellen, dass keine dieser Regeln neue Formen derselben ID einführt. So sollten Sie beispielsweise sicherstellen, dass keine VISTA- oder Verarbeitungsregeln die Eigenschaftsvariable oder die eVar nur für einen Teil der Treffer einschränken.
* Die Verwendung von mehr als einer Prop oder einer eVar zu Heftzwecken wird nicht durch die feldbasierte Heftbildung unterstützt. Wenn eVar12 beispielsweise eine Anmelde-ID und eVar20 eine E-Mail-ID enthält, müssen Sie eine davon auswählen.
* Bei der feldbasierten Suche werden keine Felder kombiniert oder verkettet (z. B. eVar10 + prop5).
* Die Eigenschaftsvariable oder die eVar sollte einen einzelnen ID-Typ enthalten. Beispielsweise sollte die Eigenschaftsvariable oder die eVar keine Kombination aus Anmelde-IDs und E-Mail-IDs enthalten.
* Wenn mehrere Treffer mit demselben Zeitstempel für denselben Besucher, jedoch mit unterschiedlichen Werten in der Heftingeigenschaft oder in der eVar auftreten, wählt CDA eine alphabetische Reihenfolge. Wenn also Besucher A zwei Treffer mit demselben Zeitstempel hat und einer der Treffer Bob und der andere Ann angibt, wählt CDA Ann.


## Nächste Schritte

Sobald Ihr Unternehmen alle Anforderungen erfüllt und die Einschränkungen versteht, können Sie den Beginn [Einrichten von geräteübergreifenden Analysen](setup.md) ausführen.
