---
title: "Angive personaleparametre (HR) på tværs af juridiske enheder"
description: "Du skal konfigurere delte parametre for poster, der deles på tværs af virksomheder, herunder stillingsposter. I denne artikel beskrives det, hvordan du kan bruge personaleparametre på tværs af juridiske enheder."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: cc5acf7ba1b350ee2c91923c7de3b4780385f3ef
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a><span data-ttu-id="002a5-104">Angive personaleparametre (HR) på tværs af juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="002a5-104">Set up Human resources (HR) parameters across legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="002a5-105">Du skal konfigurere delte parametre for poster, der deles på tværs af virksomheder, herunder stillingsposter.</span><span class="sxs-lookup"><span data-stu-id="002a5-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="002a5-106">I denne artikel beskrives det, hvordan du kan bruge personaleparametre på tværs af juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="002a5-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="002a5-107">Visse typer poster, f.eks. stillingsposter, deles på tværs af firmaer.</span><span class="sxs-lookup"><span data-stu-id="002a5-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="002a5-108">Du skal konfigurere delte parametre for disse poster.</span><span class="sxs-lookup"><span data-stu-id="002a5-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="002a5-109">Du kan f.eks. bruge siden **Delte parametre for personale** for at konfigurere personaleparametre på tværs af juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="002a5-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="002a5-110">På siden **Delte parametre for personale** er parametrene grupperet i områder, baseret på deres funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="002a5-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="002a5-111">Tidligere frigiven funktionalitet</span><span class="sxs-lookup"><span data-stu-id="002a5-111">Previously released functionality</span></span>
<span data-ttu-id="002a5-112">På fanen **Identifikation** skal du vælge de identifikationstyper, der repræsenterer de identifikationsnumre, der er angivet på siden.</span><span class="sxs-lookup"><span data-stu-id="002a5-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="002a5-113">Før du kan angive identifikationsoplysninger om arbejderne, skal du konfigurere identifikationstyper.</span><span class="sxs-lookup"><span data-stu-id="002a5-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="002a5-114">Oplysninger om CPR-nummer, nationalt id-nummer, ID for udlænding og personlige id-kode vedligeholdes på siden **Identifikationstype**.</span><span class="sxs-lookup"><span data-stu-id="002a5-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="002a5-115">Hvis du vil definere en ny identifikationstype eller gennemse listen over eksisterende typer, skal du klikke på **Personalestyring** &gt; **fanen Links** &gt; **Konfiguration** &gt; **Identifikationstyper**.</span><span class="sxs-lookup"><span data-stu-id="002a5-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="002a5-116">Du kan indtaste en simpel kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="002a5-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="002a5-117">Hvis du bruger Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="002a5-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="002a5-118">På fanen **Identifikation** skal du vælge de identifikationstyper, der repræsenterer de identifikationsnumre, der er angivet på siden.</span><span class="sxs-lookup"><span data-stu-id="002a5-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="002a5-119">Før du kan angive identifikationsoplysninger om arbejderne, skal du konfigurere identifikationstyper.</span><span class="sxs-lookup"><span data-stu-id="002a5-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="002a5-120">Oplysninger om CPR-nummer, nationalt id-nummer, ID for udlænding og personlige id-kode vedligeholdes på siden **Identifikationstype**.</span><span class="sxs-lookup"><span data-stu-id="002a5-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="002a5-121">Hvis du vil definere en ny identifikationstype, eller gennemse listen over eksisterende typer, skal du klikke på **Personale** &gt; **Opsætning** &gt; **Identifikationstyper**.</span><span class="sxs-lookup"><span data-stu-id="002a5-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="002a5-122">Du kan indtaste en simpel kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="002a5-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="002a5-123">På fanen **Nummerserier** kan du vælge den nummerserie, der bruges til følgende poster: personalenummer, stilling, Id for brugeranmodning, I-9-dokument, ansøger, diskussion, Frynsegode-id og personalehandling (hvis denne posttype er aktiveret).</span><span class="sxs-lookup"><span data-stu-id="002a5-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="002a5-124">Brug listesiden **Nummerserier**, hvis du vil vedligeholde nummerseriereferencer og -koder.</span><span class="sxs-lookup"><span data-stu-id="002a5-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="002a5-125">Brug sidesøgefunktionen for at finde denne side.</span><span class="sxs-lookup"><span data-stu-id="002a5-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="002a5-126">På fanen **Stillinger** skal du angive, om nye stillinger er tilgængelige for tildeling som standard:</span><span class="sxs-lookup"><span data-stu-id="002a5-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="002a5-127">**Altid** – Du kan tildele arbejdere til nye stillinger, når stillingerne oprettes.</span><span class="sxs-lookup"><span data-stu-id="002a5-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="002a5-128">Når der oprettes stillinger, angives dato og klokkeslæt for **Tilgængelig for tildeling** under fanen **Generelt** på siden **Stilling** automatisk til oprettelsesdatoen og -klokkeslættet.</span><span class="sxs-lookup"><span data-stu-id="002a5-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="002a5-129">**Aldrig** – Du kan ikke tildele arbejdere til nye stillinger, når stillingerne oprettes.</span><span class="sxs-lookup"><span data-stu-id="002a5-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="002a5-130">Hvis du vælger denne indstilling, skal du åbne siden **Stilling** for hver ny stilling, når den bliver tilgængelig, og derefter, på fanen **Generelt**, angive datoen **Tilgængelig for tildeling** for at aktivere arbejdertildeling.</span><span class="sxs-lookup"><span data-stu-id="002a5-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="002a5-131">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="002a5-131">Additional resources</span></span>
--------

[<span data-ttu-id="002a5-132">Oprette firmaspecifikke parametre for personale</span><span class="sxs-lookup"><span data-stu-id="002a5-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)




