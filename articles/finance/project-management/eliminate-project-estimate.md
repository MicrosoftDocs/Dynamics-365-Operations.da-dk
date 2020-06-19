---
title: Eliminere et projektestimat
description: Dette emne indeholder oplysninger om eliminering af et projektestimat, efter at det er færdigt.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410202"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="26014-103">Eliminere et projektestimat</span><span class="sxs-lookup"><span data-stu-id="26014-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26014-104">Projektestimater giver den økonomiske visning for arbejde, der er forkalkuleret og planlagt for et projekt.</span><span class="sxs-lookup"><span data-stu-id="26014-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="26014-105">For at arbejde med estimater for et projekt, skal projektet knyttes til et forkalkuleret projekt.</span><span class="sxs-lookup"><span data-stu-id="26014-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="26014-106">Et forkalkuleret projekt er altid baseret på et eksisterende projekt, men flere projekter kan referere til et enkelt forkalkuleret projekt.</span><span class="sxs-lookup"><span data-stu-id="26014-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="26014-107">Der kan kun knyttes fastpris- og investeringsprojekter til forkalkulerede projekter, og de pågældende projekter skal tilhøre samme projektgruppe som det forkalkulerede projekt.</span><span class="sxs-lookup"><span data-stu-id="26014-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="26014-108">Hvis du vil eliminere et forkalkuleret projekt, skal dette være færdigt.</span><span class="sxs-lookup"><span data-stu-id="26014-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="26014-109">I følgende fremgangsmåde beskrives det, hvordan du eliminerer et estimat.</span><span class="sxs-lookup"><span data-stu-id="26014-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="26014-110">Gå til **Projektstyring og regnskab** > **Alle projekter**, og åbn projektet.</span><span class="sxs-lookup"><span data-stu-id="26014-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="26014-111">På fanen **Administrer** skal du vælge **Estimater** og på siden **Estimat** skal du vælge **Eliminer**.</span><span class="sxs-lookup"><span data-stu-id="26014-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="26014-112">På siden **Eliminer estimat** på fanen **Generelt** skal du væge følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="26014-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="26014-113">**Periodekode**: Vælg den periodekode, som skal vælge de forkalkulerede projekter.</span><span class="sxs-lookup"><span data-stu-id="26014-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="26014-114">**Estimatdato**: Vælg estimatdatoen for eliminering.</span><span class="sxs-lookup"><span data-stu-id="26014-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="26014-115">**Eliminer med IGVA-advarsler**: Aktivér denne indstilling for at give besked, når et estimat, der er tilknyttet et igangværende arbejde (IGVA), elimineres.</span><span class="sxs-lookup"><span data-stu-id="26014-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="26014-116">Hvis denne indstilling ikke er aktiveret, kan elimineringen ikke fortsætte, hvis der findes posteringer, som ikke er estimerede.</span><span class="sxs-lookup"><span data-stu-id="26014-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="26014-117">Denne indstilling er kun tilgængelig, hvis eliminering anvendes på et forkalkuleret projekt.</span><span class="sxs-lookup"><span data-stu-id="26014-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="26014-118">Den er ikke tilgængelig, hvis du anvender periodiske posteringer.</span><span class="sxs-lookup"><span data-stu-id="26014-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="26014-119">Denne indstilling fungerer sammen med indstillingerne på fanen **Estimat** på siden **Projektparametre** i feltgruppen **Tillad eliminering, når der findes ikke-forkalkulerede posteringer**.</span><span class="sxs-lookup"><span data-stu-id="26014-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="26014-120">**Indstil stadie til Færdig**: Aktivér denne indstilling for at angive det forkalkulerede projeks stadie til **Færdig,** når du har kørt elimineringen.</span><span class="sxs-lookup"><span data-stu-id="26014-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="26014-121">**Udskriv estimatliste**: Vælg de oplysninger, som skal medtages, når estimatlisten udskrives.</span><span class="sxs-lookup"><span data-stu-id="26014-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="26014-122">**Vis infolog**: Aktivér denne indstilling for at få vist infologgen.</span><span class="sxs-lookup"><span data-stu-id="26014-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="26014-123">**Bogføringsdato**: Vælg estimatets finansbogføringsdato.</span><span class="sxs-lookup"><span data-stu-id="26014-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="26014-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="26014-124">Select **OK**.</span></span>
5. <span data-ttu-id="26014-125">Når elimineringsprocessen er færdig, vises det eliminerede forkalkulerede projekt med en negativ værdi.</span><span class="sxs-lookup"><span data-stu-id="26014-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="26014-126">Hvis du ikke har tænkt dig at eliminere et estimat, kan du vælge det eliminerede estimat og vælge **Tilbagefør eliminering**.</span><span class="sxs-lookup"><span data-stu-id="26014-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
