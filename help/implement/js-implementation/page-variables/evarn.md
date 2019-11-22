---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
solution: Analytics
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 47291fb3d55ab3eb5ef181770bf2078c7ea55bc4

---


# eVarN

Mit den [!UICONTROL eVar]-Variablen werden benutzerdefinierte Berichte erstellt.


<!-- 

eVarN.xml

 -->

Wenn in einer eVar ein Wert für einen Benutzer festgelegt ist, bleibt dieser Wert bis zum Ablaufzeitpunkt gespeichert. Sämtliche Erfolgsereignisse, die bei einem Besucher auftreten, während der eVar-Wert aktiv ist, werden im eVar-Wert gezählt.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 255 Byte | V1-v75 ( [oder v100 oder v250](/help/implement/js-implementation/page-variables/page-variables.md)) | Benutzerspezifische Konversion | "" |

**Ablauf**

`eVars` laufen nach dem von Ihnen festgelegten Zeitraum ab. Nach dem Ablauf werden in der eVar keine Erfolgsereignisse mehr gezählt. eVars können auch so konfiguriert werden, dass sie bei Erfolgsereignissen ablaufen. Beispiel: Wenn Sie eine interne Werbeaktion haben, die am Ende eines Besuchs abläuft, werden für diese interne Werbeaktionen nur Einkäufe oder Registrierungen gezählt, die während des Besuchs erfolgten, in der sie aktiviert wurde.

Es gibt zwei Möglichkeiten für den Ablauf einer eVar:

* Sie können die eVar so einstellen, dass sie nach einem bestimmten Zeitraum oder Ereignis abläuft.
* Sie können das Ablaufen einer eVar erzwingen (z. B. wenn eine Variable für einen anderen Zweck eingesetzt werden soll).

Wenn zum Beispiel eine eVar im Mai dazu dienen soll, interne Werbeaktionen widerzuspiegeln (wobei sie nach 21 Tagen ablaufen soll) und im Juni dann eingesetzt wird, um interne Keywords zu erfassen, müssen Sie am 1. Juni ihren Ablauf erzwingen oder die Variable zurücksetzen. So verhindern Sie, dass die Werte zu der internen Werbeaktion vom Mai nicht im Bericht vom Juni auftauchen.

**Groß-/Kleinschreibung**

Bei eVars wird zwischen Groß- und Kleinschreibung unterschieden, sie werden jedoch in der Schreibweise angezeigt, die sie an der ersten Stelle ihres Auftretens hatten. Beispiel: Wenn eVar1 bei der ersten Instanz den Wert „Angemeldet“ enthält, in den darauf folgenden Instanzen jedoch „angemeldet“ heißt, wird in Berichten immer „Angemeldet“ als Wert von eVar angezeigt.

**Zähler**

Während eVars meist zur Speicherung von Zeichenfolgenwerten dienen, können sie auch so konfiguriert werden, dass sie als Zähler funktionieren. Als Zähler sind eVars dann nützlich, wenn Sie die Anzahl von Aktionen zählen möchten, die ein Benutzer vor einem Ereignis durchführt. So können Sie eine eVar beispielsweise einsetzen, um die Anzahl der internen Suchvorgänge vor einem Kauf zu zählen. Sobald ein Besucher eine Suche durchführt, wird der Wert der eVar um 1 erhöht. Wenn ein Besucher vier Suchen durchführt, bevor er einen Einkauf tätigt, wird Ihnen zu jeder Instanz eine Zählersumme angezeigt (1,00, 2,00, 3,00 und 4.00). Für das Kaufereignis wird jedoch nur die 4,00 gutgeschrieben (Bestellungen und Umsatz). Als Werte für eVar-Zähler sind nur positive Zahlen erlaubt.

**Subrelationen**

Eine gängige Anforderung an Berichte mit benutzerdefinierten eVars besteht darin, dass ein benutzerdefinierter eVar-Bericht nach einem anderen Bericht weiter aufgeschlüsselt werden kann. Wenn zum Beispiel eine eVar das Geschlecht und eine andere das Gehalt enthält, könnten Sie vielleicht die folgende Frage stellen: Wie viel Umsätze haben weibliche Besucher auf meiner Site getätigt, deren jährliches Einkommen mehr als 50.000 EUR beträgt? Aufschlüsselungen dieser Art sind mit allen eVars möglich, die vollständig miteinander verknüpft werden können. Beispiel: Wenn bei der eVar für das Geschlecht vollständige Subrelationen aktiviert sind, können alle anderen Berichte mit benutzerdefinierten eVars nach dem Geschlecht aufgeschlüsselt werden (und umgekehrt, d. h., das Geschlecht kann nach allen weiteren Aspekten, die in anderen eVar-Berichten aufgeführt sind, aufgeschlüsselt werden). Damit die Beziehung zwischen zwei Berichten angezeigt wird, müssen nur bei einem der beiden Berichte vollständige Subrelationen aktiviert sein. Standardmäßig sind die Berichte "Kampagne", "Produkte"und "Kategorie"vollständig untergeordnet (jede eVar kann nach Kampagne oder Produkten aufgeschlüsselt werden).

**Syntax und mögliche Werte**

Auch wenn eVars umbenannt werden dürfen, sollten Verweise auf eVars in der JavaScript-Datei immer in der Form „eVarX“ erfolgen, wobei X eine Zahl zwischen 1 und 75 ist ([oder 100 oder 250](/help/implement/js-implementation/page-variables/page-variables.md)).

```js
s.eVarX="value"
```

Außer beim Einsatz als Zähler gelten für eVars die gleichen Einschränkungen wie für alle anderen Variablen. In eVars, die als Zähler dienen, werden numerische Werte erwartet (z. B. „1“ oder „2,5“) Wenn mehr als zwei Dezimalstellen angegeben sind, wird die Zähler-eVar auf zwei Dezimalstellen gerundet. Negative Zahlen sind in Zähler-eVar nicht erlaubt.

**Beispiele**

```js
s.eVar1="logged in"
```

```js
s.eVar23="internal spring promo 4"
```

**Konfigurationseinstellungen**

eVars können unter Analytics &gt; Admin &gt; Report Suites &gt; Einstellungen bearbeiten &gt; Konversion &gt; Konversionsvariablen konfiguriert werden]. Bei allen eVars können Name, Typ, Zuordnung, Läuft ab nach und Zurücksetzen konfiguriert werden. Jede Konfigurationseinstellung wird separat vorgenommen.

<table id="table_5C524B71520849FA8A9A6B79A3EE77C9"> 
 <thead> 
  <tr> 
   <th class="entry"> Einstellung </th> 
   <th class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Name </td> 
   <td> Hiermit können Sie den Namen des eVar-Berichts in <span class="keyword">Analytics</span> ändern. <p>Unabhängig davon, welchen Namen der Bericht in <span class="keyword">Analytics</span> erhält, sollte die eVar im JavaScript-Code weiter in der Form „s.eVarX“ referenziert werden. </p> </td> 
  </tr> 
  <tr> 
   <td> Typ </td> 
   <td> Hiermit können Sie festlegen, ob die eVar eine Textzeichenfolge oder ein Zähler sein soll. </td> 
  </tr> 
  <tr> 
   <td> Zuordnung </td> 
   <td> Hiermit können Sie konfigurieren, welcher Wert in der eVar bei Erfolgsereignissen vermerkt werden soll. <p>Wenn „Zuordnung“ auf „Zuletzt verwendet (Letzter)“ festgelegt ist, erhält B die Gutschrift. </p> <p>Wenn „Zuordnung“ auf „Ausgangswert (Erster)“ festgelegt ist, erhält A die Gutschrift. </p> <p>Wenn „Zuordnung“ auf „Linear“ festgelegt ist, wird in A und B jeweils die Hälfte des Kaufwerts gutgeschrieben. </p> </td> 
  </tr> 
  <tr> 
   <td> Läuft ab nach </td> 
   <td> Hiermit können Sie festlegen, ob eine eVar bei einem bestimmten Ereignis (z. B. einen Kauf) oder nach einer benutzerdefinierten Zeitspanne ablaufen soll. </td> 
  </tr> 
  <tr> 
   <td> Zurücksetzen </td> 
   <td> Wenn Sie bei einer eVar das Kontrollkästchen <span class="wintitle">Zurücksetzen</span> aktivieren und unten auf der Seite auf <span class="wintitle">Speichern</span> klicken, laufen sämtliche Werte dieser eVar sofort ab. Danach werden in der eVar nur neue Gutschriften bei Erfolgsereignissen vermerkt. </td> 
  </tr> 
 </tbody> 
</table>

**Probleme, Fragen und Tipps**

* Im Unterschied zu [!UICONTROL Eigenschaftsvariablen] dürfen eVars keine Listen aus getrennten Werten sein. Wenn Sie in einer eVar eine Liste mit Werten eintragen (z. B. „Eins,Zwei,Drei“), wird als Wert exakt diese Zeichenfolge in Berichten angezeigt.
* Negative Zahlen sind in Zähler-eVar nicht erlaubt.
