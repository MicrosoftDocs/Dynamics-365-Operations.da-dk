---
title: Foretage fejlfinding af problemer under den første synkronisering
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172708"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="315d6-103">Foretage fejlfinding af problemer under den første synkronisering</span><span class="sxs-lookup"><span data-stu-id="315d6-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="315d6-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="315d6-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="315d6-105">Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="315d6-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="315d6-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="315d6-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="315d6-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="315d6-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="315d6-108">Kontrollere, om der er fejl i første synkronisering i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="315d6-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="315d6-109">Når du har aktiveret tilknytningsskabelonerne, skal status for tilknytningerne være **Kører**.</span><span class="sxs-lookup"><span data-stu-id="315d6-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="315d6-110">Hvis status er **Kører ikke**, er der opstået fejl under den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="315d6-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="315d6-111">Hvis du vil have vist fejlene, skal du vælge fanen **Oplysninger om første synkronisering** på siden **Dobbeltskrivning**.</span><span class="sxs-lookup"><span data-stu-id="315d6-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Fanen Oplysninger om første synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="315d6-113">Du kan ikke fuldføre den første synkronisering: 400 ugyldig anmodning</span><span class="sxs-lookup"><span data-stu-id="315d6-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="315d6-114">**Påkrævet rolle for at rette fejlen:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="315d6-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="315d6-115">Du kan få vist følgende fejlmeddelelse, når du forsøger at køre tilknytningen og den første synkronisering:</span><span class="sxs-lookup"><span data-stu-id="315d6-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="315d6-116">*Fjernserveren returnerede en fejl: (400) ugyldig anmodning. AX-eksport registrerede en fejl*</span><span class="sxs-lookup"><span data-stu-id="315d6-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="315d6-117">Her er et eksempel på den fulde fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="315d6-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="315d6-118">Hvis denne fejl opstår konsekvent, og du ikke kan fuldføre den første synkronisering, skal du følge disse trin for at løse problemet.</span><span class="sxs-lookup"><span data-stu-id="315d6-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="315d6-119">Log på den virtuelle maskine (VM) for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="315d6-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="315d6-120">Åbn Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="315d6-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="315d6-121">I ruden **Services** skal du sikre dig, at Microsoft Dynamics 365 Dataimport/eksportstruktur-tjenesten kører.</span><span class="sxs-lookup"><span data-stu-id="315d6-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="315d6-122">Genstart, hvis den er stoppet, fordi den første synkronisering kræver det.</span><span class="sxs-lookup"><span data-stu-id="315d6-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="315d6-123">Fejl under første synkronisering: 403 forbudt</span><span class="sxs-lookup"><span data-stu-id="315d6-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="315d6-124">Du kan få vist følgende fejlmeddelelse under første synkronisering:</span><span class="sxs-lookup"><span data-stu-id="315d6-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="315d6-125">*(\[Forbudt\], Fjernserveren returnerede en fejl: (403) forbudt.), AX-eksport registrerede en fejl*</span><span class="sxs-lookup"><span data-stu-id="315d6-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="315d6-126">Følg disse trin for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="315d6-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="315d6-127">Log på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="315d6-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="315d6-128">Slet **DtAppID**-klienten på siden **Azure Active Directory-programmer**, og tilføj den derefter igen.</span><span class="sxs-lookup"><span data-stu-id="315d6-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Liste over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="315d6-130">Selvreferencefejl under første synkronisering</span><span class="sxs-lookup"><span data-stu-id="315d6-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="315d6-131">Du kan få vist en fejlmeddelelse, der minder om følgende, hvis nogen af dine tilknytninger har selvreferencer:</span><span class="sxs-lookup"><span data-stu-id="315d6-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="315d6-132">*I forbindelse med Kreditor V2 vises følgende fejlmeddelelse: Post-id: ny post, ErrorMessage: Det var ikke muligt at fortolke GUID'et for feltet: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Opslagsværdien blev ikke fundet: CN-001. Prøv følgende URL-adresse(r) for at se, om referencedataene findes: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="315d6-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="315d6-133">Denne type fejl opstår ved første synkronisering af tilknytninger, der har selvreferencer.</span><span class="sxs-lookup"><span data-stu-id="315d6-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="315d6-134">I det foregående eksempel refererer feltet fakturakonto til kreditorenheden.</span><span class="sxs-lookup"><span data-stu-id="315d6-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="315d6-135">Hvis du vil løse problemet, skal du muligvis køre tilknytningen to gange, før den første synkronisering lykkes.</span><span class="sxs-lookup"><span data-stu-id="315d6-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

