---
title: Gebyrer for uoverensstemmelsesoperationer
description: Dette emne beskriver, hvordan du opretter kvalitetsgebyrer, der kan bruges sammen med operationer for en uoverensstemmelse.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956592"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="4e647-103">Gebyrer for uoverensstemmelsesoperationer</span><span class="sxs-lookup"><span data-stu-id="4e647-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e647-104">Dette emne beskriver, hvordan du opretter kvalitetsgebyrer, der kan bruges sammen med operationer for en uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="4e647-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="4e647-105">Du kan bruge siden **Kvalitetsgebyrer** til at definere de typer gebyrer, der kan tillægges operationer for en uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="4e647-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="4e647-106">Gebyrer giver dig mulighed for at spore oplysninger om gebyrer eller gebyrer, som du skylder en kunde for uoverensstemmende produkter, eller som en kreditor skylder dig for uoverensstemmende produkter, du har modtaget.</span><span class="sxs-lookup"><span data-stu-id="4e647-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="4e647-107">Du kan også bruge gebyrer til at spore omkostninger, der kræves af eksterne leverandører eller tjenester for at udføre en operation.</span><span class="sxs-lookup"><span data-stu-id="4e647-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="4e647-108">Eksempler på kvalitetsgebyrer</span><span class="sxs-lookup"><span data-stu-id="4e647-108">Examples of quality charges</span></span>

<span data-ttu-id="4e647-109">Du arbejder i en produktionsvirksomhed.</span><span class="sxs-lookup"><span data-stu-id="4e647-109">You work for a manufacturing company.</span></span> <span data-ttu-id="4e647-110">Din virksomhed har kontrakter med flere leverandører.</span><span class="sxs-lookup"><span data-stu-id="4e647-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="4e647-111">Disse kontrakter skitserer standarderne for rettidig levering, skader og produktkvalitet for varer.</span><span class="sxs-lookup"><span data-stu-id="4e647-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="4e647-112">På samme måde har flere kunder aftaler med virksomheden om returneringer, skader og produktkvalitet.</span><span class="sxs-lookup"><span data-stu-id="4e647-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="4e647-113">Der defineres en gebyrstruktur for hvert forhold, og den angives i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="4e647-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="4e647-114">Du kan konfigurere kvalitetsgebyrer for at skitsere forskellige gebyrtyper som f.eks. *Skader*, *Forsinket levering* og *Kvalitet*.</span><span class="sxs-lookup"><span data-stu-id="4e647-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="4e647-115">Når du derefter opretter en uoverensstemmelse, tilføjer du en eller flere operationer.</span><span class="sxs-lookup"><span data-stu-id="4e647-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="4e647-116">For hver operation skal du vælge **Gebyrer** for at definere detaljerne om gebyrerne.</span><span class="sxs-lookup"><span data-stu-id="4e647-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="4e647-117">Oprette et kvalitetsgebyr</span><span class="sxs-lookup"><span data-stu-id="4e647-117">Create a quality charge</span></span>

1. <span data-ttu-id="4e647-118">Gå til **Lagerstyring \> Opsætning \> Kvalitetsstyring \> Kvalitetsgebyrer**.</span><span class="sxs-lookup"><span data-stu-id="4e647-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="4e647-119">Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret.</span><span class="sxs-lookup"><span data-stu-id="4e647-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="4e647-120">Angiv følgende felter til den nye række:</span><span class="sxs-lookup"><span data-stu-id="4e647-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="4e647-121">**Gebyrkode** – Angiv et entydigt id eller navn for kvalitetsgebyret.</span><span class="sxs-lookup"><span data-stu-id="4e647-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="4e647-122">**Beskrivelse** – Indtast en detaljeret beskrivelse af kvalitetsgebyret.</span><span class="sxs-lookup"><span data-stu-id="4e647-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="4e647-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4e647-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="4e647-124">Føje et kvalitetsgebyr til en operation for en uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="4e647-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="4e647-125">Yderligere oplysninger om, hvordan du føjer operationer til en uoverensstemmelse og lægger gebyrer på dem, finder du i [Operationer for uoverensstemmelser](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="4e647-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e647-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="4e647-126">Additional resources</span></span>

- [<span data-ttu-id="4e647-127">Oversigt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="4e647-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="4e647-128">Aktivere styring af kvalitet og uoverensstemmelse</span><span class="sxs-lookup"><span data-stu-id="4e647-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="4e647-129">Arbejdere, der er ansvarlige for godkendelse af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="4e647-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="4e647-130">Karantænezoner for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="4e647-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="4e647-131">Diagnosticeringstyper for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="4e647-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="4e647-132">Kvalitetsgebyrer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="4e647-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="4e647-133">Operationer for uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="4e647-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="4e647-134">Kvalitetsstyring for lagerstedsprocesser.</span><span class="sxs-lookup"><span data-stu-id="4e647-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
