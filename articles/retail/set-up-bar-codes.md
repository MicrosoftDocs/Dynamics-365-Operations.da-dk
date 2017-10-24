---
title: Konfigurer stregkoder
description: I denne artikel beskrives, hvordan du bruger stregkoder i Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fdc56bf468babd4b0b0652d9791114af676c8470
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-bar-codes"></a><span data-ttu-id="fb529-103">Konfigurere stregkoder</span><span class="sxs-lookup"><span data-stu-id="fb529-103">Set up bar codes</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="fb529-104">I denne artikel beskrives, hvordan du bruger stregkoder i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="fb529-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="fb529-105">Du kan bruge stregkoder til at købe og sælge produkter, spore produktvarianter og konfigurere kunder og medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="fb529-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="fb529-106">Du kan også bruge stregkoder til at udstede og påtegne kuponer, gavekort og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="fb529-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="fb529-107">Du kan konfigurere detailprodukter, så de indeholder standardstregkoder eller brugerdefinerede, interne stregkoder.</span><span class="sxs-lookup"><span data-stu-id="fb529-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="fb529-108">Produkter kan have mere end en stregkode.</span><span class="sxs-lookup"><span data-stu-id="fb529-108">Products can have more than one bar code.</span></span> <span data-ttu-id="fb529-109">Et produkt kan f.eks. eventuelt have flere stregkoder, hvis det stammer fra forskellige producenter, eller hvis det har varianter, der er baseret på størrelse, typografi eller farve.</span><span class="sxs-lookup"><span data-stu-id="fb529-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="fb529-110">Stregkoder kan omfatte produktets vægt eller pris.</span><span class="sxs-lookup"><span data-stu-id="fb529-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="fb529-111">Stregkodemasker er skabeloner, der bruges til at oprette stregkoder.</span><span class="sxs-lookup"><span data-stu-id="fb529-111">Bar code masks are templates that are used to create bar codes.</span></span> <span data-ttu-id="fb529-112">**Bemærk:** Når du tildeler en entydig stregkode til hver variantkombination, kan du scanne stregkoden i kasseapparatet og lade programmet afgøre, hvilken variant af produktet der sælges.</span><span class="sxs-lookup"><span data-stu-id="fb529-112">**Note:** If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="fb529-113">Du kan også indsamle og få vist statistik over salg efter variant.</span><span class="sxs-lookup"><span data-stu-id="fb529-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="fb529-114">Hver størrelses-, farve- og typografigruppe kan tildeles et entydigt nummer, der identificerer gruppen i stregkoden.</span><span class="sxs-lookup"><span data-stu-id="fb529-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="fb529-115">Dynamics 365 for Retail bruger stregkodemasken til automatisk at generere stregkoder til alle variantkombinationer.</span><span class="sxs-lookup"><span data-stu-id="fb529-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="fb529-116">Denne funktionalitet kan være praktisk, hvis der er mange størrelser, farver og typografier, da antallet af kombinationer øges betydeligt, efterhånden som hver variantkode tilføjes.</span><span class="sxs-lookup"><span data-stu-id="fb529-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="fb529-117">Hvis denne funktionalitet ikke bruges, skal stregkoder tildeles manuelt til hver enkelt kombination, der repræsenterer en produktvariant.</span><span class="sxs-lookup"><span data-stu-id="fb529-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span> <span data-ttu-id="fb529-118">Du kan oprette stregkoder manuelt eller automatisk.</span><span class="sxs-lookup"><span data-stu-id="fb529-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="fb529-119">Udfør følgende opgaver i den rækkefølge, hvori de er angivet, for at oprette stregkoder.</span><span class="sxs-lookup"><span data-stu-id="fb529-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1.  <span data-ttu-id="fb529-120">[Opsætning af stregkodemasketegn](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="fb529-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2.  <span data-ttu-id="fb529-121">[Opsætning af stregkodemasker](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="fb529-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3.  <span data-ttu-id="fb529-122">Konfigurer stregkodeopsætninger.</span><span class="sxs-lookup"><span data-stu-id="fb529-122">Configure bar code setups.</span></span>
4.  <span data-ttu-id="fb529-123">Opret stregkoder til produkter.</span><span class="sxs-lookup"><span data-stu-id="fb529-123">Create bar codes for products.</span></span>


<a name="see-also"></a><span data-ttu-id="fb529-124">Se også</span><span class="sxs-lookup"><span data-stu-id="fb529-124">See also</span></span>
--------

[<span data-ttu-id="fb529-125">Opsætning af stregkodemasker</span><span class="sxs-lookup"><span data-stu-id="fb529-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)




