---
description: Verarbeitungsregeln werden verwendet, um Werte von Kontextdatenvariablen in props und eVars zu verschieben.
subtopic: Processing rules
title: Kopieren einer Kontextdatenvariable in eine eVar
feature: Admin Tools
uuid: 1beaec4c-71e9-49ce-b154-78408cc532a3
exl-id: f52c2c6c-da3d-43d6-be13-92d0820c93b4
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 100%

---

# Kopieren einer Kontextdatenvariable in eine eVar

Verarbeitungsregeln werden verwendet, um Werte von Kontextdatenvariablen in props und eVars zu verschieben. Ohne Verarbeitungsregeln sind Kontextdatenvariablen bedeutungslos und füllen keine Berichte in Analytics aus.

Die [!UICONTROL Kontextvariablenliste] enthält alle Variablen, die in den letzten 30 Tagen an die Report Suite gesendet wurden. Wenn Sie den Namen der Kontextdatenvariablen kennen, diese aber nicht an die aktuelle Report Suite gesendet haben, können Sie einen Wert hinzufügen, indem Sie den Variablennamen eingeben und auf **[!UICONTROL Kontextdaten für Variablennamen hinzufügen]** klicken:

![Hinzufügen](assets/add-context-variable.png)

Im folgenden Beispiel wird die Kontextdatenvariable `search_term` genommen und ihr Wert in `eVar3` gesetzt:

![Festlegen](assets/set-context-data.png)

Das obige Beispiel funktioniert hervorragend, wenn nur wenige eVars gefüllt werden müssen. Wenn Ihre Organisation über Hunderte von Kontextdatenvariablen verfügt, die jeweils eine eigene eVar benötigen, können Sie bedingte Anweisungen verwenden. Dutzende bedingte Anweisungen können in eine einzige Verarbeitungsregel passen, sodass Ihre Organisation alle eVars in einer Report Suite füllen kann, ohne das Verarbeitungsregellimit von 150 Regeln zu verletzen.

Im folgenden Beispiel wird `prop7` mit der Kontextdatenvariablen `testhierarchy` gefüllt, jedoch nur, wenn `testhierarchy` festgelegt ist:

![Bedingt](assets/add-conditional.png)

Weitere Informationen zur Implementierung von Kontextdatenvariablen finden Sie unter [Kontextdatenvariablen](/help/implement/vars/page-vars/contextdata.md) im Benutzerhandbuch zur Implementierung.
