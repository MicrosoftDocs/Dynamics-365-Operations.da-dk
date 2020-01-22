---
title: Gem opgaveguider for LCS, og afspil dem
description: I dette emne beskrives, hvordan du kan gemme opgaveguider til Microsoft Dynamics Lifecycle Services (LCS) og derefter afspille dem igen.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6ee3556e033cf298bbd5102746d2b57884f5e6d0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898058"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="092b7-103">Gem opgaveguider for LCS, og afspil dem</span><span class="sxs-lookup"><span data-stu-id="092b7-103">Save task guides to LCS and replay them</span></span>

<span data-ttu-id="092b7-104">**Miljøoplysninger**</span><span class="sxs-lookup"><span data-stu-id="092b7-104">**Environment details**</span></span> 

<span data-ttu-id="092b7-105">Microsoft Dynamics 365 Talent, som blev installeret via Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="092b7-105">Microsoft Dynamics 365 Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="092b7-106">**Afgang**</span><span class="sxs-lookup"><span data-stu-id="092b7-106">**Issue**</span></span>

<span data-ttu-id="092b7-107">Kunden ønsker at gemme nye opgaveregistreringer til sit LCS-projekt og derefter afspille de gemte opgaveguider igen.</span><span class="sxs-lookup"><span data-stu-id="092b7-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="092b7-108">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="092b7-108">**Resolution**</span></span>

<span data-ttu-id="092b7-109">Følg disse trin for at gemme en opgaveregistrering til LCS.</span><span class="sxs-lookup"><span data-stu-id="092b7-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="092b7-110">Log på LCS, og vælg projektet.</span><span class="sxs-lookup"><span data-stu-id="092b7-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="092b7-111">Vælg feltet **Forretningsmodeldesigner**.</span><span class="sxs-lookup"><span data-stu-id="092b7-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="092b7-112">Få vist siden i "Opdateret BPM-oplevelse".</span><span class="sxs-lookup"><span data-stu-id="092b7-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="092b7-113">Vælg et bibliotek, og vælg derefter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="092b7-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="092b7-114">Angiv et navn til forretningsmodeldesigneren (BPM).</span><span class="sxs-lookup"><span data-stu-id="092b7-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="092b7-115">Log på Talent fra LCS.</span><span class="sxs-lookup"><span data-stu-id="092b7-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="092b7-116">Skriv **hjælp** i feltet **Søg**.</span><span class="sxs-lookup"><span data-stu-id="092b7-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="092b7-117">Hjælp til Lifecycle Services åbnes.</span><span class="sxs-lookup"><span data-stu-id="092b7-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="092b7-118">Vælg knappen **Opdater** til konfiguration af Lifecycle Services Hjælp.</span><span class="sxs-lookup"><span data-stu-id="092b7-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="092b7-119">Dit nye BPM-bibliotek vises, og det skal være aktivt.</span><span class="sxs-lookup"><span data-stu-id="092b7-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="092b7-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="092b7-120">Close the page.</span></span>
10. <span data-ttu-id="092b7-121">Opret en opgaveregistrering.</span><span class="sxs-lookup"><span data-stu-id="092b7-121">Create a task recording.</span></span>
11. <span data-ttu-id="092b7-122">Når du har gjort det, skal du vælge **Gem Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="092b7-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Gem i Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="092b7-124">Vælg det BPM-bibliotek og den node, som opgaveregistreringen skal gemmes til.</span><span class="sxs-lookup"><span data-stu-id="092b7-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="092b7-125">Følg disse trin for at afspille en opgaveguide fra LCS.</span><span class="sxs-lookup"><span data-stu-id="092b7-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="092b7-126">Start Arbejdsrutineoptager.</span><span class="sxs-lookup"><span data-stu-id="092b7-126">Start Task recorder.</span></span>
2. <span data-ttu-id="092b7-127">Vælg **Åbn fra LCS**.</span><span class="sxs-lookup"><span data-stu-id="092b7-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="092b7-128">Vælg biblioteket og den BPM-node, der har den gemte opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="092b7-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="092b7-129">Åbn opgaveguiden.</span><span class="sxs-lookup"><span data-stu-id="092b7-129">Open the task guide.</span></span>
