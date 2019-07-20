---
description: AJAX ist ein Konzept, das sich beim Webdesign zunehmender Beliebtheit erfreut, da hiermit dynamische Inhalte auf Webseiten durch Einsatz mehrerer Technologien erstellt und verwaltet werden können.
keywords: Analytics-Implementierung
seo-description: AJAX ist ein Konzept, das sich beim Webdesign zunehmender Beliebtheit erfreut, da hiermit dynamische Inhalte auf Webseiten durch Einsatz mehrerer Technologien erstellt und verwaltet werden können.
seo-title: AJAX-Tracking Rich Media-Anwendungen
solution: Analytics
title: AJAX-Tracking Rich Media-Anwendungen
topic: Entwickler und Implementierung
uuid: ffe 6 a 263-ae 18-4875-badb-b 3 aea 3 efcb 64
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# AJAX-Tracking Rich Media-Anwendungen

AJAX ist ein Konzept, das sich beim Webdesign zunehmender Beliebtheit erfreut, da hiermit dynamische Inhalte auf Webseiten durch Einsatz mehrerer Technologien erstellt und verwaltet werden können.

Die Verfolgung von Benutzerinteraktionen mit [!UICONTROL AJAX] und anderen Rich-Media-Anwendungen ist von zentraler Bedeutung, damit Analytics erfolgreich arbeitet und sich die in das Webdesign getätigten Investitionen bezahlt machen. Das vorliegende Whitepaper soll vor allem Empfehlungen für das Verfolgen von Rich Internet Applications (RIAs) – insbesondere solcher mit [!UICONTROL AJAX] – geben.

## Rich Internet Applications (RIA) {#section_CDCAFC4E05B44985BCBF34DFCB35DCA6}

Rich Internet Applications (RIAs) haben das Aussehen des Internets verändert. Sie erfüllen das, was bedarfsgesteuerte Technologien versprechen, indem sie eine wirklichkeitsnahe Bedienbarkeit für eine breite Anwenderschicht ermöglichen. Im Verlauf der Jahre sind RIAs immer ausgereifter geworden. Den größten Sprung nach vorne haben sie mit der breiten Einführung von Browsern gemacht, die die Technologien unterstützen, auf denen diese Anwendungen basieren. Auch wenn es bei RIAs die verschiedensten Ausführungen und Technologien gibt, sind AJAX und Flash die gängigsten und vielleicht auch beliebtesten Implementierungen. Allerdings darf man RIA nicht auf die zugrunde liegende Technologie reduzieren – es sind die Bedienbarkeit und der Einsatzzweck, die RIA ausmachen.

## Was soll rückverfolgt werden? {#section_E96EC5127E554B8384FD0A7A0B3118DF}

Eine der häufigsten Fragen im Zusammenhang mit RIA lautet, wie auf Mikroebene erfolgende Aktivitäten von solchen unterschieden werden sollen, die auf Makroebene stattfinden, und wann so eine Unterscheidung überhaupt sinnvoll ist. Ein Beispiel: Sie haben eine Anwendung, mit der Kunden ein Produkt ganz nach ihren Wünschen konfigurieren können. Diese Anwendung enthält einige wichtige Schritte, die die Benutzer durchführen müssen. Sollen diese Schritte nun als Seitenansichten behandelt werden? Außerdem besteht jeder einzelne Schritt auch noch aus kleineren Aktivitäten („Mikroaktivitäten“). Sollen auch diese Aktivitäten als Seitenaufrufe nachverfolgt werden?

Und was ist, wenn Sie wissen möchten, wie die Abläufe zwischen den einzelnen Aktivitäten aussehen oder auf welche Features die meiste Aktivität entfällt? Das Problem bei RIA besteht darin, dass jede Anwendung einzigartig ist. RIA-Anwendungen werden so gestaltet, dass sie Aktionen aus dem richtigen Leben möglichst real nachstellen. Und da Aktionen immer mit einer Situation im Zusammenhang stehen, gibt es unendlich viele Möglichkeiten. Die meisten Anwendungen bestehen jedoch aus einigen wenigen Hauptkomponenten – den wichtigsten Schritten, Funktionen und Mikroaktionen innerhalb der Funktionen. Während also bei jeder Anwendung überlegt werden muss, was genau gemessen werden soll, gibt es einige allgemein gültige Punkte, die für die Verfolgung von RIAs gelten.
Zu Makroaktivitäten gehört meist das Laden der Anwendung. Dieser Punkt gibt Aufschluss über Besuche, Besucher, Instanzen, Werte für weitere Aktionen usw. Zu Makroaktivitäten können – und sollten – auch die wichtigsten Schritte im Ablauf der RIA-Anwendung gehören. Als Faustregel kann Folgendes gelten: Wenn eine RIA-Aktion die Anwendung um mehr als 50 % verändert (oder wenn sie eine erhebliche Änderung bei dem Benutzererlebnis oder dem Inhalt der Anwendung bewirkt), dann gilt die Aktion als Makroaktivität und sollte als Seitenaufruf verfolgt werden.
Zu Mikroaktivitäten gehören alle Aktionen, bei denen sich die Abläufe in der Anwendung um weniger als 50 % ändern (oder bei denen es nicht zu erheblichen Änderungen bei dem Benutzererlebnis oder dem Inhalt kommt). So wäre zum Beispiel der Wechsel einer ausgewählten Farbe eine Mikroaktivität. Adobe empfiehlt, dass Verfolgungen auf Mikroebene immer mit Funktionen in Zusammenhang gesetzt werden sollten. Wäre es zum Beispiel beim Wechsel einer ausgewählten Farbe von Interesse, welche Farben in Betracht gezogen wurden? Oder reicht es aus zu wissen, dass die Funktion für die Farbauswahl verwendet wurde? Vielleicht sind beide Aspekte wichtig und sollten dann auch beide erfasst werden. Wenn Sie jedoch nachmessen möchten, wie effizient Ihre RIA funktioniert, sollte sich die auf der Funktionsebene stattfindende Aktivität als nützlicher erweisen.

Alle Aktivitäten auf der Mikroebene sollten in Form von benutzerspezifischen Links nachverfolgt werden, wobei die einzelnen Details über zugehörige Traffic-Variablen gemessen werden (Eigenschaftsvariablen und eVars, wenn die Messung anhand von Erfolgsereignissen erfolgen soll). So wird sichergestellt, dass die Zählung der Seitenansichten nicht durch Mikroaktivitäten unnötig in die Höhe getrieben wird. Außerdem ist auf diese Weise eine Pfadanalyse über die Traffic-Variable möglich.

## Was soll analysiert werden? {#section_56824EF675874BA99127A566F6B1383F}

Es ist wichtig, dass Sie wissen, wie effizient der RIA-Aspekt zum Erfolg Ihrer Website beiträgt. Der Erfolg wird für gewöhnlich über Konversionen gemessen. Eine Makroebenenanalyse gibt Einblick in die RIA-Effizienz insgesamt. Eine Mikroebenenanalyse kann Aufschluss darüber geben, welche Funktionen zu mehr Konversionen beigetragen haben.

Die Effizienz Ihrer RIA sollten Sie nachmessen. Für diese Analyse setzen Sie die Mikroaktivitäten mit den RIA-Kennzahlen auf der Makroebene in Relation. Werden Besucher durch mehr Schritte als erforderlich geführt, um an das gleiche Ziel zu gelangen? Solche Analysen können zum Beispiel wie folgt aussehen: Besuche/Funktionsaktivität; Seitenansichten/Funktionsaktivität, Besucher/Funktionsaktivität usw.

Führen Sie eine Analyse der Pfadverläufe und Abgänge durch. Verzichten Benutzer auf die RIA-Funktionalität und suchen einen anderen Weg zum Ziel? Führen Sie Fallout-Berichte für die Website und den RIA-Verlauf aus. Führen Sie Pfadanalysen von Landingpages aus, um die echten Traffic-Muster zu vermessen. Achten Sie auf Hindernisse und Anreize, die Benutzer in Richtung Ziel lenken.

## Vorgeschlagene Kennzahlen {#section_AB7047D6C74740C6B6E47ED93602DB07}

* RIA-Besuche
* RIA-Besucher
* RIA-Seitenansichten
* RIA-Funktionsaktivität (benutzerspezifische Links) zum Messen der Klickaktivität pro Funktion

## Vorgeschlagene Analysen {#section_5BE0FB9ECA3049E5965BEAD733DA5B6E}

* RIA-Funktionsaktivität / RIA-Seitenansichten
* RIA-Funktionsaktivität / RIA-Besuche
* RIA-Seitenansichten / Erfolgsmetrik – Konversionsverhältnis: misst die Anwendungseffizienz
* RIA-Aktivität insgesamt / Erfolgsmetrik – Konversionsverhältnis: misst die Anwendungseffizienz
* RIA-Aktivität pro Funktion / Erfolgsmetrik – Konversionsverhältnis: misst die Effizienz einer Funktion der Anwendung
* Pfadverlauf zu und aus RIA
* Abgänge während des RIA-Konversionsprozesses

