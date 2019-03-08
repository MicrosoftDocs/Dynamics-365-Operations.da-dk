---
title: Administrere produktkategorier og produkter i Retail
description: I dette emne beskrives, hvordan markedsføringschefer kan bruge detailproduktkategorier til at administrere relationer mellem detailprodukthierarkiet og oplysninger om frigivne produkter.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bcc5989edd9913fce414c0c24068f111d8c1aeb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "344679"
---
# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="87729-103">Administrere produktkategorier og produkter i Retail</span><span class="sxs-lookup"><span data-stu-id="87729-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="87729-104">Dette emne beskriver en forbedret metode til styring af Retail-produktkategorier og produkter i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="87729-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="87729-105">Disse forbedringer giver markedsføringschefer mulighed for at se en fælles struktur for produktegenskaber, der deles mellem produkthierarkiet i Retail og frigivne produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="87729-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="87729-106">Yderligere oplysninger om administration af detailproduktkategorier i arbejdsområdet **Kategori og produktstyring**, skal du vælge feltet **Detailprodukthierarki**.</span><span class="sxs-lookup"><span data-stu-id="87729-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="87729-107">Bemærk, at den forbedrede struktur på siden **Detailprodukthierarki** vises.</span><span class="sxs-lookup"><span data-stu-id="87729-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="87729-108">I tidligere versioner af Retail var produktegenskaberne inddelt i *Grundlæggende produktegenskaber* og *Egenskaber for detailprodukt*, baseret på omfanget af deres anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="87729-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="87729-109">Egenskaber for detailprodukt er *globale* i omfanget af deres anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="87729-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="87729-110">For en bestemt produktegenskab i Retail deles den samme værdi således på tværs af alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="87729-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="87729-111">I modsat fald er de grundlæggende produktegenskaber *specifikke for den juridiske enhed*.</span><span class="sxs-lookup"><span data-stu-id="87729-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="87729-112">For en given grundlæggende produktegenskab kan værdien med andre ord variere på tværs af juridiske enheder baseret på de enkelte forretningsbehov for hver juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="87729-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="87729-113">I den forbedrede struktur for produktkategorier i Retail er produktegenskaber logisk adskilte ud fra deres anvendelighed i en gruppe, så de afspejler detaljeformstrukturen formularstrukturen for de frigivne produktegenskaber.</span><span class="sxs-lookup"><span data-stu-id="87729-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Felterne grupperes ud fra egenskabernes anvendelighed](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="87729-115">Du kan skifte mellem at administrere egenskaber, der er specifikke for juridiske enheder på tværs af alle juridiske enheder og administrere dem for en bestemt juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="87729-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="87729-116">For at administrere egenskaber på tværs af alle juridiske enheder skal du vælge **Vis for alle juridiske enheder** (eller **Rediger for alle juridiske enheder**).</span><span class="sxs-lookup"><span data-stu-id="87729-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Få vist eller redigere for alle juridiske enheder](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="87729-118">For at administrere egenskaberne for en bestemt juridisk enhed, skal du vælge **Vis for en bestemt juridisk enhed** (eller **Rediger for en bestemt juridisk enhed**).</span><span class="sxs-lookup"><span data-stu-id="87729-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Få vist og redigere for en bestemt juridisk enhed](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="87729-120">Derudover kan en markedsføringschef i den forbedrede struktur for detailproduktkategorier nu også definere standardværdier for et ekstra sæt produktegenskaber for det enkelte kategoriniveau.</span><span class="sxs-lookup"><span data-stu-id="87729-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="87729-121">Når der derefter oprettes produkter, bliver de tildelt standardværdierne for deres produktegenskaber ud fra tilknytningen af disse egenskaber til en bestemt kategori i produkthierarkiet i Retail.</span><span class="sxs-lookup"><span data-stu-id="87729-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="87729-122">Disse nedarvede produktegenskaber kan også ændres for hvert produkt for at opfylde individuelle virksomhedsbehov.</span><span class="sxs-lookup"><span data-stu-id="87729-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="87729-123">Valg af egenskaber til opdatering af produkter på siden Detailprodukthierarki</span><span class="sxs-lookup"><span data-stu-id="87729-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="87729-124">Du kan bruge den nye forbedrede struktur for produktegenskaber til at vælge, hvilke opdaterede produktegenskaber der skal anvendes til de tilknyttede produkter.</span><span class="sxs-lookup"><span data-stu-id="87729-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="87729-125">På siden **Detailprodukthierarki** i handlingsruden skal du vælge **Kategori**. Vælg derefter **Opdater produkter** for at åbne dialogboksen **Opdater produkter**.</span><span class="sxs-lookup"><span data-stu-id="87729-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Dialogboksen Opdater produkter](media/NewUpdateProductsEnhancedView.PNG)
