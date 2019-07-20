---
description: 'null '
seo-description: 'null '
seo-title: Bewährte Verfahren
title: Bewährte Verfahren
uuid: d 1 e 9 bfff -9 b 04-4 e 3 e -9 b 4 e-a 6 e 527 b 1 b 2 e 3
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# Bewährte Verfahren

>[!NOTE]
>
>Beachten Sie, dass die Kennzeichnung jedes Mal überprüft werden muss, wenn eine neue Report Suite erstellt wird oder wenn in einer vorhandenen Report Suite neue Variable aktiviert ist. Sie müssen die Beschriftung möglicherweise auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen zur Verfügung stellen können, für die eine Beschriftung erforderlich ist. Durch eine erneute Implementierung Ihrer Mobile Apps oder Websites kann sich die Art und Weise der Verwendung vorhandener Variablen ändern. Dadurch kann ebenfalls eine Aktualisierung der Beschriftungen erforderlich sein.

## Direkt und indirekt identifizierbare IDs {#section_030799AA1397433FBA61A2BC60A7A750}

Bevor Sie ermitteln, welche Beschriftungen den einzelnen Variablen und Feldern hinzugefügt werden müssen, sollten Sie zunächst die Grundlagen zu den IDs kennen, die Sie in Ihren Analytics-Daten erfassen, und entscheiden, welche hiervon Sie für DSGVO-Anfragen verwenden wollen. Die DSGVO erweitert den Umfang dessen, was als ID gilt. IDs lassen sich allgemein in zwei Klassen unterteilen: direkt identifizierbare (Identitätsbeschriftung: I1) und indirekt identifizierbare IDs (Identitätsbeschriftung: I2).

* **Direkt identifizierbare IDs (I1)**: benennen entweder die Person oder bieten eine direkte Methode, sie zu kontaktieren. Dies umfasst beispielsweise den Namen einer Person (selbst ein allgemeiner Name, wie z. B. Max Müller, den viele Menschen gemeinsam haben), E-Mail-Adressen, Telefonnummern usw. Auch eine Postanschrift ohne Name kann als direkt identifizierbar gelten, obwohl statt einer bestimmten Person ein übergeordneter Haushalt oder ein Unternehmen identifiziert wird.
* **Indirekt identifizierbare IDs (I2)**: ermöglichen nicht die direkte Identifikation einer Person, sondern müssen mit anderen Informationen (ob in Ihrem Besitz oder nicht) kombiniert werden, um die Person zu bestimmen. Hierzu zählen beispielsweise Kundentreue- oder im Unternehmens-CRM-System verwendete IDs, die für jeden Kunden eindeutig sind. Unter der DSGVO können die anonymen IDs, die in von Analytics verwendeten Tracking-Cookies gespeichert werden, als indirekt identifizierbar gelten, obwohl sie nur ein Gerät und keine Person identifizieren können. Auf einem gemeinsam genutzten Gerät können diese Cookies nicht zwischen den verschiedenen Nutzern des Systems unterscheiden. Das Cookie kann beispielsweise nicht dazu verwendet werden, einen Computer zu finden, der das Cookie enthält, jedoch kann eine Person, die auf den Computer zugreifen kann und das Cookie dort findet, das Analytics-Cookie auf den Computer zurückführen.

   Auch eine IP-Adresse gilt als indirekt identifizierbar, da sie immer nur einem Gerät zugeordnet sein kann. Internetprovider können die IP-Adressen der meisten Benutzer jedoch ändern und tun dies regelmäßig. Deshalb können IP-Adressen mit der Zeit von mehreren Benutzern verwendet werden. Darüber hinaus kommt es nicht selten vor, dass mehrere Kunden eines Internetanbieters oder viele Mitarbeiter eines Unternehmens, die sich im selben Intranet befinden, eine externe IP-Adresse teilen. Deswegen unterstützt Adobe die Verwendung von IP-Adressen als IDs für [DSGVO-Anfragen](../../admin/c-data-governance/gdpr-submit-access-delete.md#concept_0941C076F76641FF8BF865C7C1CB916B) nicht. Wenn eine zulässige ID im Rahmen einer Löschanfrage verwendet wird, löschen wir darüber hinaus die IP-Adressen, die mit dieser ID aufgetreten sind. Sie müssen ermitteln, ob Sie andere IDs erfassen, die in diese Kategorie (I1/I2) fallen, aber nicht für die Verwendung als eindeutige ID für DSGVO-Anfragen geeignet sind.

Selbst wenn Ihr Unternehmen innerhalb Ihrer Analytics-Daten viele verschiedene IDs erfasst, können Sie nur einen Teil dieser IDs für DSGVO-Anfragen verwenden. Hierfür gibt es folgende mögliche Gründe:

* In Ihren eigenen Systemen können Sie eine der IDs (z. B. die E-Mail-Adresse) einer anderen ID (z. B. der CRM-ID) zuordnen. Daraufhin verwenden Sie zur Einheitlichkeit nur die CRM-ID für DSGVO-Anfragen in Ihrer DSGVO-Verarbeitung.
* Sie verfügen nicht über eine Methode, um zu überprüfen, ob die Person wirklich der Benutzer ist, der mit der ID verknüpft ist. Es kann beispielsweise sehr schwierig sein, zu überprüfen, ob eine IP-Adresse immer nur von einer einzigen Person verwendet wurde und ob der Benutzer, der die Anfrage sendet, wirklich diese Person ist.
* Manche IDs gelten für mehrere Personen und Sie können nicht riskieren, Informationen zu anderen Personen mit derselben ID zurückzugeben. Selbst wenn Sie beispielsweise validieren können, dass der Name der Person Max Müller lautet, können Sie nicht alle Daten über alle Max Müllers in Ihrem System zurückgeben.
* Ein weiteres Beispiel ist die Geräte-ID, wie z. B. die Analytics-Cookie-ID. Wenn die ID in einer App auftritt, gehen Sie vielleicht davon aus, dass alle Interaktionen unter Verwendung dieser ID dem Besitzer des entsprechenden Mobilgeräts zur Verfügung stehen sollten. Wenn diese ID jedoch auf einem gemeinsam genutzten Gerät verwendet wird, wie z. B. einem PC oder Computer in einer Bibliothek oder einem Internetcafé, können Sie nicht zwischen den verschiedenen Benutzern dieses Geräts unterscheiden. Deshalb ist das Risiko, Daten anderer Benutzer zurückzugeben, möglicherweise zu hoch, um diesen ID-Typ zu verwenden.

## Best Practices für Analytics-unterstützte IDs {#section_B6481505FF1949498D4B4B35B780D050}

Anhand dieser Tabelle können Sie die ID-Typen bestimmen, mit deren Hilfe Sie DSGVO-Anfragen an Analytics senden. Sobald Sie diese Informationen kennen, können Sie die anderen Beschriftungen, die Sie für Ihre Variablen verwenden sollten, leichter bestimmen.

<table id="table_E25612E32A03449A8E5DA00B88FCEB9E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> ID-Typ </th> 
   <th colname="col2" class="entry"> Recommendations </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie-IDs </p> 
    <ul id="ul_CB43CEA3054E490585CBF3AB46F95B5B"> 
     <li id="li_9174CB3910AF4EF8BA7165DB537765A5"> <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_analytics.html" format="html" scope="external">Analytics-Cookie (Legacy)</a> </li> 
     <li id="li_7B6A9A788BBD47428315B3893FC07BC3"> <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/" format="https" scope="external"> Identitätsdienst-Cookie </a> (ECID), früher Marketing Cloud ID (MCID) </li> 
    </ul> </td> 
   <td colname="col2"> <p>Diese Cookies identifizieren ein Gerät oder genauer gesagt einen Browser für einen Benutzer eines Geräts. Auf einem gemeinsam genutzten Gerät, auf dem ein allgemeiner Login verwendet wird, kann diese ID für mehrere/alle Benutzer des Geräts gelten. Adobe hat <a href="https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.htm" format="html" scope="external">einheitlichen JavaScript-Code</a> entwickelt, den Sie in Ihre Website einfügen können, um diese Cookies zu erfassen, sofern Sie sie für DSGVO-Anfragen zulassen wollen. </p> <p>Benutzer des mobilen Adobe Analytics-SDK verfügen auch über eine Experience Cloud-ID (ECID). Im SDK sind API-Aufrufe enthalten, die diese ID auslesen. So können Sie Ihre App so erweitern, dass sie die ID für DSGVO-Anfragen erfasst. </p> <p>Viele Unternehmen behandeln Browsercookie-IDs wie IDs gemeinsam genutzter Geräte. Dementsprechend unterstützen sie in Absprache mit ihren Rechtsabteilungen diese IDs möglicherweise nicht als zulässige IDs für DSGVO-Anfragen, geben nur begrenzte Daten zurück, wenn diese IDs verwendet werden, oder akzeptieren sie nur für Löschanfragen. </p> <p>Diese Cookies verfügen über eine ID-DEVICE-Beschriftung, die nicht geändert werden kann (sowie die Beschriftungen „I2“ und „DEL-DEVICE“). Die standardmäßige Adobe Analytics-Konfiguration gibt nur allgemeine Informationen zum Gerät, wie z. B. Gerätetyp, Betriebssystem, Browser usw., sowie Uhrzeit und Datum des Besuchs unter Verwendung dieser IDs zurück. Wenn Sie diese IDs jedoch wie unten erläutert für DSGVO-Anfragen unterstützen möchten, können Sie ACC-ALL-Beschriftungen hinzufügen oder entfernen, um genau die Felder zu konfigurieren, die bei einer DSGVO-Zugriffsanfrage zurückgegeben werden sollen. </p> <p>Insbesondere wenn die Report Suite zu einer Mobile App gehört und Ihre Mobile App eine Anmeldung erfordert, gehen Sie möglicherweise davon aus, dass die Experience Cloud-ID für das Gerät mit einem bestimmten Benutzer verknüpft ist, und versehen deshalb mehr Felder mit der ACC-ALL-Beschriftung, einschließlich der Namen der besuchten Seiten, aufgerufener Produkte usw. </p> <p>Hinweis: Wenn Sie die Option „expandIds“ in Ihrer DSGVO-Anfrage angeben, enthalten Ihre Anfragen zusätzlich zu den anderen von Ihnen angegebenen IDs immer Cookie-IDs. Weitere Einzelheiten finden Sie unter <a href="../../admin/c-data-governance/gdpr-analytics-ids.md#section_D55C0722BC834118BE6F958C30AD5913" format="dita" scope="local">ID-Erweiterung</a>. In diesen Instanzen geben Treffer, die außer einer Cookie-ID keine weiteren IDs aufweisen, im Rahmen der Zugriffsanfragen nur mit ACC-ALL beschriftete Daten zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IDs in benutzerspezifischen Variablen </p> </td> 
   <td colname="col2"> <p>Manche Kunden speichern IDs in <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/props_eVars.html" format="html" scope="external">benutzerspezifischen Traffic-Variablen (Props) oder benutzerspezifischen Konversionsvariablen (eVars) </a>. Zwar wird am häufigsten die CRM-ID verwendet, jedoch sind auch andere IDs möglich, darunter E-Mail-Adressen, Anmeldenamen, Treuenummern oder Hashes dieser Werte. </p> 
    <ul id="ul_0B9492CF786046BB97E31CCF83A85FEA"> 
     <li id="li_D35B61CC6A8B485A8E09358A46D3F598">Wenn Sie eine dieser IDs für DSGVO-Anfragen verwenden wollen, müssen Sie das Feld, das sie enthält, mit einer ID-PERSON-Beschriftung versehen. </li> 
     <li id="li_94541340B054436297C5565F074413DC">(Deutlich seltener) Wenn eine ID in diesen benutzerspezifischen Variablen nur ein Gerät identifiziert, das möglicherweise von mehreren Benutzern gemeinsam genutzt wird, können Sie stattdessen die ID-DEVICE-Beschriftung verwenden. </li> 
     <li id="li_8115B999E8DA46CAB359BCF1F4A4DCAE">Diese Felder erfordern auch I1- oder I2-Beschriftungen und sollten darüber hinaus die Beschriftung DEL-PERSON oder DEL-DEVICE enthalten. Für gewöhnlich stimmt die PERSON-/DEVICE-Option der DEL-Beschriftung mit der PERSON-/DEVICE-Option der ID-Beschriftung überein. </li> 
    </ul> <p> Es kommt selten vor, dass eine Report Suite über mehr als ein oder zwei benutzerspezifische Variablen verfügt, die IDs enthalten, die Sie zur Identifikation von Datensubjekten für DSGVO-Anfragen verwenden können. Möglicherweise sind den I1- oder I2-Beschriftungen mehrere Variablen zugeordnet, jedoch verfügt in der Regel nur eine von ihnen über ID-PERSON- oder ID-DEVICE-Beschriftungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerspezifische Besucher-ID </p> </td> 
   <td colname="col2"> <p>Obwohl sie nicht häufig verwendet wird, unterstützt Analytics auch Implementierungen, bei denen eine benutzerspezifische Besucher-ID bereitgestellt wird, die sofern vorhanden anstelle des Legacy-Analytics-Trackingcookies verwendet wird. Dieses Feld verfügt über die Beschriftungen „I2“, „ID-PERSON“ und „DEL-PERSON“. </p> <p>Viele Implementierungen leiten diese ID aus einer CRM-ID ab, damit sie nur vorhanden ist, während die entsprechende Person bei der Site angemeldet ist. So kann dieselbe benutzerspezifische Besucher-ID auf mehreren Geräten verwendet werden. Ein technischer Nachteil hierbei ist es, dass das Tracking, das stattfindet, bevor sich der Benutzer anmeldet, nicht dem Tracking nach der Anmeldung zugeordnet werden kann. Wenn Sie stattdessen die benutzerspezifische Besucher-ID verwenden, um ein Gerät zu identifizieren, sollten Sie die ID-PERSON- und DEL-PERSON-Beschriftungen zu ID-DEVICE bzw. DEL-DEVICE ändern. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Best Practices für Löschbeschriftungen {#section_08166C99B48E49218392FAC18922C10E}

>[!NOTE]
>
>Bei Props wird immer zwischen Groß- und Kleinschreibung unterschieden. eVars sind standardmäßig nicht von der Schreibweise abhängig, können jedoch über die Adobe-Kundenunterstützung entsprechend konfiguriert werden. Wenn Sie eVars verwenden, die von der Groß-/Kleinschreibung abhängig sind und eine ID enthalten, müssen Sie beim Einreichen von DSGVO-Anfragen auf die richtige Schreibweise achten, damit sie mit der Schreibweise in den Hits übereinstimmt, die die entsprechenden IDs enthalten.

Die Löschbeschriftungen DEL-DEVICE und DEL-PERSON sollten sparsam eingesetzt werden. Wenn sie auf eine Variable angewendet werden, die keine ID enthält, die im Rahmen der DSGVO-Anfrage verwendet wurde, ändern sich fast in allen Fällen die Werte (Metriken) in älteren Analytics-Berichten.

* Wir empfehlen, dass Sie eine dieser Beschriftungen auf jede Variable mit der Beschriftung „I1“, „I2“ oder „S1“ anwenden. Sie können nicht auf Variablen ohne die I1-, I2- oder S1-Beschriftung angewendet werden.
* Durch die DEL-Beschriftungen werden diese Variablen [anonymisiert](../../admin/c-data-governance/gdpr-labels.md#section_F3DEE591671A4B16A8E043F91C137ECB) (die ID wird durch eine zufällige Zeichenfolge ersetzt, der „GDPR-“ vorangestellt wird). Dieser anonymisierte Wert wird in allen Instanzen des ursprünglichen Wertes ersetzt – in allen Hits, die über eine in der Anfrage enthaltene ID identifiziert werden. Wenn es sich beim ursprünglichen Wert in diesem Feld um eine dieser IDs handelte, ändern sich die Berichtsmetriken nicht.
* Allgemein gilt: Wenn ein Feld die ID-DEVICE-Beschriftung aufweist, sollten Sie auch die Beschriftung DEL-DEVICE zuweisen.
* Und wenn dem Feld die ID-PERSON-Beschriftung zugewiesen wurde, sollten Sie auch die Beschriftung DEL-PERSON hinzufügen.
* Wenn für ein Feld keine ID-Beschriftung vorhanden ist, es jedoch identifizierbare Informationen enthält, die Sie anonymisieren wollen, ist die passende Beschriftung (DEVICE oder PERSON) von Ihrer Implementierung abhängig. Wenn Sie nur Cookie-IDs für DSGVO-Anfragen verwenden, sollten Sie DEL-DEVICE verwenden.
* Wenn Sie benutzerspezifische IDs in einem anderen Feld mit ID-PERSON-Beschriftung verwenden und Werte nur in Zeilen löschen wollen, in denen die ID auftritt, verwenden Sie DEL-PERSON.
* Wenn Sie die ID-Erweiterung verwenden und alle Werte für alle Hits auf allen identifizierten Geräten löschen wollen, verwenden Sie DEL-DEVICE. Bei Bedarf können Sie in diesem Fall sowohl die Beschriftung DEL-DEVICE als auch DEL-PERSON anwenden. Die Beschriftung DEL-PERSON ist jedoch unnötig, weil aufgrund der ID-Erweiterung alle Zeilen, die mit einer Personen-ID übereinstimmen, auch mit einer Geräte-ID übereinstimmen.
* Wenn Sie angeben, dass die ID-Erweiterung nicht verwendet wird, Sie jedoch für verschiedene Anfragen eine Kombination aus Geräte- und Personen-IDs verwenden, sollten Sie sowohl DEL-DEVICE- als auch DEL-PERSON-Beschriftungen für Variablen angeben, die beim Verwenden beider ID-Typen gelöscht werden sollen.
* Beachten Sie, dass bei der Angabe einer DEL-DEVICE- oder DEL-PERSON-Beschriftung für eine beliebige Variable, die nicht zusätzlich als ID für die jeweilige Anfrage verwendet wird (einschließlich einer erweiterten ID), eindeutige Werte in der betreffenden Variable nur für Treffer anonymisiert werden, in denen eine bestimmte (oder erweiterte) ID vorkommt. Wenn andere Treffer denselben Wert enthalten, erfolgt unter den anderen Speicherorten keine Aktualisierung. Dadurch kann sich die Anzahl (Metriken) ändern.

   Wenn beispielsweise drei Treffer den Wert „foo“ in eVar7 enthalten, jedoch nur einer davon auch eine ID in einer anderen Variable beinhaltet, die einem Löschvorgang zugeordnet ist, wird der Wert „foo“ für diesen Treffer zu einem Wert wie „GDPR-123456789“ geändert, während er für die anderen beiden Treffer unverändert bleibt. In einem Bericht, der Aufschluss über die Anzahl eindeutiger Werte für eVar7 gibt, werden nun mehr eindeutige Werte angezeigt als zuvor. In einem Bericht mit den Höchstwerten für eVars ist „foo“ möglicherweise nur mit zwei Instanzen enthalten (anstatt zuvor mit 3), und der neue Wert wird ebenfalls mit einer einzelnen Instanz angezeigt.

## Best Practices für Zugriffsbeschriftungen {#section_AC7E216F81C141FCA6A62F8836E06EE7}

Zwar verfügen nur wenige Felder über einige der anderen Beschriftungen, jedoch wird es häufig vorkommen, dass viele Felder ACC-Beschriftungen aufweisen. Die passenden Zugriffsbeschriftungen hängen von den IDs ab, die Sie für DSGVO-Anfragen verwenden.

<table id="table_A5B834CC08C641D99E2691A2361997E4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Bei Verwendung von ... </th> 
   <th colname="col2" class="entry"> ... beachten Sie folgende Empfehlungen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nur Geräte-IDs </p> </td> 
   <td colname="col2"> <p>Wenn Sie nur Cookie-IDs oder IDs mit ID-DEVICE-Beschriftung nutzen, sollten Sie die Beschriftung ACC-ALL verwenden. </p> <p>Sie erhalten ein Dateienpaar pro Zugriffsanfrage: eines mit einer Zeile für jeden passenden Treffer, das alle angegebenen ACC-ALL-Felder enthält, und ein zweites mit einer Zusammenfassung dieser Daten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Personen-IDs ohne ID-Erweiterung </p> </td> 
   <td colname="col2"> <p>Wenn Sie nur benutzerspezifische IDs mit der ID-PERSON-Beschriftung verwenden und die ID-Erweiterung nicht nutzen, sollten Sie ACC-PERSON-Beschriftungen verwenden. Sie müssen jedoch nicht die standardmäßigen ACC-ALL-Beschriftungen ändern. Diese Felder werden automatisch der Zugriffsanfrage hinzugefügt. </p> <p>Sie erhalten ein Dateienpaar pro Zugriffsanfrage: eines mit einer Zeile für jeden passenden Treffer, das alle angegebenen ACC-DEVICE- und ACC-PERSON-Felder enthält, und ein zweites mit einer Zusammenfassung dieser Daten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gemischte IDs und/oder ID-Erweiterung </p> </td> 
   <td colname="col2"> <p>Wenn Sie Geräte- und Personen-IDs in DSGVO-Anfragen hinzufügen oder benutzerspezifische IDs (benutzerspezifische Besucher-ID oder eine ID in einer Prop oder einer eVar) nutzen, müssen Sie auf die verwendeten ACC-Beschriftungen achten. Jede Zugriffsanfrage gibt zwei Dateienpaare zurück: eines mit den Daten aus Treffern, die eine passende Personen-ID enthalten, und ein zweites, das Daten aus Treffern enthält, die nicht mit der Personen-, aber mit der Geräte-ID übereinstimmen. </p> <p>Die „Personen-ID“-Dateien enthalten Daten zu allen Hits, die mit den Personen-IDs übereinstimmen, mit sämtlichen Feldern, die entweder über eine ACC-PERSON- oder ACC-ALL-Beschriftung verfügen (eine Datei mit allen übereinstimmenden Hits und die andere als Zusammenfassung). </p> <p>Das Geräte-ID-Dateienpaar enthält nur Felder, die eine ACC-ALL-Beschriftung aufweisen, und nur Treffer, die keine passende Personen-ID enthalten. Diese Dateien können Daten enthalten, die von anderen Benutzern eines gemeinsam genutzten Geräts generiert wurden. Deshalb sollten Sie sorgfältig überlegen, welche Felder mit ACC-ALL-Beschriftung Sie hinzufügen. Analytics fügt diese Beschriftung standardmäßig nur Feldern mit allgemeinen Geräteinformationen (Gerätetyp, Betriebssystem, Browser usw.) sowie Uhrzeit und Datum der einzelnen Hits hinzu. </p> <p>Sie können festlegen, dass Sie sowohl Geräte- als auch Personendateien von Adobe erhalten, und lediglich die Personendateien weitergeben. So geben Sie keine Daten zurück, die möglicherweise von anderen Benutzern eines gemeinsam genutzten Geräts generiert wurden. Sie können die Daten aus einer oder beiden Gruppen auch mit anderen Informationen kombinieren, die Ihnen zur betroffenen Person vorliegen, und sie in Ihrem eigenen Format zurückgeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

