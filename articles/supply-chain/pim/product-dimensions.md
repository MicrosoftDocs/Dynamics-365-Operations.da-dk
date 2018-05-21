---
title: Produktdimensioner
description: "Der er fire produktdimensioner – farve, konfiguration, størrelse og type. Du kan kombinere produktdimensioner i dimensionsgrupper og tildele dimensionsgrupper til produktmastere. Kombinationerne af produktdimensioner bestemmer, hvordan produktvarianter defineres."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 9cb4bded4b8d841c6d164e6b8ded2cb3fb4d0978
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---

# <a name="product-dimensions"></a>Produktdimensioner

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

Der er fire produktdimensioner – farve, konfiguration, størrelse og type. Du kan kombinere produktdimensioner i dimensionsgrupper og tildele dimensionsgrupper til produktmastere. Kombinationerne af produktdimensioner bestemmer, hvordan produktvarianter defineres.

Produktdimensioner er egenskaber, der identificerer en produktvariant. Du kan bruge kombinationer af produktdimensioner til at definere produktvarianter. Du skal definere mindst én produktdimension for en produktmaster for at oprette en produktvariant.
Produktvarianter
----------------

Produktvarianter kaldes også varer. En vare er et fysisk produkt, som ikke er det samme som en tjeneste. Det er også muligt at definere en produktmaster af typen Tjeneste. Ved hjælp af typen af service kan du angive produktvarianter, der omfatter tjenester. For eksempel kan du angive en produktmaster for konsulentbistand og produktvarianter for arbejde, der udføres af erfarne konsulenter og yngre konsulenter.

## <a name="product-dimensions"></a>Produktdimensioner
Følgende produktdimensioner er tilgængelige: konfiguration, farve, størrelse og type. En produktvariant kan genereres på basis af produktdimensionsværdierne.

Produktets dimensionsværdier, f.eks størrelse, farve og typografi, kan oprettes på siderne **Størrelse**, **Farve** og **Type**, som kan åbnes fra følgende placeringer: **Administration af produktoplysninger** &gt; **Konfiguration** &gt; **Dimensions- og variantgrupper** &gt; **Størrelser/Farver/Typer**. Produktets dimensionsværdier for dimensionen Konfiguration oprettes typisk ved hjælp af enten Variantstyring eller Dimensionsbaseret konfiguration. Produktdimensioner kan også oprettes og vedligeholdes på siden **Produktdimensioner**, der kan åbnes fra følgende steder:
-   Klik på **Administration af produktoplysninger** &gt; **Produkter** &gt; **Produktmastere**. Klik på **Produktdimensioner** i **handlingsruden**.
-   Klik på **Administration af produktoplysninger** &gt; **Produkter** &gt; **Alle produkter og produktmastere**. Vælg en produktmaster. Klik på **Produktdimensioner** i **handlingsruden**.
-   Klik på **Administration af produktoplysninger** &gt; **Frigivne produkter**. Vælg en produktmaster. Klik på **Produkt** i **handlingsruden**. Klik på **Produktdimensioner** i gruppen **Produktmaster**.

Antallet af varianter, der kan oprettes for en vare, er begrænset af antallet af mulige kombinationer af produktdimensioner.

| **Tip!**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Når du bruger et produkt på for eksempel en ordrelinje, skal du vælge produktdimensioner for at identificere den produktvariant, som du vil arbejde med. |

## <a name="example"></a>Eksempel
Et firma sælger denimbukser. Til varen cowboybukser bruges produktdimensionerne farve og størrelse. Cowboybukserne sælges i tre forskellige farver og seks forskellige størrelser. Farver: blå, sort, brun Størrelser: XS, S, M, L, XL, XXL ikke alle størrelser er tilgængelige i alle tre farver. Hvis alle kombinationer var tilgængelige, ville det skabe 18 forskellige typer af cowboybukser. I dette eksempel produceres kun følgende ni kombinationer af produktvarianter.

| Farve | Størrelse |
|-------|------|
| Blå  | XS   |
| Blå  | L    |
| Blå  | M    |
| Sort | M    |
| Sort | L    |
| Sort | XL   |
| Brun | L    |
| Brun | XL   |
| Brun | XXL  |






