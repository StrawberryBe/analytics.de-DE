---
title: Listenvariablen
description: Erstellen und konfigurieren Sie Listenvariablen für die Verwendung in Berichten.
exl-id: 6d9a52d4-e7f3-4bbc-bad4-55c79f30b9f7
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '496'
ht-degree: 100%

---

# Listenvariablen

Erstellen und konfigurieren Sie Listenvariablen für die Verwendung in Berichten. Legen Sie hier Trennzeichen, Ablauf, Zuordnung und Höchstwert fest.

Sie können auf die Konfiguration in der Admin Console zugreifen:

1. Navigieren Sie zu: **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
2. Wählen Sie die Report Suite aus.
3. Klicken Sie auf **[!UICONTROL Einstellungen bearbeiten]** > **[!UICONTROL Konversion]** > **[!UICONTROL Listenvariablen]**.

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
