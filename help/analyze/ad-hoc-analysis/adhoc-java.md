---
description: Anleitung zum Ausführen von Ad Hoc Analysis mit Java 11.
title: Ad Hoc Analysis mit Java 11 ausführen
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Ad Hoc Analysis mit Java 11 ausführen

Sie müssen beim Ausführen von Ad-hoc-Analysen mit Java 11 im Vergleich zum Ausführen mit Java 8 weitere Schritte ausführen.

## Voraussetzungen

Arbeiten Sie mit Ihrem IT-Team zusammen, um Folgendes sicherzustellen:

* Java 11 muss mit der Umgebungsvariablen *JAVA_HOME* installiert sein
* JavaFX muss installiert werden, wobei die Variable *PATH_TO_FX_SDK* -Umgebung auf den JavaFX SDK-Ordner verweist. Beispiel: *PATH_TO_FX_SDK=/homedir/javafx-sdk-11.0.2* auf einem Mac oder *PATH_TO_FX_SDK=C:\Users\username\javafx-sdk-11.0.2* auf einem PC.

## Ad-hoc-Analysen für Java 11 installieren

1. Öffnen von **[!UICONTROL Analytics > Tools > Ad Hoc Analysis]**.
1. Klicken Sie auf **[!UICONTROL Ad Hoc Analysis (Java 11)]**. Dadurch wird eine ZIP-Datei heruntergeladen.
1. Dekomprimieren Sie die heruntergeladene Datei.
1. **Wählen Sie die .bat-Datei (PC) oder die .sh-Datei (Mac) aus**. Wählen Sie die entsprechende Rechenzentrumsdatei aus, indem Sie nach der Nummer in der Adobe Analytics-URL nach „sc“ suchen. (3 = LON, 4 = SIN, 5 = PNW) Wenn Sie einen PC verwenden, überprüfen Sie, ob Sie ein 32-Bit- oder ein 64-Bit-Windows-Betriebssystem verwenden, indem Sie zu „Über Ihren PC“ gehen. Wählen Sie dann die entsprechende .bat-Datei aus.
1. **Führen Sie die ausgewählte Datei** aus. Für PC: Doppelklicken Sie auf die .bat-Datei. Mac: Klicken Sie mit der rechten Maustaste auf die .sh-Datei und wählen Sie **[!UICONTROL Open With > Other... > Utilities > (Enable all applications) > select Terminal > Open]**.
1. Melden Sie sich bei Ad Hoc Analysis an.

>[!NOTE] Die Authentifizierungsmethoden für Verbund- und Enterprise IDs werden in der Java 11-Version der Ad Hoc Analysis nicht unterstützt.

## Nicht unterstützte Funktionen in der Ad Hoc Analysis (Java 11)

Es gibt einige bekannte Einschränkungen in der mit Ad Hoc Analysis kompatiblen Java 11-Version:

* Authentifizierungsmethoden für Federated &amp; Enterprise ID werden nicht unterstützt.
* Linux-Betriebssysteme werden nicht unterstützt.
* Verwenden Sie bei Verwendung eines Mac nicht das Mac-Anwendungsmenü (einschließlich *cmd + Q*). Dies kann dazu führen, dass Ad-hoc-Analysen ohne Vorwarnung geschlossen werden. Verwenden Sie stattdessen das Menü in der Ad-hoc-Analyse.
* Die Visualisierung der Site-Analyse wird nicht unterstützt, wenn Ad-hoc-Analysen unter MacOS ausgeführt werden.

## FAQs

**F: Ich erhalte die Fehlermeldung „\bin\javaw kann nicht gefunden werden“ (Beispiel unten). Was soll ich tun?**

![](/help/analyze/ad-hoc-analysis/assets/error-java.png)

A: Wenn dieser Fehler auftritt, wenden Sie sich an Ihr IT-Team, um die Umgebungsvariable *JAVA_HOME* zu definieren, die zum Ausführen der Ad Hoc Analysis in Java 11 erforderlich ist.
