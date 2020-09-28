---
title: Synkronisere ressourcekapacitet
description: Dette emne giver oplysninger om, hvordan du kan synkronisere en ressources kapacitet på tværs af kalendere og projekter.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760502"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="a7b5e-103">Synkronisere ressourcekapacitet</span><span class="sxs-lookup"><span data-stu-id="a7b5e-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7b5e-104">Processerne til ressourcesynkronisering hjælper med at sikre, at oplysningerne til kalenderen og basiskalenderen videreføres til ressourceplanlægning for projektet.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="a7b5e-105">Hvis kalenderen ændres, foretager processerne de nødvendige opdateringer af planlægningen af projektressourcerne.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="a7b5e-106">Processerne forbedrer også ydeevnen, da kalenderens ressourceoplysninger synkroniseres på forhånd.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="a7b5e-107">Opdateringer til oplysninger om ressourceplanlægning udføres derfor hurtigere.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="a7b5e-108">Vi anbefaler, at du planlægger processerne som en batch i stedet for én ad gangen.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="a7b5e-109">Ellers er der risiko for, at nogen vil glemme inklusive-datoerne, hvor oplysningerne sidst blev synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="a7b5e-110">Hvis inklusive-datoer ikke bruges, kan der opstå mellemrum under synkronisering af datoer.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="a7b5e-112">Synkronisér ressourcekapacitet, opkøb</span><span class="sxs-lookup"><span data-stu-id="a7b5e-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="a7b5e-113">Synkroniseringsprocessen er designet til at synkronisere alle oplysninger i ressourcekalenderen.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="a7b5e-114">Disse oplysninger omfatter basiskalenderoplysninger om eventuelle ændringer af projektets tabel for ressourcekalenderkapacitet.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="a7b5e-115">Hvis der tilføjes nye ressourcer i projektet, hjælper synkroniseringen med at sikre, at de opdaterede kalenderoplysninger er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="a7b5e-116">Denne synkronisering kan udføres når som helst.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="a7b5e-117">Vi anbefaler, at du bruger en batch.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-117">We recommend that you use a batch.</span></span> <span data-ttu-id="a7b5e-118">Indstillingerne er tilgængelige under synkronisering af kapacitetsreservationer.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="a7b5e-119">Vælg **Projektstyring og regnskab** &gt; **Periodisk** &gt; **Kapacitetssynkronisering** &gt; **Synkronisér ressourcekapacitet akkumuleringer**.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="a7b5e-120">Angiv indstillingerne i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="a7b5e-121">Indstilling</span><span class="sxs-lookup"><span data-stu-id="a7b5e-121">Option</span></span>      | <span data-ttu-id="a7b5e-122">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a7b5e-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="a7b5e-123">Periodekode</span><span class="sxs-lookup"><span data-stu-id="a7b5e-123">Period code</span></span> | <span data-ttu-id="a7b5e-124">Vælg datointervalkoden for Finans for at angive start- og slutdatoer for synkroniseringsprocessen for ressourcekapacitet akkumuleringer.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="a7b5e-125">Igangsæt dato</span><span class="sxs-lookup"><span data-stu-id="a7b5e-125">Start date</span></span>  | <span data-ttu-id="a7b5e-126">Angiv startdatoen for synkroniseringsprocessen for ressourcekapacitet akkumuleringer.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="a7b5e-127">Slutdato</span><span class="sxs-lookup"><span data-stu-id="a7b5e-127">End date</span></span>    | <span data-ttu-id="a7b5e-128">Angiv slutdatoen for synkroniseringsprocessen for ressourcekapacitet akkumuleringer.</span><span class="sxs-lookup"><span data-stu-id="a7b5e-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="a7b5e-129">[![Synkroniseringsproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="a7b5e-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
