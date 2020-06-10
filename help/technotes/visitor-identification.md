---
description: Adobe setzt ein Cookie zur Verfolgung individueller Browser/Geräte ein.
keywords: Analytics Implementation
subtopic: Visitors
title: Unique Visitors identifizieren
topic: Developer and implementation
translation-type: tm+mt
source-git-commit: f7c2a366b409995c1fe790db97de5c708882ab3d
workflow-type: tm+mt
source-wordcount: '1913'
ht-degree: 96%

---


# Unique Visitors identifizieren

Adobe setzt ein Cookie zur Verfolgung individueller Browser/Geräte ein.

## Reihenfolge Analytics-Besucher-ID {#section_DE1DC9FC9B6D4388995B70E35B8BCDDF}

Adobe Analytics bietet verschiedene Mechanismen zur Identifizierung von Besuchern. Die folgende Tabelle listet verschiedene Methoden auf, mit denen ein Besucher in Analytics identifiziert werden kann (in der bevorzugten Reihenfolge):

| Verwendete Reihenfolge | Abfrageparameter (Erfassungsmethode) | Vorhanden, wenn |
|---|---|---|
| 1 | vid (s.visitorID) | s.visitorID festgelegt ist. |
| 2 | aid (s_vi-Cookie) | der Besucher über bestehendes s_vi-Cookie verfügt, bevor Sie den Besucher-ID-Dienst bereitgestellt haben, oder wenn Sie eine Schonfrist für die Besucher-ID konfiguriert haben. |
| 3 | mid (AMCV_-Cookie, der vom Experience Cloud-Besucher-ID-Dienst gesetzt wird) | der Browser des Besuchers Cookies (von Erstanbietern) akzeptiert. |
| 4 | fid (Ausweich-Cookie) | der Browser des Besuchers Cookies (von Erstanbietern) akzeptiert. |
| 5 | IP-Adresse, Benutzeragent, Gateway-IP-Adresse | der Browser des Besuchers keine Cookies akzeptiert. |

In vielen Szenarien sehen Sie möglicherweise 2 oder 3 verschiedene IDs für einen Aufruf, jedoch verwendet Analytics die erste vorhandene ID aus der vorigen Tabelle als offizielle Besucher-ID. Wenn Sie beispielsweise eine benutzerspezifische Besucher-ID festlegen (die im vid-Abfrageparameter enthalten ist), wird diese ID bevorzugt vor anderen IDs verwendet, die möglicherweise für denselben Treffer vorliegen.

>[!NOTE] Jede Analytics-Besucher-ID ist einem Besucherprofil auf Adobe-Servern zugewiesen. Besucherprofile werden nach einer Inaktivität von mindestens 13 Monaten gelöscht, unabhängig vom Ablauf der Besucher-ID-Cookies.

## Benutzerspezifische Besucher-ID

Sie können eine benutzerspezifische Methode implementieren, um Besucher zu identifizieren, indem Sie die Variable „s.visitorID“ festlegen.

Eine benutzerspezifische Besucher-ID kann auf Sites verwendet werden, bei denen Sie Besucher auf eindeutige Weise identifizieren können. So wird z. B. möglicherweise eine ID generiert, wenn sich ein Benutzer mit einem Benutzernamen und einem Passwort bei einer Website anmeldet.

Wenn Sie die [!UICONTROL Besucher-IDs] Ihrer Benutzer ableiten und verwalten können, stehen die folgenden Methoden zum Festlegen der ID zur Verfügung:

| Methode | Beschreibung |
|---|---|
| Variable [„s.visitorID“](../implement/vars/config-vars/visitorid.md) | Wenn JavaScript im Browser verwendet wird oder Sie eine andere AppMeasurement-Bibliothek verwenden, können Sie die Besucher-ID in einer Datenerfassungsvariablen festlegen. |
| Abfragezeichenfolgenparameter in der Bildanforderung | Bei dieser Option können Sie die [!UICONTROL Besucher-ID] über den Abfragezeichenfolgenparameter [!UICONTROL vid] in einer fest programmierten Bildanforderung an Adobe übergeben. |
| Dateneinfüge-API | Bei Geräten mit Wireless-Protokollen, die kein JavaScript akzeptieren, können Sie einen XML-Post mit dem XML-Element `<visitorid/>` von Ihren Servern an Adobe-Erfassungsserver senden. |
| Umschreiben der URL und VISTA | Einige Implementierungsarchitekturen bieten Unterstützung für das Umschreiben von URLs an, damit der Sitzungsstatus auch dann aufrechterhalten werden kann, wenn das Setzen eines Cookies nicht möglich ist. In solchen Fällen kann Adobe Engineering Services eine [!DNL VISTA]-Regel implementieren, die nach dem Sitzungswert in der URL der Seite sucht und diesen dann formatiert und in die [!UICONTROL visid]-Werte einsetzt. |
>[!CAUTION]
>**Benutzerspezifische Besucher-IDs müssen ausreichend granular/eindeutig sein:** Eine ungültige Implementierung benutzerspezifischer Besucher-IDs kann zu falschen Daten und schlechter Berichterstellung führen. Wenn die benutzerdefinierte Besucher-ID nicht eindeutig oder granular genug ist oder falsch auf einen allgemeinen Standardwert wie die Zeichenfolge „NULL“ bzw. „0“eingestellt ist, werden die Hits vieler verschiedener Besucher von Adobe Analytics als einzelner Besucher gewertet. Dies führt zu falschen Daten, da die Besucherzahlen zu niedrig sind und Segmente für diesen Besucher nicht richtig funktionieren. Eine nicht ausreichend granulare benutzerdefinierte Besucher-ID verhindert auch, dass die Daten ordnungsgemäß über Knoten im Analytics-Berichtscluster verteilt werden. In diesem Fall wird ein Knoten überlastet und kann Berichtsanforderungen nicht zeitnah verarbeiten. Schließlich schlägt die Berichterstellung für die Report Suite fehl.<br>Schlecht implementierte benutzerdefinierte Besucher-IDs wirken sich möglicherweise nicht sofort auf die Berichterstellungsleistung aus, da Analytics häufig unausgeglichene Daten aus mehreren Monaten verarbeiten kann. Im Laufe der Zeit kann ein schlecht implementierter benutzerdefinierter Besucher-ID-Wert jedoch so problematisch werden, dass Analytics die Verarbeitung für betroffene Report Suites deaktivieren muss.</br><br>Implementierer sollten die Richtlinie befolgen, wonach einem einzelnen benutzerdefinierten Besucher-ID-Wert nie mehr als 1 % des Traffics einer Report Suite zugerechnet werden sollte. Obwohl die Leitlinie von 1 % für die meisten Report Suites ausreicht, kann die tatsächliche Grenze, ab der die Berichtsleistung beeinträchtigt werden könnte, bei sehr großen Report Suites unter 1 % liegen.</br>

## Analytics-Besucher-ID

Wenn ein Benutzer Ihre Site besucht, wird ein beständiges Cookie vom Adobe-Webserver gesetzt, indem es in die HTTP-Antwort an den Browser aufgenommen wird. Dieses Cookie wird in der angegebenen Datenerfassungsdomäne gesetzt.

Wenn eine Anforderung an den Adobe-Datenerfassungsserver gesendet wird, wird geprüft, ob der Header das Besucher-ID-Cookie (`s_vi`) enthält. Wenn der Cookie in der Anforderung enthalten ist, wird er zur Identifizierung des Besuchers verwendet. Wenn der Cookie nicht in der Anforderung enthalten ist, generiert der Server eine Unique Visitor-ID, setzt diese als Cookie im HTTP-Antwort-Header, und sendet diesen mit der Anforderung zurück. Der Cookie wird im Browser gespeichert und bei nachfolgenden Besuchen auf der Website zurück zum Datenerfassungsserver gesendet, sodass der Besucher bei allen Besuchen identifiziert werden kann.

### Drittanbieter-Cookies und CNAME-Datensätze {#section_61BA46E131004BB2B75929C1E1C93139}

Einige Browser, wie Apple Safari, speichern keine Cookies mehr, die im HTTP-Header gesetzt sind von Domänen, die nicht mit der Domäne der aktuellen Website übereinstimmen (dies ist ein Cookie, das in einem Drittanbieterkontext verwendet wird, bzw. ein Drittanbieter-Cookie). Wenn Ihre Domäne z. B. `mysite.com` ist und sich Ihr Datenerfassungsserver unter der Domäne `mysite.omtrdc.net` befindet, wird der von `mysite.omtrdc.net` im HTTP-Header zurückgegebene Cookie möglicherweise vom Browser abgewiesen.

Um dies zu vermeiden, haben viele Kunden für ihre Datenerfassungsserver CNAME-Einträge als [Erstanbieter-Cookie-Implementierung](https://docs.adobe.com/content/help/de-DE/core-services/interface/ec-cookies/cookies-first-party.html) implementiert. Wenn ein CNAME-Eintrag so konfiguriert wurde, dass ein Hostname unter der Domäne des Kunden einem Datenerfassungsserver zugeordnet wird (z. B. die Zuordnung von `metrics.mysite.com` zu `mysite.omtrdc.net`), wird der Besucher-ID-Cookie gespeichert, da die Datenerfassungsdomäne nun mit der Domäne der Website übereinstimmt. Somit besteht zwar eine höhere Wahrscheinlichkeit, dass das Besucher-ID-Cookie gespeichert wird, es entsteht jedoch auch etwas Mehraufwand, da CNAME-Einträge konfiguriert und SSL-Zertifikate für Datenerfassungsserver verwaltet werden müssen.

### Cookies auf Mobilgeräten {#section_7D05AE259E024F73A95C48BD1E419851}

Wenn Mobilgeräte anhand von Cookies nachverfolgt werden, können Sie den Ablauf von Messungen anhand einiger Einstellungen anpassen. Die Lebensdauer von Cookies beträgt fünf Jahre, aber Sie können diesen Standardwert mit der Abfrageparametervariablen für die Lebensdauer von Cookies (`s.cookieLifetime`) andern. Mit der CDP-Abfragezeichenfolge `s.cookieDomainPeriods` können Sie den Cookie-Speicherort für CNAME-Implementierungen festlegen. Der Standardwert ist 2, sofern kein anderer Wert festgelegt wird, und der Standard-Speicherort ist „domain.com“. Bei Implementierungen, die keine CNAME-Einträge verwenden, befindet sich der Speicherort für den Besucher-ID-Cookie unter der Domäne „207.net“.

## Identitätsdienst

Der Identitätsdienst ersetzt den bisher verwendeten Analytics-Besucher-ID-Mechanismus und ist für [!UICONTROL Heartbeat]-Videomessungen, Analytics für Target sowie zukünftige zentrale Dienste und Integrationen von Experience Cloud erforderlich.

Die Produktdokumentation zu diesem Service finden Sie unter [Identitätsdienst](https://docs.adobe.com/content/help/de-DE/id-service/using/home.html).

## Mobile Geräte identifizieren

Die meisten Mobilgeräte akzeptieren Browser-Cookies. Wenn Geräte allerdings keine Cookies akzeptieren, werden Wireless-Geräte anhand einer anderen Methode eindeutig identifiziert.

Adobe hat eine Reihe von HTTP-Abonnenten-ID-Headern identifiziert, über die die meisten Mobilgeräte eindeutig identifiziert werden können. Diese Header enthalten oftmals die Telefonnummer des Geräts (in Klartext- oder Hashform) oder andere IDs. Die meisten aktuellen Geräte verfügen über einen oder mehrere der Header, anhand derer das Gerät eindeutig identifiziert werden kann, und alle Adobe-Datenerfassungsserver verwenden diese Header dann automatisch anstelle einer Besucher-ID.

In einer normalen Bildanforderung führt eine „1“ im Pfad (`/b/ss/rsid/1`) dazu, dass Adobe-Server ein GIF-Bild zurückgeben und versuchen, ein beständiges [!UICONTROL Besucher-ID]-Cookie (`AMCV_` oder `s_vi`) zu setzen. Wenn das Gerät allerdings basierend auf den HTTP-Headern als Mobilgerät erkannt wird, wird eine „5“ anstelle der „1“ übergeben. Dies gibt an, dass ein Bild im WBMP-Format zurückgegeben werden soll und dass unsere Liste mit bekannten Wireless-Headern (kein Cookie) zur Identifizierung des Geräts verwendet werden soll.

In der folgenden Tabelle wird die Reihenfolge der verwendeten ID-Methoden basierend auf dem Rückgabebild-Typwert („1“ oder „5“) im Pfad aufgeführt:

<table id="table_07B0E55D5DAA4552A5CBC6937D47A857"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Einstellung </th> 
   <th colname="col2" class="entry"> Reihenfolge der ID-Methoden </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <code> /1/</code> </td> 
   <td colname="col2"> <p>Standard: </p> 
    <ul id="ul_E37E9919658A492C92187BAA18D33AB6"> 
     <li id="li_1A9E39C7CFB24C68AA07C8E85D33A858">Benutzerspezifische Besucher-ID </li> 
     <li id="li_0DC8D17828C848BEB614C6E47C090064">Cookie </li> 
     <li id="li_52706792FAD14F459266E3A672F92EA1">Abonnenten-ID-Header </li> 
     <li id="li_ECAD713D22314338BB5C92167DC0BB02"> IP-Adresse, Benutzeragent, Gateway-IP-Adresse </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <code> /5/ /5.1/ /5.5/</code> </td> 
   <td colname="col2"> <p>Gerät wurde als Wireless-Gerät erkannt, oder <code> /5/</code> wurde manuell in der Bildanforderung gesendet: </p> 
    <ul id="ul_624BEDFA3E1243CF9B42081D8B8EFFFB"> 
     <li id="li_D65761D23B684DB59BC23E92C9098122">Benutzerspezifische Besucher-ID </li> 
     <li id="li_ADBA806B74CA43EFA8612301E06106C6">Abonnenten-ID-Header </li> 
     <li id="li_79DFD0DEAA1242C09A03E8134A40F799">Cookie </li> 
     <li id="li_A462B9120FC6443480D62F37D456747E">IP-Adresse, Benutzeragent, Gateway-IP-Adresse </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Sie können auch eine „1“ oder eine „5“ in manuellen Bildanforderungen übergeben. Achten Sie aber darauf, dass sich diese Codes gegenseitig ausschließen. Wenn Sie also immer „5“ übergeben, wird kein Cookie genutzt, wenn dies unterstützt wird. Sie können einen eigenen Mechanismus einfügen, um festzustellen, ob ein Gerät Cookies unterstützt, und dann anstelle der „5“ eine „1“ im Bild übergeben. Die Verbesserungen hinsichtlich der Genauigkeit, die so erzielt werden können, sind dabei nur bei Geräten möglich, die Cookies unterstützen.

### Abonnenten-ID-Header {#section_60D6EAC0D16945A89DD5A7ADF3B8298D}

Die Methode mit Abonnenten-IDs zur Benutzeridentifizierung ist in der Regel zuverlässiger als ein Cookie, da Cookies möglicherweise gelöscht oder nicht zugelassen werden oder weil es möglicherweise Probleme mit der Verwaltung von Gateway-Cookies gibt.

Sie können die Änderungen bei der Identifizierung eines Besuchers verbessern, indem Sie zur Zulässigen Liste für den Mobilnetzbetreiber hinzugefügt werden, den Ihre Besucher verwenden. Um Zugriff auf die Besucher-ID des Netzbetreibers zu erhalten, wenden Sie sich an den Netzbetreiber, um Ihre Domäne zu seiner zulässigen Liste hinzuzufügen. Wenn Sie sich in der Zulässigkeitsliste eines Netzbetreibers befinden, haben Sie auch Zugriff auf Abonnenten-ID-Header, auf die Sie sonst möglicherweise nicht zugreifen können.

In der folgenden Liste sind die Header aufgeführt, mit denen Wireless-Geräte identifiziert werden. Der Algorithmus für die Verarbeitung der Header beinhaltet

1. die Extrahierung des HTTP-Header-Schlüssels (der Name des Headers, wie „X-Up-Calling-Line-ID“)
1. das Entfernen aller Zeichen, die keine Buchstaben sind (A–Z und a–z)
1. das Konvertieren des Header-Schlüssels in Kleinbuchstaben
1. den Vergleich des Schlüsselendes mit denen in der folgenden Tabelle, um eine Übereinstimmung zu finden:

| Kopfzeile | Typ | Beispiel |
|---|---|---|
| callinglineid | ID | X-Up-Calling-Line-ID: 8613802423312 |
| subno | ID | x-up-subno: swm_10448371100_vmag.mycingular.net |
| clientid | ID | ClientID: eGtUpsqEO19zVHmbOkgaPVI-@sprintpcs.com |
| uid | ID | x-jphone-uid: a2V4Uh21XQH9ECNN |
| clid | ID | X-Hts_clid: 595961714786 |
| deviceid | ID | rim-device-id: 200522ae |
| forwardedfor | ID oder IP-Adresse | X-Forwarded-For: 127.0.0.1 |
| msisdn | ID oder IP-Adresse | X-Wap-msisdn: 8032618185 |
| clientip | IP-Adresse | Client-ip: 10.9.41.2 |
| wapipaddr | IP-Adresse | X-WAPIPADDR: 10.48.213.162 |
| huaweinasip | IP-Adresse | x-huawei-NASIP: 211.139.172.70 |
| userip | IP-Adresse | UserIP: 70.214.81.241 |
| ipaddress | IP-Adresse | X-Nokia-ipaddress: 212.97.227.125 |
| subscriberinfo | IP-Adresse | X-SUBSCRIBER-INFO: IP=10.103.132.128 |

So würde zum Beispiel „callinglineid“ mit „X-Up-Calling-Line-ID“ und „nokia-callinglineid“ übereinstimmen. Anhand des Header-Typs erkennen wir, was im Header stehen soll. Die Reihenfolge der Einträge in der Liste gibt die Priorität der Header wieder (wenn z. B. ein „callinglineid“-Header vorhanden ist, wird er anstelle von „subno“ verwendet).

Sie können [dynamische Variablen](../implement/vars/page-vars/dynamic-variables.md) verwenden, um spezielle Werte aus einem Header zu extrahieren.

## Ausweich-ID-Methoden

Wenn andere Besucher-ID-Methoden fehlschlagen, setzt Adobe ein Ausweich-Cookie oder verwendet eine Kombination aus IP-Adresse und Benutzeragent, um den Besucher zu identifizieren.

### Ausweichmethode zur Besucheridentifizierung {#section_2BA15E4FA6034C3EBF43859406343EB6}

AppMeasurement für JavaScript 1.x und JavaScript H.25.3 (Januar 2013 veröffentlicht) enthalten eine neue Ausweichmethode zur Identifizierung von Besuchern, in deren Browsern das von Adobes Datenerfassungsservern gesetzte Cookie (`s_vi`) blockiert wird. Bislang wurden Besucher, wenn ein Cookie nicht gesetzt werden konnte, bei der Datenkollektion anhand einer Kombination von IP-Adresse und Benutzeragentenzeichenfolge identifiziert.

Mit diesem Update wird, wenn das normale `s_vi`-Cookie nicht verfügbar ist, ein Ausweich-Cookie in der Domäne der Website mit einer zufällig generierten eindeutigen ID erstellt. Dieses Cookie mit dem Namen `s_fid` wird mit einem Ablaufzeitraum von 2 Jahren festgelegt und dient als Ausweichmöglichkeit bei zukünftigen Identifizierungen. Diese Änderung sollte zu erhöhter Genauigkeit bei der Besuchs- und Besucherzählung führen in Situationen, in denen das primäre Cookie (`AMCV_` oder `s_vi`) nicht gesetzt werden kann.

In den Besuchen insgesamt sind alle Besucher enthalten, die anhand des `s_vi`-Cookies oder nach einer Ausweichmethode identifiziert werden.

### IP-Adresse, Benutzeragent, Gateway-IP-Adresse {#section_104819D74C594ECE879144FCC5DEF4BF}

  Wenn die Cookies `AMCV_` oder `s_vi` und `s_fid` nicht gesetzt werden können, werden Besucher anhand einer Kombination aus IP-Adresse und Benutzeragent identifiziert.
