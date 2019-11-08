---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (23. januar 2019)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 3c7a389ef4a651135836ce682d7cda95c536011a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550199"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-23-2019"></a><span data-ttu-id="2e418-103">Nyheder eller ændringer i Dynamics 365 Talent - Core HR (23. januar 2019)</span><span class="sxs-lookup"><span data-stu-id="2e418-103">What's new or changed in Dynamics 365 Talent - Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2e418-104">**Build 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="2e418-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="2e418-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.</span><span class="sxs-lookup"><span data-stu-id="2e418-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="2e418-106">Ændringer</span><span class="sxs-lookup"><span data-stu-id="2e418-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="2e418-107">Import af fast løn for medarbejdere fungerer ikke, når du opretter nye poster for fast løn</span><span class="sxs-lookup"><span data-stu-id="2e418-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="2e418-108">Er der foretaget en ændring af den enhed for fast løn til medarbejdere, så kompensationsniveauet hentes ved import.</span><span class="sxs-lookup"><span data-stu-id="2e418-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="2e418-109">Før denne version blev der vist en meddelelse, som angav, at niveauet var påkrævet.</span><span class="sxs-lookup"><span data-stu-id="2e418-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="2e418-110">Fjerne feltet med minimumsaldo fra dialogboksen til anmodning om fridag</span><span class="sxs-lookup"><span data-stu-id="2e418-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="2e418-111">Feltet **Mindste saldo** er blevet fjernet fra dialogboksen **Anmodning om fridage**.</span><span class="sxs-lookup"><span data-stu-id="2e418-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="2e418-112">Denne ændring påvirker alle de områder, hvor der kan anmodes om fridage.</span><span class="sxs-lookup"><span data-stu-id="2e418-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="2e418-113">Dataopgradering for kompensationsniveauer, der ikke opdateres i alle scenarier</span><span class="sxs-lookup"><span data-stu-id="2e418-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="2e418-114">Er der foretaget en ændring, der opdaterer kompensationsniveauet i planer for fast løn.</span><span class="sxs-lookup"><span data-stu-id="2e418-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="2e418-115">Denne ændring angiver en værdi for kompensationsniveauet i planer for faste løn for det job, der er tildelt til medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="2e418-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="2e418-116">Lønoplysninger på siden Administrer ændringer er kun tilgængelige, når brugeren er logget på som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="2e418-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="2e418-117">Denne ændring giver medarbejdere med rollen Lønadministrator adgang til lønoplysninger på siden **Tidslinje for ændringer > Administrere ændringer** for stillingen.</span><span class="sxs-lookup"><span data-stu-id="2e418-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="2e418-118">Jobfelter får som standard værdien stillinger</span><span class="sxs-lookup"><span data-stu-id="2e418-118">Job fields default to positions</span></span>
<span data-ttu-id="2e418-119">Når jobbet ændres for en stilling, anvendes stillingsværdien for jobfelter som standard.</span><span class="sxs-lookup"><span data-stu-id="2e418-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="2e418-120">Der vises en meddelelse med mulighed for at acceptere standardværdierne eller beholde de eksisterende værdier for disse felter.</span><span class="sxs-lookup"><span data-stu-id="2e418-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="2e418-121">Prøvetiden og kalenderen vises ikke for kommende medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="2e418-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="2e418-122">Med denne ændring er felterne **Prøvetid** og **Kalender** blevet føjet til siden **Administrer ændringer**, så kommende og tidligere medarbejdere kan indtaste data.</span><span class="sxs-lookup"><span data-stu-id="2e418-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23-for-finance-and-operations"></a><span data-ttu-id="2e418-123">Platform update 23 til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2e418-123">Platform update 23 for Finance and Operations</span></span>
<span data-ttu-id="2e418-124">Rettelser af mindre programfejl er inkluderet som en del af Platform update 23 til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2e418-124">Minor bug fixes have been included as part of Platform update 23 for Finance and Operations.</span></span> <span data-ttu-id="2e418-125">Du kan finde flere oplysninger i [Nyheder eller ændringer i Dynamics 365 Finance and Operations platformsopdatering 23 (januar 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="2e418-125">For more information, see [What's new or changed in Dynamics 365 Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
