---
description: Mit dem Plug-in „getValOnce“ wird verhindert, dass eine bestimmte Variable auf den zuvor definierten Wert gesetzt wird. Es verwendet ein Cookie, um den für eine Variable zuletzt verwendeten Wert zu ermitteln. Falls der aktuelle Wert dem Cookiewert entspricht, wird die Variable mit einer leeren Zeichenfolge überschrieben, bevor er an die Verarbeitungsserver von Adobe abgesendet wird. Dieses Plug-in ist nützlich, um ein Aufblasen von Variableninstanzen für Konversionen zu vermeiden, die beim Aktualisieren der Seite oder dem Klicken auf die Schaltfläche „Zurück“ durch den Benutzer generiert werden.
keywords: Analytics Implementation
subtopic: Plug-ins
title: getValOnce
topic: Developer and implementation
uuid: 82fe0da5-3bc4-4632-8c62-7b5683f6b587
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# getValOnce

Mit dem Plug-in „getValOnce“ wird verhindert, dass eine bestimmte Variable auf den zuvor definierten Wert gesetzt wird. Es verwendet ein Cookie, um den für eine Variable zuletzt verwendeten Wert zu ermitteln. Falls der aktuelle Wert dem Cookiewert entspricht, wird die Variable mit einer leeren Zeichenfolge überschrieben, bevor er an die Verarbeitungsserver von Adobe abgesendet wird. Dieses Plug-in ist nützlich, um ein Aufblasen von Variableninstanzen für Konversionen zu vermeiden, die beim Aktualisieren der Seite oder dem Klicken auf die Schaltfläche „Zurück“ durch den Benutzer generiert werden.

>[!IMPORTANT]
>
>Dieses Plug-in wurde nicht auf Kompatibilität mit [AppMeasurement für JavaScript](/help/implement/js-implementation/c-appmeasurement-js/appmeasure-mjs.md) überprüft. Siehe [AppMeasurement-Plug-in-Unterstützung](/help/implement/js-implementation/c-appmeasurement-js/plugins-support.md).

**Parameter**

```js
s.eVar1=s.getValOnce(variable,cookie,expiration,minute);
```

* **Variable:** Die zu prüfende Variable. Dabei handelt es sich in der Regel um die gleiche Variable, die gerade definiert wird.
* **Cookie:** Der Name des Cookies, das den zu vergleichenden vorherigen Wert speichert. Das Cookie kann einen beliebigen Wert aufweisen.
* (Optional) **Ablauf:** Anzahl der Tage, nach denen das Cookie abläuft. Wenn keine Angabe gemacht wird oder der Wert auf 0 (null) gesetzt wird, ist die vorgegebene Ablaufzeit die Browsersitzung.
* (Optional) **Minute:** Wenn Sie hierfür den Zeichenfolgenwert *`m`* festlegen, wird der Ablaufwert in Minuten statt in Tagen angegeben. Wenn nicht festgelegt, ist *`days`* ist die standardmäßige Gültigkeit.

**Eigenschaften**

* Dieses Plug-in wird in der Regel für Konversionsvariablen verwendet. Es kann jedoch für beliebige [!DNL Analytics]-Variablen verwendet werden.
* Wenn JavaScript auf diese Funktion trifft, wird der definierte Wert mit dem im Cookie gespeicherten Wert verglichen. Wenn sich der definierte Wert vom Wert des Cookies unterscheidet, wird der definierte Wert festgelegt. Wenn der definierte Wert mit dem Wert des Cookies identisch ist, wird eine leere Zeichenfolge zurückgegeben.
* Das Cookie kann nur einen einzelnen Wert speichern, was bedeutet, dass das Plug-in nur den zuletzt definierten Wert in Betracht zieht.
* Das Plug-in verhindert nicht, dass alle Werte die Variable definieren, nachdem sie definiert wurde. Das Plug-in verhindert nur, dass der letzte Wert mehrmals hintereinander gesetzt wird.
* Wenn der Endbenutzer Cookies blockiert oder abweist, wird immer der ursprüngliche Wert zurückgegeben.
* Das Plug-in versteht unter einer Sitzung etwas anders, als in [!DNL Analytics] unter einer Sitzung (oder einem Besuch) verstanden wird. [!DNL Analytics] beendet eine Sitzung nach 12 Stunden Aktivität oder nach 30 Minuten Inaktivität. Da das Plug-in die Sitzungsdefinition des Browsers verwendet, wird es erst dann beendet, nachdem der Benutzer die Registerkarte geschlossen hat oder den Browser beendet.

   * Wenn ein Benutzer Ihre Seite schließt, eine andere Registerkarte öffnet und innerhalb von 30 Minuten zu Ihrer Site zurückkehrt, erstellt das Plug-in eine neue Sitzung, während der [!DNL Analytics]-Besuch geöffnet bleibt.
   * Wenn ein Benutzer das Browser-Fenster geöffnet lässt, ohne innerhalb der nächsten 30 Minuten auf einen Link zu klicken, läuft der [!DNL Analytics]-Besuch ab, während die Browsersitzung geöffnet bleibt.

> [!NOTE] Für die folgenden Anweisungen müssen Sie den Datenerfassungscode auf Ihrer Site ändern. Dies kann sich auf die Datenerfassung auf Ihrer Site auswirken und sollte daher nur von einem Entwickler durchgeführt werden, der über Erfahrung in der Verwendung und Implementierung von [!DNL Analytics] verfügt.

## Implementierung {#section_177FF7F425B64FFB83CDE15A6ACC8D21}

> [!NOTE] Falls Ihre Organisation Marketing-Kanäle verwendet und Regeln basierend auf `s.campaign` eingerichtet sind, wird empfohlen, das Plug-in „getValOnce“ nicht zu verwenden, wenn Sie den Wert für `s.campaign` festlegen. Andernfalls kann ein falscher Kanal bei einem sekundären Kampagnen-Clickthrough zugewiesen werden.

Um dieses Plug-in zu implementieren, fügen Sie den folgenden Code in die Datei [!DNL s_code.js] ein.

```js
/******************************************************************** 
 * 
 * Main Plug-in code (should be in Plug-ins section) 
 * 
 *******************************************************************/ 
/* 
 * Plugin: getValOnce_v1.11 
 */ 
s.getValOnce=new Function("v","c","e","t","" 
+"var s=this,a=new Date,v=v?v:'',c=c?c:'s_gvo',e=e?e:0,i=t=='m'?6000" 
+"0:86400000,k=s.c_r(c);if(v){a.setTime(a.getTime()+e*i);s.c_w(c,v,e" 
+"==0?0:a);}return v==k?'':v");
```

Nachdem der oben aufgeführte Code implementiert wurde, definieren Sie die gewünschte Variable mit der Funktion *`getValOnce`*. Im Folgenden sind mehrere Beispiele für die Implementierung aufgeführt.

**Verhindern, dass der gleiche Kampagnenwert definiert wird, wenn ein doppelter Wert innerhalb von 30 Tagen nach dem Setzen des Cookies erkannt wird:** `s.campaign=s.getValOnce(s.campaign,'s_cmp',30);`  **Verhindert, dass derselbe eVar1-Wert definiert wird, wenn innerhalb von 30 Minuten nach dem Setzen des Cookies ein doppelter Wert festgestellt wird:**
`s.eVar1=s.getValOnce(s.eVar1,'s_ev1',30,'m');`  **Verhindert, dass derselbe eVar2-Wert mehrmals in derselben Browsersitzung definiert wird:**
`s.eVar2=s.getValOnce(s.eVar2,'s_ev2');`  **Anmerkungen**

* Testen Sie die Installation von Plug-ins stets ausführlich, um sicherzustellen, dass die Datenerfassung wie erwartet erfolgt, bevor Sie es in die Produktionsumgebung übernehmen.
* Achten Sie darauf, das Cookie zu löschen oder neue, eindeutige Werte beim Testen zu verwenden. Andernfalls werden Variablen nicht gesendet.

