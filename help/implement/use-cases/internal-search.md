---
title: Interne Suchbegriffe erfassen
description: Verwenden Sie eine benutzerdefinierte Variable, um interne Suchbegriffe zu erfassen.
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---


# Interne Suchbegriffe erfassen

Die interne Suchberichterstellung ist für viele Unternehmen von zentraler Bedeutung und stellt mit Adobe Analytics keine vordefinierte Dimension dar. Bei minimalen Implementierungsbemühungen kann jedoch die Berichterstellung über interne Suchbegriffe einfach erfasst werden.

## Voraussetzungen

[Validieren Sie eine Entwicklungsimplementierung und veröffentlichen Sie sie in der Produktion](../launch/validate-publish-prod.md): Auf dieser Seite wird davon ausgegangen, dass Sie über eine grundlegende funktionierende Implementierung verfügen und im Adobe-Debugger eine Adobe Analytics-Bildanforderung sehen.

## Erstellen eines eVar für die interne Suche

Folgen Sie [Umrechnungsvariablen admin](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) , um eine neue eVar für die interne Suche zu erstellen. Geben Sie dem eVar einen leicht erkennbaren Namen (z. B. &quot;Interner Suchbegriff&quot;) und zeichnen Sie den neuen eVar im [Lösungsdesigndokument](../prepare/solution-design.md) Ihres Unternehmens auf.

## Internen Suchbegriff bestimmen

Die meisten internen Suchvorgänge verwenden Abfragezeichenfolgen, um Suchbegriffdaten zwischen Seiten weiterzugeben. Verwenden Sie die interne Suche Ihrer Site und notieren Sie die URL auf der Suchergebnisseite:

`https://example.com/search.html?q=kittens`

Wenn die interne Suche Ihrer Site die URL nicht verwendet, suchen Sie nach dem Suchbegriff an anderen Stellen, z. B. in einer Datenschicht oder einem Cookie. Arbeiten Sie mit Ihrem Site-Entwicklungsteam zusammen, wenn Sie nicht sicher sind, wo Sie internen Suchbegriff finden.

## Den Abfragezeichenfolgenparameter einem Datenelement zuweisen

Folgen Sie [Ordnen Sie Datenschichtobjekte Datenelementen](../launch/layer-to-elements.md) zu. Wählen Sie bei der Auswahl von **[!UICONTROL Datenelementtyp]** **[!UICONTROL Abfragezeichenfolgenparameter]** anstelle von **[!UICONTROL JavaScript-Variable]** aus. Fügen Sie den gewünschten Abfragezeichenfolgenparameter (normalerweise `q`) in das Textfeld ein.

## Ordnen Sie das Datenelement dem eVar zu

Folgen Sie [Zuordnen von Datenelementen zu Analytics-Variablen](../launch/elements-to-variable.md). Stellen Sie sicher, dass Sie dieselbe eVar auswählen, die Sie in den Report Suite-Einstellungen erstellt haben.

## Starten der Bereitstellung von Tags

Folgen Sie [Bereitstellen einer Analytics-Implementierung in einer Entwicklungsumgebung](../launch/deploy-dev.md). Nachdem Sie bestätigt haben, dass die Implementierung in Ihrer Entwicklungsumgebung funktioniert, können Sie [eine Entwicklungsimplementierung validieren und in der Produktion veröffentlichen](../launch/validate-publish-prod.md).

## Reporting in Workspace

Geben Sie Ihrer Implementierung etwas Zeit für die Datenerfassung und können Sie dann mit der Verwendung der Dimension in Analysis Workspace beginnen.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Wenn Sie nicht automatisch bei Adobe Analytics angemeldet sind, klicken Sie auf das 9-Raster-Symbol oben rechts und wählen Sie **[!UICONTROL Analytics]** aus.
3. Klicken Sie auf die Registerkarte **[!UICONTROL Workspace]** und erstellen Sie ein neues Projekt.
4. Suchen Sie den Namen der von Ihnen unter Dimensionen erstellten eVar und ziehen Sie sie in die Arbeitsfläche des Arbeitsbereichs.
