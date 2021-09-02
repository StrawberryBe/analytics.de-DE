---
title: Adobe Analytics in einer Entwicklungsumgebung bereitstellen
description: Hier erfahren Sie, wie Sie Tags verwenden, um Adobe Analytics in Ihrer Entwicklungsumgebung bereitzustellen.
exl-id: 324943db-cb0b-40b1-8884-56bb3f608278
source-git-commit: ea6812c8e596773abb8a05bbdb37bc641967c9b8
workflow-type: ht
source-wordcount: '594'
ht-degree: 100%

---

# Analytics-Implementierung in einer Entwicklungsumgebung bereitstellen

Nachdem Sie eine Tag-Eigenschaft erstellt und konfiguriert haben, können die Bibliotheken bereitgestellt und Code auf Ihrer Site implementiert werden.

>[!NOTE]
>Adobe Experience Platform Launch wurde umbenannt und umfasst eine Suite von Datenerfassungstechnologien in Experience Platform. Infolgedessen wurden in der gesamten Produktdokumentation mehrere terminologische Änderungen vorgenommen. Eine Übersicht der terminologischen Änderungen finden Sie im folgenden [Dokument](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=de).

## Voraussetzungen

[Erstellen und konfigurieren einer Tag-Eigenschaft für Adobe Analytics](create-analytics-property.md): Greifen Sie auf das Werkzeug zu und erstellen Sie einen Raum für Ihre Analytics-Implementierung.

## Erstellen von Adaptern und Umgebungen

Tags ermöglichen durch die Bereitstellung von Code zahlreiche betriebliche Arbeitsabläufe. Führen Sie die folgenden Schritte aus, um die erforderlichen Mindestkomponenten für eine Analytics-Implementierung zu erstellen. Als Tag-Administrator können Sie innerhalb Ihres Unternehmens den richtigen Arbeitsablauf für die Bereitstellung von Adobe-Lösungen einrichten.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die Registerkarte „Adapter“ und dann auf „Adapter hinzufügen“.
4. Benennen Sie ihn mit „Akamai“ und wählen Sie „Akamai“ im Dropdown-Menü „Typ“. Klicken Sie auf „Speichern“.
5. Wechseln Sie zur Registerkarte „Umgebungen“ und klicken Sie dann auf „Neue Umgebung erstellen“.
6. Wählen Sie „Entwicklung“, geben Sie den Namen „Entwicklungsumgebung“ ein und wählen Sie dann den Akamai-Adapter aus der Dropdown-Liste. Klicken Sie auf „Erstellen“ und dann auf „Schließen“.
7. Klicken Sie auf „Umgebung hinzufügen“, wählen Sie „Staging“, geben Sie ihr den Namen „Staging-Umgebung“ und wählen Sie dann den Akamai-Adapter aus. Klicken Sie auf „Erstellen“ und dann auf „Schließen“.
8. Klicken Sie erneut auf „Umgebung hinzufügen“, wählen Sie „Produktion“, geben Sie ihr den Namen „Produktionsumgebung“ und wählen Sie dann den Akamai-Adapter aus. Klicken Sie auf „Erstellen“ und dann auf „Schließen“.

## Erstellen einer Dev-Bibliothek

Trotz aller bisherigen Änderungen und Konfigurationen wurde kein Code veröffentlicht. Wenn Sie eine Bibliothek erstellen, also eine Sammlung von Änderungen, können Sie Code auf Ihrer Website veröffentlichen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei der [Datenerfassungs-Benutzeroberfläche](https://experience.adobe.com/data-collection) an.
2. Klicken Sie auf die Tag-Eigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die Registerkarte „Publishing“ und dann auf „Neue Bibliothek hinzufügen“.
4. Benennen Sie die Bibliothek mit „Erste Änderungen“ und wählen Sie Ihre Entwicklungsumgebung aus.
5. Klicken Sie auf „Alle geänderten Ressourcen hinzufügen“. Adobe Analytics, der Identitätsdienst und Core werden automatisch aufgeführt.
6. Klicken Sie auf „Speichern“.
7. Klicken Sie im Bildschirm „Publishing-Workflow“ auf das Dropdown-Menü neben der neuen Bibliothek und klicken Sie auf „Für Entwicklung erstellen“. Nach einigen Sekunden wird der gelbe Punkt in der Bibliothek grün, was darauf hinweist, dass die Erstellung erfolgreich war.
8. Gehen Sie zur Registerkarte „Umgebungen“ und klicken Sie dann auf Ihre Entwicklungsumgebung.
9. Kopieren Sie unter „Tags installieren“ die Code-Blöcke und stellen Sie sie den Verantwortlichen Ihrer Unternehmens-Website zur Verfügung.

## Installieren von Tags in der Entwicklungsumgebung Ihrer Website

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

- [Schnellstartanleitung](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=de): Hier lernen Sie den grundlegenden Workflow der Tag-Implementierung kennen
- [Publishing-Übersicht](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=de): Hier erfahren Sie mehr über das Publishing und Umgebungen

## Nächste Schritte

[Validieren Sie Ihre Analytics-Implementierung und veröffentlichen Sie sie für die Produktion](validate-publish-prod.md): Mehrwert schaffen mit Adobe Analytics.
