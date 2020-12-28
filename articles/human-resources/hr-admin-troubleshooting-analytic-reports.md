---
title: Fejlfinding af analyserapporter
description: I denne artikel beskrives det, hvad du skal gøre, hvis en kundes dataændringer ikke vises i nogen af kundens arbejdsområder.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417837"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="2993b-103">Fejlfinding af analyserapporter</span><span class="sxs-lookup"><span data-stu-id="2993b-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="2993b-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="2993b-104">**Issue**</span></span>

<span data-ttu-id="2993b-105">En kundes dataændringer vises ikke under **Analyse**-fanerne i nogen af kundens arbejdsområder.</span><span class="sxs-lookup"><span data-stu-id="2993b-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="2993b-106">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="2993b-106">**Cause**</span></span>

<span data-ttu-id="2993b-107">Som standard opdateres Microsoft Power BI-rapporter hver fjerde time inden for fristerne for batchjobbet Installer måling.</span><span class="sxs-lookup"><span data-stu-id="2993b-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="2993b-108">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="2993b-108">**Resolution**</span></span>

<span data-ttu-id="2993b-109">Dette problem er muligvis kun et spørgsmål om timing.</span><span class="sxs-lookup"><span data-stu-id="2993b-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="2993b-110">Følg disse trin for at starte batchjobbet og opdatere analysearbejdsområderne.</span><span class="sxs-lookup"><span data-stu-id="2993b-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="2993b-111">Åbn siden **Batchjob** på **Systemadministration \> Links \> Batchjob \> Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="2993b-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="2993b-112">Du kan også bruge funktionen Søg og skrive **Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="2993b-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="2993b-113">Find jobbet **Installer måling** på listen.</span><span class="sxs-lookup"><span data-stu-id="2993b-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="2993b-114">Vælg **Rediger** øverst på siden, og indstil den planlagte startdato/-klokkeslæt til en værdi, der opdaterer analysen, så den er tættere på det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="2993b-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchjob](media/batch-jobs.png)
