---
description: Erfahren Sie, wie Sie Verarbeitungsregeln für Mobile Services auf Adobe Analytics migrieren.
title: Migrieren von Verarbeitungsregeln für Mobile Services auf Adobe Analytics
translation-type: tm+mt
source-git-commit: d6601640d06f65dd1ddd09cb9bde0267df20eec3
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 6%

---


# Migrieren von Verarbeitungsregeln für Mobile Services auf Adobe Analytics

In diesem Dokument erhalten Sie Anweisungen zur Migration zusätzlicher Verarbeitungsregeln - über Lebenszyklusmetriken hinaus -, die Sie in der Mobile Services-Benutzeroberfläche nach Adobe Analytics erstellt haben.

Verarbeitungsregeln werden verwendet, um Werte von Kontextdatenvariablen in props und eVars zu verschieben. Sie können beispielsweise den Wert einer Kontextdatenvariablen für &quot;Suchbegriff&quot;in den Wert einer Commerce-Variablen-eVar setzen und diesen Wert bei jedem Treffer überschreiben. Ohne Verarbeitungsregeln sind Kontextdatenvariablen bedeutungslos und füllen keine Berichte in Analytics aus.

Dieses Dokument zeigt Ihnen auch, wie Sie Berichte zur Mobilnutzung in Analysis Workspace durchführen.

## Verarbeitungsregeln migrieren

Wenn Sie Mobile Services für zusätzliche Funktionen wie Verarbeitungsregeln und Funktionen des Berichte nutzen, können Sie zur Ausführung dieser Funktionen nahtlos zur Analytics-Benutzeroberfläche (Benutzeroberfläche für Verarbeitungsregeln oder Analysis Workspace) wechseln. Für Lebenszyklusmetriken oder Regeln, die in der Benutzeroberfläche der Verarbeitungsregeln eingerichtet wurden, müssen Sie keine Migration durchführen. Lebenszyklusmetriken sind vordefinierte Metriken, die automatisch erfasst werden, wenn das Mobile SDK zum ersten Mal in Ihrer App implementiert wird.

Wenn Sie jedoch zusätzliche Verarbeitungsregeln in der Mobile Services-Benutzeroberfläche (über Lebenszyklusmetriken hinaus) einrichten, sollten Sie diese migrieren, damit Sie sie in Analytics bearbeiten/löschen können, nachdem Sie den Zugriff auf Mobile Services verloren haben.

1. Log in to `experience.adobe.com` and go to Mobile Services.
1. Klicken Sie auf das Zahnradsymbol einer mobilen App, deren Kontextvariablenzuordnungen Sie nach Adobe Analytics migrieren möchten.
1. Klicken Sie auf das Menüelement Variablen und Metriken **[!UICONTROL verwalten]** und dann auf die Registerkarte **[!UICONTROL Benutzerspezifische Variablen]** . Hier können Sie sehen, welche Kontextvariablenzuordnungen (Kontextdaten) zur Konfiguration hinzugefügt wurden. Notieren Sie sich diese Konfigurationen (oder machen Sie einen Screenshot). Beispiel:

   ![Kontextvariable](assets/context-var.png)

1. Wechseln Sie in Experience Cloud zu Adobe Analytics und stellen Sie sicher, dass Sie sich in derselben Mobil-Report Suite befinden, die Sie auch in Mobile Services angesehen haben.
1. Gehen Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Einstellungen **[!UICONTROL bearbeiten]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Verarbeitungsregeln]**.
1. Klicken Sie auf **[!UICONTROL Regel hinzufügen]**.
1. Ignorieren Sie die Bedingungen und fügen Sie die gleichen Kontextvariablen hinzu, die in Mobile Services vorhanden sind/sind.

   ![Verarbeitungsregel](assets/proc-rule.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

## Berichte zur Mobilnutzung in Analysis Workspace

Zusätzlich zu den Metriken und Dimensionen für Mobilgeräte (sofern die Report Suite für Mobile Services aktiviert ist) enthält Analysis Workspace mehrere Mobile-Projektvorlagen, die die Analyse erleichtern können:

* **[!UICONTROL Messaging]**: Konzentriert sich auf die Leistung von In-App- und Push-Nachrichten.
* **[!UICONTROL Ort]**: Beinhaltet eine Karte, die Standortdaten anzeigt.
* **[!UICONTROL Schlüsselmetriken]**: Halten Sie einen Impuls für die Schlüsselmetriken Ihrer App.
* **[!UICONTROL App-Nutzung]**: Wie viele App-Benutzer, -Starts und -Erststarts hat die App gehabt und wie lange war die durchschnittliche Sitzungslänge?
* **[!UICONTROL Akquise]**: Wie funktionieren mobile Akquise-Links?
* **[!UICONTROL Leistung]**: Wie funktioniert die App und wo haben Benutzer Probleme?
* **[!UICONTROL Treue]**: Wer sind meine treuen Benutzer und was tun sie?
* **[!UICONTROL Reisen]**: Welches sind die markanten Verwendungsmuster für meine App?

Im Folgenden finden Sie einen Ausschnitt der Vorlage zur Verwendung mobiler Apps:

![Mobile App-Nutzung](assets/mobile-app-usage.png)

So greifen Sie auf die Vorlagen zu:

1. Log in to `experience.adobe.com` and select Analytics.
1. Vergewissern Sie sich, dass Sie sich in einer Report Suite befinden, die für Mobile Services aktiviert ist.
1. Click the **[!UICONTROL Workspace]** tab.
1. Klicken Sie auf **[!UICONTROL Neues Projekt erstellen]**.
1. Wählen Sie eine der Mobile-Vorlagen aus und klicken Sie auf **[!UICONTROL Erstellen]**.

## Andere Mobile Services-Funktionen migrieren

Die folgende Mobile Services-Funktion ist auch mit Adobe Analytics verbunden, erfordert jedoch eine erworbene Adobe Analytics-SKU:

* Akquise-Links
* Push-Benachrichtigung
* In-App-Nachrichten
* Verwaltung von Standorten

Wenn Sie Mobile Services für gebührenpflichtige Funktionen nutzen, haben Sie keinen brauchbaren Migrationspfad zu anderen internen/externen Werkzeugen:

* Für Akquise-Links können wir Sie zu Adobe Partners weiterleiten, um Ihre Bedürfnisse zu befriedigen.
* Push-Nachrichten und In-App-Nachrichten sind in Adobe Campaign Standard und Adobe Campaign Classic verfügbar (nur Push). Der für das Targeting verwendete Datensatz ist jedoch anders. Wir empfehlen, mit Ihrem Adoben-Kontoteam zusammenzuarbeiten, um Migrationsoptionen für Nachrichtendaten zu ermitteln.
* Für die Funktion Location sollten Sie den neuen [Adobe Experience Platform Location Service](https://www.adobe.com/experience-platform/location-service.html)übernehmen, der für alle AEP-Kunden kostenlos ist.
