---
title: Genklassificer anlægsaktiver
description: Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cdcb9c337440b8fa9de2bdeb78d3b2d118e91ca
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138271"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="06089-103">Genklassificer anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="06089-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06089-104">Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe.</span><span class="sxs-lookup"><span data-stu-id="06089-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="06089-105">Når et anlægsaktiv genklassificeres:</span><span class="sxs-lookup"><span data-stu-id="06089-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="06089-106">Alle bøger til det eksisterende anlægsaktiv oprettes for det nye anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="06089-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="06089-107">Oplysninger, der var oprettet for det oprindelige anlægsaktiv, kopieres til det nye anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="06089-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="06089-108">Status for det oprindelige anlægsaktivs bøger er Lukket.</span><span class="sxs-lookup"><span data-stu-id="06089-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="06089-109">Det nye anlægsaktivs nye bøger indeholder datoen for genklassificeringen i feltet **Anskaffelsesdato**.</span><span class="sxs-lookup"><span data-stu-id="06089-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="06089-110">Datoen i feltet **Startdato for afskrivning** kopieres fra de oprindelige aktivoplysninger.</span><span class="sxs-lookup"><span data-stu-id="06089-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="06089-111">Hvis afskrivningen allerede er startet, vises datoen for genklassificeringen i feltet **Dato, hvor afskrivning sidst blev udført**.</span><span class="sxs-lookup"><span data-stu-id="06089-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="06089-112">De eksisterende anlægsaktivposteringer for det oprindelige anlægsaktiv annulleres og oprettes for det nye anlægsaktiv igen.</span><span class="sxs-lookup"><span data-stu-id="06089-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="06089-113">Benyt følgende fremgangsmåde for at genklassificere et anlægsaktiv:</span><span class="sxs-lookup"><span data-stu-id="06089-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="06089-114">Gå til **Anlægsaktiver > Periodiske opgaver > Genklassificering**.</span><span class="sxs-lookup"><span data-stu-id="06089-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="06089-115">I feltet **Anlægsaktivgruppe** skal du vælge den gruppe, som skal genklassificeres.</span><span class="sxs-lookup"><span data-stu-id="06089-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="06089-116">Vælg det anlægsaktiv, der skal genklassificeres, i feltet **Nummer på anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="06089-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="06089-117">Vælg en gruppe, som det nye anlægsaktiv skal overføre til, i feltet **Ny anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="06089-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="06089-118">Hvis den nye anlægsaktivgruppe er knyttet til en nummerserie, opdateres feltet **Nyt nummer på anlægsaktivet** med nummeret fra nummerserien for den nye anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="06089-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="06089-119">Ellers opdateres feltet **Nyt nummer på anlægsaktivet** med nummeret fra nummerserien, der er konfigureret på siden **Parametre for anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="06089-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="06089-120">Hvis der ikke er konfigureret en nummerserie på siden **Parametre for anlægsaktiver**, skal du angive et tal i feltet **Nyt nummer på anlægsaktivet**.</span><span class="sxs-lookup"><span data-stu-id="06089-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="06089-121">Indtast en dato i feltet **Dato for genklassificering**.</span><span class="sxs-lookup"><span data-stu-id="06089-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="06089-122">Indtast eller vælg en værdi i feltet **Bilagsserie**.</span><span class="sxs-lookup"><span data-stu-id="06089-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="06089-123">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="06089-123">Click **OK**.</span></span>
