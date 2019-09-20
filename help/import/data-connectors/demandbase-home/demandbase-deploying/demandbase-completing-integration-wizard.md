---
description: Zum Aktivieren der Integration müssen Sie den Konfigurationsassistenten in der Data Connectors-Oberfläche ausführen.
seo-description: Zum Aktivieren der Integration müssen Sie den Konfigurationsassistenten in der Data Connectors-Oberfläche ausführen.
seo-title: Ausführen des Adobe Integration Wizard
title: Ausführen des Adobe Integration Wizard
uuid: 75260b92-a6f5-44b6-b3ea-d5945fdd1ecb
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e060fb745d611f37f28708b3fe103c1191aa483b

---


# Ausführen des Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

Zum Aktivieren der Integration müssen Sie den Konfigurationsassistenten in der Data Connectors-Oberfläche ausführen.

1. Navigieren Sie zum Bereich Data Connectors (früher Genesis) in der Adobe Experience Cloud.
1. Starten Sie den Integrationsassistenten von Demandbase 2.0.
1. Wählen Sie die gewünschte Report Suite und geben Sie einen Namen für die Integration ein.
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
   <td colname="col2"> Die E-Mail-Adresse des Hauptkontakts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Beschreibung </td> 
   <td colname="col2"> (Optional) Beschreibung für diese Integration. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Demandbase-API-Schlüssel </td> 
   <td colname="col2"> Sie können dies von Ihrem Demandbase-Vertreter abrufen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Benutzerdefinierte DemandBase-Dimension Nr. </td> 
   <td colname="col2"> Dies sind die IDs für die 8 optionalen Dimensionen. Weitere Informationen finden Sie unter Benutzerdefinierte Dimensionen der Demandbase. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> An Adobe Target senden </td> 
   <td colname="col2">Bei "true"werden die Demandbase-Dimensionen auch mit einer ausgeblendeten mbox an Adobe Target gesendet. <p>Hinweis:  Eine konfigurierte mbox.js-Datei muss auf der Webseite implementiert werden, damit Dimensionen erfasst werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Konfigurieren Sie die folgenden Elemente für die Variablenzuordnung:

   | Element | Beschreibung |
   |---|---|
   | Demandbase-Dimensionen | Wählen Sie eine verfügbare eVar-Variable aus Ihrer Report Suite. |
   | Benutzerdefinierte Dimensionen der Demandbase (optional) | Wählen Sie eine verfügbare eVar-Variable aus Ihrer Report Suite. |

1. Konfigurieren Sie die Namen für die benutzerdefinierte Dimension (falls zutreffend).

   1. Wenn Sie sich dafür entschieden haben, benutzerdefinierte Dimensionen in Schritt 4 einzubeziehen und die optionale eVar in Schritt 5 zugeordnet haben, müssen Sie benutzerfreundliche Namen für diese Dimensionen angeben. Wenn Sie beispielsweise "stock_ticker"als benutzerdefinierte Dimension 1 eingeben möchten, sollten Sie das Feld mit "Dimension 1"in "Stock Ticker"ändern.
   1. Ändern Sie **NICHT** die Namen der 8 Standarddimensionen (d.h. Demandbase SID, Firmenname, Branche usw.).

1. Markieren Sie das Kästchen, damit das Dashboard "Demandbase-Integration"automatisch für Sie erstellt wird (empfohlen).
1. Überprüfen Sie alle Konfigurationselemente und klicken Sie auf Jetzt **[!UICONTROL aktivieren]**.

