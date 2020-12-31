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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a7ba4fa4771324b4bcb8464649bd8ce8f32024c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683547"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="2a073-103">Foretage fejlfinding af problemer under den første synkronisering</span><span class="sxs-lookup"><span data-stu-id="2a073-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2a073-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2a073-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="2a073-105">Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="2a073-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a073-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="2a073-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="2a073-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="2a073-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="2a073-108">Kontrollere, om der er fejl i første synkronisering i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="2a073-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="2a073-109">Når du har aktiveret tilknytningsskabelonerne, skal status for tilknytningerne være **Kører**.</span><span class="sxs-lookup"><span data-stu-id="2a073-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="2a073-110">Hvis status er **Kører ikke**, er der opstået fejl under den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="2a073-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="2a073-111">Hvis du vil have vist fejlene, skal du vælge fanen **Oplysninger om første synkronisering** på siden **Dobbeltskrivning**.</span><span class="sxs-lookup"><span data-stu-id="2a073-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Fejl under fanen Oplysninger om første synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="2a073-113">Du kan ikke fuldføre den første synkronisering: 400 ugyldig anmodning</span><span class="sxs-lookup"><span data-stu-id="2a073-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="2a073-114">**Påkrævet rolle for at rette fejlen:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="2a073-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="2a073-115">Du kan få vist følgende fejlmeddelelse, når du forsøger at køre tilknytningen og den første synkronisering:</span><span class="sxs-lookup"><span data-stu-id="2a073-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="2a073-116">*(\[Ugyldig anmodning\], Fjernserveren returnerede en fejl: (400) Ugyldig anmodning). AX-eksport registrerede en fejl*</span><span class="sxs-lookup"><span data-stu-id="2a073-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="2a073-117">Her er et eksempel på den fulde fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="2a073-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="2a073-118">Hvis denne fejl opstår konsekvent, og du ikke kan fuldføre den første synkronisering, skal du følge disse trin for at løse problemet.</span><span class="sxs-lookup"><span data-stu-id="2a073-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="2a073-119">Log på den virtuelle maskine (VM) for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="2a073-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="2a073-120">Åbn Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="2a073-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="2a073-121">I ruden **Services** skal du sikre dig, at Microsoft Dynamics 365 Dataimport/eksportstruktur-tjenesten kører.</span><span class="sxs-lookup"><span data-stu-id="2a073-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="2a073-122">Genstart, hvis den er stoppet, fordi den første synkronisering kræver det.</span><span class="sxs-lookup"><span data-stu-id="2a073-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="2a073-123">Fejl under første synkronisering: 403 forbudt</span><span class="sxs-lookup"><span data-stu-id="2a073-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="2a073-124">Du kan få vist følgende fejlmeddelelse under første synkronisering:</span><span class="sxs-lookup"><span data-stu-id="2a073-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="2a073-125">*(\[Forbudt\], Fjernserveren returnerede en fejl: (403) forbudt.), AX-eksport registrerede en fejl*</span><span class="sxs-lookup"><span data-stu-id="2a073-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="2a073-126">Følg disse trin for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="2a073-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="2a073-127">Log på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="2a073-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="2a073-128">Slet **DtAppID**-klienten på siden **Azure Active Directory-programmer**, og tilføj den derefter igen.</span><span class="sxs-lookup"><span data-stu-id="2a073-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID-klient på listen over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="2a073-130">Selvreference- eller cirkulær referencefejl under første synkronisering</span><span class="sxs-lookup"><span data-stu-id="2a073-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="2a073-131">Du kan få vist en fejlmeddelelse, hvis nogen af dine tilknytninger har selvreferencer eller cirkulære referencer.</span><span class="sxs-lookup"><span data-stu-id="2a073-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="2a073-132">Fejlene falder i disse kategorier:</span><span class="sxs-lookup"><span data-stu-id="2a073-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="2a073-133">Fejl i tabeltilknytningen V2–to–msdyn_vendors for kreditorer</span><span class="sxs-lookup"><span data-stu-id="2a073-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="2a073-134">Fejl i tabeltilknytningen V3–to–Accounts for debitorer</span><span class="sxs-lookup"><span data-stu-id="2a073-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="2a073-135">Løse fejl i tabeltilknytningen V2–to–msdyn_vendors for kreditorer</span><span class="sxs-lookup"><span data-stu-id="2a073-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="2a073-136">Du kan støde ind i indledende synkroniseringsfejl for tilknytning af **Kreditorer V2** til **msdyn\_vendors**, hvis tabellerne har eksisterende rækker med værdier i felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="2a073-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="2a073-137">Disse fejl skyldes, at **InvoiceVendorAccountNumber** er et selvrefererende felt, og at **PrimaryContactPersonId** er en cirkulær reference i kreditortilknytningen.</span><span class="sxs-lookup"><span data-stu-id="2a073-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="2a073-138">De fejlmeddelelser, du modtager, har følgende form.</span><span class="sxs-lookup"><span data-stu-id="2a073-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="2a073-139">*GUID for feltet kunne ikke fortolkes: \<field\>. Opslaget blev ikke fundet: \<value\>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="2a073-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="2a073-140">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="2a073-140">Here are some examples:</span></span>

- <span data-ttu-id="2a073-141">*GUID for feltet kunne ikke fortolkes: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="2a073-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="2a073-142">*GUID for feltet kunne ikke fortolkes: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Opslaget blev ikke fundet: V24-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="2a073-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="2a073-143">Hvis der er rækker i kreditorenheden med værdier i felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**, skal du følge disse trin for at fuldføre den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="2a073-143">If any rows in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="2a073-144">I Finance and Operations-appen skal du slette felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** fra tilknytningen og derefter gemme tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="2a073-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="2a073-145">Gå til siden dobbeltskrivning-tilknytning for **Kreditorer V2 (msdyn\_vendors)**, og vælg fanen **Tabeltilknytninger**. I venstre filter skal du vælge **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="2a073-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="2a073-146">I højre filter skal du vælge **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="2a073-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="2a073-147">Søg efter **primarycontactperson** for at finde kildefeltet **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="2a073-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="2a073-148">Vælg **Handlinger**, og vælg derefter **Slet**.</span><span class="sxs-lookup"><span data-stu-id="2a073-148">Select **Actions**, and then select **Delete**.</span></span>

        ![Slette feltet PrimaryContactPersonId](media/vend_selfref3.png)

    4. <span data-ttu-id="2a073-150">Gentag disse trin for at slette feltet **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="2a073-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![Sletning af feltet InvoiceVendorAccountNumber.](media/vend-selfref4.png)

    5. <span data-ttu-id="2a073-152">Gem ændringerne i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="2a073-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="2a073-153">Slå ændringssporing fra for **Kreditorer V2**-enheden.</span><span class="sxs-lookup"><span data-stu-id="2a073-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="2a073-154">I arbejdsområdet **Datastyring** skal du markere feltet **Datatabeller**.</span><span class="sxs-lookup"><span data-stu-id="2a073-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="2a073-155">Vælg enheden **Kreditorer V2**.</span><span class="sxs-lookup"><span data-stu-id="2a073-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="2a073-156">I handlingsruden skal du vælge **Indstillinger** og derefter vælge **Ændringssporing**.</span><span class="sxs-lookup"><span data-stu-id="2a073-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Valg af indstillingen Ændringssporing](media/selfref_options.png)

    4. <span data-ttu-id="2a073-158">Vælg **Deaktiver ændringssporing**.</span><span class="sxs-lookup"><span data-stu-id="2a073-158">Select **Disable Change Tracking**.</span></span>

        ![Valg af Deaktiver ændringssporing](media/selfref_tracking.png)

3. <span data-ttu-id="2a073-160">Kør den første synkronisering for tilknytningen **Kreditorer V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="2a073-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="2a073-161">Den første synkronisering skal køres uden fejl.</span><span class="sxs-lookup"><span data-stu-id="2a073-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="2a073-162">Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontakter)**.</span><span class="sxs-lookup"><span data-stu-id="2a073-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="2a073-163">Du skal synkronisere denne tilknytning, hvis du vil synkronisere feltet for den primære kontakt på kreditorenheden, fordi den første synkronisering også skal udføres for kontaktrækkerne.</span><span class="sxs-lookup"><span data-stu-id="2a073-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="2a073-164">Føj felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbage til tilknytningen **Kreditorer V2 (msdyn\_vendors)**, og gem tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="2a073-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="2a073-165">Kør den første synkronisering igen for tilknytningen **Kreditorer V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="2a073-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="2a073-166">Alle rækker synkroniseres, fordi ændringssporing er deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="2a073-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="2a073-167">Slå ændringssporing til igen for **Kreditorer V2**-enheden.</span><span class="sxs-lookup"><span data-stu-id="2a073-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="2a073-168">Løse fejl i tabeltilknytningen V3–to–Accounts for debitorer</span><span class="sxs-lookup"><span data-stu-id="2a073-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="2a073-169">Du kan støde ind i indledende synkroniseringsfejl for tilknytning af **Kreditorer V3** til **Konti**, hvis tabellerne har eksisterende rækker med værdier i felterne **ContactPersonId** og **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="2a073-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="2a073-170">Disse fejl opstår, fordi **InvoiceAccount** er et selvrefererende felt, og at **ContactPersonID** er en cirkulær reference i kreditortilknytningen.</span><span class="sxs-lookup"><span data-stu-id="2a073-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="2a073-171">De fejlmeddelelser, du modtager, har følgende form.</span><span class="sxs-lookup"><span data-stu-id="2a073-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="2a073-172">*GUID for feltet kunne ikke fortolkes: \<field\>. Opslaget blev ikke fundet: \<value\>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="2a073-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="2a073-173">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="2a073-173">Here are some examples:</span></span>

- <span data-ttu-id="2a073-174">*GUID for feltet kunne ikke fortolkes: primarycontactid.msdyn\_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="2a073-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="2a073-175">*GUID for feltet kunne ikke fortolkes: msdyn\_billingaccount.accountnumber. Opslaget blev ikke fundet: 1206-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="2a073-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="2a073-176">Hvis der er rækker i debitorenheden med værdier i felterne **ContactPersonID** og **InvoiceAccount**, skal du følge disse trin for at fuldføre den første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="2a073-176">If any rows in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="2a073-177">Du kan bruge denne fremgangsmåde til alle indbyggede tabeller, f.eks. **Konti** og **Kontakter**.</span><span class="sxs-lookup"><span data-stu-id="2a073-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="2a073-178">I Finance and Operations-appen skal du slette felterne **ContactPersonID** og **InvoiceAccount** fra tilknytningen **Debitorer V3 (konti)** og derefter gemme tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="2a073-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="2a073-179">Gå til siden med dobbeltskrivning-tilknytning for **Debitorer V3 (konti)**, og vælg fanen **Tabeltilknytninger**. I venstre filter skal du vælge **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="2a073-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="2a073-180">I højre filter skal du vælge **Dataverse.Account**.</span><span class="sxs-lookup"><span data-stu-id="2a073-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="2a073-181">Søg efter **contactperson** for at finde kildefeltet **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="2a073-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="2a073-182">Vælg **Handlinger**, og vælg derefter **Slet**.</span><span class="sxs-lookup"><span data-stu-id="2a073-182">Select **Actions**, and then select **Delete**.</span></span>

        ![Sletning af feltet ContactPersonID](media/cust_selfref3.png)

    4. <span data-ttu-id="2a073-184">Gentag disse trin for at slette feltet **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="2a073-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![Sletning af feltet InvoiceAccount](media/cust_selfref4.png)

    5. <span data-ttu-id="2a073-186">Gem ændringerne i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="2a073-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="2a073-187">Slå ændringssporing fra for **Debitorer V3**-enheden.</span><span class="sxs-lookup"><span data-stu-id="2a073-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="2a073-188">I arbejdsområdet **Datastyring** skal du markere feltet **Datatabeller**.</span><span class="sxs-lookup"><span data-stu-id="2a073-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="2a073-189">Vælg enheden **Debitorer V3**.</span><span class="sxs-lookup"><span data-stu-id="2a073-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="2a073-190">I handlingsruden skal du vælge **Indstillinger** og derefter vælge **Ændringssporing**.</span><span class="sxs-lookup"><span data-stu-id="2a073-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Valg af indstillingen Ændringssporing](media/selfref_options.png)

    4. <span data-ttu-id="2a073-192">Vælg **Deaktiver ændringssporing**.</span><span class="sxs-lookup"><span data-stu-id="2a073-192">Select **Disable Change Tracking**.</span></span>

        ![Valg af Deaktiver ændringssporing](media/selfref_tracking.png)

3. <span data-ttu-id="2a073-194">Kør den første synkronisering for tilknytningen **Debitorer V3 (konti)**.</span><span class="sxs-lookup"><span data-stu-id="2a073-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="2a073-195">Den første synkronisering skal køres uden fejl.</span><span class="sxs-lookup"><span data-stu-id="2a073-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="2a073-196">Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontakter)**.</span><span class="sxs-lookup"><span data-stu-id="2a073-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2a073-197">Der er to tilknytninger med samme navn.</span><span class="sxs-lookup"><span data-stu-id="2a073-197">There are two maps that have the same name.</span></span> <span data-ttu-id="2a073-198">Vælg tilknytningen med følgende beskrivelse under fanen **Detaljer**: **Dobbeltskrivningsskabelon for synkronisering mellem FO.CDS Kreditorkontakter V2 til CDS.Contacts. Kræver ny pakke \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="2a073-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="2a073-199">Tilføj felterne **InvoiceAccount** og **ContactPersonId** igen i tilknytningen **Debitorer V3 (konti)**, og gem tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="2a073-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="2a073-200">Nu er både feltet **InvoiceAccount** og feltet **ContactPersonId** igen en del af den direkte synkroniseringstilstand.</span><span class="sxs-lookup"><span data-stu-id="2a073-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="2a073-201">I det næste trin udfører du den første synkronisering for disse felter.</span><span class="sxs-lookup"><span data-stu-id="2a073-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="2a073-202">Kør den første synkronisering igen for tilknytningen **Debitorer V3 (konti)**.</span><span class="sxs-lookup"><span data-stu-id="2a073-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="2a073-203">Da ændringssporing er slået fra, bliver dataene for **InvoiceAccount** og **ContactPersonId** synkroniseret fra Finance and Operations-appen til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2a073-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="2a073-204">Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Dataverse til Finance and Operations-appen, skal du bruge et dataintegrationsprojekt.</span><span class="sxs-lookup"><span data-stu-id="2a073-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="2a073-205">I Power Apps skal du oprette et dataintegrationsprojekt mellem **Sales.Account**- og **Finance and Operations apps.Customers V3**-tabellerne.</span><span class="sxs-lookup"><span data-stu-id="2a073-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="2a073-206">Dataretningen skal ligge fra Dataverse til Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="2a073-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="2a073-207">Da **InvoiceAccount** er en ny attribut i dobbeltskrivning, kan det være en god idé at springe den første synkronisering over for den.</span><span class="sxs-lookup"><span data-stu-id="2a073-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="2a073-208">Du kan finde flere oplysninger under [Integrere data i Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="2a073-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="2a073-209">Følgende illustration viser et projekt, der opdaterer **CustomerAccount** og **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="2a073-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Dataintegrationsprojektet, der skal opdatere CustomerAccount og ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="2a073-211">Tilføj firmakriterierne i filteret på Dataverse-siden, så kun de rækker, der opfylder filterkriterierne, opdateres i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="2a073-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="2a073-212">Hvis du vil tilføje et filter, skal du vælge filterknappen.</span><span class="sxs-lookup"><span data-stu-id="2a073-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="2a073-213">I dialogboksen **Rediger forespørgsel** kan du tilføje en filterforespørgsel som **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="2a073-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="2a073-214">[BEMÆRK] Hvis filterknappen ikke er til stede, skal du oprette en supportanmodning for at bede dataintegrationsteamet om at aktivere filtreringsfunktionen på din lejer.</span><span class="sxs-lookup"><span data-stu-id="2a073-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="2a073-215">Hvis du ikke indtaster en filterforespørgsel for **\_msdyn\_company\_value**, synkroniseres alle rækker.</span><span class="sxs-lookup"><span data-stu-id="2a073-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Tilføjelse af en filterforespørgsel](media/cust_selfref7.png)

    <span data-ttu-id="2a073-217">Den første synkronisering af rækkerne er nu fuldført.</span><span class="sxs-lookup"><span data-stu-id="2a073-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="2a073-218">Aktivér ændringssporing igen i Finance and Operations-appen for **Debitorer V3**-enheden.</span><span class="sxs-lookup"><span data-stu-id="2a073-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
