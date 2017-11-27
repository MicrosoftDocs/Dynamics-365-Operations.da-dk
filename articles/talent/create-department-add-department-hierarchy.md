---
title: Oprette en afdeling og knytte den til afdelingshierarkiet
description: "En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation. En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale. Du kan bruge afdelinger til at rapportere om funktionsområder. Afdelinger kan have ansvar for driftsregnskabet."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cea3ecd66a57780c9ef1b3a3c21f1e5273faa0ef
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a><span data-ttu-id="46489-106">Oprette en afdeling og knytte den til afdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="46489-106">Create a department and associate it with the department hierarchy</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="46489-107">En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation.</span><span class="sxs-lookup"><span data-stu-id="46489-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="46489-108">En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale.</span><span class="sxs-lookup"><span data-stu-id="46489-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="46489-109">Du kan bruge afdelinger til at rapportere om funktionsområder.</span><span class="sxs-lookup"><span data-stu-id="46489-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="46489-110">Afdelinger kan have ansvar for driftsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="46489-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="46489-111">En afdeling kan også omfatte en gruppe af bærere.</span><span class="sxs-lookup"><span data-stu-id="46489-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="46489-112">Stillinger kan tildeles til afdelinger.</span><span class="sxs-lookup"><span data-stu-id="46489-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="46489-113">For at oprette en afdeling skal du klikke på **Personale** &gt; **Afdelinger** &gt; **Afdeling**.</span><span class="sxs-lookup"><span data-stu-id="46489-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="46489-114">I følgende tabel forklares de felter, der er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="46489-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="46489-115">Felt</span><span class="sxs-lookup"><span data-stu-id="46489-115">Field</span></span>               | <span data-ttu-id="46489-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="46489-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46489-117">Navn</span><span class="sxs-lookup"><span data-stu-id="46489-117">Name</span></span>                | <span data-ttu-id="46489-118">Angiv et navn for afdelingen.</span><span class="sxs-lookup"><span data-stu-id="46489-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="46489-119">Afdelingsnummer</span><span class="sxs-lookup"><span data-stu-id="46489-119">Department number</span></span>   | <span data-ttu-id="46489-120">Der kan automatisk genereres en standardværdi, hvis der er knyttet en nummerseriekode til referencen for **Organisationsnummer** på siden **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="46489-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="46489-121">Søgenavn</span><span class="sxs-lookup"><span data-stu-id="46489-121">Search name</span></span>         | <span data-ttu-id="46489-122">Angiv et navn eller et akronym, der kan bruges til en hurtig søgning efter afdelingen.</span><span class="sxs-lookup"><span data-stu-id="46489-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="46489-123">Notat</span><span class="sxs-lookup"><span data-stu-id="46489-123">Memo</span></span>                | <span data-ttu-id="46489-124">Angiv yderligere oplysninger her.</span><span class="sxs-lookup"><span data-stu-id="46489-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="46489-125">I hierarki</span><span class="sxs-lookup"><span data-stu-id="46489-125">In hierarchy</span></span>        | <span data-ttu-id="46489-126">Et markeret afkrydsningsfelt angiver, at en afdeling er medtaget i afdelingshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="46489-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="46489-127">Du kan finde oplysninger om, hvordan du føjer en afdeling til afdelingshierarkiet senere i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="46489-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="46489-128">DUNS-nummer</span><span class="sxs-lookup"><span data-stu-id="46489-128">DUNS number</span></span>         | <span data-ttu-id="46489-129">DUNS står for Data Universal Number System.</span><span class="sxs-lookup"><span data-stu-id="46489-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="46489-130">Dette er et 9-cifret tal, der er udstedt af Dun & Bradstreet.</span><span class="sxs-lookup"><span data-stu-id="46489-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="46489-131">Leder</span><span class="sxs-lookup"><span data-stu-id="46489-131">Manager</span></span>             | <span data-ttu-id="46489-132">Angiv den karakter, der administrerer afdelingen.</span><span class="sxs-lookup"><span data-stu-id="46489-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="46489-133">Adresser</span><span class="sxs-lookup"><span data-stu-id="46489-133">Addresses</span></span>           | <span data-ttu-id="46489-134">Tilføj afdelingens adresseoplysninger.</span><span class="sxs-lookup"><span data-stu-id="46489-134">Add the address information for the department.</span></span> <span data-ttu-id="46489-135">Tilføj f.eks. postadressen for den bygning, som afdelingen findes i.</span><span class="sxs-lookup"><span data-stu-id="46489-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="46489-136">Kontaktoplysninger</span><span class="sxs-lookup"><span data-stu-id="46489-136">Contact information</span></span> | <span data-ttu-id="46489-137">Tilføj kontaktoplysninger afdelingen.</span><span class="sxs-lookup"><span data-stu-id="46489-137">Add contact information for the department.</span></span> <span data-ttu-id="46489-138">Du kan f.eks. føje et telefonnummer til afdelingens helpdesk.</span><span class="sxs-lookup"><span data-stu-id="46489-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="46489-139">Følg disse trin for at føje en afdeling til afdelingshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="46489-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="46489-140">Klik på **Personale** &gt; **Afdelinger** &gt; **Afdelingshierarki**.</span><span class="sxs-lookup"><span data-stu-id="46489-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="46489-141">Klik på **Rediger**, og vælg derefter den organisation, som afdelingen skal være under.</span><span class="sxs-lookup"><span data-stu-id="46489-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="46489-142">Klik på **Indsæt**, og vælg **Afdeling** på listen.</span><span class="sxs-lookup"><span data-stu-id="46489-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="46489-143">På listen over afdelinger, der vises, skal du vælge afdelingen til at føje den til hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="46489-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="46489-144">Gem ændringerne.</span><span class="sxs-lookup"><span data-stu-id="46489-144">Save your changes.</span></span> <span data-ttu-id="46489-145">Du modtager en meddelelse om, at der er oprettet en kladdeversion af hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="46489-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="46489-146">Når du er klar, skal du klikke på **Udgiv** i hierarkidesigner.</span><span class="sxs-lookup"><span data-stu-id="46489-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="46489-147">Du kan angive en ikrafttrædelsesdato, der angiver, hvornår hierarkiet skal offentliggøres.</span><span class="sxs-lookup"><span data-stu-id="46489-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="46489-148">Hvis du f.eks. vil tilføje en ny afdeling i starten af næste kalenderår, skal du sætte ikrafttrædelsesdatoen til 1. januar i det nye kalenderår.</span><span class="sxs-lookup"><span data-stu-id="46489-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="46489-149">Ændringer af hierarkiet træder i kraft på denne dato.</span><span class="sxs-lookup"><span data-stu-id="46489-149">The changes to the hierarchy will take effect on that date.</span></span>





