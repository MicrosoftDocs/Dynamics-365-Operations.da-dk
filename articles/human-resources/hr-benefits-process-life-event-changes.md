---
title: Behandle ændringer af livshændelse
description: Behandl ændringer af livshændelser i Microsoft Dynamics 365 Human Resources for ændringer af livshændelser.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3cddc6205660b48abd9067bfdcaa04c9d2ba541
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790902"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="61243-103">Behandle ændringer af livshændelse</span><span class="sxs-lookup"><span data-stu-id="61243-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="61243-104">Behandl ændringer af livshændelser i Microsoft Dynamics 365 Human Resources for to ændringer af livshændelser:</span><span class="sxs-lookup"><span data-stu-id="61243-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="61243-105">Fødselsdagsændringer</span><span class="sxs-lookup"><span data-stu-id="61243-105">Birthday changes</span></span>
- <span data-ttu-id="61243-106">Berettigelsesregel tilsidesætte udløbsændringer</span><span class="sxs-lookup"><span data-stu-id="61243-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="61243-107">Vælg **Behandling af ændringer af livshændelse** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="61243-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="61243-108">Angiv værdier for følgende felter i dialogboksen **Kør behandling af ændringer af livshændelse**:</span><span class="sxs-lookup"><span data-stu-id="61243-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="61243-109">Felt</span><span class="sxs-lookup"><span data-stu-id="61243-109">Field</span></span> | <span data-ttu-id="61243-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="61243-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="61243-111">Tilmeldingsperiode</span><span class="sxs-lookup"><span data-stu-id="61243-111">Enrollment period</span></span> | <span data-ttu-id="61243-112">Den tilmeldingsperiode, der skal behandles ændringer af livshændelse for.</span><span class="sxs-lookup"><span data-stu-id="61243-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="61243-113">Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="61243-113">Legal entity</span></span> | <span data-ttu-id="61243-114">Den juridiske enhed, der skal behandles ændringer af livshændelse for.</span><span class="sxs-lookup"><span data-stu-id="61243-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="61243-115">Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="61243-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="61243-116">Angiv oplysninger om processen.</span><span class="sxs-lookup"><span data-stu-id="61243-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="61243-117">Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="61243-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="61243-118">Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="61243-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="61243-119">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="61243-119">Select **OK**.</span></span> <span data-ttu-id="61243-120">Processen køres med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="61243-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="61243-121">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="61243-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]