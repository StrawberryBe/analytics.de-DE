---
description: Anleitung zum Ausführen von Ad Hoc Analysis mit Java 11.
title: Ad Hoc Analysis mit Java 11 ausführen
translation-type: tm+mt
source-git-commit: d4cb2acb4ecaecce3644a2f3cf29913440e5cd6a
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 97%

---


# Ad Hoc Analysis mit Java 11 ausführen

>[!IMPORTANT]
>
>Die Adobe bringt Ad Hoc Analysis am 1. März 2021 in den Status als lebensbedrohlich. [Weitere Infos...](https://adobe.ly/discoverworkspace).

Wenn Sie Ad Hoc Analysis mit Java 11 ausführen, müssen Sie im Vergleich zu Java 8 zusätzliche Schritte ausführen.

## Voraussetzungen

Arbeiten Sie mit Ihrem IT-Team zusammen, um sicherzustellen, dass Folgendes erfüllt ist:

* Java 11 muss mit der Umgebungsvariablen *JAVA_HOME* installiert sein
* JavaFX muss installiert sein, wobei die Umgebungsvariable *PATH_TO_FX_SDK* auf das JavaFX SDK-Verzeichnis verweist. Zum Beispiel *PATH_TO_FX_SDK=/homedir/javafx-sdk-11.0.2* auf einem Mac oder *PATH_TO_FX_SDK=C:\Users\username\javafx-sdk-11.0.2* auf einem PC.

## Ad Hoc Analysis für Java 11 installieren

1. Gehen Sie zu **[!UICONTROL Analyse > Werkzeuge > Ad Hoc Analysis]**.
1. Klicken Sie auf **[!UICONTROL Ad Hoc Analysis (Java 11)]**. Dadurch wird eine Zip-Datei heruntergeladen.
1. Extrahieren Sie die heruntergeladene Datei.
1. **Wählen Sie die Datei .bat (PC) oder .sh (Mac)**. Wählen Sie die entsprechende Rechenzentrumsdatei aus, indem Sie nach der Nummer in der Adobe Analytics-URL nach „sc“ suchen. (3 = LON, 4 = SIN, 5 = PNW) Wenn Sie einen PC verwenden, überprüfen Sie, ob Sie ein 32-Bit- oder ein 64-Bit-Windows-Betriebssystem verwenden, indem Sie zu „Über Ihren PC“ gehen. Wählen Sie dann die entsprechende .bat-Datei aus.
1. **Führen Sie die ausgewählte Datei aus**. Für PC: Doppelklicken Sie auf die .bat-Datei. Für Mac: Klicken Sie mit der rechten Maustaste auf die .sh-Datei und wählen Sie anschließend **[!UICONTROL Öffnen mit > Sonstige... > Dienstprogramme > (Alle Anwendungen aktivieren) > Terminal auswählen > Öffnen]**.
1. Melden Sie sich bei Ad Hoc Analysis an.

>[!NOTE]
>
>Die Authentifizierungsmethoden für Verbund- und Enterprise IDs werden in der Java 11-Version der Ad Hoc Analysis nicht unterstützt.

## Nicht unterstützte Funktionen in der Ad Hoc Analysis (Java 11)

Es gibt einige bekannte Einschränkungen in der mit Ad Hoc Analysis kompatiblen Java 11-Version:

* Authentifizierungsmethoden für Verbund- und Enterprise IDs werden nicht unterstützt.
* Linux-Betriebssysteme werden nicht unterstützt.
* Verwenden Sie bei Verwendung eines Mac nicht das Mac-Anwendungsmenü (einschließlich *cmd + Q*). Dies kann dazu führen, dass die Ad Hoc Analysis ohne Vorwarnung geschlossen wird. Verwenden Sie stattdessen das Menü innerhalb der Ad Hoc Analysis.
* Die Visualisierung der Site-Analyse wird bei der Ausführung der Ad Hoc Analysis unter MacOS nicht unterstützt.

## Häufig gestellte Fragen

**F: Ich erhalte die Fehlermeldung „\bin\javaw kann nicht gefunden werden“ (Beispiel unten). Was soll ich tun?**

![](/help/analyze/ad-hoc-analysis/assets/error-java.png)

A: Wenn dieser Fehler auftritt, wenden Sie sich an Ihr IT-Team, um die Umgebungsvariable *JAVA_HOME* zu definieren, die zum Ausführen der Ad Hoc Analysis in Java 11 erforderlich ist.
