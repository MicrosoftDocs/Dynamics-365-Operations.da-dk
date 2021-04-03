---
title: Behandle ændringer af livshændelse
description: Behandl ændringer af livshændelser i Microsoft Dynamics 365 Human Resources for ændringer af livshændelser.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 2726dcb3c847c9af2a431358de04a27341b9e66c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464244"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="96320-103">Behandle ændringer af livshændelse</span><span class="sxs-lookup"><span data-stu-id="96320-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="96320-104">Behandl ændringer af livshændelser i Microsoft Dynamics 365 Human Resources for to ændringer af livshændelser:</span><span class="sxs-lookup"><span data-stu-id="96320-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="96320-105">Fødselsdagsændringer</span><span class="sxs-lookup"><span data-stu-id="96320-105">Birthday changes</span></span>
- <span data-ttu-id="96320-106">Berettigelsesregel tilsidesætte udløbsændringer</span><span class="sxs-lookup"><span data-stu-id="96320-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="96320-107">Vælg **Behandling af ændringer af livshændelse** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="96320-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="96320-108">Angiv værdier for følgende felter i dialogboksen **Kør behandling af ændringer af livshændelse**:</span><span class="sxs-lookup"><span data-stu-id="96320-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="96320-109">Felt</span><span class="sxs-lookup"><span data-stu-id="96320-109">Field</span></span> | <span data-ttu-id="96320-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="96320-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="96320-111">Tilmeldingsperiode</span><span class="sxs-lookup"><span data-stu-id="96320-111">Enrollment period</span></span> | <span data-ttu-id="96320-112">Den tilmeldingsperiode, der skal behandles ændringer af livshændelse for.</span><span class="sxs-lookup"><span data-stu-id="96320-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="96320-113">Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="96320-113">Legal entity</span></span> | <span data-ttu-id="96320-114">Den juridiske enhed, der skal behandles ændringer af livshændelse for.</span><span class="sxs-lookup"><span data-stu-id="96320-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="96320-115">Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="96320-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="96320-116">Angiv oplysninger om processen.</span><span class="sxs-lookup"><span data-stu-id="96320-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="96320-117">Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="96320-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="96320-118">Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="96320-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="96320-119">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="96320-119">Select **OK**.</span></span> <span data-ttu-id="96320-120">Processen køres med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="96320-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="96320-121">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="96320-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]