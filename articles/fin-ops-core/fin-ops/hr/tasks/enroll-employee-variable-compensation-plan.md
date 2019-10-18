---
title: Melde en medarbejder til en variabel lønstruktur
description: Chefen for kompensation og frynsegoder kan tilmelde medarbejdere til planer for variabel kompensation for at beregne bonusser i naturalier eller kontanter for medarbejdere.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d120f8bb52252956d75178d2ffac6ab632385e00
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177078"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="8a77a-103">Melde en medarbejder til en variabel lønstruktur</span><span class="sxs-lookup"><span data-stu-id="8a77a-103">Enroll an employee in a variable compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a77a-104">Chefen for kompensation og frynsegoder kan tilmelde medarbejdere til planer for variabel kompensation for at beregne bonusser i naturalier eller kontanter for medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="8a77a-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="8a77a-105">Denne procedure forudsætter, at en variabel kompensationsstruktur er blevet oprettet med feltet Aktiver tilmelding angivet til Ja, og at berettigelsesregler er oprettet for den variable kompensationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="8a77a-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="8a77a-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="8a77a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8a77a-107">Du begynder denne procedure ved at gå til Personale > Arbejdere > Medarbejdere > Kompensation > Tilmelding til variabel plan</span><span class="sxs-lookup"><span data-stu-id="8a77a-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="8a77a-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8a77a-108">Click New.</span></span>
2. <span data-ttu-id="8a77a-109">Klik på rullelisten i feltet Plan for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="8a77a-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8a77a-110">Opslaget Plan filtreres til kun at vise de planer for variabel kompensation, som medarbejderen er berettiget til, baseret på Berettigelsesregler.</span><span class="sxs-lookup"><span data-stu-id="8a77a-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="8a77a-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="8a77a-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8a77a-112">Slå udvidelsen af sektionen Generelt til/fra.</span><span class="sxs-lookup"><span data-stu-id="8a77a-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="8a77a-113">Angiv en dato i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="8a77a-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="8a77a-114">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="8a77a-114">Click Save.</span></span>
7. <span data-ttu-id="8a77a-115">Slå udvidelsen af sektionen Tilsidesættelser til/fra.</span><span class="sxs-lookup"><span data-stu-id="8a77a-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="8a77a-116">Eventuelt kan en dato for ansættelsesregel indstilles til at tilsidesætte medarbejderens ansættelsesdato, hvis ansættelsesreglen, der er angivet for den valgte variable struktur, er i Procent.</span><span class="sxs-lookup"><span data-stu-id="8a77a-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="8a77a-117">Hvis den variable struktur er en procentdel af den grundlæggende struktur, kan bonusprocenten tilsidesættes for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="8a77a-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="8a77a-118">Hvis den variable kompensationsstruktur er et antal enheder på plan, kan antallet af enheder tilsidesættes for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="8a77a-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="8a77a-119">Hvis medarbejderen skal modtage et fladt beløb som bonus, kan du angive beløbet her.</span><span class="sxs-lookup"><span data-stu-id="8a77a-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="8a77a-120">Slå udvidelse af sektionen Organisationsmæssige overstyringer til eller fra.</span><span class="sxs-lookup"><span data-stu-id="8a77a-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="8a77a-121">Hvis medarbejderens præstation skal tages i betragtning, præstationen i forskellige afdelinger eller en anden afdeling end den, der er tildelt på medarbejderens stilling, kan afdelingen tilsidesættes.</span><span class="sxs-lookup"><span data-stu-id="8a77a-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="8a77a-122">Kolonnen Procent bør i alt være 100.</span><span class="sxs-lookup"><span data-stu-id="8a77a-122">The Percent column should total 100.</span></span>  

