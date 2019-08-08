---
description: In der folgenden Abbildung sehen Sie, wie die Datenerfassung funktioniert.
keywords: DFA
seo-description: In der folgenden Abbildung sehen Sie, wie die Datenerfassung funktioniert.
seo-title: Adobe Integration Real-Time Data Collection
solution: Analytics
title: Adobe Integration Real-Time Data Collection
topic: Data Connectors
uuid: 5 dce 319 c -7 d 4 b -4475-8 e 6 d-dc 5 c 972 a 82 e 9
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e96de98b3176a05654fdf697210f992b0fd4adb1

---


# Adobe-Integration: Echtzeit-Datenerfassung{#adobe-integration-real-time-data-collection}

In der folgenden Abbildung sehen Sie, wie die Datenerfassung funktioniert.

![](assets/DFA_data_collection.png)

Die Datenerfassung der Adobe-Integration beginnt, sobald die Besucher auf die Landingpage gelangen (1). Beim Adobe-Datenerfassungscode, der auf der Seite ausgeführt wird, haben die vorherigen Interaktionen der Besucher mit bereitgestellten Anzeigen keinerlei Bedeutung. Das Google-DFA-Team hat einen Service erstellt, der auf dem DFA Floodlight-Server ausgeführt wird und mit dessen Hilfe über den Adobe-Code Anzeigeninformationen zu Besuchern abgerufen werden können, die sich gerade auf der Site befinden (2). Zum Abruf dieser Daten wird das Adobe-Bild-Beacon kurzzeitig verzögert und die Daten vom Floodlight-Server abgerufen.

Wenn diese Daten ankommen oder der Abruf zu viel Zeit in Anspruch nimmt, wird ein Treffer an die Adobe-Trackingserver gemeldet (3).

Das Integrationsmodul ist ein besonderes Adobe-JavaScript-Kernmodul, durch das das Adobe-Bild-Beacon verzögert und für eine bestimmte Zeit ( *`s.maxDelay`*). *`s.maxDelay`* wird bestimmt, wie lange das Integrate-Modul auf Daten des DFA Floodlight-Servers wartet, bis das Bild-Tag an den Browser der Besucher gesendet wird. Diese Vorgehensweise ist für die weitere Erfassung grundlegender Besucherdaten wichtig, auch wenn die DFA Floodlight-Server ausfallen oder stark ausgelastet sind. Kommen die Floodlight-Daten an, bevor *`s.maxDelay`* abgelaufen ist, werden die Adobe-Trackingdaten sofort gesendet. Sie enthalten auch die zusätzlichen DFA-Daten.

Bei einem Timeout kann im Seiten-Code ein Adobe Reports &amp; Analysen-Ereignis als Zeitüberschreitungsereignis festgelegt werden. Ein solches Ereignis kann bei der Diagnose von Problemen oder bei der Anpassung von *`s.maxDelay`*. Erhöhen Sie im Falle zahlreich auftretender Timeouts den Wert für *`s.maxDelay`*. *`s.maxDelay`* kann zu hoch eingestellt werden. In diesem Fall können Besucher die Site verlassen, bevor der *`s.maxDelay`* Timer abläuft. For more discussion on this topic, see [Tuning s.maxDelay](../dfa-data-connector-analytics/dfa-integration/dfa-tuning-s-maxlelay.md#concept-6deb28eee18e414db220d6009d449f0d).

Manchmal gibt der Floodlight-Server Fehler zu Besuchern aus. Dieser Fall tritt normalerweise ein, wenn dem Floodlight-Server keine Informationen zu Besuchern vorliegen, da sie zuvor noch keine Anzeigen gesehen haben oder kein DFA-Besuchercookie verwenden. Im Seiten-Code kann eine benutzerspezifische Konversionsvariable (eVar) festgelegt werden, in der diese Fehler erfasst werden. Dadurch können die Fehlerbehebung bei Implementierungsproblemen erleichtert und Fehler bei der Google-Transkation erkannt werden. Die herkömmlichsten Fehler sind, wie in folgender Tabelle beschrieben, „No History“ (Kein Verlauf), „No Cookie“ (Kein Cookie), „Query Error“ (Abfragefehler) und „Opted Out“ (Abgemeldet):

| Fehler | Name | Beschreibung |
|---|---|---|
| nh | No History | Besucher haben keine Anzeigen gesehen oder angeklickt. |
| nc | No Cookie | Besucher verfügen über kein DFA-Cookie. |
| qe | Query Error | Bei der Abfrage von Daten für den Floodlight-Server ist ein Fehler aufgetreten. |
| oo | Opted Out | Der Besucher hat sich vom Google-Impressions-/Klick-Tracking abgemeldet. |

