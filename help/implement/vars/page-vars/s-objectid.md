---
title: s_objectID
description: Help Activity Map identifiziert eindeutige Links auf Ihrer Site.
translation-type: tm+mt
source-git-commit: c7d596be4f70c820039725be6a5fddc8572156d9

---


# s_objectID

Die `s_objectID` Variable stellt einen eindeutigen Bezeichner für einen Link bereit. Damit werden Berichte in [Activity Map](/help/analyze/activity-map/activity-map.md) genauer. Wenn Sie Links auf einer Seite haben, die sich häufig ändern, können Sie die `s_objectID` Variable verwenden, um Activity Map die Position eines eindeutigen Links anzuzeigen, damit die Daten nach Wunsch korrekt gruppiert werden können.

Wenn die Genauigkeit von Activity Map für Ihr Unternehmen von entscheidender Bedeutung ist, empfiehlt Adobe, die `s_objectID` Variable in den `onClick` Fall von Links auf Ihrer Site aufzunehmen. Weitere Informationen finden Sie unter [Activity Map-Linktracking-Anwendungsfälle](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-use-case.md) im Benutzerhandbuch Analyze.

## Objekt-ID beim Start der Adobe Experience Platform

Es gibt kein spezielles Feld in Launch, um diese Variable zu verwenden. Verwenden Sie den benutzerdefinierten Code-Editor entsprechend der AppMeasurement-Syntax.

## s_objectID in AppMeasurement und Starten des benutzerdefinierten Code-Editors

Die `s_objectID` Variable ist eine globale Variable, d. h. sie funktioniert unabhängig vom Analytics-Verfolgungsobjekt (`s` standardmäßig). Gültige Werte für diese Variable können beliebige Zeichenfolgen mit einer Länge von bis zu 100 Byte sein. Wenn diese Variable nicht definiert ist, verwendet Activity Map die Link-URL als Bezeichner für den Link.

Diese Variable wird normalerweise bei `onClick` einem HTML-Link eingestellt.

```HTML
<a href="https://example.com" onClick="s_objectID='Example identifier';">Example link</a>
```

> [!NOTE] Schließen Sie immer das Semikolon ein, das eine JavaScript-Anweisung beendet. Das Semikolon ist erforderlich, damit Activity Map funktioniert.

## Anwendungsbeispiele

Die `s_objectID` Variable ist immer dann nützlich, wenn Sie eine höhere Genauigkeit in Activity Map-Berichten wünschen.

### Aggregieren von Links aus hochdynamischen Inhalten

Einige Sites verfügen über hochdynamische Inhalte, z. B. Nachrichten- oder Einzelhandels-Sites mit häufig wechselnden Artikeln. Da Activity Map die Link-URL standardmäßig als Bezeichner verwendet, ist es schwierig, die Bereiche zu verstehen, in denen Links sich am häufigsten ändern. Wenn Sie die `s_objectID` innerhalb dieser Links verwenden, versteht Activity Map, welche Links unabhängig von den URLs, auf die sie verweisen, aggregiert werden können.

```HTML
<a href="story1.html" onClick="s_objectID='Top left link';">Story 1</a>
<a href="story2.html" onClick="s_objectID='Top center link';">Story 2</a>
<a href="story3.html" onClick="s_objectID='Top right link';">Story 3</a>
```

Unabhängig davon, wo die Links zeigen oder wie oft Sie diese Links ändern, aggregiert Activity Map Daten basierend auf dem Wert in `s_objectID`.

### Links auf einer Seite getrennt halten

Einige Sites verfügen über Links, die an verschiedenen Orten auf denselben Ort verweisen. Beispiel: Ein Link zur Homepage in der Kopf- und Fußzeile Ihrer Site. Da diese Links dieselbe URL haben, aggregiert Activity Map ihre Daten. Sie können sie mithilfe der `s_objectID` Variablen trennen:

```HTML
<a href="index.html" onClick="s_objectID='Header home link';">Example link in Header</a>
<a href="index.html" onClick="s_objectID='Footer home link';">Example link in Footer</a>
```

Auch wenn Links auf dieselbe URL verweisen, kann Activity Map die `s_objectID` Variable verwenden, um sie bei der Berichterstellung korrekt zu unterscheiden.
