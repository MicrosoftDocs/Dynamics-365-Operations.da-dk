---
title: Foreslå anskaffelser af anlægsaktiver
description: I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839899"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="d631f-103">Foreslå anskaffelser af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="d631f-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d631f-104">I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.</span><span class="sxs-lookup"><span data-stu-id="d631f-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="d631f-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="d631f-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="d631f-106">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**.</span><span class="sxs-lookup"><span data-stu-id="d631f-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="d631f-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d631f-107">Select **New**.</span></span>
3. <span data-ttu-id="d631f-108">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d631f-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="d631f-109">Gå til handlingsruden, og vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="d631f-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="d631f-110">Vælg **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="d631f-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="d631f-111">Vælg **Anskaffelsesforslag**.</span><span class="sxs-lookup"><span data-stu-id="d631f-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="d631f-112">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="d631f-112">Select **Filter**.</span></span> <span data-ttu-id="d631f-113">Vælg **Nulstil** for at rydde tidligere værdier.</span><span class="sxs-lookup"><span data-stu-id="d631f-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="d631f-114">Vælg rækken **Anlægsaktivnummer**.</span><span class="sxs-lookup"><span data-stu-id="d631f-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="d631f-115">Indtast eller vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="d631f-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="d631f-116">Angiv de resterende kriterier for anlægsaktiverne, du vil hente med dette forslag.</span><span class="sxs-lookup"><span data-stu-id="d631f-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="d631f-117">Vælg **OK** to gange for at forlade ruden.</span><span class="sxs-lookup"><span data-stu-id="d631f-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="d631f-118">Bekræft de oprettede transaktionslinjer.</span><span class="sxs-lookup"><span data-stu-id="d631f-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="d631f-119">Kun anlægsaktiver med anskaffelsesdatoen og anskaffelsesprisen angivet i bogen medtages i anskaffelsesforslaget.</span><span class="sxs-lookup"><span data-stu-id="d631f-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="d631f-120">Vælg fanen **Bøger** på siden.</span><span class="sxs-lookup"><span data-stu-id="d631f-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="d631f-121">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="d631f-121">Select **Post**.</span></span>

