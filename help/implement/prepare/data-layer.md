---
title: Datenschicht erstellen
description: Erfahren Sie, was eine Datenschicht in Ihrer Analytics-Implementierung ist und wie sie zur Zuordnung von Variablen in Adobe Analytics verwendet werden kann.
translation-type: tm+mt
source-git-commit: ec6d8e6a3cef3a5fd38d91775c83ab95de47fd55
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 91%

---


# Datenschicht erstellen

Eine Datenschicht ist ein Framework von JavaScript-Objekten auf Ihrer Website, die alle in Ihrer Implementierung verwendeten Variablenwerte enthalten. Sie ermöglicht eine bessere Kontrolle und einfachere Wartung Ihrer Implementierung.

## Voraussetzungen

[Erstellen Sie ein Lösungsdesigndokument](solution-design.md): Für Ihr Unternehmen ist es wichtig, die Tracking-Anforderungen abzustimmen. Stellen Sie sicher, dass Sie mit einem Lösungsdesign-Dokument vorbereitet sind, bevor Sie sich an Entwicklungsteams in Ihrem Unternehmen wenden.

## Workflow

Die Implementierung von Adobe Analytics mit einer Datenschicht folgt normalerweise diesen Schritten:

1. **Arbeiten Sie mit Ihrem Website-Entwicklungs-Team zusammen, um eine Datenschicht zu implementieren**: Ihr Website-Entwicklungs-Team ist in erster Linie dafür verantwortlich, dass das Datenschichtobjekt mit den richtigen Werten gefüllt wird. Gehen Sie diese Seite mit Ihrem Website-Entwicklungs-Team durch, um sicherzustellen, dass die Erwartungen zwischen den Teams abgestimmt sind.

   >[!NOTE]
   >
   >Das Befolgen der von Adobe empfohlenen Datenschichtspezifikationen ist optional. Wenn Sie bereits über eine Datenschicht verfügen oder sich anderweitig gegen die Adobe-Spezifikationen entscheiden, stellen Sie sicher, dass Ihre Organisation sich an den zu befolgenden Spezifikationen orientiert.
1. **Validieren Sie Ihre Datenschicht mithilfe einer Browser-Konsole**: Sobald eine Datenschicht erstellt ist, können Sie mit der Entwicklerkonsole eines beliebigen Browsers überprüfen, ob sie funktioniert. Sie können die Entwicklerkonsole in den meisten Browsern mit der Taste `F12` öffnen. Ein Beispiel für einen Variablenwert wäre `digitalData.page.pageInfo.pageID`.
1. **Verwenden Sie Adobe Experience Platform Launch, um Datenschichtobjekte auf Launch-Datenelemente abzubilden**: Erstellen Sie Datenelemente in Launch und ordnen Sie sie den in Ihrer Datenschicht beschriebenen JavaScript-Attributen zu.
1. **Verwenden Sie die Adobe Analytics-Erweiterung in Launch, um Datenelemente auf Analytics-Variablen abzubilden**: Ordnen Sie nach Ihrem Lösungsentwurfsdokument jedes Datenelement der entsprechenden Analytics-Variablen zu.

## Spezifikationen

Adobe empfiehlt, sich an die von der [Customer Experience Digital Data Community Group](https://www.w3.org/community/custexpdata/) veröffentlichten Dokumentation [Customer Experience Digital Data Layer](https://www.w3.org/2013/12/ceddl-201312.pdf) zu halten. In den folgenden Abschnitten erfahren Sie, wie Datenschichtelemente mit Adobe Analytics interagieren.

Es wird empfohlen, das übergreifende Datenschichtobjekt `digitalData` zu verwenden. Im folgenden Beispiel wird ein etwas umfangreiches JSON-Objekt mit Beispielwerten aufgeführt:

```js
digitalData = {
    pageInstanceID: "Example page - production",
    page: {
        pageInfo: {
            pageID: "5093",
            pageName: "Example page",
            destinationURL: "https://example.com/index.html",
            referringURL: "https://example.com/referrer.html",
            sysEnv: "desktop",
            variant: "2",
            version: "1.14",
            breadCrumbs: ["Home","Example group","Example page"],
            author: "J Smith",
            issueDate: "Example date",
            effectiveDate: "Example date",
            expiryData: "Example date",
            language: "en-US",
            geoRegion: "US",
            industryCodes: "Example industry codes",
            publisher: "Example publisher"
        },
        category: {
            primaryCategory: "Example page category",
            subCategory: "Sub-category example"
        },
        attributes: {
            country: "US",
            language: "en-US"
        }
    },
    product: [{
        productInfo: {
            productID: "4859",
            productName: "Example product",
            description: "Example description",
            productURL: "https://example.com/product.html",
            productImage: "https://example.com/product_image.png",
            productThumbnail: "https://example.com/product_thumbnail.png",
            manufacturer: "Example manufacturer",
            quantity: 1,
            size: "Product size"
        },
        category: {
            primaryCategory: "Example product category",
            subCategory: "Example sub-category"
        }
    }],
    cart: {
        cartID: "934856",
        price: {
            basePrice: 200.00,
            voucherCode: "EXAMPLEVOUCHER1",
            voucherDiscount: 0.50,
            currency: "USD",
            taxRate: 0.20,
            shipping: 5.00,
            shippingMethod: "UPS",
            priceWithTax: 120,
            cartTotal: 125
        }
    },
    transaction: {
        transactionID: "694025",
        profile: {
            profileInfo: {
                profileID: "exampleprofile",
                userName: "exampleusername",
                email: "user@example.com"
            },
            address: {
                line1: "123 Vague Street",
                line2: "Apt 1",
                city: "Austin",
                stateProvince: "TX",
                postalCode: "78610",
                country: "USA"
            },
            shippingAddress: {
                line1: "123 Vague Street",
                line2: "Apt 1",
                city: "Austin",
                stateProvince: "TX",
                postalCode: "78610",
                country: "USA"
            }
        }
    },
    event: [{
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    }],
    component: [{
        componentInfo: {
            componentID: "4921",
            componentName: "Example component"
        },
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    }],
    user: [{
        segment: "Premium membership",
        profile: [{
            profileInfo: {
                profileID: "exampleprofile",
                userName: "exampleusername",
                email: "user@example.com",
                language: "en-US",
                returningStatus: "New"
            },
            social: {
                facebook: "examplefacebookid",
                twitter: "exampletwitterhandle"
            }
        }]
    }],
    privacy: {
        accessCategories: [{
            categoryName: "Default",
            domains: "adobedtm.com"
        }]
    },
    version: "1.0"
}
```

Details zu den einzelnen Objekten und Unterobjekten finden Sie im Bericht [Customer Experience Digital Data Layer](https://www.w3.org/2013/12/ceddl-201312.pdf). Nicht alle Websites verwenden alle Objekte. Wenn Sie z. B. eine News-Site hosten, ist es unwahrscheinlich, dass Sie für das Objekt-Array `digitalData.product` verwenden.

Datenschichten sind erweiterbar. Wenn Sie unternehmensspezifische Anforderungen haben, können Sie Objekte in Ihre Datenschicht aufnehmen, um diese Anforderungen zu erfüllen.

## Festlegen von Datenschichtwerten

Datenschichten werden normalerweise Server-seitig generiert und verweisen auf dieselben Objekte, die zum Erstellen des Website-Inhalts verwendet wurden. Richten Sie die Datenschicht der Website anhand der im [Lösungsdesigndokument](solution-design.md) Ihres Unternehmens festgelegten Tracking-Anforderungen ein.

## Nächste Schritte

[Ordnen Sie Datenschichtobjekte Datenelementen zu](../launch/layer-to-elements.md): Verwenden Sie die Datenschicht Ihrer Site in Adobe Experience Platform Launch.
