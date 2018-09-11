--- 
title: "Angive ansøger og ansøgningsdata manuelt"
description: "Denne fremgangsmåde viser, hvordan du manuelt vedligeholder oplysninger om ansøgere og deres ansøgninger."
author: kherr75
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 27f9c43f517e85a6196beed3165680cf5a6185ca
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="f345e-103">Angive ansøger og ansøgningsdata manuelt</span><span class="sxs-lookup"><span data-stu-id="f345e-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f345e-104">Denne fremgangsmåde viser, hvordan du manuelt vedligeholder oplysninger om ansøgere og deres ansøgninger.</span><span class="sxs-lookup"><span data-stu-id="f345e-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="f345e-105">Du kan angive og vedligeholde personlige oplysninger, dato og klokkeslæt for jobsamtaler, referencer, kompetencer og tilpasningsanmodninger for ansøgere.</span><span class="sxs-lookup"><span data-stu-id="f345e-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="f345e-106">Du kan også opdatere status for ansøgernes jobansøgninger og oprette breve eller e-mailmeddelelser for at kommunikere med ansøgerne.</span><span class="sxs-lookup"><span data-stu-id="f345e-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="f345e-107">Når du opretter en ansøgningspost, oprettes en personpost for ansøgeren i det globale adressekartotek.</span><span class="sxs-lookup"><span data-stu-id="f345e-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="f345e-108">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="f345e-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="f345e-109">Opret en ny ansøgerpost</span><span class="sxs-lookup"><span data-stu-id="f345e-109">Create a new applicant record</span></span>
1. <span data-ttu-id="f345e-110">Gå til Personale > Rekruttering > Ansøgere > Ansøgere.</span><span class="sxs-lookup"><span data-stu-id="f345e-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="f345e-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f345e-111">Click New.</span></span>
3. <span data-ttu-id="f345e-112">Skriv en værdi i feltet Fornavn.</span><span class="sxs-lookup"><span data-stu-id="f345e-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="f345e-113">Indtast en værdi i feltet Efternavn.</span><span class="sxs-lookup"><span data-stu-id="f345e-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="f345e-114">Hvis de er tilgængelige, kan du angive yderligere oplysninger om ansøger.</span><span class="sxs-lookup"><span data-stu-id="f345e-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="f345e-115">Oplysningerne kan omfatte ansøgerens højeste grad, aktuelle stilling eller tidligere arbejdsgiver.</span><span class="sxs-lookup"><span data-stu-id="f345e-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="f345e-116">Slå udvidelsen af sektionen Kontaktoplysninger til/fra.</span><span class="sxs-lookup"><span data-stu-id="f345e-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="f345e-117">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f345e-117">Click Add.</span></span>
7. <span data-ttu-id="f345e-118">Skriv "Kommunikations-e-mail" i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f345e-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="f345e-119">Vælg en indstilling i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="f345e-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="f345e-120">Skriv en værdi i feltet Kontaktpersons nummer/adresse.</span><span class="sxs-lookup"><span data-stu-id="f345e-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="f345e-121">Denne e-mailadresse bruges til at generere e-mailkommunikation med ansøgeren.</span><span class="sxs-lookup"><span data-stu-id="f345e-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="f345e-122">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f345e-122">Click Add.</span></span>
11. <span data-ttu-id="f345e-123">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f345e-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="f345e-124">Skriv en værdi i feltet Kontaktpersons nummer/adresse.</span><span class="sxs-lookup"><span data-stu-id="f345e-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="f345e-125">Ansøgers personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="f345e-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="f345e-126">Du kan angive yderligere personlige oplysninger om ansøgeren, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="f345e-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="f345e-127">Dette kan for eksempel omfatte fødselsdato, etnisk oprindelse, køn eller ægteskabelige status.</span><span class="sxs-lookup"><span data-stu-id="f345e-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="f345e-128">Klik på knappen Kompetencer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f345e-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="f345e-129">Du kan angive ansøgerens kompetenceprofil, herunder kvalifikationer, erhvervserfaring, uddannelse, prøver eller certifikater.</span><span class="sxs-lookup"><span data-stu-id="f345e-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="f345e-130">Disse oplysninger kan bruges til at knytte ansøgerens færdigheder til de færdigheder, der er knyttet til de job, der er defineret i firmaets data.</span><span class="sxs-lookup"><span data-stu-id="f345e-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="f345e-131">Opret en ansøgning for ansøgeren</span><span class="sxs-lookup"><span data-stu-id="f345e-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="f345e-132">Klik på Ansøgninger.</span><span class="sxs-lookup"><span data-stu-id="f345e-132">Click Applications.</span></span>
2. <span data-ttu-id="f345e-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f345e-133">Click New.</span></span>
3. <span data-ttu-id="f345e-134">Klik på rullelisten i feltet Rekrutteringsprojekt for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="f345e-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f345e-135">Ved at vælge et rekrutteringsprojekt, knyttes ansøgeren til en bestemt åbning, der er inkluderet i dette rekrutteringsprojekt.</span><span class="sxs-lookup"><span data-stu-id="f345e-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="f345e-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f345e-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f345e-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f345e-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f345e-138">Som standard er job og afdeling baseret på det valgte rekrutteringsprojekt.</span><span class="sxs-lookup"><span data-stu-id="f345e-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="f345e-139">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f345e-139">Click Save.</span></span>
    * <span data-ttu-id="f345e-140">Når du har gemt ansøgningen, kan du knytte dokumenter til den, herunder ansøgerens erfaring, priser og følgebrev.</span><span class="sxs-lookup"><span data-stu-id="f345e-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  


