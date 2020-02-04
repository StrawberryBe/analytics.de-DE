---
title: Fehlerbehebung bei der JavaScript-Implementierung
description: Erfahren Sie mehr über häufige Probleme und Best Practices zur Fehlerbehebung bei Ihrer JavaScript-Implementierung.
translation-type: tm+mt
source-git-commit: 8aa6932dcbb6dad88c27ba1cd4f5aad3bafcfc52

---


# Fehlerbehebung bei der JavaScript-Implementierung

Im Folgenden werden einige Gründe erläutert, aus denen Ihr Unternehmen Probleme mit dem korrekten Eingang von Daten in Adobe Analytics haben könnte.

## Verwenden von Anführungszeichen

Die meisten Variablen, die an Adobe gesendet werden, sind Zeichenfolgen. In JavaScript können Sie einfache oder doppelte Anführungszeichen verwenden.

### Kombinieren von Anführungszeichen zur Definition einer Variablen

Als Best Practice sollten Sie sicherstellen, dass Sie mit den von Ihnen verwendeten Anführungszeichenarten konsistent sind. Wenn ein einzelnes Anführungszeichen den Anfang einer Zeichenfolge angibt, muss ein einfaches Anführungszeichen zum Schließen verwendet werden.

Beispielsweise sind beide `s.eVar1 = 'Value'` und `s.eVar1 = "Value"` beide gültig. `s.eVar1 = 'Value"` ist nicht gültig.

### Einfache oder doppelte Anführungszeichen in eine Zeichenfolge einschließen

Manchmal ist es wünschenswert, ein einfaches oder doppeltes Anführungszeichen in eine Zeichenfolge einzufügen. Sie möchten beispielsweise den Wert `Alex's sale` oder `John the "Hunter"` in Berichte aufnehmen. Es gibt zwei Methoden, um diese Werte einzubeziehen:

* **Verwenden Sie den anderen Anführungszeichentyp**:Zum Beispiel `s.eVar1 = "Alex's sale"` und `s.eVar1 = 'John the "Hunter"'` sind beide gültig.
* **Escape-Anführungszeichen**: Verwenden Sie einen umgekehrten Schrägstrich, um Anführungszeichen zu vermeiden. Zum Beispiel `s.eVar1 = 'Alex\'s sale'` und `s.eVar1 = "John the \"Hunter\""` sind beide gültig.

### Vermeiden Sie die Verwendung von geschweiften Anführungszeichen

Einige Programme konvertieren neutrale Anführungszeichen (`"..."` und `'...'`) automatisch in geschweifte Anführungszeichen (`“...”` und `‘...’`). Vermeiden Sie den Einsatz von Dokumenteditoren (z. B. Microsoft Word) oder das Senden von Codefragmenten per E-Mail. Kurze Anführungszeichen können in JavaScript nicht verwendet werden.

## Referenzieren des Analytics-Objekts

Alle an Adobe gesendeten Variablen verwenden das Analytics-Objekt. Die meisten Implementierungen verwenden das `s` Objekt. Achten Sie darauf, dass Sie beim Referenzieren von Variablen das Analytics-Objekt in Ihre Referenz aufnehmen.

Beispiel: `s.eVar1 = 'Value'` ist gültig, `eVar1 = 'Value'` nicht jedoch.

## Jede Variable einmal definieren

Wenn eine Verfolgungsfunktion (`s.t()`) ausgeführt wird, nimmt AppMeasurement alle definierten Variablen und kompiliert sie in einer Bildanforderung. Wenn Sie eine Variable in Ihrer Implementierung mehrmals definieren, wird nur der neueste Wert verwendet. Stellen Sie sicher, dass alle Variablenwerte den richtigen Wert enthalten, wenn die track-Funktion ausgeführt wird.

## Variablengroßschreibung korrigieren

Einige Variablen verwenden Großbuchstaben. Bei JavaScript-Variablen wird die Groß-/Kleinschreibung beachtet. Achten Sie beim Definieren von Variablen auf die richtige Groß-/Kleinschreibung. Beispiel: `s.eVar1 = 'Value'` ist gültig, `s.evar1 = 'Value'` nicht jedoch.

## Plug-ins

Einige Unternehmen verwenden Plug-ins, um ihre Implementierung von Adobe Analytics zu verbessern. Vergessen Sie beim Aktualisieren von AppMeasurement-Versionen nicht, installierte Plug-Ins erneut einzuschließen. Der im [!UICONTROL Code-Manager] erstellte Code enthält keinen Plug-in-Code. Erstellen Sie eine Kopie Ihres vorhandenen Codes, falls Sie zu einer früheren Version von AppMeasurement zurückkehren müssen.

## Leerraum in Variablenwerten

In HTML gibt es mehrere Zeichen, die zu einem Leerzeichen führen. Dazu gehören Leerzeichen, Tabulatoren und Wagenrücklauf (oder Zeilenvorschub). Siehe folgendes Beispiel:

```html
<head>
  <title>
    Home Page
  </title>
</head>
<body>
<script language="javascript">
  s.pageName = document.title;
</script>
</body>
```

In this case, `document.title` populates `s.pageName`, which receives a value of &quot;Home Page&quot;. In einigen Browsern kann der Leerraum jedoch anders interpretiert werden. Das Ergebnis kann eines der folgenden Beispiele sein:

```js
s.pageName = "Home Page";
```

```js
s.pageName = "        Home Page";
```

Diese beiden Variablenwerte werden in Adobe Analytics als gesondert betrachtet. Der Leerraum wird jedoch automatisch für Anzeigezwecke entfernt. Das Ergebnis ist ein Bericht, der zwei scheinbar identische &quot;Homepage&quot;-Zeilenelemente anzeigt. Achten Sie darauf, dass Variablenwerte vor oder nach dem gewünschten Wert keine Leerzeichen enthalten.
