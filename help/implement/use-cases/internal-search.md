---
title: Interne Suchbegriffe erfassen
description: Verwenden Sie eine benutzerspezifische Variable, um interne Suchbegriffe zu erfassen.
translation-type: tm+mt
source-git-commit: 091e4b859addc1780d94d90c8b59748277890241
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 2%

---


# Interne Suchbegriffe erfassen

Der Berichte der internen Suche ist für viele Organisationen unverzichtbar und stellt mit Adobe Analytics keine vordefinierte Dimension dar. Bei minimalen Implementierungsbemühungen kann der Berichte interner Suchbegriffe jedoch problemlos erfasst werden.

## Voraussetzungen

[Validieren einer Implementierung der Entwicklung und Veröffentlichen in der Produktion](../launch/validate-publish-prod.md): Auf dieser Seite wird davon ausgegangen, dass Sie über eine grundlegende Arbeitsimplementierung verfügen und im Adobe-Debugger eine Adobe Analytics-Bildanforderung angezeigt wird.

## Erstellen einer eVar für die interne Suche

Folgen Sie [dem Admin](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) für Konversionsvariablen, um eine neue eVar für die interne Suche zu erstellen. Geben Sie dem eVar einen leicht erkennbaren Namen (z. B. &quot;Interner Suchbegriff&quot;) und zeichnen Sie die neue eVar im [Lösungsdesign-Dokument](../prepare/solution-design.md)Ihres Unternehmens auf.

## Interne Suchbegriffe bestimmen

Die meisten internen Suchvorgänge verwenden Abfragen-Zeichenfolgen, um Suchbegriffdaten zwischen den Seiten weiterzugeben. Verwenden Sie die interne Suche Ihrer Site und beachten Sie die URL auf der Suchergebnisseite:

`https://example.com/search.html?q=kittens`

Wenn die interne Suche Ihrer Site die URL nicht verwendet, suchen Sie den Suchbegriff an anderen Stellen, z. B. in einer Datenschicht oder einem Cookie. Arbeiten Sie mit Ihrem Site-Entwicklungsteam zusammen, wenn Sie nicht sicher sind, wo Sie internen Suchbegriff finden.

## Den Abfrage-Zeichenfolgenparameter einem Datenelement zuweisen

Follow [Map data layer objects to data elements](../launch/layer-to-elements.md). Wählen Sie bei der Auswahl des **[!UICONTROL Datenelementtyps]** den **[!UICONTROL Abfragen-Zeichenfolgenparameter]** anstelle der **[!UICONTROL JavaScript-Variable]**. Geben Sie den gewünschten Zeichenfolgenparameter (normalerweise `q`) in das Textfeld ein.

## Ordnen Sie das Datenelement dem eVar zu

Follow [Map Launch data elements to Analytics variables](../launch/elements-to-variable.md). Stellen Sie sicher, dass Sie die gleiche eVar auswählen, die Sie in den Report Suite-Einstellungen erstellt haben.

## Beginn der Bereitstellung starten

Follow [Deploy an Analytics implementation to a development environment](../launch/deploy-dev.md). Nachdem Sie bestätigt haben, dass die Entwicklungsumgebung in Ihrer dev-Umgebung funktioniert, können Sie eine Entwicklungsumgebung [überprüfen und in der Produktion](../launch/validate-publish-prod.md)veröffentlichen.

## Berichte in Workspace.

Geben Sie Ihrer Implementierung etwas Zeit, um Daten zu erfassen, und dann können Sie mit der Dimension in Analysis Workspace Beginn ausführen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Wenn Sie nicht automatisch bei Adobe Analytics angemeldet sind, klicken Sie oben rechts auf das 9-Raster-Symbol und wählen Sie &quot; **[!UICONTROL Analytics]**&quot;aus.
3. Klicken Sie auf die Registerkarte **[!UICONTROL Arbeitsbereich]** und erstellen Sie ein neues Projekt.
4. Suchen Sie den Namen der eVar, die Sie unter &quot;Dimensionen&quot;erstellt haben, und ziehen Sie sie in die Arbeitsfläche.
