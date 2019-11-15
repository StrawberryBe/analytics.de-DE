---
description: Verarbeitungsregeln werden verwendet, um Werte von Kontextdatenvariablen in props und eVars zu verschieben.
solution: Analytics
subtopic: Processing rules
title: Kontextdatenvariable in eine eVar kopieren
topic: Admin tools
uuid: 1beaec4c-71e9-49ce-b154-78408cc532a3
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Kontextdatenvariable in eine eVar kopieren

Verarbeitungsregeln werden verwendet, um Werte von Kontextdatenvariablen in Props und eVars zu verschieben. Ohne Verarbeitungsregeln sind Kontextdatenvariablen bedeutungslos und füllen keine Berichte in Analytics aus.

Die [!UICONTROL Kontextvariablenliste] enthält alle Variablen, die in den vorherigen 30 Tagen an die Report Suite gesendet wurden. If you know the context data variable name but have not sent it into the current report suite, you can add a value by typing the variable name and clicking **[!UICONTROL Add variable name context data]**:

![Fügen Sie](assets/add-context-variable.png)

Im folgenden Beispiel wird die `search_term` Kontextdatenvariable verwendet und ihr Wert in `eVar3`:

![Legen Sie](assets/set-context-data.png)

Das obige Beispiel funktioniert hervorragend, wenn nur wenige eVars gefüllt werden müssen. Wenn Ihr Unternehmen über Hunderte von Kontextdatenvariablen verfügt, die jeweils eine eigene eVar benötigen, können Sie bedingte Anweisungen verwenden. Dutzende bedingte Anweisungen können in eine einzige Verarbeitungsregel passen, sodass Ihr Unternehmen alle eVars in einer Report Suite füllen kann, ohne die Verarbeitungsregel von 150 Regeln einzuhalten.

Das folgende Beispiel wird `prop7` mit der Kontextdatenvariablen gefüllt `testhierarchy`, jedoch nur, wenn `testhierarchy` festgelegt:

![Bedingt](assets/add-conditional.png)

Weitere Informationen zur Implementierung von Kontextdatenvariablen finden Sie unter [Kontextdatenvariablen](/help/implement/js-implementation/c-variables/context-data-variables.md) im Implementierungs-Benutzerhandbuch.
