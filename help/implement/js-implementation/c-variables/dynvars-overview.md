---
description: Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.
keywords: Analytics Implementation
subtopic: Variables
title: Dynamische Variablen
topic: Developer and implementation
uuid: 1c6db083-570e-4bc4-858d-84cf46e7bec8
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Dynamische Variablen

Mit dynamischen Variablen können Sie Werte von einer Variablen in eine andere kopieren, ohne die vollständigen Werte mehrfach in die Bildanforderung auf Ihrer Site eingeben zu müssen.

Dynamische Variablen werden verwendet, wenn Sie die gleichen Daten (z. B. Kampagnen-Trackingcodes) gleichzeitig in mehreren Variablen verwenden. Dies ist eine häufige Vorgehensweise in den Fällen, in denen verschiedene Berichte eindeutige und wichtige Metriken beinhalten. Wenn Sie zum Beispiel interne Keywords in einer Variablen des Typs [!UICONTROL benutzerspezifischer Konversion] und in einer Variablen des Typs [!UICONTROL benutzerspezifischer Traffic] erfassen, können Sie die Metriken [!UICONTROL Umsatz] und [!UICONTROL Wöchentliche Unique Visitors] anzeigen, die sich jeweils auf diese Begriffe beziehen..

Dynamische Variablen sind auch zum Anzeigen von Daten unter verschiedenen Bedingungen bei der Berichterstellung nützlich. Ein Kampagnen-Trackingcode kann in mehreren eVars mit verschiedenen Zuordnungs- und Cookie-Ablaufeinstellungen erfasst werden. Auf diese Weise können die Benutzer selbst festlegen, wie sie die Konversionsmetriken dieser Kampagnen mit Attributen versehen möchten.

> [!NOTE]Dynamische Variablen werden in Kombination mit Cookies nicht unterstützt (s_cc, s_sq, s_fid, s_vi und sämtliche durch ein Plug-in bestimmte Cookies) Sie können `D=<cookie value>` nicht verwenden.

Ein deutlicher Vorteil von dynamischen Variablen besteht darin, lange Datenzeichenfolgen in mehreren Variablen zu erfassen, ohne die lange Zeichenfolge tatsächlich mehrmals übergeben zu müssen. In einigen Browsern ist die maximale Länge von HTTP-GET-Anforderungen eingeschränkt (einschließlich der Adobe-Bildanforderung). Durch die Verwendung dynamischer Variablen können Sie sicherstellen, dass alle Daten erfasst werden, indem die Länge der Anforderungen an die Server von Adobe in den Fällen verringert wird, in denen die Daten in mehreren Variablen dupliziert werden..

In der Adobe-Bildanforderung, die in der Seitenansicht auftritt, sehen Sie (wenn Sie dynamische Variablen zum Kopieren des Werts von [!UICONTROL benutzerspezifischem Traffic ] in [!UICONTROL benutzerspezifische Konversion ] verwenden) `v1=D=c1`1=1. Wenn eVar1 bereits zuvor einen Wert aus der Anforderung erhalten hat, kopieren die Server von Adobe während der Datenverarbeitung den Wert von [!UICONTROL benutzerspezifischem Traffic 1] dynamisch in [!UICONTROL benutzerspezifischer Konversion 1]. Als Ergebnis erscheint der Wert, der ursprünglich mit [!UICONTROL benutzerspezifischem Traffic 1] übergeben wurde, auch in den [!UICONTROL benutzerspezifischer Konversion 1]-Berichten.

Dynamische Variablen werden übergeben, indem eine Variable auf den gewünschten Wert gesetzt wird und andere Variablen anschließend auf `D=[variable abbreviation]` gesetzt werden. Abkürzungen für jede Variable finden Sie unter [Datenerfassungs-Abfrageparameter](/help/implement/js-implementation/data-collection/query-parameters.md). Dynamische Variablen können Daten von folgenden Orten abrufen:

* Andere Abfragezeichenfolgevariablen
* HTTP-Header (den Cookie-HTTP-Header ausgenommen)

Fügen Sie am Anfang des Wertes ein Präfix hinzu, um eine dynamische Variable zu generieren. Das Standard-Präfix ist „D=“. Es gibt zwei Methoden zum Kennzeichnen von dynamischen Variablen:

* Verwenden Sie das Standard-Präfix „D=“ (z. B.: s.prop1="D=User-Agent").
* Bei Implementierungen ohne JavaScript können Sie ein benutzerdefiniertes Präfix festlegen, indem Sie den Abfragezeichenfolgeparameter „D“ verwenden. Wenn der Abfragezeichenfolgeparameter z. B. `"&D=$"` ist, können Sie mit dem folgenden Befehl eine dynamische Variable generieren: `s.prop1="$User-Agent"`.

Die verwendete Variablenabkürzung muss mit dem Parameternamen der Variablen übereinstimmen, der in der Bildaufforderung übergeben wird. Einige Variablen besitzen mehrere akzeptierte Parameter, die in unterschiedlichen Fällen verwendet werden. Beispielsweise übergeben `pageName=` und `gn=` jeweils den Seitennamen, doch wird letzterer meistens in mobilen oder hartcodierten Implementierungen verwendet. Wenn in der Bildanforderung mit `pageName=` der Seitenname übergeben wird, ist `D=pageName` zulässig, `D=gn` jedoch nicht. Wenn die Bildanforderung `gn=` verwendet, ist `D=gn` zulässig und `D=pageName` nicht.

Die folgenden Informationen beziehen sich auf dynamische Variablen:

* Dynamische Variablen können mit allen Version des AppMeasurement-Codes verwendet werden.
* Bei dynamischen Variablen muss die Groß-/Kleinschreibung berücksichtigt werden.
* Dynamische Variablen unterstützen in Anführungszeichen gesetzte Literalzeichenketten.
* Der Austausch der dynamischen Variablen findet vor der Verarbeitung von Regeln, von VISTA oder von sonstigen Verarbeitungsschritten statt.
* Das Präfix „D=“ für dynamische Variablen muss an den Anfang des Variablenwertes gesetzt werden und nicht in die Mitte. Verwenden Sie zum Beispiel `c2='D="test7"+User-Agent'` anstelle von `c2='"test7"+D=User-Agent'`.

* Wie bei allen Implementierungsmethoden empfiehlt Adobe auch hier dringend, die Implementierung der dynamischen Variablen ausführlich in einer Entwicklungsumgebung zu testen, bevor sie in die Produktionsumgebung übernommen wird. Da die kopierten Zeichenfolgen in clientseitigen Debugging-Tools nicht vollständig sichtbar sind, sollten Sie die entsprechenden Analytics-Berichte auf eine erfolgreiche Implementierung hin überprüfen.
* Wenn Sie Werte zwischen Variablen mit verschiedenen Höchstlängen kopieren, beachten Sie, dass Werte gekürzt werden, wenn sie in eine Zielvariable mit geringerer Höchstlänge kopiert werden. So können für Variablen des Typs [!UICONTROL benutzerspezifischer Traffic] höchstens 100 Zeichen verwendet werden, wohingegen für Variablen des Typs [!UICONTROL benutzerspezifischer Konversion] 255 Zeichen verwendet werden können. Wenn Sie einen Wert mit einer Länge von 150 Zeichen aus s.eVar1 in s.prop1 kopieren und dabei dynamische Variablen verwenden, wird dieser Wert im Bericht [!UICONTROL benutzerspezifischer Traffic] bei 100 Zeichen gekürzt.

## Beispiele zu dynamischen Variablen {#section_5CE4468D978540FBA384B9D6477C92EC}

<!-- 

dynvars_examples.xml

 -->

Beispiele zu dynamischen Variablen, die Sie in Analytics verwenden können.

In der Adobe-Bildanforderung, die in der Seitenansicht auftritt, sehen Sie (wenn Sie dynamische Variablen zum Kopieren des Werts von [!UICONTROL benutzerspezifischem Traffic ] in [!UICONTROL benutzerspezifische Konversion ] verwenden) `v1=D=c1`1=1. Wenn eVar1 bereits zuvor einen Wert aus der Anforderung erhalten hat, kopieren die Server von Adobe während der Datenverarbeitung den Wert von [!UICONTROL benutzerspezifischem Traffic 1] dynamisch in [!UICONTROL benutzerspezifischer Konversion 1]. Als Ergebnis erscheint der Wert, der ursprünglich mit [!UICONTROL benutzerspezifischem Traffic 1] übergeben wurde, auch in den [!UICONTROL benutzerspezifischer Konversion 1]-Berichten.

Beachten Sie, dass der Wert für `D=[variable]` in Anführungszeichen gesetzt werden muss. Der Analytics-Code behandelt dies wie eine Zeichenfolge. Die Zeichenfolge wird bei der Übergabe in Analytics als URL kodiert (dies können Sie erkennen, wenn Sie die Anforderung im DigitalPulse-Debugger oder in einem ähnlichen Dienstprogramm anzeigen). Dies ist normal. Die Server von Adobe erkennen die `D=[variable]`-Konstruktion und kopieren den entsprechenden Wert, wenn sie auf diese Zeichenfolge treffen.

> [!NOTE]Wenn die Bildanforderung zum Verfolgen von Links dienen soll, muss der Typ des Links (Downloadlink=lnk_d, Ausstiegslink=lnk_e, Benutzerspezifischer Link=lnk_o) als Link-URL/Name (pev2) definiert sein. Links müssen manuell implementiert werden, bevor der Code manuell in das `<a href>`-Tag eingefügt werden kann.

> [!NOTE]Dynamische Variablen werden in Kombination mit Cookies nicht unterstützt (s_cc, s_sq, s_fid, s_vi und sämtliche durch ein Plug-in bestimmte Cookies) Sie können `D=<cookie value>` nicht verwenden.

<table id="table_A25D5EA2A8C446F5A55AB32955B9848C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> JavaScript-Beispiel </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.eVar1="D=pageName" 
    </code> </td> 
   <td colname="col2"> <p>Erfasst den Wert für „pageName“ in „eVar1“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.prop1='D=v2+":"+c2'&amp;nbsp; 
    </code> </td> 
   <td colname="col2"> <p>Verkettet „eVar2:prop2“ mit „prop1“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.prop1=s.eVar1="D=g"&amp;nbsp; 
    </code> </td> 
   <td colname="col2"> <p>Übergibt die Seiten-URL sowohl an „prop1“ als auch an „eVar1“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.eVar1="D=v0" 
    </code> </td> 
   <td colname="col2"> <p>Erfasst die Kampagne in „eVar1“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      s.prop1='D=User-Agent+" ;- "+Accept-Language' 
    </code> </td> 
   <td colname="col2"> <p>Verkettet die Header für Benutzeragenten und das Annehmen der Sprache in „prop1“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code>
      s.prop1="D=User-Agent" 
    </code> </td> 
   <td colname="col2"> <p>Erfasst den Benutzeragenten in „prop1“. </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_DD0B7F0648054E01A5F98CDF18D745E4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Beispiel für Bildanforderung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      /b/ss/rsid/?gn=Home&amp;D=~~&amp;c1=~~v0 /b/ss/rsid/?gn=Home&amp;D=~~&amp;c1=~~campaign /b/ss/rsid/?gn=Home&amp;c1=D%3dv0%3d&nbsp;is /b/ss/rsid/?gn=Home&amp;c1=%5b%5bv0%5d%5d%5b
    </code> </td> 
   <td colname="col2"> <p>Vier Möglichkeiten zum Festlegen von „prop1“ auf eine Kampagne </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code>
      /b/ss/rsid/?gn=Home&amp;D=~~&amp;c2=~~x-up-subno 
    </code> </td> 
   <td colname="col2"> <p> Zieht den Header „x-up-subno“ in „prop2“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code>
      c1=D%3DUser-Agent 
    </code> </td> 
   <td colname="col2"> <p> Macht „prop1“ zur dynamischen Variablen, die mit dem HTTP-Header „Benutzeragent“ gefüllt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      &amp;c1=D%3D%22test%22 
    </code> </td> 
   <td colname="col2"> <p> Macht „prop1“ zur dynamischen Variablen, die mit der Zeichenfolge „test“ gefüllt wird. Dies ist effizienter mit einer Verkettung, die den Operator „+“ verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      &amp;c1=D%3D%22US%3A%20%22%2BUser-Agent 
    </code> </td> 
   <td colname="col2"> <p> Macht „prop1“ zur dynamischen Variablen, die mit „UA:“ gefolgt vom Benutzeragenten gefüllt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <code class="syntax javascript">
      &amp;vid=D%3DX-TM-ANTID 
    </code> </td> 
   <td colname="col2"> <p> In diesem Beispiel wird nach einem eindeutigen Header gesucht, wobei es sich in diesem Fall um „X-TM-ANTID“ handelt. </p> </td> 
  </tr> 
 </tbody> 
</table>
