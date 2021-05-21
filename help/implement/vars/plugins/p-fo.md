---
title: p_fo (Page First Only (nur einmal pro Seite))
description: Stellen Sie sicher, dass bestimmte Routinen nur einmal pro Seite ausgelöst werden.
exl-id: e82d77f9-2ea9-4b1b-b645-b12879c344ec
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '628'
ht-degree: 100%

---

# Adobe-Plug-in: p_fo (Page First Only (nur einmal pro Seite))

>[!IMPORTANT]
>
>Dieses Plug-in wird von Adobe Consulting bereitgestellt, damit Sie die Vorteile von Adobe Analytics besser nutzen können. Die Adobe-Kundenunterstützung bietet keine Unterstützung für dieses Plug-in, einschließlich Installation und Fehlerbehebung. Wenn Sie Hilfe mit diesem Plug-in benötigen, wenden Sie sich an den Kundenbetreuer Ihres Unternehmens. Sie können ein Treffen mit einem Berater zur Unterstützung arrangieren.

Das `p_fo`-Plug-in ist ein Dienstprogramm, das prüft, ob ein bestimmtes JavaScript-Objekt vorhanden ist. Wenn das Objekt nicht vorhanden ist, erstellt das Plug-in das Objekt und gibt `true` zurück. Wenn das JavaScript-Objekt bereits auf der Seite vorhanden ist, gibt es `false` zurück. Dieses Plug-in ist nützlich, um Code exakt einmal auf einer Seite auszuführen. Mehrere andere Plug-ins sind auf diesen Code angewiesen, um zu funktionieren. Dieses Plug-in ist nicht erforderlich, wenn Sie nicht daran interessiert sind, wie oft Code auf einer Seite ausgeführt wird, oder wenn Sie keine abhängigen Plug-ins verwenden.

## Installieren des Plug-ins mit der Adobe Experience Platform Launch-Erweiterung

Adobe bietet eine Erweiterung, mit der Sie die gängigsten Plug-ins verwenden können.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann auf die Schaltfläche [!UICONTROL Katalog].
1. Installieren und Veröffentlichen der Erweiterung [!UICONTROL Common Analytics Plugins].
1. Wenn Sie dies noch nicht getan haben, erstellen Sie eine Regel mit der Bezeichnung „Plug-ins initialisieren“ mit der folgenden Konfiguration:
   * Bedingung: Keine
   * Ereignis: Core – Bibliothek geladen (Seitenanfang)
1. Fügen Sie der obenstehenden Regel eine Aktion mit der folgenden Konfiguration hinzu:
   * Erweiterung: Common Analytics Plugins
   * Aktionstyp: p_fo initialisieren
1. Speichern und veröffentlichen Sie die Änderungen an der Regel.

## Installieren des Plug-ins mit dem benutzerdefinierten Code-Editor in Launch

Wenn Sie die Plug-in-Erweiterung nicht verwenden möchten, können Sie den Editor für benutzerdefinierten Code verwenden.

1. Melden Sie sich mit Ihren Adobe ID-Anmeldeinformationen bei [launch.adobe.com](https://launch.adobe.com) an.
1. Klicken Sie auf die gewünschte Eigenschaft.
1. Gehen Sie zur Registerkarte [!UICONTROL Erweiterungen] und klicken Sie dann unter der Erweiterung „Adobe Analytics“ auf die Schaltfläche [!UICONTROL Konfigurieren].
1. Erweitern Sie das Akkordeon [!UICONTROL Tracking mit benutzerdefiniertem Code konfigurieren], wodurch die Schaltfläche [!UICONTROL Editor öffnen] angezeigt wird.
1. Öffnen Sie den Editor für benutzerdefinierten Code und fügen Sie den unten angegebenen Plug-in-Code in das Bearbeitungsfenster ein.
1. Speichern und veröffentlichen Sie die Änderungen an der Analytics-Erweiterung.

## Installieren des Plug-ins mit AppMeasurement

Kopieren Sie den folgenden Code und fügen Sie ihn an beliebiger Stelle in der AppMeasurement Datei ein, nachdem das Analytics-Tracking-Objekt instanziiert wurde (unter Verwendung von [`s_gi`](../functions/s-gi.md)). Die Beibehaltung von Kommentaren und Versionsnummern des Codes in Ihrer Implementierung hilft Adobe bei der Fehlerbehebung potenzieller Probleme.

```js
/******************************************* BEGIN CODE TO DEPLOY *******************************************/
/* Adobe Consulting Plugin: p_fo (pageFirstOnly) v3.0 (Requires AppMeasurement) */
function p_fo(c){if("-v"===c)return{plugin:"p_fo",version:"3.0"};a:{if("undefined"!==typeof window.s_c_il){var a=0;for(var b;a<window.s_c_il.length;a++)if(b=window.s_c_il[a],b._c&&"s_c"===b._c){a=b;break a}}a=void 0}"undefined"!==typeof a&&(a.contextData.p_fo="3.0");window.__fo||(window.__fo={});if(window.__fo[c])return!1;window.__fo[c]={};return!0};
/******************************************** END CODE TO DEPLOY ********************************************/
```

## Verwenden des Plug-ins

Die `p_fo`-Methode verwendet die folgenden Argumente:

* **on** (erforderlich, Zeichenfolge): Der Name des JavaScript-Objekts, das vom Plug-in erzeugt wird, wenn das Objekt noch nicht auf der Seite vorhanden ist.

Wenn das Objekt noch nicht vorhanden ist, gibt diese Methode `true` zurück und erzeugt das Objekt. Wenn das Objekt bereits vorhanden ist, gibt diese Methode `false` zurück.

## Beispielaufrufe

### Beispiel 1

Der folgende Code prüft, ob das Objekt „myobject“ auf der Seite vorhanden ist.  Wenn das Objekt „myobject“ nicht vorhanden ist, erzeugt der Code das Objekt „myobject“ und gibt den Wert „true“ zurück.  Daher wird der Code innerhalb der bedingten Anweisung (z. B. „Console.log(&#39;hello&#39;);“) ausgeführt.

Wenn hingegen das Objekt „myobject“ bereits vorhanden ist, wenn p_fo aufgerufen wird, gibt die p_fo-Funktion den Wert „false“ zurück und die bedingte Anweisung wird daher als „false“ betrachtet.  In diesem Fall wird der Code innerhalb der bedingten Anweisung nicht ausgeführt.

```javascript
if(s.p_fo("myobject"))
{
  console.log("hello");
}
```

**HINWEIS:** Jedes Mal, wenn ein neues Seitenobjekt/DOM geladen wird (oder die aktuelle Seite erneut geladen wird), ist das im on-Argument angegebene Objekt nicht mehr vorhanden. Daher gibt das p_fo-Plug-in nach dem ersten Laden der Seite erneut „true“ zurück, wenn es ausgeführt wird.

## Versionsverlauf

### 3.0 (19. März 2021)

* Versionsnummer als Kontextdaten hinzugefügt.

### 2.0

* Zwischenversion (neu kompiliert, kleinere Code-Größe).
* Rückgabewerttyp von Integer (Ganzzahl) auf Boolean (Boolesch) geändert.

### 1.0

* Erste Version.
