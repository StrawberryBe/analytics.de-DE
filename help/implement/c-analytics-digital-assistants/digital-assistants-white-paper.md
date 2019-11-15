---
description: 'null'
title: Analytics für digitale Assistenten implementieren
uuid: c61e6a1a-ec08-4936-9053-5f57223f57ff
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Implementierung von Analytics für digitale Assistenten

<!-- 
https://wiki.corp.adobe.com/display/mobileanalytics/Analytics+for+Digital+Assistants+Whitepaper
https://marketing.adobe.com/resources/help/en_US/sc/implement/digital-assistants-white-paper.html
Ticket: https://jira.corp.adobe.com/browse/AN-157750
-->

Aufgrund der jüngsten Fortschritte in den Bereichen Cloud Computing, maschinelles Lernen und natürliche Sprachverarbeitung werden digitale Assistenten zu einem Teil des täglichen Lebens. Die Verbraucher beginnen damit, mit ihren Geräten zu sprechen und erwarten, dass sie Menschen verstehen und darauf reagieren. Indem sich diese Plattformen zunehmend etablieren, können Marken ihre Dienste den Verbrauchern auf die gleiche natürliche Art präsentieren. Beispielsweise können Verbraucher Fragen wie die folgenden stellen:

* „Alexa, frage mein Auto, ob es einen Ölwechsel braucht.“
* „Cortana, wie viel Geld ist noch auf meinem Girokonto?“
* „Siri, sende John über meine Bank-App 20 $ für das Abendessen gestern.“

Diese Seite bietet einen Überblick darüber, wie Adobe Analytics am besten zur Messung und Optimierung dieser Erlebnistypen verwendet werden kann.

## Übersicht über die Architektur digitaler Erlebnisse

![](assets/Digital-Assitants.png)

Die meisten heutigen digitalen Assistenten basieren auf einer ähnlichen allgemeinen Architektur:

1. **Gerät:** Ein Gerät (wie Amazon Echo oder ein Telefon) mit einem Mikrofon, über das der Benutzer eine Frage stellen kann.
1. **Digitaler Assistent:** Das Gerät interagiert mit dem Dienst, der den digitalen Assistenten steuert. Dort wird die Sprache in maschinenverständliche „Intents“ (Absichten) umgewandelt, und die Details der Anfrage werden analysiert. Sobald die Absicht des Benutzers verstanden wurde, leitet der digitale Assistent den Intent und Details der Anfrage an die App weiter, die die Anfrage bearbeitet.
1. **„App“:** Bei der App kann es sich entweder um eine Telefon- oder um eine Sprach-App handeln. Die App ist für die Beantwortung der Anfrage verantwortlich. Sie antwortet dem digitalen Assistenten, und der digitale Assistent antwortet dann dem Benutzer.

## Wo kann Analytics implementiert werden?

Am besten implementieren Sie Analytics in der App. Die App erhält die Absicht und die Details vom digitalen Assistenten, und dann bestimmt die App, wie sie reagiert.

Während einer Anforderung gibt es zwei Male, die hilfreich sein können, um Daten an Adobe Analytics zu senden.

1. Wenn die Anforderung an Ihre App gesendet wird.
1. Nachdem die Antwort von der App zurückgegeben wird.

Wenn Sie, zum Zwecke zukünftiger Optimierungen, nur festhalten möchten, was mit dem Kunden geschehen ist, senden Sie eine Anfrage an Adobe Analytics, nachdem die Antwort zurückgegeben wurde. Sie haben den vollständigen Kontext, was die Anforderung war und wie das System reagiert hat.

## Neue Installationen

Für einige digitale Assistenten erhalten Sie eine Benachrichtigung, wenn jemand die Fähigkeiten installiert, insbesondere wenn die Authentifizierung betroffen ist. Adobe empfiehlt, ein Install-Ereignis zu senden, indem die Kontextdatenvariable festgelegt wird `a.InstallEvent=1`. Diese Funktion steht nicht für alle digitalen Assistenten zur Verfügung, ist aber hilfreich, wenn sie zur Verfügung steht, um die Bindung zu prüfen. Im folgenden Codebeispiel werden die Werte Install-Ereignis, Install Date und AppID in Kontextdatenvariablen gesendet.

```text
GET
/b/ss/[rsid]/1?vid=[UserID]&c.a.InstallEvent=1&c.a.InstallDate=2017-04-24&c.a.AppID=Spoofify1.0&c.OSType=Alexa&pageName=install
HTTP/1.1
Host:
<xref href="https://sc.omtrdc.net">
  sc.omtrdc.net
 Cache-Control: no-cache
</xref href="https:>
```

## Mehrere Assistenzkräfte oder mehrere Apps

Ihre Organisation möchte wahrscheinlich Apps für mehrere Plattformen. Dabei hat es sich als Best Practice bewährt, bei jeder Anfrage auch eine App-ID zu senden. This variable can be set in the `a.AppID` context data variable. Follow the format of `[AppName] [BundleVersion]`, for example, BigMac for Alexa 1.2:

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.a.Launches=1&c.Product=AmazonEcho&c.OSType=Alexa&pageName=install  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify2.0&c.a.Launches=1&c.Product=GoogleHome&c.OSType=Android&pageName=install  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

## Benutzer-/Besucheridentifizierung

Adobe Analytics verwendet den [Adobe Experience Cloud-Identitätsdienst](https://docs.adobe.com/content/help/en/id-service/using/home.html) , um Interaktionen über einen bestimmten Zeitraum hinweg mit derselben Person zu verbinden. Die meisten digitalen Assistenten geben eine zurück, `userID` die Sie verwenden können, um die Aktivität für verschiedene Benutzer zu halten. In den meisten Fällen können Sie diesen Wert als eindeutigen Bezeichner weitergeben. Einige Plattformen geben einen Bezeichner zurück, der länger als die zulässigen 100 Zeichen ist. In diesen Fällen empfiehlt Adobe, dass Sie den eindeutigen Bezeichner mithilfe eines standardmäßigen Hashing-Algorithmus wie MD5 oder Sha1 auf einen Wert mit fester Länge hash.

Die Verwendung des ID-Diensts bietet den meisten Wert, wenn Sie ECIDs auf verschiedenen Geräten zuordnen (z. B. Web-to-Digital-Assistenzkraft). Wenn es sich bei Ihrer App um eine mobile App handelt, verwenden Sie die Experience Platform-SDKs unverändert und senden Sie die Benutzer-ID mit der `setCustomerID` Methode. However, if your app is a service, use the user ID provided by the service as the ECID, as well as setting it in `setCustomerID`.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&pageName=[intent]  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

## Sitzungen

Da digitale Assistenten auf Konversationen basieren, sind sie häufig mit dem Konzept einer Sitzung verbunden. Beispiel:

**Verbraucher:** „Okay Google, rufe mir ein Taxi.“

**Google:**: „Sicher. Für welche Uhrzeit?“

**Verbraucher:** „20:30 Uhr.“

**Google:** „Klingt gut, der Fahrer ist um 20:30 Uhr hier.“

Sitzungen sind wichtig, um den Kontext zu wahren und mehr Details zu sammeln, um die digitale Assistenzkraft natürlicher zu machen. Bei der Implementierung von Analytics für eine Konversation müssen beim Starten einer neuen Sitzung zwei Schritte ausgeführt werden:

1. **Verwenden Sie Audience Manager:** Rufen Sie die relevanten Segmente ab, zu denen ein Benutzer gehört, damit Sie die Antwort anpassen können. (Zum Beispiel: Diese Person ist zurzeit berechtigt, einen Mehrkanal-Rabatt zu erhalten.)
2. **Senden Sie eine neue Sitzung oder ein Launch-Ereignis:** Wenn Sie die erste Antwort an Analytics senden, fügen Sie ein Launch-Ereignis hinzu. Normalerweise kann dies gesendet werden, indem `a.LaunchEvent=1` als Kontextdaten eingestellt werden.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.LaunchEvent=1&c.Intent=[intent]&pageName=[intent]  HTTP/1.1
Host: sc.omtrdc.net
Cache-Control: no-cache
```

## Intents

Jeder digitale Assistent verfügt über Algorithmen, die Intents erkennen und dann den Intent an die „App“ weitergeben, damit die App weiß, was zu tun ist. Diese Intents entsprechen einer Kurzdarstellung der Anfrage.

Wenn ein Benutzer beispielsweise sagt: „Siri, sende John 20 $ für das Abendessen gestern über meine Bank-App“, dann lautet der Intent etwa *sendMoney*.

Indem Sie jede dieser Anforderungen als eVar senden, können Sie Pfadsetzungsberichte für jede der Absichten von Konversations-Apps ausführen. Stellen Sie sicher, dass Ihre App Anforderungen auch ohne Absicht bearbeiten kann. Adobe empfiehlt die Übergabe von "Kein beabsichtigter Zweck angegeben"an die Variable für Inhaltsdaten, anstatt die Variable zu bestätigen.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Penmo1.0&c.a.LaunchEvent=1&c.Intent=SendPayment&pageName=[intent]  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

oder

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Penmo1.0&c.a.LaunchEvent=1&c.Intent=No_Intent_Specified&pageName=[intent]  HTTP/1.1
Host: sc.omtrdc.net
Cache-Control: no-cache
```

## Parameter/Slots/Entitäten

Zusätzlich zu der Absicht haben digitale Assistenten oft eine Reihe von Schlüssel/Wert Paaren, die Details der Absicht. Diese können als Slots, Entitäten oder Parameter bezeichnet werden. Zum Beispiel hätte "Siri, Send John $20 zum Abendessen gestern Abend von meiner Bank-App"die folgenden Parameter:

* Wer = John
* Betrag = 20
* Grund = Essen

In der Regel gibt es eine endliche Anzahl dieser Werte in Ihrer App. Um diese Werte in Analytics zu verfolgen, senden Sie sie in Kontextdatenvariablen und ordnen Sie dann jeden Parameter einer eVar zu.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Penmo1.0=1&c.a.LaunchEvent=1&c.Intent=SendPayment&c.Amount=20.00&c.Reason=Dinner&c.ReceivingPerson=John&c.Intent=SendPayment&pageName=[intent]  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

## Fehlerstatus

Manchmal liefert der digitale Assistent Ihre App mit Eingaben, die er nicht handhaben kann. Zum Beispiel "Siri, Send John 20 Taschen Kohle zum Abendessen gestern Abend aus meiner Banking-App"

Wenn dies der Fall ist, bitten Sie Ihre App um Klärung. Senden Sie außerdem Daten an Adobe, die darauf hindeuten, dass die App einen Fehlerstatus sowie eine eVar aufweist, die angibt, welcher Fehlertyp aufgetreten ist. Denken Sie daran, Fehler einzuschließen, wenn die Eingaben nicht korrekt sind und Fehler aufgetreten sind, wenn die App ein Problem hatte.

```text
GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Penmo1.0&c.Error=1&c.ErrorName=InvalidCurrency&pageName=[intent]  HTTP/1.1
Host: example.sc.omtrdc.net
Cache-Control: no-cache
```

## Gerätefunktionen

Die meisten Plattformen stellen zwar das Gerät, mit dem der Benutzer gesprochen hat, nicht zur Verfügung, stellen aber die Funktionen des Geräts offen. Zum Beispiel Audio, Bildschirm, Video usw. Diese Informationen sind nützlich, da sie die Inhaltstypen definieren, die bei der Interaktion mit Ihren Benutzern verwendet werden können. Bei der Messung der Gerätefunktionen ist es am besten, sie (in alphabetischer Reihenfolge) zu verketten.

Beispiel: `":Audio:Camera:Screen:Video:"`

Vor- und nachfolgende Doppelpunkte helfen beim Erstellen von Segmenten. Zeigen Sie beispielsweise alle Treffer mit `:Audio:` Funktionen an.

* [Amazon-Funktionen](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/alexa-skills-kit-interface-reference) mit Amazon Alexa
* [Google-Funktionen](https://developers.google.com/actions/assistant/surface-capabilities) mit Aktionen auf Google

## Beispiele

| Benutzer | Geräteantwort | Aktion/Intent | GET-Anforderung |
| --- | --- | --- | --- | ---|
| Installiere Spoofify | Keine Antwort | Installieren | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.InstallEvent=1&c.a.InstallDate=[currentDate]&c.a.AppID=Spoofify1.0&c.OSType=Alexa&c.Intent=Install&pageName=Install  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| Spiele Spoofify | "Okay, Spoofify spielen" | Play | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.a.LaunchEvent=1&c.Intent=Play&pageName=PlayApp  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| Spiele etwas anderes | "Okay, welches Lied willst du?" | ChangeSong | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangeSong&pageName= Ask%20For%20Song  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| Spielen Sie "Baby Shark" | "Okay, ich spiele 'Baby Shark' von PinkFong" | ChangeSong | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangeSong&pageName=Action%20Play%20Song&c.SongID=[012345]  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| Ändere die Playliste | "Okay, welche Playlist willst du?" | ChangePlaylist | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangePlaylist&pageName=Ask%20For%20Playlist  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| Abspielen meiner Lieblingslieder-Playlist | "Okay, spielen Sie Ihre Lieblingslieder-Playlist" | ChangePlaylist | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangePlaylist&pageName=Action%20Play%20Playlist&c.Playlist=My%20Favorite%20Songs  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
| Schalte die Musik aus | Keine Reaktion, Musik deaktiviert | Aus | `GET /b/ss/[rsid]/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=Off&pageName=Music%20Off  HTTP/1.1`<br>`Host: example.sc.omtrdc.net`<br>`Cache-Control: no-cache` |
