---
description: Die Variable „pageName“ sollte einen intuitiv verständlichen Seitenbezeichner enthalten.
keywords: Analytics Implementation
title: Strategien für die Seitenbenennung
topic: Developer and implementation
uuid: a829d0c7-6ebf-459a-b403-5e9c05161e5c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Strategien für die Seitenbenennung

Die Variable „pageName“ sollte einen intuitiv verständlichen Seitenbezeichner enthalten.

Sie können durch einen Blick auf die Struktur Ihrer Website die beste Art und Weise bestimmen, mit der die Variable *`pageName`* ausgefüllt wird. Unten sind verschiedene Methoden aufgeführt, die zum Auffüllen der Variable *`pageName`* verfügbar sind.

Während *`pageName`* die wichtigste Variable zur Identifizierung des Benutzerverhaltens ist, empfiehlt Adobe, mehrere Variablen zur Angabe von Seiteninformationen zu verwenden. Bei den besten Seitenbenennungsstrategien wird für jede Hierarchieebene der Site eine andere Variable eingesetzt:

* Die Variable Variable *`channel`* kann eingesetzt werden, um den Site-Abschnitt anzugeben.
* Die Variable *`pageName`* kann eingesetzt werden, um den Content-Typ anzugeben.
* Eine [!UICONTROL Custom Insight]-Variable (prop1) kann für detaillierte Inhalte eingesetzt werden.

Die Detailebenen variieren je nach der Eigenschaft (siehe Tabelle):

| Variable | Detailebene | Beispiel |
|---|---|---|
| Channel | Allgemeiner Abschnitt | Elektronik |
| Prop1 | Unterabschnitt | Sport: Lokaler Sport |
| PageName | Allgemeine Inhaltsbeschreibung | Kredite: Hypothek: Ratenvergleich |
| Prop2 | Detaillierte Inhaltsbeschreibung | Elektronik: Notebook-PC: Detaillierte Spezifikation: IBM Thinkpad T20 |

Je mehr Ebenen eine Site hat, umso mehr Variablen sollten zur Angabe der Seiteninhalte verwendet werden. Es kann auch sinnvoll sein, eine Überschneidung von Variablen einzukalkulieren. So kann eine detailliertere Variable zum Beispiel Informationen zum angezeigten Produkt, aber auch Informationen zum Site-Abschnitt und Unterabschnitt enthalten. Dies ist besonders nützlich, wenn ein Produkt oder Artikel in mehreren Abschnitten einer Site angezeigt wird.

Die folgenden Strategien beschreiben, wie Sie die Variable *`pageName`* auffüllen. Vielleicht sind Sie versucht, die Seitenbenennungsstrategie zu wählen, die sich am einfachsten implementieren lässt. Denken Sie jedoch daran, dass diese Strategie für die Benutzerfreundlichkeit aller [!UICONTROL Pfadsetzung]- und [!UICONTROL Seiten]berichte ausschlaggebend ist. Überlegen Sie es sich daher gut, wie Sie bei der Benennung von Seiten vorgehen.

## Eindeutiger Name für jede Seite {#section_24704CA39E2F4C00ACEAFF39CA0A921B}

Die sinnvollste Seitenbenennungsmethode besteht darin, jeder Seite einen eindeutigen Bezeichner zuzuordnen, der für alle [!DNL Analytics]-Benutzer in Ihrer Organisation intuitiv verständlich ist. Das können zum Beispiel Namen sein, wie „Homepage“, „Startseite Elektronikabteilung“ oder „Sport: Lokaler Sport: Hochschule“.

Für die meisten [!DNL Analytics]-Benutzer sind hierarchische Seitennamen am nützlichsten, wenn es um das Auffinden von Seiten innerhalb der Site als auch um die Identifizierung des Seitenzwecks geht. Die folgende Tabelle zeigt einige Beispielseitennamen für verschiedene Branchen:

| Konversion | Medien | Finanzen |
|---|---|---|
| Homepage | Homepage | Homepage |
| Elektronik | Technologie | Eigenheimdarlehen |
| Elektronik: Notebooks | Technologie: Neue Geräte | Eigenheimdarlehen: Ratenvergleich |
| Elektronik: Notebooks: Produktseite | Technologie: Neue Geräte: Artikelseite | Eigenheimdarlehen: Ratenvergleich: 10 Jahre Festzins |

## Dateipfad (nicht die vollständige URL) {#section_37FDCDA00DA84B3D9B8AB4290555FF34}

Bei einigen Websites ist der Dateipfad eindeutig und leicht verständlich. Jeder Benutzer kann dort anhand der URL erkennen, auf welche Seite sich der Dateipfad bezieht. Ist dies bei Ihrer Site der Fall, können Sie mithilfe einer Server-seitigen Variable den Pfad zu der Datei wie folgt in die Variable *`pageName`* eintragen:

```js
s.pageName="<%= file_path %>"
```

Adobe rät davon ab, *`pageName`* leer zu lassen (was dazu führen würde, dass die vollständige URL der Seite verwendet wird), obwohl Sie möglicherweise versucht sind, dies zu tun. Die folgenden Nebenwirkungen werden durch Leerlassen der Variable *`pageName`* und Verwenden von *`pageURL`* als Seitenkennung verursacht.

* Domäne und Pfad einer Seite würden unter Umständen nicht immer identisch angezeigt. So würden zum Beispiel die folgenden vier URLs eine einzige Seite zurückgeben:

   * `https://www.mysite.com/index.jsp`
   * `https://www.mysite.com`
   * `https://mysite.com/index.jsp`
   * `https://mysite.com/`
   Wenn *`pageName`* leer ist, würde es zu jedem dieser Seitennamen einen separaten Eintrag in Berichten geben.

* Einige Seiten (z. B. Formulare) senden an sich selbst, sodass zwischen Originalformular und Ergebnis nicht mehr unterschieden werden kann.
* Wenn Ihre Seite von Suchmaschinen oder anderen Onlinetools in eine andere Sprache übersetzt wird, entspricht die URL der Seite der URL der Suchmaschine (nicht der URL Ihrer Site).

## HTML (document.title) {#section_B99B8F66B0E2410FA7BFE44E6851EB3F}

Wenn Sie viel Zeit und Mühen in intuitiv verständliche HTML-Titel investiert haben, ziehen Sie vielleicht in Betracht, diese Titel als Werte in der Variable *`pageName`* zu nutzen. Adobe empfiehlt die Verwendung einer Server-seitigen Variable zum Ausfüllen von *`pageName`*, anstatt [!DNL document.title] von JavaScript zu verwenden. Der HTML-Titel wird nicht von allen Browsern auf die gleiche Weise interpretiert, was dazu führen kann, dass [!DNL Analytics] von verschiedenen Browsern unterschiedliche Seitennamen erhalten würde.

Bei der Verwendung des HTML-Titels ist es Best Practice, die vorhandenen Titel für jede Seite in eine separate Variable oder ein separates Content Management-Element zu kopieren. Wenn Sie zwecks Suchmaschinenoptimierung oder aus anderen Gründen Änderungen am HTML-Titel vornehmen möchten, hat dies keine Auswirkungen auf die [!DNL Analytics]-Seitennamen. Wenn sich der Name einer Seite in [!DNL Analytics] ändert, wird sie dadurch zu einer neuen Seite und ist, unabhängig von der zugehörigen URL, nicht mehr mit dem alten Seitennamen verknüpft.
