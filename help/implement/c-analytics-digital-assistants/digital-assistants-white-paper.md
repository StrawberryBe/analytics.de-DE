---
description: 'null '
seo-description: 'null '
seo-title: Analytics für digitale Berater implementieren
title: Analytics für digitale Berater implementieren
uuid: c 61 e 6 a 1 a-ec 08-4936-9053-5 f 77223 f 57 ff
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Analytics für digitale Berater implementieren

<!-- 

<p>https://wiki.corp.adobe.com/display/mobileanalytics/Analytics+for+Digital+Assistants+Whitepaper </p> 
<p>https://marketing.adobe.com/resources/help/en_US/sc/implement/digital-assistants-white-paper.html </p> 
<p>Ticket: https://jira.corp.adobe.com/browse/AN-157750 </p>

 -->

Mit den jüngsten Entwicklungen in den Bereichen Cloud Computing, maschinelles Lernen und Verarbeitung natürlicher Sprache haben digitale Assistenten das dunkle Zeitalter von „Clippy“ hinter sich gelassen und werden Teil unseres täglichen Lebens. Verbraucher beginnen mit ihren Geräten zu sprechen und erwarten, dass sie Sätze wie „Alexa, schalte das Licht im Wohnzimmer ein“ oder „Okay Google, wie ist das Wetter draußen?“ hören, verstehen und auf natürliche, menschenähnliche Weise darauf reagieren.

Indem sich diese Plattformen zunehmend etablieren, können Marken ihre Dienste den Verbrauchern auf die gleiche natürliche Art präsentieren. Beispielsweise können Verbraucher Fragen wie die folgenden stellen:

* „Alexa, frage mein Auto, ob es einen Ölwechsel braucht.“
* „Cortana, wie viel Geld ist noch auf meinem Girokonto?“
* „Siri, sende John über meine Bank-App 20 $ für das Abendessen gestern.“

Dieses Whitepaper bietet einen Überblick darüber, wie Sie die Adobe Analytics Cloud am besten nutzen können, um diese Art von Erfahrungen zu messen und zu optimieren.

## Übersicht über die digitale Erfahrungsarchitektur {#concept_26AC08D291724223A943C80B1C6F2333}

![](assets/Digital-Assitants.png)

Die meisten heutigen digitalen Assistenten basieren auf einer ähnlichen allgemeinen Architektur:

1. **Gerät:** Ein Gerät (wie Amazon Echo oder ein Telefon) mit einem Mikrofon, über das der Benutzer eine Frage stellen kann.
1. **Digitaler Assistent:** Das Gerät interagiert mit dem Dienst, der den digitalen Assistenten steuert. Dieser Dienst ist für einen Großteil der Magie verantwortlich. Dort wird die Sprache in maschinenverständliche „Intents“ (Absichten) umgewandelt, und die Details der Anfrage werden analysiert. Sobald die Absicht des Benutzers verstanden wurde, leitet der digitale Assistent den Intent und Details der Anfrage an die App weiter, die die Anfrage bearbeitet.
1. **„App“:** Bei der App kann es sich entweder um eine Telefon- oder um eine Sprach-App handeln. Die App ist für die Beantwortung der Anfrage verantwortlich. Sie antwortet dem digitalen Assistenten, und der digitale Assistent antwortet dann dem Benutzer.

## Wo kann Analytics implementiert werden? {#concept_F53A0566589042658DEA5B86B22C10CB}

Am besten implementieren Sie Analytics in der App. Die App erhält den [Intent](../../implement/c-analytics-digital-assistants/digital-assistants-white-paper.md#section_BB339BDB5C3D40C6B5C426B0E092B48A) einschließlich aller Details vom digitalen Assistenten und entscheidet über die Antwort.

Während des Lebenszyklus einer Anfrage kann es an zwei Stellen hilfreich sein, die Analytics Cloud aufzurufen.

1. Wenn die Anfrage an die „App“ gesendet wird. Falls Sie vor der Beantwortung der Anfrage zusätzlichen Kontext zum Benutzer benötigen, sollten Sie die Audience Manager-Funktion nutzen, um die Segmente abzurufen, zu denen der Benutzer gehört.
1. Nachdem die Antwort von der App zurückgegeben wird. Wenn Sie, zum Zwecke zukünftiger Optimierungen, nur festhalten möchten, was mit dem Kunden geschehen ist, senden Sie eine Anfrage an Adobe Analytics, nachdem die Antwort zurückgegeben wurde. Auf diese Weise verfügen Sie über den vollständigen Kontext, d. h, Sie wissen, wie die Anfrage lautete und wie das System reagiert hat.

## Neuinstallationen {#section_FD63267479DB47C2A081244A3E65A0CC}

Bei einigen digitalen Assistenten erhalten Sie eine Benachrichtigung, wenn der Skill installiert wird. Dies ist besonders der Fall, wenn eine Authentifizierung erforderlich ist. Zu diesem Zeitpunkt sollten Sie Adobe das Ereignis *`Install`* senden, indem Sie `a.InstallEvent=1` als Kontextdaten festlegen. Beachten Sie, dass dies nicht auf allen Plattformen verfügbar ist. Es ist jedoch hilfreich, wenn es um die Beibehaltung geht. Mit dem folgenden Beispielcode werden *`Install`**`Install Date`*, und *`AppID`*.

**Codebeispiel**

```
GET 
/b/ss/[rsid]/0?vid=[UserID]&c.a.InstallEvent=1&amp;c.a.InstallDate=2017-04-24&c.a.AppID=Spoofify1.0&c .OSType=Alexa&pageName=install 
HTTP/1.1 
Host:  
<xref href="https: sc.omtrdc.net="" " format="http"  scope="external">
  sc.omtrdc.net 
 Cache-Control: no-cache 
</xref href="https:>
```

## Mehrere Assistenten oder mehrere Apps {#section_81740741752E4142BE42DA4C9DDEEDF5}

Wahrscheinlich entwickeln Sie Apps für mehrere Plattformen. Dabei hat es sich als Best Practice bewährt, bei jeder Anfrage auch eine App-ID zu senden. Dies kann in den Kontextdaten `a.AppID` eingestellt werden. Follow the format of `[AppName] [BundleVersion]`, for example, BigMac for Alexa 1.2

**Codebeispiel**

```
GET /b/ss/[rsid]/0?vid=[UserID]&c.a.AppID=Spoofify1.0&c.a.Launches=1&c.Product=AmazonEcho&c.OSType=Alexa&pageName=install  HTTP/1.1 
Host: [prefix].sc.omtrdc.net 
Cache-Control: no-cache
```

```
 GET /b/ss/[rsid]/0?vid=[UserID]&c.a.AppID=Spoofify2.0&c.a.Launches=1&c.Product=GoogleHome&c.OSType=Android&pageName=install  HTTP/1.1 
Host: sc.omtrdc.net 
Cache-Control: no-cache
```

## Benutzer-/Besucheridentifizierung {#section_7CE70FEB43C44B90954702CA30F87D58}

The Analytics Cloud uses the [Identity Service](https://marketing.adobe.com/resources/help/en_US/mcvid/) (ECID) service to tie interactions across time to the same person. Most of the digital assistants will return a *`userID`* that you can use to keep the activity for different users separate in the ECID service. In den meisten Fällen sollten Sie dies an den ECID-Dienst übergeben. Einige Plattformen geben eine *`userID`* zurück, die länger als die in Analytics zulässigen 100 Zeichen ist. If that is the case, Adobe recommends that you hash the *`userId`* to a fixed-length value using a standard hashing algorithm, such as MD5 or Sha1.

Sie können dafür zwar den ECID-Dienst verwenden, jedoch ist dies nur sinnvoll, wenn Sie ECIDs über verschiedene Geräte hinweg (z. B. Web zu digitalem Assistenten) zuordnen möchten. Wenn es sich bei Ihrer App um eine mobile App handelt (z. B. einen Deep-Link), sollten Sie das SDK unverändert verwenden und die Informationen senden. Die Variable *`userID`* kann mithilfe der setCustomerID-Methode an den ECID-Dienst angehängt werden, damit Geräte besser verbunden werden können. However, if your app is a service, use the *`userID`* provided by the service as the ECID, as well as setting it in the setCustomerID. Dadurch können Sie feststellen, wie der digitale Assistent über die Zeit verwendet wird.

**Codebeispiel**

```
GET /b/ss/[rsid]/0?vid=[UserID]&pageName=[intent]  HTTP/1.1 
Host: sc.omtrdc.net 
Cache-Control: no-cache
```

## Sitzungen {#section_BA4F996F976043B8993F2F7D24FE27FB}

Da digitale Assistenten auf Konversationen basieren, sind sie häufig mit dem Konzept einer Sitzung verbunden. Beispiel:

**Verbraucher:** „Okay Google, rufe mir ein Taxi.“

**Google:**: „Sicher. Für welche Uhrzeit?“

**Verbraucher:** „20:30 Uhr.“

**Google:** „Klingt gut, der Fahrer ist um 20:30 Uhr hier.“

Diese Sitzungen sind wichtig, um den Kontext beizubehalten. Sie helfen dabei, mehr Details zu erfassen und die digitalen Assistenten natürlicher erscheinen zu lassen.

Wenn Sie Analytics für eine Konversation implementieren, sollten Sie zweierlei tun, sobald eine neue Sitzung gestartet wird:

1. **Verwenden Sie Audience Manager:** Rufen Sie die relevanten Segmente ab, zu denen ein Benutzer gehört, damit Sie die Antwort anpassen können. (Zum Beispiel: Diese Person ist zurzeit berechtigt, einen Mehrkanal-Rabatt zu erhalten.)
1. **Senden Sie eine neue Sitzung oder ein Launch-Ereignis:** Wenn Sie die erste Antwort an Analytics senden, fügen Sie ein Launch-Ereignis hinzu. Normalerweise kann dies gesendet werden, indem `a.LaunchEvent=1` als Kontextdaten eingestellt werden.

**Codebeispiel für[!DNL Launch, by Adobe]**

```
GET /b/ss/[rsid]/0?vid=[UserID]&c.a.LaunchEvent=1&c.Intent=[intent]&pageName=[intent]  HTTP/1.1 
Host: sc.omtrdc.net 
Cache-Control: no-cache
```

## Intents {#section_BB339BDB5C3D40C6B5C426B0E092B48A}

Jeder digitale Assistent verfügt über Algorithmen, die Intents erkennen und dann den Intent an die „App“ weitergeben, damit die App weiß, was zu tun ist. Diese Intents entsprechen einer Kurzdarstellung der Anfrage.

Wenn ein Benutzer beispielsweise sagt: „Siri, sende John 20 $ für das Abendessen gestern über meine Bank-App“, dann lautet der Intent etwa *`sendMoney`* zu trennen.

Indem Sie jede dieser Anfragen als eVar einsenden, können Sie Pfadsetzungsberichte für jeden Intent für Konversations-Apps erstellen. Sie sollten auch sicherstellen, dass die „App“ Anfragen ohne Intent verarbeiten kann. Es wird empfohlen, den Wert *`No Intent Specified`*(Kein Intent angegeben) statt eines leeren Werts einzusenden.

**Codebeispiel**

```
GET /b/ss/[rsid]/0?vid=[UserID]&c.a.AppID=Penmo1.0&c.a.LaunchEvent=1&c.Intent=SendPayment&pageName=[intent]  HTTP/1.1 
Host: sc.omtrdc.net 
Cache-Control: no-cache
```

oder

```
GET /b/ss/[rsid]/0?vid=[UserID]&c.a.AppID=Penmo1.0&c.a.LaunchEvent=1&c.Intent=No_Intent_Specified&pageName=[intent]  HTTP/1.1 
Host: sc.omtrdc.net 
Cache-Control: no-cache
```

## Parameter/Slots/Entitäten {#section_041CD1730F9E4096BE75DFF2CC810852}

Zusätzlich zu einem Intent hat der digitale Assistent oft mehrere Schlüsselwertpaare, mit denen die Details des Intents angegeben werden. Diese werden als Slots, Entitäten oder Parameter bezeichnet. Beispiel:

Beispielsweise hat „Siri, sende John über meine Bank-App 20 $ für das Abendessen gestern“ die folgenden Parameter:

* Wer = John
* Betrag = 20
* Grund = Essen

Normalerweise verfügt Ihre App über eine begrenzte Anzahl dieser Parameter. Um sie in Analytics zu verfolgen, senden Sie sie innerhalb von Kontextdaten und ordnen Sie jeden Parameter einer eVar zu.

**Codebeispiel**

```
GET /b/ss/[rsid]/0?vid=[UserID]&c.a.AppID=Penmo1.0=1&c.a.LaunchEvent=1&c.Intent=SendPayment&c.Amount=20.00&c.Reason=Dinner&c.ReceivingPerson=John&c.Intent=SendPayment&pageName=[intent]  HTTP/1.1 
Host: sc.omtrdc.net 
Cache-Control: no-cache
```

## Sitzung {#section_17D69D6B298E46E88E175F62F1ACD831}

Obwohl nicht alle Apps dazu vorgesehen sind, Umsatz zu generieren, sollten Sie überlegen, wie Sie Erfolg definieren und messen können. Adobe Analytics kann den Umsatz, Anzeigenimpressionen und andere Formen des Erfolgs zusammen mit dem Benutzerverhalten messen.

## Fehlerstatus {#section_E8EFF8D610B24DC899C34E50B058864D}

In einigen Fällen sendet der digitale Assistent Informationen an die App, die sie nicht verarbeiten kann. Beispiel.

„Siri, sende John über meine Bank-App 20 Mäuse für das Abendessen gestern.“

Wenn dies geschieht, sollte die App um Erklärung bitten. Wenn Sie auf eine Anfrage wie diese reagieren, sollten Sie Analytics außerdem ein Ereignis senden, das darauf hinweist, dass die App einen Fehlerstatus aufweist, sowie eine eVar, die angibt, welcher Fehlertyp aufgetreten ist.

Stellen Sie sicher, dass Fehler für fehlerhafte Angaben und App-Probleme vorhanden sind.

**Codebeispiel**

```
GET /b/ss/[rsid]/0/?vid=[UserID]&c.a.AppID=Penmo1.0&c.Error=1&c.ErrorName=InvalidCurrency&pageName=[intent] HTTP/1.1 
Host: sc.omtrdc.net 
Cache-Control: no-cache
```

## Gerätefunktionen {#section_6770D82A3B0E4AD5A2172A7E67B0DF20}

Die meisten Plattformen zeigen das Gerät, mit dem der Benutzer gesprochen hat, nicht an. Stattdessen werden nur die Funktionen des Geräts als verfügbare Schnittstellen (z. B. Audio, Bildschirm, Video usw.) angezeigt. Dies sind nützliche Informationen, da sie die Inhaltstypen definieren, die bei der Interaktion mit Ihren Benutzern verwendet werden können. Beim Messen der Schnittstellen ist es am besten, sie zu verketten (in alphabetischer Reihenfolge).

Beispiel: `:Audio:Camera:Screen:Video:`

Beachten Sie die Doppelpunkte am Anfang und am Ende. These help when creating segments (for example, give me all interactions with `:Audio:` capabilities).

Amazon-Funktionen: [https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/alexa-skills-kit-interface-reference](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/alexa-skills-kit-interface-reference)

Google-Funktionen: [https://developers.google.com/actions/assistant/surface-capabilities](https://developers.google.com/actions/assistant/surface-capabilities)

## Analytics Reporting für digitale Assistenten {#concept_265BC8E99C5545D0A9B9412C11EE58CC}

Sobald die App für Ihren digitalen Assistenten implementiert ist, können Sie alle Adobe Analytics-Funktionen nutzen. Im Folgenden finden Sie einige Beispiele für die Möglichkeiten, die Ihnen mit Analytics zur Verfügung stehen.

## Überwachen von Intents {#section_6632D9F2EF9045A7A1A4263D3561C78F}

Die meisten Apps verfügen über mehrere Intents und Funktionen, die Sie ausführen können. You could easily use [!UICONTROL Analysis Workspace] to keep track of the top intents by instances and by users

<!-- 

<p>--- Image of Intents --- </p>

 -->

Sie können feststellen, welche Funktionen am häufigsten verwendet werden, und erhalten einen Überblick über die Akzeptanz neuer Funktionen.

## Anfragen mit Fehlern {#section_CF1A79003E784F88A03F4EEF6CDC7A7C}

Sie können Fehler überwachen, um zu ermitteln, an welchen Stellen Benutzer häufiger Probleme haben.

<!-- 

<p>--- Image of Errors --- </p>

 -->

## Fluss zwischen Ereignissen {#section_08FA8EBD384D41ED8CA52EFE438C8CD2}

Eine der leistungsfähigsten Funktionen ist die Untersuchung des Intent-Flusses. Dies ist auf zwei Arten hilfreich. Zunächst können Sie innerhalb einer Sitzung ermitteln, wie die Benutzer in einer Konversation von einem Intent zum nächsten wechseln. Danach können Sie den Intent-Fluss innerhalb eines längeren Zeitrahmens untersuchen, um festzustellen, wie sich die Nutzung der App entwickelt.

## Beispiel  {#concept_2B13D5E7A8E042D1A4B7BB80BBAACD12}

**Vorinstallierte App**

<table id="table_70BF4E41D0BE4482BD925FB3A1768CE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Benutzer </th> 
   <th colname="col2" class="entry"> Antwort des Geräts </th> 
   <th colname="col3" class="entry"> Aktion/Intent </th> 
   <th colname="col4" class="entry"> Get-Anfrage </th> 
   <th colname="col5" class="entry"> Analytics-Daten </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Spiele Spoofify </p> </td> 
   <td colname="col2"> <p> „Okay, ich spiele Spoofify“ </p> </td> 
   <td colname="col3"> <p> Play </p> </td> 
   <td colname="col4"> <p> 
     <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. a. launchevent = 1 &amp; c. Intent = Play &amp; pagename = playapp HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_E80B0BBEBE764023BB9B49FE5F15B918"> 
      <li id="li_9BC2CCABB0ED4246A57C37633666CDE2">Visitor ID </li> 
      <li id="li_1E7F9E979A3D49CE90899CE82C70BCD0">App-Version </li> 
      <li id="li_C4BD7653B0FA47F6A3E4F1FF18138F10">Anzahl der Starts </li> 
      <li id="li_B7FA47CBD75747E8A8A25E228C90E524">Intent </li> 
      <li id="li_48274BA200704730A22C85FD682AE3B0">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Spiele etwas anderes </p> </td> 
   <td colname="col2"> <p> „Okay, welchen Song?“ </p> </td> 
   <td colname="col3"> <p> ChangeSong </p> </td> 
   <td colname="col4"> <p> 
     <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = changesong &amp; pagename = askforsong HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_AE8CF669F06547FDA68801F20BD8CBCE"> 
      <li id="li_5A03E41891AF4F37A3BE05BC11F197BC">Visitor ID </li> 
      <li id="li_435FF7DEB169466E8C3F9258C91315D1">App-Version </li> 
      <li id="li_AB2B602D9DC74B3D951A0942B6CF8B39">Intent </li> 
      <li id="li_C9F87F3BB7104C9C978BB046C5DB9092">*Leere Wiedergabeliste </li> 
      <li id="li_FB762962468A44A18DF93488EC2CB848">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Spiele „My Heart Will Go On“ von Celine Dion </p> </td> 
   <td colname="col2"> <p> „Okay, ich spiele ‚My Heart Will Go On‘ von Celine Dion“ </p> </td> 
   <td colname="col3"> <p> ChangeSong </p> </td> 
   <td colname="col4"> <p> 
     <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = changeplaylist &amp; pagename = actionplaysong &amp; c. songid = [012345] HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_2AFEE1E928A8499E96B1BC6C5CC21F81"> 
      <li id="li_4BDF8093373A4DA1BB24A608FAC5B7CF">Visitor ID </li> 
      <li id="li_79B4FACCD333472EB9FC1F94B904AFB4">App-Version </li> 
      <li id="li_3EDAB6208CB24213A934167BD08BD1AE">Intent </li> 
      <li id="li_C8E6609F9E0A45A8AED15F73374F40B2">Song-ID </li> 
      <li id="li_C4D99387C4D748189E15476F5E03BB76">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ändere die Playliste </p> </td> 
   <td colname="col2"> <p> „Okay, welche Playliste?“ </p> </td> 
   <td colname="col3"> <p> ChangePlaylist </p> </td> 
   <td colname="col4"> <p> 
     <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = changeplaylist &amp; pagename = askforplaylist HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_913CF31C3EB34BDB819AD54D28F9DE5D"> 
      <li id="li_93036A142FB34A73A95B8AB114EA99C3">Visitor ID </li> 
      <li id="li_F699CDD7866C4EB4BECFF0FAA4689736">App-Version </li> 
      <li id="li_6AB1FF7ED6A247FAA8922390410F2F5F">Intent </li> 
      <li id="li_9DF30E2E1958468783FF753D014F1A5F">*Leere Wiedergabeliste </li> 
      <li id="li_B1106A51B8CD49DD8B566B946176F854">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Spiele Usher </p> </td> 
   <td colname="col2"> <p> „Okay, ich spiele Usher“ </p> </td> 
   <td colname="col3"> <p> ChangePlaylist </p> </td> 
   <td colname="col4"> <p> 
     <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = changeplaylist &amp; pagename = actionplayplaylist &amp; c. Playlist = Usher HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_B70E7C9BEFA54C2FA8B7485F9BC7CEE7"> 
      <li id="li_2B0319D20189497D8C9981F871D4FBC4">Visitor ID </li> 
      <li id="li_78C28F34FC7C41589EB111ADCC5A0D66">App-Version </li> 
      <li id="li_8ACF819CF80E4E8F942E0903DF75AE33">Intent </li> 
      <li id="li_49F407E43F474356A5F131F82B6C4EB9">der Wiedergabeliste </li> 
      <li id="li_7380EC51B0DE420EB5DD48BCE21B0567">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Schalte die Musik aus </p> </td> 
   <td colname="col2"> <p> *keine Antwort, Musik wird ausgeschaltet </p> </td> 
   <td colname="col3"> <p> Aus </p> </td> 
   <td colname="col4"> <p> 
     <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = Off &amp; pagename = turnsoffmusic HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_BCA19F2A98CC42788A23E668B260F553"> 
      <li id="li_12A9DA8684B2479D90F3C357AE4F1D15">Visitor ID </li> 
      <li id="li_9E543F7F12D247D0900E5B1BE8EB0F61">App-Version </li> 
      <li id="li_9627816FE3594C418EC52DAD42501BCA">Intent </li> 
      <li id="li_5D59C5D8D0F34F5193F592A867AE5639">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Benutzer muss App installieren**

<table id="table_C178E3A2C87043A0A2B8C365869102A3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Benutzer </th> 
   <th colname="col2" class="entry"> Antwort des Geräts </th> 
   <th colname="col3" class="entry"> Aktion/Intent </th> 
   <th colname="col4" class="entry"> Get-Anfrage </th> 
   <th colname="col5" class="entry"> Analytics-Daten </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Installiere Spoofify </p> </td> 
   <td colname="col2"> <p> *keine Antwort </p> </td> 
   <td colname="col3"> <p> Installieren </p> </td> 
   <td colname="col4"> <p> 
     <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; amp; amp; c. a. installevent = 1 &amp; c. a. installdate = 2017-04-24 &amp; c. a. appid = Spoofify 1.0 &amp; c. ostype = Alexa &amp; c. Intent = Install &amp; pagename = Install HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_83A7731E5EA84477906AF4BFB3B50F48"> 
      <li id="li_A23A342B0D5745B3854B90ADFDD15EB2">Visitor ID </li> 
      <li id="li_E2F89B771B5F445B995E30C7E76BF2D2">Datum </li> 
      <li id="li_03378BC9365F4020B7E28461AFDCB160">Intent </li> 
      <li id="li_6E1ECC9AF55141D1857688DA6A33DEEA">OS-Version </li> 
      <li id="li_A4D06A0DFBC247499D9586F6B76571C4">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Spiele Spoofify </p> </td> 
   <td colname="col2"> <p> „Okay, ich spiele Spoofify“ </p> </td> 
   <td colname="col3"> <p> Play </p> </td> 
   <td colname="col4"> <p> 
     <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. a. launchevent = 1 &amp; c. Intent = Play &amp; pagename = playapp HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_8FCA2B1357A8496DAF563775F019404F"> 
      <li id="li_78E84586A5284164B5B577B68A113394">Visitor ID </li> 
      <li id="li_977915DC425A43BDA69D9F76ADFBAB0C">App-Version </li> 
      <li id="li_12725E1D4540485B8A3DB2EC82C6AD4C">Anzahl der Starts </li> 
      <li id="li_5B7F4487682241C38071A7037157F473">Intent </li> 
      <li id="li_A6AC81D56BF44E07B2FC0F2740CAB237">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Spiele etwas anderes </p> </td> 
   <td colname="col2"> <p> „Okay, welchen Song?“ </p> </td> 
   <td colname="col3"> <p>ChangeSong </p> </td> 
   <td colname="col4"> 
    <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = changesong &amp; pagename = askforsong HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </td> 
   <td colname="col5"> <p> 
     <ul id="ul_C0FCB407A1344527A532A1EAEF0387E4"> 
      <li id="li_8905BCF15F0F493D90B5F1135AEC149C">Visitor ID </li> 
      <li id="li_2D1FAAF35CE24CE49D1AE3F24E4A5A86">App-Version </li> 
      <li id="li_A7D11680A9554414878E6CBD03B66DC4">Intent </li> 
      <li id="li_64308721D00441FBB7E6EA6EDF93C100">*Leere Wiedergabeliste </li> 
      <li id="li_A1B2C4E27F9E4B61AAA6373DA8CEB8F2">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Spiele „My Heart Will Go On“ von Celine Dion </p> </td> 
   <td colname="col2"> <p> „Okay, ich spiele ‚My Heart Will Go On‘ von Celine Dion“ </p> </td> 
   <td colname="col3"> <p> ChangeSong </p> </td> 
   <td colname="col4"> 
    <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = changeplaylist &amp; pagename = actionplaysong &amp; c. songid = [012345] HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </td> 
   <td colname="col5"> <p> 
     <ul id="ul_5D782E44875144BF96877897E1180D18"> 
      <li id="li_CB5009ED407A4D4ABF3AAFE73133CC66">Visitor ID </li> 
      <li id="li_D15D65E315964E0CBF75A87CF3FCF9B5">App-Version </li> 
      <li id="li_055D7621BE1D44BA8B8C50E2E45DA6DF">Intent </li> 
      <li id="li_1D52C0AB9C12483E9CD7DC216D809E44">Song-ID </li> 
      <li id="li_5CFB748D02E84050AE216FDC55C680E2">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Ändere die Playliste </p> </td> 
   <td colname="col2"> <p> „Okay, welche Playliste?“ </p> </td> 
   <td colname="col3"> <p> ChangePlaylist </p> </td> 
   <td colname="col4"> 
    <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = changeplaylist &amp; pagename = askforplaylist HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </td> 
   <td colname="col5"> <p> 
     <ul id="ul_7167AE13BBC64CC99E4A81B1FF6C9208"> 
      <li id="li_15554F7C8AC3487797A2FB65C8C1E636">Visitor ID </li> 
      <li id="li_11254FBCFA60436FB705D5FE4C313CC5">App-Version </li> 
      <li id="li_4F3AE5B191DB4E73A2C08065A3D75188">Intent </li> 
      <li id="li_7F03D76A26254E65AAEB8E7D647895CA">*Leere Wiedergabeliste </li> 
      <li id="li_DFB50E6BCEAF440D942B30A56CDD1503">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Spiele Usher </p> </td> 
   <td colname="col2"> <p> „Okay, ich spiele Usher“ </p> </td> 
   <td colname="col3"> <p> ChangePlaylist </p> </td> 
   <td colname="col4"> 
    <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = changeplaylist &amp; pagename = actionplayplaylist &amp; c. Playlist = Usher HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </td> 
   <td colname="col5"> <p> 
     <ul id="ul_BE5815D13CFA48408B4612D220356518"> 
      <li id="li_716EA824A56241A282FD1774A51CF52C">Visitor ID </li> 
      <li id="li_02CC3C2A66E44BB4BA865893F3206A6C">App-Version </li> 
      <li id="li_558B15EC8605495B8DC01E644602FC4F">Intent </li> 
      <li id="li_21599097A3B14E368693C77CC7BA8ADD">der Wiedergabeliste </li> 
      <li id="li_70F4254A33704DA18D4D22028A1656E4">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Schalte die Musik aus </p> </td> 
   <td colname="col2"> <p> *keine Antwort, Musik wird ausgeschaltet </p> </td> 
   <td colname="col3"> <p> Aus </p> </td> 
   <td colname="col4"> 
    <code>GET /b/ss/ [rsid]/0? vid = [userid] &amp; c. a. appid = Spoofify 1.0 &amp; c. Intent = Off &amp; pagename = turnsoffmusic HTTP/1.1 
 Host: sc. omtrdc. net 
 Cache-Control: no-cache </code>
  </td> 
   <td colname="col5"> <p> 
     <ul id="ul_C623E19496DD466DA299AD610CE5ED1D"> 
      <li id="li_6A7AEF89A74C431C84D107E4F23AE223">Visitor ID </li> 
      <li id="li_B8CFF6AAB2E2476786026A98337589AF">App-Version </li> 
      <li id="li_534596CB56B24B729AAA801A7B4D9D31">Intent </li> 
      <li id="li_CA3328E5FFF442BAA0F11C51DF2ED53F">Antwort </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

