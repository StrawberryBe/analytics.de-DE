---
title: s_objectID
description: Hilft Activity Map, eindeutige Links auf Ihrer Website zu identifizieren.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 100%

---


# s_objectID

Die `s_objectID`-Variable stellt eine eindeutige Kennung für einen Link bereit. Damit werden Berichte in [Activity Map](/help/analyze/activity-map/activity-map.md) genauer. Wenn Sie Links auf einer Seite haben, die sich häufig ändern, können Sie die `s_objectID`-Variable verwenden, um Activity Map die Position eines eindeutigen Links anzuzeigen, damit die Daten nach Wunsch korrekt gruppiert werden können.

Wenn die Genauigkeit von Activity Map für Ihr Unternehmen von entscheidender Bedeutung ist, empfiehlt Adobe, die `s_objectID`-Variable in das `onClick`-Ereignis von Links auf Ihrer Website aufzunehmen. Weitere Informationen finden Sie unter [Anwendungsbeispiele für Activity Map-Linktracking](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-use-case.md) im Analysebenutzerhandbuch.

## Objekt-ID in Adobe Experience Platform Launch

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den Editor für benutzerdefinierten Code entsprechend der AppMeasurement-Syntax.

## s_objectID in AppMeasurement und im benutzerdefinierten Code-Editor in Launch

Die `s_objectID`-Variable ist eine globale Variable, d. h. sie funktioniert unabhängig vom Analytics-Tracking-Objekt (standardmäßig `s`). Beliebige Zeichenfolgen mit einer Länge von bis zu 100 Byte können gültige Werte für diese Variable sein. Wenn diese Variable nicht definiert ist, verwendet Activity Map die Link-URL als Kennung für den Link.

Diese Variable wird normalerweise im `onClick`-Ereignis eines HTML-Links gesetzt.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

>[!NOTE]
>
>Fügen Sie immer das Semikolon ein, das eine JavaScript-Anweisung abschließt. Das Semikolon ist erforderlich, damit Activity Map funktioniert.

## Anwendungsbeispiele

Die `s_objectID`-Variable ist immer dann nützlich, wenn Sie eine höhere Genauigkeit in Activity Map-Berichten wünschen.

### Aggregieren von Links aus hochdynamischen Inhalten

Einige Websites verfügen über hochdynamische Inhalte, z. B. Nachrichten- oder Retail-Websites mit häufig wechselnden Artikeln. Da Activity Map standardmäßig die Link-URL als Kennung verwendet, ist es schwierig, die am häufigsten geklickten Bereiche auf Seiten zu verstehen, deren Links sich häufig ändern. Wenn Sie die `s_objectID` innerhalb dieser Links verwenden, versteht Activity Map, welche Links aggregiert werden können, unabhängig von den URLs, auf die sie verweisen.

```HTML
<a href="story1.html" onClick="s_objectID='Top left link';">Story 1</a>
<a href="story2.html" onClick="s_objectID='Top center link';">Story 2</a>
<a href="story3.html" onClick="s_objectID='Top right link';">Story 3</a>
```

Unabhängig davon, wohin die Links zeigen oder wie oft Sie diese Links ändern, aggregiert Activity Map die Daten auf der Grundlage des Wertes in `s_objectID`.

### Links auf einer Seite getrennt halten

Einige Websites verfügen über Links, die an verschiedenen Stellen auf dieselbe Stelle verweisen. Beispiel: Ein Link zur Homepage in der Kopf- und Fußzeile Ihrer Website. Da diese Links dieselbe URL haben, aggregiert Activity Map ihre Daten. Sie können sie mithilfe der `s_objectID`-Variablen trennen:

```HTML
<a href="index.html" onClick="s_objectID='Header home link';">Example link in Header</a>
<a href="index.html" onClick="s_objectID='Footer home link';">Example link in Footer</a>
```

Auch wenn Links auf dieselbe URL verweisen, kann Activity Map die `s_objectID`-Variable verwenden, um sie bei der Berichterstellung korrekt zu unterscheiden.
