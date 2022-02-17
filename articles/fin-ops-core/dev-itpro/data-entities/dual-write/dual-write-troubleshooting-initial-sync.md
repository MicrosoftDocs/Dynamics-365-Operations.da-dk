---
title: Foretage fejlfinding af problemer under den første synkronisering
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 030e565ffff561f6c1efbdd0de9928f70c7c46c0
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063052"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Foretage fejlfinding af problemer under den første synkronisering

[!include [banner](../../includes/banner.md)]



Dette emne indeholder fejlfindingsoplysninger for dobbeltskrivning mellem Finans- og driftsapps og Dataverse. Specifikt indeholder emnet fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer, der kan opstå under den første synkronisering.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Kontrollere for indledende synkroniseringsfejl i en Finans og drift-app

Når du har aktiveret tilknytningsskabelonerne, skal status for tilknytningerne være **Kører**. Hvis status er **Kører ikke**, er der opstået fejl under den første synkronisering. Hvis du vil have vist fejlene, skal du vælge fanen **Oplysninger om første synkronisering** på siden **Dobbeltskrivning**.

![Fejl under fanen Oplysninger om første synkronisering.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Du kan ikke fuldføre den første synkronisering: 400 ugyldig anmodning

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist følgende fejlmeddelelse, når du forsøger at køre tilknytningen og den første synkronisering:

*(\[Ugyldig anmodning\], Fjernserveren returnerede en fejl: (400) Ugyldig anmodning). AX-eksport registrerede en fejl.*

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

1. Log på den virtuelle maskine (VM) for Finans- og driftsapps.
2. Åbn Microsoft Management Console.
3. I ruden **Services** skal du sikre dig, at Microsoft Dynamics 365 Dataimport/eksportstruktur-tjenesten kører. Genstart, hvis den er stoppet, fordi den første synkronisering kræver det.

## <a name="initial-synchronization-error-403-forbidden"></a>Fejl under første synkronisering: 403 forbudt

Du kan få vist følgende fejlmeddelelse under første synkronisering:

*(\[Forbudt\], Fjernserveren returnerede en fejl: (403) forbudt.), AX-eksport registrerede en fejl*

Følg disse trin for at løse dette problem.

1. Log på Finans og drift-appen.
2. Slet **DtAppID**-klienten på siden **Azure Active Directory-programmer**, og tilføj den derefter igen.

![DtAppID-klient på listen over Azure AD-programmer.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Selvreference- eller cirkulær referencefejl under første synkronisering

Du kan få vist en fejlmeddelelse, hvis nogen af dine tilknytninger har selvreferencer eller cirkulære referencer. Fejlene falder i disse kategorier:

- [Fejl i tabeltilknytningen V2–to–msdyn_vendors for kreditorer](#error-vendor-map)
- [Fejl i tabeltilknytningen V3–to–Accounts for debitorer](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Løse fejl i tabeltilknytningen V2–to–msdyn_vendors for kreditorer

Du kan støde ind i indledende synkroniseringsfejl for tilknytning af **Kreditorer V2** til **msdyn\_vendors**, hvis tabellerne har eksisterende rækker med værdier i kolonnerne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**. Disse fejl skyldes, at **InvoiceVendorAccountNumber** er en selvrefererende kolonne, og at **PrimaryContactPersonId** er en cirkulær reference i kreditortilknytningen.

De fejlmeddelelser, du modtager, har følgende form.

*GUID for feltet kunne ikke fortolkes: \<field\>. Opslaget blev ikke fundet: \<value\>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Her er nogle eksempler:

- *GUID for feltet kunne ikke fortolkes: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *GUID for feltet kunne ikke fortolkes: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Opslaget blev ikke fundet: V24-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Hvis der er rækker i kreditortabellen med værdier i kolonnerne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**, skal du følge disse trin for at fuldføre den første synkronisering.

1. I Finans og drift-appen skal du slette kolonnerne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** fra tilknytningen og derefter gemme tilknytningen.

    1. Gå til siden dobbeltskrivning-tilknytning for **Kreditorer V2 (msdyn\_vendors)**, og vælg fanen **Tabeltilknytninger**. I venstre filter skal du vælge **Finans- og driftsapps.Kreditorer V2**. I højre filter skal du vælge **Sales.Vendor**.
    2. Søg efter **primarycontactperson** for at finde kildekolonnen **PrimaryContactPersonId**.
    3. Vælg **Handlinger**, og vælg derefter **Slet**.

        ![Sletning af kolonnen PrimaryContactPersonId.](media/vend_selfref3.png)

    4. Gentag disse trin for at slette kolonnen **InvoiceVendorAccountNumber**.

        ![Sletning af kolonnen InvoiceVendorAccountNumber.](media/vend-selfref4.png)

    5. Gem ændringerne i tilknytningen.

2. Slå ændringssporing fra for tabellen **Kreditorer V2**.

    1. I arbejdsområdet **Datastyring** skal du markere feltet **Datatabeller**.
    2. Vælg tabellen **Kreditorer V2**.
    3. I handlingsruden skal du vælge **Indstillinger** og derefter vælge **Ændringssporing**.

        ![Valg af indstillingen Ændringssporing.](media/selfref_options.png)

    4. Vælg **Deaktiver ændringssporing**.

        ![Valg af Deaktiver ændringssporing.](media/selfref_tracking.png)

3. Kør den første synkronisering for tilknytningen **Kreditorer V2 (msdyn\_vendors)**. Den første synkronisering skal køres uden fejl.
4. Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontakter)**. Du skal synkronisere denne tilknytning, hvis du vil synkronisere kolonnen med den primære kontakt i kreditortabellen, fordi den første synkronisering også skal udføres for kontaktrækkerne.
5. Føj kolonnerne **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** tilbage til tilknytningen **Kreditorer V2 (msdyn\_vendors)**, og gem tilknytningen.
6. Kør den første synkronisering igen for tilknytningen **Kreditorer V2 (msdyn\_vendors)**. Alle rækker synkroniseres, fordi ændringssporing er deaktiveret.
7. Slå ændringssporing til igen for tabellen **Kreditorer V2**.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Løse fejl i tabeltilknytningen V3–to–Accounts for debitorer

Du kan støde ind i indledende synkroniseringsfejl for tilknytning af **Kreditorer V3** til **Konti**, hvis tabellerne har eksisterende rækker med værdier i kolonnerne **ContactPersonId** og **InvoiceAccount**. Disse fejl opstår, fordi **InvoiceAccount** er en selvrefererende kolonne, og **ContactPersonID** er en cirkulær reference i kreditortilknytningen.

De fejlmeddelelser, du modtager, har følgende form.

*GUID for feltet kunne ikke fortolkes: \<field\>. Opslaget blev ikke fundet: \<value\>. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Her er nogle eksempler:

- *GUID for feltet kunne ikke fortolkes: primarycontactid.msdyn\_contactpersonid. Opslaget blev ikke fundet: 000056. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *GUID for feltet kunne ikke fortolkes: msdyn\_billingaccount.accountnumber. Opslaget blev ikke fundet: 1206-1. Prøv følgende URL-adresse(r) for at kontrollere, om referencedataene findes: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Hvis der er rækker i debitortabellen med værdier i kolonnerne **ContactPersonID** og **InvoiceAccount**, skal du følge disse trin for at fuldføre den første synkronisering. Du kan bruge denne fremgangsmåde til alle indbyggede tabeller, f.eks. **Konti** og **Kontakter**.

1. I appen Finans og drift skal du slette kolonnerne **ContactPersonID** og **InvoiceAccount** fra tilknytningen **Debitorer V3 (konti)** og derefter gemme tilknytningen.

    1. Gå til siden med dobbeltskrivning-tilknytning for **Debitorer V3 (konti)**, og vælg fanen **Tabeltilknytninger**. I venstre filter skal du vælge **Finans og driftsapps.Debitorer V3**. I højre filter skal du vælge **Dataverse.Account**.
    2. Søg efter **contactperson** for at finde kildekolonnen **ContactPersonID**.
    3. Vælg **Handlinger**, og vælg derefter **Slet**.

        ![Sletning af kolonnen ContactPersonID.](media/cust_selfref3.png)

    4. Gentag disse trin for at slette kolonnen **InvoiceAccount**.

        ![Sletning af kolonnen InvoiceAccount.](media/cust_selfref4.png)

    5. Gem ændringerne i tilknytningen.

2. Slå ændringssporing fra for tabellen **Debitorer V3**.

    1. I arbejdsområdet **Datastyring** skal du markere feltet **Datatabeller**.
    2. Vælg tabellen **Debitorer V3**.
    3. I handlingsruden skal du vælge **Indstillinger** og derefter vælge **Ændringssporing**.

        ![Valg af indstillingen Ændringssporing.](media/selfref_options.png)

    4. Vælg **Deaktiver ændringssporing**.

        ![Valg af Deaktiver ændringssporing.](media/selfref_tracking.png)

3. Kør den første synkronisering for tilknytningen **Debitorer V3 (konti)**. Den første synkronisering skal køres uden fejl.
4. Kør den første synkronisering for tilknytningen **CDS kontakter V2 (kontakter)**.

    > [!NOTE]
    > Der er to tilknytninger med samme navn. Vælg tilknytningen med følgende beskrivelse under fanen **Detaljer**: **Dobbeltskrivningsskabelon for synkronisering mellem FO.CDS Kreditorkontakter V2 til CDS.Contacts. Kræver ny pakke \[Dynamics365SupplyChainExtended\].**

5. Tilføj kolonnerne **InvoiceAccount** og **ContactPersonId** igen i tilknytningen **Debitorer V3 (konti)**, og gem tilknytningen. Nu er både kolonnen **InvoiceAccount** og kolonnen **ContactPersonId** igen en del af den direkte synkroniseringstilstand. I det næste trin udfører du den første synkronisering for disse kolonner.
6. Kør den første synkronisering igen for tilknytningen **Debitorer V3 (konti)**. Da ændringssporing er slået fra, bliver dataene for **InvoiceAccount** og **ContactPersonId** synkroniseret fra appen Finans og drift til Dataverse.
7. Hvis du vil synkronisere dataene for **InvoiceAccount** og **ContactPersonId** fra Dataverse til appen Finans og drift, skal du bruge et dataintegrationsprojekt.

    1. I Power Apps skal du oprette et dataintegrationsprojekt mellem tabellerne **Sales.Account** og **Finans- og driftsapps.Debitorer V3**. Dataretningen skal ligge fra Dataverse til appen Finans og drift. Da **InvoiceAccount** er en ny attribut i dobbeltskrivning, kan det være en god idé at springe den første synkronisering over for den. Du kan finde flere oplysninger under [Integrere data i Dataverse](/power-platform/admin/data-integrator).

        Følgende illustration viser et projekt, der opdaterer **CustomerAccount** og **ContactPersonId**.

        ![Dataintegrationsprojektet, der skal opdatere CustomerAccount og ContactPersonId.](media/cust_selfref6.png)

    2. Tilføj firmakriterierne i filteret på Dataverse-siden, så kun de rækker, der opfylder filterkriterierne, opdateres i appen Finans og drift. Hvis du vil tilføje et filter, skal du vælge filterknappen. I dialogboksen **Rediger forespørgsel** kan du tilføje en filterforespørgsel som **\_msdyn\_company\_value eq '\<guid\>'**.

        > [BEMÆRK] Hvis filterknappen ikke er til stede, skal du oprette en supportanmodning for at bede dataintegrationsteamet om at aktivere filtreringsfunktionen på din lejer.

        Hvis du ikke indtaster en filterforespørgsel for **\_msdyn\_company\_value**, synkroniseres alle rækker.

        ![Tilføjelse af en filterforespørgsel.](media/cust_selfref7.png)

    Den første synkronisering af rækkerne er nu fuldført.

8. Aktivér ændringssporing igen i appen Finans og drift for tabellen **Debitorer V3**.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>Første synkroniseringsfejl på oversigter med mere end 10 opslagsfelter

Du kan få vist følgende fejlmeddelelse, når du forsøger at køre en første synkroniseringsfejl i **Debitor V3 – Konti**, tilknytninger af **Salgsordrer** eller en oversigt med mere end 10 opslagsfelter:

*CRMExport: Pakkeudførelse fuldført. Fejlbeskrivelse: 5 forsøg på at hente data fra https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc failed.*

På grund af opslagsbegrænsningen i forespørgslen mislykkes den første synkronisering, når enhedstilknytningen indeholder mere end 10 opslag. Yderligere oplysninger finder du i [Hente relaterede tabelposter med en forespørgsel](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Følg disse trin for at løse dette problem:

1. Fjern valgfrie opslagsfelter fra enhedsoversigten for dobbeltskrivning, så antallet af opslag er 10 eller færre.
2. Gem oversigten, og udfør den første synkronisering.
3. Når den første synkronisering af det første trin lykkes, skal du tilføje de resterende opslagsfelter og fjerne de opslagsfelter, du har synkroniseret i første trin. Sørg for, at antallet af opslagsfelter er 10 eller færre. Gem oversigten, og kør den første synkronisering.
4. Gentag disse trin, indtil alle opslagsfelter er synkroniseret.
5. Føj alle opslagsfelterne tilbage til oversigten, gem oversigten, og kør oversigten den **Spring første synkronisering over**.

Denne proces aktiverer oversigten for live-synkroniseringstilstand.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Kendt problem under første synkronisering af parts postadresser og elektroniske adresser

Du kan få vist følgende fejlmeddelelse, når du prøver at køre den første synkronisering af parts postadresser og elektroniske adresser:

*Partnummer blev ikke fundet i Dataverse.*

Der er angivet et interval på **DirPartyCDSEntity** i Finans og driftsapps, der filtrerer parter af typen **Person** og **Organisation**. Som følge heraf vil en første synkronisering af tilknytningen **CDS-parter – msdyn_parties** ikke synkronisere parter af andre typer, herunder **Juridisk enhed** og **Driftsenhed**. Når den første synkronisering køres for **CDS-parts postadresser (msdyn_partypostaladdresses)** eller **Partkontakter V3 (msdyn_partyelectronicaddresses)**, kan du få modtage fejlmeddelelsen.

Vi arbejder på en rettelse for at fjerne parttypeintervallet på Finans og drift-enheden, så parter af alle typer kan synkroniseres med Dataverse uden problemer.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Er der problemer med ydeevnen under den første synkronisering af debitor- eller kontaktdata?

Hvis du har kørt den første synkronisering af data for **Debitor** og har aktive tilknytninger af typen **Debitor**, og du derefter kører den første synkronisering af data for **Kontakter**, kan der være problemer med ydeevnen under indsættelser og opdateringer til tabellerne **LogisticsPostalAddress** og **LogisticsElectronicAddress** for adresser for **Kontakter**. Samme globale postadresse og elektroniske adressetabeller spores for **CustCustomerV3Entity** og **VendVendorV2Entity**, og dobbeltskrivning forsøger at oprette flere forespørgsler for at skrive data til en anden side. Hvis du allerede har kørt den første synkronisering for **Debitor**, skal du stoppe den tilsvarende oversigt, mens du kører den første synkronisering af data for **Kontakter**. Gør det samme med data for **Kreditor**. Når den første synkronisering er fuldført, kan du køre alle oversigterne ved at springe over den første synkronisering.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
