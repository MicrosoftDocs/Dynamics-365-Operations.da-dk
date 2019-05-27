---
title: Analyserapporter opdateres ikke
description: I dette emne beskrives, hvad du skal gøre, hvis en kundes dataændringer ikke vises i nogen af kundens arbejdsområder.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517659"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="2f922-103">Analyserapporter opdateres ikke</span><span class="sxs-lookup"><span data-stu-id="2f922-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f922-104">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="2f922-104">**Issue**</span></span>

<span data-ttu-id="2f922-105">En kundes dataændringer vises ikke under **Analyse**-fanerne i nogen af kundens arbejdsområder.</span><span class="sxs-lookup"><span data-stu-id="2f922-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="2f922-106">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="2f922-106">**Cause**</span></span>

<span data-ttu-id="2f922-107">Som standard opdateres Microsoft Power BI-rapporter hver fjerde time inden for fristerne for batchjobbet Installer måling.</span><span class="sxs-lookup"><span data-stu-id="2f922-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="2f922-108">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="2f922-108">**Resolution**</span></span>

<span data-ttu-id="2f922-109">Dette problem er muligvis kun et spørgsmål om timing.</span><span class="sxs-lookup"><span data-stu-id="2f922-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="2f922-110">Følg disse trin for at starte batchjobbet og opdatere analysearbejdsområderne.</span><span class="sxs-lookup"><span data-stu-id="2f922-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="2f922-111">Åbn siden **Batchjob** på **Systemadministration \> Links \> Batchjob \> Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="2f922-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="2f922-112">Du kan også bruge funktionen Søg og skrive **Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="2f922-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="2f922-113">Find jobbet **Installer måling** på listen.</span><span class="sxs-lookup"><span data-stu-id="2f922-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="2f922-114">Vælg **Rediger** øverst på siden, og indstil den planlagte startdato/-klokkeslæt til en værdi, der opdaterer analysen, så den er tættere på det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="2f922-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchjob](media/batch-jobs.png)
