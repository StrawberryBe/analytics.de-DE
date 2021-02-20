---
title: Adobe Analytics in einer Entwicklungsumgebung bereitstellen
description: Erfahren Sie, wie Sie Adobe Experience Platform Launch verwenden, um Adobe Analytics in Ihrer Entwicklungsumgebung bereitzustellen.
translation-type: tm+mt
source-git-commit: 365944140bb1dfc9bc8669ae530c631e8ff1629b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 100%

---


# Analytics-Implementierung in einer Entwicklungsumgebung bereitstellen

Nachdem eine Eigenschaft in Launch erstellt und konfiguriert wurde, können die Bibliotheken bereitgestellt und Code auf Ihrer Website implementiert werden.

## Voraussetzungen

[Erstellen und konfigurieren Sie eine Eigenschaft für Adobe Analytics in Launch](create-analytics-property.md): Greifen Sie auf das Tool zu und erstellen Sie einen Raum für Ihre Analytics-Implementierung.

## Erstellen von Adaptern und Umgebungen

Launch ermöglicht die Bereitstellung von Code mit vielen organisatorischen Arbeitsabläufen. Führen Sie die folgenden Schritte aus, um die erforderlichen Mindestkomponenten für eine Analytics-Implementierung zu erstellen. Als Launch-Administrator können Sie innerhalb Ihres Unternehmens den richtigen Arbeitsablauf für die Bereitstellung von Adobe-Lösungen festlegen.

1. Wechseln Sie zu [Adobe Experience Platform Launch](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
2. Klicken Sie auf die Launch-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die Registerkarte „Adapter“ und dann auf „Adapter hinzufügen“.
4. Benennen Sie ihn mit „Akamai“ und wählen Sie „Akamai“ im Dropdown-Menü „Typ“. Klicken Sie auf „Speichern“.
5. Wechseln Sie zur Registerkarte „Umgebungen“ und klicken Sie dann auf „Neue Umgebung erstellen“.
6. Wählen Sie „Entwicklung“, geben Sie den Namen „Entwicklungsumgebung“ ein und wählen Sie dann den Akamai-Adapter aus der Dropdown-Liste. Klicken Sie auf „Erstellen“ und dann auf „Schließen“.
7. Klicken Sie auf „Umgebung hinzufügen“, wählen Sie „Staging“, geben Sie ihr den Namen „Staging-Umgebung“ und wählen Sie dann den Akamai-Adapter aus. Klicken Sie auf „Erstellen“ und dann auf „Schließen“.
8. Klicken Sie erneut auf „Umgebung hinzufügen“, wählen Sie „Produktion“, geben Sie ihr den Namen „Produktionsumgebung“ und wählen Sie dann den Akamai-Adapter aus. Klicken Sie auf „Erstellen“ und dann auf „Schließen“.

## Erstellen einer Dev-Bibliothek

Trotz aller bisherigen Änderungen und Konfigurationen wurde kein Code veröffentlicht. Wenn Sie eine Bibliothek erstellen, also eine Sammlung von Änderungen, können Sie Code auf Ihrer Website veröffentlichen.

1. Wechseln Sie zu [Adobe Experience Platform Launch](https://launch.adobe.com) und melden Sie sich bei entsprechender Aufforderung an.
2. Klicken Sie auf die Launch-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die Registerkarte „Publishing“ und dann auf „Neue Bibliothek hinzufügen“.
4. Benennen Sie die Bibliothek mit „Erste Änderungen“ und wählen Sie Ihre Entwicklungsumgebung aus.
5. Klicken Sie auf „Alle geänderten Ressourcen hinzufügen“. Adobe Analytics, der Identitätsdienst und Core werden automatisch aufgeführt.
6. Klicken Sie auf „Speichern“.
7. Klicken Sie im Bildschirm „Publishing-Workflow“ auf das Dropdown-Menü neben der neuen Bibliothek und klicken Sie auf „Für Entwicklung erstellen“. Nach einigen Sekunden wird der gelbe Punkt in der Bibliothek grün, was darauf hinweist, dass die Erstellung erfolgreich war.
8. Gehen Sie zur Registerkarte „Umgebungen“ und klicken Sie dann auf Ihre Entwicklungsumgebung.
9. Kopieren Sie unter „Launch installieren“ die Codeblöcke und stellen Sie sie den Website-Inhabern Ihres Unternehmens zur Verfügung.

## Installation von Launch in der Entwicklungsumgebung Ihrer Website

Wenn Sie den Code Ihrer Website steuern, implementieren Sie die beiden Codeblöcke an ihren jeweiligen Positionen (im `<head>`-Tag und direkt über dem schließenden `</body>`-Tag) auf jeder Seite Ihrer Website. Dieser Code wird normalerweise in der übergreifenden Vorlage der Website platziert. Eine leere Seite, die nur Implementierungscode enthält, würde wie folgt aussehen:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example page</title>
  <script src="//assets.adobedtm.com/launch-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx-development.min.js"></script>
</head>
<body>
   <p>This is a test page.</p>
   <script type="text/javascript">_satellite.pageBottom();</script>
</body>
</html>
```

## Fehlerbehebung

**Der Build-Versuch schlägt fehl.**

Ein häufiger Grund dafür ist, dass Elemente bereits in anderen Bibliotheken vorhanden sind, die in die Staging- oder Produktionsumgebung verschoben werden. Stellen Sie beim Erstellen von Bibliotheken sicher, dass der Bibliothek nur geänderte Ressourcen hinzugefügt werden.

## Dokumentation und zusätzliche Ressourcen

- [Erste Schritte mit Launch](https://docs.adobe.com/content/help/de-DE/launch/using/intro/get-started/quick-start.html): Grundlegender Workflow von Launch
- [Publishing mit Launch](https://docs.adobe.com/content/help/de-DE/launch/using/reference/publish/overview.html): Erfahren Sie mehr über Publishing und Umgebungen

## Nächste Schritte

[Validieren Sie Ihre Analytics-Implementierung und veröffentlichen Sie sie für die Produktion](validate-publish-prod.md): Mehrwert schaffen mit Adobe Analytics.
