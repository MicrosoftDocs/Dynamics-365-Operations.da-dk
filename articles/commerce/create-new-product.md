---
title: Oprette et nyt produkt
description: Dette emne beskriver, hvordan du opretter et nyt produkt i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 356bf91b2a946e7c0f5d5af9e2fe0b64342b856e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001958"
---
# <a name="create-a-new-product"></a>Oprette et nyt produkt


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter et nyt produkt i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et produkt defineres primært af produktnummer, navn og beskrivelse. Andre data er dog også nødvendige for at beskrive en vare eller tjenesteydelse:

## <a name="create-a-new-product"></a>Oprette et nyt produkt

1. Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Produkter efter kategori** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. På rullelisten **Produkttype** skal du vælge enten **Vare** eller **Tjeneste**.
1. På rullelisten **Produktundertype** skal du vælge enten **Produkt** (hvis produktet ikke skal have varianter) eller **Produktmaster** (hvis produktet skal have varianter).
1. Angiv et produktnummer i feltet **Produktnummer**, hvis det ikke allerede er udfyldt på forhånd.
1. Indtast et produktnavn i feltet **Produktnavn**.
1. Angiv et søgenavn i feltet **Søgenavn**.
1. Vælg en relevant kategori på rullelisten **Detailkategori**.
1. Hvis produktet er en pakke, skal du vælge **Ja** for **Produktpakke**.
1. Hvis produktundertypen er produktmaster, skal du angive **Produktdimensionsgruppe** for at medtage de understøttede varianter. Indstillingerne omfatter **Farve**, **Størrelse**, **Typografi** og **Konfiguration**. Det kan være nødvendigt at oprette flere produktdimensionsgrupper efter behov.
1. Vælg en relevant indstilling på rullelisten **Konfigurationsteknologi**.
1. Vælg **OK**.

Følgende billede viser et eksempel på tilføjelse af produkt.

![Oprette et produkt](media/create-new-product.png)

Når et produkt er tilføjet, kan der angives yderligere data for det, f.eks. **Produktbeskrivelse**, **Variantgrupper**, **Dimensionsgrupper**, **Produktattributter** og **Relaterede produkter**.

Følgende billede viser flere oplysninger om et produkt.

![Produktdetaljer](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Opret produktvarianter

Hvis produktundertypen er **Produktmaster**, skal der oprettes specifikke varianter. 

Følg disse trin for at oprette produktvarianter.

1. Vælg **Produktvarianter** i handlingsruden.
1. Hvis der er valgt variantgrupper i handlingsruden, skal du vælge **Forslag til varianter*.
1. Vælg de varianter, du vil understøtte for produktet.
1. Vælg **Opret**.

## <a name="release-a-product"></a>Frigive et produkt

Hvis du vil sælge et produkt, skal det først frigives til en juridisk enhed.

1. Vælg **Frigiv produkter** på produktsiden.

    ![Frigive produkt](media/create-new-product-3.png)

1. Vælg det produkt, der skal frigives, og vælg derefter **Næste**.

    ![Vælge produkt til frigivelse](media/create-new-product-4.png)

1. Vælg den række produktvarianter, der skal frigives, og vælg derefter **Næste**.

    ![Vælge varianter til frigivelse](media/create-new-product-5.png)

1. Vælg den juridiske enhed, og vælg derefter **Næste**.

    ![Vælg juridisk enhed](media/create-new-product-6.png)

1. Vælg **Udfør**.

    ![Udføre produktfrigivelse](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Konfigurere et frigivet produkt

Når et produkt er frigivet, kræver det en yderligere konfiguration, der omfatter tilføjelse af en pris til produktet.

1. Gå til **Moduler \> Retail og Commerce \> Produkter og kategorier \> Frigivne produkter efter kategori** i navigationsruden.
1. Vælg produktkategorinoden for det produkt, der blev frigivet, og vælg derefter produktet på produktlisten.
1. Vælg **Rediger** i handlingsruden.
1. I sektionen **Køb** skal du konfigurere de påkrævede egenskaber, herunder **Enhed**, **Pris** og **Antal**.
1. Vælg **Valider** i handlingsruden for at sikre, at der ikke rapporteres fejl for manglende felter.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på konfiguration af et frigivet produkt.

![Konfigurere frigivet produkt](media/create-new-product-8.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette juridiske enheder](channels-legal-entities.md)

[Oprette en variantgruppe](create-variant-group.md) 
