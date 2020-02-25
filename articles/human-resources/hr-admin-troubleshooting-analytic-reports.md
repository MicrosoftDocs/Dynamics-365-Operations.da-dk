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
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008435"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="1f777-103">Fejlfinding af analyserapporter</span><span class="sxs-lookup"><span data-stu-id="1f777-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="1f777-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="1f777-104">**Issue**</span></span>

<span data-ttu-id="1f777-105">En kundes dataændringer vises ikke under **Analyse**-fanerne i nogen af kundens arbejdsområder.</span><span class="sxs-lookup"><span data-stu-id="1f777-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="1f777-106">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="1f777-106">**Cause**</span></span>

<span data-ttu-id="1f777-107">Som standard opdateres Microsoft Power BI-rapporter hver fjerde time inden for fristerne for batchjobbet Installer måling.</span><span class="sxs-lookup"><span data-stu-id="1f777-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="1f777-108">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="1f777-108">**Resolution**</span></span>

<span data-ttu-id="1f777-109">Dette problem er muligvis kun et spørgsmål om timing.</span><span class="sxs-lookup"><span data-stu-id="1f777-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="1f777-110">Følg disse trin for at starte batchjobbet og opdatere analysearbejdsområderne.</span><span class="sxs-lookup"><span data-stu-id="1f777-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="1f777-111">Åbn siden **Batchjob** på **Systemadministration \> Links \> Batchjob \> Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="1f777-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="1f777-112">Du kan også bruge funktionen Søg og skrive **Batchjob**.</span><span class="sxs-lookup"><span data-stu-id="1f777-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="1f777-113">Find jobbet **Installer måling** på listen.</span><span class="sxs-lookup"><span data-stu-id="1f777-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="1f777-114">Vælg **Rediger** øverst på siden, og indstil den planlagte startdato/-klokkeslæt til en værdi, der opdaterer analysen, så den er tættere på det aktuelle tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="1f777-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Batchjob](media/batch-jobs.png)
