---
title: Mobilgerätedimensionen
description: Dimensionen basierend auf der Benutzeragentenzeichenfolge des Geräts.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 89%

---


# Mobilgerätedimensionen

*Auf dieser Seite werden die Eigenschaften von Mobilgeräten aufgeführt, die auf Ihre Website zugreifen. Weitere Informationen zur Verfolgung von Geräten in einer Mobile App finden Sie unter [Implementieren von Analytics für Mobilgeräte](/help/implement/mobile-device-sdk.md) im Benutzerhandbuch zu Implementierungen.*

Mobilgerätedimensionen bieten Einblicke in die Eigenschaften von Mobilgeräten, die Ihre Site besuchen. Anhand dieser Dimensionen können Sie erkennen, welche Funktionen ein Mobilgerät unterstützt.

## Füllen dieser Dimensionen mit Daten

Diese Dimensionen verweisen auf interne Suchregeln von Adobe. Der Suchwert basiert auf der mit dem Treffer gesendeten `User-Agent`-HTTP-Kopfzeile. Adobe arbeitet mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um Suchen zwischen Benutzeragent und Mobilgerätedimensionen zu unterstützen. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über Adobe Experience Platform Launch), sind alle Mobilgerätedimensionen vorkonfiguriert.

## Beschreibung der Mobilgerätedimensionen

>[!NOTE]
>
>Dimension items labeled `"None"` are non-mobile devices. Wenn Sie einen Bericht wünschen, der nur Mobilgeräte enthält, ziehen Sie die Dimension „Mobilgerät“ in den Segmentbereich der Arbeitsfläche von Workspace.

* **Mobilgerät – Audio-Unterstützung**: Stellt die Dateiformate fest, die vom Gerät wiedergegeben werden können. Zu den Beispielwerten gehören `"MP3"`, `"AAC"` und `"MIDI Monophonic"`. Werte in dieser Dimension schließen sich nicht gegenseitig aus; Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.
* **Mobilnetzbetreiber**: Wenn der Benutzeragent ein netzwerkspezifisches Gerät enthält, ist der Netzbetreiber ein Dimensionselement. Zu den Beispielwerten gehören `"Reliance Jio"`, `"Airtel"`, `"Vodafone"` und `"Verizon"`.
* **Mobilgerät – Farbtiefe**: Die Farbtiefe des Mobilgeräts in Bit.
* **Mobilgerät – Cookie-Unterstützung**: Stellt fest, ob das Mobilgerät Cookies unterstützt. Dieser Bericht gibt nicht an, ob der Browser Cookies akzeptiert. Dimension items include `"Supported"`, `"Not supported"`, and `"Unknown"`.
* **Mobilgerät**: Das Mobilgerät, das der Besucher verwendet.
* **Mobilgerätenummer**: Stellt fest, ob das Mobilgerät seine Nummer übermittelt. Dimension items include `"Supported"`, `"Not supported"`, and `"Unknown"`.
* **Mobilgerätetyp**: Der Typ des Mobilgeräts. Zu den Beispielwerten gehören `"Mobile phone"`, `"Tablet"`, `"Media player"` und `"Gaming console"`.
* **Mobil-DRM**: Der DRM-Typ, den das Mobilgerät unterstützt. Zu den Beispielwerten gehören `"DRM OMA forward"`, `"DRM OMA combined delivery"` und `"DRM OMA separate delivery"`.
* **Mobilgerät – Bildunterstützung**: Die Bildtypen, die vom Mobilgerät unterstützt werden. Zu den Beispielwerten gehören `"PNG"`, `"JPEG"` und `"GIF 87"`. Werte in dieser Dimension schließen sich nicht gegenseitig aus; Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.
* **Mobile Informationsdienste**: Die vom Gerät unterstützten Arten von Nachrichtendiensten. Neuere Geräte melden diese Informationen normalerweise nicht.
* **Mobile Java-VM**: Die Java-Versionen, die das Gerät unterstützt.
* **Mobiles Mail-Design**: Stellt fest, ob das Gerät Decomail unterstützt, eine Funktion, die auf japanischen Geräten bereits verwendet wird.
* **Mobilgerätehersteller**: Gruppiert Mobilgeräte nach Hersteller. Zu den Beispielwerten gehören `"Apple"`, `"Samsung"`, `"Huawei"` und `"Motorola"`.
* **Maximale mobile Lesezeichenlänge**: Die maximale Anzahl von Byte, die das Mobilgerät in mit Lesezeichen versehenen URLs unterstützt. Für neuere Geräte gibt es in der Regel keine Beschränkung.
* **Maximale mobile Browser-URL-Länge**: Die maximale Anzahl von Byte, die das Mobilgerät in URLs unterstützt. Für neuere Geräte gibt es in der Regel keine Beschränkung.
* **Maximale mobile E-Mail-Länge**: Die maximale Anzahl von Byte, die das Mobilgerät in E-Mails unterstützt. Für neuere Geräte gibt es in der Regel keine Beschränkung.
* **Mobile Netzprotokolle**: Die Protokolltypen, die das Gerät beim Zugriff auf das Internet unterstützt. Zu den Beispielwerten gehören `"EDGE"`, `"GPRS"`, `"UMTS"` und `"LTE"`.
* **Mobiles Betriebssystem (veraltet)**: Verwenden Sie stattdessen die Dimension [Betriebssystem](operating-systems.md).
* **Mobiles PTT**: Stellt fest, ob das Gerät PTT (Push to Talk) unterstützt, wodurch das Mobilgerät sich ähnlich wie ein Funkgerät verhalten kann. Neuere Geräte melden diese Funktion normalerweise nicht.
* **Mobilgerät – Bildschirmhöhe**: Die Höhe des Bildschirms in Pixel. Beachten Sie, dass ein iPhone immer `"480"` meldet, da die iPhone-Geräteversion nicht ermittelt werden kann. Informationen zum Bestimmen der Geräteversion eines iPhone finden Sie im folgenden Abschnitt.
* **Mobilgerät – Bildschirmgröße**: Die vollständigen Abmessungen des Mobilgeräts in Pixel. Die Bildschirmgröße im Bericht lässt keine Rückschlüsse auf die Ausrichtung des Geräts zu. Jedes Gerät besitzt eine feste Bildschirmauflösung im Bericht, unabhängig von der Bildschirmausrichtung. Diese Größe beruht auf Untersuchungen, in denen ermittelt wurde, welche Ausrichtung am ehesten verwendet wird. Sie können Größen wie `"768x1024"` und `"1024x768"` im selben Bericht sehen, wobei jede Größe ein oder mehrere verschiedene Geräte repräsentiert.
* **Mobilgerät – Bildschirmbreite**: Die Breite des Bildschirms in Pixel.
* **Mobilgerät – Video-Unterstützung**: Die Videodateiformate und Codecs, die vom Mobilgerät unterstützt werden. Für verschiedene Codecs von MP4- und 3GPP-Dateien gibt es verschiedene Dimensionselemente. Werte in dieser Dimension schließen sich nicht gegenseitig aus; Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.

## Aufteilen von iPhone-Geräten nach Modell oder Version

Mobilgeräte melden ihre Firmware-Version in ihrer Benutzeragenten-Zeichenfolge, nicht die Geräteversion. Beispielsweise enthält ein iPhone der aktuellen Generation einen identischen Benutzeragenten wie das iPhone der letzten Generation, wenn sie dieselbe Firmware-Version verwenden. Da es nicht möglich ist, die Geräteversion eines iPhone mit JavaScript zu bestimmen, gehören alle iPhones in denselben Behälter. Die Mobilgerätedimensionen basieren ausschließlich auf Suchvorgängen, die auf den Benutzeragenten verweisen. Sie werden also feststellen, dass alle iPhone-Geräte eine Bildschirmgröße von `320 x 480` angeben.

Wenn Sie die Geräteversion eines iPhone erfassen möchten, gibt es zwei Möglichkeiten, diese Einschränkung zu umgehen.

* **Verwenden des iOS SDK**: Das Mobile SDK enthält Dimensionen, die die Geräteversion für die Verwendung beim Reporting verfügbar machen. Diese Methode eignet sich besser für Mobile Apps als für Websites.
* **Verwenden andere Variablen, die über JavaScript verfügbar sind**: Einige Variablen, wie `screen.height` und `screen.width`, können verwendet werden, um die Geräteversion abzuleiten. Sie könnten beispielsweise den folgenden Code-Ausschnitt auf Ihrer Site verwenden:

   ```js
   if (navigator.userAgent.indexOf('iPhone') > -1) {
     s.eVarXX = screen.width + "x" + screen.height;
     }
   ```

   Dieser Code-Block erkennt zunächst, ob es sich bei dem Gerät um ein iPhone handelt. Ist dies der Fall, verwendet der Code JavaScript, um die Bildschirmauflösung in eine eVar zu ziehen. Mit dieser Methode können Sie die Geräteversion in etwa erkennen, wenn die Bildschirmauflösungen eindeutig sind.
