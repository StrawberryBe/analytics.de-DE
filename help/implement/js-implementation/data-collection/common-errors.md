---
description: In den folgenden Abschnitten werden die häufigsten Fehler bei dynamischen Konten beschrieben.
keywords: Analytics Implementation
subtopic: Troubleshooting
title: Häufige Fehler
topic: Developer and implementation
uuid: 04345355-60cc-4678-81c3-390c86752df1
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Häufige Fehler

In den folgenden Abschnitten werden die häufigsten Fehler bei dynamischen Konten beschrieben.

## Hartcodiertes Konto {#section_FB6F89BF317F45D387C00986ACA690BC}

Wenn Daten stets an eine bestimmte Report Suite gesendet werden sollen, legen Sie [!UICONTROL s_dynamicAccountSelection] auf „false“ fest (alternativ dazu können die Variablen auch komplett entfernt werden):

```js
var s_account="defaultreportsuiteid" 
REMOVE: s.dynamicAccountSelection=true 
REMOVE: s.dynamicAccountList="devreportsuite1=qa.client.com;reportsuite1=client.com" 
```

Im oben gezeigten Beispiel wird „defaultreportsuiteid“ immer verwendet, nachdem die anderen beiden Zeilen entfernt wurden.

## Codeplatzierung {#section_05375CB2EF5A414794BC8209C906AEEB}

Beim Definieren von *`s_account`* hinter den Codezeilen wird die dynamische Kontoauswahl nicht überschrieben.

```js
var s_account="defaultreportsuiteid" 
s.dynamicAccountSelection=true 
s.dynamicAccountList="devreportsuite1=qa.client.com;reportsuite1=client.com" 
s_account="anotherreportsuiteid" 
```

In dem Beispiel oben überschreibt das Konto „anotherreportsuiteid“ zwar das Konto „defaultreportsuiteid“, nicht jedoch etwaige Übereinstimmungen, die in [!UICONTROL s.dynamicAccountList] vorkommen. Die Funktion, die [!UICONTROL s.dynamicAccountList] auswertet, wird tatsächlich erst viel später in der JS-Datei ausgeführt.

## Multi-Suite-Tagging {#section_6C014FA9B87D4622B483BCDE4281D2A9}

Wie unten gezeigt, kann in Verbindung mit dynamischer Kontoauswahl auch Multi-Suite-Tagging eingesetzt werden.

```js
s.dynamicAccountSelection=true 
s.dynamicAccountList="suiteid1,suiteid2=client.com" 
```

## Dynamischer Kontovergleich {#section_647AB47B38D640D6BCC853FDA4E4342D}

Setzen Sie die [!UICONTROL dynamicAccountMatch]-Variablen nicht in Anführungszeichen. Die verfügbaren Optionen sind nachfolgend aufgeführt.

| Host-/Domänenname | Keine |
|---|---|
| Abfragezeichenfolge | s.dynamicAccountMatch=(window.location.search?window.location.search:"?") |
| Host/Domäne und Pfad | s.dynamicAccountMatch=window.location.host+window.lcation.pathname |
| Pfad und Abfragezeichenfolge | s.dynamicAccountMatch=window.location.pathname+(window.location.search?window.location.search""?") |
| Vollständige URL | s.dynamicAccountMatch=window.location.href |

