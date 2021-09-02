---
title: Erfassen interner Suchbegriffe
description: Verwenden Sie eine benutzerdefinierte Variable, um interne Suchbegriffe zu erfassen.
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: ht
source-wordcount: '372'
ht-degree: 100%

---


# Erfassen interner Suchbegriffe

Das Reporting über interne Suchen ist für viele Unternehmen von zentraler Bedeutung und stellt bei Adobe Analytics keine vordefinierte Dimension dar. Bei minimalem Implementierungsaufwand kann jedoch das Reporting über interne Suchbegriffe einfach eingerichtet werden.

## Voraussetzungen

[Validieren Sie eine Implementierung in der Entwicklungsumgebung und veröffentlichen Sie sie in der Produktionsumgebung](../launch/validate-publish-prod.md): Auf dieser Seite wird davon ausgegangen, dass Sie über eine grundlegende, funktionierende Implementierung verfügen und im Adobe-Debugger eine Adobe Analytics-Bildanforderung sehen.

## Erstellen einer eVar zur Erfassung interner Suchvorgänge

Folgen Sie [Konversionsvariablen Admin](/help/admin/admin/conversion-var-admin/conversion-var-admin.md), um eine neue eVar für die interne Suche zu erstellen. Geben Sie der eVar einen leicht erkennbaren Namen (z. B. „Interner Suchbegriff“) und halten Sie die neue eVar im [Lösungs-Design-Dokument](../prepare/solution-design.md) Ihres Unternehmens fest.

## Bestimmen eines internen Suchbegriffs

Die meisten internen Suchvorgänge verwenden Abfragezeichenfolgen, um Suchbegriffdaten zwischen Seiten weiterzugeben. Verwenden Sie die interne Suche Ihrer Site und notieren Sie die URL auf der Suchergebnisseite:

`https://example.com/search.html?q=kittens`

Wenn die interne Suche Ihrer Site die URL nicht verwendet, suchen Sie nach dem Suchbegriff an anderen Stellen, z. B. in einer Datenschicht oder einem Cookie. Arbeiten Sie mit Ihrem Site-Entwicklungsteam zusammen, wenn Sie nicht sicher sind, wo Sie einen internen Suchbegriff finden.

## Zuweisen des Abfragezeichenfolgenparameters zu einem Datenelement

Befolgen Sie [Zuordnen von Datenschichtobjekten zu Datenelementen](../launch/layer-to-elements.md). Wählen Sie bei der Auswahl des **[!UICONTROL Datenelementtyps]** **[!UICONTROL Abfragezeichenfolgenparameter]** anstelle von **[!UICONTROL JavaScript-Variable]** aus. Fügen Sie den gewünschten Abfragezeichenfolgenparameter (normalerweise `q`) in das Textfeld ein.

## Zuordnen des Datenelements zur eVar

Befolgen Sie [Zuordnen von Datenelementen zu Analytics-Variablen](../launch/elements-to-variable.md). Stellen Sie sicher, dass Sie dieselbe eVar auswählen, die Sie in den Report Suite-Einstellungen erstellt haben.

## Starten der Bereitstellung von Tags

Befolgen Sie [Analytics-Implementierung in einer Entwicklungsumgebung bereitstellen](../launch/deploy-dev.md). Nachdem Sie geprüft haben, dass die Implementierung in Ihrer Entwicklungsumgebung funktioniert, können Sie [eine Entwicklungsimplementierung validieren und in der Produktionsumgebung veröffentlichen](../launch/validate-publish-prod.md).

## Reporting in Workspace

Warten Sie einige Zeit, damit Ihre Implementierung Daten erfassen kann. Danach können Sie die Dimension in Analysis Workspace verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [experiencecloud.adobe.com](https://experiencecloud.adobe.com) an.
2. Wenn Sie nicht automatisch bei Adobe Analytics angemeldet werden, klicken Sie auf das Gittersymbol oben rechts und wählen Sie **[!UICONTROL Analytics]** aus.
3. Klicken Sie auf die Registerkarte **[!UICONTROL Workspace]** und erstellen Sie ein neues Projekt.
4. Suchen Sie den Namen der von Ihnen unter „Dimensionen“ erstellten eVar und ziehen Sie sie in die Arbeitsfläche des Arbeitsbereichs.
