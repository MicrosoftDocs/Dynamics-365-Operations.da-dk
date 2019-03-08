---
title: Analyserapporter opdateres ikke
description: I dette emne beskrives, hvad du skal gøre, hvis en kundes dataændringer ikke vises i nogen af kundens arbejdsområder.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303701"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="d6908-103">Analyserapporter opdateres ikke</span><span class="sxs-lookup"><span data-stu-id="d6908-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6908-104">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="d6908-104">**Issue**</span></span>

<span data-ttu-id="d6908-105">En kundes dataændringer vises ikke under **Analyse**-fanerne i nogen af kundens arbejdsområder.</span><span class="sxs-lookup"><span data-stu-id="d6908-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="d6908-106">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="d6908-106">**Cause**</span></span>

<span data-ttu-id="d6908-107">Som standard opdateres Microsoft Power BI-rapporter hver fjerde time inden for fristerne for batchjobbet Installer måling.</span><span class="sxs-lookup"><span data-stu-id="d6908-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="d6908-108">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="d6908-108">**Resolution**</span></span>

<span data-ttu-id="d6908-109">Dette problem er muligvis kun et spørgsmål om timing.</span><span class="sxs-lookup"><span data-stu-id="d6908-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="d6908-110">Følg disse trin for at starte batchjobbet og opdatere analysearbejdsområderne.</span><span class="sxs-lookup"><span data-stu-id="d6908-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="d6908-111">Åbn siden **Batchjob** på **Systemadministration \> Links \> Batchjob \> Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="d6908-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="d6908-112">Du kan også bruge funktionen Søg og skrive **Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="d6908-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="d6908-113">Find jobbet **Installer måling** på listen.</span><span class="sxs-lookup"><span data-stu-id="d6908-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="d6908-114">Vælg **Rediger** øverst på siden, og indstil den planlagte startdato/-klokkeslæt til en værdi, der opdaterer analysen, så den er tættere på det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="d6908-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchjob](media/batch-jobs.png)
