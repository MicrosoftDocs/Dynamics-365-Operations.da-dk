---
title: Produktdimensioner
description: "Der er fire produktdimensioner - farve, konfiguration, størrelse og typografi. Du kan kombinere produktdimensioner i dimensionsgrupper og tildele dimensionsgrupper til produktmastere. Kombinationerne af produktdimensioner bestemmer, hvordan produktvarianter defineres."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8854ab94a71cc363bcd073d2df47bc01a243b6cd
ms.lasthandoff: 03/31/2017


---

# <a name="product-dimensions"></a>Produktdimensioner

Der er fire produktdimensioner - farve, konfiguration, størrelse og typografi. Du kan kombinere produktdimensioner i dimensionsgrupper og tildele dimensionsgrupper til produktmastere. Kombinationerne af produktdimensioner bestemmer, hvordan produktvarianter defineres.

Produktdimensioner er egenskaber, der identificerer en produktvariant. Du kan bruge kombinationer af produktdimensioner til at definere produktvarianter. Du skal definere mindst én produktdimension for en produktmaster for at oprette en produktvariant.
Produktvarianter
----------------

Produktvarianter kaldes også varer. En vare er et fysisk produkt, som ikke er det samme som en tjeneste. Du kan også definere en produktmaster med tjenestetypen. Ved hjælp af typen af service kan du angive produktvarianter, der omfatter tjenester. For eksempel kan du angive en produktmaster for konsulentbistand og produktvarianter for arbejde, der udføres af erfarne konsulenter og yngre konsulenter.

## <a name="product-dimensions"></a>Produktdimensioner
Følgende produktdimensioner for, der er tilgængelige: konfiguration, farve, størrelse og typografi. En produktvariant kan genereres baseret på dimensionsværdierne for produktet.

Produkt dimensioner værdier, f.eks. størrelse, farve og typografi kan oprettes på den **størrelse**, **farve** og **stil** sider, som kan åbnes fra følgende placeringer: **administration af produktoplysninger**&gt;**Setup**&gt;**Dimension og variant grupper**&gt;**farver/størrelser/typografier**. Produktets dimensionsværdier for dimensionen Konfiguration oprettes typisk ved hjælp af enten Variantstyring eller Dimensionsbaseret konfiguration. Produktdimensioner kan også oprettes og vedligeholdes på siden **Produktdimensioner**, der kan åbnes fra følgende steder:
-   Klik på **administration af produktoplysninger**&gt;**produkter**&gt;**produktmastere**. På den **handlingsruden**, skal du klikke på **produktdimensioner**.
-   Klik på **administration af produktoplysninger**&gt;**produkter**&gt;**alle produkter og produktmastere**. Vælg en produktmaster. På den **handlingsruden**, skal du klikke på **produktdimensioner**.
-   Klik på **administration af produktoplysninger**&gt;**frigivne produkter**. Vælg en produktmaster. På den **handlingsruden**, skal du klikke på **produkt**. Klik på **Produktdimensioner** i gruppen **Produktmaster**.

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




