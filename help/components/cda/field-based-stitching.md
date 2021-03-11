---
title: Feldbasiertes Stitching
description: Machen Sie sich mit den Voraussetzungen und Einschränkungen der Datenzuordnung mithilfe von feldbasiertem Stitching vertraut.
translation-type: tm+mt
source-git-commit: 7b43c4ebbf9446507ab90a90e26c51635303dcc6
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 68%

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

* Feldbasiertes Stitching funktioniert am besten bei Report Suites mit einer hohen Benutzeridentifizierungsrate. Wenn Ihre Report Suite eine niedrige Identifizierungs- oder Anmelderate aufweist, sollten Sie das [Co-op-Diagramm](device-graph.md) verwenden.
* Obwohl Props und eVars jeweils Regeln für die Behandlung von Groß- und Kleinbuchstaben für Berichte haben, transformiert die feldbasierte Suche die Eigenschaft oder das eVar, die für das Zuordnen verwendet wird, in keiner Weise. Bei der feldbasierten Suche wird der Wert im angegebenen Feld verwendet, da es Post VISTA-Regeln und Nachbearbeitungsregeln gibt. Wenn das Wort &quot;Bob&quot;beispielsweise manchmal in der Eigenschaftsvariablen/eVar angezeigt wird und manchmal das Wort &quot;BOB&quot;angezeigt wird, werden diese als zwei separate Personen behandelt.

## Nächste Schritte

Sobald Ihr Unternehmen alle Anforderungen erfüllt und die Einschränkungen versteht, können Sie den Beginn [Einrichten von geräteübergreifenden Analysen](setup.md) ausführen.
