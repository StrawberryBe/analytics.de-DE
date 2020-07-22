---
title: Mobile Dimensionen
description: Dimensionen basierend auf der user-agent-Zeichenfolge des Geräts.
translation-type: tm+mt
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 4%

---


# Mobile Dimensionen

*Diese Seite listet Eigenschaften von Mobilgeräten auf, die auf Ihre Website zugreifen. Wenn Sie Geräte in einer mobilen App verfolgen möchten, finden Sie weitere Informationen unter[Implementieren von Analytics für Mobilgeräte](/help/implement/mobile-device-sdk.md)im Implementierungs-Benutzerhandbuch.*

Mobile Dimensionen bieten Einblicke in die Eigenschaften von Mobilgeräten, die Ihre Site besuchen. Anhand dieser Dimensionen können Sie erkennen, welche Funktionen ein Mobilgerät unterstützt.

## Diese Dimensionen mit Daten füllen

Diese Dimensionen verweisen auf interne Nachschlageregeln von Adobe. Der Nachschlagewert basiert auf dem `User-Agent` HTTP-Header, der mit dem Treffer gesendet wird. Adobe arbeitet mit [DeviceAtlas](https://deviceatlas.com/) zusammen, um Suchen zwischen Benutzeragent und Mobildimension zu verwalten. Wenn Sie eine AppMeasurement-Bibliothek verwenden (z. B. über den Start der Adobe Experience Platform), funktionieren alle mobilen Dimensionen standardmäßig.

## Beschreibungen der mobilen Dimension

>[!NOTE]
>
>Dimensionselemente, die als `"None"` Nicht-Mobilgeräte bezeichnet werden. Wenn Sie einen Bericht wünschen, der nur Mobilgeräte enthält, ziehen Sie die Dimension &quot;Mobilgerät&quot;in den Segmentbereich der Arbeitsfläche.

* **Mobile Audiounterstützung**: Legt die Dateiformate fest, die vom Gerät wiedergegeben werden können. Zu den Beispielwerten gehören `"MP3"`, `"AAC"`und `"MIDI Monophonic"`. Werte in dieser Dimension schließen sich nicht gegenseitig aus; Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.
* **Mobilnetzbetreiber**: Wenn der Benutzeragent ein netzwerkspezifisches Gerät enthält, ist der Netzbetreiber ein Dimensionselement. Zu den Beispielwerten gehören `"Reliance Jio"`, `"Airtel"`, `"Vodafone"`und `"Verizon"`.
* **Mobilgerät - Farbtiefe**: Die Farbtiefe des mobilen Geräts in Bit.
* **Unterstützung** von mobilen Cookies: Stellt fest, ob das Mobilgerät Cookies unterstützt. Dieser Bericht gibt nicht an, ob der Browser Cookies akzeptiert. Dimensionselemente umfassen `"Supported"`, `"Not supported"`und `"Unknown"`.
* **Mobilgerät**: Das Mobilgerät, das der Besucher verwendet.
* **Mobilgerätnummer**: Bestimmt, ob das Mobilgerät seine Nummer übermittelt. Dimensionselemente umfassen `"Supported"`, `"Not supported"`und `"Unknown"`.
* **Mobilgerätetyp**: Der Typ des Mobilgeräts. Zu den Beispielwerten gehören `"Mobile phone"`, `"Tablet"`, `"Media player"`und `"Gaming console"`.
* **Mobile DRM**: Der DRM-Typ, den das Mobilgerät unterstützt. Zu den Beispielwerten gehören `"DRM OMA forward"`, `"DRM OMA combined delivery"`und `"DRM OMA separate delivery"`.
* **Unterstützung** von mobilen Bildern: Die Arten von Bildern, die von Mobilgeräten unterstützt werden. Zu den Beispielwerten gehören `"PNG"`, `"JPEG"`und `"GIF 87"`. Werte in dieser Dimension schließen sich nicht gegenseitig aus; Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.
* **Mobile Informationsdienst**: Die vom Gerät unterstützten Arten von Nachrichtendiensten. Letzte Geräte melden diese Informationen normalerweise nicht.
* **Mobile Java VM**: Die Java-Versionen, die das Gerät unterstützt.
* **Mobilgerät - Mail-Dekoration**: Stellt fest, ob das Gerät Decomail unterstützt, eine Funktion, die auf japanischen Geräten bereits verwendet wird.
* **Mobilgerätehersteller**: Fasst Mobilgeräte nach Hersteller zusammen. Zu den Beispielwerten gehören `"Apple"`, `"Samsung"`, `"Huawei"`und `"Motorola"`.
* **Mobil max. Lesezeichenlänge**: Die maximale Anzahl von Bytes, die das Mobilgerät in mit Lesezeichen versehenen URLs unterstützt. Für neuere Geräte gibt es in der Regel keine Beschränkung.
* **Mobil max. Länge** der Browser-URL: Die maximale Anzahl von Bytes, die das Mobilgerät in URLs unterstützt. Für neuere Geräte gibt es in der Regel keine Beschränkung.
* **Mobil max. E-Mail-Länge**: Die maximale Anzahl von Bytes, die das Mobilgerät in einer E-Mail unterstützt. Für neuere Geräte gibt es in der Regel keine Beschränkung.
* **Mobilfunknetzprotokolle**: Die Protokolltypen, die das Gerät beim Zugriff auf das Internet unterstützt. Zu den Beispielwerten gehören `"EDGE"`, `"GPRS"`, `"UMTS"`und `"LTE"`.
* **Mobiles Betriebssystem (nicht mehr unterstützt)**: Verwenden Sie stattdessen die [Betriebssystemdimension](operating-systems.md) .
* **Mobile Push to Talk**: Bestimmt, ob das Gerät PTT (Push to Talk) unterstützt, wodurch das Mobilgerät sich ähnlich wie ein Zweiweg-Radio verhalten kann. Letzte Geräte melden diese Funktion normalerweise nicht.
* **Mobilgerät - Bildschirmhöhe**: Die Höhe des Bildschirms in Pixel. Beachten Sie, dass iPhones immer gemeldet werden, `"480"` weil die iPhone-Geräteversion nicht ermittelt werden kann. Informationen zum Bestimmen der iPhone-Geräteversion finden Sie im folgenden Abschnitt.
* **Mobilgerät - Bildschirmgröße**: Die vollständigen Abmessungen des Mobilgeräts in Pixel. Die Bildschirmgröße im Bericht lässt keine Rückschlüsse auf die Ausrichtung des Geräts zu. Jedes Gerät besitzt eine feste Bildschirmauflösung im Bericht, unabhängig von der Bildschirmausrichtung. Diese Größe beruht auf Untersuchungen, in denen ermittelt wurde, welche Ausrichtung am ehesten verwendet wird. You can see sizes such as `"768x1024"` and `"1024x768"` in the same report with each size representing one or more different devices.
* **Breite** des mobilen Bildschirms: Die Breite des Bildschirms in Pixel.
* **Unterstützung** von mobilen Videos: Die Videodateiformate und -codecs, die vom Mobilgerät unterstützt werden. Für verschiedene Codecs von MP4- und 3GPP-Dateien gibt es verschiedene Dimensionselemente. Werte in dieser Dimension schließen sich nicht gegenseitig aus; Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.

## Trennen des iPhone nach Modell oder Version

Mobilgeräte melden ihre Firmware-Version in der Benutzeragenten-Zeichenfolge, nicht in der Geräteversion. Beispielsweise enthält ein aktuelles gen iPhone einen identischen Benutzeragenten wie das iPhone der letzten Generation, wenn es sich auf derselben Firmware-Version befindet. Da es nicht möglich ist, die Geräteversion eines iPhones mit JavaScript zu bestimmen, gehören alle iPhones in denselben Behälter. Die Dimensionen für Mobilgeräte basieren strikt auf Lookups, die auf den Benutzeragenten verweisen. Daher werden Sie feststellen, dass alle iPhones eine Mobilgerät-Bildschirmgröße von `320 x 480`haben.

Wenn Sie die iPhone-Geräteversion erfassen möchten, gibt es zwei Möglichkeiten, diese Einschränkung zu umgehen.

* **Verwenden Sie das iOS-SDK**: Das mobile SDK enthält Dimensionen, die die Geräteversion für die Verwendung in Berichte verfügbar machen. Diese Methode eignet sich besser für mobile Apps als für Websites.
* **Verwenden Sie andere Variablen, die über JavaScript** verfügbar sind: Einige Variablen, wie `screen.height` und `screen.width`, können verwendet werden, um die Geräteversion abzuleiten. Sie könnten beispielsweise den folgenden Codeausschnitt auf Ihrer Site verwenden:

   ```js
   if (navigator.userAgent.indexOf('iPhone') > -1) {
     s.eVarXX = screen.width + "x" + screen.height;
     }
   ```

   Dieser Codeblock erkennt zunächst, ob es sich bei dem Gerät um ein iPhone handelt. Ist dies der Fall, verwendet der Code JavaScript, um die Bildschirmauflösung in eine eVar zu ziehen. Mit dieser Methode können Sie die Geräteversion ungefähr erkennen, wenn die Bildschirmauflösungen eindeutig sind.
