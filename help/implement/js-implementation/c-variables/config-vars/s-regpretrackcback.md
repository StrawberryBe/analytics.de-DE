---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics-Implementierung
seo-description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
solution: null
title: Dynamische Variablen
translation-type: tm+mt
source-git-commit: 60dd1b300035e5149f53870239de85fb3174a77a

---


# s.registerPreTrackCallback und s.registerPostTrackCallback

Diese Funktionen verwenden als Parameter: den Rückruf (eine Funktion) und die Parameter für diese Funktion. Beispiel:

```
s.registerPreTrackCallback(function(requestUrl,a,b,c) { 
    console.log("pre track callback"); 
    console.dir(requestUrl); // Request URL 
    console.dir(a); // param1 
    console.dir(b); // param2 
    console.dir(c); // param3 
}, "param1", "param2", "param3");
```

Der Rückruf wird über die `requestUrl` und sämtliche Parameter aufgerufen, die weitergegeben werden, wenn der Rückruf registriert wird. Das geschieht entweder vor oder nach dem Tracking-Anruf, abhängig davon, welche Methode bei der Registrierung des Rückrufs verwendet wird.

Die Reihenfolge, in der diese Rückrufe aufgerufen werden, steht nicht fest. Rückrufe, die in der Funktion „Pre“ registriert sind, werden aufgerufen, nachdem die finale Tracking-URL erstellt wurde. Die „Post“-Rückrufe werden auf einen erfolgreichen Tracking-Anruf hin aufgerufen (wenn der Tracking-Anruf fehlschlägt, werden diese Funktionen nicht aufgerufen). Mit `registerPreTrackCallback` registrierte Rückrufe beeinträchtigen den Tracking-Anruf nicht. Außerdem wird das Aufrufen jeglicher Tracking-Methoden in jeglichen registrierten Rückrufen nicht empfohlen, da es zu einer Endlosschleife führen könnte.
