---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (11. januar 2019)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460705"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a><span data-ttu-id="b2690-103">Nyheder eller ændringer i Dynamics 365 Talent - Core HR (11. januar 2019)</span><span class="sxs-lookup"><span data-stu-id="b2690-103">What's new or changed in Dynamics 365 Talent - Core HR (January 11, 2019)</span></span>

<span data-ttu-id="b2690-104">**Build 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="b2690-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="b2690-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.</span><span class="sxs-lookup"><span data-stu-id="b2690-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="b2690-106">Ændringer</span><span class="sxs-lookup"><span data-stu-id="b2690-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="b2690-107">Validere fraværsanmodninger ved at budgettere disponibel balance</span><span class="sxs-lookup"><span data-stu-id="b2690-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="b2690-108">Ændringer i denne version gør det muligt for medarbejdere at bede om fremtidig orlov uden at trække fra deres aktuelle saldo.</span><span class="sxs-lookup"><span data-stu-id="b2690-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="b2690-109">Standardarbejdsprocesser bruges til alle fremtidige anmodninger.</span><span class="sxs-lookup"><span data-stu-id="b2690-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="b2690-110">Du kan få flere oplysninger ved at læse [Periodisering af fravær baseret på antal arbejdstimer](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="b2690-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="b2690-111">Se budgetteret orlovssaldo i ESS og Personer</span><span class="sxs-lookup"><span data-stu-id="b2690-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="b2690-112">Med denne funktion kan personale, ledere og medarbejdere få vist saldi for fremtidige orlovsperioder.</span><span class="sxs-lookup"><span data-stu-id="b2690-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="b2690-113">Medarbejdere kan få vist fremtidige saldi i arbejdsområdet **Employee Self-Service**, og HR har adgang til de samme oplysninger ved hjælp af arbejdsområdet **Personer**.</span><span class="sxs-lookup"><span data-stu-id="b2690-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="b2690-114">Beskeder om ændring af orlovssaldi</span><span class="sxs-lookup"><span data-stu-id="b2690-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="b2690-115">Orlovssaldi viser den aktuelle saldo for medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="b2690-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="b2690-116">Fremtidige saldi kan ses i arbejdsområderne **Employee Self-Service** og **Personer** ved at angive en "pr. dato" til beregning af den budgetterede balance.</span><span class="sxs-lookup"><span data-stu-id="b2690-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="b2690-117">Navigation til visning af budgetterede saldi er blevet tilføjet i følgende områder:</span><span class="sxs-lookup"><span data-stu-id="b2690-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="b2690-118">**Fridage**-kort i arbejdsområdet **Employee Self-Service**.</span><span class="sxs-lookup"><span data-stu-id="b2690-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="b2690-119">**Orlov og fravær**-kort i arbejdsområdet **Chefselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="b2690-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="b2690-120">**Orlov og fravær**-siden i arbejdsområdet **Personer**.</span><span class="sxs-lookup"><span data-stu-id="b2690-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="b2690-121">Tillade decimaler i planer for variabel kompensation (kontantplaner)</span><span class="sxs-lookup"><span data-stu-id="b2690-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="b2690-122">Variable kontantbonusser og -planer har nu den ekstra fleksibilitet for beløb og tilsidesættelser for værdier med decimale beløb.</span><span class="sxs-lookup"><span data-stu-id="b2690-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="b2690-123">Datoerne i Tilmelding til variabel kompensation, kan ikke ændres, når planen er gemt.</span><span class="sxs-lookup"><span data-stu-id="b2690-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="b2690-124">Denne ændring giver mulighed for at opdatere slutdatoen for planen kan (udvidet eller udløbet), når planen er blevet gemt.</span><span class="sxs-lookup"><span data-stu-id="b2690-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="b2690-125">Du kan stadig aktivere eller deaktivere planer, uafhængigt af start- og slutdatoer.</span><span class="sxs-lookup"><span data-stu-id="b2690-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="b2690-126">Lønoplysninger, der er tilgængelige for den, der er tildelt sikkerhedsrollen lønadministrator</span><span class="sxs-lookup"><span data-stu-id="b2690-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="b2690-127">Rollen Lønadministrator er blevet opdateret, så der er adgang til lønoplysninger under anmodningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="b2690-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="b2690-128">Medarbejderselvbetjening | Stillingshierarki-detailudledning fra felt kan ikke hente overordnet node</span><span class="sxs-lookup"><span data-stu-id="b2690-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="b2690-129">Der er foretaget ændringer for at fjerne en fejl, der opstår, når du tilføjer stillingshierarkiet til nye arbejdsområder og navigerer i organisationsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="b2690-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="b2690-130">Ny valideringsmeddelelse, når personalenummerserie er i brug</span><span class="sxs-lookup"><span data-stu-id="b2690-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="b2690-131">Der er foretaget en ændring for at præcisere, hvad problemet er, når du ansætter en medarbejder, og det næste personalenummer er i brug.</span><span class="sxs-lookup"><span data-stu-id="b2690-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="b2690-132">Arbejdsområdet til medarbejderselvbetjening valgt som startside</span><span class="sxs-lookup"><span data-stu-id="b2690-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="b2690-133">Når arbejdsområdet **Medarbejderselvbetjening** indledningsvis vælges som startside for en bruger, og brugeren ikke er tildelt medarbejderrollen, omdirigerer systemet til standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="b2690-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="b2690-134">Årsagskode for fratrædelse opdaterer stillingstildelingspost</span><span class="sxs-lookup"><span data-stu-id="b2690-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="b2690-135">Årsagskoden for fratrædelse opdaterer nu stillingstildelingen, når du afskediger en medarbejder og afslutter stillingen.</span><span class="sxs-lookup"><span data-stu-id="b2690-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
