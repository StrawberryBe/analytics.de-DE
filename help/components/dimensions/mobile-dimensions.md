---
title: Mobile Suchdimensionen
description: Dimensionen basierend auf der IP-Adresse und dem Benutzeragenten des Geräts.
feature: Dimensions
exl-id: fa460888-513d-4d14-93b1-33d308e0758a
source-git-commit: e32821dd3f30404166554b8437c508172e4764e5
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 60%

---

# Mobile Suchdimensionen

*Auf dieser Seite werden die Eigenschaften von Mobilgeräten beschrieben, die auf Ihre Website zugreifen. Siehe [Mobile Lebenszyklusdimensionen](lifecycle-dimensions.md) oder [Mobile Lebenszyklusmetriken](../metrics/lifecycle-metrics.md) für das Tracking in einer mobilen App.*

Mobile-Suche [Dimensionen](overview.md) bieten Einblicke in die Eigenschaften von Mobilgeräten, die Ihre Site besuchen. Diese Eigenschaften basieren auf dem Benutzeragenten und der IP-Adresse des Treffers. Sie können diese Dimensionen verwenden, um zu verstehen, welche Funktionen ein Mobilgerät unterstützt.

## Füllen dieser Dimensionen mit Daten

Diese Dimensionen verweisen auf interne Suchregeln von Adobe.

* Für [!UICONTROL Mobilnetzbetreiber] Dimension, Adobe-Partner mit [Digitales Element](https://www.digitalelement.com/) Verwendung von NetActivity zur Pflege der Suche zwischen IP-Adresse und Mobilnetzbetreiber.
* Für alle anderen Mobilgerätedimensionen arbeitet Adobe mit [DeviceAtlas](https://deviceatlas.com/) , um die Suche zwischen dem Benutzeragenten und den jeweiligen Mobilgerätedimensionen zu gewährleisten.

Die Verfügbarkeit dieser Dimensionen hängt vom Implementierungstyp ab:

* Bei AppMeasurement-Implementierungen sind diese Dimensionen vorkonfiguriert.
* Aktivieren Sie für Web SDK-Implementierungen [!UICONTROL Geo-Suche] (für Mobilnetzbetreiber) oder [!UICONTROL Gerätesuche] (für alle anderen Dimensionen) wann [Konfigurieren eines Datenspeichers](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=de).

## Beschreibung der Mobilgerätedimensionen

>[!NOTE]
>
>Mit `"None"` gekennzeichnete Dimensionselemente sind keine Mobilgeräte. Wenn Sie einen Bericht wünschen, der nur Mobilgeräte enthält, ziehen Sie die Dimension „Mobilgerät“ in den Segmentbereich der Arbeitsfläche von Workspace.

* **[!UICONTROL Mobilgerät – Audio-Unterstützung]**: Stellt die Dateiformate fest, die vom Gerät wiedergegeben werden können. Zu den Beispielwerten gehören `"MP3"`, `"AAC"` und `"MIDI Monophonic"`. Die Werte in dieser Dimension schließen sich nicht gegenseitig aus. Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.
* **[!UICONTROL Mobilnetzbetreiber]**: Das Telefon oder der Datenanbieter für das Gerät. Zu den Beispielwerten gehören `"Reliance Jio"`, `"Airtel"`, `"Vodafone"` und `"Verizon"`.
* **[!UICONTROL Mobilgerät – Farbtiefe]**: Die Farbtiefe des Mobilgeräts in Bit.
* **[!UICONTROL Mobilgerät – Cookie-Unterstützung]**: Stellt fest, ob das Mobilgerät Cookies unterstützt. Diese Dimension gibt nicht an, ob der Browser Cookies akzeptiert. Zu den Dimensionselementen gehören `"Supported"`, `"Not supported"` und `"Unknown"`.
* **[!UICONTROL Mobilgerät]**: Das Mobilgerät, das der Besucher verwendet.
* **[!UICONTROL Mobilgerätenummer]**: Stellt fest, ob das Mobilgerät seine Nummer übermittelt. Diese Dimension stellt nicht die Mobiltelefonnummer selbst bereit. Zu den Dimensionselementen gehören `"Supported"`, `"Not supported"` und `"Unknown"`.
* **[!UICONTROL Mobilgerätetyp]**: Der Typ des Mobilgeräts. Zu den Beispielwerten gehören `"Mobile phone"`, `"Tablet"`, `"Media player"` und `"Gaming console"`.
* **[!UICONTROL Mobil-DRM]**: Der DRM-Typ, den das Mobilgerät unterstützt. Zu den Beispielwerten gehören `"DRM OMA forward"`, `"DRM OMA combined delivery"` und `"DRM OMA separate delivery"`.
* **[!UICONTROL Mobilgerät - Bildunterstützung]**: Die Bildtypen, die vom Mobilgerät unterstützt werden. Zu den Beispielwerten gehören `"PNG"`, `"JPEG"` und `"GIF 87"`. Die Werte in dieser Dimension schließen sich nicht gegenseitig aus. Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.
* **[!UICONTROL Mobile Informationsdienste]**: Die vom Gerät unterstützten Arten von Nachrichtendiensten. Moderne Geräte melden diese Informationen normalerweise nicht.
* **[!UICONTROL Mobile Java-VM]**: Die Java-Versionen, die das Gerät unterstützt.
* **[!UICONTROL Mobilgerät - Mail-Dekoration]**: Stellt fest, ob das Gerät unterstützt [Decom](https://en.wikipedia.org/wiki/Decome), eine Funktion, die einst auf japanischen Geräten beliebt war.
* **[!UICONTROL Mobilgeräthersteller]**: Klassifiziert Mobilgeräte nach Hersteller. Zu den Beispielwerten gehören `"Apple"`, `"Samsung"`, `"Huawei"` und `"Motorola"`.
* **[!UICONTROL Maximale mobile Lesezeichenlänge]**: Die maximale Anzahl von Byte, die das Mobilgerät in mit Lesezeichen versehenen URLs unterstützt. Moderne Geräte haben in der Regel keine Beschränkung.
* **[!UICONTROL Maximale mobile Browser-URL-Länge]**: Die maximale Anzahl von Byte, die das Mobilgerät in URLs unterstützt. Moderne Geräte haben in der Regel keine Beschränkung.
* **[!UICONTROL Maximale mobile E-Mail-Länge]**: Die maximale Anzahl von Byte, die das Mobilgerät in E-Mails unterstützt. Moderne Geräte haben in der Regel keine Beschränkung.
* **[!UICONTROL Mobile Netzprotokolle]**: Die Protokolltypen, die das Gerät beim Zugriff auf das Internet unterstützt. Zu den Beispielwerten gehören `"EDGE"`, `"GPRS"`, `"UMTS"` und `"LTE"`.
* **[!UICONTROL Mobiles Betriebssystem (veraltet)]**: Verwenden Sie stattdessen die Dimension [Betriebssystem](operating-systems.md).
* **[!UICONTROL Mobiles PTT]**: Stellt fest, ob das Gerät PTT (Push to Talk) unterstützt, wodurch das Mobilgerät sich ähnlich wie ein Funkgerät verhalten kann. Moderne Geräte melden diese Funktion normalerweise nicht.
* **[!UICONTROL Mobilgerät – Bildschirmhöhe]**: Die Höhe des Bildschirms in Pixel. iPhones-Bericht immer `"480"` aufgrund der Unfähigkeit, die iPhone-Geräteversion zu ermitteln. Informationen zum Bestimmen der iPhone-Geräteversion finden Sie im folgenden Abschnitt.
* **[!UICONTROL Mobilgerät – Bildschirmgröße]**: Die vollständigen Abmessungen des Mobilgeräts in Pixel. Die Bildschirmgröße im Bericht lässt keine Rückschlüsse auf die Ausrichtung des Geräts zu. Jedes Gerät besitzt eine feste Bildschirmauflösung im Bericht, unabhängig von der Bildschirmausrichtung. Diese Größe beruht auf Untersuchungen, in denen ermittelt wurde, welche Ausrichtung am ehesten verwendet wird. Sie können Größen wie `"768x1024"` und `"1024x768"` im selben Bericht sehen, wobei jede Größe ein oder mehrere verschiedene Geräte repräsentiert.
* **[!UICONTROL Mobilgerät – Bildschirmbreite]**: Die Breite des Bildschirms in Pixel.
* **[!UICONTROL Mobilgerät – Video-Unterstützung]**: Die Videodateiformate und Codecs, die vom Mobilgerät unterstützt werden. Für verschiedene Codecs von MP4- und 3GPP-Dateien existieren verschiedene Dimensionselemente. Die Werte in dieser Dimension schließen sich nicht gegenseitig aus. Ein einzelner Treffer kann mehreren Dimensionselementen zugeordnet werden.

## Aufteilen von iPhone-Geräten nach Modell oder Version

Mobilgeräte melden ihre Firmware-Version in ihrer Benutzeragenten-Zeichenfolge, nicht die Geräteversion. Beispielsweise enthält ein iPhone der aktuellen Generation einen identischen Benutzeragenten wie das iPhone der letzten Generation, wenn sie dieselbe Firmware-Version verwenden. Da es nicht möglich ist, die Geräteversion eines iPhone mit JavaScript zu bestimmen, gehören alle iPhones in denselben Behälter. Mobilgerätedimensionen basieren ausschließlich auf Suchvorgängen, die auf den Benutzeragenten verweisen. Dies führt dazu, dass alle iPhones eine Bildschirmgröße von Mobilgeräten von `320 x 480`.

Wenn Sie die iPhone-Geräteversion erfassen möchten, gibt es zwei Möglichkeiten, diese Einschränkung zu umgehen.

* **Mobile SDK verwenden**: Das Mobile SDK enthält Dimensionen, die die Geräteversion zur Verwendung in Berichten verfügbar machen. Diese Methode eignet sich besser für Mobile Apps als für Websites.
* **Verwenden andere Variablen, die über JavaScript verfügbar sind**: Einige Variablen, wie `screen.height` und `screen.width`, können verwendet werden, um die Geräteversion abzuleiten. Sie könnten beispielsweise den folgenden Code-Ausschnitt auf Ihrer Site verwenden:

  ```js
  if (navigator.userAgent.indexOf('iPhone') > -1) {
    s.eVarXX = screen.width + "x" + screen.height;
    }
  ```

  Dieser Code-Block erkennt zunächst, ob es sich bei dem Gerät um ein iPhone handelt. Ist dies der Fall, verwendet der Code JavaScript, um die Bildschirmauflösung in eine eVar zu ziehen. Mit dieser Methode können Sie die Geräteversion ungefähr erkennen, wenn die Bildschirmauflösungen eindeutig sind.
