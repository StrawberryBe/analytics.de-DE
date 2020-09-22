---
description: Häufig gestellte Fragen zur automatischen Konfiguration der Adobe Analytics-Implementierung. Bei der automatischen Konfigurationsmethode wird der AppMeasurement-Code für Sie verwaltet.
keywords: Dynamic Tag Management;plug-ins;staging;effect on current settings;revision history;potential pitfalls;report suite id;currency code;tracking server;ssl tracking server;custom code;library management
solution: Experience Cloud,Analytics,Target
title: Häufig gestellte Fragen zum Adobe Analytics-Tool
uuid: 8fcef893-e305-4a95-a033-9066a56b09cd
translation-type: tm+mt
source-git-commit: a4542164031fc9f181dfdc471a1d54b5056b1223
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 100%

---


# Häufig gestellte Fragen zum Adobe Analytics-Tool

Häufig gestellte Fragen zur automatischen Konfiguration der Adobe Analytics-Implementierung. Bei der automatischen Konfigurationsmethode wird der [!DNL AppMeasurement]-Code für Sie verwaltet.

<table id="table_A50D00E2C47A473B92DA800FB08FE640"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Frage </th> 
   <th colname="col2" class="entry"> Antwort </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Wo werden die Plug-ins bei einer Adobe Analytics-Implementierung über DTM eingefügt? </p> </td> 
   <td colname="col2"> <p> Wenn Sie DTM zum manuellen Hosten von <code> s_code</code> verwenden, können Plug-ins im selben Editor wie der gehostete <code> s_code</code> hinzugefügt werden, ganz so wie bei einer typischen Adobe Analytics-Implementierung. </p> <p>Es ist jedoch auch eine Option, die Plug-ins im Editor im Abschnitt <span class="term">Seiten-Code anpassen</span> der Tool-Einstellungen zu platzieren. Beide Implementierungsmethoden sollten gleichermaßen effektiv sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wenn ich in der neuen Version des Tools Änderungen an der Konfiguration vornehme, kann ich sie im Staging testen, bevor ich sie in der Produktion veröffentliche? </p> </td> 
   <td colname="col2"> <p>Ja. </p> <p>Alle Änderungen können im Staging getestet werden, so wie Sie es normalerweise auch vor der Bereitstellung in einer Produktionsumgebung tun würden. Wenn Sie sich gegen eine Veröffentlichung entscheiden, weil Sie im Staging Probleme feststellen, funktioniert der Produktionscode weiterhin wie vor der Veröffentlichung der neuen Integration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Wenn ich von manueller Konfiguration (Standardeinstellung für vorhandene Tools) auf automatische Konfiguration umstelle, wirkt sich dies auf meine aktuellen Einstellungen aus? </p> </td> 
   <td colname="col2"> <p>Nein. </p> </td> 
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

Siehe [Adobe Analytics-Tool hinzufügen](/help/implement/other/dtm/c-aa-tool/analytics-dtm.md), um Konfigurationsinformationen zu erhalten

## Potenzielle Fallstricke {#section_201BF9E0EB7D4BC2B72A617543C2030B}

Es besteht ein geringes Risiko, dass die Integration Probleme bei der Datenerfassung verursachen kann, wenn Sie derzeit [!DNL Adobe Analytics] verwenden. Diese Probleme können nur auftreten, wenn Sie Ihre Bibliothek nach der Veröffentlichung der neuen Integration in der Produktion veröffentlichen. (Produktionscode bleibt bis zur Veröffentlichung intakt.)

Um diese Probleme zu vermeiden, stellen Sie Folgendes sicher:

* Die Report Suite-IDs sind im Tool richtig eingegeben.
* Die Report Suite-IDs im Tool stimmen mit den IDs im [!DNL AppMeasurement]-Code überein.
* Die Konfigurationsfelder für Währungscode, Zeichensatz, Tracking-Server und SSL-Tracking-Server sind korrekt mit den unterstützten Werten eingerichtet.
* Benutzerdefinierter Code wird in [!DNL Library Management] definiert.

