---
title: Eigenschaft
description: Eine benutzerdefinierte Dimension, die Sie in Berichte verwenden können.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 26%

---


# Eigenschaft

*Auf dieser Hilfeseite wird beschrieben, wie Props als Dimension funktionieren. For information on how to implement props, see[props](/help/implement/vars/page-vars/prop.md)in the Implement user guide.*

Props sind benutzerspezifische Variablen, die Sie beliebig verwenden können. Sie bleiben nicht über den Treffer hinaus erhalten, den sie ausgelöst haben.

>[!TIP]
>
>Adobe recommends using [eVars](evar.md) in most cases. In früheren Versionen von Adobe Analytics hatten Props und eVars Vorteile und Nachteile. Adobe hat eVars jedoch dahingehend verbessert, dass sie fast alle Anwendungsfälle für Props erfüllen.

Wenn Sie über ein [Lösungsdesign-Dokument](/help/implement/prepare/solution-design.md)verfügen, können Sie diese benutzerspezifischen Dimensionen den unternehmensspezifischen Werten zuordnen. Die Anzahl der verfügbaren Props hängt von Ihrem Vertrag mit Adobe ab. Es stehen bis zu 75 Props zur Verfügung, wenn Ihr Vertrag mit Adobe dies unterstützt.

## Eigenschaftsvariablen mit Daten füllen

Jede Eigenschaftsvariable sammelt Daten aus der [`c1` - `c75` Abfrage-Zeichenfolge](/help/implement/validate/query-parameters.md) in Bildanforderungen. Beispielsweise erfasst der Parameter `c1` Abfrage String Daten für prop1, während der Parameter `c68` Abfrage String Daten für prop68 erfasst.

AppMeasurement, das JavaScript-Variablen in eine Bildanforderung für die Datenerfassung kompiliert, verwendet die Variablen `prop1` - `prop75`. Implementierungsrichtlinien finden Sie unter [Eigenschaftsvariablen](/help/implement/vars/page-vars/prop.md) im Implementierungs-Benutzerhandbuch.

## Dimensionswerte

Da Eigenschaftsvariablen benutzerdefinierte Zeichenfolgen in Ihrer Implementierung enthalten, bestimmt Ihr Unternehmen, welche Dimensionswerte für jede Eigenschaftsvariable gelten. Vergewissern Sie sich, dass Sie den Zweck der einzelnen Eigenschaftsvariablen und die typischen Dimensionswerte in einem [Lösungsdesign-Dokument](/help/implement/prepare/solution-design.md)aufzeichnen.

## Wert von Props über eVars

Adobe empfiehlt in den meisten Fällen die Verwendung von eVars. Ausnahmen von dieser Aussage sind:

* Sie können Eigenschaftsvariablen in Echtzeitberichten verwenden. Die Anzeige von eVars im Berichte dauert mindestens 30 Minuten.
* Props können zu Listen-Props werden, die mehrere Werte im selben Treffer akzeptieren. Listenvariablen sind eine separate Variable, und es sind nur drei Listenvariablen verfügbar.
* Wenn Sie Pfade für eine Eigenschaftsvariable aktivieren, stehen [die Dimensionen &quot;Einstieg](entry-dimensions.md) &quot;und &quot; [Ausstieg](exit-dimensions.md) &quot;sofort zur Verfügung. Wenn Sie die Ein- und Ausstiegsdimensionen für eVars festlegen möchten, können Sie ein Segment manuell erstellen.

Weitere Vergleiche zwischen Props und eVars finden Sie unter [eVar](evar.md) .
