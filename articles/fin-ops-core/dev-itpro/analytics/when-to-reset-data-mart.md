---
title: Hvornår et datacenter skal nulstilles
description: I dette emne kan du se de forhold, der kan blive forbedret, hvis du nulstiller et datacenter, og forhold, hvor nulstilling af datacenteret sandsynligvis ikke hjælper.
author: jinniew
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c88994a336528650bf8ab6e239c873fa6cd36c46
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754138"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="e3043-103">Hvornår et datacenter skal nulstilles</span><span class="sxs-lookup"><span data-stu-id="e3043-103">When to reset a data mart</span></span>

<span data-ttu-id="e3043-104">Nulstilling af et datacenter kan være tidskrævende.</span><span class="sxs-lookup"><span data-stu-id="e3043-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="e3043-105">Afhængigt af forholdene er denne handling muligvis ikke den løsning, der er brug for.</span><span class="sxs-lookup"><span data-stu-id="e3043-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="e3043-106">I dette emne kan du se de forhold, der kan blive forbedret, hvis du nulstiller et datacenter, samt forhold, hvor nulstilling af datacenteret sandsynligvis ikke hjælper.</span><span class="sxs-lookup"><span data-stu-id="e3043-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="e3043-107">Hvornår skal du nulstille et datacenter?</span><span class="sxs-lookup"><span data-stu-id="e3043-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="e3043-108">Overvej følgende spørgsmål, før du nulstiller et datacenter.</span><span class="sxs-lookup"><span data-stu-id="e3043-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="e3043-109">Hvis du svarer ja til et eller flere spørgsmål, kan det være en fordel for din organisation at nulstille datacenteret.</span><span class="sxs-lookup"><span data-stu-id="e3043-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="e3043-110">Applikationsdatabasen blev gendannet, men databasen for datacenteret blev ikke gendannet.</span><span class="sxs-lookup"><span data-stu-id="e3043-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="e3043-111">Du kan se forkerte data i en regnskabsperiode, hvilket ikke er resultatet af en fejl i rapportdesignet.</span><span class="sxs-lookup"><span data-stu-id="e3043-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="e3043-112">Du kan se forkerte data for en regnskabsperiode, og poster vises under Integrationsforsøg på siden **Integrationsstatus** i Rapportdesigner (start Rapportdesigneren, og vælg **Værktøjer > Integrationsstatus**).</span><span class="sxs-lookup"><span data-stu-id="e3043-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="e3043-113">Du har åbnet en supporthændelse, og en supporttekniker har givet dig besked på at nulstille datacenteret som en del af et fejlfindingstrin.</span><span class="sxs-lookup"><span data-stu-id="e3043-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="e3043-114">Hvornår er det ikke relevant at nulstille et datacenter?</span><span class="sxs-lookup"><span data-stu-id="e3043-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="e3043-115">Der er nogle forhold, hvor vi ikke anbefaler, at du nulstiller et datacenter.</span><span class="sxs-lookup"><span data-stu-id="e3043-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="e3043-116">Blandt andet:</span><span class="sxs-lookup"><span data-stu-id="e3043-116">These include the following.</span></span> 

- <span data-ttu-id="e3043-117">Når årsagen ikke er angivet i dette emne.</span><span class="sxs-lookup"><span data-stu-id="e3043-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="e3043-118">Du oplever ydeevneproblemer forbundet med datasynkronisering. I dette tilfælde hjælper det sandsynligvis ikke at nulstille datacenter.</span><span class="sxs-lookup"><span data-stu-id="e3043-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="e3043-119">Hvis oplever har et tilbagevendende nulstillingsmønster af en af følgende årsager:</span><span class="sxs-lookup"><span data-stu-id="e3043-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="e3043-120">**Manglende data** – Du skal først eliminere fejl i rapportdesignet og fejl i tidsindstillingen for datasynkronisering. Du bemærker f.eks., at faktaoversigten ikke har kørt, siden de manglende data blev bogført.</span><span class="sxs-lookup"><span data-stu-id="e3043-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="e3043-121">**Låst integrationstilstand** – Hvis integrationen er langsom eller virker låst, kan du ikke løse fejlen ved at nulstille datacenteret.</span><span class="sxs-lookup"><span data-stu-id="e3043-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="e3043-122">**Forsøg på nulstilling mislykkedes** – Hvis der er foretaget et antal forsøg på at fuldføre en nulstilling, og dette mislykkedes på grund af manglende data, anbefales det, at du åbner en supporthændelse og samarbejder med en supporttekniker for at analysere din situation, inden du forsøger at nulstille datacenteret igen.</span><span class="sxs-lookup"><span data-stu-id="e3043-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="e3043-123">**Gamle poster** – Gamle poster i sig selv berettiger ikke nødvendigvis en nulstilling af datacenteret.</span><span class="sxs-lookup"><span data-stu-id="e3043-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="e3043-124">Hvis du har et stort datasæt, tager det et stykke tid at køre nulstillingsprocessen, men der sker sandsynligvis ingen forbedring.</span><span class="sxs-lookup"><span data-stu-id="e3043-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="e3043-125">Hvad en nulstilling af datacenteret ikke gør</span><span class="sxs-lookup"><span data-stu-id="e3043-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="e3043-126">En nulstilling starter kun, når eksisterende opgaver er fuldført.</span><span class="sxs-lookup"><span data-stu-id="e3043-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="e3043-127">Derved sikres, at gamle data ikke indsættes.</span><span class="sxs-lookup"><span data-stu-id="e3043-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="e3043-128">På dette tidspunkt vil du muligvis få vist en meddelelse som f.eks. "Nulstillingen af datacenteret kunne ikke behandles på grund af en aktiv opgave.</span><span class="sxs-lookup"><span data-stu-id="e3043-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="e3043-129">Prøv igen senere."</span><span class="sxs-lookup"><span data-stu-id="e3043-129">Please try again later.”</span></span>
- <span data-ttu-id="e3043-130">Nulstillingen deaktiverer integrationsopgaverne og sletter alle data i datacenteret.</span><span class="sxs-lookup"><span data-stu-id="e3043-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="e3043-131">Integrationen er aktiveret igen.</span><span class="sxs-lookup"><span data-stu-id="e3043-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="e3043-132">Følgende punkter angiver to ting, som en nulstilling af et datacenter *ikke* vil gøre.</span><span class="sxs-lookup"><span data-stu-id="e3043-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="e3043-133">Nulstillinger fjerner ikke rapportdesign.</span><span class="sxs-lookup"><span data-stu-id="e3043-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="e3043-134">Nulstillinger rydder ikke firma- eller brugerdata, medmindre disse er valgt.</span><span class="sxs-lookup"><span data-stu-id="e3043-134">Resets do not clear company data or user data unless selected.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]