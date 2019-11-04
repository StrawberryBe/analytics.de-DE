---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics-Implementierung
seo-description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
seo-title: Seitenvariablen
solution: Analytics
subtopic: Variablen
title: Seitenvariablen
topic: Entwickler und Implementierung
uuid: 2578eddd-74db-4a8a-96f2-d0289ec1826b
translation-type: tm+mt
source-git-commit: 8a96dc0587125e1b72e3146eb2f0923cecd808fb

---


# Seitenvariablen

Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.

## browserHeight {#concept_DB87062001824369A56AA1E7969EC02A}

Die Variable „“ gibt die Höhe des Browser-Fensters an.

<!-- 
browserheight.xml
-->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

**Parameter**

<table id="table_94598A2204CF42FF9DD14D353D5C0468"> 
 <thead> 
  <tr> 
   <th class="entry"> Abfrageparameter </th> 
   <th class="entry"> Wert </th> 
   <th class="entry"> Beispiel </th> 
   <th class="entry"> Betroffene Berichte </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>bh </p> </td> 
   <td> <p>Eine positive Ganzzahl </p> </td> 
   <td> <p>865 </p> </td> 
   <td> <p>„Datenverkehr“ &gt; „Technologie“ &gt; „Browserhöhe“ </p> </td> 
  </tr> 
 </tbody> 
</table>

## browserWidth {#concept_BA0C4C2D655D41A4AEF059E21E4A55A2}

Die Variable „“ gibt die Breite des Browser-Fensters an.

<!-- 

browserwidth.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

**Parameter**

<table id="table_B70F279A8CD240328520E5BD889806BD"> 
 <tbody> 
  <tr> 
   <td> <p> <b>Abfrageparameter</b> </p> </td> 
   <td> <p> <b>Wert</b> </p> </td> 
   <td> <p> <b>Beispiel</b> </p> </td> 
   <td> <p> <b>Betroffene Berichte</b> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>bw </p> </td> 
   <td> <p>Eine positive Ganzzahl </p> </td> 
   <td> <p>1179 </p> </td> 
   <td> <p>„Datenverkehr“ &gt; „Technologie“ &gt; „Browserbreite“ </p> </td> 
  </tr> 
 </tbody> 
</table>

## Kampagne {#concept_C7BF7B8A69D048A6AB482052A98A91F8}

In der Variablen sind die Marketing-Kampagnen angegeben, über die Besucher zu Ihrer Site gelangen. Der Wert wird normalerweise einem Abfragezeichenfolgen-Parameter entnommen.

<!-- 

campaign.xml

 -->

**Parameter**

<table id="table_A35175678B6C4D3D86287199AFBE6803"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>255 Byte </p> </td> 
   <td> <p>v0 </p> </td> 
   <td> <p>„Konversion“ &gt; „Kampagnen“ &gt; „Trackingcode“ </p> </td> 
   <td> <p>"" </p> </td> 
  </tr> 
 </tbody> 
</table>

Jedem Element in einer Marketing-Kampagne muss ein eindeutiger Trackingcode zugeordnet sein. So hat z. B. ein Keyword aus einer kostenpflichtigen Suchmaschinenkampagne den Trackingcode „112233“. Wenn ein Besucher auf das Keyword mit dem Trackingcode „112233“ klickt und auf die zugehörige Website gelangt, wird der Trackingcode in der *`campaign`*-Variablen vermerkt.

Es gibt zwei Möglichkeiten zum Auffüllen der Variable *`campaign`*:

* Das Plug-in [!UICONTROL getQueryParam] aus der JavaScript-Datei ruft einen Abfragezeichenfolgen-Parameter aus der URL ab. Weitere Informationen zum Plug-in [!UICONTROL getQueryParam] finden Sie in [Plug-ins für Implementierungen](../../../implement/js-implementation/plugins/impl-plugins.md#concept_021F5E4A6BD745AE91E85E7138BE930F).

* Weisen Sie der Variable *`campaign`* im HTML-Code auf der Webseite einen Wert zu.

Bei beiden Methoden zum Füllen der Variable *`campaign`* kann der Traffic der Zurück-Schaltfläche die tatsächliche Anzahl der Clickthroughs eines Kampagnenelements erhöhen.

Beispiel: Ein Besucher gelangt auf Ihre Website, indem er auf einen Keyword aus einer kostenpflichtigen Suchmaschinenkampagne klickt. Wenn der Besucher auf Ihre Landingpage gelangt, enthält die URL einen Abfragezeichenfolgen-Parameter, der den Trackingcode für den Keyword angibt. Anschließend klickt der Besucher auf einen Link zu einer anderen Seite, kehrt dann jedoch wieder auf Ihre Landingpage zurück, indem er auf die Schaltfläche „Zurück“ klickt. Wenn der Besucher zum zweiten Mal auf Ihre Landingpage gelangt, gibt die URL mit dem Abfragezeichenfolgen-Parameter erneut diesen Trackingcode an. Auch dieser zweite Clickthrough wird registriert und führt dann dazu, dass die Clickthrough-Rate fälschlicherweise zu hoch vermerkt wird.

Um diesen Effekt zu vermeiden, empfiehlt Adobe, mithilfe des Plug-ins [!UICONTROL getValOnce] zu erzwingen, dass jeder Kampagnen-Clickthrough nur einmal pro Sitzung gezählt wird. Weitere Informationen zum Plug-in [!UICONTROL getValOnce] finden Sie unter [Plug-ins für Implementierungen](../../../implement/js-implementation/plugins/impl-plugins.md#concept_021F5E4A6BD745AE91E85E7138BE930F).

**Syntax und mögliche Werte** {#section_91A141841A6D4711A1EE08A6145A301D}

```js
s.campaign="112233"
```

Für die Variable *`campaign`* gelten die gleichen Einschränkungen wie für alle anderen Variablen. Adobe empfiehlt, sich bei Werten für diese Variable auf standardmäßige ASCII-Zeichen zu beschränken.

**Groß-/Kleinschreibung** {#section_112A9A0F886148B6BEF9A7C94BE0A36F}

Bei eVars wird zwischen Groß- und Kleinschreibung unterschieden, sie werden jedoch in der Schreibweise angezeigt, die sie an der ersten Stelle ihres Auftretens hatten. Beispiel: Wenn eVar1 bei der ersten Instanz den Wert „Angemeldet“ enthält, in den darauf folgenden Instanzen jedoch „angemeldet“ heißt, wird in Berichten immer „Angemeldet“ als Wert von eVar angezeigt.

**Beispiele** {#section_705A25D05F6848E29C78320247AECB5F}

```js
s.campaign="112233"
```

```js
s.campaign=s.getQueryParam('cid');
```

**Konfigurationseinstellungen** {#section_4083F281968443169EAF8C0E8529D7BC}

Jeder Kampagnenwert bleibt für einen Benutzer aktiv, und in ihm werden bis zum Ablauf der Variablen alle Aktivitäten und Erfolgsereignisse des zugehörigen Benutzers vermerkt. Den Ablaufzeitpunkt der Kampagnenvariablen können Sie in der Admin Console ändern.

**Probleme, Fragen und Tipps** {#section_94B5C4BF9DE84BA3A16F9E9E9D197F0C}

* Um zu verhindern, dass die Clickthrough-Rate unnötig hochgezählt wird, verwenden Sie das Plug-in [!UICONTROL getValOnce], damit die Clickthrough-Raten für eine Kampagne nur einmal pro Sitzung gezählt werden. Weitere Informationen zum Plug-in [!UICONTROL getValOnce] finden Sie in [Plug-ins für Implementierungen](../../../implement/js-implementation/plugins/impl-plugins.md#concept_021F5E4A6BD745AE91E85E7138BE930F).

* Weitere Informationen über das Verfolgen von Marketing-Kampagnen und gekauften Keywords finden Sie in [Kampagnen](https://marketing.adobe.com/resources/help/en_US/reference/campaign.html).
* Mit dem [!DNL DigitalPulse Debugger] können Sie ermitteln, wie hoch der tatsächliche Wert von Kampagnen ist („v0“ im Debugger). Wenn „v0“ im Debugger nicht angezeigt wird, bedeutet dies, dass für diese Seite keine Kampagnendaten vermerkt wurden.

## kanal {#concept_C7770B8C15724A99B10F8F468AF82D0D}

Die Variable „“ wird meist verwendet, um einen Abschnitt einer Website zu identifizieren.

<!-- 

channel.xml

 -->

So könnten bei einem Händler zum Beispiel die Abschnitte „Elektronik“, „Spielzeug“ oder „Kleidung“ heißen. Eine Mediensite könnte die Abschnitte „Nachrichten“, „Sport“ oder „Wirtschaft“ enthalten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | CH | „Site-Content“ &gt; „Site-Abschnitte“ | "" |

Adobe empfiehlt, die Kanalvariable auf jeder Seite mit Werten zu füllen. Sie können auch eine Korrelation zwischen den Variablen *`channel`* und [!UICONTROL page name] aktivieren.

Wenn Bereiche eine oder mehrere Ebenen mit Unterbereichen aufweisen, können Sie diese Bereiche in der Variable *`channel`* zeigen oder mithilfe von gesonderten Variablen ausweisen.

**Syntax und mögliche Werte** {#section_ED90592730B64242A737F4090F1DCEE4}

```js
s.channel="value"
```

Für die Variable *`channel`* gibt es keine speziellen Einschränkungen.

**Beispiele** {#section_2527B2BB1CFD46CB952178ABF7A9028A}

```js
s.channel="Electronics"
```

```js
s.channel="Media"
```

**Probleme, Fragen und Tipps** {#section_61941D5E4E644B59A267A4F44FD5DE8C}

Wenn Ihre Site mehrere Ebenen enthält, können Sie die Variable *`hierarchy`* oder eine andere Variable verwenden, um diese Ebenen zu bezeichnen. Der Wert *`channel`* ist nicht beständig, aber die auf der gleichen Seite ausgelösten Erfolgsereignisse werden dem Wert *`channel`* zugeordnet.

## colorDepth {#concept_756516E181F449B996DA9CC5A53FFA3D}

In der Variablen „“ ist angegeben, mit wie vielen Bit die Farbe jedes Pixels dargestellt wird.

<!-- 

colordepth.xml

 -->

So würde zum Beispiel der Wert 32 bedeuten, dass die Farbtiefe des Bildschirms 32 Bit beträgt. Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in `props/eVars` kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| c | 8,16 und 32 | 32 | „Datenverkehr“ &gt; „Technologie“ &gt; „Bildschirmfarbtiefe“ |

## connectionType {#concept_2F98ECB8BB3D490F834F274EFF02860E}

Die Variable „“ in Internet Explorer gibt an, ob der Browser für eine LAN- oder eine Modemverbindung konfiguriert ist.

<!-- 

conntype.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in `props/eVars` kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| ct | „lan“ oder „modem“ | lan | „Datenverkehr“ &gt; „Technologie“ &gt; „Verbindungstyp“ |

## cookiesEnabled {#concept_DF5B37E38D0D4F6DB910F419F92467ED}

Die Variable „“ gibt an, ob JavaScript Sitzungscookies von Erstanbietern setzen darf.

<!-- 

cookiesenabled.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in `props/eVars` kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel |
|---|---|---|
| k | J oder N | Y |

## dc {#concept_ECE6C83376704B3C84A920EFDD338A31}

(Veraltet) Mithilfe der Variablen „“ können Sie auswählen, zu welchem Data Center Ihre Daten gesendet werden.

<!-- 

dc.xml

 -->

> [!NOTE] Die Variable „dc“ ist veraltet. Legen Sie *`trackingServer`bei allen Implementierungen auf den vom Code-Manager in s_code.js generierten Wert fest.*

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | 112 |

Das Data Center ist in der Variablen *`dc`* zum Abgleich mit [!UICONTROL ActionSource] angegeben.

## eVarN {#concept_74FFDDB44B5344E18ABC6F2F99DF4649}

Mit den [!UICONTROL eVar]-Variablen werden benutzerdefinierte Berichte erstellt.

<!-- 

eVarN.xml

 -->

Wenn in einer eVar ein Wert für einen Benutzer festgelegt ist, bleibt dieser Wert bis zum Ablaufzeitpunkt gespeichert. Sämtliche Erfolgsereignisse, die bei einem Besucher auftreten, während der eVar-Wert aktiv ist, werden im eVar-Wert gezählt.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 255 Byte | V1-v75 ( [oder v100 oder v250](../../../implement/js-implementation/c-variables/page-variables.md#concept_558663F3B8164986AB5D94128FEA7B28)) | Benutzerspezifische Konversion | "" |

**Ablauf** {#section_6DB5882B960D4660AE248B91B76883C4}

[!UICONTROL eVars] laufen nach dem von Ihnen festgelegten Zeitraum ab. Nach dem Ablauf werden in der eVar keine Erfolgsereignisse mehr gezählt. eVars können auch so konfiguriert werden, dass sie bei Erfolgsereignissen ablaufen. Beispiel: Wenn Sie eine interne Werbeaktion haben, die am Ende eines Besuchs abläuft, werden für diese interne Werbeaktionen nur Einkäufe oder Registrierungen gezählt, die während des Besuchs erfolgten, in der sie aktiviert wurde.

Es gibt zwei Möglichkeiten für den Ablauf einer eVar:

* Sie können die eVar so einstellen, dass sie nach einem bestimmten Zeitraum oder Ereignis abläuft.
* Sie können das Ablaufen einer eVar erzwingen (z. B. wenn eine Variable für einen anderen Zweck eingesetzt werden soll).

Wenn zum Beispiel eine eVar im Mai dazu dienen soll, interne Werbeaktionen widerzuspiegeln (wobei sie nach 21 Tagen ablaufen soll) und im Juni dann eingesetzt wird, um interne Keywords zu erfassen, müssen Sie am 1. Juni ihren Ablauf erzwingen oder die Variable zurücksetzen. So verhindern Sie, dass die Werte zu der internen Werbeaktion vom Mai nicht im Bericht vom Juni auftauchen.

**Groß-/Kleinschreibung** {#section_6E9145B7FCC2438E95BB35AAE3857412}

Bei eVars wird zwischen Groß- und Kleinschreibung unterschieden, sie werden jedoch in der Schreibweise angezeigt, die sie an der ersten Stelle ihres Auftretens hatten. Beispiel: Wenn eVar1 bei der ersten Instanz den Wert „Angemeldet“ enthält, in den darauf folgenden Instanzen jedoch „angemeldet“ heißt, wird in Berichten immer „Angemeldet“ als Wert von eVar angezeigt.

**Zähler** {#section_D8403F0C175E4BC9BE4F2E794B1F4D33}

Während eVars meist zur Speicherung von Zeichenfolgenwerten dienen, können sie auch so konfiguriert werden, dass sie als Zähler funktionieren. Als Zähler sind eVars dann nützlich, wenn Sie die Anzahl von Aktionen zählen möchten, die ein Benutzer vor einem Ereignis durchführt. So können Sie eine eVar beispielsweise einsetzen, um die Anzahl der internen Suchvorgänge vor einem Kauf zu zählen. Sobald ein Besucher eine Suche durchführt, wird der Wert der eVar um 1 erhöht. Wenn ein Besucher vier Suchen durchführt, bevor er einen Einkauf tätigt, wird Ihnen zu jeder Instanz eine Zählersumme angezeigt (1,00, 2,00, 3,00 und 4.00). Für das Kaufereignis wird jedoch nur die 4,00 gutgeschrieben (Bestellungen und Umsatz). Als Werte für eVar-Zähler sind nur positive Zahlen erlaubt.

**Subrelationen** {#section_2BEABBBC735241F4BA42E74D19B5AEE0}

Eine gängige Anforderung an Berichte mit [!UICONTROL benutzerdefinierten eVars] besteht darin, dass ein [!UICONTROL benutzerdefinierter eVar]-Bericht nach einem anderen Bericht weiter aufgeschlüsselt werden kann. Wenn zum Beispiel eine eVar das Geschlecht und eine andere das Gehalt enthält, könnten Sie vielleicht die folgende Frage stellen: Wie viel Umsätze haben weibliche Besucher auf meiner Site getätigt, deren jährliches Einkommen mehr als 50.000 EUR beträgt? Aufschlüsselungen dieser Art sind mit allen eVars möglich, die vollständig miteinander verknüpft werden können. Beispiel: Wenn bei der eVar für das Geschlecht vollständige Subrelationen aktiviert sind, können alle anderen Berichte mit benutzerdefinierten eVars nach dem Geschlecht aufgeschlüsselt werden (und umgekehrt, d. h., das Geschlecht kann nach allen weiteren Aspekten, die in anderen eVar-Berichten aufgeführt sind, aufgeschlüsselt werden). Damit die Beziehung zwischen zwei Berichten angezeigt wird, müssen nur bei einem der beiden Berichte vollständige Subrelationen aktiviert sein. In der Standardeinstellung sind bei den Berichten [!UICONTROL Kampagnen], [!UICONTROL Produkte] und [!UICONTROL Kategorie] vollständige Subrelationen aktiviert (d. h., jede beliebige eVar kann nach der Kampagne oder nach Produkten weiter aufgeschlüsselt werden).

**Syntax und mögliche Werte** {#section_BD46438B14F3488FB9AC42994C317B06}

Auch wenn eVars umbenannt werden dürfen, sollten Verweise auf eVars in der JavaScript-Datei immer in der Form „eVarX“ erfolgen, wobei X eine Zahl zwischen 1 und 75 ist ([oder 100 oder 250](../../../implement/js-implementation/c-variables/page-variables.md#concept_558663F3B8164986AB5D94128FEA7B28)).

```js
s.eVarX="value"
```

Außer beim Einsatz als Zähler gelten für eVars die gleichen Einschränkungen wie für alle anderen Variablen. In eVars, die als Zähler dienen, werden numerische Werte erwartet (z. B. „1“ oder „2,5“) Wenn mehr als zwei Dezimalstellen angegeben sind, wird die Zähler-eVar auf zwei Dezimalstellen gerundet. Negative Zahlen sind in Zähler-eVar nicht erlaubt.

**Beispiele** {#section_B37F4B0D56734DA3AB02BB218825BA4E}

```js
s.eVar1="logged in"
```

```js
s.eVar23="internal spring promo 4"
```

**Konfigurationseinstellungen** {#section_BD1FE63001C84D3DB69F3DEE243960B6}

eVars können unter [!UICONTROL Analytics &gt; Admin &gt; Report Suites &gt; Einstellungen bearbeiten &gt; Konversion &gt; Konversionsvariablen] konfiguriert werden. Bei allen eVars können [!UICONTROL Name], [!UICONTROL Typ], [!UICONTROL Zuordnung], [!UICONTROL Läuft ab nach] und [!UICONTROL Zurücksetzen] konfiguriert werden. Jede Konfigurationseinstellung wird separat vorgenommen.

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

**Probleme, Fragen und Tipps** {#section_DA6912C802E445F986C6DE4234C6C737}

* Im Unterschied zu [!UICONTROL Eigenschaftsvariablen] dürfen eVars keine Listen aus getrennten Werten sein. Wenn Sie in einer eVar eine Liste mit Werten eintragen (z. B. „Eins,Zwei,Drei“), wird als Wert exakt diese Zeichenfolge in Berichten angezeigt.
* Negative Zahlen sind in Zähler-eVar nicht erlaubt.

## Ereignisse {#concept_FFD115543D54401B98FE683BD7D5B3FE}

Die Variable „“ wird zur Aufzeichnung von Erfolgsereignissen normaler Warenkorbvorgänge sowie benutzerspezifischer Erfolgsereignisse verwendet.

<!-- 

events.xml

 -->

<table id="table_9EB9D08C80544CD68C4B1A2012440472"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Keine Begrenzung </td> 
   <td> events </td> 
   <td> <p>Warenkorbereignisse </p> <p>Benutzerspezifische Ereignisse </p> </td> 
   <td> Keine </td> 
  </tr> 
 </tbody> 
</table>

[!UICONTROL Ereignisse] sollten als Meilenstein in einer Site dienen. Erfolgsereignisse werden in den meisten Fällen auf der abschließenden Bestätigungsseite eines Vorgangs (z. B. einer Registrierung oder einer Anmeldung) ausgefüllt. Benutzerspezifische Ereignisse werden definiert, indem in der „events“-Variablen entsprechende Zeichenwerte eingetragen werden (siehe dazu Abschnitt Mögliche Werte weiter unten).

In der Standardeinstellung werden Erfolgsereignisse als *Zählerereignisse* konfiguriert. Zählerereignisse zählen, wie oft ein Erfolgsereignis eintritt (x+1). Ereignisse können auch als *numerische* Ereignisse festgelegt werden. Mithilfe numerischer Ereignisse können Sie angeben, um welche Höhe ein Wert erhöht werden soll (was beim Zählen dynamischer oder beliebiger Werte nützlich sein kann, zum Beispiel bei der Anzahl der von einer internen Suche zurückgegebenen Ergebnisse).

Mit Ereignissen vom Typ *Währung* können Sie einen hinzuzufügenden Geldbetrag festlegen. Dieser ist eine Zahlangabe wie bei numerischen Ereignissen, wird jedoch in Berichten als Geldbetrag angezeigt. Er kann gemäß der im Wert s. *`currencyCode`* und der in Ihrer Report Suite festgelegten Standardwährung in andere Währungen umgerechnet werden. Weitere Informationen zur Arbeit mit numerischen und Währungs-Ereignissen finden Sie in [Produkte](../../../implement/js-implementation/c-variables/page-variables.md#concept_A4007F6307E4419DAA65E1668A8FEBA2).

**Konfigurieren der Variablen** {#section_9195286C34C54B02B2598E2B856492C3}

Die Variable [!UICONTROL s.events] ist in der Standardeinstellung für alle Implementierungen aktiviert. Die sieben vorkonfigurierten Konversionsereignisse sind bei allen neuen Report Suites automatisch aktiviert. Neue benutzerspezifische Ereignisse (event1– [event100 oder event1000](../../../implement/js-implementation/c-variables/page-variables.md#concept_558663F3B8164986AB5D94128FEA7B28)) können von jedem Nutzer mit Administratorrechten über die Admin Console aktiviert werden.

**Mögliche Werte** {#section_18395A3BEFEB4E9F8D7B2ED0001FBE4E}

Die folgenden Werte sind in der „events“-Variablen möglich:

| Ereignis | Beschreibung | Ausgefüllte Berichte |
|---|---|---|
| prodView | Produktansichten | Produkte |
| scOpen | Öffnen / Initialisieren eines neuen Warenkorbs | Warenkörbe |
| scAdd | Hinzufügen von Artikeln zum Warenkorb | Zusatz zum Warenkorb |
| scRemove | Entfernen von Artikeln aus dem Warenkorb | Entnahme aus Warenkorb |
| scView | Anzeigen von Warenkorb | Warenkorbansicht |
| scCheckout | Beginn des Checkout-Prozess | Checkouts |
| purchase | Abschluss eines Kaufs (oder einer Bestellung) | Bestellungen |
| event1 - event1000 (event100 für Punktprodukt) | Benutzerspezifische Ereignisse | Benutzerspezifische Ereignisse |

**Syntax und Beispiele** {#section_45A159DF00114066B8551DDEB15E084C}

Zählerereignisse werden festgelegt, indem die gewünschten Ereignisse in die [!UICONTROL s.events]-Variable eingetragen werden (bei mehreren Ereignissen in Form einer kommagetrennten Liste).

```js
s.events="scAdd"
```

```js
s.events="scAdd,event1,event7"
```

```js
s.events="event5"
```

```js
s.events="purchase,event10"
```

In H23-Code (oder höher) können Zählerereignissen auch ganzzahlige Werte größer Eins zugewiesen werden.

```js
s.events="event1=10"
```

```js
s.events="scRemove=3,event6,event2=4"
```

Zählerereignisse, die mit ganzzahligen Werten implementiert sind, werden so behandelt, als ob das Ereignis innerhalb der Bildanforderung mehrere Male ausgelöst wurde. Dezimalstellen sind in Zählerereignissen nicht zulässig. Sollte dies erforderlich sein, empfiehlt sich stattdessen die Verwendung von numerischen Ereignissen.
Numerische und Währungs-Ereignisse müssen in der Variablen [!UICONTROL s.events] stehen, obwohl sie ihre numerischen Werte (z. B. „24,99“) meist über die Variable [!UICONTROL s.products] erhalten. Dadurch können Sie bestimmte numerische und Währungswerte mit bestimmten Produkteinträgen verknüpfen.

**Ereignis-Serialisierung** {#section_A89488EF4471405AAFC4D6DD05E77621}

In der Standardeinstellung wird ein Ereignis jedes Mal gezählt, wenn es auf Ihrer Site festgestellt wird.

Weitere Informationen dazu finden Sie unter [Ereignis-Serialisierung](../../../implement/js-implementation/event-serialization.md#concept_092B638D7FEE423D91F8A57EA8E09705).

**Syntax** {#section_8559D42D3F344AF3BB3C0125F78C4989}

```js
s.events="event1:3167fhjkah"
```

**Beispiele** {#section_7B5B5728A59648ADB3E2548CDAD2C9D4}

```js
s.events="scAdd:003717174"
```

```js
s.events="scAdd:user228197,event1:577247280,event7:P7fhF8571"
```

## hierN {#concept_C4475D1584D544ACB4C0A573EB60FA08}

Die Variable [!UICONTROL hierarchy] bestimmt die Positionierung einer Seite in der Hierarchie der Site.

<!-- 

hierN.xml

 -->

Bei Sites mit mehr als drei Ebenen in der Sitestruktur ist diese Variable besonders nützlich. So kann zum Beispiel eine Mediensite über vier Ebenen im Abschnitt „Sport“ verfügen: Sport, Lokaler Sport, Fußball, Bayern München. Wenn ein Besucher die Fußballseite aufruft, wird dieser Besuch in den Ebenen „Sport“, „Lokaler Sport“ und „Fußball“ widergegeben.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 255 Byte | H1-H5 | Hierarchie | "" |

Es sind fünf [!UICONTROL hierarchy]-Variablen verfügbar, die vom Adobe-Kundendienst aktiviert werden müssen. Bei Aktivierung der hierarchy-Variablen müssen Sie festlegen, welches Trennzeichen verwendet werden soll und über wie viele Ebenen die Hierarchie maximal verfügen soll. Wenn beispielsweise ein Komma als Trennzeichen dient, wird die Sporthierarchie wie folgt dargestellt.

```js
s.hier1="Sports,Local Sports,Baseball"
```

Achten Sie darauf, dass keiner Ihrer Abschnittsnamen das Trennzeichen enthält. Wenn zum Beispiel einer Ihrer Abschnitte „Trainer Heynckes, Jupp“ heißt, sollten Sie kein Komma als Trennzeichen festlegen. Jeder Hierarchieabschnitt ist auf 255 Byte beschränkt, wobei das Limit für die Variable insgesamt 255 Byte beträgt. Nach Auswahl des Trennzeichens (zum Zeitpunkt der Erstellung der Hierarchie) ist eine spätere Änderung nicht so einfach möglich.

Wenden Sie sich an den Adobe-Kundendienst, wenn Sie bei einer vorhandenen Hierarchie das Trennzeichen ändern möchten. Trennzeichen können auch aus mehreren Zeichen bestehen (z. B. || oder /|\), bei denen es unwahrscheinlich ist, dass sie in Namen von Hierarchieabschnitten enthalten sind.

**Syntax und mögliche Werte** {#section_0739948A68A2420DAB1CBEA3115A5A66}

Zwischen den einzelnen Trennzeichen darf kein Leerzeichen stehen. Im folgenden Syntaxbeispiel steht „N“ für eine Ziffer zwischen 1 und 5.

```js
s.hierN="Level 1[<delimiter>Level 2[<delimiter>Level 3[...]]]"
```

Setzen Sie das Trennzeichen nur ein, um die Ebenen der Hierarchie voneinander zu trennen. Als Trennzeichen sind ein oder mehrere beliebige Zeichen Ihrer Wahl erlaubt.

**Beispiele** {#section_38E0929F88DD45B6ACDF473DF155971D}

```js
s.hier1="Toys|Boys 6+|Legos|Super Block Tub"
```

```js
s.hier4="Sports/Local Sports/Baseball"
```

**Konfigurationseinstellungen** {#section_E823FB3CAD744D2480EBCE2DF9B134CC}

Keine

**Probleme, Fragen und Tipps** {#section_104E5BD320764BDEA5FA8D13A70C78E3}

* Das Trennzeichen darf nach dem Einrichten der Hierarchie nicht mehr geändert werden. Wenn Sie bei Ihrer Hierarchie das Trennzeichen ändern müssen, wenden Sie sich an den Adobe-Kundendienst.
* Die Anzahl der Ebenen darf nach dem Einrichten der Hierarchie nicht mehr geändert werden.

> [!NOTE] Änderungen an Hierarchien können dazu führen, dass eine kostenpflichtige Serviceleistung berechnet wird.

## homepage {#concept_0A3E416F1A064BA396B5FCEABFB7B0B4}

Die Variable „“ in Internet Explorer gibt an, ob die aktuelle Seite als Startseite des Benutzers festgelegt ist.

<!-- 

homepage.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| hp | J oder N | Y | „Datenverkehr“ &gt; „Technologie“ &gt; „Homepage“ |

## javaEnabled {#concept_F24A3536F1F0453DA214B16BAA5A6F67}

Die Variable „“ zeigt an, ob im Browser Java aktiviert ist.

<!-- 

javaEnabled.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor „doPlugins“ ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| v | J oder N | Y | Datenverkehr &gt; Technologie &gt; Java |

## javascriptVersion {#concept_19E2C9F87BB24E69B911C0F5873CAA90}

Die Variable „“ gibt an, welche JavaScript-Version vom Browser unterstützt wird.

<!-- 

javascriptVersion.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| j | 1.0, 1.1, 1.2, … 1.7 | 1.7 | Datenverkehr &gt; Technologie &gt; JavaScript Version |

Ab der Version H.10 der JavaScript-Datei werden Versionen bis zu 1.7 genau erkannt (welches die aktuellste Version zum Zeitpunkt der Veröffentlichung von H.10 war). Ältere Versionen der JavaScript-Datei konnten nur bis zu Version 1.3 erkennen.

## linkName {#concept_1B2A3F56C9AD4C23A8A4331730EC2B8F}

Die Variable „“ ist eine optionale Variable, die beim [!UICONTROL Linktracking] den Namen eines benutzerspezifischen Links, eines Exitlinks oder Downloadlinks angibt.

<!-- 

linkName.xml

 -->

Die Variable *`linkName`* ist normalerweise nicht erforderlich, da diese Variable durch den dritten Parameter in der Funktion *`tl()`* ersetzt wird.

<table id="table_4B0D1C9AADA542A59B626E077D5FC568"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 100 Byte </td> 
   <td> pev2 </td> 
   <td> <p>Dateiladungen </p> <p>Benutzerspezifische Links </p> <p>Exitlinks </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

[!UICONTROL Benutzerspezifische Links] verweisen auf Links, die Rückverfolgungsdaten senden. Die Variable *`linkName`* (oder der dritte Parameter in der Funktion *`tl()`*) wird verwendet, um den Wert zu identifizieren, der im [!UICONTROL Benutzerspez.], [!UICONTROL Download-] oder [!UICONTROL Exitlinks-]Bericht erscheint. Wenn *`linkName`* nicht aufgefüllt ist, wird im Bericht die URL des Links angezeigt.

**Syntax und mögliche Werte** {#section_C8D89834C98B4C7A858C947293C4148E}

```js
s.linkName="Link Name"
```

*`linkName`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_5F68766210184E82A23D2A6ECD80BA0B}

```js
s.linkName="Nav Bar Home Link"
```

```js
s.linkName="Partner Link to A.com"
```

**Konfigurationseinstellungen** {#section_F15FF429FC274F708D50DF79D4668EA3}

Keine

**Probleme, Fragen und Tipps** {#section_170A78452A7340B5B229713AC1FB71FA}

* Die Variable *`linkName`* wird durch den dritten Parameter in der Funktion *`tl()`* ersetzt.

* Wenn die Variable *`linkName`* und der dritte Parameter in der Funktion *`tl()`* leer sind, wird die vollständige URL des Links (mit Ausnahme der Abfragezeichenfolge) im Bericht angezeigt (auch bei einem relativen Link).

## „linkType“{#concept_7695692AF5D843E3B370F6D345E32964}

Die Variable „“ ist optional und gibt bei der Linktracking an, in welchem Bericht ein Linkname oder eine Link-URL angezeigt wird (benutzerspezifische, Download- oder Exitlinks).

<!-- 

linkType.xml

 -->

Die Variable *`linkType`* ist normalerweise nicht erforderlich, da diese Variable durch den zweiten Parameter in der Funktion *`tl()`* ersetzt wird.

<table id="table_3D1A2FC1CECD4709BE2F9E32AC2DC730"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Ein Zeichen </td> 
   <td> pe=[lnk_o|lnk_d|lnk_e] </td> 
   <td> <p>Dateiladungen </p> <p>Benutzerspezifische Links </p> <p>Exitlinks </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

Benutzerspezifische Links senden Daten nach Analytics Die Variable *`linkType`* (oder der zweite Parameter in der Funktion *`tl()`*) wird verwendet, um den Bericht zu identifizieren, in dem der Linkname oder die URL erscheint ( [!UICONTROL Benutzerspez.], [!UICONTROL Download-], oder [!UICONTROL Exitlinks-] Bericht).

Bei Exitlinks und Downloadlinks wird die Variable *`linkType`* automatisch gefüllt, je nachdem, ob es sich bei dem angeklickten Link um einen Exitlink oder Downloadlink handelt. Ein benutzerspezifischer Link kann konfiguriert werden, um Daten an einen dieser drei Berichte mit dieser Variablen oder den zweiten Parameter in der Funktion *`tl()`* zu senden. Durch die Einstellung von *`linkType`* auf „o“, „e“ oder „d“ wird *`linkName`* bzw. die Link-URL an den Bericht [!UICONTROL Benutzerspezifische Links], [!UICONTROL Exitlinks] bzw. [!UICONTROL Datei-Downloads] gesendet.

**Syntax und mögliche Werte** {#section_18DB3A8083FB4F75B970055ED336DA4E}

Die Syntax der Variable *`linkType`* hängt davon ab, ob Sie XML oder eine Abfragezeichenfolge verwenden.

Wenn Sie XML verwenden, darf die Variable nur ein einziges Zeichen, nämlich „o“ „e“ oder „d“, enthalten.

```js
s.tl(this,'o','Link Name');
```

Wenn Sie die Abfragezeichenfolge `pe` verwenden, müssen Sie `lnk_e`, `lnk_d` oder `lnk_o` hinzufügen.

**Beispiele** {#section_242B5DFFD1C9462A9A8EB1556B2E3160}

```js
<a href="index.html" onClick=" 
 var s=s_gi('rsid'); **see note below on the rsid** 
 s.tl(this,'o','Link Name'); 
 ">My Page</a> 
```

**Konfigurationseinstellungen** {#section_59738AD1B5E94294B8D36F4E772DEDB3}

Keine

**Probleme, Fragen und Tipps** {#section_F0D01DDE3FDA486C987162DA50A79C45}

* Wenn *`linkType`* nicht angegeben ist, wird von benutzerspezifischen Links („o“) ausgegangen.

## Listen-Props {#concept_83ED74232225431F83A796E22FFC75B4}

Listen-Props sind eine Liste getrennter Werte, die in einer Variablen übergeben und in Berichten dann als einzelne Zeilenelemente behandelt werden. Listen-Props werden meist auf Seiten implementiert, die vom Benutzer auswählbare Werte enthalten (wie z. B. Artikellisten mit Kontrollkästchen oder Optionsschaltern). Sie sind nützlich, wenn Sie mehrere Werte in einer einzigen Variablen definieren möchten, ohne dass mehrere Bildanforderungen gesendet werden.

<!-- 

list_props.xml

 -->

**Zu beachten**

* Listen-Props sind nur für Traffic-Variablen ( [props](../../../implement/js-implementation/c-variables/page-variables.md#concept_0F10FA2DE69B4029A31EA5E9313AA254)).
* Die Pathing-Funktion und Korrelationen können bei Listen-Props nicht aktiviert werden.
* Analytics gibt Besuche und Unique Visitors in fast jedem Bericht an (inklusive aller Listen-Props-Berichte).
* Für Listen-Props werden Classifications unterstützt.
* Jede benutzerspezifische Traffic-Variable kann zu einer Listen-Prop werden. (Ausnahmen: [pageName](../../../implement/js-implementation/c-variables/page-variables.md#concept_5827B499DAC34B5D8445F9D9140CC328), [channel](../../../implement/js-implementation/c-variables/page-variables.md#concept_C7770B8C15724A99B10F8F468AF82D0D) und [server](../../../implement/js-implementation/c-variables/page-variables.md#concept_BF77952603BA454BAFC9A0A81D06A7D2).)

* Wenn in einer Bildanforderung Werte doppelt definiert sind, werden Instanzen nicht dedupliziert.

Ein Prop kann auf der Seite „Admin Tools &gt; Report Suite &gt; Traffic-Variablen“ in ein Listen-Prop umgewandelt werden, indem Sie die Listenunterstützung aktivieren und anschließend ein Trennzeichen auswählen. Häufig verwendete Trennzeichen sind: Doppelpunkt, Semikolon, Komma oder senkrechter Strich (Pipe). Als Trennzeichen können grundsätzlich die ersten 127 ASCII-Zeichen verwendet werden.

**Implementierungsbeispiele** {#section_A3DD7293A8BB4807B42BFB1F73BE11AC}

Wenn Sie eine Aktivierung von Listen-Props anfordern, müssen Sie das Trennzeichen angeben, das Sie verwenden möchten. Nach Aktivierung der gewünschten *`s.prop`* können mehrere Werte in der Variable – wie in den folgenden Beispielen gezeigt – festgelegt werden:

Eine durch einen senkrechten Strich (Pipe) begrenzte Listen-Prop, die zwei Werte übergibt:

```js
s.prop1="Banner ad impression|Sidebar impression"
```

Eine durch ein Komma begrenzte Listen-Prop, die mehrere Werte übergibt:

```js
s.prop2="cerulean,vermilion,saffron"
```

Listen-Props können auch mit einem einzelnen Wert gesendet werden:

```js
s.prop3="Single value"
```

Das Trennzeichen kann jederzeit geändert werden. Die Implementierung muss aber dem neuen Trennzeichen entsprechen. Fehler bei der Verwendung des korrekten Trennzeichens im Wert der Listen-Prop führen dazu, dass der Wert bei der Berichterstellung als einzelner verketteter Zeileneintrag behandelt wird.

Da es sich bei einer Listen-Props weiterhin um eine Traffic-Variable handelt, unterliegt sie auch den Beschränkungen für Traffic-Variablen. Listen-Props sind auf 100 Byte an Daten begrenzt und unterliegen Einstellungen für die Groß-/Kleinschreibung.

## Listenvariable {#concept_AC42F2D69B674C02A484137CE5B4E687}

Wird auch als „List Var“ bezeichnet. Ähnlich wie bei Listen-Props sind bei Listenvariablen mehrere Werte in derselben Bildanforderung möglich. Sie funktionieren auch ähnlich wie eVars, die über die Bildanforderung hinaus erhalten bleiben, für die sie definiert wurden. Sie können mit diesen Variablen bei vielen Elementen auf einer einzelnen Seite Ursache und Wirkung erkennen (z. B. bei Produktlisten, Wunschlisten, Listen mit Sucheinschränkungen oder Listen mit Display-Anzeigen).

<!-- 

listN.xml

 -->

**Zu beachten**

* Listenvariablen speichern ihre jeweiligen Werte durch Verweis auf das VisitorID-Cookie im Browser des Besuchers.
* Maximal 250 Werte werden gleichzeitig pro Besucher gespeichert. Wenn 250 Werte pro Besucher überschritten werden, so werden die letzten 250 Werte verwendet. Der Ablauf dieser Werte basiert auf dem für die Variable konfigurierten Ablauf.
* Jeder durch ein Trennzeichen begrenzte Wert kann maximal 255 Zeichen (bei Multibytezeichen weniger) enthalten. Dies ist die maximale Länge jedes Elements.
* Innerhalb dieser Variable gibt es keine Begrenzung für die Zeichenanzahl. Die einzige Ausnahme dabei gilt für ältere Versionen von Internet Explorer, in denen URL-Anforderungen maximal 2.083 Zeichen lang sein dürfen.
* Insgesamt sind pro Report Suite drei Listenvariablen verfügbar.
* Für Listenvariablen ist H23-Code oder höher erforderlich.
* Listenvariablen können klassifiziert werden.
* Wenn Werte in einer Bildanforderung doppelt definiert sind, deduplizieren Listenvariablen alle Instanzen dieser Werte.
* Die gröbste Segmentierung, die bei Listenvariablen möglich ist, erfolgt auf Hitebene (oder Seitenansichtsebene). Wenn in einer Bildanforderung eine Listenvariable mit drei Werten vorhanden ist und eine beliebige Segmentregel auf einen der Werte zutrifft, werden alle drei Werte in die Berichterstellung aufgenommen. Umgekehrt gilt, wenn eine Ausschlussregel definiert ist, die mit einem der Werte übereinstimmt, werden alle drei Werte ausgeschlossen.

**Konfiguration** {#section_8CADFF581D2447518BA3F7F79B2D80A9}

Sie können über die Admin Console auf die Konfiguration zugreifen und sie aktualisieren, ohne dabei die Hilfe des Adobe Kundendiensts in Anspruch zu nehmen:

1. Navigieren Sie zu: **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]**
1. Wählen Sie die Report Suite aus.
1. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** &gt; **[!UICONTROL Konversion]** &gt; **[!UICONTROL Listenvariablen]**.

* **Name**: Jeder durch ein Trennzeichen begrenzte Wert kann maximal 255 Zeichen (bei Multibytezeichen weniger) enthalten. Dies ist die maximale Länge jedes Elements.
* **Trennzeichen für Werte**: Das Zeichen, mit dem Werte in der Listenvariable voneinander getrennt werden. Häufig handelt es sich dabei um Zeichen wie Komma, Doppelpunkt, senkrechter Strich (Pipe) usw.

   >[!NOTE]
   >
   >Multi-Byte-Zeichen werden als Trennzeichen in Listenvariablen nicht unterstützt. Das Trennzeichen muss ein Single-Byte-Zeichen sein.

* **Ablauf**: Bestimmt, ähnlich wie beim eVar-Ablaufdatum, den Zeitraum, der zwischen der Listenvariable und dem zugehörigen Konversionsereignis liegen kann.

   * **Auf Seitenansichts- oder Besuchsebene**: Erfolgsereignisse außerhalb der Seitenansicht oder des Besuchs werden nicht wieder mit Werten in der Listenvariablen verknüpft.
   * **Auf Basis eines Zeitraums (Tag, Woche, Monat usw.)**: Erfolgsereignisse außerhalb des angegebenen Zeitraums werden nicht wieder mit Werten in der Listenvariablen verknüpft. Hier kann auch eine benutzerspezifische Anzahl von Tagen festgelegt werden.
   * **Bestimmte Konversionsereignisse**: Alle anderen Erfolgsereignisse, die nach dem angegebenen Ereignis ausgelöst werden, werden nicht wieder mit Werten in der Listenvariable verknüpft.
   * **Nie**: Zwischen der Listenvariablen und dem Erfolgsereignis kann ein beliebiger Zeitraum vergehen.

* **Zuordnung**: Diese Einstellung gibt vor, wie Erfolgsereignisse Gutschriften auf Werte aufteilen:

   * **Vollständig**: Erfolgsereignisse werden in allen Variablenwerten, die vor dem Ablauf der Variablen definiert sind, vollständig gutgeschrieben.
   * **Linear**: Konversionsereignisse werden in allen Variablenwerten, die vor dem Ablauf der Variablen definiert sind, aufgeteilt gutgeschrieben.
   * Variablenwerte werden niemals überschrieben, sondern die Gutschriften werden zu den Werten, in denen Erfolgsereignisse gutgeschrieben werden, hinzugefügt.

* **Höchstwerte**: Gibt die Anzahl der für diese Listenvariable zulässigen aktiven Werte an. Wenn dieser Wert z. B. auf „3“ gesetzt ist, werden nur die letzten drei erfassten Werte gespeichert, und alle vorhergehenden Werte werden verworfen. Beachten Sie, dass beim Senden von mehreren Werten innerhalb eines Treffers für dieselbe Listenvariable und wenn Sie einen Höchstwert festgelegt haben, jeder Wert mit demselben Zeitstempel versehen wird und nicht sicher ist, welcher Wert gespeichert wird.

   Maximal 250 Werte werden gleichzeitig pro Besucher gespeichert. Wenn 250 Werte pro Besucher überschritten werden, so werden die letzten 250 Werte verwendet. Der Ablauf dieser Werte basiert auf dem für die Variable konfigurierten Ablauf.

   Die Höchstwert-Einstellung kann dazu verwendet werden, die Attribuierung auf eine bestimmte Anzahl von Werten zu begrenzen. Wenn eine Listenvariable auf der ersten Seite eines Besuchs z. B. auf „A,B,C“ und auf der nächsten Seite auf „X,Y,Z“ gesetzt ist, wird die Attribuierung basierend auf der Zuordnung auf diese sechs Werte verteilt. Wenn Sie die Attribuierung nur auf „X,Y,Z“ begrenzen möchten, können Sie den Höchstwert auf „3“ setzen.

Um Listenvariablen einzurichten oder zu bearbeiten, navigieren Sie zu **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL Report Suites]** &gt; **[!UICONTROL Einstellungen bearbeiten]** &gt; **[!UICONTROL Konversion]** &gt; **[!UICONTROL Listenvariablen]**.

**Implementierungsbeispiele** {#section_564AFE6A2F524BFEB372EC0F7FEBA656}

In den folgenden Beispielen wird ein Komma als Trennzeichen für Werte verwendet.

**Definieren eines einzelnen Werts in einer Listenvariable:**

```js
s.list1="Cat";
```

**Übergeben von mehreren Werten:**

```js
s.list2="Tabby,Persian,Siamese"; 
s.list1="Product 1,Product 2,Product 3";
```

**Zuweisung des Umsatzes zu einer Listenvariable:**

```js
//Define this code on the landing page: 
s.list3="Top Banner Ad,Side Bar Ad,Internal Campaign 1"; 
 
//Have these variables fire on the purchase confirmation page: 
s.products=";Kitten;1;50" 
s.events="purchase";
```

Dieses Ergebnis zeigt drei Zeileneinträge mit jeweils 50 USD Umsatz an (Top Banner Ad, Side Bar Ad und Internal Campaign 1). Beachten Sie, dass bei der Gesamtsumme dieses Berichts der Umsatz dedupliziert wird, daher würde die Gesamtsumme auch 50 USD betragen.

**Zuweisung des Umsatzes zu einer Listenvariable, die während eines Besuchs mehrmals festgelegt wurde:**

**Zuordnung**: Vollständig

**Ablauf**: Besuch

<table id="table_09E1879B44624A858555449E2DC74E69"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Seite </th> 
   <th colname="col2" class="entry"> s.list1 </th> 
   <th colname="col3" class="entry"> s.events/s.products </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Seite 1 </td> 
   <td colname="col2"> <code> s.list1="value1,value2,value3"; </code> </td> 
   <td colname="col3"> (Nicht festgelegt) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Seite 2 </td> 
   <td colname="col2"> <code> s.list1="value4,value5,value6"; </code> </td> 
   <td colname="col3"> <p> <code> s.events="purchase"; </code> </p> <p> <code> s.products=";product;1;200" </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ergebnis**: Der Einkauf wird in allen Werten in der Listenvariablen1, die während des Besuchs festgelegt wurden (value1, value2, value3, value4, value5, value6), vollständig gutgeschrieben.

## maxDelay {#concept_B355038C3B094BB68C0DC6C80F9FE5B0}

Die Variable „s.maxDelay“ dient hauptsächlich in Genesis DFA-Integrationen zur Bestimmung der Timeout-Zeitdauer beim Herstellen von Verbindungen zum DFA-Host. Wenn Adobe innerhalb des in der „“-Variablen festgelegten Zeitraums keine Antwort von DFA-Servern erhält, wird die Verbindung abgebrochen und die Daten werden normal verarbeitet. Diese Variable implementieren Sie, wenn es bei den DFA-Antwortzeiten der einzelnen Seiten zu Problemen kommt. Es empfiehlt sich, diesen Wert versuchsweise zu ändern, um einen optimalen Timeout-Wert zu finden.

<!-- 

maxDelay.xml

 -->

**Implementierungsbeispiel**

```
s.maxDelay="750";
```

**Eigenschaften**

* Diese Variable ist eine optionale Ereignismetrik, die über das auf Ihrer Site implementierte JavaScript aufgefüllt wird.
* Wenn der DFA-Host nicht innerhalb der angegebenen Zeitdauer antwortet, wird das für Timeouts vorgesehene Ereignis (das per Genesis-Integrations-Assistenten zugewiesen wird) ausgelöst.
* Die Variable darf nur einen numerischen Wert enthalten.
* Die Zeitdauer wird in Millisekunden angegeben.
* Wenn Sie die Wartezeit erhöhen, können mehr DFA-Daten gesammelt werden, es steigt aber auch das Risiko, Analytics-Trefferdaten zu verlieren.

   Der Verlust von Analytics-Trefferdaten würde auftreten, wenn der Benutzer während des *`s.maxDelay`*-Zeitraums von der Seite weg navigiert.

* Bei einer niedrigeren Wartezeit sinkt das Risiko, Analytics-Trefferdaten zu verlieren, dabei kann es jedoch auch zu einer Verringerung der mit den Trefferdaten gesendeten DFA-Daten kommen.

   Das Löschen von DFA-Integrationsdaten erfolgt, wenn der *`s.maxDelay`*-Zeitraum nicht genügend Zeit für die Reaktion des DFA-Hosts bietet.

> [!NOTE] Adobe hat keine Kontrolle über die Antwortzeiten von DFA. Sollten bei Ihnen Probleme auftreten, die auch nach einer (vernünftigen) Anhebung der maximalen Wartezeit nicht verschwinden, wenden Sie sich an den DFA-Konto-Administrator Ihrer Organisation.

## mediaLength {#concept_F52B1670122C4461824223E525307060}

Die Variable gibt die Gesamtlänge des Mediums an, das abgespielt wird.

<!-- 

mediaLength.xml

 -->

<table id="table_B1AE8A9DF9D545C2965CDB2DB6C2969B"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Für die gesamte pev3-Anforderung gibt es keine Größenbeschränkung – stattdessen gilt die Längenbeschränkung des jeweiligen Browsers für URLs. </td> 
   <td> pev3 </td> 
   <td> Besuchszeit für Video; <p>Angezeigte Videosegmente </p> </td> 
   <td> Keine </td> 
  </tr> 
 </tbody> 
</table>

**Syntax und mögliche Werte** {#section_FEC1B01FDD234ACEB63C0558BEEB5CBC}

**Bei Einsatz von autoTrack:**

Bei Verwendung von [!UICONTROL s.Media.autoTrack] muss die Variable [!UICONTROL mediaLength] nicht explizit implementiert werden. Sie wird vom AppMeasurement für JavaScript-Code automatisch ermittelt.

**Manuelle Verfolgung:**

Syntax:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName)
```

Mögliche Werte:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

**Beispiele** {#section_048B2D31BB584647A5D335AE94E5A599}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
Resulting pev3 parameter syntax: pev3= [Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]  
  
```

```js
Possible pev3 values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32
```

**Probleme, Fragen und Tipps** {#section_1CEDC78FEF4940E9BC02A2AF1EE2FB01}

* Sie müssen die Methoden für die Medienverfolgung nur dann aufrufen, wenn der Player nicht mittels „[!UICONTROL s.Media.autoTrack] = true“ verfolgt werden kann.
* Beim Verfolgen von Medien ohne den Einsatz von [!UICONTROL autoTrack] müssen Sie daran denken, die Länge in Sekunden festzulegen.

## mediaName {#concept_A4CB1782DE244C23BA6CBB5E806DDE6A}

Diese Variable gibt den Namen des Video- oder Medienelements an.

<!-- 

mediaName.xml

 -->

Sie ist nur über die [!UICONTROL Dateneinfüge-API] und [!UICONTROL Vollständige Verarbeitung von Datenquelle] verfügbar.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 64 KB | pev3 | Videos, Nächster Videofluss, Vorheriger Videofluss, Angezeigte Videosegmente, Besuchszeit für Video | Keine |

**Syntax und mögliche Werte** {#section_F97A2253BBD24FEBBC225F233A319F5D}

**Bei Einsatz von autoTrack:**

Bei Verwendung von [!UICONTROL s.Media.autoTrack] muss die *`mediaName`*-Variable nicht explizit implementiert werden. Sie wird vom AppMeasurement für JavaScript-Code automatisch ermittelt.

**Manuelle Verfolgung:**

Syntax:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName) 
```

```js
s.Media.play(mediaName,mediaOffset)
```

```js
s.Media.stop(mediaName,mediaOffset)
```

```js
s.Media.close(mediaName)
```

Mögliche Werte:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

```js
s.Media.close("de_bofr_1045Making_400k")
```

**Beispiele** {#section_4B9584265B1A47289818141B2A88021D}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230") 
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

```js
s.Media.close("de_bofr_1045Making_400k")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]  
  
```

```js
Possible pev3 Values: 
  pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 
  11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32  
  
```

**Probleme, Fragen und Tipps** {#section_941A445BB52E4063B0F6920E61BB90DE}

* Sie müssen die Methoden für die Medienverfolgung nur dann aufrufen, wenn der Player nicht mittels „[!UICONTROL s.Media.autoTrack] = true“ verfolgt werden kann.
* Diese Variable wird als mySQL TEXT-Variable im Gegensatz zu VARCHAR(100) gespeichert.

## mediaPlayer {#concept_1932756C093B4B2FBA0484E5A58EF927}

Diese Variable gibt an, mit welchem Player ein Video- oder Medienelement wiedergegeben wird.

<!-- 

mediaPlayer.xml

 -->

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | pev3 | Video-Player | Keine |

**Syntax und mögliche Werte** {#section_EAA55A3A45B5405F903E3BE6ACAB143F}

**Bei Einsatz von autoTrack:**

```js
s.Media.playerName = "My Custom Player Name"  //configure player name in global JavaScript or ActionSource
```

**Manuelle Verfolgung:**

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName)
```

Mögliche Werte:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

**Beispiele** {#section_64967E1333D542CCB6CF62F0A1E0EF88}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers] 
```

```js
Possible pev3 Values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32
```

**Probleme, Fragen und Tipps** {#section_0020E031338F4A4880B9AC5B9A85BEF5}

Sie müssen die Methoden für die Medienverfolgung nur dann aufrufen, wenn der Player nicht mittels „s.Media.autoTrack = true“ verfolgt werden kann.

## mediaSession {#concept_19E6C850C3244CB6973140709BDCB0B9}

Diese Variable gibt an, welche Segmente eines Video- oder Medienelements abgespielt wurden.

<!-- 

mediaSession.xml

 -->

<table id="table_8681473270FE44DFBBCCC0FBA6737104"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 255 Byte </td> 
   <td> pev3 </td> 
   <td> Besuchszeit für Video <p>Angezeigte Videosegmente </p> </td> 
   <td> Keine </td> 
  </tr> 
 </tbody> 
</table>

**Syntax und mögliche Werte** {#section_9A63266633C4427CB4A6549E4D887B85}

**Bei Einsatz von autoTrack:**

Bei Verwendung von [!UICONTROL s.Media.autoTrack] muss die *`mediaName`*-Variable nicht explizit implementiert werden. Sie wird vom AppMeasurement für JavaScript-Code automatisch ermittelt.

**Manuelle Verfolgung:**

Syntax:

```js
s.Media.open(mediaName,mediaLength,mediaPlayerName) 
```

```js
s.Media.play(mediaName,mediaOffset)
```

```js
s.Media.stop(mediaName,mediaOffset)
```

Mögliche Werte:

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230") 
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

**Beispiele** {#section_3446EC37E017407FA3F43C9BDAEA0B85}

```js
s.Media.open("de_bofr_1045Making_400k", "414","Windows Media Player 11.0.5721.5230") 
```

```js
s.Media.play("de_bofr_1045Making_400k", "0")
```

```js
s.Media.play("de_bofr_1045Making_400k", "414")
```

```js
Resulting pev3 parameter syntax: pev3=[Asset Name]--**--[Total length of asset]--**--[Player name]--**--[Total seconds consumed]--**--[Timestamp]--**--[Chronological record of all starts and stops along with accompanying markers]
```

```js
Possible pev3 Values: pev3=de_bofr_1045Making_400k--**--414--**--Windows Media Player 11.0.5721.5230--**--288--**--1207893838--**--S0E0S0E256S0E32 
```

**Probleme, Fragen und Tipps** {#section_1BCEB037AB724B6EBE87420BD3604B88}

Sie müssen die Methoden für die Medienverfolgung nur dann aufrufen, wenn der Player nicht mittels „[!UICONTROL s.Media.autoTrack] = true“ verfolgt werden kann.

## Media.trackEvents {#concept_B1C5FF6C437949EBA5D52040AC6BB6D9}

Die variable „“ gibt an, welche Ereignisse bei einem Medientreffer gesendet werden sollen.

<!-- 

media_trackEvents.xml

 -->

Dies gilt nur bei JavaScript und [!UICONTROL ActionSource].

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | s.Media.trackEvents="None" |

**Syntax und mögliche Werte** {#section_66A978EF56914BEAAE73359A268A1B4A}

Ereignisnamen, wie „event1“ oder „purchase“.

**Beispiele** {#section_140A55D80EA24011954F9383CF312237}

```js
s.Media.trackEvents="event1,purchase"
```

**Probleme, Fragen und Tipps** {#section_030B11C64EE84D46A85CA550DB732D28}

Achten Sie darauf, dass in [!UICONTROL trackVars] der Wert „events“ steht, wenn diese Variable einen Wert hat.

## Media.trackVars {#concept_4350CA9A892148AE93C8133AB3B4BEA4}

Die variable „“ gibt an, welche Variablen bei einem Medientreffer gesendet werden sollen.

<!-- 

media_trackVars.xml

 -->

Dies gilt nur bei JavaScript und [!UICONTROL ActionSource].

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | s.Media.trackVars="None" |

**Syntax und mögliche Werte** {#section_7374684A7EB34AE685E8C40A66CFD289}

Variablennamen wie [!UICONTROL propN], *`eVarN`*, *`events`*, *`channel`* usw.

**Beispiele** {#section_48653222ABA14AB0A3C4471659971FAA}

```js
s.Media.trackVars="prop2,events,eVar3"
```

**Probleme, Fragen und Tipps** {#section_615AE1B696124B00B78F651B03813EAB}

* Selbst wenn „eVar3“ in [!UICONTROL trackVars] angegeben ist, wird es mit dem Medientreffer gesendet.

## mobile {#concept_0CEE045F57B444138C0EAA015FC7EA70}

Die Variable „“ steuert, in welcher Reihenfolge Cookies und Abonnenten-IDs zum Identifizieren von Besuchern eingesetzt werden.

<!-- 

mobile.xml

 -->

Siehe [Mobilfunkprotokolle](../../../implement/js-implementation/c-additional-libraries/network-protocols.md#concept_2425537FC9CB45DD868B5FA2298B6CAC).

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | /5/ oder /1/ im Pfad der Bild-URL | Keine | Keine |

**Syntax und mögliche Werte** {#section_7F1C58090C454882BA9D3D66C9263A76}

```js
s.mobile="any_string" //subscriber id used first, produces /5/ in path of image url 
s.mobile=""  // if set to an empty string or not set at all, cookies used first, produces /1/ in path of image url 
```

**Probleme, Fragen und Tipps** {#section_06CD5CB4EF1E4B9FBE3B9D1F18AAFA30}

Verwenden Sie besucherübergreifende Identifikation, um mögliche Spitzen im Besucher-Traffic bei der Verwendung der Variable *`s.mobile`* mit der JavaScript-Cookie-Implementierung zu vermeiden.

## pageName {#concept_5827B499DAC34B5D8445F9D9140CC328}

Die Variable „“ enthält den Namen von jeder Seite Ihrer Website.

<!-- 

pageName.xml

 -->

<table id="table_0D09BAEC2FFD43F7905ED3649B3F8E05"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 100 Byte </td> 
   <td> pageName </td> 
   <td> <p>Seiten </p> <p>Pfade </p> </td> 
   <td> Seiten-URL </td> 
  </tr> 
 </tbody> 
</table>

Die Variable *`pageName`* sollten Werte stehen, die für die Benutzer in Ihrem Unternehmen intuitiv verständlich sind. In den meisten Fällen ist der *`pageName`*-Wert nicht die URL oder der Pfad zur Datei. Übliche *`pageName`*-Werte umfassen zum Beispiel „Homepage“, „Checkout“, „Vielen Dank für Ihren Einkauf“ oder „Registrierung“.

Achten Sie darauf, dass in „pageName“ oder anderen Variablen keine Zeichen für Zeilenumbrüche, Gedankenstriche (em- oder en-Dashes) oder HTML-Zeichen enthalten sind. Zeilenumbrüche werden von manchen Browsern gesendet, von anderen nicht – für Analytics wären das dann zwei unterschiedliche Seitennamen. Bindestriche werden in vielen Textverarbeitungen und E-Mail-Clients noch während der Eingabe automatisch in lange oder kurze Gedankenstriche umgewandelt. Da lange oder kurze Gedankenstriche in Analytics-Variablen nicht zulässig sind (wie alle ASCII-Zeichen mit einer Nummer über 127), würde Analytics bei solch einem unzulässigen Seitennamen stattdessen die URL angeben.

Wenn *`pageName`* leer ist, wird die URL als Seitenname angegeben. Das Leerlassen von *`pageName`* ist meist problematisch, da die URL bei einer Seite nicht immer gleich bleibt (so sind z. B. `www.mysite.com` und `mysite.com` zwar unterschiedliche URLs, aber es ist die gleiche Seite).

**Syntax und mögliche Werte** {#section_7A61EE70F1A84D26B414404998C84BA8}

Die Variable *`pageName`* sollte einen für geschäftliche Benutzer von Analytics verständlichen Bezeichner enthalten.

```js
s.pageName="page_name"
```

*`pageName`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_8BB4F86F84E246A08B72DEC47FFC0765}

```js
s.pageName="Search Results" 
```

```js
s.pageName="Standard Offer List"
```

**Konfigurationseinstellungen** {#section_58CBC68C805344A999EB47455FEBA8D5}

Administratoren haben die Möglichkeit, mit dem Tool Seiten benennen den Seitennamen zu ändern, der in [!UICONTROL Analytics] angezeigt wird. Das kann jedoch gefährlich sein und negative Folgen in Berichten haben. Bitte wenden Sie sich zuerst an den Adobe-Kundendienst, bevor Sie das Tool [!UICONTROL Seiten benennen] verwenden.

**Probleme, Fragen und Tipps** {#section_BB41DC9682C34385B9CAA80D5257C113}

Vergewissern Sie sich, dass *`pageName`* keine unzulässigen Zeichen enthält.

## pageType {#concept_F67870238EF74491B5D3909A33CDB985}

Die Variable „“ dient nur zur Angabe einer Fehlerseite für den HTML-Fehler 404 (Seite nicht gefunden).

<!-- 

pageType.xml

 -->

<table id="table_0492B136E9D14070A6CA49ED534BCA4C"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> 20 Byte </td> 
   <td> pageType </td> 
   <td> Pfade &gt; Seiten &gt; Seiten <p>nicht gefunden </p> </td> 
   <td> "" </td> 
  </tr> 
 </tbody> 
</table>

The *`pageType`* variable captures the errant URL when a 404 Error page is displayed, which allows you to quickly find broken links and paths that are no longer valid on the custom site. Richten Sie die Variable *`pageType`* auf der Fehlerseite genau wie unten dargestellt ein.

Verwenden Sie auf 404-Fehlerseiten nicht die Variable „pageName“. Die Variable *`pageType`* wird nur für die 404-Fehlerseite verwendet.

Die 404-Fehlerseite ist in den meisten Fällen eine statische Seite, die fest einprogrammiert ist. In solchen Situationen ist es wichtig, dass als Verweis auf die JS-Datei ein entsprechender globaler oder relativer Pfad/Verzeichnis festgelegt ist.

**Syntax und mögliche Werte** {#section_C1C59968226446559B05F6EE7374D525}

Der einzige zulässige Wert von *`pageType`* ist „errorPage“, wie unten dargestellt.

```js
s.pageType="errorPage"
```

**Beispiele** {#section_6CE22FCB835B4A19B633B7F67E73A115}

```js
s.pageType="errorPage"
```

**Konfigurationseinstellungen** {#section_3B304A6D3A6C48F2BE90B4DA92A39DDB}

Keine

**Probleme, Fragen und Tipps** {#section_943681AB01FE47BEAC72E93CB60C53C8}

Wenn Sie andere Server-seitige Fehler erfassen möchten (z. B. Fehler aus der 500-Reihe), speichern Sie die Fehlermeldung in einer Prop und setzen Sie in der Variable *`pageName`* den Wert `500 Error: <URL>`, wobei `<URL>` die angeforderte URL ist. Auf diese Weise können Sie in [!UICONTROL Pfadsetzungsberichten] erkennen, welche Pfade bei Benutzern zu Fehlern der 500-Reihe geführt haben. Die vom Server angegebene Fehlermeldung wird in der Eigenschaftsvariablen erklärt.

## pageURL {#concept_A15F710CD0174297A2286BF3E7452113}

Die Variable „“ überschreibt die tatsächliche URL der Seite.

<!-- 

pageURL.xml

 -->

In seltenen Fällen kann es vorkommen, dass die URL der Seite nicht die ist, die in Analytics-Berichten aufgeführt wird.

<table id="table_D4DC6B476FFD4BEEB36A5C6B2D026255"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> Keine Einschränkung* </td> 
   <td> <p>G </p> </td> 
   <td> Datenverkehr &gt; Segmentierung &gt; Bevorzugte Seitenpfade </td> 
   <td> „Seiten-URL“ </td> 
  </tr> 
 </tbody> 
</table>

> [!NOTE] Adobe erlaubt *`pageURL`*-Werte von bis zu 64.000. Bei einigen Browsern gibt es eine Größenbeschränkung bei URLs von Bildanforderungen. Um das Abschneiden von anderen Daten zu verhindern, werden Seiten-URLs, die länger als 255 Byte sind, geteilt, wobei die ersten 255 Byte im Parameter `g=` und die verbleibenden Bytes später in der Abfragezeichenfolge im Abfrageparameter `-g=` integriert werden.

**Syntax und mögliche Werte** {#section_22AF3BF7C2F743549967B0C760A095C0}

Die Variable *`pageURL`* muss eine gültige URL mit einem gültigen Protokoll sein. Die Domäne wird zwangsweise in Kleinbuchstaben umgewandelt, bevor sie in Berichte aufgenommen wird. Die Abfragezeichenfolge kann je nach den Einstellungen in Analytics möglicherweise gekürzt sein.

```js
s.pageURL="proto://domain/path?query_string"
```

Als Seiten-URL sind nur URL-kompatible Zeichen zulässig.

> [!NOTE] Es wird dringend empfohlen, sich vor der Verwendung der Variable *`pageURL`* für benutzerdefinierte Zwecke an Ihren Adobe-Berater oder die Kundenunterstützung zu wenden.

**Beispiele** {#section_45158FDA3F8F4574BDEB5CBC9F7E6C97}

```js
s.pageURL="https://mysite.com/home.jsp?id=1224" 
```

```js
s.pageURL="https://www.mysite.com/"
```

**Konfigurationseinstellungen** {#section_A8F77DAD88164528ACC5C16C066B47DF}

Keine

## plugins {#concept_B570F04FEDA34EB7A9826687FE633953}

Die im Browser installierten werden bei Netscape- und Mozilla-basierten Browsern in der „plugins“-Variablen aufgelistet.

<!-- 

plugins.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| p | Erkannte Plug-ins | IE Tab-Plug-in, QuickTime-Plug-in 7.1.6, Mozilla-Standard-Plug-in, iTunes Application Detector, Adobe Acrobat, ActiveTouch General Plugin Container, Shockwave Flash, Microsoft Office 2003, Java(TM) Platform SE 6 U1, Windows Media Player-Plug-in Dynamic Link Library, Microsoft® DRM, | Datenverkehr &gt; Technologie &gt; Plugins |

## „products“{#concept_A4007F6307E4419DAA65E1668A8FEBA2}

Die Variable „“ dient zur Nachverfolgung von Produkten und Produktkategorien (sowie von Kaufmenge und Kaufpreis). „Products“ wird normalerweise zusammen mit einem Warenkorbereignis oder einem Ereignis festgelegt.

<!-- 

products.xml

 -->

>[!IMPORTANT]
>
>Im Januar 2016 haben wir die Logik aktualisiert, mit der das *`prodView`*-Ereignis automatisch eingestellt wird, was passiert, wenn *`product`*, aber nicht *`event`* vorhanden ist. Diese Aktualisierung kann zu einer gesteigerten Anzahl an *`prodView`*-Ereignissen führen. *`prodViews`* nimmt nur zu, wenn:
>
>1. Die Ereignisvariable ausschließlich ein nicht erkanntes Ereignis, wie beispielsweise *`shoppingCart`* oder *`cart`* enthält, bei denen es sich nicht um gültige Ereignisse handelt.
   >
   >
1. Die Variable *`products`* nicht leer ist.
>
>
Als mögliche Nebenwirkung werden möglicherweise Merchandising-eVars, die durch *`prodView`*-Ereignisse ausgelöst werden, einem leeren *`product`* zugeordnet. Das ist jedoch nur dann der Fall, wenn die *`product list`* nur ein ungültiges Produkt enthält (z. B. ein Semikolon ohne angegebenes Produkt).

Die Variable *`products`* dient zur Verfolgung der Interaktionen von Besuchern mit Produkten auf einer Site. So kann zum Beispiel in der Variablen „products“ verfolgt werden, wie oft ein Produkt angezeigt, in den Warenkorb gelegt, ausgecheckt und gekauft wird. Außerdem können Sie mit der Variablen auch die relative Effizienz von Merchandising-Kategorien auf Ihrer Site verfolgen. Nachfolgend sind einige der häufigsten Szenarien für den Einsatz der Variablen „products“ aufgeführt.

Die Variable *`products`* sollte immer in Verbindung mit einem Erfolgsereignis festgelegt werden.

<table id="table_D5A11AFDDD364D0993D387906343DDF3"> 
 <thead> 
  <tr> 
   <th class="entry"> Maximale Größe </th> 
   <th class="entry"> Debug-Parameter </th> 
   <th class="entry"> Ausgefüllte Berichte </th> 
   <th class="entry"> Standardwert </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Die Zeichenfolge <span class="wintitle">Produkte</span> hat eine maximale Größe von 64.000. </p> </td> 
   <td> „products“ </td> 
   <td> Produkte <p>Kategorien (optional) </p> <p>Umsatz (optional) </p> <p>Einheiten (optional) </p> <p>Benutzerspezifische Ereignisse (optional) </p> <p>eVars (optional) </p> </td> 
   <td> " " </td> 
  </tr> 
 </tbody> 
</table>

**Syntax** {#section_ABA3682985E540E6AA67A510176CCFFC}

```js
"Category;Product;Quantity;Price;eventN=X[|eventN2=X2];eVarN=merch_category[|eVarN2=merch_category2]"
```

| Feld | Definition |
|---|---|
| Kategorie | Enthält die zugehörige Produktkategorie. In Version 15 können Produkte mit mehreren Kategorien verknüpft werden. Damit wird eine Einschränkung aus Version 14 aufgehoben. Wenn Sie eine Produktkategorie zuvor nicht aufgezeichnet haben, sollten Sie dieses Feld nun für Reports Suites ausfüllen, die in Version 15 vorhanden sind. |
| Produkt | (Erforderlich) Der Bezeichner, der zum Verfolgen eines Produkts dient. Anhand dieses Bezeichners wird der Bericht [!UICONTROL Produkte] aufgefüllt. Achten Sie darauf, bis zum Checkout-Prozess immer den gleichen Bezeichner zu verwenden. |
| Quantität | Die Anzahl der gekauften Artikel. Dieses Feld muss bei einem [!UICONTROL Kauf]ereignis festgelegt sein, das aufgezeichnet werden soll. |
| Preis | Bezieht sich auf die kombinierten Kosten der insgesamt gekauften Menge (Einheiten x individueller Stückpreis) und nicht auf den individuellen Preis. Dieses Feld muss bei einem [!UICONTROL Kauf]ereignis, das aufgezeichnet werden soll, festgelegt sein. |
| Ereignisse | Mit dem angegebenen Produkt verknüpfte Währungsereignisse. Siehe [Produktspezifische Währungsereignisse](../../../implement/js-implementation/c-variables/page-variables.md#section_F814DF053C0D463A97DA039E6323720C) und [Auf Bestellung bezogene Währungsereignisse](../../../implement/js-implementation/c-variables/page-variables.md#section_D06F76A8A1F8498EB1BD6D8C8B9D5BE0). |
| eVars | Merchandising eVar-Werte, die mit einem bestimmten Produkt verknüpft sind. Siehe [Merchandising-Variablen](/help/components/c-variables/c-merch-variables/var-merchandising.md). |

Die in der Variable *`products`* enthaltenen Werte basieren auf dem Typ des aufgezeichneten Ereignisses. Wenn Kategorien ausgelassen werden, ist das Trennzeichen zwischen Kategorie/Produkt (;) als Platzhalter erforderlich. Andere Trennzeichen sind nur erforderlich, wenn sie zum Hervorheben des aufzunehmenden Parameters notwendig sind, wie in den Beispielen auf dieser Seite dargestellt.

**Festlegen von „products“ mit anderen als einem „purchase“-Ereignis** {#section_D5E689D4AAE941EC851CA9B98328A4DE}

Die Variable *`products`* muss in Verbindung mit einem Erfolgsereignis festgelegt werden.

**Festlegen von „products“ mit einem „purchase“-Ereignis** {#section_618AAC96E7B541A7AABAA028E5F4E5C3}

Das *`purchase`*-Ereignis sollte auf die endgültige Bestätigung („Vielen Dank!“) des Bestellvorgangs gesetzt werden. Produktname, Kategorie, Menge und Preis werden alle in der Variablen *`products`* festgelegt. Obwohl die Variable *`purchaseID`* nicht erforderlich ist, wird ihre Verwendung ausdrücklich empfohlen, damit Bestellungen nicht doppelt entgegengenommen werden.

**Produktspezifische Währungsereignisse** {#section_F814DF053C0D463A97DA039E6323720C}

Wenn ein Währungsereignis einen Wert in der Variable *`products`* anstelle der Ereignisvariable erhält, gilt dies nur für diesen Wert. Dies ist nützlich, um produktspezifische Rabatte, den Produktversand und ähnliche Werte zu verfolgen. Beispiel: Wenn Sie Ereignis 1 konfigurieren, um den Produktversand zu verfolgen, kann ein Produkt mit einer Versandgebühr von 4,50 wie folgt angezeigt werden:

```js
s.events="event1" 
s.products="Footwear;Running Shoes;1;99.99;event1=4.50"
```

In diesem Beispiel wird der Wert 4,50 direkt mit dem Produkt „Running Shoes“ verknüpft. Wenn Sie event1 zum Produktbericht hinzufügen, wird „4,50“ für das Einzelelement „Running Shoes“ aufgeführt. Ähnlich wie beim Preis sollte dieser Wert die Summe für die aufgeführte Menge widerspiegeln. Wenn 2 Artikel mit einer Versandgebühr von jeweils 4,50 vorliegen, sollte event1 „9,00“ lauten.

**Auf Bestellung bezogene Währungsereignisse** {#section_D06F76A8A1F8498EB1BD6D8C8B9D5BE0}

Wenn ein Währungsereignis einen Wert in der Ereignisliste anstelle der Variable *`products`* erhält, gilt dies für alle Produkte in der Variable *`products`*. Dies ist nützlich, wenn Sie Rabatte, Versandkosten und ähnliche Werte, die für die gesamte Bestellung gelten, verfolgen möchten, ohne den Produktpreis zu ändern oder ihn separat in der Produktliste zu verfolgen.

Beispiel: Wenn Sie event10 so konfiguriert haben, dass es einen auftragsweiten Rabatt enthält, sieht ein Kauf mit 10 % Rabatt ungefähr so aus:

```js
s.events="purchase,event10=9.95" 
s.products="Footwear;Running Shoes;1;69.95,Running Essentials;Running Socks;10;29.50" 
s.purchaseID="1234567890"
```

In Währungsberichten ist der Gesamtwert nicht die Summe der Ereigniswerte der einzelnen Produkte, sondern der deduplizierte Gesamtwert des Ereignisses (in diesem Beispiel die Summe aller im Berichterstattungszeitraum gewährten Rabatte). Beispiel: „9,95“ würde sowohl für „Running Shoes“ als auch für „Running Socks“ aufgeführt werden, und die Summe wäre ebenfalls „9,95“.

> [!NOTE] Wenn ein Wert für dasselbe numerische/Währungs-Ereignis in der Variable *`products`* und in der Variable *`events`* angegeben ist, wird der Wert aus dem *`events`*-Wert verwendet.

**Probleme, Fragen und Tipps** {#section_D38FD0B79C0347B9AB4CF1632183DA2E}

* Die Variable *`products`* sollte immer in Verbindung mit einem [!UICONTROL Erfolgs]ereignis (Ereignisse) gesetzt werden. Wenn kein [!UICONTROL Erfolgs]ereignis angegeben ist, lautet das Standardereignis [!UICONTROL prodView].

* Entfernen Sie alle Kommas und Semikolons aus Produkt- und Kategorienamen, bevor diese in „products“ übernommen werden.
* Entfernen Sie alle HTML-Zeichen (Warenzeichen, Symbole für eingetragene Marken usw.).
* Entfernen Sie alle Währungssonderzeichen ($) aus dem Preis.

**Beispiele** {#section_FCC6EF43D3534ECB9A95CDB05820F564}

<table id="table_6F1334E73CE048A5AC0CC28B561C1B2D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <code> s.products="Category;ABC123" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products="Category2;ABC123,;ABC456" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products="Category3;ABC123;1;10" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.products="Category;ABC123;1;10,;ABC456;2;19.98" </code> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1" </code> <p> <code> s.products="Category;ABC123;;;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99,;ABC123;2;19.98;event1=1.99" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping|evar2=3 Stars" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping, ;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2,event3" </code> <p> <code> s.products="Category;ABC123;1;10;event1=1.99|event2=25;evar1=2 Day Shipping,;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping,;;;;event3=2.9;evar3=20% off" </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> s.events="event1,event2,event3=9.95" </code> <p> <code> s.products="Category;ABC123;,;ABC456;2;19.98;event1=1.99|event2=100;evar1=Ground Shipping,;;;;event3=2.9;evar3=20% off" </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## propN {#concept_0F10FA2DE69B4029A31EA5E9313AA254}

Mithilfe von Eigenschaftsvariablen ([!UICONTROL props]) werden benutzerdefinierte Berichte im [!UICONTROL Datenverkehrmodul] erstellt.

<!-- 

propN.xml

 -->

Eigenschaftsvariablen können als Zähler verwendet werden (um zu zählen, wie oft eine Seitenansicht gesendet wird), in Pfadsetzungsberichten oder in Korrelationsberichten.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | c1 - c75 | Benutzerspezifischer Traffic | "" |

**Syntax und mögliche Werte** {#section_4D3013AF2979426B9589CA2BB9D254CD}

```js
s.propN="value"
```

Für [!UICONTROL Eigenschafts]variablen gelten die gleichen Einschränkungen wie für alle normalen Variablen.

**Beispiele** {#section_FFBB916DA9F44B668D5FAB7C511F6182}

```js
s.prop2="editorial" 
```

```js
s.prop15="toy category"
```

**Konfigurationseinstellungen** {#section_25FDEB6ECA8242A2A44EE540C083078A}

Wenden Sie sich an den Adobe-Kundendienst, wenn Sie Fragen zu [!UICONTROL Besuchs]-, [!UICONTROL Besucher]- und [!UICONTROL Pfad]metriken bei [!UICONTROL Eigenschaft]svariablen haben.

## purchaseID {#concept_21937434E63F413CB469007623B933AE}

Die „“ verhindert, dass eine Bestellung in Berichten mehrmals gezählt wird.

<!-- 

purchaseID.xml

 -->

Wann immer das [!UICONTROL Kaufereignis] auf Ihrer Site verwendet wird, sollten Sie die Variable *`purchaseID`* verwenden.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 20 Byte | purchaseID | Konversion &gt; Einkäufe &gt; Umsatzkonversion | "" |

Wenn ein Besucher einen Artikel auf Ihrer Site einkauft, wird *`purchaseID`* auf der Seite „Vielen Dank!“ an der gleichen Stelle aufgefüllt, an der das [!UICONTROL Kauf]ereignis ausgelöst wird. Wenn *`purchaseID`* aufgefüllt ist, werden die Produkte auf der Seite „Vielen Dank!“ nur einmal pro *`purchaseID`* gezählt. Das ist überaus wichtig, da viele Besucher die Dankseite oder die Bestätigungsseite für Informationszwecke speichern werden. Die Variable *`purchaseID`* verhindert, dass bereits getätigte Einkäufe jedes Mal gezählt werden, wenn die gespeicherte Seite erneut angezeigt wird.

Zusätzlich dazu, dass die Kaufdaten nicht doppelt gezählt werden, verhindert *`purchaseID`* bei Verwendung, dass alle Konversionsdaten in Berichten doppelt gezählt werden.

**Syntax und mögliche Werte** {#section_E352CE2370D54BA69A368E1F63A9C32D}

```js
s.purchaseID="unique_id"
```

*`purchaseID`* darf maximal 20 Zeichen lang sein und nur normale ASCII-Zeichen enthalten.

**Beispiele** {#section_60A5C1EAF42F4611898CD6A4F4CF5A28}

```js
s.purchaseID="11223344" 
s.purchaseID="a8g784hjq1mnp3"
```

**Konfigurationseinstellungen** {#section_1808631C96674380BF9C4A6D9A2C568E}

Keine

**Probleme, Fragen und Tipps** {#section_F5D010F234ED43F19AD1FCD2CD64E060}

Die Variable *`purchaseID`* ermöglicht es, dass alle auf der Seite enthaltenen Konversionsvariablen in Berichten nur einmal gezählt werden.

## referrer {#concept_3D8E6A5D30DC4D92982EFA34D4C7F81B}

Mithilfe der Variablen „“ können verlorene Referrer-Informationen wiederhergestellt werden.

<!-- 

referrer.xml

 -->

Häufig werden serverseitige und JavaScript-Umleitungen eingesetzt, um Besucher an die richtigen Stellen weiterzuleiten. Beim Umleiten eines Browsers geht jedoch die ursprüngliche Verweis-URL verloren.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 255 Byte | R | Datenverkehr &gt; Suchmethoden Konversion &gt; Suchmethoden | document.referrer |

Viele Firmen setzen Umleitungen an zahlreichen Stellen auf ihren Websites ein. So kann zum Beispiel ein Besucher aus einem gebührenpflichtigen Suchergebnis einer Suchmaschine umgeleitet werden. Beim Umleiten eines Browsers geht die verweisende URL häufig verloren. Die Variable *`referrer`* kann verwendet werden, um den ursprünglichen *`referrer`*-Wert auf der ersten Seite nach einer Umleitung wiederherzustellen. *`referrer`* kann Server-seitig oder über JavaScript aus der Abfragezeichenfolge gefüllt werden.

Damit Analytics einen Referrer aufzeichnet, muss dieser korrekt formatiert sein, d. h., er muss im normalen URL-Format mit Angabe eines Protokolls und geeigneten Speicherorts formuliert sein.

**Syntax und mögliche Werte** {#section_A0365D76789C4F4A959E81FE5A9D491D}

```js
s.referrer="URL"
```

Im *`referrer`*. Stellen Sie sicher, dass die Zeichenfolge URL-kodiert ist (keine Leerzeichen).

**Beispiele** {#section_86FB1577670C4AA18BF3718F0832FCD4}

```js
s.referrer="https://www.google.com/search?q=search+string" 
s.referrer=<%=referrerVar%> // populated server-side  
if(s.getQueryParam('ref') 
s.referrer=s.getQueryParam('ref') 
```

**Konfigurationseinstellungen** {#section_7AAEF28A7CBC446984F32C0659EFBF8D}

Keine

**Probleme, Fragen und Tipps** {#section_B42BF7FBA1094FF9805707FEA810CFE1}

*`referrer`* muss wie eine normale URL aussehen und eine Angabe zum Protokoll enthalten.

## resolution {#concept_8CBDDBE710744A3AA09E6B1E1519BF30}

Die Variable „“ gibt die Bildschirmauflösung des Besuchers an, von dem die Webseite angezeigt wird.

<!-- 

resolution.xml

 -->

Diese Variable erhält ihren Wert nach dem Seiten-Code und bevor *`doPlugins`* ausgeführt wird.

> [!NOTE] Diese Variable sollte nur gelesen und nie geschrieben werden.

Sie dürfen diese Werte lesen und in Eigenschaftsvariablen/eVars kopieren, jedoch nie ändern. Diese Variable wird mit der Version H.11 der JavaScript-Datei neu eingeführt.

| Abfrageparameter | Wert | Beispiel | Betroffene Berichte |
|---|---|---|---|
| s | BxH | 1.680 x 1.050 | Datenverkehr &gt; Technologie &gt; Bildschirmauflösung |

## s_objectID {#concept_48B50DE6B7E546EBB4D187033F1CAF2B}

Die Variable ist eine globale Variable, die im [!UICONTROL onClick]-Ereignis eines Links festgelegt wird.

<!-- 

s_objectID.xml

 -->

Durch Erstellung einer eindeutigen Objekt-ID für einen Link oder eine Linkposition auf einer Seite können Sie das Tracking der Besucheraktivität verbessern oder [!UICONTROL Activity Map] zum Generieren von Berichten zum Linktyp oder zur Linkposition anstelle der Link-URL verwenden.

> [!NOTE] Bei Verwendung von s_objectID mit [Activity Map](https://marketing.adobe.com/resources/help/en_US/analytics/activitymap/activitymap-link-tracking-use-case.html)ist ein nachfolgender Semikolon (;) erforderlich.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | OID | [!UICONTROL Activity Map], [!UICONTROL ClickMap] | Die absolute URL eines angeklickten Links |

Für die Verwendung von *`s_objectID`* gibt es drei gängige Gründe:

* Zusammenfassen von Besucheraktivitäten, die sich im Laufe eines Tages häufig ändern
* Herausfiltern von Link-Aktivitäten, die [!UICONTROL Activity Map] kombiniert.
* Verbessern der Genauigkeit der [!UICONTROL Activity Map]-Datenberichterstellung.

**Aggregieren von Klicks auf extrem dynamische Links** {#section_BA730A0393B149DDBCAA272C3C23A1C5}

Wenn Ihre Website sehr dynamisch ist und sich die Links auf einigen Seiten im Laufe des Tages ändern, kann *`s_objectID`* verwendet werden, um die Position eines Links auf der Seite zu identifizieren. Wenn *`s_objectID`* auf „links oben 1“ oder „links oben 2“ gesetzt wird, was beispielsweise den ersten Link oben links auf der Seite darstellt, werden alle Links, die an diesem Ort erscheinen (bzw. die den gleichen Wert wie *`s_objectID`* haben), zusammen mit der Besucher-ClickMap gemeldet. Wenn Sie *`s_objectID`* nicht verwenden, wird Ihnen zwar angezeigt, wie oft auf einen bestimmten Link geklickt wurde, Sie können jedoch nicht mehr erkennen, wie alle anderen Links an dieser Stelle von Besuchern verwendet wurden.

**Unterscheidung zusammengefasster Klicks** {#section_1AE91FB8A2D3423CBE064ACF02FEEA47}

Wenn die Variable *`pageName`* auf Ihrer Site verwendet wird, um den Abschnitt oder die Vorlage anzuzeigen, den/die ein Besucher anzeigt, und nicht die spezifische Seite, die der Besucher anzeigt, können Sie Links mit *`s_objectID`* trennen, die in mehreren Versionen dieser Seitenvorlage angezeigt werden sollen. Wenn Sie zum Beispiel über eine Vorlagenseite für alle Produkte auf Ihrer Site verfügen, enthält diese Vorlage sehr wahrscheinlich für alle Seiten einen Link zu Ihrer Homepage und zu einem Suchfeld. Wenn Sie sehen möchten, wie diese Links bei einzelnen Produkten genutzt werden (anstatt auf Basis einer Vorlage), können Sie in *`s_objectID`* einen produktspezifischen Wert eintragen (wie z. B. „Produkt 123789 Homepage“ oder „Produkt 123789 Suche“). Anschließend basieren [!UICONTROL Activity Map]-Berichte zu diesen Links auf einzelnen Produkten.

**Verbessern der[!UICONTROL Activity Map]-Genauigkeit** {#section_08B3406821294DCCABEEB99C90CF5C52}

In einigen Fällen werden andere Browser als Internet Explorer, Firefox, Netscape, Opera und Safari in Berichten nicht aufgeführt. Diese machen zwar nur einen kleinen prozentualen Anteil aus, tragen aber zu einigen Klicks und anderen Metriken mit bei. Verwenden Sie *`s_objectID`* in Links zur eindeutigen Identifizierung der Adressen des Browser-Berichtsproblems. Das folgende Beispiel zeigt, wie Sie Ihre Links zur Verwendung von *`s_objectID`*:

```js
<a href="/art.jsp?id=559" onClick="s_objectID='top left 1';">Article 559</a> 
<a href="/home.jsp" onClick="s_objectID='prod 123789 home page';">Home</a> 
```

**Syntax und mögliche Werte** {#section_85841DF9F06A4680953D9B2A884A1A5A}

In „s_objectID“ darf ein beliebiger Textbezeichner stehen.

```js
s_objectID="unique_id" 
```

*`s_objectID`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_33F119D532CA4ACAA3426253C42030BB}

```js
s_objectID="top left 2" 
```

```js
s_objectID="prod 123789 search"
```

**Konfigurationseinstellungen** {#section_95396657D55B41ECB66B83D0534EA827}

Keine

## server {#concept_BF77952603BA454BAFC9A0A81D06A7D2}

Die Variable „“ gibt entweder die Domäne einer Webseite an (damit Sie wissen, welche Ihrer Domänen besucht wird) oder den Server, von dem die Seite stammt (als Referenz für Lastenausgleichszwecke).

<!-- 

server.xml

 -->

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | server | Server | "" |

Wenn die Inhalte Ihrer Site aus mehreren Domänen stammen, kann mithilfe der Variable *`server`* auch verfolgt werden, welche dieser Domänen von Besuchern verwendet wird. Das folgende JavaScript trägt die Domäne der Seite in die „server“-Variable ein.

```js
s.server=window.location.hostname
```

Wenn Sie die „server“-Variable als Orientierungshilfe beim Lastenausgleich einsetzen, können Sie in dieser Variable einen Servernamen oder eine Nummer ablegen. Siehe folgendes Beispiel:

```js
s.server="server 14"
```

Der Bericht [!UICONTROL Bevorzugte Server] kann zwar als Orientierungshilfe beim Lastenausgleich genutzt werden, stellt jedoch keine präzise Messung von Serverlasten dar. So führt zum Beispiel Datenverkehr, der über die Schaltfläche „Zurück“ erzeugt wird, nicht zu einer Erhöhung der Serverlast, wird jedoch in Berichten angezeigt. Der Bericht gibt nicht an, von welchen Servern Bilder oder große Downloads stammen.

**Syntax und mögliche Werte** {#section_48E4B9BFEBFF4409A246D86EC0C0FB13}

```js
s.server="server_name"
```

Die Variable *`server`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_78B9EE3C27FB491384869E3D0BD503D6}

```js
s.server="server 18" 
s.server=window.location.hostname 
```

**Konfigurationseinstellungen** {#section_969DB379D5BD469FBEE8D505D3000E49}

Keine

**Probleme, Fragen und Tipps** {#section_42A28F9B01574F38891D9D54B411D8FE}

Die Variable *`server`* kann eingesetzt werden, um anzugeben, welche Domänen die beliebtesten sind oder von welchen Servern die meisten Seiten kommen.

## state {#concept_82295D22888947BF8B1C76182C635C6C}

Die Variablen „“ und „“ sind Konversionsvariablen.

<!-- 

state.xml

 -->

Sie erfassen wie eVars Ereignisse, sind jedoch nicht persistent. Die Variablen *`zip`* und *`state`* sind mit eVars vergleichbar, die unverzüglich ablaufen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 50 Byte | state | Konversion &gt; Besucherprofil &gt; Bundesstaat des Besuchers | "" |

Weil die Variablen *`state`* und *`zip`* sofort ablaufen, sind die einzigen Ereignisse, die ihnen zugeordnet sind, Ereignisse, die auf derselben Seite ausgelöst werden, auf der sie eingetragen sind. Wenn Sie beispielsweise die Variable *`state`* verwenden, um Konversionsraten nach dem Bundesstaat zu vergleichen, sollte die Variable *`state`* auf jeder Seite des Checkout erscheinen. Bei Konversions-Websites empfiehlt Adobe, die PLZ aus der Rechnungsadresse zu entnehmen. Sie können jedoch auch die Versandadresse verwenden (vorausgesetzt, zu der Bestellung ist nur eine Versandadresse vorhanden). Auf einer Medien-Website können *`zip`* und *`state`* zur Registrierung oder zum Anzeigen-Clickthrough-Tracking verwendet werden.

**Syntax und mögliche Werte** {#section_EDD1F5F9EDBC457898E61695F08C1744}

```js
s.state="state"
```

Bei der Variablen *`state`* sind keine besonderen Einschränkungen hinsichtlich Wert oder Format zu beachten. *`state`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_D181B163F79A41D199CA4C70765E583F}

```js
s.state="california" 
```

```js
s.state="prince edward island"
```

**Konfigurationseinstellungen** {#section_DB0D6DC3F4764AC59C11B10D27D2806C}

Keine

**Probleme, Fragen und Tipps** {#section_02F1620D0BB14AA6A838966FDB9A234F}

* Füllen Sie *`state`* auf jeder Seite auf, auf der ein relevantes Ereignis ausgelöst wird (z. B. auf jeder Seite des Checkout-Prozesses).
* Die Variablen *`zip`* und *`state`* verhalten sich wie eVars, die nach der Seitenansicht ablaufen.

## timestamp {#concept_D997A2FF4D134C80A614C0BC7A4D7507}

Mit dieser Variable können Sie den Zeitstempel von Treffern anpassen, ähnlich wie dies in den AppMeasurement-Bibliotheken für andere Plattformen erfolgt.

<!-- 

timestamp.xml

 -->

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 4 Byte | Datum/Zeit | Ist in Berichten nicht direkt angegeben. | Wird von Datenerfassungsservern festgelegt. |

**Syntax** {#section_1DF752B1202C4412A301AC7CC10874DF}

```js
s.timestamp="UNIX or ISO-8601 format timestamp"
```

Die Variable *`timestamp`* muss in dem Format stehen, das im nächsten Abschnitt näher beschrieben wird.

>[!IMPORTANT]
>
>Um die Variable *`timestamp`* verwenden zu können, muss die Kundenunterstützung zunächst die Unterstützung von Zeitstempeln für Ihre Report Suite aktivieren. Nachdem die Unterstützung von Zeitstempeln aktiviert wurde, müssen alle von JavaScript an diese Report Suite gesendeten Treffer manuell mit Zeitstempeln versehen werden (anhand von *`s.timestamp`*). Andernfalls werden die Treffer nicht aufgezeichnet.
>
>Des Weiteren müssen alle von JavaScript an diese Report Suite gesendeten Treffer manuell mit Zeitstempeln versehen werden (anhand von *`s.timestamp`*). Sie können Treffer mit Zeitstempel und Treffer ohne Zeitstempel nicht an ein und dieselbe Report Suite senden.
>
>Sie können auch die Einstellung [Zeitstempel optional](../../../implement/js-implementation/timestamps-overview.md#concept_1A7DF6F7BDA34467B51A6F61E08BB73F) verwenden, um mit Zeitstempel versehene Daten in derselben globalen Report Suite zu kombinieren, mit Zeitstempel versehene Daten aus einer App in eine globale Report Suite zu senden und Apps zu aktualisieren, um Zeitstempel zu ermöglichen, ohne eine neue Report Suite erstellen zu müssen.

**Formate für Zeitstempel** {#section_C12CBCECCD7047D38EF63A5800761CE9}

Zeitstempel müssen im UNIX-Format (d. h. Sekunden seit dem 1.Januar 1970) oder im ISO-8601-Format stehen, wobei für das ISO-8601-Format die folgenden Einschränkungen gelten:

* Sowohl das Datum als auch die Uhrzeit müssen durch ein „T“ getrennt angegeben werden
* Das Datum muss ein vollständiges Kalenderdatum sein (Jahr, Monat und Tag). . Wochentage und Datumsangaben mit Ordnungszahlen werden nicht unterstützt.
* Das Datum kann im standardmäßigen oder im erweiterten Format (`YYYY-MM-DD` oder `YYYYMMDD`) angegeben werden, es muss jedoch die Stunde und die Minute enthalten. Sekunden sind optional ( `HH:MM`, `HH:MM:SS`, `HHMM` oder `HHMMSS`). Es können Bruchteile von Minuten und Sekunden eingereicht werden, diese Bruchteile werden jedoch ignoriert.

* Es kann eine optionale Zeitzone im standardmäßigen oder im erweiterten Format (`±HH`, `±HH:MM`, `±HH`, `±HHMM` oder Z) angegeben werden.

UNIX-Zeitstempel werden weiterhin unterstützt (Sekunden seit dem 1.Januar 1970).

**Beispiele** {#section_FA19C53D70DE4CF2AF259A5B968B84C3}

```js
s.timestamp=Math.round((new Date()).getTime()/1000);
```

```js
s.timestamp="2012-04-20T12:49:31-0700";
```

Zulässige Zeitstempel im ISO-8601-Format sehen zum Beispiel wie folgt aus:

```
2013-01-01T12:30:05+06:00 
2013-01-01T12:30:05Z 
2013-01-01T12:30:05 
2013-01-01T12:30
```

**Konfigurationseinstellungen** {#section_5275D206F2CB4009B3681E8C4457124A}

Vor der Verwendung dieser Variablen muss eine Report Suite aktiviert werden, damit benutzerdefinierte Zeitstempel vom Kundendienst entgegengenommen werden können. Nach Aktivierung benutzerdefinierter Zeitstempel müssen alle an die Report Suite gesendeten Treffer über einen Zeitstempel verfügen (andernfalls werden sie verworfen).

**Probleme, Fragen und Tipps** {#section_EFDE8F67D13C4775A461E0B00D30AFD7}

* Zeitstempel dienen hauptsächlich zur Verfolgung von Offlinedaten auf mobilen Plattformen. Benutzerdefinierte Zeitstempel sind meist deaktiviert, es sei denn, es sollen gleichzeitig sowohl Web- als auch Offline-App-Daten in der gleichen Report Suite erfasst werden.
* Daten werden mit einem Zeitstempel versehen, wenn Offlinedaten im mobilen SDK aktiviert sind (Standardeinstellung) oder wenn eine Report Suite konfiguriert ist, Daten mit Zeitstempel zu akzeptieren. Offline erfasste Daten können Stunden oder Wochen nach dem Datum des ursprünglichen Ereignisses gesendet werden. Diese Treffer werden innerhalb der Analytics-Plattform einige Minuten oder Stunden länger als Treffer ohne Zeitstempel in die Warteschlange gestellt:

   * Bei Daten mit Zeitstempel, die in sehr kurzer Zeit gesendet werden, beträgt die wahrscheinliche Verzögerung 10-15 Minuten.
   * Bei Daten mit Zeitstempel, die von gestern gesendet wurden, beträgt die wahrscheinliche Verzögerung etwa 2 Stunden.
   * Bei Daten mit Zeitstempel, die älter als gestern gesendet werden, erhöht sich die tägliche Verzögerung um etwa 2 Stunden, höchstens jedoch um 48 Stunden.

## trackingServer {#concept_45EE91B1A99B4A37AFAEF1C0A8A6B02F}

Die Variable „“ dient in Erstanbieter-Cookie-Implementierungen zur Angabe der Domäne, in die die Bildanforderung und das Cookie geschrieben werden.

<!-- 

trackingServer.xml

 -->

Wird bei nicht sicheren Seiten verwendet. Wenn *`trackingServer`* definiert ist, werden keine Daten an „2o7.net“ gesendet. Wenn *`trackingServer`* nicht definiert ist, werden Daten an 112.2o7.net gesendet.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | "" |

Eine Liste mit den Adobe-Rechenzentren finden Sie [hier](https://helpx.adobe.com/analytics/kb/determining-data-center.html).

## trackingServerSecure {#concept_28132A2606E34A2F87BEC9E7ACADC7DD}

Die Variable „“ dient in Erstanbieter-Cookie-Implementierungen zur Angabe der Domäne, in die die Bildanforderung und das Cookie geschrieben werden.

<!-- 

trackingServerSecure.xml

 -->

Wird bei sicheren Seiten verwendet. Wenn *`trackingServerSecure`* nicht definiert ist, werden SSL-Daten an *`trackingServer`* gesendet.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | Keine | Keine | "" |

## transactionID {#concept_FBFA55E137E644A2BD97B41E92F6AFEF}

[!UICONTROL Integration-Data Sources] verwenden eine [!UICONTROL Transaktions-ID], um Offlinedaten mit einer Onlinetransaktion (z. B. Leads oder online generierte Einkäufe) zu verknüpfen.

<!-- 

transactionID.xml

 -->

Jede eindeutige an Adobe gesendete *`transactionID`* wird bei der Vorbereitung eines [!UICONTROL Data Sources]-Uploads von Offlineinformationen zu dieser Transaktion aufgezeichnet. Siehe [Data Sources](https://marketing.adobe.com/resources/help/en_US/sc/datasources/).

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 100 Byte | xact | Keine | "" |

**Aktivieren des Transaktions-ID-Speichers** {#section_3EA2C9DC9D4C4F0FBE4AB67981BCB52E}

Bevor *`transactionID`*-Werte aufgezeichnet werden, muss [!UICONTROL Transaktions-ID-Speicherung] für die im Report Suite Manager ausgewählte Report Suite aktiviert sein. Diese Einstellung nehmen Sie hier vor:

```
Analytics > Admin > Report Suites > Edit Settings > General > General Account Settings.
```

Ob bei einer Report Suite *`transactionID Storage`* aktiviert ist, sehen Sie hier:

```
Analytics > Admin > Data Sources > Manage
```

**Syntax und mögliche Werte** {#section_0C18329203DC45E989DBAE70C0FB4801}

```js
s.transactionID="unique_id"
```

*`transactionID`* sollte nur alphanumerische Zeichen enthalten. Wenn bei einem einzelnen Treffer mehrere [!UICONTROL transactionIDs] aufgezeichnet werden sollen, können Sie die einzelnen Werte mit einem Komma voneinander trennen.

**Beispiele** {#section_A4C1F0E54CB54AD7B86A22147E9B5FEF}

```js
s.transactionID="11123456"
```

```js
s.transactionID="lead_12345xyz"
```

```js
s.transactionID=s.purchaseID
```

**Probleme, Fragen und Tipps** {#section_4299BAD5D0154DBC88A9EF0E2C252BB4}

* Wenn die *`transactionID`*-Aufzeichnung nicht aktiviert ist, werden *`transactionID`*-Werte verworfen und stehen für die Verwendung mit [!UICONTROL Integrationsdatenquellen] nicht zur Verfügung. Stellen Sie sicher, dass auf der Seite, auf der *`transactionID`* gesetzt ist, eine Konversionsvariable oder ein Ereignis (eVar bzw. Ereignisvariable) festgelegt ist. Andernfalls werden keine Daten für *`transactionID`* aufgezeichnet.

* Wenn Sie [!UICONTROL transactionIDs] für mehrere Systeme wie Einkäufe und Interessenten aufzeichnen, stellen Sie sicher, dass der Wert in *`transactionID`* immer eindeutig ist. Zu diesem Zweck können Sie der ID eine entsprechende Zeichenfolge voranstellen (z. B. „Lead_1234“ oder „Einkauf_1234“). [!UICONTROL Integrationsdatenquellen] funktionieren nicht wie erwartet ([!UICONTROL Datenquellen]-Daten werden an die falschen Daten gebunden), wenn eine eindeutige *`transactionID`* zweimal erfasst wird.

* Standardmäßig werden *`transactionID`*-Werte 90 Tage lang gespeichert. Wenn die Offline-Interaktion länger als 90 Tage dauert, lassen Sie diese Zeitspanne vom Kundendienst verlängern.

> [!NOTE] Die Variable *`transactionID`* kann jedes beliebige Zeichen außer einem Komma enthalten. Sie sollte sich an der gleichen Stelle befinden, an der die Zeichenbegrenzung (100 Byte) angegeben ist. Bei Verwendung von Multi-Byte-Zeichen muss Multi-Byte-Zeichen-Unterstützung aktiviert werden, damit es nicht zu Problemen kommt, weil unerwartete Zeichen in *`transactionID`*.

## visitorID {#concept_CD273CC915CC4ABD8F52E4209FF9557E}

Besucher können anhand der Variablen „“ oder mittels IP-Adresse/Benutzeragent identifiziert werden.

<!-- 

visitorID.xml

 -->

*`visitorID`* kann bis zu 100 alphanumerische Zeichen lang sein und darf keine Bindestriche enthalten.

Wenn Sie ausdrücklich eine benutzerdefinierte ID einstellen, wird diese immer vor anderen ID-Methoden verwendet.

Die Reihenfolge der Verwendung lautet: s.visitorID &gt; s_vi &gt; s_fid &gt; IP/UA.

| ** Maximale Größe** | ** Debug-Parameter** | ** Ausgefüllte Berichte** | ** Standardwert** |
|---|---|---|---|
| 100 Byte | vid | Keine | "" |

**Syntax und mögliche Werte** {#section_5F768C7AE6824557997E92B295C09280}

```js
s.visitorID="visitor_id"
```

> [!NOTE] Die Variable *`visitorID`* darf keinen Bindestrich enthalten.

**Beispiele** {#section_F7F07FEFAC3644A5A084D166ACE1315E}

```js
s.visitorID="abc123"
```

**Konfigurationseinstellungen** {#section_582B376FE55C4BCA8F978E0F62B5DB54}

Keine

## visitorNamespace {#concept_8369DDB3830C4BF2905F1CFC8C8B0D92}

Anhand dieser Variablen wird die Domäne identifiziert, bei der Cookies gesetzt werden.

<!-- 

visitorNamespace.xml

 -->

Wenn *`visitorNamespace`* in Ihrer JavaScript-Datei verwendet wird, dürfen Sie sie weder löschen noch ändern. Wenn *`visitorNamespace`* sich ändert, können alle in Analytics gemeldeten Besucher zu neuen Besuchern werden. Der Besucherverlauf würde bei aktuellem und zukünftigem Datenverkehr unterbrochen werden. Ändern Sie diese Variable daher nie ohne vorherige Genehmigung von einem Adobe-Support-Mitarbeiter!

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| Keine | ns | Keine | "" |

Analytics verwendet ein Cookie, um Besucher Ihrer Site eindeutig zu identifizieren. Wenn *`visitorNamespace`* nicht verwendet wird, wird das Cookie 2o7.net zugeordnet. Wenn *`visitorNamespace`* verwendet wird, wird das Cookie einer Subdomain von 2o7.net zugeordnet. Die Cookies aller Besucher Ihrer Site sollten der gleichen Domäne oder Subdomäne zugeordnet sein.

Durch Einsatz der Variablen *`visitorNamespace`* soll verhindert werden, dass ein Cookie-Grenzwert von Browsern überschritten wird. In Internet Explorer gibt es ein Limit von 20 Cookies pro Domäne. Durch Einsatz der Variablen *`visitorNamespace`* vermeiden Sie Konflikte mit den Analytics-Cookies anderer Firmen.

**Syntax und mögliche Werte** {#section_EE247FE371784CA4B6058182181F3EA1}

Der Wert von *`visitorNamespace`* muss eine von Adobe angegebene Zeichenfolge aus ASCII-Zeichen sein (in der Kommas, Punkte, Leerzeichen oder Sonderzeichen unzulässig sind).

```js
s.visitorNamespace="company_specific_value"
```

**Besucher-Identifizierung über Report Suites** {#section_7AC5A97FC8C045DD8850245A62BB09F4}

Wenn Sie keinen `visitorNamespace` angeben, erhält jede Report Suite in Ihrem Unternehmen ein eigenes Besucher-ID-Cookie in der Schreibweise `s_vi_[random string]`. Wenn Sie `visitorNamespace` angeben, wird dasselbe `s_vi`-Cookie für alle Report Suites verwendet, die Daten an den angegebenen `trackingServer` senden. Vergewissern Sie sich bei der Implementierung von Multi-Suite-Tagging, dass Sie den Besucher-Namespace angeben, damit dasselbe Cookie von jeder Report Suite verwendet wird.

**Beispiele** {#section_89A95852AB9446E794AD3283B8800B09}

```js
s.visitorNamespace="company_name"
```

```js
s.visitorNamespace="Adobe"
```

**Konfigurationseinstellungen** {#section_1128A2531ECC43DFA6749ECC21F050A2}

Keine

## zip {#concept_C1DF93083553410DA36EAB61FBFDF69A}

Die Variablen „“ und „“ sind Konversionsvariablen.

<!-- 

zip.xml

 -->

Sie erfassen wie eVars Ereignisse, sind jedoch nicht persistent. Die Variablen *`zip`* und *`state`* sind mit eVars vergleichbar, die unverzüglich ablaufen.

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| 50 Byte | zip | Konversion &gt; Besucherprofil &gt; PLZ/Postleitzahlen | "" |

Since the *`state`* and *`zip`* variables expire immediately, the only events associated with them are events fired on the same page that are populated. Wenn Sie beispielsweise die Variable *`zip`* verwenden, um Konversionsraten nach der Postleitzahl zu vergleichen, sollte die Variable *`zip`* auf jeder Seite des Checkout erscheinen. Adobe empfiehlt, als Quelle für die Postleitzahlen die Rechnungsadresse zu verwenden. Sie könnten stattdessen auch die Versandadresse verwenden (vorausgesetzt, für die Bestellung ist nur eine einzige Versandadresse vorhanden). Auf einer Medien-Website können *`zip`* und *`state`* zur Registrierung oder zum Anzeigen-Clickthrough-Tracking verwendet werden.

**Syntax und mögliche Werte** {#section_5EDCFCAC8FC241D1B4CC777996858CD7}

```js
s.zip="zip_code"
```

Die Variable *`zip`* legt keine Wert- oder Formatbeschränkungen fest. *`zip`* unterliegt keinen Beschränkungen, die über die Standardbeschränkungen von Variablen hinausgehen.

**Beispiele** {#section_F25C0D0CC3C04B81892A662CD605C593}

```js
s.zip="92806"
```

```js
s.zip="92806-4115"
```

**Konfigurationseinstellungen** {#section_7987084EECC34DD38B643B94F82385CA}

Keine

**Probleme, Fragen und Tipps** {#section_E86774D5CE8B40EFA36353CDEE3A84D0}

* Füllen Sie [!UICONTROL zip] auf jeder Seite mit Werten, auf der ein relevantes Ereignis ausgelöst wird (z. B. auf jeder Seite des Checkout-Prozess).
* Die Variablen *`zip`* und *`state`* verhalten sich wie eVars, die nach der Seitenansicht ablaufen.

