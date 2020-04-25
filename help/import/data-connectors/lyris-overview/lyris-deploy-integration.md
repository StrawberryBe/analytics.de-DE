---
description: Beschreibt den dreistufigen Bereitstellungsprozess.
title: Bereitstellen der Integration
uuid: a3c0ef21-ed9a-44d7-bdce-19b3bd5b8b80
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Bereitstellen der Integration {#deploying-the-integration}

Beschreibt den dreistufigen Bereitstellungsprozess.

Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert:

## Abschließen des Integrationsassistenten {#completing-the-integration-wizard}

Schritte zum Verwenden des Integrationsassistenten.

Zum Aktivieren der Integration müssen Sie den Lyris-Integrationsassistenten auf der Data Connectors-Oberfläche ausführen.

1. Navigieren Sie in der Adobe Experience Cloud zum Bereich „Data Connectors“ (früher Genesis).

   ![](assets/data_connectors.png)

1. Klicken Sie unter **[!UICONTROL Integration hinzufügen]** unter „Lyris HQ“ auf **[!UICONTROL Aktivieren]**.

   ![](assets/add_integration.png)

1. Wählen Sie unter **[!UICONTROL Allgemeine Einstellungen]** die gewünschte Report Suite aus. Geben Sie dann einen Namen für die Integration ein.
1. Tragen Sie unter **[!UICONTROL Benutzerdefinierte Werte]** alle Ihre Lyris-Kontoinformationen ein.

   ![](assets/general_settings.png)

1. Wählen Sie die entsprechenden reservierten eVars und Ereignisse aus den Dropdown-Menüs aus.

   ![](assets/variable_mapping.png)

1. Abgesehen von den 3 automatisierten Partnersegmenten können Sie Ihre eigenen Segmente unter **[!UICONTROL Ihre Segmente]** auswählen.
1. Bei dieser Integration kann es sein, dass Sie einige Datenpunkte in Ihr Lyris-Konto herunterladen müssen. Unter **[!UICONTROL Zugriffsanforderung]** können Sie Zugriff darauf gewähren.
1. Unter **[!UICONTROL Datenerfassung]** können Sie eine automatisierte oder manuelle Lösung (JavaScript-Plug-in) verwenden, um Abfragezeichenfolgenparameter aus der URL der Landingpage zu erfassen. Wenn Sie sich für eine automatisierte Lösung entscheiden, geben Sie Ihren Abfragezeichenfolgenparameter für die Nachrichten-ID und Empfänger-ID ein. Wenden Sie sich für ein JavaScript-Plug-in an Ihren Adobe-Berater.

   ![](assets/data_collection.png)

1. Sie können das Lyris Dashboard und die Lesezeichen automatisch für Sie generieren lassen.

   ![](assets/dashboard_generation.png)

1. Überprüfen Sie die Integrationszusammenfassung. Klicken Sie dann auf **[!UICONTROL Aktivieren]**.

## Konfiguration in Lyris EmailLabs {#configuration-within-the-lyris-emaillabs}

In diesen Schritten ist beschrieben, was nach Abschluss des Assistenten in Lyris konfiguriert werden soll.

1. Nach Abschluss des Integrationsassistenten müssen Sie mit dem Lyris Professional-Team zusammenarbeiten, um die Integration in Ihr Lyris HQ-Konto abzuschließen und Tests zu erleichtern.
1. Fügen Sie URL-Abfragezeichenfolgenparameter hinzu: Vergewissern Sie sich, dass die angehängte URL-Zeichenfolge ordnungsgemäß in die Organisationseinstellungen der Benutzeroberfläche eingegeben wurde. Diese sollte die Kampagnenebenen-ID (hq_m) und die ID der Empfängerebene (hq_v) enthalten.

   Beispiel einer Zeichenfolgen-ID:

   ```
   hq_lid=149&hq_m=96843&hq_l=23&hq_v=7703a51905
   ```

   >[!NOTE]
   >
   >Wenn Sie das native Analysetool von Lyris anwenden, markiert *Klick-Tracking* alle hinzugefügten erforderlichen Variablen.

## Überprüfen der Integration {#verifying-the-integration}

Schritte zum Überprüfen, ob die Lyris-/Adobe Analytics-Integration erfolgreich war.

Nach Abschluss sämtlicher Implementierungsschritte können Sie überprüfen, ob die Integration die Daten erfolgreich übertragen hat.

>[!NOTE] Es dauert ein paar Tage, bis der Datenaustausch beginnt. Wenden Sie sich nach der Aktivierung der Integration an Lyris.

1. Navigieren Sie zu Ihrer Lyris-Integration in „Data Connectors“. Auf der Registerkarte **[!UICONTROL Support]** > **[!UICONTROL Protokoll zu den Integrationsaktivitäten]** sollten Ereignisse wie **[!UICONTROL Metrikdaten wurden erfolgreich importiert]** bzw. **[!UICONTROL Classification-Daten wurden erfolgreich importiert]** angezeigt werden:

   ![](assets/integration_info.png)

1. Zeigen Sie jetzt Ihre Lyris-Nachrichtenberichte mit den entsprechenden Metriken an. Wählen Sie in der Adobe Experience Cloud **[!UICONTROL Reports &amp; Analysen]** aus.
1. Wählen Sie die gewünschte Report Suite aus.
1. Wählen Sie unter **[!UICONTROL Benutzerspezifische Konversionen]** die Option **[!UICONTROL Nachrichten-ID-Berichte]** und dann **[!UICONTROL Nachrichten-ID/Nachrichtenname]** aus.

## Abfragezeichenfolgen-Param-Plug-in-Code {#query-string-param-plug-in-code}

Zeigt den Lyris-Plug-in-Code zur Verwendung mit Adobe Analytics an.

>[!NOTE] Stellen Sie sicher, dass Sie die erforderlichen eVars im Admin Tool von Adobe Analytics reserviert haben, bevor Sie mit dem unten stehenden Code arbeiten. Sobald Sie wissen, welche eVars Sie reserviert haben, ersetzen Sie eVarN durch die entsprechende eVar. Zum Beispiel eVar10.

```
/* 
  * Plugin: getQueryParam 2.3 
  */ 
s.getQueryParam=new Function("p","d","u","" 
+"var s=this,v='',i,t;d=d?d:'';u=u?u:(s.pageURL?s.pageURL:s.wd.locati" 
+"on);if(u=='f')u=s.gtfs().location;while(p){i=p.indexOf(',');i=i<0?p" 
+".length:i;t=s.p_gpv(p.substring(0,i),u+'');if(t){t=t.indexOf('#')>-" 
+"1?t.substring(0,t.indexOf('#')):t;}if(t)v+=v?d+t:t;p=p.substring(i=" 
+"=p.length?i:i+1)}return v"); 
s.p_gpv=new Function("k","u","" 
+"var s=this,v='',i=u.indexOf('?'),q;if(k&&i>-1){q=u.substring(i+1);v" 
+"=s.pt(q,'&','p_gvf',k)}return v"); 
s.p_gvf=new Function("t","k","" 
+"if(t){var s=this,i=t.indexOf('='),p=i<0?t:t.substring(0,i),v=i<0?'T" 
+"rue':t.substring(i+1);if(p.toLowerCase()==k.toLowerCase())return s." 
+"epa(v)}return ''"); 
 
/*in the s_doPlugins function - Replace N with actual eVar number*/ 
s.eVarN=s.getQueryParam("<insert Lyris QS Param>");  
//places query param value from Message ID in eVarN variable s.eVarN=s.getQueryParam("<insert Lyris QS Param>");  
//places query param value from Recepient ID in eVarN variable 
```
