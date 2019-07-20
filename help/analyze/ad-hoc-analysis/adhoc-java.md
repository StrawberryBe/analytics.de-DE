---
description: Anleitung zum Ausführen von Ad-hoc-Analysen mit Java 11.
seo-description: Anleitung zum Ausführen von Ad-hoc-Analysen mit Java 11.
seo-title: Ad-hoc-Analysen und Java 11
title: Ad-hoc-Analysen mit Java 11 ausführen
translation-type: tm+mt
source-git-commit: 23bdb0c24416c376ec1df7b609a5794dbf8886f2

---


# Ad-hoc-Analysen mit Java 11 ausführen

Wenn Sie Ad Hoc Analysis mit Java 11 ausführen, müssen Sie im Vergleich zu Java 8 zusätzliche Schritte ausführen.

## Voraussetzungen

Arbeiten Sie mit Ihrem IT-Team zusammen, um sicherzustellen, dass Folgendes erfüllt ist:

* Java 11 must be installed, with *JAVA_HOME* environment variable set
* JavaFX muss installiert sein, wobei die Umgebungsvariable *PATH_TO_FX_SDK* auf das JavaFX SDK-Verzeichnis verweist. Zum Beispiel *PATH_TO_FX_SDK=/homedir/javafx-sdk-11.0.2* auf einem Mac oder *PATH_TO_FX_SDK=C:\Users\username\javafx-sdk-11.0.2* auf einem PC.

## Ad Hoc Analysis für Java 11 installieren

1. Gehen Sie zu **[!UICONTROL Analyse &gt; Werkzeuge &gt; Ad Hoc Analysis]**.
1. Klicken Sie auf **[!UICONTROL Ad Hoc Analysis (Java 11)]**. Dadurch wird eine Zip-Datei heruntergeladen.
1. Extrahieren Sie die heruntergeladene Datei.
1. **Wählen Sie die Datei .bat (PC) oder .sh (Mac)**. Wählen Sie die entsprechende Rechenzentrumsdatei aus, indem Sie die Nummer in der Adobe Analytics-URL nach „sc“ überprüfen. (3 = LAM, 4 = SIN, 5 = PNW) Überprüfen Sie, ob Sie ein 32-Bit- oder ein 64-Bit-Windows-Betriebssystem ausführen, indem Sie zu "Über Ihr PC" navigieren. Wählen Sie dann die entsprechende .bat-Datei aus.
1. **Führen Sie die ausgewählte Datei aus**. Für PC: Doppelklicken Sie auf die .bat-Datei. Für Mac: Klicken Sie mit der rechten Maustaste auf die .sh-Datei und wählen Sie anschließend **[!UICONTROL Öffnen mit &gt; Sonstige...  &gt; Dienstprogramme &gt; (Alle Anwendungen aktivieren) &gt; Terminal auswählen &gt; Öffnen]**.
1. Melden Sie sich bei Ad Hoc Analysis an.

>[!Note]
>
> Federated and Enterprise ID Authentication Methods sind nicht mit der Java 11-Version der Ad-hoc-Analysen kompatibel.

## Nicht unterstützte Funktionen in der Ad Hoc Analysis (Java 11)

In der mit Ad-hoc-Analysen kompatiblen Version Java 11 gibt es einige bekannte Einschränkungen:

* Authentifizierungsmethoden für Verbund- und Enterprise IDs werden nicht unterstützt.
* Linux-Betriebssysteme werden nicht unterstützt.
* When using a Mac, do not use the Mac application menu (including *cmd + Q*). Dies kann dazu führen, dass die Ad Hoc Analysis ohne Vorwarnung geschlossen wird. Verwenden Sie stattdessen das Menü innerhalb der Ad Hoc Analysis.
* Die Visualisierung der Site-Analyse wird bei der Ausführung der Ad Hoc Analysis unter MacOS nicht unterstützt.

## FAQs

**Q: Ich erhalte den Fehler "Kann\ bin\ javaw nicht finden" (Beispiel unten) - was soll ich tun?**

![](/help/analyze/ad-hoc-analysis/assets/error-java.png)

A: Wenn dieser Fehler auftritt, arbeiten Sie mit Ihrem IT-Team zusammen, um die Umgebungsvariable *JAVA_HOME* festzulegen, die zum Ausführen der Ad Hoc Analysis in Java 11 erforderlich ist.