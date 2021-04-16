---
title: Bruge eksterne kataloger til PunchOut e-indkøb
description: Dette emne forklarer, hvordan du kan bruge eksterne kataloger til at oprette og sende rekvisitioner.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a839f672454105871a101c190ee87d701e58db4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811056"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a><span data-ttu-id="3fcab-103">Bruge eksterne kataloger til PunchOut e-indkøb</span><span class="sxs-lookup"><span data-stu-id="3fcab-103">Use external catalogs for PunchOut e-procurement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fcab-104">Ved hjælp af eksterne kataloger til PunchOut-e-indkøb skal du ikke vedligeholde oplysninger om dine kreditorers produkter i dine egne masterdata.</span><span class="sxs-lookup"><span data-stu-id="3fcab-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="3fcab-105">I stedet konverteres indkøbsvognen på en leverandørs websted til rekvisitionslinjer, der har de korrekte produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="3fcab-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="3fcab-106">Du skal undgå at vedligeholde beskrivelserne af og priserne for dine leverandørers produkter i dine egne produktmasterdata.</span><span class="sxs-lookup"><span data-stu-id="3fcab-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="3fcab-107">Brug i stedet eksterne kataloger til PunchOut e-indkøb.</span><span class="sxs-lookup"><span data-stu-id="3fcab-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="3fcab-108">Derefter, når medarbejdere opretter indkøbsrekvisitioner, kan de "stemple ud" til en leverandørs eksterne katalogwebsted (med andre ord forlader de dit system og går til leverandørens websted).</span><span class="sxs-lookup"><span data-stu-id="3fcab-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="3fcab-109">De produkter, der føjes til indkøbsvognen på leverandørens websted, kan derefter konverteres til rekvisitionslinjer.</span><span class="sxs-lookup"><span data-stu-id="3fcab-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="3fcab-110">Derfor kan du få de korrekte produktoplysninger: produkt-id, navn, pris og så videre.</span><span class="sxs-lookup"><span data-stu-id="3fcab-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="3fcab-111">Hvis du vil bruge eksterne kataloger, skal en medarbejder oprette en rekvisition på siden **Mine indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="3fcab-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="3fcab-112">Den medarbejder, der opretter en rekvisition, kaldes klargøreren af rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="3fcab-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="3fcab-113">Som klargører kan du udføre følgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="3fcab-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="3fcab-114">Brug linjen **Eksterne kataloger** til at åbne en side, der indeholder alle eksterne kataloger, der er tilgængelige for den angivne anmoder, juridiske indkøbsenhed og modtagerdriftsenhed.</span><span class="sxs-lookup"><span data-stu-id="3fcab-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="3fcab-115">Alt efter dine rettigheder kan du ændre anmoderen, den juridiske indkøbsenhed og modtagerdriftsenheden.</span><span class="sxs-lookup"><span data-stu-id="3fcab-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="3fcab-116">En ændring i disse værdier kan ændre listen over eksterne kataloger, der er tilgængelige for en anmoder.</span><span class="sxs-lookup"><span data-stu-id="3fcab-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="3fcab-117">Eksterne kataloger, der er tilgængelige, afhænger af de aktuelle aktive indkøbspolitikker for den juridiske indkøbsenhed eller modtagerdriftsenheden.</span><span class="sxs-lookup"><span data-stu-id="3fcab-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="3fcab-118">Disse politikker kan tillade eller forhindre adgang til bestemte indkøbskategorier.</span><span class="sxs-lookup"><span data-stu-id="3fcab-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="3fcab-119">Listen over eksterne kataloger, der er knyttet til disse indkøbskategorier, kan derfor påvirkes.</span><span class="sxs-lookup"><span data-stu-id="3fcab-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="3fcab-120">Du kan finde flere oplysninger om politikker i [Oversigt over indkøbspolitikker](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="3fcab-120">For more information about policies, see [Purchasing policies overview](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="3fcab-121">For at finde eksterne kataloger til bestemte indkøbskategorier kan du indtaste tekst i søgefeltet til kataloger.</span><span class="sxs-lookup"><span data-stu-id="3fcab-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="3fcab-122">Hvis du vil tilføje produkter fra en leverandørs eksterne katalog på leverandørens websted, skal du klikke på det eksterne katalog.</span><span class="sxs-lookup"><span data-stu-id="3fcab-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="3fcab-123">Føj derefter produkter til indkøbsvognen, og check ud. Linjerne fra indkøbsvognen overføres til Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3fcab-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="3fcab-124">Hvis der er flere muligheder for indkøbskategorier, kan du vælge den korrekte indkøbskategori, før du tilføjer linjerne i rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="3fcab-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="3fcab-125">Når du har føjet linjer til en rekvisition, kan du tilføje flere linjer uden at bruge eksterne kataloger.</span><span class="sxs-lookup"><span data-stu-id="3fcab-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="3fcab-126">Alternativt kan du fortsætte med at bruge eksterne kataloger til at tilføje linjer.</span><span class="sxs-lookup"><span data-stu-id="3fcab-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="3fcab-127">Når indkøbsrekvisitionen er klar, kan du bruge handlingen **Arbejdsgang** > **Send** til at sende den til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="3fcab-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="3fcab-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3fcab-128">Additional resources</span></span>

- [<span data-ttu-id="3fcab-129">Konfigurere et eksternt katalog til PunchOut e-indkøb</span><span class="sxs-lookup"><span data-stu-id="3fcab-129">Set up an external catalog for PunchOut e-procurement</span></span>](set-up-external-catalog-for-punchout.md)
- [<span data-ttu-id="3fcab-130">Forbedringer af indkøbs-cXML</span><span class="sxs-lookup"><span data-stu-id="3fcab-130">Purchasing cXML enhancements</span></span>](purchasing-cxml-enhancements.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]