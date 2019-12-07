---
description: Seitenvariablen werden direkt in Berichten ausgefüllt, z. B. pageName, List Props, List Variables usw.
keywords: Analytics Implementation
subtopic: Variables
title: Seitenvariablen
topic: null
uuid: null
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# visitorNamespace

Anhand dieser Variablen wird die Domäne identifiziert, bei der Cookies gesetzt werden.


<!-- 

visitorNamespace.xml

 -->

Wenn *`visitorNamespace`* in Ihrer JavaScript-Datei verwendet wird, dürfen Sie sie weder löschen noch ändern. Wenn *`visitorNamespace`* sich ändert, können alle in Analytics gemeldeten Besucher zu neuen Besuchern werden. Der Besucherverlauf würde bei aktuellem und zukünftigem Datenverkehr unterbrochen werden. Ändern Sie diese Variable daher nie ohne vorherige Genehmigung von einem Adobe-Support-Mitarbeiter!

| Maximale Größe | Debug-Parameter | Ausgefüllte Berichte | Standardwert |
|---|---|---|---|
| nicht angegeben | ns | nicht angegeben | "" |

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
