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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176948"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="8ce90-103">Foreslå anskaffelser af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="8ce90-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ce90-104">I dette emne beskrives, hvordan du henter et anlægsaktiv ved hjælp af anskaffelsesforslaget i Anlægsaktivkladden.</span><span class="sxs-lookup"><span data-stu-id="8ce90-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="8ce90-105">Den bruger rollen Revisor og demodata for den juridiske enhed USMF.</span><span class="sxs-lookup"><span data-stu-id="8ce90-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="8ce90-106">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Kladdeposteringer > Anlægsaktivkladde**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="8ce90-107">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-107">Select **New**.</span></span>
3. <span data-ttu-id="8ce90-108">Indtast eller vælg en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="8ce90-109">Gå til handlingsruden, og vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="8ce90-110">Vælg **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="8ce90-111">Vælg **Anskaffelsesforslag**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="8ce90-112">Vælg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-112">Select **Filter**.</span></span> <span data-ttu-id="8ce90-113">Vælg **Nulstil** for at rydde tidligere værdier.</span><span class="sxs-lookup"><span data-stu-id="8ce90-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="8ce90-114">Vælg rækken **Anlægsaktivnummer**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="8ce90-115">Indtast eller vælg en værdi i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="8ce90-116">Angiv de resterende kriterier for anlægsaktiverne, du vil hente med dette forslag.</span><span class="sxs-lookup"><span data-stu-id="8ce90-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="8ce90-117">Vælg **OK** to gange for at forlade ruden.</span><span class="sxs-lookup"><span data-stu-id="8ce90-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="8ce90-118">Bekræft de oprettede transaktionslinjer.</span><span class="sxs-lookup"><span data-stu-id="8ce90-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="8ce90-119">Kun anlægsaktiver med anskaffelsesdatoen og anskaffelsesprisen angivet i bogen medtages i anskaffelsesforslaget.</span><span class="sxs-lookup"><span data-stu-id="8ce90-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="8ce90-120">Vælg fanen **Bøger** på siden.</span><span class="sxs-lookup"><span data-stu-id="8ce90-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="8ce90-121">Vælg **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="8ce90-121">Select **Post**.</span></span>

