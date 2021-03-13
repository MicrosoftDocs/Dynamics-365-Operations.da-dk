---
title: Fejlfinding af analyserapporter
description: I denne artikel beskrives det, hvad du skal gøre, hvis en kundes dataændringer ikke vises i nogen af kundens arbejdsområder.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111932"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="ae8cd-103">Fejlfinding af analyserapporter</span><span class="sxs-lookup"><span data-stu-id="ae8cd-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="ae8cd-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="ae8cd-104">**Issue**</span></span>

<span data-ttu-id="ae8cd-105">En kundes dataændringer vises ikke under **Analyse**-fanerne i nogen af kundens arbejdsområder.</span><span class="sxs-lookup"><span data-stu-id="ae8cd-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="ae8cd-106">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="ae8cd-106">**Cause**</span></span>

<span data-ttu-id="ae8cd-107">Som standard opdateres Microsoft Power BI-rapporter hver fjerde time inden for fristerne for batchjobbet Installer måling.</span><span class="sxs-lookup"><span data-stu-id="ae8cd-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="ae8cd-108">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="ae8cd-108">**Resolution**</span></span>

<span data-ttu-id="ae8cd-109">Dette problem er muligvis kun et spørgsmål om timing.</span><span class="sxs-lookup"><span data-stu-id="ae8cd-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="ae8cd-110">Følg disse trin for at starte batchjobbet og opdatere analysearbejdsområderne.</span><span class="sxs-lookup"><span data-stu-id="ae8cd-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="ae8cd-111">Åbn siden **Batchjob** på **Systemadministration \> Links \> Batchjob \> Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="ae8cd-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="ae8cd-112">Du kan også bruge funktionen Søg og skrive **Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="ae8cd-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="ae8cd-113">Find jobbet **Installer måling** på listen.</span><span class="sxs-lookup"><span data-stu-id="ae8cd-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="ae8cd-114">Vælg **Rediger** øverst på siden, og indstil den planlagte startdato/-klokkeslæt til en værdi, der opdaterer analysen, så den er tættere på det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="ae8cd-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchjob](media/batch-jobs.png)
