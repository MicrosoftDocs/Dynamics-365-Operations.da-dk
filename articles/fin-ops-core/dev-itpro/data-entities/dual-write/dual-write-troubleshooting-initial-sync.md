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
ms.openlocfilehash: e4ee3bf07a1df445875197f38f655464cc9b44d3
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443843"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Foretage fejlfinding af problemer under den første synkronisering

[!include [banner](../../includes/banner.md)]

Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Kontrollere, om der er fejl i første synkronisering i en Finance and Operations-app

Når du har aktiveret tilknytningsskabelonerne, skal status for tilknytningerne være **Kører**. Hvis status er **Kører ikke**, er der opstået fejl under den første synkronisering. Hvis du vil have vist fejlene, skal du vælge fanen **Oplysninger om første synkronisering** på siden **Dobbeltskrivning**.

![Fejl under fanen Oplysninger om første synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Du kan ikke fuldføre den første synkronisering: 400 ugyldig anmodning

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist følgende fejlmeddelelse, når du forsøger at køre tilknytningen og den første synkronisering:

*(\[Ugyldig anmodning\], Fjernserveren returnerede en fejl: (400) Ugyldig anmodning). AX-eksport registrerede en fejl*

Her er et eksempel på den fulde fejlmeddelelse.

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

Hvis denne fejl opstår konsekvent, og du ikke kan fuldføre den første synkronisering, skal du følge disse trin for at løse problemet.

1. Log på den virtuelle maskine (VM) for Finance and Operations-appen.
2. Åbn Microsoft Management Console.
3. I ruden **Services** skal du sikre dig, at Microsoft Dynamics 365 Dataimport/eksportstruktur-tjenesten kører. Genstart, hvis den er stoppet, fordi den første synkronisering kræver det.

## <a name="initial-synchronization-error-403-forbidden"></a>Fejl under første synkronisering: 403 forbudt

Du kan få vist følgende fejlmeddelelse under første synkronisering:

*(\[Forbudt\], Fjernserveren returnerede en fejl: (403) forbudt.), AX-eksport registrerede en fejl*

Følg disse trin for at løse dette problem.

1. Log på Finance and Operations-appen.
2. Slet **DtAppID**-klienten på siden **Azure Active Directory-programmer**, og tilføj den derefter igen.

![DtAppID-klient på listen over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Selvreference- eller cirkulær referencefejl under første synkronisering

Du kan få vist en fejlmeddelelse, hvis nogen af dine tilknytninger har selvreferencer eller cirkulære referencer. Fejlene falder i disse kategorier:

- [Fejl i enhedstilknytning V2–to–msdyn_vendors for kreditorer](#error-vendor-map)
- [Fejl i enhedstilknytning V3–to–Accounts for debitorer](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Løse fejl i enhedstilknytning V2–to–msdyn_vendors for kreditorer

Du kan støde ind i indledende synkroniseringsfejl for tilknytning af **Kreditorer V2** til **msdyn\_vendors**, hvis enhederne har eksisterende poster med værdier i felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**. Disse fejl skyldes, at **InvoiceVendorAccountNumber** er et selvrefererende felt, og at **PrimaryContactPersonId** er en cirkulær reference i kreditortilknytningen.

De fejlmeddelelser, du modtager, har følgende form.

*GUID for feltet kunne ikke fortolkes: \<field\>. Opslaget blev ikke fundet: \<value\>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Her er nogle eksempler:

- *GUID for feltet kunne ikke fortolkes: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *GUID for feltet kunne ikke fortolkes: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Opslaget blev ikke fundet: V24-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Hvis der er poster i kreditorenheden med værdier i felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**, skal du følge disse trin for at fuldføre den første synkronisering.

1. I Finance and Operations-appen skal du slette felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** fra tilknytningen og derefter gemme tilknytningen.

    1. Gå til siden dobbeltskrivning-tilknytning for **Kreditorer V2 (msdyn\_vendors)**, og vælg fanen **Enhedstilknytninger**. I venstre filter skal du vælge **Finance and Operations apps.Vendors V2**. I højre filter skal du vælge **Sales.Vendor**.
    2. Søg efter **primarycontactperson** for at finde kildefeltet **PrimaryContactPersonId**.
    3. Vælg **Handlinger**, og vælg derefter **Slet**.

        ![Slette feltet PrimaryContactPersonId](media/vend_selfref3.png)

    4. Gentag disse trin for at slette feltet **InvoiceVendorAccountNumber**.

        ![Sletning af feltet InvoiceVendorAccountNumber.](media/vend-selfref4.png)

    5. Gem ændringerne i tilknytningen.

2. Slå ændringssporing fra for **Kreditorer V2**-enheden.

    1. I arbejdsområdet **Datastyring** skal du markere feltet **Dataenheder**.
    2. Vælg enheden **Kreditorer V2**.
    3. I handlingsruden skal du vælge **Indstillinger** og derefter vælge **Ændringssporing**.

        ![Valg af indstillingen Ændringssporing](media/selfref_options.png)

    4. Vælg **Deaktiver ændringssporing**.

        ![Valg af Deaktiver ændringssporing](media/selfref_tracking.png)

3. Kør den første synkronisering for tilknytningen **Kreditorer V2 (msdyn\_vendors)**. Den første synkronisering skal køres uden fejl.
4. Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontakter)**. Du skal synkronisere denne tilknytning, hvis du vil synkronisere feltet for den primære kontakt på kreditorenheden, fordi den første synkronisering også skal udføres for kontaktposterne.
5. Føj felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbage til tilknytningen **Kreditorer V2 (msdyn\_vendors)**, og gem tilknytningen.
6. Kør den første synkronisering igen for tilknytningen **Kreditorer V2 (msdyn\_vendors)**. Alle poster synkroniseres, fordi ændringssporing er deaktiveret.
7. Slå ændringssporing til igen for **Kreditorer V2**-enheden.

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a>Løse fejl i enhedstilknytning V3–to–Accounts for debitorer

Du kan støde ind i indledende synkroniseringsfejl for tilknytning af **Kreditorer V3** til **Konti**, hvis enhederne har eksisterende poster med værdier i felterne **ContactPersonId** og **InvoiceAccount**. Disse fejl opstår, fordi **InvoiceAccount** er et selvrefererende felt, og at **ContactPersonID** er en cirkulær reference i kreditortilknytningen.

De fejlmeddelelser, du modtager, har følgende form.

*GUID for feltet kunne ikke fortolkes: \<field\>. Opslaget blev ikke fundet: \<value\>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Her er nogle eksempler:

- *GUID for feltet kunne ikke fortolkes: primarycontactid.msdyn\_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *GUID for feltet kunne ikke fortolkes: msdyn\_billingaccount.accountnumber. Opslaget blev ikke fundet: 1206-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Hvis der er poster i debitorenheden med værdier i felterne **ContactPersonID** og **InvoiceAccount**, skal du følge disse trin for at fuldføre den første synkronisering. Du kan bruge denne fremgangsmåde til alle indbyggede enheder, f.eks. **Konti** og **Kontakter**.

1. I Finance and Operations-appen skal du slette felterne **ContactPersonID** og **InvoiceAccount** fra tilknytningen **Debitorer V3 (konti)** og derefter gemme tilknytningen.

    1. Gå til siden med dobbeltskrivning-tilknytning for **Debitorer V3 (konti)**, og vælg fanen **Enhedstilknytninger**. I venstre filter skal du vælge **Finance and Operations apps.Customers V3**. I højre filter skal du vælge **Common Data Service.Account**.
    2. Søg efter **contactperson** for at finde kildefeltet **ContactPersonID**.
    3. Vælg **Handlinger**, og vælg derefter **Slet**.

        ![Sletning af feltet ContactPersonID](media/cust_selfref3.png)

    4. Gentag disse trin for at slette feltet **InvoiceAccount**.

        ![Sletning af feltet InvoiceAccount](media/cust_selfref4.png)

    5. Gem ændringerne i tilknytningen.

2. Slå ændringssporing fra for **Debitorer V3**-enheden.

    1. I arbejdsområdet **Datastyring** skal du markere feltet **Dataenheder**.
    2. Vælg enheden **Debitorer V3**.
    3. I handlingsruden skal du vælge **Indstillinger** og derefter vælge **Ændringssporing**.

        ![Valg af indstillingen Ændringssporing](media/selfref_options.png)

    4. Vælg **Deaktiver ændringssporing**.

        ![Valg af Deaktiver ændringssporing](media/selfref_tracking.png)

3. Kør den første synkronisering for tilknytningen **Debitorer V3 (konti)**. Den første synkronisering skal køres uden fejl.
4. Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontakter)**.

    > [!NOTE]
    > Der er to tilknytninger med samme navn. Vælg tilknytningen med følgende beskrivelse under fanen **Detaljer**: **Dobbeltskrivningsskabelon for synkronisering mellem FO.CDS Kreditorkontakter V2 til CDS.Contacts. Kræver ny pakke \[Dynamics365SupplyChainExtended\].**

5. Tilføj felterne **InvoiceAccount** og **ContactPersonId** igen i tilknytningen **Debitorer V3 (konti)**, og gem tilknytningen. Nu er både feltet **InvoiceAccount** og feltet **ContactPersonId** igen en del af den direkte synkroniseringstilstand. I det næste trin udfører du den første synkronisering for disse felter.
6. Kør den første synkronisering igen for tilknytningen **Debitorer V3 (konti)**. Da ændringssporing er slået fra, bliver dataene for **InvoiceAccount** og **ContactPersonId** synkroniseret fra Finance and Operations-appen til Common Data Service.
7. Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Common Data Service til Finance and Operations-appen, skal du bruge et dataintegrationsprojekt.

    1. I Power Apps skal du oprette et dataintegrationsprojekt mellem **Sales.Account**- og **Finance and Operations apps.Customers V3**-enhederne. Dataretningen skal ligge fra Common Data Service til Finance and Operations-appen. Da **InvoiceAccount** er en ny attribut i dobbeltskrivning, kan det være en god idé at springe den første synkronisering over for den. Du kan finde flere oplysninger under [Integrere data i Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Følgende illustration viser et projekt, der opdaterer **CustomerAccount** og **ContactPersonId**.

        ![Dataintegrationsprojektet, der skal opdatere CustomerAccount og ContactPersonId](media/cust_selfref6.png)

    2. Tilføj firmakriterierne i filteret på Common Data Service-siden, så kun de poster, der opfylder filterkriterierne, opdateres i Finance and Operations-appen. Hvis du vil tilføje et filter, skal du vælge filterknappen. I dialogboksen **Rediger forespørgsel** kan du tilføje en filterforespørgsel som **\_msdyn\_company\_value eq '\<guid\>'**. 

        > [BEMÆRK] Hvis filterknappen ikke er til stede, skal du oprette en supportanmodning for at bede dataintegrationsteamet om at aktivere filtreringsfunktionen på din lejer.

        Hvis du ikke indtaster en filterforespørgsel for **\_msdyn\_company\_value**, synkroniseres alle poster.

        ![Tilføjelse af en filterforespørgsel](media/cust_selfref7.png)

    Den første synkronisering af posterne er nu fuldført.

8. Aktivér ændringssporing igen i Finance and Operations-appen for **Debitorer V3**-enheden.
