---
description: 'null'
title: Best Practices für Beschriftungen
uuid: d1e9bfff-9b04-4e3e-9b4e-a6e527b1b2e3
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Best Practices für Beschriftungen

>[!NOTE] Beachten Sie, dass die Beschriftung jedes Mal überprüft werden muss, wenn eine neue Report Suite erstellt wird oder in einer vorhandenen Report Suite eine neue Variable aktiviert wird. Sie müssen die Beschriftung möglicherweise auch dann überprüfen, wenn neue Lösungsintegrationen aktiviert werden, da sie neue Variablen zur Verfügung stellen können, für die eine Beschriftung erforderlich ist. Eine erneute Implementierung Ihrer mobilen Apps oder Websites kann die Art und Weise ändern, wie vorhandene Variablen verwendet werden. Dies kann auch Aktualisierungen der Beschriftungen erforderlich machen.

## Direkt und indirekt identifizierbare IDs {#section_030799AA1397433FBA61A2BC60A7A750}

Bevor Sie ermitteln, welche Beschriftungen den einzelnen Variablen und Feldern hinzugefügt werden müssen, sollten Sie zunächst die Grundlagen zu den IDs kennen, die Sie in Ihren Analytics-Daten erfassen, und entscheiden, welche hiervon Sie für Datenschutzanfragen verwenden wollen. Datenschutz erweitert den Umfang dessen, was als ID gilt. IDs lassen sich in zwei breite Klassen unterteilen: direkt identifizierbar (Identitätskennzeichnung: I1) und indirekt identifizierbar (Identitätskennzeichnung: I2).

* **Eine direkt identifizierbare ID (I1)**: Benennen Sie die Person oder geben Sie eine direkte Kontaktmethode an. Beispiele wären der Name einer Person (selbst ein geläufiger Name wie John Smith, der von Hunderten von Menschen geteilt werden kann), eine beliebige E-Mail-Adresse oder Telefonnummer eines Benutzers usw. Eine Postanschrift ohne Namen kann als direkt identifizierbar angesehen werden, auch wenn sie nur einen Haushalt oder ein Unternehmen anstelle einer bestimmten Person innerhalb dieses Haushalts oder Unternehmens identifiziert.
* **Eine indirekt identifizierbare ID (I2)**: Ermöglicht nicht die Identifizierung einer Person selbst, sondern kann mit anderen Informationen (die in Ihrem Besitz sein können oder nicht) kombiniert werden, um jemanden zu identifizieren. Beispiele wären eine Kundenloyalitätsnummer oder eine von einem CRM-System der Firma verwendete ID, die für jeden Kunden eindeutig ist. Unter Datenschutz können die anonymen IDs, die in von Analytics verwendeten Tracking-Cookies gespeichert werden, als indirekt identifizierbar gelten, obwohl sie nur ein Gerät und keine Person identifizieren können. Auf einem gemeinsam genutzten Gerät können diese Cookies nicht zwischen den verschiedenen Nutzern des Systems unterscheiden. So kann beispielsweise der Cookie nicht verwendet werden, um einen Computer zu finden, der das Cookie enthält. Wenn jemand Zugriff auf den Computer hat und das Cookie sucht, können die Analytics-Cookie-Daten dann an den Computer zurückgebunden werden.

   Eine IP-Adresse gilt auch als indirekt identifizierbar, da sie zu jedem Zeitpunkt nur einem einzelnen Gerät zugewiesen werden kann. ISPs können jedoch die IP-Adressen für die meisten Benutzer regelmäßig ändern, sodass im Laufe der Zeit eine IP-Adresse von einem ihrer Benutzer verwendet wurde. Es ist auch nicht ungewöhnlich, dass viele Kunden eines ISP oder mehrere Mitarbeiter innerhalb eines Unternehmens, die sich im selben Intranet befinden, dieselbe externe IP-Adresse teilen. Deswegen unterstützt Adobe die Verwendung von IP-Adressen als IDs für [Datenschutzanfragen nicht.](/help/admin/c-data-governance/gdpr-submit-access-delete.md#submit-requests) Wenn eine zulässige ID im Rahmen einer Löschanfrage verwendet wird, löschen wir darüber hinaus die IP-Adressen, die mit dieser ID aufgetreten sind. Sie müssen ermitteln, ob Sie andere IDs erfassen, die in diese Kategorie (I1/I2) fallen, aber nicht für die Verwendung als eindeutige ID für Datenschutzanfragen geeignet sind.

Selbst wenn Ihr Unternehmen innerhalb Ihrer Analytics-Daten viele verschiedene IDs erfasst, können Sie nur einen Teil dieser IDs für Datenschutzanfragen verwenden. Mögliche Gründe hierfür sind:

* Innerhalb Ihrer eigenen Systeme können Sie eine ID (z. B. eine E-Mail-Adresse) einer anderen ID zuordnen (z. B. einer CRM-ID). Daraufhin verwenden Sie zur Einheitlichkeit nur die CRM-ID für Datenschutzanfragen in Ihrer Datenschutzverarbeitung.
* Sie haben keine Methode, zu bestätigen, dass jemand tatsächlich die mit der ID verbundene Person ist. So kann es zum Beispiel sehr schwierig sein, zu bestätigen, dass eine IP-Adresse nur von einer einzigen Person verwendet wurde und dass die Person, die den Antrag einreichte, tatsächlich diese Person ist.
* Einige IDs entsprechen möglicherweise mehreren Personen und Sie möchten nicht riskieren, dass Informationen über eine Person an eine andere Person mit derselben ID zurückgegeben werden. Wenn Sie beispielsweise überprüfen können, ob der Name eines Benutzers John Smith ist, möchten Sie möglicherweise nicht alle Daten zu allen John Smiths in Ihrem System zurückgeben.
* Ein weiteres Beispiel ist eine Geräte-ID, z. B. die Analytics-Cookie-ID. Tritt die ID auf einer Handy-App auf, können Sie entscheiden, dass alle Interaktionen, die diese ID verwenden, für den Inhaber des Mobiltelefons verfügbar sein sollten. Wenn es jedoch auf einem freigegebenen Gerät wie einem Heimcomputer oder einem in einer Bibliothek oder einem Internetcafé vorkommt, können Sie entscheiden, dass Sie nicht zwischen Benutzern dieses Geräts unterscheiden können und das Risiko der Rückgabe von Daten für einen anderen Benutzer zu groß ist, um die Verwendung dieser ID zu ermöglichen.

## Best Practices für Analytics-unterstützte IDs  {#section_B6481505FF1949498D4B4B35B780D050}

Anhand dieser Tabelle können Sie die ID-Typen bestimmen, mit deren Hilfe Sie Datenschutzanfragen an Analytics senden. Sobald Sie diese Informationen kennen, ist es einfacher, die anderen Beschriftungen zu bestimmen, die Sie für Ihre Variablen verwenden sollten.

<table id="table_E25612E32A03449A8E5DA00B88FCEB9E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> ID-Typ </th> 
   <th colname="col2" class="entry"> Empfehlungen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie-IDs </p> 
    <ul id="ul_CB43CEA3054E490585CBF3AB46F95B5B"> 
     <li id="li_9174CB3910AF4EF8BA7165DB537765A5"> <a href="https://marketing.adobe.com/resources/help/de_DE/whitepapers/cookies/cookies_analytics.html">Analytics-Cookie (Legacy)</a> </li> 
     <li id="li_7B6A9A788BBD47428315B3893FC07BC3"> <a href="https://marketing.adobe.com/resources/help/de_DE/mcvid/">Identity Service Cookie</a> (ECID), zuvor als Marketing Cloud ID (MCID) bezeichnet </li> 
    </ul> </td> 
   <td colname="col2"> <p>Diese Cookies kennzeichnen ein Gerät oder, genauer gesagt, einen Browser für einen Benutzer eines Geräts. Bei einem freigegebenen Gerät, bei dem eine gemeinsame Anmeldung verwendet wird, könnte diese ID für alle Benutzer des Geräts gelten. Adobe hat <a href="https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.htm"> einheitlichen JavaScript-Code</a> entwickelt, den Sie in Ihre Website einfügen können, um diese Cookies zu erfassen, sofern Sie sie für Datenschutzanfragen zulassen möchten. </p> <p>Benutzer des mobilen Adobe Analytics-SDK verfügen auch über eine Experience Cloud ID (ECID). Im SDK sind API-Aufrufe enthalten, die diese ID auslesen. So können Sie Ihre App so erweitern, dass sie die ID für Datenschutzanfragen erfasst. </p> <p>Viele Unternehmen behandeln Browsercookie-IDs wie IDs gemeinsam genutzter Geräte. Dementsprechend unterstützen sie in Absprache mit ihren Rechtsabteilungen diese IDs möglicherweise nicht als zulässige IDs für Datenschutzanfragen, geben nur begrenzte Daten zurück, wenn diese IDs verwendet werden, oder akzeptieren sie nur für Löschanfragen. </p> <p>Diese Cookies haben eine ID-GERÄTEbeschriftung, die nicht geändert werden kann (sowie die Beschriftungen I2 und DEL-GERÄTE). Die standardmäßige Adobe Analytics-Konfiguration gibt nur allgemeine Informationen zum Gerät zurück, z. B. Gerätetyp, Betriebssystem, Browser usw. sowie die Uhrzeit/Daten, zu denen Ihre Website bei Verwendung dieser IDs besucht wurde. Wenn Sie diese IDs jedoch wie unten erläutert für Datenschutzanfragen unterstützen möchten, können Sie ACC-ALL-Beschriftungen hinzufügen oder entfernen, um genau die Felder zu konfigurieren, die bei einer Datenschutz-Zugriffsanfrage zurückgegeben werden sollen. </p> <p>Insbesondere wenn die Report Suite zu einer Mobile App gehört und Ihre Mobile App eine Anmeldung erfordert, gehen Sie möglicherweise davon aus, dass die Experience Cloud ID für das Gerät mit einem bestimmten Benutzer verknüpft ist, und versehen deshalb mehr Felder mit der ACC-ALL-Beschriftung, einschließlich der Namen der besuchten Seiten, aufgerufener Produkte usw. </p> <p>Hinweis: Wenn Sie die Option „expandIds“ in Ihrer Datenschutzanfrage angeben, enthalten Ihre Anfragen zusätzlich zu den anderen von Ihnen angegebenen IDs immer Cookie-IDs. Weitere Informationen finden Sie unter <a href="/help/admin/c-data-governance/gdpr-id-expansion.md">ID-Erweiterung</a>. In diesen Fällen geben Treffer, die nur eine Cookie-ID, aber keine andere ID haben, nur Daten mit der Bezeichnung ACC-ALL als Teil der Zugriffsanforderung zurück. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>IDs in benutzerspezifischen Variablen </p> </td> 
   <td colname="col2"> <p>Manche Kunden speichern IDs in <a href="https://marketing.adobe.com/resources/help/de_DE/sc/implement/props_eVars.html">benutzerspezifischen Traffic-Variablen (Props) oder benutzerspezifischen Konversionsvariablen (eVars)</a>. Zwar wird am häufigsten die CRM-ID verwendet, jedoch sind auch andere IDs möglich, darunter E-Mail-Adressen, Anmeldenamen, Treuenummern oder Hashes dieser Werte. </p> 
    <ul id="ul_0B9492CF786046BB97E31CCF83A85FEA"> 
     <li id="li_D35B61CC6A8B485A8E09358A46D3F598">Wenn Sie eine dieser IDs für Datenschutzanfragen verwenden wollen, müssen Sie das Feld, das sie enthält, mit einer ID-PERSON-Beschriftung versehen. </li> 
     <li id="li_94541340B054436297C5565F074413DC">(Deutlich seltener) Wenn eine ID in diesen benutzerspezifischen Variablen nur ein Gerät identifiziert, das möglicherweise von mehreren Benutzern gemeinsam genutzt wird, können Sie stattdessen die ID-DEVICE-Beschriftung verwenden. </li> 
     <li id="li_8115B999E8DA46CAB359BCF1F4A4DCAE">Diese Felder erfordern auch die Beschriftungen I1 oder I2 und sollten eine DEL-PERSON- oder DEL-GERÄTEbeschriftung enthalten. In der Regel stimmt die PERSON-/GERÄTEoption der DEL-Beschriftung mit der PERSON-/GERÄTEoption der ID-Beschriftung überein. </li> 
    </ul> <p> Es kommt selten vor, dass eine Report Suite über mehr als ein oder zwei benutzerspezifische Variablen verfügt, die IDs enthalten, die Sie zur Identifikation von Datensubjekten für Datenschutzanfragen verwenden können. Es können mehrere Variablen vorhanden sein, denen I1- oder I2-Beschriftungen zugewiesen sind. Normalerweise sind jedoch nur eine oder zwei dieser Variablen mit ID-PERSON- oder ID-GERÄTEbeschriftungen versehen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Benutzerspezifische Besucher-ID </p> </td> 
   <td colname="col2"> <p>Obwohl dies nicht oft verwendet wird, unterstützt Analytics auch eine Implementierung, bei der eine benutzerspezifische Besucher-ID bereitgestellt werden kann, die, falls vorhanden, anstelle des Legacy-Analytics-Tracking-Cookies verwendet wird. Dieses Feld enthält die Bezeichnungen I2, ID-PERSON und DEL-PERSON. </p> <p>Viele Implementierungen leiten diese ID von einer CRM-ID ab, sodass sie nur vorhanden ist, wenn jemand bei der Site angemeldet ist. Auf diese Weise kann dieselbe benutzerdefinierte Besucher-ID auch geräteübergreifend verwendet werden. Ein technischer Nachteil ist, dass die Verfolgung, die vor der Anmeldung des Benutzers erfolgt, nicht an die Verfolgung gebunden werden kann, die nach der Anmeldung erfasst wurde. Wenn Sie stattdessen die benutzerdefinierte Besucher-ID verwenden, um ein Gerät zu identifizieren, sollten Sie die Beschriftungen "ID-PERSON"und "DEL-PERSON"in "ID-GERÄT"bzw. "DEL-GERÄT"ändern. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Best Practices für Löschbeschriftungen {#section_08166C99B48E49218392FAC18922C10E}

>[!NOTE] Bei Props spielt die Groß-/Kleinschreibung keine Rolle. eVars sind standardmäßig nicht von der Schreibweise abhängig, können jedoch über die Adobe-Kundenunterstützung entsprechend konfiguriert werden. Wenn Sie eVars verwenden, die von der Groß-/Kleinschreibung abhängig sind und eine ID enthalten, müssen Sie beim Einreichen von Datenschutzanfragen auf die richtige Schreibweise achten, damit sie mit der Schreibweise in den Hits übereinstimmt, die die entsprechenden IDs enthalten.

Die Löschbeschriftungen DEL-DEVICE und DEL-PERSON sollten sparsam eingesetzt werden. Wenn sie auf eine Variable angewendet werden, die keine ID enthält, die im Rahmen der Datenschutzanfrage verwendet wurde, ändern sich fast in allen Fällen die Werte (Metriken) in älteren Analytics-Berichten.

* Wir empfehlen, dass Sie eine dieser Beschriftungen auf jede Variable mit der Beschriftung „I1“, „I2“ oder „S1“ anwenden. Sie können nicht auf Variablen ohne die I1-, I2- oder S1-Beschriftung angewendet werden.
* Durch die DEL-Beschriftungen werden diese Variablen [anonymisiert](/help/admin/c-data-governance/gdpr-labels.md#data-governance-labels) (die ID wird durch eine zufällige Zeichenfolge ersetzt, der „Datenschutz-“ vorangestellt wird). Derselbe anonymisierte Wert ersetzt alle Instanzen des ursprünglichen Werts in allen Treffern, die durch eine in der Anforderung verwendete ID identifiziert wurden. Wenn der ursprüngliche Wert in diesem Feld eine dieser IDs war, ändern sich die Berichtsmetriken nicht.
* Wenn ein Feld die ID-GERÄT der Beschriftung hat, sollten Sie auch die Bezeichnung DEL-GERÄT zuweisen.
* Wenn ein Feld die ID-PERSON hat, sollten Sie auch die Bezeichnung DEL-PERSON zuweisen.
* Wenn für ein Feld keine ID-Beschriftung vorhanden ist, es jedoch identifizierbare Informationen enthält, die Sie anonymisieren wollen, ist die passende Beschriftung (DEVICE oder PERSON) von Ihrer Implementierung abhängig. Wenn Sie nur Cookie-IDs für Datenschutzanfragen verwenden, sollten Sie DEL-DEVICE verwenden.
* Wenn Sie benutzerdefinierte IDs für ein anderes Feld mit einer ID-PERSON-Bezeichnung verwenden und diese nur in Zeilen löschen möchten, in denen diese ID auftritt, verwenden Sie DEL-PERSON.
* Wenn Sie die ID-Erweiterung verwenden und den gesamten Wert für alle Treffer auf allen identifizierten Geräten löschen möchten, verwenden Sie DEL-GERÄT. Sie können in diesem Fall sowohl die DEL-GERÄT- als auch die DEL-PERSON-Beschriftung anwenden, aber die DEL-PERSON-Beschriftung ist nicht erforderlich, da die ID-Erweiterung bedeutet, dass alle Zeilen, die einer Personen-ID entsprechen, auch mit einer Geräte-ID übereinstimmen.
* Wenn Sie nicht angeben, dass Sie die ID-Erweiterung verwenden möchten, sondern eine Kombination aus Geräte- und Personen-IDs für verschiedene Anforderungen verwenden, sollten Sie sowohl DEL-GERÄT- als auch DEL-PERSON-Beschriftungen für Variablen angeben, die gelöscht werden sollen, wenn einer der ID-Typen verwendet wird.
* Beachten Sie, dass bei der Angabe einer DEL-DEVICE- oder DEL-PERSON-Beschriftung für eine beliebige Variable, die nicht zusätzlich als ID für die jeweilige Anfrage verwendet wird (einschließlich einer erweiterten ID), eindeutige Werte in der betreffenden Variable nur für Treffer anonymisiert werden, in denen eine bestimmte (oder erweiterte) ID vorkommt. Wenn andere Treffer denselben Wert enthalten, erfolgt unter den anderen Speicherorten keine Aktualisierung. Dies kann dazu führen, dass sich Zählungen (Metriken) ändern.

   Wenn beispielsweise drei Treffer den Wert „foo“ in eVar7 enthalten, jedoch nur einer davon auch eine ID in einer anderen Variable beinhaltet, die einem Löschvorgang zugeordnet ist, wird der Wert „foo“ für diesen Treffer zu einem Wert wie „Datenschutz-123456789“ geändert, während er für die anderen beiden Treffer unverändert bleibt. In einem Bericht, der Aufschluss über die Anzahl eindeutiger Werte für eVar7 gibt, werden nun mehr eindeutige Werte angezeigt als zuvor. In einem Bericht mit den Höchstwerten für eVars ist „foo“ möglicherweise nur mit zwei Instanzen enthalten (anstatt zuvor mit 3), und der neue Wert wird ebenfalls mit einer einzelnen Instanz angezeigt.

## Best Practices für Zugriffsbeschriftungen  {#section_AC7E216F81C141FCA6A62F8836E06EE7}

Zwar verfügen nur wenige Felder über einige der anderen Beschriftungen, jedoch wird es häufig vorkommen, dass viele Felder ACC-Beschriftungen aufweisen. Die passenden Zugriffsbeschriftungen hängen von den IDs ab, die Sie für Datenschutzanfragen verwenden.

<table id="table_A5B834CC08C641D99E2691A2361997E4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wenn Sie ... </th> 
   <th colname="col2" class="entry"> ...diese Empfehlungen verwenden </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nur Geräte-IDs </p> </td> 
   <td colname="col2"> <p>Wenn die einzigen IDs, die Sie verwenden, Cookie-IDs oder ID-GERÄTE sind, sollten Sie nur die ACC-ALL-Bezeichnung verwenden. </p> <p>Sie erhalten für jede Zugriffsanforderung ein Dateipaar, eines mit einer Zeile für jeden Treffer mit allen angegebenen ACC-ALL-Feldern und eines mit einer Zusammenfassung dieser Daten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Personen-IDs ohne ID-Erweiterung </p> </td> 
   <td colname="col2"> <p>Wenn Sie nur benutzerdefinierte IDs mit ID-PERSON-Bezeichnung verwenden und keine ID-Erweiterung durchführen, sollten Sie ACC-PERSON-Beschriftungen verwenden. Sie müssen die Standardbeschriftungen für ACC-ALL jedoch nicht ändern. Diese Felder werden automatisch in die Zugriffsanfrage aufgenommen. </p> <p>Sie erhalten für jede Zugriffsanforderung ein Dateipaar, eines mit einer Zeile für jeden übereinstimmenden Treffer mit allen angegebenen ACC-GERÄT- und ACC-PERSON-Feldern und eines mit einer Zusammenfassung dieser Daten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gemischte IDs und/oder ID-Erweiterung </p> </td> 
   <td colname="col2"> <p>Wenn Sie Geräte- und Personen-IDs in Datenschutzanfragen hinzufügen oder benutzerspezifische IDs (benutzerspezifische Besucher-ID oder eine ID in einer Prop oder einer eVar) nutzen, müssen Sie auf die verwendeten ACC-Beschriftungen achten. Jede Zugriffsanfrage gibt zwei Dateienpaare zurück: eines mit den Daten aus Treffern, die eine passende Personen-ID enthalten, und ein zweites, das Daten aus Treffern enthält, die nicht mit der Personen-, aber mit der Geräte-ID übereinstimmen. </p> <p>Die "Person-ID"-Dateien enthalten Daten zu allen Treffern, die mit den Personen-IDs übereinstimmen, mit allen Feldern, die entweder eine ACC-PERSON- oder eine ACC-ALL-Bezeichnung haben (eine Datei mit allen übereinstimmenden Treffern und die andere eine Zusammenfassung). </p> <p>Das Geräte-ID-Dateienpaar enthält nur Felder, die eine ACC-ALL-Beschriftung aufweisen, und nur Treffer, die keine passende Personen-ID enthalten. Diese Dateien können Daten enthalten, die von anderen Benutzern eines gemeinsam genutzten Geräts generiert wurden. Deshalb sollten Sie sorgfältig überlegen, welche Felder mit ACC-ALL-Beschriftung Sie hinzufügen. Die Standardbeschriftung in Analytics wendet diese Beschriftung nur auf allgemeine Informationsfelder an, die sich auf das Gerät beziehen (Gerätetyp, Betriebssystem, Browser usw.) plus Datum/Uhrzeit jedes Treffers. </p> <p>Sie können festlegen, dass sowohl die Geräte- als auch die Personendateisätze von Adobe empfangen und dann nur die Personendateien freigegeben werden, damit keine potenziell von anderen Benutzern eines freigegebenen Geräts generierten Daten freigegeben werden. Oder Sie möchten Daten aus einem oder beiden Datensätzen mit anderen Informationen über die betroffene Person kombinieren und in Ihrem eigenen Format zurückgeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

