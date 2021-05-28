---
title: Hvornår et datacenter skal nulstilles
description: I dette emne kan du se de forhold, der kan blive forbedret, hvis du nulstiller et datacenter, og forhold, hvor nulstilling af datacenteret sandsynligvis ikke hjælper.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988986"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="ed897-103">Hvornår et datacenter skal nulstilles</span><span class="sxs-lookup"><span data-stu-id="ed897-103">When to reset a data mart</span></span>

<span data-ttu-id="ed897-104">Nulstilling af et datacenter kan være tidskrævende.</span><span class="sxs-lookup"><span data-stu-id="ed897-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="ed897-105">Afhængigt af forholdene er denne handling muligvis ikke den løsning, der er brug for.</span><span class="sxs-lookup"><span data-stu-id="ed897-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="ed897-106">I dette emne kan du se de forhold, der kan blive forbedret, hvis du nulstiller et datacenter, samt forhold, hvor nulstilling af datacenteret sandsynligvis ikke hjælper.</span><span class="sxs-lookup"><span data-stu-id="ed897-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="ed897-107">Hvornår skal jeg nulstille et datacenter?</span><span class="sxs-lookup"><span data-stu-id="ed897-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="ed897-108">Overvej følgende spørgsmål, før du nulstiller et datacenter.</span><span class="sxs-lookup"><span data-stu-id="ed897-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="ed897-109">Hvis du svarer ja til et eller flere spørgsmål, kan det være en fordel for din organisation at nulstille datacenteret.</span><span class="sxs-lookup"><span data-stu-id="ed897-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="ed897-110">Blev programdatabasen gendannet?</span><span class="sxs-lookup"><span data-stu-id="ed897-110">Was the application database restored?</span></span>
- <span data-ttu-id="ed897-111">Hvis du har åbnet en supporthændelse, som en supporttekniker har givet dig besked på at nulstille datacenteret som en del af et fejlfindingstrin?</span><span class="sxs-lookup"><span data-stu-id="ed897-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="ed897-112">Hvornår er det ikke relevant at nulstille et datacenter?</span><span class="sxs-lookup"><span data-stu-id="ed897-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="ed897-113">Der er nogle forhold, hvor vi ikke anbefaler, at du nulstiller et datacenter.</span><span class="sxs-lookup"><span data-stu-id="ed897-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="ed897-114">Blandt andet:</span><span class="sxs-lookup"><span data-stu-id="ed897-114">These include the following.</span></span> 

- <span data-ttu-id="ed897-115">Du oplever forskellige performance-problemer, der er forbundet med datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="ed897-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="ed897-116">Hvis oplever har et tilbagevendende nulstillingsmønster af en af følgende årsager:</span><span class="sxs-lookup"><span data-stu-id="ed897-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="ed897-117">**Manglende data**</span><span class="sxs-lookup"><span data-stu-id="ed897-117">**Missing data**</span></span> 
  - <span data-ttu-id="ed897-118">**Låst integrationstilstand**</span><span class="sxs-lookup"><span data-stu-id="ed897-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="ed897-119">**Gamle poster** – Gamle poster i sig selv berettiger ikke nødvendigvis en nulstilling af datacenteret.</span><span class="sxs-lookup"><span data-stu-id="ed897-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="ed897-120">Hvis du har et stort datasæt, tager det et stykke tid at køre nulstillingsprocessen, men der sker sandsynligvis ingen forbedring.</span><span class="sxs-lookup"><span data-stu-id="ed897-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="ed897-121">Hvad er nulstilling af et datacenter?</span><span class="sxs-lookup"><span data-stu-id="ed897-121">What is a data mart reset?</span></span>
- <span data-ttu-id="ed897-122">En nulstilling starter kun, når eksisterende opgaver er fuldført.</span><span class="sxs-lookup"><span data-stu-id="ed897-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="ed897-123">Derved sikres, at gamle data ikke indsættes.</span><span class="sxs-lookup"><span data-stu-id="ed897-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="ed897-124">På dette tidspunkt vil du muligvis få vist en meddelelse som f.eks. "Nulstillingen af datacenteret kunne ikke behandles på grund af en aktiv opgave.</span><span class="sxs-lookup"><span data-stu-id="ed897-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="ed897-125">Prøv igen senere."</span><span class="sxs-lookup"><span data-stu-id="ed897-125">Please try again later.”</span></span>
- <span data-ttu-id="ed897-126">Nulstillingen deaktiverer integrationsopgaverne og sletter alle data i datacenteret.</span><span class="sxs-lookup"><span data-stu-id="ed897-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="ed897-127">Integrationen er aktiveret igen.</span><span class="sxs-lookup"><span data-stu-id="ed897-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="ed897-128">Hvis jeg nulstiller datacenteret, mister jeg så rapporter, som jeg allerede har udarbejdet?</span><span class="sxs-lookup"><span data-stu-id="ed897-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="ed897-129">Nej, rapporterne gemmes i SQL-tabeller, der ikke påvirkes af, at dataene nulstilles.</span><span class="sxs-lookup"><span data-stu-id="ed897-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="ed897-130">Hvis du er bange for at miste rapporter, du har oprettet, kan du sikkerhedskopiere de design, du ikke ønsker at miste.</span><span class="sxs-lookup"><span data-stu-id="ed897-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="ed897-131">Du kan sikkerhedskopier dem ved at åbne Report Designer og gå til **Firma > Firmaer > Komponenter > Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="ed897-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="ed897-132">Er det nødvendigt, at alle brugere forlader systemet, når dataene skal nulstilles?</span><span class="sxs-lookup"><span data-stu-id="ed897-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="ed897-133">Nej, brugere kan fortsætte med at arbejde i systemet, når data nulstilles.</span><span class="sxs-lookup"><span data-stu-id="ed897-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="ed897-134">De vil dog ikke kunne få adgang til rapporter, der er oprettet med Financial Reporter, før nulstillingen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="ed897-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
