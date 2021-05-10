---
description: Häufig gestellte Fragen zum Linktracking in Activity Map.
title: Linktracking – Häufig gestellte Fragen
uuid: 10172073-b98b-4950-8397-67a18b37b3b4
feature: Activity Map
role: Business Practitioner, Administrator
exl-id: b6ccdf91-98ce-413f-842d-c5423598ed49
translation-type: tm+mt
source-git-commit: 7ba73d75dde80571125c83efb3265441b8d3278a
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 53%

---

# Linktracking – Häufig gestellte Fragen

Häufig gestellte Fragen zum Linktracking in Activity Map.

>[!CAUTION]
>
>Beim Aktivieren von Activity Map-Tracking **erfassen Sie möglicherweise persönlich identifizierbare Informationen (PII)**. Diese Daten können alleine oder in Verbindung mit anderen Informationen dazu verwendet werden, eine Einzelperson zu identifizieren, zu kontaktieren oder zu lokalisieren oder eine Einzelperson im Kontext zu identifizieren.

Im Folgenden finden Sie einige Fälle, in denen PII-Daten möglicherweise mit dem Activity Map-Tracking gesammelt werden:

* `Mailto`-Links. Ein Mailto-Link ist ein HTML-Linktyp, der den standardmäßigen E-Mail-Client auf dem Computer für das Senden einer E-Mail aktiviert.
* `User ID`-Links, die in der Kopf-/Fußzeile einer Website angezeigt werden, nachdem sich der Benutzer angemeldet hat.
* Für Kreditinstitute wird möglicherweise die Kontonummer als ein Link angezeigt. Wenn darauf geklickt wird, wird der Linktext erfasst.
* Auf Websites für das Gesundheitswesen werden PII-Daten ebenfalls als Links angezeigt. Durch Klicken auf diese Links wird der Linktext erfasst. Dadurch werden die PII-Daten gesammelt.

## Wann findet die Linktracking statt?

Sobald ein Benutzer auf eine Seite klickt, identifiziert Activity Map den Link und die Region.

## Was wird standardmäßig verfolgt?

Wenn auf ein Element geklickt wird, durchläuft es mehrere Prüfungen, um zu bestimmen, ob es von AppMeasurement als Link behandelt wird. Die Prüfungen sind:

* Ist dies ein `A`- oder `AREA`-Tag mit einer `href`-Eigenschaft?
* Gibt es ein `onclick`-Attribut, das eine `s_objectID`-Variable festlegt?
* Ist dies ein `INPUT`-Tag oder eine `SUBMIT`-Schaltfläche mit einem Wert oder einem untergeordneten Text?
* Ist dies ein `INPUT`-Tag mit dem Typ `IMAGE` und einer `src`-Eigenschaft?
* Ist dies ein `BUTTON`?

Wenn die Antwort auf eine der vorangehenden Fragen Ja ist, wird dieses Element als Link verwendet und verfolgt.

>[!IMPORTANT]
>
>Schaltflächen-Tags mit dem Attribut type=&quot;button&quot; werden von AppMeasurement nicht als Links betrachtet. Erwägen Sie, type=&quot;button&quot; für die Schaltflächen-Tags zu entfernen und stattdessen role=&quot;button&quot; oder submit=&quot;button&quot; hinzuzufügen.

>[!IMPORTANT]
>
>Ein Verankerungs-Tag mit einem &quot;href&quot;, das Beginn mit &quot;#&quot;verwenden, wird von AppMeasurement als interner Speicherort für Zielgruppen und nicht als Link betrachtet (da Sie die Seite nicht verlassen). Standardmäßig verfolgt Activity Map diese internen Zielorte nicht. Es werden nur Links verfolgt, die den Benutzer zu einer neuen Seite führen.

## Wie verfolgt Activity Map andere visuelle HTML-Elemente?

a. Über die Funktion `s.tl()`.

Wenn der Klick über einen `s.tl()`-Aufruf erfolgte, erhält Activity Map auch dieses Klick-Ereignis und stellt fest, ob eine `linkName`-Zeichenfolgenvariable gefunden wurde. Während der Ausführung von `s.tl()` wird dieser linkName als Activity Map-Link-ID festgelegt. Das Element, auf das geklickt wurde, das den `s.tl()`-Aufruf ausgelöst hat, wird zur Bestimmung der Region verwendet. Beispiel: 

```
<img onclick="s.tl(true,'o','abc')" src="someimageurl.png"/>
```

b. Über die Variable `s_objectID`. Beispiel: 

    &quot;
    
    &lt;a>&lt;img>&lt;/a>
    
    &lt;a>Linktext hier&lt;/a>
    
    
    &quot;

>[!IMPORTANT]
>
>Bei Verwendung von `s_objectID` in Activity Map ist ein nachfolgender Semikolon (;) erforderlich.

## Können Sie mir einige Beispiele für Links nennen, die verfolgt werden?

### Beispiel 1

```
  <a hef="/home?lang=en>Home</a>
```

### Beispiel 2

```
 <input type="submit" value="Submit"/>
```

### Beispiel 3

```
  <input type="image" src="submit-button.png"/>
```

### Beispiel 4

```
    <p onclick="var s_objectID='custom link id';">
      <span class="title">Current Market Rates</span>
      <span class="subtitle">1.45USD</span>
    </p>
```

### Beispiel 5

```
    <div onclick="s.tl(true,'o','custom link id')">
      <span class="title">Current Market Rates</span>
      <span class="subtitle">1.45USD</span>
    </div>
```

## Können Sie mir einige Beispiele von Links nennen, die NICHT verfolgt werden?

1. Grund: Anker-Tag hat keine gültige `href`:
   `<a name="innerAnchor">Section header</a>`

1. Grund: Weder `s_ObjectID` noch `s.tl()` sind vorhanden:

   ```
   <p onclick="showPanel('market rates')">
     <span class="title">Current Market Rates</span>
     <span class="subtitle">1.45USD</span>
   </p>
   ```

1. Grund: Weder `s_ObjectID` noch `s.tl()` sind vorhanden:

   ``` 
   <input type="radio" onclick="changeState(this)" name="group1" value="A"/>
   <input type="radio" onclick="changeState(this)" name="group1" value="B"/>
   <input type="radio" onclick="changeState(this)" name="group1" value="C"/>
   
   ```  
   
1. Grund: Bei der Eigenschaft &quot;src&quot;fehlt ein Formulareingabeelement:

   `<input type="image"/>`
