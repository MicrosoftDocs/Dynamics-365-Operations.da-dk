---
title: Lagerstedsordrer til sky- og kantskalaenheder
description: Dette emne indeholder oplysninger om lagerstedsordrefunktionaliteten, der bruges som en del af arbejdsbyrden for lagerstedsskalaenheden.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105698"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="88088-103">Lagerstedsordrer til sky- og kantskalaenheder</span><span class="sxs-lookup"><span data-stu-id="88088-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="88088-104">Ikke alle forretningsfunktioner understøttes fuldt ud i den offentlige prøveversion, når der anvendes skalaenhed for arbejdsbyrder.</span><span class="sxs-lookup"><span data-stu-id="88088-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="88088-105">Hvis du bruger skalaenheder, skal du sørge for kun at bruge de processer, som dette emne direkte beskriver som understøttede.</span><span class="sxs-lookup"><span data-stu-id="88088-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="88088-106">Hvad er lagerstedsordrer?</span><span class="sxs-lookup"><span data-stu-id="88088-106">What are warehouse orders?</span></span>

<span data-ttu-id="88088-107">*Lagerstedsordrer* er en ordretype, der er oprettet for at understøtte implementering af lagersteders hub og skalaenhed.</span><span class="sxs-lookup"><span data-stu-id="88088-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="88088-108">De giver dig mulighed for at modtage lager, når du kører en lagerstedsbelastning på en skalaenhed.</span><span class="sxs-lookup"><span data-stu-id="88088-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="88088-109">De bruges i øjeblikket kun i forbindelse med indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="88088-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="88088-110">Lagerstedsordrer bruges som en del af behandlingen af lokationsstyring, f.eks. når lagerstedsappen bruges til at registrere fysisk lagerbeholdning under behandlingen af en indgående indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="88088-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="88088-111">Lagerstedsordrer oprettes som en del af processen *Frigiv til lagersted*, der er tilgængelig for indkøbsordrer, som angiver et skalaenhedslagersted og varer, der er aktiveret til at bruge lokationsstyringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="88088-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88088-112">Lagerstedsordrer er kun tilgængelige i installationer, hvor der bruges [sky- og kantskalaenheder til arbejdsbyrder i lokationsstyring](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="88088-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="88088-113">Oprette en lagerstedsordre</span><span class="sxs-lookup"><span data-stu-id="88088-113">Create a warehouse order</span></span>

<span data-ttu-id="88088-114">Følg disse trin for at oprette en lagerstedsordre.</span><span class="sxs-lookup"><span data-stu-id="88088-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="88088-115">Log på forekomsten af Microsoft Dynamics 365 Supply Chain Management, der kører på hubben.</span><span class="sxs-lookup"><span data-stu-id="88088-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="88088-116">(Du skal starte *Frigiv til lagersted*-processen, mens du er logget på hubben).</span><span class="sxs-lookup"><span data-stu-id="88088-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="88088-117">Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="88088-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="88088-118">Vælg **Frigiv til lagersted** i gruppen **Handlinger** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="88088-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="88088-119">Hvis du vil se de tilknyttede ordrelinjer for lagerstedet, skal du åbne den relevante indkøbsordre, vælge en linje i sektionen **Indkøbsordrelinjer** og derefter vælge **Lagersted \> Ordrelinjer for lagersted**.</span><span class="sxs-lookup"><span data-stu-id="88088-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="88088-120">Du kan få vist alle linjerne ved at gå til **Lokationsstyring \> Forespørgsler og rapporter \> Ordrelinjer for lagersted**.</span><span class="sxs-lookup"><span data-stu-id="88088-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="88088-121">Annullere en lagerstedsordre</span><span class="sxs-lookup"><span data-stu-id="88088-121">Cancel a warehouse order</span></span>

<span data-ttu-id="88088-122">Som en del af processen *Frigiv til lagersted* er lagertransaktioner for indkøbsordrer kædet sammen med lagerstedsordrer og låst, så de ikke opdateres af hubben.</span><span class="sxs-lookup"><span data-stu-id="88088-122">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="88088-123">Hvis du ved en fejl har frigivet til lagerstedet, eller hvis du har en anden grund til at tilbageføre oprettelsen af ordrelinjer for lagerstedet, kan du anmode om at annullere lagerstedsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="88088-123">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="88088-124">Følg disse trin for at annullere en lagerstedsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="88088-124">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="88088-125">Log på den forekomst af Supply Chain Management, der kører på hubben.</span><span class="sxs-lookup"><span data-stu-id="88088-125">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="88088-126">Gå til **Lokationsstyring \> Forespørgsler og rapporter \> Ordrelinjer for lagersted**.</span><span class="sxs-lookup"><span data-stu-id="88088-126">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="88088-127">Vælg den relevante linje.</span><span class="sxs-lookup"><span data-stu-id="88088-127">Select the relevant line.</span></span>
1. <span data-ttu-id="88088-128">Vælg **Annuller lagerstedsordrelinjer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="88088-128">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="88088-129">Anmodningen om at annullere linjer afvises for linjer, der allerede afventer annullering, eller som behandles på et lagersted, hvor arbejdsbyrden køres i en skalaenhed.</span><span class="sxs-lookup"><span data-stu-id="88088-129">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="88088-130">Overvåge en lagerstedsordre</span><span class="sxs-lookup"><span data-stu-id="88088-130">Monitor a warehouse order</span></span>

<span data-ttu-id="88088-131">I visningen **Lagerstedsordrelinjer** kan du overvåge status for indgående modtagelse ved at gennemse værdierne i kolonnen **Resterende antal til modtagelse**.</span><span class="sxs-lookup"><span data-stu-id="88088-131">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="88088-132">Hvis du vil have vist detaljer, der er relateret til arbejde, der udføres ved hjælp af lagerstedsappen, skal du følge et af disse trin.</span><span class="sxs-lookup"><span data-stu-id="88088-132">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="88088-133">Gå til **Lokationsstyring \> Forespørgsler og rapporter \> Ordrelinjer for lagersted**, og brug filteret til at finde det, du leder efter.</span><span class="sxs-lookup"><span data-stu-id="88088-133">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="88088-134">Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**, og åbn den relevante indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="88088-134">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="88088-135">Vælg en eller flere linjer i sektionen **Indkøbsordrelinjer**, og vælg derefter **Lagersted \> Lagerstedstilgangsposter**.</span><span class="sxs-lookup"><span data-stu-id="88088-135">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>
