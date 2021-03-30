---
title: Foreslå anskaffelser af anlægsaktiver
description: I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 426a5e42c1fc26958ab37eddd915334f8b0e19cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205022"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="410a1-103">Foreslå anskaffelser af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="410a1-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="410a1-104">I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.</span><span class="sxs-lookup"><span data-stu-id="410a1-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="410a1-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="410a1-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="410a1-106">Hvis du vil erhverve et anlægsaktiv via en forslagskladde, skal du først oprette anlægsaktivposten og derefter definere anskaffelsesprisen i anlægskartoteket.</span><span class="sxs-lookup"><span data-stu-id="410a1-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="410a1-107">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**.</span><span class="sxs-lookup"><span data-stu-id="410a1-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="410a1-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="410a1-108">Select **New**.</span></span>
3. <span data-ttu-id="410a1-109">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="410a1-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="410a1-110">Gå til handlingsruden, og vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="410a1-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="410a1-111">Vælg **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="410a1-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="410a1-112">Vælg **Anskaffelsesforslag**.</span><span class="sxs-lookup"><span data-stu-id="410a1-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="410a1-113">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="410a1-113">Select **Filter**.</span></span> <span data-ttu-id="410a1-114">Vælg **Nulstil** for at rydde tidligere værdier.</span><span class="sxs-lookup"><span data-stu-id="410a1-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="410a1-115">Vælg rækken **Anlægsaktivnummer**.</span><span class="sxs-lookup"><span data-stu-id="410a1-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="410a1-116">Indtast eller vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="410a1-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="410a1-117">Angiv de resterende kriterier for anlægsaktiverne, du vil hente med dette forslag.</span><span class="sxs-lookup"><span data-stu-id="410a1-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="410a1-118">Vælg **OK** to gange for at forlade ruden.</span><span class="sxs-lookup"><span data-stu-id="410a1-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="410a1-119">Bekræft de oprettede transaktionslinjer.</span><span class="sxs-lookup"><span data-stu-id="410a1-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="410a1-120">Kun anlægsaktiver med anskaffelsesdatoen og anskaffelsesprisen angivet i bogen medtages i anskaffelsesforslaget.</span><span class="sxs-lookup"><span data-stu-id="410a1-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="410a1-121">Vælg fanen **Bøger** på siden.</span><span class="sxs-lookup"><span data-stu-id="410a1-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="410a1-122">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="410a1-122">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]