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
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Foretage fejlfinding af problemer under den første synkronisering

[!include [banner](../../includes/banner.md)]

Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Kontrollere, om der er fejl i første synkronisering i en Finance and Operations-app

Når du har aktiveret tilknytningsskabelonerne, skal status for tilknytningerne være **Kører**. Hvis status er **Kører ikke**, er der opstået fejl under den første synkronisering. Hvis du vil have vist fejlene, skal du vælge fanen **Oplysninger om første synkronisering** på siden **Dobbeltskrivning**.

![Fanen Oplysninger om første synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Du kan ikke fuldføre den første synkronisering: 400 ugyldig anmodning

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist følgende fejlmeddelelse, når du forsøger at køre tilknytningen og den første synkronisering:

*Fjernserveren returnerede en fejl: (400) ugyldig anmodning. AX-eksport registrerede en fejl*

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

![Liste over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Selvreference- eller cirkulære referencefesjl under første synkronisering

Du kan få vist en fejlmeddelelse, hvis nogen af dine tilknytninger har selvreferencer eller cirkulære referencer. Fejlene falder i disse kategorier:

- [Kreditorer V2 til msdyn_vendors med enhedstilknytning](#error-vendor-map)
- [Debitorer V3 til konti med enhedstilknytning](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Løse en fejl i Kreditorer V2 til msdyn_vendors med enhedstilknytning

Du kan støde ind i følgende indledende synkroniseringsfejl på **Kreditorer V2** til **msdyn_vendors**-tilknytning, hvis enhederne har eksisterende poster med værdier i felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**. Dette skyldes, at **InvoiceVendorAccountNumber** er et selvrefererende felt, og at **PrimaryContactPersonId** er en cirkulær reference i kreditortilknytningen.

*GUID for feltet kunne ikke fortolkes: <field>. Opslaget blev ikke fundet: <value>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$Select=<field>&$filter=<field> eq <value>*

Her er et par eksempler:

- *GUID for feltet kunne ikke fortolkes: msdyn_vendorprimarycontactperson. msdyn_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select = msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *GUID for feltet kunne ikke fortolkes: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Opslaget blev ikke fundet: V-24-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Hvis der er poster med værdier i disse felter i kreditorenheden, skal du følge trinnene i afsnittet nedenfor for at fuldføre den første synkronisering.

1. I Finance and Operations-appen skal du slette felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** fra tilknytningen og gemme ændringerne.

    1. Gå til siden dobbeltskrivning-tilknytning for **Kreditorer V2 (msdyn_vendors)**, og vælg fanen **Enhedstilknytninger**. I venstre filter skal du vælge **Finance and Operations apps.Vendors V2**. I højre filter skal du vælge **Sales.Vendor**.

    2. Søg efter **primarycontactperson** for at finde kildefeltet **PrimaryContactPersonId**.
    
    3. Klik på knappen **Handlinger**, og vælg **Slet**.
    
        ![selv- eller cirkulær reference 3](media/vend_selfref3.png)
    
    4. Gentag for at slette feltet **InvoiceVendorAccountNumber**.
    
        ![selv- eller cirkulær reference 4](media/vend-selfref4.png)
    
    5. Gem ændringerne i tilknytningen.

2. Deaktiver ændringssporingen for **Kreditorer v2**-enheden.

    1. Naviger til **Datastyring \> Dataenheder**.
    
    2. Vælg enheden **Kreditorer V2**.
    
    3. Klik på **Indstillinger** på menulinjen og derefter på **Ændringssporing**.
    
        ![selv- eller cirkulær reference 5](media/selfref_options.png)
    
    4. Klik på **Deaktiver ændringssporing**.
    
        ![selv- eller cirkulær reference 6](media/selfref_tracking.png)

3. Kør den første synkronisering af tilknytningen **Kreditorer V2 (msdyn_vendors)**. Den første synkronisering skal køres uden fejl.

4. Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontaktpersoner)**. Du skal synkronisere denne tilknytning, hvis du vil synkronisere feltet for den primære kontaktperson på kreditorenheden, når kontaktpersonposterne også skal synkroniseres.

5. Føj felterne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbage til tilknytningen **Kreditorer V2 (msdyn_vendors)**, og gem tilknytningen.

6. Kør den første synkronisering igen for tilknytningen **Kreditorer V2 (msdyn_vendors)**. Alle poster synkroniseres, fordi ændringssporing er deaktiveret.

7. Aktivér ændringssporing for **Kreditorer V2**-enheden.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Løse en fejl i Debitorer V3 til konti med enhedstilknytning

Du kan støde ind i følgende indledende synkroniseringsfejl på **Kreditorer V3** til **Konti**-tilknytningen, hvis enhederne har eksisterende poster med værdier i felterne **ContactPersonID** og **InvoiceAccount**. Dette skyldes, at **InvoiceAccount** er et selvrefererende felt, og at **ContactPersonID** er en cirkulær reference i kreditortilknytningen.

*GUID for feltet kunne ikke fortolkes: <field>. Opslaget blev ikke fundet: <value>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$Select=<field>&$filter=<field> eq <value>*

- *GUID for feltet kunne ikke fortolkes: primarycontactid.msdyn_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *GUID for feltet kunne ikke fortolkes: msdyn_billingaccount.accountnumber. Opslaget blev ikke fundet: 1206-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

Hvis der er poster med værdier i disse felter i debitorenheden, skal du følge trinnene i afsnittet nedenfor for at fuldføre den første synkronisering. Du kan bruge denne fremgangsmåde til alle out-of-the-box-enhederne, f.eks. Konti og Kontaktpersoner.

1. I Finance and Operations-appen skal du slette felterne **ContactPersonID** og **InvoiceAccount** fra tilknytningen **Debitorer V3 (konti)** og gemme tilknytningen.

    1. Gå til siden dobbeltskrivning-tilknytning for **Debitorer V3 (konti)**, og vælg fanen **Enhedstilknytninger**. I venstre filter skal du vælge **Finance and Operations apps.Customers V3**. I højre filter skal du vælge **Common Data Service.Account**.

    2. Søg efter **contactperson** for at finde kildefeltet **ContactPersonID**.
    
    3. Klik på knappen **Handlinger**, og vælg **Slet**.
    
        ![selv- eller cirkulær reference 3](media/cust_selfref3.png)
    
    4. Gentag for at slette feltet **InvoiceAccount**.
    
        ![selv- eller cirkulær reference](media/cust_selfref4.png)
    
    5. Gem ændringerne i tilknytningen.

2. Deaktiver ændringssporing for **Debitorer V3**-enheden.

    1. Naviger til **Datastyring \> Dataenheder**.
    
    2. Vælg enheden **Debitorer V3**.
    
    3. Klik på **Indstillinger** på menulinjen og derefter på **Ændringssporing**.
    
        ![selv- eller cirkulær reference 5](media/selfref_options.png)
    
    4. Klik på **Deaktiver ændringssporing**.
    
        ![selv- eller cirkulær reference 6](media/selfref_tracking.png)

3. Kør den første synkronisering for tilknytningen **Debitorer V3 (konti)**. Den første synkronisering skal køres uden fejl.

4. Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontaktpersoner)**. Der er 2 tilknytninger med samme navn. Vælg en med beskrivelsen af **Dobbeltskrivningsskabelon for synkronisering mellem FO.CDS Kreditorkontakter V2 til CDS.Contacts. Kræver ny pakke \[Dynamics365SupplyChainExtended\].** på fanen **Detaljer** på tilknytningen.

5. Tilføj felterne **InvoiceAccount** og **ContactPersonId** igen på tilknytningen **Debitorer V3 (konti)**, og gem tilknytningen. Nu er både **InvoiceAccount** og feltet **ContactPersonId** igen en del af den direkte synkroniseringstilstand. I det næste trin udfører du den første synkronisering for disse felter.

6. Kør den første synkronisering for tilknytningen **Debitorer V3 (konti)** igen. Da ændringssporing er deaktiveret, vil kørsel af synkroniseringen synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Finance and Operations-appen med Common Data Service.

7. Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Common Data Service med Finance and Operations, skal du bruge et dataintegrationsprojekt.

    1. I Power Apps skal du oprette et dataintegrationsprojekt mellem **Sales.Account**- og **Finance and Operations apps.Customers V3**-enhederne. Dataretningen skal ligge fra Common Data Service til Finance and Operations-appen.  Da **InvoiceAccount** er en ny attribut i dobbeltskrivning, kan det være en god idé at springe den første synkronisering over for denne attribut. Du kan finde flere oplysninger under [Integrere data i Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Følgende billede viser et projekt, der opdaterer **CustomerAccount** og **ContactPersonId**.

        ![selv- eller cirkulær reference](media/cust_selfref6.png)

    2. Tilføj firmakriterierne i filteret på Common Data Service-siden, da det kun er de poster, der opfylder filterkriterierne, der opdateres i Finance and Operations-appen. Hvis du vil tilføje et filter, skal du klikke på filterikonet. I dialogboksen **Rediger forespørgsel** kan du tilføje en filterforespørgsel som **_msdyn_company_value eq '\<guid\> '**. Hvis filterikonet ikke er til stede, skal du oprette en supportanmodning for at bede dataintegrationsteamet om at aktivere filtreringsevnen på din lejer. Hvis du ikke indtaster en filterforespørgsel for **_msdyn_company_value**, synkroniseres alle poster.

        ![selv- eller cirkulær reference](media/cust_selfref7.png)

        Dermed er den første synkronisering af posterne fuldført.

8. Aktivér ændringssporing for **Debitorer V3**-enheden i Finance and Operations-appen.

