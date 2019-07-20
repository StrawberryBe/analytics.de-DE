---
description: Häufig gestellte Fragen über die automatische Konfiguration der Adobe Analytics-Implementierung. Bei der automatischen Konfigurationsmethode wird der AppMeasurement-Code für Sie verwaltet.
keywords: Dynamisches Tag-Management; Plugins; staging; Auswirkung auf aktuelle Einstellungen; Revisionsverlauf; potenzielle Fallstricke; Report Suite ID; Währungscode; Tracking-Server; ssl tracking server; benutzerdefinierter Code; Bibliotheksverwaltung
seo-description: Häufig gestellte Fragen über die automatische Konfiguration der Adobe Analytics-Implementierung. Bei der automatischen Konfigurationsmethode wird der AppMeasurement-Code für Sie verwaltet.
seo-title: Häufig gestellte Fragen zum Adobe Analytics-Tool
solution: Marketing Cloud, Analytics, Target, Dynamisches Tag-Management
title: Häufig gestellte Fragen zum Adobe Analytics-Tool
uuid: 8 fcef 933-e 305-4 a 95-a 033-9066 a 56 b 09 cd
translation-type: tm+mt
source-git-commit: 01a6fc7e44dc71b868bd38a4f6a5a4089eae6349

---


# Häufig gestellte Fragen zum Adobe Analytics-Tool

Häufig gestellte Fragen über die automatische Konfiguration der Adobe Analytics-Implementierung. The automatic configuration method manages the [!DNL AppMeasurement] code for you.

<table id="table_A50D00E2C47A473B92DA800FB08FE640"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Wo füge ich meine Plugins ein, wenn ich Adobe Analytics über DTM implementiere? </p> </td> 
   <td colname="col2"> <p> Wenn Sie DTM zum manuellen Hosten des <code>s_code</code> verwenden, können Plugins im selben Editor wie der gehostete <code>s_code</code> hinzugefügt werden, ganz so wie bei einer typischen Adobe Analytics-Implementierung. </p> <p>However, it is also an option to place the plugins in the editor within the <span class="term"> Customize Page Code</span> section of the tool settings. Beide Implementierungsmethoden sollten gleichermaßen effektiv sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wenn ich in der neuen Version des Tools Änderungen an der Konfiguration vornehme, kann ich sie im Staging testen, bevor ich sie in der Produktion veröffentliche? </p> </td> 
   <td colname="col2"> <p>Ja.  </p> <p>Alle Änderungen können im Staging getestet werden, so wie Sie es normalerweise auch vor der Bereitstellung in einer Produktionsumgebung tun würden. Wenn Sie sich gegen eine Veröffentlichung entscheiden, weil Sie im Staging Probleme feststellen, funktioniert der Produktionscode weiterhin wie vor der Veröffentlichung der neuen Integration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wenn ich von manueller Konfiguration (Standardeinstellung für vorhandene Tools) auf automatische Konfiguration umstelle, wirkt sich dies auf meine aktuellen Einstellungen aus? </p> </td> 
   <td colname="col2"> <p>Nein.  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wenn ich von manueller Bibliotheksverwaltung auf „Verwaltet von Adobe“ umstelle, wirkt sich dies auf meine aktuellen Einstellungen oder meinen Code aus? </p> </td> 
   <td colname="col2"> <p>Sämtlicher Benutzercode, den Sie angegeben haben, wird mit der <span class="keyword">AppMeasurement</span>-Basisbibliothek überschrieben. Sie müssen diesen Code in den neuen Abschnitt <span class="wintitle">Benutzerdefinierter Seiten-Code</span> am Ende der Tool-Konfiguration verschieben, damit der Code weiter ausgeführt wird. Auf diese Weise kann die <span class="keyword">AppMeasurement</span>-Bibliothek getrennt vom benutzerdefinierten Code des Benutzers verwaltet (und aktualisiert) werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wird der Überarbeitungsverlauf für das <span class="keyword">Adobe Analytics</span>-Tool beibehalten, wenn die neue Integration veröffentlicht wird? </p> </td> 
   <td colname="col2"> <p>Ja. </p> </td> 
  </tr> 
 </tbody> 
</table>

See [Add Adobe Analytics Tool](../../../implement/c-implement-with-dtm/c-aa-tool/analytics-dtm.md#concept_FBA6679A0B79490F8296437F11E5E4F8) for configuration information.

## Potenzielle Fallstricke {#section_201BF9E0EB7D4BC2B72A617543C2030B}

Es besteht ein geringes Risiko, dass die Integration Probleme bei der Datenerfassung verursachen kann, wenn Sie derzeit [!DNL Adobe Analytics] verwenden. Diese Probleme können nur auftreten, wenn Sie Ihre Bibliothek nach der Veröffentlichung der neuen Integration in der Produktion veröffentlichen. (Produktionscode bleibt bis zur Veröffentlichung intakt.)

Um diese Probleme zu vermeiden, stellen Sie Folgendes sicher:

* Die Report Suite-IDs sind im Tool richtig eingegeben.
* Die Report Suite-IDs im Tool stimmen mit den IDs im [!DNL AppMeasurement]-Code überein.
* Die Konfigurationsfelder für Währungscode, Zeichensatz, Tracking-Server und SSL-Tracking-Server sind korrekt mit den unterstützten Werten eingerichtet.
* Custom code is defined in [!DNL Library Management].

