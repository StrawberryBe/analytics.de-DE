---
description: Mithilfe von Veröffentlichungslisten können verschiedene Berichte ganz einfach an unterschiedliche Gruppen in Ihrer Organisation gesendet werden, ohne dass dazu gesondert terminierte Berichte erstellt werden müssen. Veröffentlichungslisten sind bei standortspezifischen Report Suites hilfreich, wenn Sie jeder entsprechenden Abteilung ein Exemplar eines bestimmten Dashboards bereitstellen möchten. Sie können Veröffentlichungslisten auch verwenden, um bei der Arbeit mit einer einzelnen Report Suite Daten an viele Empfänger zu senden, ohne jeweils die einzelnen E-Mail-Adressen eingeben zu müssen.
title: Veröffentlichungslisten
feature: Admin Tools
uuid: 07dad661-c302-4981-80d1-3169ad1fe90e
exl-id: 5c9a0ae7-742b-4247-bcbc-2e979af6160c
source-git-commit: 2f14b9059601fd0b8d1603cb7dfc4a0b4a3ff55e
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 49%

---

# Veröffentlichungslisten

Mithilfe von Veröffentlichungslisten können verschiedene Berichte ganz einfach an unterschiedliche Gruppen in Ihrer Organisation gesendet werden, ohne dass dazu gesondert terminierte Berichte erstellt werden müssen. Veröffentlichungslisten sind bei standortspezifischen Report Suites hilfreich, wenn Sie jeder entsprechenden Abteilung ein Exemplar eines bestimmten Dashboards bereitstellen möchten. Sie können Veröffentlichungslisten auch verwenden, um bei der Arbeit mit einer einzelnen Report Suite Daten an viele Empfänger zu senden, ohne jeweils die einzelnen E-Mail-Adressen eingeben zu müssen.

Beim Planen eines Berichts können mehrere Veröffentlichungslisten angegeben werden.

## Abschaffung der Veröffentlichungslisten

Wie Sie wahrscheinlich wissen, werden Reports and Analytics (R&amp;A) sowie das SiteCatalyst-Punktprodukt am 31. Dezember 2023 von Adobe eingestellt. [Hier erfahren Sie mehr über das Ende des Lebenszyklus und darüber, wie Sie sich darauf vorbereiten können.](https://express.adobe.com/page/6WnF8JK6IRDhf/).

Eine der Funktionen in R&amp;A, die am aktuellen Datum voraussichtlich das Ende der Unterstützung erreichen wird, ist die Veröffentlichung von Listen. Einige Funktionen wie Kalenderereignisse und Seitenzusammenfassungsberichte verfügen über eine Paritätsversion in Analysis Workspace. Veröffentlichungslisten gehören jedoch nicht zu diesen Listen und werden eingestellt, wenn die Forschung und Entwicklung beendet wird. **Sie können keine neuen Veröffentlichungslisten erstellen oder auf vorhandene Veröffentlichungslisten zugreifen, um Analysis Workspace-Projekte zu senden oder zu planen.**

Um Störungen Ihrer aktuellen Berichtverteilungs-Workflows, die auf Veröffentlichungslisten beruhen, zu vermeiden, empfehlen wir, die folgenden Alternativen in Betracht zu ziehen:

* Wenn Sie Veröffentlichungslisten verwenden, um dieselbe Version des Berichts an mehrere Benutzer zu verteilen (ohne Report Suite-Überschreibung anzuwenden):

   Nachdem Sie Ihre Berichte in Analysis Workspace als Projekte neu erstellt haben, können Sie eine Kombination aus einer für Ihren E-Mail-Client erstellten Kontaktgruppe oder Verteilerliste und der Funktion Geplante Projekte von Workspace verwenden, um den wiederkehrenden Versand des Projekts zu senden oder zu planen. Wie Veröffentlichungslisten wird dann eine PDF-/CSV-Version des Projekts an jede E-Mail-ID gesendet, die Teil der Gruppe/Liste ist. Weitere Informationen finden Sie unter [Geplante Projekte hier](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/t-schedule-report.html?lang=en#:~:text=Scheduled%20Analysis%20Workspace%20projects%20can,options%20in%20the%20left%20rail.).

* Wenn Sie Veröffentlichungslisten verwenden, um mehrere Versionen des Berichts oder Dashboards an mehrere Benutzer zu verteilen (über die Funktion zur Report Suite-Überschreibung ):

   Analysis Workspace unterstützt keine Report Suite-Überschreibungen. Sie unterstützt auch nicht die Möglichkeit, Report Suites beim Freigeben oder Planen von Projekten zu sperren. Um den Workflow zu replizieren, müssen Sie möglicherweise mehrere Versionen desselben Projekts mit einer anderen Report Suite erstellen, die auf jede Version angewendet wird, und dann die oben beschriebene Funktion für geplante Projekte verwenden.

Bei weiteren Fragen oder bezüglich Support wenden Sie sich bitte an die Kundenunterstützung von Adobe.

## Veröffentlichungslisten-Manager – Beschreibungen {#section_099DF8AC5691495F9B22C71266DD6004}

| Element | Beschreibung |
|--- |--- |
| [!UICONTROL Suchen nach] | Hiermit filtern Sie die Tabelle beim Suchen nach einer Veröffentlichungsliste. |
| [!UICONTROL Report Suites einschließen] | Überschreibt die Report Suite für einen terminierten Bericht oder für alle Reportlets in einem Dashboard. Technisch gesehen unterliegt die Anzahl der einzelnen Einträge einer Report Suite zwar keinen Einschränkungen, eine Beschränkung auf 50 wird jedoch empfohlen. Bei der Anzahl der E-Mail-Adressen, die einbezogen werden können, gibt es keine Einschränkungen. |
| [!UICONTROL E-Mail-Adressen] | Eine durch Kommas getrennte Liste aller E-Mail-Adressen, an die der Bericht mit der neuen Report Suite gesendet wird.  Klicken Sie auf **[!UICONTROL Klicken zur Bearbeitung]**, um die zu empfangenden E-Mail-Adressen anzugeben. Geben Sie die einzelnen E-Mail-Adressen mit Semikolon (;) voneinander getrennt ein. Drücken Sie zum Abschluss `<Enter>`. <br>Im Feld „E-Mail-Zahl“ wird die Zahl der zurzeit mit diesem Report Suite-Eintrag verknüpften E-Mail-Adressen angezeigt. |
| [!UICONTROL Duplizieren] | Erstellt eine Kopie der Veröffentlichungsliste. |
