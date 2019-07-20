---
description: Die Variable „pageName“ sollte einen intuitiv verständlichen Seitenbezeichner enthalten.
keywords: Analytics-Implementierung
seo-description: Die Variable „pageName“ sollte einen intuitiv verständlichen Seitenbezeichner enthalten.
seo-title: Strategien für Seitennamen
solution: Analytics
title: Strategien für Seitennamen
topic: Entwickler und Implementierung
uuid: a 829 d 0 c 7-6 ebf -459 a-b 403-5 e 9 c 05161 e 5 c
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Strategien für Seitennamen

Die Variable „pageName“ sollte einen intuitiv verständlichen Seitenbezeichner enthalten.

You can determine the best way of populating the *`pageName`* variable by looking at the structure of your website. The methods listed below outline various ways of populating the *`pageName`* variable.

While the *`pageName`* variable is central to identifying user behavior, Adobe recommends using multiple variables to indicate page information. Bei den besten Seitenbenennungsstrategien wird für jede Hierarchieebene der Site eine andere Variable eingesetzt:

* Die Variable *`channel`* kann eingesetzt werden, um den Site-Abschnitt anzugeben.
* The *`pageName`* variable can be used to show content type.
* Eine [!UICONTROL Custom Insight]-Variable (prop1) kann für detaillierte Inhalte eingesetzt werden.

Die Detailebenen variieren je nach der Eigenschaft (siehe Tabelle):

| Variable | Detailebene | Beispiel |
|---|---|---|
| Channel | Allgemeiner Abschnitt | Elektronik |
| Prop1 | Unterabschnitt | Sport: Lokaler Sport |
| PageName | Allgemeine Inhaltsbeschreibung | Kredite: Hypothek: Ratenvergleich |
| Prop2 | Detaillierte Inhaltsbeschreibung | Elektronik: Notebook-PC: Detaillierte Spezifikation: IBM Thinkpad T20 |

Je mehr Ebenen eine Site hat, umso mehr Variablen sollten zur Angabe der Seiteninhalte verwendet werden. Es kann auch sinnvoll sein, eine Überschneidung von Variablen einzukalkulieren. So kann eine detailliertere Variable zum Beispiel Informationen zum angezeigten Produkt, aber auch Informationen zum Site-Abschnitt und Unterabschnitt enthalten. Dies ist besonders nützlich, wenn ein Produkt oder Artikel in mehreren Abschnitten einer Site angezeigt wird.

Die folgenden Strategien beschreiben, wie die Variable *`pageName`* fest. Vielleicht sind Sie versucht, die Seitenbenennungsstrategie zu wählen, die sich am einfachsten implementieren lässt. Denken Sie jedoch daran, dass diese Strategie für die Benutzerfreundlichkeit aller [!UICONTROL Pfadsetzung]- und [!UICONTROL Seiten]berichte ausschlaggebend ist. Überlegen Sie es sich daher gut, wie Sie bei der Benennung von Seiten vorgehen. 

## Eindeutiger Name für jede Seite {#section_24704CA39E2F4C00ACEAFF39CA0A921B}

Die sinnvollste Seitenbenennungsmethode besteht darin, jeder Seite einen eindeutigen Bezeichner zuzuordnen, der für alle [!DNL Analytics]-Benutzer in Ihrer Organisation intuitiv verständlich ist. Das können zum Beispiel Namen sein, wie „Homepage“, „Startseite Elektronikabteilung“ oder „Sport: Lokaler Sport: Hochschule“.

Für die meisten [!DNL Analytics]-Benutzer sind hierarchische Seitennamen am nützlichsten, wenn es um das Auffinden von Seiten innerhalb der Site als auch um die Identifizierung des Seitenzwecks geht. Die folgende Tabelle zeigt einige Beispielseitennamen für verschiedene Branchen:

| Konversion | Medien | Finanzen |
|---|---|---|
| Homepage | Homepage | Homepage |
| Elektronik | Technologie | Eigenheimdarlehen |
| Elektronik: Notebooks | Technologie: Neue Geräte  | Eigenheimdarlehen: Ratenvergleich |
| Elektronik: Notebooks: Produktseite | Technologie: Neue Geräte: Artikelseite | Eigenheimdarlehen: Ratenvergleich: 10 Jahre Festzins  |

## Dateipfad (nicht die vollständige URL) {#section_37FDCDA00DA84B3D9B8AB4290555FF34}

Bei einigen Websites ist der Dateipfad eindeutig und leicht verständlich. Jeder Benutzer kann dort anhand der URL erkennen, auf welche Seite sich der Dateipfad bezieht. Ist dies bei Ihrer Site der Fall, können Sie mithilfe einer serverseitigen Variablen den Pfad zu der Datei wie folgt in die Variable *`pageName`* eintragen:

```js
s.pageName="<%= file_path %>"
```

Adobe does not recommend leaving the *`pageName`* blank, (which results in using the full URL of the page) even though you may be tempted to do so. The following side-effects are caused by leaving the *`pageName`* variable blank and using the *`pageURL`* as the page identifier.

* Domäne und Pfad einer Seite würden unter Umständen nicht immer identisch angezeigt. So würden zum Beispiel die folgenden vier URLs eine einzige Seite zurückgeben:

   * `https://www.mysite.com/index.jsp`
   * `https://www.mysite.com`
   * `https://mysite.com/index.jsp`
   * `https://mysite.com/`
   If the *`pageName`* is left blank, each of these page names would occupy a separate entry in reports.

* Einige Seiten (z. B. Formulare) senden an sich selbst, sodass zwischen Originalformular und Ergebnis nicht mehr unterschieden werden kann.
* Wenn Ihre Seite von Suchmaschinen oder anderen Onlinetools in eine andere Sprache übersetzt wird, entspricht die URL der Seite der URL der Suchmaschine (nicht der URL Ihrer Site).

## HTML (document.title) {#section_B99B8F66B0E2410FA7BFE44E6851EB3F}

If you have invested time into making your HTML titles readable and intuitive, you might consider using the same title as the value in the *`pageName`* variable. Adobe recommends using a server-side variable to populate the *`pageName`* rather than using JavaScript's [!DNL document.title]. Der HTML-Titel wird nicht von allen Browsern auf die gleiche Weise interpretiert, was dazu führen kann, dass [!DNL Analytics] von verschiedenen Browsern unterschiedliche Seitennamen erhalten würde.

Bei der Verwendung des HTML-Titels ist es Best Practice, die vorhandenen Titel für jede Seite in eine separate Variable oder ein separates Content Management-Element zu kopieren. Wenn Sie zwecks Suchmaschinenoptimierung oder aus anderen Gründen Änderungen am HTML-Titel vornehmen möchten, hat dies keine Auswirkungen auf die [!DNL Analytics]-Seitennamen. Wenn sich der Name einer Seite in [!DNL Analytics] ändert, wird sie dadurch zu einer neuen Seite und ist, unabhängig von der zugehörigen URL, nicht mehr mit dem alten Seitennamen verknüpft.
