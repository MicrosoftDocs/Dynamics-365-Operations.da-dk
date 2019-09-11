---
title: Konfigurere hovedkontokategorier
description: I dette emne beskrives, hvordan du konfigurerer hovedkontokategorier i Dynamics 365 for Finance and Operations.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d37deb0bda225abb111375d8a00ae22d9e0c4fe
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916062"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="591c2-103">Konfigurere hovedkontokategorier</span><span class="sxs-lookup"><span data-stu-id="591c2-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="591c2-104">I dette emne beskrives, hvordan du konfigurerer hovedkontokategorier i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="591c2-104">This topic explains how to set up main account categories in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="591c2-105">Hovedkontokategorier bruges til standardrapporter i økonomisk rapportering og Power BI.</span><span class="sxs-lookup"><span data-stu-id="591c2-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="591c2-106">Hovedkontokategorier, der oprettes som standard, kan omdøbes, men ikke slettes.</span><span class="sxs-lookup"><span data-stu-id="591c2-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="591c2-107">Yderligere kontokategorier kan oprettes og bruges til rapportering og analyse.</span><span class="sxs-lookup"><span data-stu-id="591c2-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="591c2-108">I dette emne demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="591c2-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="591c2-109">Opret en hovedkontokategori</span><span class="sxs-lookup"><span data-stu-id="591c2-109">Create a main account category</span></span>
1. <span data-ttu-id="591c2-110">Gå i navigationsruden **Moduler > Finans > Kontoplan > Konti > Hovedkontokategorier**.</span><span class="sxs-lookup"><span data-stu-id="591c2-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="591c2-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="591c2-111">Select **New**.</span></span>
3. <span data-ttu-id="591c2-112">Angiv et entydigt navn i feltet **Hovedkontokategori**.</span><span class="sxs-lookup"><span data-stu-id="591c2-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="591c2-113">Angiv en beskrivelse af hovedkontokategorien i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="591c2-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="591c2-114">I feltet **Hovedkontotype** skal du vælge den hovedkontotype, der skal knyttes til kategorien.</span><span class="sxs-lookup"><span data-stu-id="591c2-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="591c2-115">Link hovedkonti til kontokategori</span><span class="sxs-lookup"><span data-stu-id="591c2-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="591c2-116">Klik på **Sammenkæd hovedkonti**.</span><span class="sxs-lookup"><span data-stu-id="591c2-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="591c2-117">På listen skal du vælge de hovedkonti, der skal knyttes til hovedkontokategorien, ved at markere felterne i kolonnen **Tilknyttet**.</span><span class="sxs-lookup"><span data-stu-id="591c2-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="591c2-118">Hvis du tildeler hovedkonti til en hovedkontokategori, samles saldiene for kontiene, når denne kategori bruges til finansiel rapportering og analyse.</span><span class="sxs-lookup"><span data-stu-id="591c2-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="591c2-119">Markér eller fjern markeringen af indstillingen **Tilknyttet** for at vælge hovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="591c2-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="591c2-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="591c2-120">Select **OK**.</span></span>
5. <span data-ttu-id="591c2-121">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="591c2-121">Select **Yes**.</span></span>
