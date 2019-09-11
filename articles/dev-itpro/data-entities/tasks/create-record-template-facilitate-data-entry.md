---
title: Oprette en postskabelon for at lette dataindtastning
description: Dette emne viser, hvordan du opretter en postskabelon, så feltværdier, som bruges ofte, ikke behøver at angives eksplicit for hver ny post.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08ee7d0f0ce7e92eaa85137dcd2761bfd702eb8c
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866922"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="abec8-103">Oprette en postskabelon for at lette dataindtastning</span><span class="sxs-lookup"><span data-stu-id="abec8-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="abec8-104">Dette emne viser, hvordan du opretter en postskabelon, så feltværdier, som bruges ofte, ikke behøver at angives eksplicit for hver ny post.</span><span class="sxs-lookup"><span data-stu-id="abec8-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="abec8-105">I denne procedure skal oprette en ny post til nye bærbare computere, der skal føjes til dine anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="abec8-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="abec8-106">Denne procedure bruger eksempelfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="abec8-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="abec8-107">I navigationsruden skal du gå til **Moduler > Anlægsaktiver > Anlægsaktiver > Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="abec8-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="abec8-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="abec8-108">Select **New**.</span></span>
3. <span data-ttu-id="abec8-109">Skriv eller vælg en værdi i feltet **Anlægsaktivgruppe**.</span><span class="sxs-lookup"><span data-stu-id="abec8-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="abec8-110">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="abec8-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="abec8-111">Angiv f.eks. **Bærbar for potentiel kunde**.</span><span class="sxs-lookup"><span data-stu-id="abec8-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="abec8-112">Angiv en værdi i feltet **Søgenavn**.</span><span class="sxs-lookup"><span data-stu-id="abec8-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="abec8-113">Du kan f.eks. skrive **bærbar**.</span><span class="sxs-lookup"><span data-stu-id="abec8-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="abec8-114">Udvid sektionen **Tekniske oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="abec8-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="abec8-115">Skriv værdier i felterne **Fabrikat**, **Model** og **Modelår**.</span><span class="sxs-lookup"><span data-stu-id="abec8-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="abec8-116">Vælg **Indstillinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="abec8-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="abec8-117">Vælg **Postoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="abec8-117">Select **Record info**.</span></span>
10. <span data-ttu-id="abec8-118">Vælg **Brugerskabelon**.</span><span class="sxs-lookup"><span data-stu-id="abec8-118">Select **User template**.</span></span>
11. <span data-ttu-id="abec8-119">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="abec8-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="abec8-120">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="abec8-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="abec8-121">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="abec8-121">Select **OK**.</span></span>
14. <span data-ttu-id="abec8-122">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="abec8-122">Select **Close**.</span></span>

