---
title: Feldbasiertes Stitching
description: Machen Sie sich mit den Voraussetzungen und Einschränkungen der Datenzuordnung mithilfe von feldbasiertem Stitching vertraut.
translation-type: ht
source-git-commit: beed7ffcc39b9b2628b1487b5e2eac42fa3a94d0
workflow-type: ht
source-wordcount: '499'
ht-degree: 100%

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

* Die feldbasierte Zuordnung funktioniert am besten bei Report Suites mit einer hohen Benutzeridentifizierungs- bzw. Benutzerauthentifizierungsrate.
* Obwohl Props und eVars jeweils Regeln hinsichtlich der Behandlung von Groß- und Kleinbuchstaben für Berichte haben, transformiert die feldbasierte Zuordnung die Eigenschaft oder eVar, die für das Zuordnen verwendet wird, in keinster Weise. Bei der feldbasierten Zuordnung wird der Wert im angegebenen Feld nach Anwendung der VISTA-Regeln und Verarbeitungsregeln verwendet. Beim Zuordnen wird zwischen Groß- und Kleinschreibung unterschieden. Wenn beispielsweise im Prop/eVar-Feld manchmal das Wort „Bob“ und manchmal das Wort „BOB“ angezeigt wird, werden diese im Zuordnungsprozess als zwei separate Personen behandelt.
* Da bei der feldbasierten Zuordnung die Groß- und Kleinschreibung beachtet werden muss, empfiehlt Adobe die Überprüfung aller VISTA-Regeln oder Verarbeitungsregeln, die für Prop oder eVar gelten, die für die feldbasierte Zuordnung verwendet werden. Sie müssen überprüft werden, um sicherzustellen, dass keine dieser Regeln neue Formen derselben ID einführt. So sollten Sie beispielsweise sicherstellen, dass keine VISTA-Regeln oder Verarbeitungsregeln dafür sorgen, dass bei Prop oder eVar nur für einen Teil der Treffer Kleinschreibung verwendet wird.
* Die Verwendung von mehr als einer Prop oder einer eVar zur Zuordnung wird von der feldbasierten Zuordnung nicht unterstützt. Wenn eVar12 beispielsweise eine Anmelde-ID und eVar20 eine E-Mail-ID enthält, müssen Sie eine davon auswählen.
* Bei der feldbasierten Zuordnung werden keine Felder kombiniert oder verkettet (z. B. eVar10 + prop5).
* Die Prop oder eVar sollte einen einzigen ID-Typ enthalten. Beispielsweise sollte die Prop oder eVar keine Kombination aus Anmelde-IDs und E-Mail-IDs aufweisen.
* Wenn mehrere Treffer mit demselben Zeitstempel für denselben Besucher auftreten, die jedoch unterschiedliche Werte bei der für die Zuordnung verwendeten Prop oder eVar haben, wird die Cross-Device-Analyse gemäß alphabetischer Reihenfolge wählen. Wenn also für Besucher A zwei Ereignisse mit demselben Zeitstempel vorliegen und eines der Ereignisse „Bob“ und das andere „Ann“ als Wert hat, wählt die Cross-Device-Analyse „Ann“.


## Nächste Schritte

Sobald Ihre Organisation alle Anforderungen erfüllt und die Einschränkungen versteht, können Sie mit der [Einrichtung der Cross-Device-Analyse](setup.md) beginnen.
