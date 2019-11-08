---
title: Tilstandsvurdering
description: Dette emne forklarer, hvordan du opretter en skabelon til tilstandsvurdering og registrering af et aktiv i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05d1a38ab8de406a1615c474ffe39d231335fb67
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570047"
---
# <a name="condition-assessment"></a><span data-ttu-id="2516e-103">Tilstandsvurdering</span><span class="sxs-lookup"><span data-stu-id="2516e-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2516e-104">Dette emne forklarer, hvordan du opretter en skabelon til tilstandsvurdering og registrering af et aktiv i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="2516e-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="2516e-105">Tilstandsvurdering udføres med jævne mellemrum, og det primære formål er at oprette og vedligeholde tilstandsdata for aktiver.</span><span class="sxs-lookup"><span data-stu-id="2516e-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="2516e-106">Set fra et forebyggende vedligeholdelsesperspektiv er det vigtigt at overvåge nøgleoplysninger såsom aktuel tilstand og resterende levetid.</span><span class="sxs-lookup"><span data-stu-id="2516e-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="2516e-107">Desuden, hvis du udfører tilstandsvurdering med jævne mellemrum, vil du være i stand til at overvåge og sammenligne tilstande på maskinerne i din fabrik.</span><span class="sxs-lookup"><span data-stu-id="2516e-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="2516e-108">Tilstandsvurdering kan bruges til at måle og overvåge mange tilstande på dit udstyr.</span><span class="sxs-lookup"><span data-stu-id="2516e-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="2516e-109">Eksempel: Du kan måle vibrationer på dine maskiner.</span><span class="sxs-lookup"><span data-stu-id="2516e-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="2516e-110">Når du har registreret vibrationsmålinger i Styring af aktiver på forskellige typer udstyr, kan du søge efter den seneste registrerede vurdering og se vibrationsmålinger.</span><span class="sxs-lookup"><span data-stu-id="2516e-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="2516e-111">Tilstandsvurdering oprettes på aktiver.</span><span class="sxs-lookup"><span data-stu-id="2516e-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="2516e-112">Du konfigurerer en tilstandsvurderingsskabelon på en aktivtype, før du udfører proceduren for tilstandsvurdering.</span><span class="sxs-lookup"><span data-stu-id="2516e-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="2516e-113">Årsagen til at bruge skabeloner til tilstandsvurdering er at undgå variation af tilstandsdata for lignende aktiver.</span><span class="sxs-lookup"><span data-stu-id="2516e-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="2516e-114">Rækkefølgen for opsætning og brug af tilstandsvurdering i Styring af aktiver er: Først skal du oprette de påkrævede skabeloner til tilstandsvurdering.</span><span class="sxs-lookup"><span data-stu-id="2516e-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="2516e-115">Derefter knytter du skabeloner til aktivtyper i formen **Aktivtyper**.</span><span class="sxs-lookup"><span data-stu-id="2516e-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="2516e-116">Endelig kan du oprette registreringer af tilstandsvurderinger for et aktiv i formen **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="2516e-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="2516e-117">Oprette en skabelon til tilstandsvurdering</span><span class="sxs-lookup"><span data-stu-id="2516e-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="2516e-118">Vælg **Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tilstandsvurdering**.</span><span class="sxs-lookup"><span data-stu-id="2516e-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="2516e-119">Vælg **Ny** for at oprette en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="2516e-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="2516e-120">I feltet **Skabelon** skal du skrive skabelon-id'et.</span><span class="sxs-lookup"><span data-stu-id="2516e-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="2516e-121">Angiv et navn til skabelonen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="2516e-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="2516e-122">I oversigtspanelet **Tilstandsvurderingslinjer** skal du tilføje de linjer, der kræves til tilstandsvurderingen, herunder valg af den relevante tilstandstype og måleenhed.</span><span class="sxs-lookup"><span data-stu-id="2516e-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="2516e-123">Brug oversigtspanelet **Aktivtyper** til at tilføje de aktivtyper, der skal bruge skabelonen til tilstandsvurdering.</span><span class="sxs-lookup"><span data-stu-id="2516e-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="2516e-124">I felterne **Linjer** og **Aktivtyper** i gruppen **Detaljer** øverst på skærmen kan du se antallet af vurderingslinjer og aktivtyper, der er relateret til den valgte tilstandsvurderingsskabelon.</span><span class="sxs-lookup"><span data-stu-id="2516e-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="2516e-125">Oprette registrering af tilstandsvurdering på et aktiv</span><span class="sxs-lookup"><span data-stu-id="2516e-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="2516e-126">Vælg **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="2516e-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="2516e-127">På listen skal du vælge det aktiv, du vil oprette en registrering af tilstandsvurdering for.</span><span class="sxs-lookup"><span data-stu-id="2516e-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="2516e-128">Klik på **Tilstandsvurdering** under fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="2516e-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="2516e-129">Klik på **Ny** for at foretage en ny registrering.</span><span class="sxs-lookup"><span data-stu-id="2516e-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="2516e-130">Vælg datoen for tilstandsvurderingen i feltet **Dato**.</span><span class="sxs-lookup"><span data-stu-id="2516e-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="2516e-131">Vælg navnet på den arbejder, der foretog vurderingsregistreringen, i feltet **Arbejder**.</span><span class="sxs-lookup"><span data-stu-id="2516e-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="2516e-132">I feltet **Linjer** får du vist antallet af vurderingslinjer, der er konfigureret på tilstandsvurderingen.</span><span class="sxs-lookup"><span data-stu-id="2516e-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="2516e-133">Vælg en skabelon for tilstandsvurderingen i feltet **Skabelon**.</span><span class="sxs-lookup"><span data-stu-id="2516e-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="2516e-134">Navnet på skabelonen indsættes automatisk i feltet **Navn**, og de relaterede registreringslinjer indsættes i oversigtspanelet **Tilstandsvurderingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="2516e-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="2516e-135">Du kan indsætte noter vedrørende den valgte tilstandsvurdering i oversigtspanelet **Noter**.</span><span class="sxs-lookup"><span data-stu-id="2516e-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="2516e-136">For hver tilstandsvurderingslinje skal du indsætte måledata i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="2516e-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="2516e-137">Du kan indsætte en kommentar, der vedrører den valgte registreringslinje, i oversigtspanelet **Tilstandsvurderingslinjer** > feltet **Kommentarer**.</span><span class="sxs-lookup"><span data-stu-id="2516e-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="2516e-138">Hvis du tilføjer en kommentar på en linje, markeres afkrydsningsfeltet **Kommentar** automatisk.</span><span class="sxs-lookup"><span data-stu-id="2516e-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="2516e-139">Når du har foretaget en registrering af tilstandsvurdering for et aktiv, kan du udskrive en tilstandsvurderingsrapport.</span><span class="sxs-lookup"><span data-stu-id="2516e-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="2516e-140">Du kan også registrere tilstandsvurdering på en arbejdsordre (**Styring af aktiver** > **Almindeligt** > **Arbejdsordrer** > **Alle arbejdsordrer** > **Tilstandsvurdering**-knap).</span><span class="sxs-lookup"><span data-stu-id="2516e-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>
