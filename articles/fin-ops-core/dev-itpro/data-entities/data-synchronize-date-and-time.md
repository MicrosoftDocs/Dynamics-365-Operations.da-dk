---
title: Synkronisere dato og klokkeslæt i importjob
description: Brug UTC-tidszoner i importjob for at undgå problemer med tidszonekonverteringer.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798713"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="30736-103">Synkronisere dato og klokkeslæt i importjob</span><span class="sxs-lookup"><span data-stu-id="30736-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30736-104">Det er vigtigt at angive tidszonen for importjobbet til UTC-tid (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="30736-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="30736-105">Der kan forekomme uventede datoer og klokkeslæt i de importerede data, hvis du bruger en anden indstilling.</span><span class="sxs-lookup"><span data-stu-id="30736-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="30736-106">Uden den korrekte indstilling konverterer importprocessen UTC-datoen til det lokale format, og systemindstillingerne konverterer det igen.</span><span class="sxs-lookup"><span data-stu-id="30736-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="30736-107">Denne dobbelte konvertering bevirker, at der ændres datoer mellem programmer.</span><span class="sxs-lookup"><span data-stu-id="30736-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="30736-108">Konverteringen kan f.eks. bevirke, at en medarbejders startdato er forskellig i Dynamics 365 Human Resources og Dynamics 365 Finance pga. forskelle i lokale tidszoner.</span><span class="sxs-lookup"><span data-stu-id="30736-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="30736-109">Når importjobbet indstilles til UTC-tid, løses dette problem.</span><span class="sxs-lookup"><span data-stu-id="30736-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="30736-110">Vælg **Datastyring** i Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="30736-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="30736-111">Vælg **Importer projekter**, og vælg derefter projektet.</span><span class="sxs-lookup"><span data-stu-id="30736-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="30736-112">Vælg **CSV-Unicode** under **Kildedatoformat**.</span><span class="sxs-lookup"><span data-stu-id="30736-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="30736-113">[![Skifte kildedatoformat til UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="30736-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="30736-114">Skift **Tidszone** til **UTC-tid**, og skift **Sprog** til **da-dk**.</span><span class="sxs-lookup"><span data-stu-id="30736-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>


