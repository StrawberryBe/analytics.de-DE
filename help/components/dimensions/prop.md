---
title: Prop
description: Eine benutzerdefinierte Dimension, die Sie in Berichte verwenden können.
translation-type: ht
source-git-commit: 7c722e361978a3d7517e95c23442b703e7e25270
workflow-type: ht
source-wordcount: '467'
ht-degree: 100%

---


# Prop

*Auf dieser Hilfeseite wird beschrieben, wie Props als Dimension funktionieren. Weitere Informationen zur Implementierung von Props finden Sie unter[Props](/help/implement/vars/page-vars/prop.md)im Benutzerhandbuch zu Implementierungen.*

Props sind benutzerdefinierte Variablen, die Sie beliebig verwenden können. Sie bleiben nicht über den von ihnen festgelegten Treffer hinaus bestehen.

>[!TIP]
>
>Adobe empfiehlt in den meisten Fällen die Verwendung von [eVars](evar.md). In früheren Versionen von Adobe Analytics hatten Props und eVars Vorteile und Nachteile. Adobe hat eVars jedoch dahingehend verbessert, dass sie fast alle Anwendungsfälle für Props erfüllen.

Wenn Sie über ein [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) verfügen, können Sie diese benutzerspezifischen Dimensionen den unternehmensspezifischen Werten zuordnen. Die Anzahl der verfügbaren Props hängt von Ihrem Vertrag mit Adobe ab. Es sind bis zu 75 Props verfügbar, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Füllen von Props mit Daten

Jede Prop erfasst Daten aus der [`c1` – `c75`-Abfragezeichenfolge](/help/implement/validate/query-parameters.md) in den Bildanforderungen. Beispielsweise erfasst der Abfragezeichenfolgenparameter `c1` Daten für prop1, während der Abfragezeichenfolgenparameter `c68` Daten für prop68 erfasst.

AppMeasurement, das JavaScript-Variablen in eine Bildanforderung für die Datenerfassung kompiliert, verwendet die Variablen `prop1` – `prop75`. Die Implementierungsrichtlinien finden Sie unter [Prop](/help/implement/vars/page-vars/prop.md) im Benutzerhandbuch zu Implementierungen.

## Dimensionselemente

Da Props benutzerdefinierte Zeichenfolgen in Ihrer Implementierung enthalten, bestimmt Ihr Unternehmen, welche Dimensionselemente für jede Prop gelten. Vergewissern Sie sich, dass Sie den Zweck jeder Prop und die typischen Dimensionselemente in einem [Lösungs-Design-Dokument](/help/implement/prepare/solution-design.md) aufzeichnen.

## Groß-/Kleinschreibung

Bei Props wird standardmäßig nicht zwischen Groß- und Kleinschreibung unterschieden. Wenn Sie denselben Wert mit verschiedenen Groß- und Kleinschreibungen senden (z. B. `"DOG"` und `"Dog"`), gruppiert Analysis Workspace ihn in demselben Dimensionselement. Es wird die erste Groß- und Kleinschreibung verwendet, die zu Beginn des Berichtsmonats vorkam. Data Warehouse zeigt den ersten aufgefundenen Wert innerhalb des Anforderungszeitraums an.

Sie können bei allen Props die Groß-/Kleinschreibung beachten. Sie können auch die Groß-/Kleinschreibung für jede Prop deaktivieren, sobald sie aktiviert ist. Wenden Sie sich an die Adobe-Kundenunterstützung mit der Report Suite-ID und den gewünschten Variablen, um die Groß-/Kleinschreibung zu ändern.

>[!IMPORTANT]
>
>Beim Umschalten der Groß-/Kleinschreibung können Dimensionselemente abgeschnitten werden, unerwartete Ergebnisse bei Segmenten hervorgerufen werden und Probleme mit Filtern auftreten. Adobe empfiehlt dringend, diese Einstellung zwischen zwei Hauptzeiträumen umzuschalten, z. B. am Anfang eines Monats oder Jahres.

## Wert von Props gegenüber eVars

Adobe empfiehlt in den meisten Fällen die Verwendung von eVars. Ausnahmen von dieser Aussage sind:

* Sie können Props in Echtzeitberichten verwenden. Bei eVars dauert es mindestens 30 Minuten, bis die Daten im Reporting angezeigt werden.
* Props können zu Listen-Props werden, die mehrere Werte im selben Treffer akzeptieren. Listenvariablen sind eine separate Variable, und es sind nur drei Listenvariablen verfügbar.
* Wenn Sie Pfade für eine Prop aktivieren, stehen die Dimensionen [Einstieg](entry-dimensions.md) und [Ausstieg](exit-dimensions.md) sofort zur Verfügung. Wenn Sie Eingangs- und Ausgangsdimensionen für eVars wünschen, können Sie manuell ein Segment erstellen.

Weitere Vergleiche zwischen Props und eVars finden Sie unter [eVar](evar.md).
