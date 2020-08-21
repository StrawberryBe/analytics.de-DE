---
title: Häufig gestellte Fragen zu Marketing-Kanälen
description: Häufig gestellte Fragen zu Marketing-Kanälen
translation-type: tm+mt
source-git-commit: 89c91aa7620eaba3d24e3d5de4055609c472f9f7
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 59%

---


# Häufig gestellte Fragen zu Marketing-Kanälen

Häufig gestellte Fragen zu Marketing-Kanälen

## Meine Trackingcodes folgen keinem Muster und ich habe Tausende, die für meinen Affiliates-Kanal angegeben werden müssen.

* Sortieren Sie aus, was Sie nicht brauchen. Wenn Ihre E-Mail- und Affiliates-Kanäle denselben Abfragezeichenfolgenparameter verwenden, aber nur wenig E-Mail-Trackingcodes vorliegen, können Sie die E-Mail-Trackingcodes in einem Regelsatz zu „email“ angeben. Klassifizieren Sie dann alle weiteren Trackingcodes als *`affiliates.`*
* Fügen Sie allen Landingpage-URLs in Ihrem E-Mail-System einen Abfragezeichenfolgenparameter hinzu, z. B. *`&ch=eml`*. Erstellen Sie einen Regelsatz, der erkennt, ob der „ch“-Abfrageparameter gleich *`eml`*. Wenn er *`eml`* nicht enthält, ist er ein Affiliate.

## Verweisende Domänen enthalten mehr Daten als erwartet.

* Verweisende Domänen stehen in der Liste der Verarbeitungsregeln eventuell zu weit oben. Da die Verarbeitungsreihenfolge wichtig ist, sollte dies einer der letzten bzw. der letzte Regelsatz sein.

## Ich habe eine Regel erstellt, die mit einem Abfrage-String-Parameter übereinstimmt und nicht funktioniert.

* Vergewissern Sie sich, dass der Parametername in den Feldern des Abfragenzeichenfolgenparameters angegeben ist (gewöhnlich ein alphanummerischer Wert). Vergewissern Sie sich zudem, dass der Parameterwert nach dem Operator steht, wie in folgendem Beispiel einer E-Mail-Regel dargestellt.

   ![](assets/example_email.png)

## Warum wird mein gesamter Last Touch-Traffic einer internen Domäne zugeordnet?

* Sie verwenden eine Regel, die internem Traffic entspricht. Denken Sie daran, dass diese Regeln für jeden Treffer auf Ihrer Site verarbeitet werden, nicht nur beim Erstbesuch. Wenn Sie eine Regel wie *`Page URL exists`* ohne weitere Kriterien verwenden, wird bei jedem nachfolgenden Treffer auf Ihrer Site eine Übereinstimmung mit dem betreffenden Kanal erfasst, da die Seiten-URL immer vorhanden ist.

## Wie behebe ich Traffic-Fehler, der im Bericht unter Kein Kanal identifiziert angezeigt wird?

* Regeln werden der Reihe nach verarbeitet. Wenn keine Übereinstimmung mit den spezifischen Kriterien vorliegt, fallen die Treffer in eine von drei Kategorien:

1. Kein Verweis (ein Direktbesuch).

2. Interner Verweis, auf der ersten Seite des Besuchs.

3. Ein Verarbeitungsfehler auf der Seite.

Stellen Sie sicher, dass Sie einen Kanal für diese drei Möglichkeiten haben. Erstellen Sie beispielsweise diese Regeln:

1. **[!UICONTROL Verweisende Stelle]** und **[!UICONTROL Nicht vorhanden]** und **[!UICONTROL Ist erste Seite des Besuchs]**. (Siehe [Direct.](/help/components/c-marketing-channels/c-faq.md))

2. **[!UICONTROL Referrer entspricht internen URL-Filtern]** und **[!UICONTROL Ist erste Seite des Besuchs]**. (Siehe [Internal](/help/components/c-marketing-channels/c-faq.md).)

3. **[!UICONTROL Verweisende Domäne]** und **[!UICONTROL Vorhanden]** und **[!UICONTROL Verweis stimmt nicht mit internen URL-Filtern überein]**.

Erstellen Sie abschließend einen Kanal *Sonstige*, der die verbleibenden Treffer erfasst, wie in [Kein Kanal identifiziert](/help/components/c-marketing-channels/c-faq.md#no-channel-identified) beschrieben.

## Beziehung zwischen Erstkontakt und Letztkontakt

Um die Interaktion zwischen den veralteten Erstkontakt- und Letztkontaktdimensionen zu verstehen und zu bestätigen, dass Überschreibungen erwartungsgemäß funktionieren, können Sie einen Erstkontaktkanalbericht abrufen, der sich auf einen Letztkontaktkanalbericht bezieht, wobei Ihre wichtigste Erfolgsmetrik hinzugefügt wird (siehe Beispiel unten). Das Beispiel zeigt die Interaktion zwischen Erstkontakt- und Letztkontaktkanälen.

![](assets/int-channel3.png)

Die Schnittmenge, bei der Erstkontakt gleich Letztkontakt ist, ist die Diagonale der Tabelle. Sowohl „Direkt“ als auch „Sitzungsaktualisierung“ erhalten nur dann eine Letztkontakt-Gutschrift, wenn sie auch der Erstkontaktkanal sind, da sie keine Gutschrift von anderen persistenten Kanälen erhalten können (hervorgehobene Zeilen).

## Gründe für „Kein Kanal erkannt“ {#no-channel-identified}

Wenn Ihre Regeln keine Daten erfassen oder die Regeln nicht korrekt konfiguriert sind, zeigt der Bericht die Daten in der Zeile [!UICONTROL Kein Kanal identifiziert] im Bericht an. Sie können beispielsweise am Ende der Verarbeitungsreihenfolge einen Regelsatz mit dem Namen *Sonstige* einrichten, der internen Traffic auch wie folgt identifiziert:

![](assets/example_other.png)

Diese Art von Regel dient als Auffangbehälter, um zu gewährleisten, dass Kanal-Traffic stets externem Traffic entspricht und in der Regel nicht **[!UICONTROL Kein Kanal identifiziert zugeordnet wird]**. Achten Sie darauf, keine Regel zu erstellen, die auch internen Traffic erkennt. Zur Erstellung einer wirksamen Regel „Sonstige“ ist es häufig am sinnvollsten, den Kanalwert auf **[!UICONTROL Verweisende Domäne]** oder **[!UICONTROL Seiten-URL]** zu setzen.

>[!NOTE]
>
>Es kann dennoch vorkommen, dass Kanal-Traffic teilweise in die Kategorie „Kein Kanal identifiziert“ fällt. Beispiel: Ein Besucher öffnet die Site und versieht eine Seite mit einem Lesezeichen. Beim gleichen Besuch kehrt dieser Besucher über das Lesezeichen zur Seite zurück. Da es sich dabei nicht um die erste Seite des Besuchs handelt, wird es weder dem direkten Kanal noch einem anderen Kanal zugeordnet, da keine Referrer-Domäne vorliegt.

## Gründe für „Intern“ (Sitzungsaktualisierung) {#internal}

Last Touch Internal (Session Refresh) kann nur auftreten, wenn es auch die erste Berührung war - siehe &quot;Beziehung zwischen First &amp; Last Touch&quot; oben. Die folgenden Szenarien erläutern, wie eine Sitzungsaktualisierung ein Erstkontaktkanal sein könnte.

* **Sitzungs-Timeout**: Ein Besucher besucht die Website und lässt die Registerkarte dann in ihrem Browser geöffnet, um sie später zu verwenden. Der Interaktionszeitraum des Besuchers läuft ab (oder er löscht seine Cookies freiwillig), und er verwendet die geöffnete Registerkarte, um die Website erneut zu besuchen. Da die verweisende URL eine interne Domäne ist, wird der Besuch als Sitzungsaktualisierung klassifiziert.

* **Nicht alle Seiten der Site sind mit Tags versehen**: Ein Besucher landet auf Seite A, der nicht mit Tags versehen ist, und wechselt dann zu Seite B, die mit Tags versehen ist. Seite A wird als interner Referrer angesehen, und der Besuch wird als Sitzungsaktualisierung klassifiziert.

* **Umleitungen**: Wenn eine Umleitung nicht so eingerichtet ist, dass sie die Daten des Werbers an die neue Landingpage weiterleitet, gehen die Daten des echten Werbers verloren und jetzt erscheint die Umleitungsseite (wahrscheinlich eine interne Seite) als verweisende Domäne. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

* **Domänenübergreifender Traffic**: Ein Besucher wechselt von einer Domäne, die zu Suite A ausgelöst wird, zu einer zweiten Domäne, die zu Suite B ausgelöst wird. Wenn in Suite B die interne URL-Filter die erste Domäne enthalten, wird der Besuch in Suite B als intern aufgezeichnet, da Marketing-Kanal ihn als neuen Besuch in der zweiten Suite sehen. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

* **Lange Ladezeiten** der Einstiegsseite: Ein Besucher landet auf Seite A, der sehr umfangreich ist, und der Adobe Analytics-Code befindet sich unten auf der Seite. Bevor der gesamte Inhalt (einschließlich Adobe Analytics-Bildanforderungen) geladen werden kann, klickt der Besucher auf Seite B. Seite B löst ihre Adobe Analytics-Bildanforderung aus. Da die Bildanforderung von Seite A nie geladen wurde, wird die zweite Seite als erster Treffer des Besuchs in Adobe Analytics angezeigt, wobei Seite A als Referrer dient. Der Besuch wird als Sitzungsaktualisierung klassifiziert.

* **Löschen von Cookies auf der Mid-Site**: Ein Besucher besucht die Site, und während der Sitzung werden die Cookies gelöscht. Die Erstkontakt- und Letztkontakt-Kanäle werden zurückgesetzt, und der Besuch wird als Sitzungsaktualisierung klassifiziert (weil der Referrer intern ist).

Nachstehend finden Sie ein Beispiel dafür, wie &quot;Intern (Sitzungsaktualisierung)&quot;sowohl als First Touch- als auch als Last Touch-Kanal eingestellt wird:

* Tag 1: Der Benutzer gelangt per Anzeige zur Site. Erstkontakt- und Letztkontakt-Kanäle werden auf „Anzeige“ eingestellt.
* Tag 2: Der Benutzer gelangt per natürlicher Suche zur Site. Erstkontakt bleibt „Anzeige“, Letztkontakt wird auf „Natürliche Suche“ eingestellt.
* Tag 35: Der Benutzer war seit 33 Tagen nicht mehr auf der Site und kehrt über die Registerkarte zurück, die er in seinem Browser geöffnet hatte. Bei einem Interaktionsfenster von 30 Tagen wäre das Fenster geschlossen, und die Marketingkanal-Cookies wären abgelaufen. Die Erstkontakt- und Letztkontakt-Kanäle werden zurückgesetzt und auf „Sitzungsaktualisierung“ eingestellt, da der Benutzer von einer internen URL kam.

## Warum werden einige Kanal nach der Änderung der Verarbeitungsregeln für Marketing Kanal nicht geändert?

Manchmal werden Verarbeitungsregeln für Marketing Kanal falsch eingerichtet, sodass Verarbeitungsregeln geändert werden müssen. Nach dem Anwenden der Änderungen sehen Sie einige Metriken, die Daten weiterhin einem falschen Kanal zuordnen. Es gibt mehrere Punkte zu berücksichtigen:

* **Marketing-Kanal-Daten werden in Echtzeit** erfasst: Marketing-Kanal-Daten werden bei der Datenerfassung verarbeitet und sind zu 100 % dauerhaft. Eine Änderung der Verarbeitungsregeln wirkt sich nicht rückwirkend auf die Daten aus.
* **Das Ändern von Verarbeitungsregeln hat keine unmittelbaren Auswirkungen auf First Touch-Daten**: Beispiel:
   1. Ein Benutzer gelangt über Ihren E-Mail-Kanal, weil er falsch eingerichtet wurde, und verlässt dann Ihre Site.
   2. Am nächsten Tag ändern Sie Ihre E-Mail-Verarbeitungsregel, um sie zu korrigieren.
   3. Dieser Benutzer kommt mehrere Tage später durch kostenlose Suche zurück und kauft ein.
   4. Der E-Mail-Kanal erhält First Touch-Gutschrift und die kostenlose Suche erhält Last Touch-Gutschrift.

   Auch mehrere Tage nach Änderung der Verarbeitungsregeln können Daten im falschen First Touch-Kanal erfasst werden. First Touch-Daten werden kontinuierlich im falschen Kanal erfasst, bis die Benutzerinteraktion abläuft.

Die beste Möglichkeit, diese Diskrepanzen zu beheben, besteht darin, einen oder beide der folgenden Schritte durchzuführen:

* **Manuelles Ablaufdatum aller Besucher-Interaktionszeiträume**: Diese Einstellung läuft alle First Touch- und Last Touch-Kanal in allen Besuchern sofort ab:
   1. Gehen Sie zu Admin Tools > Report Suites.
   2. Bewegen Sie den Mauszeiger über &quot;Bildbearbeitungseinstellungen&quot;> &quot;Marketing-Kanal&quot;> &quot;Besucher-Interaktionsablauf&quot;
   3. Klicken Sie auf Alle ablaufen.
   4. Klicken Sie auf OK, um das Popup-Fenster mit der Warnung anzuzeigen und zu bestätigen, dass Sie wissen, was es tun wird.

* **Nur Letztkontakt-Metriken der Ansicht ab dem Zeitpunkt, zu dem Sie die Regeln vorwärts** korrigiert haben: Letztkontakt-Metriken folgen immer dem aktuellen Regelsatz. Die Ansicht der Zeit ab dem Zeitpunkt, zu dem Sie die Verarbeitungsregeln ordnungsgemäß weitergeleitet haben, spiegelt die aktuellsten Verarbeitungsregeln wider.
