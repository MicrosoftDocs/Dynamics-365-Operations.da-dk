--- 
title: "Melde en medarbejder til en variabel lønstruktur"
description: Chefen for kompensation og frynsegoder kan tilmelde medarbejdere til planer for variabel kompensation for at beregne bonusser i naturalier eller kontanter for medarbejdere.
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: eb162e22276fc19cf11999380d551b29ba6a6d45
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="9bfdc-103">Melde en medarbejder til en variabel lønstruktur</span><span class="sxs-lookup"><span data-stu-id="9bfdc-103">Enroll an employee in a variable compensation plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9bfdc-104">Chefen for kompensation og frynsegoder kan tilmelde medarbejdere til planer for variabel kompensation for at beregne bonusser i naturalier eller kontanter for medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-104">The Compensation and Benefits manager can enrol employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="9bfdc-105">Denne procedure forudsætter, at en variabel kompensationsstruktur er blevet oprettet med feltet Aktiver tilmelding angivet til Ja, og at berettigelsesregler er oprettet for den variable kompensationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="9bfdc-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9bfdc-107">Du begynder denne procedure ved at gå til Personale > Arbejdere > Medarbejdere > Kompensation > Tilmelding til variabel plan</span><span class="sxs-lookup"><span data-stu-id="9bfdc-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="9bfdc-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-108">Click New.</span></span>
2. <span data-ttu-id="9bfdc-109">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9bfdc-110">Opslaget Plan filtreres til kun at vise de planer for variabel kompensation, som medarbejderen er berettiget til, baseret på Berettigelsesregler.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="9bfdc-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9bfdc-112">Slå udvidelsen af sektionen Generelt til/fra.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="9bfdc-113">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="9bfdc-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-114">Click Save.</span></span>
7. <span data-ttu-id="9bfdc-115">Slå udvidelsen af sektionen Tilsidesættelser til/fra.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="9bfdc-116">Eventuelt kan en dato for ansættelsesregel indstilles til at tilsidesætte medarbejderens ansættelsesdato, hvis ansættelsesreglen, der er angivet for den valgte variable struktur, er i Procent.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="9bfdc-117">Hvis den variable struktur er en procentdel af den grundlæggende struktur, kan bonusprocenten tilsidesættes for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="9bfdc-118">Hvis den variable kompensationsstruktur er et antal enheder på plan, kan antallet af enheder tilsidesættes for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="9bfdc-119">Hvis medarbejderen skal modtage et fladt beløb som bonus, kan du angive beløbet her.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="9bfdc-120">Slå udvidelse af sektionen Organisationsmæssige overstyringer til eller fra.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="9bfdc-121">Hvis medarbejderens præstation skal tages i betragtning, præstationen i forskellige afdelinger eller en anden afdeling end den, der er tildelt på medarbejderens stilling, kan afdelingen tilsidesættes.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="9bfdc-122">Kolonnen Procent bør i alt være 100.</span><span class="sxs-lookup"><span data-stu-id="9bfdc-122">The Percent column should total 100.</span></span>  


