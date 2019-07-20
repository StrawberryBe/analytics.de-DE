---
description: In den folgenden Abschnitten werden die häufigsten Fehler bei dynamischen Konten beschrieben.
keywords: Analytics-Implementierung
seo-description: In den folgenden Abschnitten werden die häufigsten Fehler bei dynamischen Konten beschrieben.
seo-title: Häufige Fehler
solution: Analytics
subtopic: 'Fehlerbehebung '
title: Häufige Fehler
topic: Entwickler und Implementierung
uuid: 04345355-60 cc -4678-81 c 3-390 c 86752 df 1
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Häufige Fehler

In den folgenden Abschnitten werden die häufigsten Fehler bei dynamischen Konten beschrieben.

## Fest programmiertes Konto {#section_FB6F89BF317F45D387C00986ACA690BC}

Wenn Daten stets an eine bestimmte Report Suite gesendet werden sollen, legen Sie [!UICONTROL s_dynamicAccountSelection] auf „false“ fest (alternativ dazu können die Variablen auch komplett entfernt werden):

```js
var s_account="defaultreportsuiteid" 
REMOVE: s.dynamicAccountSelection=true 
REMOVE: s.dynamicAccountList="devreportsuite1=qa.client.com;reportsuite1=client.com" 
```

Im oben gezeigten Beispiel wird „defaultreportsuiteid“ immer verwendet, nachdem die anderen beiden Zeilen entfernt wurden.

## Codeplatzierung {#section_05375CB2EF5A414794BC8209C906AEEB}

Defining *`s_account`* after the lines of code does not override the dynamic account selection, as shown below.

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

| Host-/Domänenname | – |
|---|---|
| Abfragezeichenfolge | s.dynamicAccountMatch=(window.location.search?window.location.search:"?") |
| Host/Domäne und Pfad | s.dynamicAccountMatch=window.location.host+window.lcation.pathname |
| Pfad und Abfragezeichenfolge | s.dynamicAccountMatch=window.location.pathname+(window.location.search?window.location.search""?") |
| Vollständige URL | s.dynamicAccountMatch=window.location.href |

