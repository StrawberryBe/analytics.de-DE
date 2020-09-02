---
description: Erfahren Sie, wie Sie Verarbeitungsregeln für Mobile Services auf Adobe Analytics migrieren.
title: Migrieren von Verarbeitungsregeln für Mobile Services auf Adobe Analytics
translation-type: tm+mt
source-git-commit: bdb6f9ba435513cd1dc3febf35eae0e821c756ca
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 18%

---


# Migrieren von Verarbeitungsregeln für Mobile Services auf Adobe Analytics

Mit dem bevorstehenden (noch unangekündigten) Auslauf der Adobe Mobile Services-Funktionalität erhalten Sie in diesem Dokument Anweisungen zur Migration zusätzlicher Verarbeitungsregeln - über Lebenszyklusmetriken hinaus -, die Sie in der Mobile Services-Benutzeroberfläche nach Adobe Analytics erstellt haben.

Verarbeitungsregeln werden verwendet, um Werte von Kontextdatenvariablen in props und eVars zu verschieben. Sie können beispielsweise den Wert einer Kontextdatenvariablen für &quot;Suchbegriff&quot;in den Wert einer Commerce-Variablen-eVar setzen und diesen Wert bei jedem Treffer überschreiben. Ohne Verarbeitungsregeln sind Kontextdatenvariablen bedeutungslos und füllen keine Berichte in Analytics aus.

## Verarbeitungsregeln migrieren

Wenn Sie Mobile Services für zusätzliche Funktionen wie Verarbeitungsregeln und Funktionen des Berichte nutzen, können Sie zur Ausführung dieser Funktionen nahtlos zur Analytics-Benutzeroberfläche (Benutzeroberfläche für Verarbeitungsregeln oder Analysis Workspace) wechseln. Für Lebenszyklusmetriken oder Regeln, die in der Benutzeroberfläche der Verarbeitungsregeln eingerichtet wurden, müssen Sie keine Migration durchführen. Lebenszyklusmetriken sind vordefinierte Metriken, die automatisch erfasst werden, wenn das Mobile SDK zum ersten Mal in Ihrer App implementiert wird.

Wenn Sie jedoch zusätzliche Verarbeitungsregeln in der Mobile Services-Benutzeroberfläche (über Lebenszyklusmetriken hinaus) einrichten, sollten Sie diese migrieren, damit Sie sie in Analytics bearbeiten/löschen können, nachdem Sie den Zugriff auf Mobile Services verloren haben.

1. Melden Sie sich bei experience.adobe.com an und gehen Sie zu Mobile Services.
1. Klicken Sie auf das Zahnradsymbol einer mobilen App, deren Kontextvariablenzuordnungen Sie nach Adobe Analytics migrieren möchten.
1. Klicken Sie auf das Menüelement Variablen und Metriken **[!UICONTROL verwalten]** und dann auf die Registerkarte **[!UICONTROL Benutzerspezifische Variablen]** . Hier können Sie sehen, welche Kontextvariablenzuordnungen (Kontextdaten) zur Konfiguration hinzugefügt wurden. Notieren Sie sich diese Konfigurationen (oder machen Sie einen Screenshot). Beispiel:

   ![Kontextvariable](assets/context-var.png)

1. Wechseln Sie in Experience Cloud zu Adobe Analytics und stellen Sie sicher, dass Sie sich in derselben Mobil-Report Suite befinden, die Sie auch in Mobile Services angesehen haben.
1. Gehen Sie zu Admin > Report Suites > Einstellungen bearbeiten > Allgemein > Verarbeitungsregeln.
1. Klicken Sie auf Regel hinzufügen.
1. Ignorieren Sie die Bedingungen und fügen Sie die gleichen Kontextvariablen hinzu, die in Mobile Services vorhanden sind/sind.

   ![Verarbeitungsregel](assets/proc-rule.png)

## Berichte zur Mobilnutzung in Analysis Workspace

Zusätzlich zu den Metriken und Dimensionen für Mobilgeräte (sofern die Report Suite für Mobile Services aktiviert ist) enthält Analysis Workspace mehrere Mobile-Projektvorlagen, die die Analyse erleichtern können:

* Messaging: Mit Augenmerk auf die Leistung von In-App- und Push-Nachrichten
* Standort: Beinhaltet eine Karte zur Anzeige von Standortdaten
* Schlüsselmetriken: Sehen Sie sich die wichtigsten Metriken Ihrer App genauer an.
* App-Nutzung: Wie viele App-Benutzer, Starts und erste Starts hat die App verzeichnet und wie lange dauerte eine durchschnittliche Sitzung?
* Akquise: Wie funktionieren mobile Akquise-Links?
* Leistung: Welche Leistung erzielt die Anwendung und wo haben Benutzer Probleme?
* Bindungsgrad: Wer sind meine treuen Benutzer und was tun sie?
* Journeys: Welche markanten Verwendungsmuster weist meine App auf?

Im Folgenden finden Sie einen Ausschnitt der Vorlage zur Verwendung mobiler Apps:

![Mobile App-Nutzung](assets/mobile-app-usage.png)

So greifen Sie auf die Vorlagen zu:

1. Melden Sie sich bei experience.adobe.com an und wählen Sie Analytics aus.
1. Vergewissern Sie sich, dass Sie sich in einer Report Suite befinden, die für Mobile Services aktiviert ist.
1. Klicken Sie auf die Registerkarte Arbeitsbereich.
1. Klicken Sie auf Neues Projekt erstellen.
1. Wählen Sie eine der Mobile-Vorlagen aus und klicken Sie auf Erstellen.

## Andere Mobile Services-Funktionen migrieren

Die folgende Mobile Services-Funktion ist auch mit Adobe Analytics verbunden, erfordert jedoch eine erworbene Adobe Analytics-SKU:

* Akquise-Links
* Push-Benachrichtigung
* In-App-Nachrichten
* Verwaltung von Standorten

Wenn Sie Mobile Services für gebührenpflichtige Funktionen nutzen, haben Sie keinen brauchbaren Migrationspfad zu anderen internen/externen Werkzeugen:

* Für Akquise-Links können wir Sie zu Adobe Partners weiterleiten, um Ihre Bedürfnisse zu befriedigen.
* Push-Nachrichten und In-App-Nachrichten finden sich zwar in Adobe Campaign Standard und Adobe Campaign Classic (nur Push), der zugrunde liegende Datensatz für das Targeting ist jedoch anders und es ist keine Migration von Daten oder Nachrichten-Aktivitäten möglich.
* Für die Funktion Location sollten Sie den neuen [Adobe Experience Platform Location Service](https://www.adobe.com/experience-platform/location-service.html)übernehmen, der für alle AEP-Kunden kostenlos ist.
