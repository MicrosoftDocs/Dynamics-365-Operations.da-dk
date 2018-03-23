---
title: Styring af produktkategorier
description: "I dette emne beskrives, hvordan markedsføringschefer kan bruge Retail-produktkategorier til at administrere relationer mellem detailprodukthierarki og oplysninger om frigivne produkter."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: da-dk
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Forbedret produkt- og kategoristyring

[!include[banner](./includes/banner.md)]

Dette emne beskriver en forbedret metode til styring af Retail-produktkategorier og produkter i Dynamics 365 for Retail. Disse forbedringer giver markedsføringschefer mulighed for at se en fælles struktur for produktegenskaber mellem produkthierarki i Retail og oplysninger om frigivne produkter.

Du kan få flere oplysninger om administration af Retail-produktkategorier ved at gå til **Detailproduktkategori** fra arbejdsområdet **Kategori og produktstyring** og notere den forbedrede struktur på siden **Detailproduktkategori**.

![Arbejdsområdet Kategori og produktstyring](media/LaunchRetailProductHierarchy.png)

I tidligere versioner var produktegenskaberne inddelt i **Grundlæggende produktegenskaber** og **Produktegenskaber i Retail**, baseret på området for deres anvendelse. **Egenskaber for detailprodukt** var *globale* med hensyn til deres anvendelsesområde, dvs. for en given **Egenskaber for detailprodukt** deles samme værdi på tværs af alle juridiske enheder. **Grundlæggende produktegenskaber** er *specifikke for juridisk enhed*. For en given **Grundlæggende produktegenskab** kan værdien med andre ord variere på tværs af juridiske enheder baseret på de enkelte forretningsbehov.

I den forbedrede struktur for detailproduktkategorien er produktegenskaber logisk adskilt baseret på deres anvendelse i en gruppe, for at afspejle detaljeformstrukturen i frigivne produkter.

![Gruppering af felter baseret på deres anvendelsesområde](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Du kan skifte mellem at administrere specifikke egenskaber for juridisk enhed på tværs af alle juridiske enheder og styre dem for en bestemt juridisk enhed. For at gøre det skal du vælge enten **Vis/Rediger for alle juridiske enheder** eller **Vis/Rediger for en bestemt juridisk enhed**.

![Skifte visning mellem en enkelt juridisk enhed og alle juridiske enheder](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Skifte visning mellem en enkelt juridisk enhed og alle juridiske enheder](media/ToggleToEditForAllLegalEntities.PNG)  

Sammenlignet med tidligere versioner kan en markedsføringschef også definere standardværdier i den nye Retail-produktkategoristruktur for et ekstra sæt produktegenskaber på et individuelt kategoriniveau. På tidspunktet for oprettelse af produktet nedarves disse standardproduktegenskabsværdier af et produkt baseret på deres tilknytning til en individuel kategori fra detailprodukthierarkiet. Disse nedarvede produktegenskaber kan også ændres for hvert produkt for at imødekomme individuelle virksomhedsbehov.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Vælg egenskaber til opdatering af produkter fra kategoriformularen i Retail 
 
Du kan bruge denne nye forbedrede struktur for produktegenskaber til at vælge, hvilke opdaterede produktegenskaber der skal anvendes på tilknyttede produkter. 

![Ny forbedret visning af Opdater produkter](media/NewUpdateProductsEnhancedView.PNG) 

Markedsføringschefer kan ændre disse nedarvede egenskaber for hvert produkt, for at imødekomme individuelle virksomhedsbehov.


