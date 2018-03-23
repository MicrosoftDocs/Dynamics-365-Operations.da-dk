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


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="7bcd5-103">Forbedret produkt- og kategoristyring</span><span class="sxs-lookup"><span data-stu-id="7bcd5-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="7bcd5-104">Dette emne beskriver en forbedret metode til styring af Retail-produktkategorier og produkter i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="7bcd5-105">Disse forbedringer giver markedsføringschefer mulighed for at se en fælles struktur for produktegenskaber mellem produkthierarki i Retail og oplysninger om frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="7bcd5-106">Du kan få flere oplysninger om administration af Retail-produktkategorier ved at gå til **Detailproduktkategori** fra arbejdsområdet **Kategori og produktstyring** og notere den forbedrede struktur på siden **Detailproduktkategori**.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Arbejdsområdet Kategori og produktstyring](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="7bcd5-108">I tidligere versioner var produktegenskaberne inddelt i **Grundlæggende produktegenskaber** og **Produktegenskaber i Retail**, baseret på området for deres anvendelse.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="7bcd5-109">**Egenskaber for detailprodukt** var *globale* med hensyn til deres anvendelsesområde, dvs. for en given **Egenskaber for detailprodukt** deles samme værdi på tværs af alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="7bcd5-110">**Grundlæggende produktegenskaber** er *specifikke for juridisk enhed*.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="7bcd5-111">For en given **Grundlæggende produktegenskab** kan værdien med andre ord variere på tværs af juridiske enheder baseret på de enkelte forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="7bcd5-112">I den forbedrede struktur for detailproduktkategorien er produktegenskaber logisk adskilt baseret på deres anvendelse i en gruppe, for at afspejle detaljeformstrukturen i frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Gruppering af felter baseret på deres anvendelsesområde](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="7bcd5-114">Du kan skifte mellem at administrere specifikke egenskaber for juridisk enhed på tværs af alle juridiske enheder og styre dem for en bestemt juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="7bcd5-115">For at gøre det skal du vælge enten **Vis/Rediger for alle juridiske enheder** eller **Vis/Rediger for en bestemt juridisk enhed**.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Skifte visning mellem en enkelt juridisk enhed og alle juridiske enheder](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Skifte visning mellem en enkelt juridisk enhed og alle juridiske enheder](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="7bcd5-118">Sammenlignet med tidligere versioner kan en markedsføringschef også definere standardværdier i den nye Retail-produktkategoristruktur for et ekstra sæt produktegenskaber på et individuelt kategoriniveau.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="7bcd5-119">På tidspunktet for oprettelse af produktet nedarves disse standardproduktegenskabsværdier af et produkt baseret på deres tilknytning til en individuel kategori fra detailprodukthierarkiet.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="7bcd5-120">Disse nedarvede produktegenskaber kan også ændres for hvert produkt for at imødekomme individuelle virksomhedsbehov.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="7bcd5-121">Vælg egenskaber til opdatering af produkter fra kategoriformularen i Retail</span><span class="sxs-lookup"><span data-stu-id="7bcd5-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="7bcd5-122">Du kan bruge denne nye forbedrede struktur for produktegenskaber til at vælge, hvilke opdaterede produktegenskaber der skal anvendes på tilknyttede produkter.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Ny forbedret visning af Opdater produkter](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="7bcd5-124">Markedsføringschefer kan ændre disse nedarvede egenskaber for hvert produkt, for at imødekomme individuelle virksomhedsbehov.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


