---
title: Behandle satsændringer
description: Behandle ændringer i frynsegodesatsen i Microsoft Dynamics 365 Human Resources, når en ny eller eksisterende frynsegodeplan har en ændring i indstillingerne for berettigelsesregler.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ebe5cfc2bdf7790770d27ece2dc67f7677db593
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008445"
---
# <a name="process-rate-changes"></a><span data-ttu-id="45298-103">Behandle satsændringer</span><span class="sxs-lookup"><span data-stu-id="45298-103">Process rate changes</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="45298-104">Behandle ændringer i frynsegodesatsen i Microsoft Dynamics 365 Human Resources, når en ny eller eksisterende frynsegodeplan har en ændring i indstillingerne for berettigelsesregler.</span><span class="sxs-lookup"><span data-stu-id="45298-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="45298-105">Hvis der oprettes en ny berettigelsesregel, som tildeles til planen, bliver systemet bedt om at køre medarbejderberettigelse igen for at kontrollere, om arbejdere nu er berettiget til planen baseret på nye indstillinger for berettigelse.</span><span class="sxs-lookup"><span data-stu-id="45298-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to re-run worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="45298-106">Vælg **Behandling af opdateret satsændring** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="45298-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="45298-107">Angiv værdier for følgende felter i dialogboksen **Kør behandling af opdateret frynsegodesats**:</span><span class="sxs-lookup"><span data-stu-id="45298-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="45298-108">Felt</span><span class="sxs-lookup"><span data-stu-id="45298-108">Field</span></span> | <span data-ttu-id="45298-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="45298-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="45298-110">Tilmeldingsperiode</span><span class="sxs-lookup"><span data-stu-id="45298-110">Enrollment period</span></span> | <span data-ttu-id="45298-111">Den tilmeldingsperiode, som satsændringer skal behandles for.</span><span class="sxs-lookup"><span data-stu-id="45298-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="45298-112">Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="45298-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="45298-113">Angiv oplysninger om processen.</span><span class="sxs-lookup"><span data-stu-id="45298-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="45298-114">Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="45298-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="45298-115">Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="45298-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="45298-116">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="45298-116">Select **OK**.</span></span> <span data-ttu-id="45298-117">Processen køres med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="45298-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="45298-118">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="45298-118">Select **OK**.</span></span>