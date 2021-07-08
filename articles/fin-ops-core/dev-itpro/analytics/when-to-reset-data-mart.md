---
title: Ofte stillede spørgsmål om nulstilling af datacenter
description: Dette emne indeholder svar på nogle af de ofte stillede spørgsmål om nulstilling af datacenter.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266603"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="4afb6-103">Ofte stillede spørgsmål om nulstilling af datacenter</span><span class="sxs-lookup"><span data-stu-id="4afb6-103">Data mart resets FAQ</span></span>

<span data-ttu-id="4afb6-104">Dette emne indeholder svar på nogle af de ofte stillede spørgsmål om nulstilling af datacenter.</span><span class="sxs-lookup"><span data-stu-id="4afb6-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="4afb6-105">En nulstilling af datacenteret kan være en tidskrævende proces, og afhængigt af omstændighederne er det muligvis ikke den løsning, der kræves.</span><span class="sxs-lookup"><span data-stu-id="4afb6-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="4afb6-106">Dette emne indeholder derfor oplysninger om situationer, hvor nulstilling af et datacenter kan være en hjælp, og situationer, hvor det sandsynligvis ikke vil hjælpe.</span><span class="sxs-lookup"><span data-stu-id="4afb6-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="4afb6-107">Hvad er nulstilling af et datacenter?</span><span class="sxs-lookup"><span data-stu-id="4afb6-107">What is a data mart reset?</span></span>

<span data-ttu-id="4afb6-108">Hvis du nulstiller et datacenter, deaktiveres integrationsopgaverne, alle dataene i datacenteret slettes, og integration aktiveres igen.</span><span class="sxs-lookup"><span data-stu-id="4afb6-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="4afb6-109">For at sikre, at gamle datacentre ikke indsættes, kan nulstilling af et datacenter først startes, når de eksisterende opgaver er fuldført.</span><span class="sxs-lookup"><span data-stu-id="4afb6-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="4afb6-110">Hvis du forsøger at nulstille datacenteret, før alle opgaver er fuldført, får du muligvis vist en meddelelse som f.eks. "Nulstilling af datacenteret kunne ikke udføres på grund af en aktiv opgave.</span><span class="sxs-lookup"><span data-stu-id="4afb6-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="4afb6-111">Prøv igen senere."</span><span class="sxs-lookup"><span data-stu-id="4afb6-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="4afb6-112">Hvornår skal jeg nulstille et datacenter?</span><span class="sxs-lookup"><span data-stu-id="4afb6-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="4afb6-113">Hvis en eller flere af følgende forhold gælder for din situation, kan din organisation med fordel nulstille et datacenter:</span><span class="sxs-lookup"><span data-stu-id="4afb6-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="4afb6-114">Programdatabasen er gendannet.</span><span class="sxs-lookup"><span data-stu-id="4afb6-114">The application database was restored.</span></span>
- <span data-ttu-id="4afb6-115">Du har åbnet en supportanmodning, og en supporttekniker har givet dig besked på at nulstille datacenteret som en del af et fejlfindingstrin.</span><span class="sxs-lookup"><span data-stu-id="4afb6-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="4afb6-116">Hvornår skal et datacenter ikke nulstilles?</span><span class="sxs-lookup"><span data-stu-id="4afb6-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="4afb6-117">Her er nogle af de situationer, hvor vi ikke anbefaler, at du nulstiller datacenteret:</span><span class="sxs-lookup"><span data-stu-id="4afb6-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="4afb6-118">Du oplever forskellige ydeevneproblemer, der er forbundet med datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="4afb6-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="4afb6-119">Du har et tilbagevendende nulstillingsmønster af en af følgende årsager:</span><span class="sxs-lookup"><span data-stu-id="4afb6-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="4afb6-120">**Manglende data** – Hvis du bemærker, at der mangler data, skal du åbne en supportanmodning hos Microsoft for at gennemse rapportformatet og eventuelle problemer med datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="4afb6-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="4afb6-121">**Låst integrationstilstand**</span><span class="sxs-lookup"><span data-stu-id="4afb6-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="4afb6-122">**Gamle poster** – Gamle poster i sig selv berettiger ikke nødvendigvis en nulstilling af datacenteret.</span><span class="sxs-lookup"><span data-stu-id="4afb6-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="4afb6-123">Hvis du har et stort datasæt, tager det et stykke tid at køre nulstillingsprocessen, men der sker sandsynligvis ingen forbedring.</span><span class="sxs-lookup"><span data-stu-id="4afb6-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="4afb6-124">Hvis jeg nulstiller datacenteret, mister jeg så rapporter, som jeg allerede har udarbejdet?</span><span class="sxs-lookup"><span data-stu-id="4afb6-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="4afb6-125">Nr.</span><span class="sxs-lookup"><span data-stu-id="4afb6-125">No.</span></span> <span data-ttu-id="4afb6-126">Dine rapporter gemmes i SQL-tabeller, der ikke påvirkes af, at dataene nulstilles.</span><span class="sxs-lookup"><span data-stu-id="4afb6-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="4afb6-127">Hvis du er bange for at miste rapporter, som du har oprettet, kan du sikkerhedskopiere de design, du ikke ønsker at miste.</span><span class="sxs-lookup"><span data-stu-id="4afb6-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="4afb6-128">Du kan sikkerhedskopier design ved at åbne Report Designer og gå til **Firma \> Firmaer \> Komponenter \> Eksportér**.</span><span class="sxs-lookup"><span data-stu-id="4afb6-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="4afb6-129">Skal alle brugere forlade systemet, før jeg kan nulstille datacenteret?</span><span class="sxs-lookup"><span data-stu-id="4afb6-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="4afb6-130">Nr.</span><span class="sxs-lookup"><span data-stu-id="4afb6-130">No.</span></span> <span data-ttu-id="4afb6-131">Brugere kan fortsætte med at arbejde i systemet, mens et datacenter nulstilles.</span><span class="sxs-lookup"><span data-stu-id="4afb6-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="4afb6-132">Brugere vil dog ikke kunne få adgang til rapporter, der er oprettet ved hjælp af Financial Reporter, før nulstillingen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="4afb6-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
