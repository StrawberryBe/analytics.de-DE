---
title: Fehlerbehebung bei der JavaScript-Implementierung
description: Informieren Sie sich über häufige Probleme und Best Practices zur Fehlerbehebung bei der Implementierung von JavaScript.
translation-type: ht
source-git-commit: 8aa6932dcbb6dad88c27ba1cd4f5aad3bafcfc52

---


# Fehlerbehebung bei der JavaScript-Implementierung

Im Folgenden werden einige Gründe erläutert, aus denen Ihr Unternehmen Probleme haben könnte, Daten korrekt in Adobe Analytics einzugeben.

## Verwenden von Anführungszeichen

Die meisten Variablen, die an Adobe gesendet werden, sind Zeichenfolgen. In JavaScript können Sie einfache oder doppelte Anführungszeichen verwenden.

### Mischen von Anführungszeichen bei der Definition einer Variablen

Als Best Practice sollten Sie sicherstellen, dass Sie mit den von Ihnen verwendeten Anführungszeichenarten konsistent sind. Wenn ein einzelnes Anführungszeichen den Anfang einer Zeichenfolge angibt, muss ein einfaches Anführungszeichen zum Schließen verwendet werden.

Zum Beispiel sind `s.eVar1 = 'Value'` und `s.eVar1 = "Value"` beide gültig. `s.eVar1 = 'Value"` ist nicht gültig.

### Einschließen von einfachen oder doppelten Anführungszeichen in eine Zeichenfolge

Manchmal ist es wünschenswert, ein einfaches oder doppeltes Anführungszeichen in eine Zeichenfolge einzufügen. Sie möchten beispielsweise den Wert `Alex's sale` oder `John the "Hunter"` in Berichte aufnehmen. Es gibt zwei Methoden, um diese Werte einzubeziehen:

* **Anderen Anführungszeichentyp verwenden**: Beispielsweise sind `s.eVar1 = "Alex's sale"` und `s.eVar1 = 'John the "Hunter"'` beide gültig.
* **Anführungszeichen maskieren**: Verwenden Sie einen umgekehrten Schrägstrich, um Anführungszeichen zu maskieren. Zum Beispiel sind `s.eVar1 = 'Alex\'s sale'` und `s.eVar1 = "John the \"Hunter\""` beide gültig.

### Typografische Anführungszeichen vermeiden

Einige Programme konvertieren neutrale Anführungszeichen (`"..."` und `'...'`) automatisch in typographische Anführungszeichen (`“...”` und `‘...’`). Vermeiden Sie den Einsatz von Dokumenteditoren (z. B. Microsoft Word) oder das Senden von Codefragmenten per E-Mail. Typographische Anführungszeichen können in JavaScript nicht verwendet werden.

## Analytics-Objekts referenzieren

Alle an Adobe gesendeten Variablen verwenden das Analytics-Objekt. Die meisten Implementierungen verwenden das `s`-Objekt. Achten Sie darauf, dass Sie beim Referenzieren von Variablen das Analytics-Objekt in Ihre Referenz aufnehmen.

Zum Beispiel ist `s.eVar1 = 'Value'` gültig, während `eVar1 = 'Value'` nicht gültig ist.

## Jede Variable einmal definieren

Wenn eine Tracking-Funktion (`s.t()`) ausgeführt wird, nimmt AppMeasurement alle definierten Variablen und kompiliert sie in eine Bildanforderung. Wenn Sie eine Variable in Ihrer Implementierung mehrmals definieren, wird nur der neueste Wert verwendet. Stellen Sie sicher, dass alle Variablenwerte den richtigen Wert enthalten, wenn die Tracking-Funktion ausgeführt wird.

## Korrekte Groß- und Kleinschreibung von Variablen

Einige Variablen verwenden Großbuchstaben. Bei JavaScript-Variablen wird zwischen Groß- und Kleinschreibung unterschieden. Achten Sie beim Definieren von Variablen auf die korrekte Groß-/Kleinschreibung. Zum Beispiel ist `s.eVar1 = 'Value'` gültig, während `s.evar1 = 'Value'` nicht gültig ist.

## Plug-ins

Einige Unternehmen verwenden Plug-ins, um ihre Implementierung von Adobe Analytics zu verbessern. Vergessen Sie beim Aktualisieren von AppMeasurement-Versionen nicht, installierte Plug-ins erneut einzuschließen. Der im [!UICONTROL Code-Manager] erstellte Code enthält keinen Plug-in-Code. Erstellen Sie eine Kopie Ihres vorhandenen Codes, falls Sie zu einer früheren Version von AppMeasurement zurückkehren müssen.

## Leerzeichen in Variablenwerten

In HTML gibt es mehrere Zeichen, die zu einem Leerzeichen führen. Dazu gehören Leerzeichen, Tabulatoren und Zeilenumschalter (oder Zeilenvorschub). Siehe folgendes Beispiel:

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

In diesem Fall füllt `document.title` die Variable `s.pageName`, die den Wert „Home Page“ erhalten würde. In einigen Browsern kann das Leerzeichen jedoch anders interpretiert werden. Das Ergebnis kann eines der folgenden Beispiele sein:

```js
s.pageName = "Home Page";
```

```js
s.pageName = "        Home Page";
```

Diese beiden Variablenwerte werden in Adobe Analytics getrennt betrachtet. Das Leerzeichen wird jedoch automatisch für Anzeigezwecke entfernt. Das Ergebnis ist ein Bericht, der zwei scheinbar identische Zeileneinträge „Home Page“ anzeigt. Achten Sie darauf, dass Variablenwerte vor oder nach dem gewünschten Wert keine Leerzeichen enthalten.
