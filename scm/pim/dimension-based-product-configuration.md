---
title: Dimensionsbaseret produktkonfiguration
description: "Dimensionsbaseret produktkonfiguration repræsenterer en enkel løsning til at oprette mange produktvarianter fra en enkelt produktmaster og tilhørende stykliste."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7fbf69dc217a2f61ec3aeda952ff221491e9385a
ms.lasthandoff: 03/31/2017


---

# <a name="dimension-based-product-configuration"></a>Dimensionsbaseret produktkonfiguration

Dimensionsbaseret produktkonfiguration repræsenterer en enkel løsning til at oprette mange produktvarianter fra en enkelt produktmaster og tilhørende stykliste.

Dimensionsbaseret produktkonfiguration er en af de tre indbyggede produkt konfigurationsteknologier. De to andre teknologier er foruddefinerede varianter og begrænsningsbaseret konfiguration. Alle tre teknologier bruger en produktmaster som udgangspunkt og tillader brugeren at oprette mange produktvarianter for en produktmaster.

## <a name="key-concepts"></a>Nøglebegreber
Dimensionsbaseret produktkonfiguration er baseret på følgende nøglebegreber:

-   Produktmastere
-   Konfiguration af produktdimension
-   Variantgrupper
-   Stykliste
-   Konfigurationsrute
-   Variantregler

### <a name="product-masters"></a>Produktmastere

En produktmaster er udgangspunktet for enhver proces til produktkonfiguration. Til den dimensionsbaserede produktkonfiguration skal du bruge en produktmaster med denne bestemte konfigurationsteknologi og en produktdimensionsgruppe, der omfatter konfigurationens produktdimension.

### <a name="configuration-product-dimension"></a>Konfiguration af produktdimension

Konfigurationens produktdimension bruges til at identificere produktvarianter for en produktmaster med den dimensionsbaserede konfigurationsteknologi. Konfigurationens dimensionsværdi er angivet af brugeren og skal hjælpe med at identificere de enkelte produktvarianter.

### <a name="configuration-groups"></a>Variantgrupper

Variantgrupper er defineret i et centralt lager og kan bruges til alle dimensionsbaserede produktkonfigurationsmodeller. Variantgrupper er knyttet til de enkelte styklistelinjer og holder en gruppe af linjer sammen, der gensidigt udelukker hinanden. Det betyder, at kun én linje i en gruppe kan vælges til en enkelt produktvariant.

### <a name="bill-of-materials-bom"></a>Stykliste

Styklisten repræsenterer byggesten for en dimensionsbaseret produktkonfiguration. Den skal indeholde alle de forskellige produkter, der kan bruges i en produktvariant. Hver linje i styklisten kan henvise til en variantgruppe. Hvis en linje ikke refererer til en variantgruppe, medtages den i alle produktvarianter.

### <a name="configuration-route"></a>Konfigurationsrute

Variantruten bestemmer rækkefølgen af variantgrupper, da de vil blive vist for brugeren under processen til produktkonfiguration.

### <a name="configuration-rules"></a>Variantregler

Variantregler repræsenterer en mekanisme til at sikre, at et produkt, der er medtaget i en variantgruppe på en stykliste, gennemtvinger enten en medtagelse eller en udelukkelse af et produkt i en anden variantgruppe på samme stykliste.

## <a name="product-modeling-process"></a>Proces til produktmodel
Den naturlige sekvens til opbygning af en produktmodel for et dimensionsbaseret produkt, starter med at definere de relevante variantgrupper. Det er vigtigt at sikre, at alle produkter, der skal bruges i styklisten, er blevet frigivet til den virksomhed, som produktmodellen er bygget til. Med disse byggeklodser på plads, kan brugeren oprette Styklisten og tildele variantgrupper til alle relevante styklistelinjer. Når Styklisten er fuldført, kan du definere en variantrute for rækkefølgen af variantgrupper i den rigtige rækkefølge. \[titeltekst-id = "vedhæftet fil\_282671" Juster = "alignnone" bredde = "1187"\][![Dimensionsbaseret produkt modeling processen](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimensionsbaseret produkt modeling processen\[/billedtekst\] Hvis der er visse produkter fra forskellige variantgrupper, der enten skal eller bør ikke anvendes sammen, kan du oprette variantregler, der gennemtvinger disse produktrelationer. Når styklisten er blevet knyttet sammen med en dimensionsbaseret produktmaster via en styklisteversion, og begge er blevet godkendt og er aktiveret, kan du oprette produktkonfigurationer og angiv et navn for hver konfiguration. Konfigurationerne kan defineres, før der genereres posteringer, eller det kan gøres, når der opstår behov for en bestemt konfiguration.

### <a name="suggested-use"></a>Foreslået anvendelse

Den dimensionsbaserede konfigurationsteknologi er bedst anvendt til produkter med begrænset variation, og kombinationen af størrelse på standardproduktdimension, farve, typografi og konfiguration egner sig ikke til at identificere en bestemt produktvariant. Et eksempel kunne være cykler med stelhøjde, hjulstørrelse, bremsetyper og forskellige gear.

