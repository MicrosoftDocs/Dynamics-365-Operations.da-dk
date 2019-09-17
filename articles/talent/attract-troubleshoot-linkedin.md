---
title: Fejlfinding af integration med LinkedIn og Microsoft Dynamics 365 for Talent - Attract
description: Dette emne forklarer, hvordan du løser problemer, når du prøver at slå job op på LinkedIn fra Microsoft Dynamics 365 for Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 82ba7c505ba09e47f3c517c74c22e6aef7cd4e65
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739351"
---
# <a name="troubleshoot-integration-with-linkedin"></a><span data-ttu-id="4fa62-103">Fejlfinding af integration med LinkedIn</span><span class="sxs-lookup"><span data-stu-id="4fa62-103">Troubleshoot integration with LinkedIn</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fa62-104">Brug følgende information som hjælp til at løse problemer, du måtte have, når du prøver at slå job op på LinkedIn fra Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="4fa62-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 for Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="4fa62-105">Du kan ikke logge på LinkedIn fra Attract</span><span class="sxs-lookup"><span data-stu-id="4fa62-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="4fa62-106">Hvis du har problemer med at logge på LinkedIn fra Attract, kan du prøve disse trin:</span><span class="sxs-lookup"><span data-stu-id="4fa62-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="4fa62-107">Kontrollér, at de legitimationsoplysninger til LinkedIn, du indtastede i Attract, er gyldige og korrekte.</span><span class="sxs-lookup"><span data-stu-id="4fa62-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="4fa62-108">Hvis legitimationsoplysningerne er gyldige og korrekte, skal du kontakte [LinkedIn-support](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="4fa62-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="4fa62-109">Hvis problemet fortsætter, skal du kontakte [Microsoft-support](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="4fa62-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="4fa62-110">Jobopslag fra Attract vises ikke på LinkedIn</span><span class="sxs-lookup"><span data-stu-id="4fa62-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="4fa62-111">Hvis dit job ikke er vist på LinkedIn efter 24 timer, kan du prøve disse trin:</span><span class="sxs-lookup"><span data-stu-id="4fa62-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="4fa62-112">Sørg for, at dit LinkedIn-firma-id-kort er tilknyttet din LinkedIn-firmaside og er korrekt indtastet i Attract Administration.</span><span class="sxs-lookup"><span data-stu-id="4fa62-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="4fa62-113">Der er mere information om, hvordan du ændrer LinkedIn-indstillinger i Administration, under [Konfigurere integration med LinkedIn](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="4fa62-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn](attract-admin-linkedin.md).</span></span> <span data-ttu-id="4fa62-114">Der er mere information om LinkedIn-firma-id under [Tilknytning af dit LinkedIn-firma-id til LinkedIn-jobportalen - ofte stillede spørgsmål](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="4fa62-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="4fa62-115">Kontrollér joboplysningerne på LinkedIn for at sikre dig, at adressen er komplet.</span><span class="sxs-lookup"><span data-stu-id="4fa62-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="4fa62-116">For at kunne slå et job op korrekt skal LinkedIn mindst have byen og landet eller regionen for jobbet.</span><span class="sxs-lookup"><span data-stu-id="4fa62-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="4fa62-117">Sørg for, at jobbet ikke dublerer et andet job, der er blevet slået op på LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="4fa62-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="4fa62-118">LinkedIn slår ikke job op, der er dubletter af hverken LinkedIn Premium-jobmuligheder eller gratis begrænsede jobopslag fra en anden kilde.</span><span class="sxs-lookup"><span data-stu-id="4fa62-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="4fa62-119">Kontrollér, at en anden person i din virksomhed ikke allerede har slået jobbet op manuelt.</span><span class="sxs-lookup"><span data-stu-id="4fa62-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fa62-120">Se også</span><span class="sxs-lookup"><span data-stu-id="4fa62-120">See also</span></span>

[<span data-ttu-id="4fa62-121">Ofte stillede spørgsmål om FAQ</span><span class="sxs-lookup"><span data-stu-id="4fa62-121">LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="4fa62-122">Slå job op på LinkedIn fra Attract</span><span class="sxs-lookup"><span data-stu-id="4fa62-122">Post jobs to LinkedIn from Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="4fa62-123">Rekruttere kandidater med LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="4fa62-123">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="4fa62-124">Oprette job</span><span class="sxs-lookup"><span data-stu-id="4fa62-124">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="4fa62-125">Fejlfinding af integration med LinkedIn</span><span class="sxs-lookup"><span data-stu-id="4fa62-125">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
