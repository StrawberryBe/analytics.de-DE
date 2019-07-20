---
title: Bereitstellen von Adobe Analytics in einer dev-Umgebung
seo-title: Bereitstellen von Adobe Analytics in einer dev-Umgebung
description: Erfahren Sie, wie Sie Adobe Analytics starten, um Adobe Analytics in Ihrer Entwicklungsumgebung bereitzustellen.
seo-description: Erfahren Sie, wie Sie Adobe Analytics starten, um Adobe Analytics in Ihrer Entwicklungsumgebung bereitzustellen.
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Bereitstellen einer Analytics-Implementierung in einer Entwicklungsumgebung

Nachdem eine Eigenschaft im Start erstellt und konfiguriert wurde, können die Bibliotheken bereitgestellt und auf Ihrer Site implementiert werden.

## Voraussetzungen

[Erstellen und konfigurieren Sie eine Eigenschaft für Adobe Analytics im Start](create-analytics-property.md): Greifen Sie auf das Tool zu und erstellen Sie einen Bereich für Ihre Analytics-Implementierung.

## Erstellen von Adaptern und Umgebungen

Starten Sie viele organisatorische Arbeitsabläufe bei der Bereitstellung von Code. Führen Sie die folgenden Schritte aus, um die erforderlichen Komponenten für eine Analytics-Implementierung zu erstellen. Als Startadministrator können Sie innerhalb Ihres Unternehmens den richtigen Arbeitsablauf für die Bereitstellung von Adobe-Lösungen einrichten.

1. Go to [Adobe Experience Platform Launch](https://launch.adobe.com) and log in if prompted.
2. Klicken Sie auf die Starteigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die Registerkarte Adapter und anschließend auf Adapter hinzufügen.
4. Nennen Sie den Namen "Akamai" und wählen Sie Akamai in der Dropdown-Liste" Typ" aus. Klicken Sie auf „Speichern“.
5. Rufen Sie die Registerkarte Umgebungen auf und klicken Sie dann auf Neue Umgebung erstellen.
6. Wählen Sie Entwicklung, nennen Sie es "Dev Environment" und wählen Sie dann den Akamai-Adapter aus der Dropdown-Liste. Klicken Sie auf Erstellen und dann auf Schließen.
7. Klicken Sie auf Umgebung hinzufügen, wählen Sie Staging aus, nennen Sie den Namen "Staging-Umgebung" und wählen Sie den Akamai-Adapter. Klicken Sie auf Erstellen und dann auf Schließen.
8. Klicken Sie erneut auf Umgebung hinzufügen, wählen Sie Produktion aus, nennen Sie den Namen "Produktionsumgebung" und wählen Sie den Akamai-Adapter. Klicken Sie auf Erstellen und dann auf Schließen.

## Erstellen einer dev-Bibliothek

Trotz aller bisher vorgenommenen Änderungen und Konfigurationen wurde kein Code veröffentlicht. Das Erstellen einer Bibliothek, die in etwa als Sammlung von Änderungen übersetzt wird, ermöglicht die Verwendung von Code auf Ihrer Site.

1. Go to [Adobe Experience Platform Launch](https://launch.adobe.com) and log in if prompted.
2. Klicken Sie auf die Starteigenschaft, die Sie auf Ihrer Site implementieren möchten.
3. Klicken Sie auf die Registerkarte Veröffentlichung und dann auf Neue Bibliothek hinzufügen.
4. Geben Sie den Namen der Bibliothek an und wählen Sie die Entwicklungsumgebung aus.
5. Klicken Sie auf Alle geänderten Ressourcen hinzufügen, wodurch Adobe Analytics, Identitätsdienst und Core automatisch aufgelistet werden.
6. Klicken Sie auf „Speichern“.
7. Klicken Sie auf dem Bildschirm "Veröffentlichungsarbeitsablauf" auf die Dropdown-Liste neben Ihrer neuen Bibliothek und klicken Sie auf" Erstellen" für die Entwicklung. Nach einigen Sekunden wird der gelbe Punkt in der Bibliothek grün dargestellt, was darauf hinweist, dass der Build erfolgreich war.
8. Rufen Sie die Registerkarte Umgebungen auf und klicken Sie dann auf Ihre Entwicklungsumgebung.
9. Kopieren Sie unter "Launch Launch" die Codeblöcke und stellen Sie sie den Website-Inhabern Ihrer Organisation bereit.

## Launch in der Entwicklungsumgebung Ihrer Website installieren

If you control your website's code, implement the two blocks of code in their respective locations (in the `<head>` tag and just above the closing `</body>` tag) on every page of your site. Dieser Code wird häufig in der überlagerten Vorlage der Site platziert. Eine leere Seite, die nur Implementierungscode enthält, würde wie folgt aussehen:

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

**Versuch zum Erstellen eines Fehlers.**

Ein allgemeiner Grund hierfür besteht darin, dass Elemente bereits in anderen Bibliotheken vorhanden sind, die an Staging oder Produktion gesendet wurden. Wenn Sie zunächst Bibliotheken erstellen, stellen Sie sicher, dass der Bibliothek nur Ressourcen hinzugefügt wurden.

## Dokumentation und zusätzliche Ressourcen

- [Erste Schritte mit Start](https://docs.adobelaunch.com/getting-started): Lernen Sie den grundlegenden Workflow des Start-Workflows kennen.
- [Administration starten](https://docs.adobelaunch.com/administration): Weitere Informationen zu Adaptiven und Umgebungen

## Nächste Schritte

[Validieren Sie Ihre Analytics-Implementierung und veröffentlichen Sie sie in der Produktion](validate-publish-prod.md): Starten Sie den Wert aus Adobe Analytics.
