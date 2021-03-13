---
title: Melde en medarbejder til en variabel lønstruktur
description: Chefen for kompensation og frynsegoder kan tilmelde medarbejdere til planer for variabel kompensation for at beregne bonusser i naturalier eller kontanter for medarbejdere.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a173403e79212be5e4aac36d99f349da159e08
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111938"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="a59c6-103">Melde en medarbejder til en variabel lønstruktur</span><span class="sxs-lookup"><span data-stu-id="a59c6-103">Enroll an employee in a variable compensation plan</span></span>

<span data-ttu-id="a59c6-104">Chefen for kompensation og frynsegoder kan tilmelde medarbejdere til planer for variabel kompensation for at beregne bonusser i naturalier eller kontanter for medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="a59c6-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="a59c6-105">Denne procedure forudsætter, at en variabel kompensationsstruktur er blevet oprettet med feltet Aktiver tilmelding angivet til Ja, og at berettigelsesregler er oprettet for den variable kompensationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="a59c6-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="a59c6-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="a59c6-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a59c6-107">Du begynder denne procedure ved at gå til Human Resources > Arbejdere > Medarbejdere > Kompensation > Tilmelding til variabel plan</span><span class="sxs-lookup"><span data-stu-id="a59c6-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="a59c6-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a59c6-108">Click New.</span></span>
2. <span data-ttu-id="a59c6-109">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a59c6-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a59c6-110">Opslaget Plan filtreres til kun at vise de planer for variabel kompensation, som medarbejderen er berettiget til, baseret på Berettigelsesregler.</span><span class="sxs-lookup"><span data-stu-id="a59c6-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="a59c6-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a59c6-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a59c6-112">Slå udvidelsen af sektionen Generelt til/fra.</span><span class="sxs-lookup"><span data-stu-id="a59c6-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="a59c6-113">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="a59c6-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="a59c6-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a59c6-114">Click Save.</span></span>
7. <span data-ttu-id="a59c6-115">Slå udvidelsen af sektionen Tilsidesættelser til/fra.</span><span class="sxs-lookup"><span data-stu-id="a59c6-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="a59c6-116">Eventuelt kan en dato for ansættelsesregel indstilles til at tilsidesætte medarbejderens ansættelsesdato, hvis ansættelsesreglen, der er angivet for den valgte variable struktur, er i Procent.</span><span class="sxs-lookup"><span data-stu-id="a59c6-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="a59c6-117">Hvis den variable struktur er en procentdel af den grundlæggende struktur, kan bonusprocenten tilsidesættes for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="a59c6-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="a59c6-118">Hvis den variable kompensationsstruktur er et antal enheder på plan, kan antallet af enheder tilsidesættes for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="a59c6-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="a59c6-119">Hvis medarbejderen skal modtage et fladt beløb som bonus, kan du angive beløbet her.</span><span class="sxs-lookup"><span data-stu-id="a59c6-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="a59c6-120">Slå udvidelse af sektionen Organisationsmæssige overstyringer til eller fra.</span><span class="sxs-lookup"><span data-stu-id="a59c6-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="a59c6-121">Hvis medarbejderens præstation skal tages i betragtning, præstationen i forskellige afdelinger eller en anden afdeling end den, der er tildelt på medarbejderens stilling, kan afdelingen tilsidesættes.</span><span class="sxs-lookup"><span data-stu-id="a59c6-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="a59c6-122">Kolonnen Procent bør i alt være 100.</span><span class="sxs-lookup"><span data-stu-id="a59c6-122">The Percent column should total 100.</span></span>  

