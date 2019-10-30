---
description: Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert.
seo-description: Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert.
seo-title: Bereitstellen der Integration
title: Bereitstellen der Integration
uuid: 9c116ca8-4dbf-44eb-a832-574527ee88b7
translation-type: tm+mt
source-git-commit: a2c38c2cf3a2c1451e2c60e003ebe1fa9bfd145d

---


# Bereitstellen der Integration{#deploying-the-integration}

Die Bereitstellung dieser Integration ist ein einfacher Prozess, der die folgenden Aktionen erfordert.

## Ausführen des Adobe Integration Wizard{#completing-the-adobe-integration-wizard}

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

## Bereitstellen des Integrationscodes{#deploying-the-integration-code}

Nach Abschluss des Integrationsassistenten müssen Sie den Integrationscode für Ihren Adobe Analytics-Bereitstellungscode (s_code) bereitstellen.

> [!NOTE] Wenn Sie Adobe TagManager oder das dynamische Tag-Management zur Bereitstellung von Adobe Analytics verwendet haben, können Sie den Integrationscode einfach mit einem dieser Tools hinzufügen.

1. Rufen Sie die Registerkarte **[!UICONTROL Support]** auf und laden Sie die `integration code v2_0_1` Ressource im Bereich Ressourcen der Integration herunter und speichern Sie sie.

1. Nehmen Sie gegebenenfalls die erforderlichen Änderungen am Code vor. Weitere Informationen finden Sie unter Ändern des Integrationscodes (auf dieser Seite).
1. Schließen Sie das Integrate-Modul ein, wenn es nicht bereits in Ihrem Adobe Analytics-Bereitstellungscode vorhanden ist.
1. Stellen Sie den Code mit einer der folgenden Methoden bereit:

   * Verwenden Sie Adobe TagManager oder das dynamische Tag-Management, um den Code hinzuzufügen.
   * Sie können den Code auch an die Organisationsressource übermitteln, die für die Aktualisierung Ihres Adobe Analytics-Bereitstellungscodes zuständig ist.

>[!IMPORTANT]
>
>Testen Sie die Bereitstellung für diese Integration in einer Entwicklungs-/Staging-Umgebung, bevor Sie sie in einer Produktionsumgebung bereitstellen.

## Ändern des Integrationscodes{#modifying-the-integration-code}

In den meisten Fällen müssen Sie keine Änderungen am Integrationscode vornehmen, der vom Data Connector-Assistenten erstellt wird.

Wenn Sie jedoch Anpassungen vornehmen müssen, werden einige der Codeeinstellungen unten beschrieben.

<table id="table_5405A73CEFD44466B3C39559F4A037C9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Codeeinstellung </th> 
   <th colname="col2" class="entry"> Beschreibung </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> s.maxDelay </td> 
   <td colname="col2">Die maximale Anzahl von Millisekunden, die die Adobe Analytics-Bildanforderung auf die Demandbase-Daten wartet, bevor sie auf den Analytics-Erfassungsserver ausgelöst werden. <p>Hinweis:  Diese Einstellung gilt für alle Integrationen, die möglicherweise über das Integrate-Modul ausgeführt werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._Schlüssel </td> 
   <td colname="col2"> Ihr Demandbase-API-Schlüssel. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._apiURL </td> 
   <td colname="col2"> Die URL-Vorlage für die Demandbase-API. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._delim </td> 
   <td colname="col2"> Das Trennzeichen, das zum Trennen der Demandbase-Dimensionswerte verwendet wird, wenn sie an Adobe Analytics gesendet werden. Eine Änderung dieser Einstellung kann dazu führen, dass die standardmäßigen Classification-Regeln nicht korrekt funktionieren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._setTnt </td> 
   <td colname="col2">Wenn "true", versucht der Integrationscode, mithilfe einer ausgeblendeten mbox die Demandbase-Dimensionen als Profilparameter an Adobe Target zu senden. <p>Hinweis:  Hierfür muss der mbox.js-Code auf der Seite vorhanden sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._tntVarPrefix </td> 
   <td colname="col2"> Diese Zeichenfolge wird jedem Demandbase-Dimensionsnamen vorangestellt, bevor er an Adobe Target gesendet wird. Wenn diese Einstellung beispielsweise den Wert "db_"hat, wird die Dimension "industry"als "db_industry"an Adobe Target gesendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._dimensionArray </td> 
   <td colname="col2"> Die standardmäßigen Demandbase-Dimensionen, die an Adobe Analytics gesendet werden. Es wird empfohlen, diese Einstellung nicht zu ändern. Die Eigenschaft "max_size"ist die Anzahl der zulässigen Zeichen für die Dimension, bevor die Kürzung erfolgt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._dimensionArrayCustom </td> 
   <td colname="col2"> Die benutzerdefinierten Demandbase-Dimensionen, die an Adobe Analytics gesendet werden. Die Eigenschaft "max_size"ist die Anzahl der zulässigen Zeichen für die Dimension, bevor die Kürzung erfolgt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._cName </td> 
   <td colname="col2"> Der Name des Sitzungs-Cookies, mit dem der Status für die Demandbase-API-Kommunikation beibehalten wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._contextName </td> 
   <td colname="col2"> Der Name der contextData-Variablen, mit der die Standarddimensionen an Adobe Analytics gesendet werden. Es wird empfohlen, diese Einstellung nicht zu ändern. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> _db._contextNameCustom </td> 
   <td colname="col2"> Der Name der contextData-Variablen, mit der die benutzerdefinierten Dimensionen an Adobe Analytics gesendet werden. Es wird empfohlen, diese Einstellung nicht zu ändern. </td> 
  </tr> 
 </tbody> 
</table>

## Einbeziehen des Integrate-Moduls{#including-the-integrate-module}

Für den Integrationscode muss das Integrate-Modul in Ihrer Adobe Analytics-Bereitstellung vorhanden sein.

Wenn Sie das Integrate-Modul noch nicht im Rahmen Ihrer Bereitstellung installiert haben, führen Sie die folgenden Schritte aus, je nach der Art der Implementierung, die Sie haben.

### Für AppMeasurement v1.0+ {#section-f28d090bf2404cabaae34cd9c66fc575}

1. Dekomprimieren Sie die AppMeasurement-ZIP-Datei, die Sie von **[!UICONTROL Analytics]** &gt; **[!UICONTROL Admin]** &gt; **[!UICONTROL CodeManager]** heruntergeladen haben.

1. Öffnen Sie die Datei mit dem Namen [!DNL AppMeasurement_Module_Integrate.js].
1. Kopieren Sie den Inhalt dieser Datei und fügen Sie ihn in Ihre primäre [!DNL AppMeasurement.js] Datei ein.

   >[!NOTE]
   >
   >Fügen Sie sie direkt vor dem Kommentar DO NOT ALTER ANYTHING BELOW THIS LINE in der Datei ein.

### Für alten Code (H-Code) {#section-bba8ad8c715e4f97883e7de3269f681a}

1. Laden Sie das Integrate-Modul aus dem Bereich "Ressourcen"in der Data Connectors-Benutzeroberfläche herunter (unter der Registerkarte "Support").

   ![](assets/h_code.png)

1. Kopieren Sie den Inhalt dieser Datei und fügen Sie ihn in Ihre [!DNL s_code] Datei ein.

   >[!NOTE]
   >
   >Fügen Sie sie direkt vor dem Kommentar DO NOT ALTER ANYTHING BELOW THIS LINE in der Datei ein.

## Überprüfen der Integration{#verifying-the-integration}

Überprüfen Sie, ob die Integration erfolgreich Daten erfasst, indem Sie die Live-Verfolgung und -Berichterstellung überprüfen.

### Live-Verfolgung {#section-9c20e8ff6b404ae09387ee07d675c9e2}

Verwenden Sie das DigitalPulse Debugger-Tool, um zu überprüfen, ob Demandbase-Dimensionsdaten an Adobe Analytics gesendet werden. Laden Sie nach dem Löschen der Cookies eine Seite auf Ihrer Website neu, auf der der Integrationscode bereitgestellt wurde. Wenn Sie davon ausgehen, dass Ihre aktuelle IP einer von Demandbase anerkannten Organisation zugeordnet ist, sollten Sie die folgenden Ergebnisse sehen.

**Reports &amp; Analysen (früher SiteCatalyst) umfasst die beiden folgenden Kontextdatenvariablen:**

![](assets/debugger1.png)

****Target Mbox enthält die Parameter "Demandbase-Profil":
Dies wird nur angezeigt, wenn Target auf der Seite implementiert ist UND Sie diese Integration für Adobe Target konfiguriert haben - siehe Schritt 4 des Adobe-Integrationsassistenten.

![](assets/debugger2.png)

### Berichterstellung {#section-1792fe75dc3249d0ad063dfd87a89162}

Überprüfen Sie Ihre Demandbase-Berichte in Adobe Analytics mit dem Dashboard, das automatisch mit dem Adobe Integration-Assistenten erstellt wurde (Schritt 7).

Alternativ können Sie in der Menüstruktur von Adobe Analytics zur Demandbase-Berichterstellung navigieren - siehe Screenshots unten.

> [!NOTE] Diese Daten sollten innerhalb von 24-48 Stunden nach erfolgreicher Bereitstellung angezeigt werden.

![](assets/reporting1.png)

![](assets/reporting2.png)

### Häufig gestellte Fragen {#section-d926b160a2ef4f07b43ea1bc67ac2a0a}

**Was bedeutet "[n/a]"?**

Der Demandbase Data Connector gibt an, wenn ein Attribut "Nicht verfügbar"ist, indem dieser Standardwert festgelegt wird. Es gibt zwei gängige Szenarien, in denen die Standardeinstellung festgelegt ist:

* Demandbase erkennt, dass der Besucher von einer IP-Adresse stammt, die nicht zu einem Unternehmen gehört.
* Es wird ein Kontoüberwachungsattribut (beginnend mit "watch_list") verwendet, das Unternehmen befindet sich jedoch nicht in Ihrer Kontoüberwachungsliste.

**Warum wird "`[n/a]`"bei bestimmten Attributen häufiger angezeigt?**

Demandbase klassifiziert alle IP-Adressen und stellt die Attribute Zielgruppe und Zielgruppe_Segment bereit, auch wenn der Besucher nicht von einer Unternehmens-IP kommt. Wenn die Zielgruppe Werte wie "Residential", "Wireless"und "Hospitality"zurückgibt, sind die übrigen Attribute wahrscheinlich nicht verfügbar.

Manchmal ist die Zielgruppe eines Besuchers "SMB", aber andere Attribute zeigen "`[n/a]`". Demandbase kann also den Besucher als kleines Unternehmen klassifizieren, aber das vollständige Unternehmensprofil ist nicht verfügbar. Dies geschieht typischerweise bei den kleinsten Unternehmen, wenn mehr als ein kleines Unternehmen denselben Service Provider oder IP-Adressblock verwendet.

### Überlegungen zu Entwicklern {#section-d33fff55bc4b4db99f82dee418ef1bc2}

Wenn Sie den Standardwert in Ihrer Implementierung anpassen müssen, aktualisieren Sie die Zeile:

```
_db._nonOrgMatchLabel = "[n/a]";
```
