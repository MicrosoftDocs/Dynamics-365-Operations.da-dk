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
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410075"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="ba1b6-103">Foretage fejlfinding af problemer under den første synkronisering</span><span class="sxs-lookup"><span data-stu-id="ba1b6-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba1b6-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="ba1b6-105">Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba1b6-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="ba1b6-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="ba1b6-108">Kontrollere, om der er fejl i første synkronisering i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="ba1b6-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="ba1b6-109">Når du har aktiveret tilknytningsskabelonerne, skal status for tilknytningerne være **Kører**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="ba1b6-110">Hvis status er **Kører ikke**, er der opstået fejl under den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="ba1b6-111">Hvis du vil have vist fejlene, skal du vælge fanen **Oplysninger om første synkronisering** på siden **Dobbeltskrivning**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Fanen Oplysninger om første synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="ba1b6-113">Du kan ikke fuldføre den første synkronisering: 400 ugyldig anmodning</span><span class="sxs-lookup"><span data-stu-id="ba1b6-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="ba1b6-114">**Påkrævet rolle for at rette fejlen:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="ba1b6-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="ba1b6-115">Du kan få vist følgende fejlmeddelelse, når du forsøger at køre tilknytningen og den første synkronisering:</span><span class="sxs-lookup"><span data-stu-id="ba1b6-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="ba1b6-116">*Fjernserveren returnerede en fejl: (400) ugyldig anmodning. AX-eksport registrerede en fejl*</span><span class="sxs-lookup"><span data-stu-id="ba1b6-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="ba1b6-117">Her er et eksempel på den fulde fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="ba1b6-118">Hvis denne fejl opstår konsekvent, og du ikke kan fuldføre den første synkronisering, skal du følge disse trin for at løse problemet.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="ba1b6-119">Log på den virtuelle maskine (VM) for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="ba1b6-120">Åbn Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="ba1b6-121">I ruden **Services** skal du sikre dig, at Microsoft Dynamics 365 Dataimport/eksportstruktur-tjenesten kører.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="ba1b6-122">Genstart, hvis den er stoppet, fordi den første synkronisering kræver det.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="ba1b6-123">Fejl under første synkronisering: 403 forbudt</span><span class="sxs-lookup"><span data-stu-id="ba1b6-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="ba1b6-124">Du kan få vist følgende fejlmeddelelse under første synkronisering:</span><span class="sxs-lookup"><span data-stu-id="ba1b6-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="ba1b6-125">*(\[Forbudt\], Fjernserveren returnerede en fejl: (403) forbudt.), AX-eksport registrerede en fejl*</span><span class="sxs-lookup"><span data-stu-id="ba1b6-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="ba1b6-126">Følg disse trin for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="ba1b6-127">Log på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="ba1b6-128">Slet **DtAppID**-klienten på siden **Azure Active Directory-programmer**, og tilføj den derefter igen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Liste over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="ba1b6-130">Selvreference- eller cirkulære referencefesjl under første synkronisering</span><span class="sxs-lookup"><span data-stu-id="ba1b6-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="ba1b6-131">Du kan få vist en fejlmeddelelse, hvis nogen af dine tilknytninger har selvreferencer eller cirkulære referencer.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="ba1b6-132">Fejlene falder i disse kategorier:</span><span class="sxs-lookup"><span data-stu-id="ba1b6-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="ba1b6-133">Kreditorer V2 til msdyn_vendors med enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="ba1b6-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="ba1b6-134">Debitorer V3 til konti med enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="ba1b6-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="ba1b6-135">Løse en fejl i Kreditorer V2 til msdyn_vendors med enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="ba1b6-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="ba1b6-136">Du kan støde ind i følgende indledende synkroniseringsfejl på **Kreditorer V2** til **msdyn_vendors**-tilknytning, hvis enhederne har eksisterende poster med værdier i felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="ba1b6-137">Dette skyldes, at **InvoiceVendorAccountNumber** er et selvrefererende felt, og at **PrimaryContactPersonId** er en cirkulær reference i kreditortilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="ba1b6-138">*GUID for feltet kunne ikke fortolkes: <field>. Opslaget blev ikke fundet: <value>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$Select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="ba1b6-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="ba1b6-139">Her er et par eksempler:</span><span class="sxs-lookup"><span data-stu-id="ba1b6-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="ba1b6-140">*GUID for feltet kunne ikke fortolkes: msdyn_vendorprimarycontactperson. msdyn_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select = msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="ba1b6-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="ba1b6-141">*GUID for feltet kunne ikke fortolkes: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Opslaget blev ikke fundet: V-24-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="ba1b6-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="ba1b6-142">Hvis der er poster med værdier i disse felter i kreditorenheden, skal du følge trinnene i afsnittet nedenfor for at fuldføre den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="ba1b6-143">I Finance and Operations-appen skal du slette felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** fra tilknytningen og gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="ba1b6-144">Gå til siden dobbeltskrivning-tilknytning for **Kreditorer V2 (msdyn_vendors)**, og vælg fanen **Enhedstilknytninger**. I venstre filter skal du vælge **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="ba1b6-145">I højre filter skal du vælge **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="ba1b6-146">Søg efter **primarycontactperson** for at finde kildefeltet **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="ba1b6-147">Klik på knappen **Handlinger**, og vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![selv- eller cirkulær reference 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="ba1b6-149">Gentag for at slette feltet **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![selv- eller cirkulær reference 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="ba1b6-151">Gem ændringerne i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="ba1b6-152">Deaktiver ændringssporingen for **Kreditorer v2**-enheden.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="ba1b6-153">Naviger til **Datastyring \> Dataenheder**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="ba1b6-154">Vælg enheden **Kreditorer V2**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="ba1b6-155">Klik på **Indstillinger** på menulinjen og derefter på **Ændringssporing**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![selv- eller cirkulær reference 5](media/selfref_options.png)
    
    4. <span data-ttu-id="ba1b6-157">Klik på **Deaktiver ændringssporing**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-157">Click **Disable Change Tracking**.</span></span>
    
        ![selv- eller cirkulær reference 6](media/selfref_tracking.png)

3. <span data-ttu-id="ba1b6-159">Kør den første synkronisering af tilknytningen **Kreditorer V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="ba1b6-160">Den første synkronisering skal køres uden fejl.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="ba1b6-161">Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontaktpersoner)**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="ba1b6-162">Du skal synkronisere denne tilknytning, hvis du vil synkronisere feltet for den primære kontaktperson på kreditorenheden, når kontaktpersonposterne også skal synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="ba1b6-163">Føj felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbage til tilknytningen **Kreditorer V2 (msdyn_vendors)**, og gem tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="ba1b6-164">Kør den første synkronisering igen for tilknytningen **Kreditorer V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="ba1b6-165">Alle poster synkroniseres, fordi ændringssporing er deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="ba1b6-166">Aktivér ændringssporing for **Kreditorer V2**-enheden.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="ba1b6-167">Løse en fejl i Debitorer V3 til konti med enhedstilknytning</span><span class="sxs-lookup"><span data-stu-id="ba1b6-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="ba1b6-168">Du kan støde ind i følgende indledende synkroniseringsfejl på **Kreditorer V3** til **Konti**-tilknytningen, hvis enhederne har eksisterende poster med værdier i felterne **ContactPersonID** og **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="ba1b6-169">Dette skyldes, at **InvoiceAccount** er et selvrefererende felt, og at **ContactPersonID** er en cirkulær reference i kreditortilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="ba1b6-170">*GUID for feltet kunne ikke fortolkes: <field>. Opslaget blev ikke fundet: <value>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$Select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="ba1b6-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="ba1b6-171">*GUID for feltet kunne ikke fortolkes: primarycontactid.msdyn_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="ba1b6-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="ba1b6-172">*GUID for feltet kunne ikke fortolkes: msdyn_billingaccount.accountnumber. Opslaget blev ikke fundet: 1206-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="ba1b6-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="ba1b6-173">Hvis der er poster med værdier i disse felter i debitorenheden, skal du følge trinnene i afsnittet nedenfor for at fuldføre den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="ba1b6-174">Du kan bruge denne fremgangsmåde til alle out-of-the-box-enhederne, f.eks. Konti og Kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="ba1b6-175">I Finance and Operations-appen skal du slette felterne **ContactPersonID** og **InvoiceAccount** fra tilknytningen **Debitorer V3 (konti)** og gemme tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="ba1b6-176">Gå til siden dobbeltskrivning-tilknytning for **Debitorer V3 (konti)**, og vælg fanen **Enhedstilknytninger**. I venstre filter skal du vælge **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="ba1b6-177">I højre filter skal du vælge **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="ba1b6-178">Søg efter **contactperson** for at finde kildefeltet **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="ba1b6-179">Klik på knappen **Handlinger**, og vælg **Slet**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![selv- eller cirkulær reference 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="ba1b6-181">Gentag for at slette feltet **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![selv- eller cirkulær reference](media/cust_selfref4.png)
    
    5. <span data-ttu-id="ba1b6-183">Gem ændringerne i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="ba1b6-184">Deaktiver ændringssporing for **Debitorer V3**-enheden.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="ba1b6-185">Naviger til **Datastyring \> Dataenheder**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="ba1b6-186">Vælg enheden **Debitorer V3**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="ba1b6-187">Klik på **Indstillinger** på menulinjen og derefter på **Ændringssporing**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![selv- eller cirkulær reference 5](media/selfref_options.png)
    
    4. <span data-ttu-id="ba1b6-189">Klik på **Deaktiver ændringssporing**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-189">Click **Disable Change Tracking**.</span></span>
    
        ![selv- eller cirkulær reference 6](media/selfref_tracking.png)

3. <span data-ttu-id="ba1b6-191">Kør den første synkronisering for tilknytningen **Debitorer V3 (konti)**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="ba1b6-192">Den første synkronisering skal køres uden fejl.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="ba1b6-193">Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontaktpersoner)**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="ba1b6-194">Der er 2 tilknytninger med samme navn.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="ba1b6-195">Vælg en med beskrivelsen af **Dobbeltskrivningsskabelon for synkronisering mellem FO.CDS Kreditorkontakter V2 til CDS.Contacts. Kræver ny pakke \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="ba1b6-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="ba1b6-196">på fanen **Detaljer** på tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="ba1b6-197">Tilføj felterne **InvoiceAccount** og **ContactPersonId** igen på tilknytningen **Debitorer V3 (konti)**, og gem tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="ba1b6-198">Nu er både **InvoiceAccount** og feltet **ContactPersonId** igen en del af den direkte synkroniseringstilstand.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="ba1b6-199">I det næste trin udfører du den første synkronisering for disse felter.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="ba1b6-200">Kør den første synkronisering for tilknytningen **Debitorer V3 (konti)** igen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="ba1b6-201">Da ændringssporing er deaktiveret, vil kørsel af synkroniseringen synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Finance and Operations-appen med Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="ba1b6-202">Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Common Data Service med Finance and Operations, skal du bruge et dataintegrationsprojekt.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="ba1b6-203">I Power Apps skal du oprette et dataintegrationsprojekt mellem **Sales.Account**- og **Finance and Operations apps.Customers V3**-enhederne.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="ba1b6-204">Dataretningen skal ligge fra Common Data Service til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="ba1b6-205">Da **InvoiceAccount** er en ny attribut i dobbeltskrivning, kan det være en god idé at springe den første synkronisering over for denne attribut.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="ba1b6-206">Du kan finde flere oplysninger under [Integrere data i Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="ba1b6-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="ba1b6-207">Følgende billede viser et projekt, der opdaterer **CustomerAccount** og **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![selv- eller cirkulær reference](media/cust_selfref6.png)

    2. <span data-ttu-id="ba1b6-209">Tilføj firmakriterierne i filteret på Common Data Service-siden, da det kun er de poster, der opfylder filterkriterierne, der opdateres i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="ba1b6-210">Hvis du vil tilføje et filter, skal du klikke på filterikonet.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="ba1b6-211">I dialogboksen **Rediger forespørgsel** kan du tilføje en filterforespørgsel som **_msdyn_company_value eq '\<guid\> '**.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="ba1b6-212">Hvis filterikonet ikke er til stede, skal du oprette en supportanmodning for at bede dataintegrationsteamet om at aktivere filtreringsevnen på din lejer.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="ba1b6-213">Hvis du ikke indtaster en filterforespørgsel for **_msdyn_company_value**, synkroniseres alle poster.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![selv- eller cirkulær reference](media/cust_selfref7.png)

        <span data-ttu-id="ba1b6-215">Dermed er den første synkronisering af posterne fuldført.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="ba1b6-216">Aktivér ændringssporing for **Debitorer V3**-enheden i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="ba1b6-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

