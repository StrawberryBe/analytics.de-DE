---
description: Um die Integration zu aktivieren, müssen Sie den Konfigurationsassistenten in der Data Connectors-Schnittstelle ausfüllen.
seo-description: Um die Integration zu aktivieren, müssen Sie den Konfigurationsassistenten in der Data Connectors-Schnittstelle ausfüllen.
seo-title: Abschluss des Adobe-Integrationsassistenten
title: Abschluss des Adobe-Integrationsassistenten
uuid: 75260 b 92-a 6 f 5-44 b 6-b 3 ea-d 5945 fdd 1 ecb
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5e22d080398d74df29b1f849258e6500168cd5aa

---


# Completing the Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

Um die Integration zu aktivieren, müssen Sie den Konfigurationsassistenten in der Data Connectors-Schnittstelle ausfüllen.

1. Navigieren Sie zum Bereich Data Connectors (ehemals Genesis) innerhalb der Adobe Marketing Cloud.
1. Starten Sie den Integrationsassistenten von Demandbase 2.0.
1. Wählen Sie die gewünschte Report Suite aus und geben Sie einen Namen für die Integration ein.
1. Konfigurieren Sie die folgenden Elemente:

<table id="table_8D60DC7C48C144DC9934749E7F9F65FF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> E-Mail-Adresse </td> 
   <td colname="col2"> Die E-Mail-Adresse des primären Kontakts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beschreibung </td> 
   <td colname="col2"> (Optional) Beschreibung für diese Integration. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Demandbase-API-Schlüssel </td> 
   <td colname="col2"> Sie können dies von Ihrem Demandbase-Kundenbetreuer abrufen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Benutzerdefinierte Demandbase-Dimension # N </td> 
   <td colname="col2"> Dies sind die IDs für die optionalen 8 Dimensionen. Weitere Informationen finden Sie unter Demandbase-benutzerdefinierte Dimensionen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> An Adobe Target senden </td> 
   <td colname="col2">Wenn "true" , werden die Dimensionen der Demandbase auch mit einer ausgeblendeten mbox an Adobe Target gesendet. <p>Hinweis: Eine konfigurierte mbox. js-Datei muss auf der Webseite für die zu erfassenden Dimensionen implementiert werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Konfigurieren Sie die folgenden Variablenzuordnungselemente:

   | Element | Beschreibung |
   |---|---|
   | Demandbase-Dimensionen | Wählen Sie eine verfügbare evar-Variable aus Ihrer Report Suite. |
   | Demandbase benutzerdefinierte Dimensionen (optional) | Wählen Sie eine verfügbare evar-Variable aus Ihrer Report Suite. |

1. Konfigurieren Sie die Namen für die benutzerdefinierte Dimension (falls vorhanden).

   1. Wenn Sie in Schritt 4 benutzerdefinierte Dimensionen einbeziehen und die optionale evar in Schritt 5 zuordnen, müssen Sie Anzeigenamen für diese Dimensionen angeben. Wenn Sie beispielsweise "stock_ ticker" als benutzerdefinierte Dimension 1 eingeben, sollten Sie das Feld mit" Dimension 1" in "Aktienticker" ändern.
   1. Do **NOT** modify the names of the standard 8 dimensions (i.e. Demandbase SID, Company Name, Industry, etc.).

1. Markieren Sie das Kästchen, um das Dashboard zur Integration von Demandbase automatisch für Sie zu erstellen (empfohlen).
1. Review all configuration items and click **[!UICONTROL Activate Now]**.

