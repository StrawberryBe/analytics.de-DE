---
description: Verwenden Sie das Dynamic Tag Management, um Kopf- und Fußzeilencode hinzuzufügen, mit dem das Laden von JavaScript und Seiteninhalten Ihrer Site definiert wird. Sie müssen sowohl den Kopf- als auch den Fußzeilencode auf jeder Seite Ihrer Website einfügen – unabhängig von der verwendeten Hosting-Option.
keywords: Analytics-Implementierung; Implementierungsmethode; dynamisches Tag-Management; dtm; code; page code; header code; Fußzeilencode; Einbettungscode; embed Registerkarte; embed
seo-description: Verwenden Sie das Dynamic Tag Management, um Kopf- und Fußzeilencode hinzuzufügen, mit dem das Laden von JavaScript und Seiteninhalten Ihrer Site definiert wird. Sie müssen sowohl den Kopf- als auch den Fußzeilencode auf jeder Seite Ihrer Website einfügen – unabhängig von der verwendeten Hosting-Option.
seo-title: Kopf- und Fußzeilencode hinzufügen
solution: Analytics
title: Kopf- und Fußzeilencode hinzufügen
topic: Entwickler und Implementierung
uuid: 23 d 89 ae 0-340 a -4 b 12-91 d 1-953 b 4613 c 98 e
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Kopf- und Fußzeilencode hinzufügen

Verwenden Sie das Dynamic Tag Management, um Kopf- und Fußzeilencode hinzuzufügen, mit dem das Laden von JavaScript und Seiteninhalten Ihrer Site definiert wird. Sie müssen sowohl den Kopf- als auch den Fußzeilencode auf jeder Seite Ihrer Website einfügen – unabhängig von der verwendeten Hosting-Option.

Da das Dynamic Tag Management Codebausteine sowohl in der Kopf- als auch in der Fußzeile einbindet, können Sie Regeln am Seitenanfang oder am Seitenende ausführen. Dies ermöglicht die Implementierung von Test-Tools und anderen Verfahren; gleichzeitig behalten Sie die Kontrolle bei der Nachverfolgung Ihrer Seiten.

Mithilfe des Dynamic Tag Managements werden Staging- und Produktions-Einbettungscodes erstellt, mit denen Ihre Änderungen in der Staging-Umgebung getestet werden können, bevor Sie sie in die Produktionsumgebung übernehmen.

>[!IMPORTANT]
>
>Für eine erfolgreiche Implementierung ist es wichtig, dass Sie diese Anweisungen wie in der Adobe-Hilfe angezeigt befolgen. Specifically, you must place the header code in the `<head>` section of your document templates. Also, you must place the footer code just before the closing `</body>` tag. Das Einfügen dieser Einbettungscodes an einer anderen Stelle im Markup, die Verwendung asynchroner Methoden zum Anhängen der Einbettungscodes oder das beliebige Umbrechen von Einbettungscodes stellen *keine* unterstützte Implementierung des Dynamic Tag Managements dar. Die Einbettungscodes müssen genau so wie angegeben implementiert werden.
>
>Eine nicht unterstützte Implementierung führt zu unerwarteten Ergebnissen und macht es dem Kundendienst und dem technischen Service unmöglich, Sie bei Ihrer Implementierung zu unterstützen.

1. Öffnen Sie die Registerkarte „[!UICONTROL Einbettung]“ in der Benutzeroberfläche des Dynamic Tag Managements, wählen Sie eine Hosting-Option (wie beispielsweise Akamai) und schalten Sie dann den Umschalter auf „Ein“. 

   Schritt 1. Kopieren Sie den Produktions-Kopfzeilencode, der auf der Registerkarte „Einbettung“ des Dynamic Tag Managements bereitgestellt wird, und fügen Sie ihn im Abschnitt [!DNL HEAD] des HTML-Codes Ihrer Website ein.

   ![](assets/dtm-embed.png)

   Place the code as close to the [!DNL <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">]-Tag. Dieser Codeabschnitt sollte auf jeder Seite Ihrer Live-Produktions-Website platziert werden.

   >[!NOTE]
   >
   >Production embed code reflects only the published items in that [property](../../../implement/c-implement-with-dtm/t-create-web-property.md#task_960467FBB7A54499AC228CB3AA3C4123). Einbettungscode für das Staging gibt jedoch alle Elemente in der zugehörigen Eigenschaft wieder, unabhängig von ihrem Veröffentlichungsstatus. Um nicht veröffentlichte Elemente auf Ihrer Produktions-Website zu testen, aktivieren Sie Staging lokal in der Konsole, siehe Anweisungen unter [Nicht veröffentlichte Regeln für Akamai-Hosting testen](../../../implement/c-implement-with-dtm/c-rules/t-test-rules-akamai.md#task_B397167F9E9B4487957AD6CE2AD47259).

1. Kopieren Sie den Produktions-Fußzeilencode und fügen Sie ihn im [!DNL BODY]-Bereich Ihres Website-HTML-Codes ein.

   Place the code as close to the [!DNL </body>]-Tag. 
1. Kopieren Sie den Staging-Kopf- und Fußzeilencode und wiederholen Sie dann die oben beschriebenen Schritte für Ihre Staging-Website.

   >[!NOTE]
   >
   >The difference between production and staging code snippets is the addition of [!DNL -staging] to the filename in the staging version. Der Fußzeilencode bleibt in der Staging- und Production-Version gleich.

