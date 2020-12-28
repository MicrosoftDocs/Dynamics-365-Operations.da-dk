---
title: Melde en medarbejder til en fast lønplan
description: Chefen for kompensation og frynsegoder kan tildele medarbejdere faste lønplaner for at administrere deres grundløn.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3029e52a7cc1fb6dfda390f5d892c89f1eda8509
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417788"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="88b59-103">Melde en medarbejder til en fast lønplan</span><span class="sxs-lookup"><span data-stu-id="88b59-103">Enroll an employee in a fixed compensation plan</span></span>

<span data-ttu-id="88b59-104">Chefen for kompensation og frynsegoder kan tildele medarbejdere faste lønplaner for at administrere deres grundløn.</span><span class="sxs-lookup"><span data-stu-id="88b59-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="88b59-105">Denne procedure forudsætter, at en fast lønplan er blevet oprettet og er aktiv, og at der er angivet berettigelsesregler for planen.</span><span class="sxs-lookup"><span data-stu-id="88b59-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="88b59-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="88b59-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="88b59-107">Du begynder proceduren ved at gå til Personale > Arbejdere > Medarbejdere > Kompensation > Fast plan</span><span class="sxs-lookup"><span data-stu-id="88b59-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="88b59-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="88b59-108">Click New.</span></span>
2. <span data-ttu-id="88b59-109">Vælg en Fast løn-handling af typen Ansæt/genansæt for at beskrive ændringen af medarbejderens kompensation i feltet Handling.</span><span class="sxs-lookup"><span data-stu-id="88b59-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="88b59-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="88b59-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="88b59-111">Klik på rullelisten i feltet Stilling for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="88b59-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="88b59-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="88b59-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="88b59-113">Det niveau, der vises, er fra jobbets kompensationsniveau for stillingen.</span><span class="sxs-lookup"><span data-stu-id="88b59-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="88b59-114">Niveauet skal være angivet på jobbet, før kompensation kan tildeles medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="88b59-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="88b59-115">Vælg Fast løn-struktur for medarbejderen i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="88b59-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="88b59-116">Opslaget Plan er filtreret til kun at vise de planer, som medarbejderen er berettiget til, baseret på Berettigelsesregler.</span><span class="sxs-lookup"><span data-stu-id="88b59-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="88b59-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="88b59-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="88b59-118">Ikrafttrædelses- og udløbsdatoer for kompensation er standard fra start- og slutdatoer for tildeling af arbejderens stilling.</span><span class="sxs-lookup"><span data-stu-id="88b59-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="88b59-119">Du kan justere disse datoer efter behov.</span><span class="sxs-lookup"><span data-stu-id="88b59-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="88b59-120">Hvis Fast lønplan er en trinplan, skal du vælge det trin, der indeholder den korrekte lønsats for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="88b59-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="88b59-121">Hvis Fast lønplan er en omfangs- eller klasseplan, skal du angive lønsatsen for medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="88b59-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="88b59-122">Lønsatsen valideres mod toleranceindstillingerne for planen og minimale og maksimale referencepunkter for jobbets kompensationsniveau.</span><span class="sxs-lookup"><span data-stu-id="88b59-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="88b59-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="88b59-123">Click OK.</span></span>

