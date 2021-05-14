---
title: Genklassificer anlægsaktiver
description: Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944705"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="5759f-103">Genklassificer anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="5759f-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5759f-104">Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe.</span><span class="sxs-lookup"><span data-stu-id="5759f-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="5759f-105">Når et anlægsaktiv genklassificeres:</span><span class="sxs-lookup"><span data-stu-id="5759f-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="5759f-106">Alle bøger til det eksisterende anlægsaktiv oprettes for det nye anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="5759f-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="5759f-107">Oplysninger, der var oprettet for det oprindelige anlægsaktiv, kopieres til det nye anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="5759f-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="5759f-108">Status for det oprindelige anlægsaktivs bøger er Lukket.</span><span class="sxs-lookup"><span data-stu-id="5759f-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="5759f-109">De nye anlægskartoteker indeholder datoen for genklassificeringen i feltet **Anskaffelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="5759f-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="5759f-110">Datoen i feltet **Startdato for afskrivning** kopieres fra de oprindelige aktivoplysninger.</span><span class="sxs-lookup"><span data-stu-id="5759f-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="5759f-111">Hvis afskrivningen allerede er startet, vises datoen for genklassificeringen i feltet **Dato, hvor afskrivning sidst blev udført**.</span><span class="sxs-lookup"><span data-stu-id="5759f-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="5759f-112">De eksisterende anlægsaktivposteringer for det oprindelige anlægsaktiv annulleres og oprettes for det nye anlægsaktiv igen.</span><span class="sxs-lookup"><span data-stu-id="5759f-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="5759f-113">Når et aktiv, der har en overførselstransaktion, er blevet omklassificeret, vil systemet vise en meddelelse i **Handlingscenteret** for at angive, at en overførselstransaktion ikke er fuldført under genklassificeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="5759f-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="5759f-114">Det er nødvendigt at fuldføre en overførselstransaktion for at flytte de eksisterende genklassificeringstransaktioner til de relevante økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="5759f-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="5759f-115">Under genklassificeringsprocessen kører systemet følgende handlinger for at genklassificere aktivsaldoen fra det oprindelige aktiv til det nye aktiv.</span><span class="sxs-lookup"><span data-stu-id="5759f-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="5759f-116">I genklassificeringsprocessen kopieres dataene fra det oprindelige anlægskartotek til det nye anlægskartotek.</span><span class="sxs-lookup"><span data-stu-id="5759f-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="5759f-117">Genklassificeringstransaktionen bruger oplysninger fra den oprindelige bogførte anskaffelse, som omfatter oplysninger om økonomiske dimensioner, der er medtaget i anskaffelsestransaktionen.</span><span class="sxs-lookup"><span data-stu-id="5759f-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="5759f-118">Samtidig tilbagefører genklassificeringsprocessen den oprindelige transaktion for aktivets anskaffelse og overførsel.</span><span class="sxs-lookup"><span data-stu-id="5759f-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="5759f-119">Følgende diagram og procedure viser et eksempel på genklassificeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="5759f-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="5759f-120">[![Diagram, der viser processen for genklassificering](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="5759f-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="5759f-121">Benyt følgende fremgangsmåde for at genklassificere et anlægsaktiv:</span><span class="sxs-lookup"><span data-stu-id="5759f-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="5759f-122">Gå til **Anlægsaktiver > Periodiske opgaver > Genklassificering**.</span><span class="sxs-lookup"><span data-stu-id="5759f-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="5759f-123">I feltet **Anlægsaktivgruppe** skal du vælge den gruppe, som skal genklassificeres.</span><span class="sxs-lookup"><span data-stu-id="5759f-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="5759f-124">Vælg det anlægsaktiv, der skal genklassificeres, i feltet **Nummer på anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="5759f-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="5759f-125">Vælg en gruppe, som det nye anlægsaktiv skal overføre til, i feltet **Ny anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="5759f-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="5759f-126">Hvis den nye anlægsaktivgruppe er knyttet til en nummerserie, opdateres feltet **Nyt nummer på anlægsaktivet** med nummeret fra nummerserien for den nye anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="5759f-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="5759f-127">Ellers opdateres feltet **Nyt nummer på anlægsaktivet** med nummeret fra nummerserien, der er konfigureret på siden **Parametre for anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="5759f-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="5759f-128">Hvis der ikke er konfigureret en nummerserie på siden **Parametre for anlægsaktiver**, skal du angive et tal i feltet **Nyt nummer på anlægsaktivet**.</span><span class="sxs-lookup"><span data-stu-id="5759f-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="5759f-129">Indtast en dato i feltet **Dato for genklassificering**.</span><span class="sxs-lookup"><span data-stu-id="5759f-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="5759f-130">Indtast eller vælg en værdi i feltet **Bilagsserie**.</span><span class="sxs-lookup"><span data-stu-id="5759f-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="5759f-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5759f-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
