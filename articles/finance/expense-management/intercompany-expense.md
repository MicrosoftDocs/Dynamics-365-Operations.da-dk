---
title: Interne udgifter
description: En medarbejder, der er ansat af en juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation. I denne situation kan du bruge funktionaliteten til interne udgifter til at tildele medarbejderens udgifter til den juridiske enhed, som arbejdet blev udført for.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390878"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="b01a3-104">Interne udgifter</span><span class="sxs-lookup"><span data-stu-id="b01a3-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b01a3-105">En medarbejder, der er ansat af en juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation.</span><span class="sxs-lookup"><span data-stu-id="b01a3-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="b01a3-106">I denne situation kan du bruge funktionaliteten til interne udgifter til at tildele medarbejderens udgifter til den juridiske enhed, som arbejdet blev udført for.</span><span class="sxs-lookup"><span data-stu-id="b01a3-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="b01a3-107">Den juridiske enhed, der ansætter medarbejderen, kaldes den juridiske udlånsenhed.</span><span class="sxs-lookup"><span data-stu-id="b01a3-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="b01a3-108">Den juridiske enhed, som medarbejderen har udgifter for, kaldes den juridiske låneenhed.</span><span class="sxs-lookup"><span data-stu-id="b01a3-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="b01a3-109">Før en arbejder kan oprette og sende udgifter for arbejde, der udføres for en anden juridisk enhed i den juridiske udlånsenhed, skal du på siden **Parametre for udgiftsstyring** vælge indstillingen **Tillad interne udgiftslinjer**.</span><span class="sxs-lookup"><span data-stu-id="b01a3-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="b01a3-110">Skattepostering for interne udgifter</span><span class="sxs-lookup"><span data-stu-id="b01a3-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b01a3-111">Hvis du vil bruge momsgrupper, der er knyttet til den juridiske enhed for udlånet (kilden) i stedet for den juridiske enhed for lånet (destinationen) i udgiftsrapporten, skal du konfigurere den under momskonfigurationen i Finans.</span><span class="sxs-lookup"><span data-stu-id="b01a3-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="b01a3-112">Hvis Finans-parameteren **Juridisk enhed for bogføring af intern skat** er angivet til **Kilde**, og **Anvend momsregler** er angivet til **Nej**, vil momskombinationen for den juridiske enhed for udlån blive brugt.</span><span class="sxs-lookup"><span data-stu-id="b01a3-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="b01a3-113">Når den samme parameter er angivet til **Destination**, vil momskombinationen for den juridisk enhed for lån blive anvendt.</span><span class="sxs-lookup"><span data-stu-id="b01a3-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="b01a3-114">Når det gælder juridiske enheder i USA, hvor parameteren er indstillet til **Kilde**, skal feltet **Indgående moms** også konfigureres på den nye side **Finanskonteringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="b01a3-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="b01a3-115">Regnskabsprogrammet bruger oplysningerne fra dette felt til momsrelateret regnskabspost.</span><span class="sxs-lookup"><span data-stu-id="b01a3-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="b01a3-116">Funktionaliteten stemmer ikke overens med de udgiftslinjer, der er bogført med eller uden et projekt.</span><span class="sxs-lookup"><span data-stu-id="b01a3-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
