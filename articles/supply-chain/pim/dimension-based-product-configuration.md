---
title: Oversigt over dimensionsbaseret produktkonfiguration
description: Dimensionsbaseret produktkonfiguration repræsenterer en enkel løsning til at oprette mange produktvarianter fra en enkelt produktmaster og tilhørende stykliste.
author: t-benebo
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19821"
- intro-internal
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba11a561f320a7f4e787e4fe3f4e6f4fb88bbfb
ms.sourcegitcommit: ca73177dedf40df16860eaf88b1c701c61992028
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2022
ms.locfileid: "9754104"
---
# <a name="dimension-based-product-configuration-overview"></a>Oversigt over dimensionsbaseret produktkonfiguration

[!include [banner](../includes/banner.md)]

Dimensionsbaseret produktkonfiguration repræsenterer en enkel løsning til at oprette mange produktvarianter fra en enkelt produktmaster og tilhørende stykliste.

Dimensionsbaseret produktkonfiguration er en af de tre indbyggede teknologier til produktkonfiguration. De to andre teknologier er foruddefinerede varianter og begrænsningsbaseret konfiguration. Alle tre teknologier bruger en produktmaster som udgangspunkt og tillader brugeren at oprette mange produktvarianter for en produktmaster.

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
Den naturlige sekvens til opbygning af en produktmodel for et dimensionsbaseret produkt, starter med at definere de relevante variantgrupper. Det er vigtigt at sikre, at alle produkter, der skal bruges i styklisten, er blevet frigivet til den virksomhed, som produktmodellen er bygget til. Med disse byggeklodser på plads kan brugeren oprette styklisten og tildele variantgrupper til alle relevante styklistelinjer. Når styklisten er fuldført, kan du definere en variantrute for rækkefølgen af variantgrupper i den rigtige rækkefølge. [![Proces til dimensionsbaseret produktmodel.](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Hvis der er visse produkter fra forskellige variantgrupper, der enten skal eller ikke skal bruges sammen, kan du oprette variantregler, der gennemtvinger disse produktrelationer. Når styklisten er blevet knyttet sammen med en dimensionsbaseret produktmaster via en styklisteversion, og begge er blevet godkendt og er aktiveret, kan du oprette produktkonfigurationer og angiv et navn for hver konfiguration. Konfigurationerne kan defineres, før der genereres posteringer, eller det kan gøres, når der opstår behov for en bestemt konfiguration.

### <a name="suggested-use"></a>Foreslået anvendelse

Den dimensionsbaserede konfigurationsteknologi er bedst anvendt til produkter med begrænset variation, og kombinationen af størrelse på standardproduktdimension, farve, typografi og konfiguration egner sig ikke til at identificere en bestemt produktvariant. Et eksempel kunne være cykler med stelhøjde, hjulstørrelse, bremsetyper og forskellige gear.

### <a name="next-step"></a><a name="sequence"></a>Næste trin

De følgende otte opgaveguider vises i den rækkefølge, som du skal udføre dem. 

1.  [Oprette en dimensionsbaseret produktmaster](tasks/create-dimension-based-product-master.md)
2.  [Frigive en dimensionsbaseret produktmaster](tasks/release-dimension-based-product-master.md)
3.  [Fuldføre grundlæggende konfiguration af en frigivet produktmaster](tasks/complete-basic-setup-released-product-master.md)
4.  [Definere variantgrupper](tasks/define-configuration-groups.md)
5.  [Oprette en stykliste for en dimensionsbaseret produktmaster](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Definere konfigurationsruter](tasks/define-configuration-route.md)
7.  [Oprette konfigurationsregler](tasks/create-configuration-rules.md)
8.  [Oprette dimensionsbaserede konfigurationer](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]