---
title: Opgradere til modellen med part- og globalt adressekartotek
description: Dette emne indeholder en beskrivelse af, hvordan du opgraderer dobbeltskrivningsdata til modellen med part- og globalt adressekartotek.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941077"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Opgradere til modellen med part- og globalt adressekartotek

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Azure Data Factory-skabelonen](https://aka.ms/dual-write-gab-adf) hjælper dig med at opgradere eksisterende tabeldata for **Konto**, **Kontakt** og **Leverandør** i dobbeltskrivning til part- og det globale adressekartoteks model. Skabelonen afstemmer dataene fra både Finance and Operations-apps og programmer til kundeengagement. I slutningen af processen oprettes der **Part**- og **Kontakt**-felter for **Part**-poster, som knyttes til posterne **Konto**, **Kontakt** og **Leverandør** i kundeengagementsprogrammer. Der genereres en .csv-fil (`FONewParty.csv`) for at oprette nye **Part**-poster i Finance and Operations-appen. Dette emne indeholder instruktioner til brug af Data Factory-skabelonen og opgradering af dine data.

Hvis du ikke har tilpasninger, kan du bruge skabelonen, som den er. Hvis du har tilpasninger af **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonen ved hjælp af følgende vejledning.

> [!Note]
> Skabelonen hjælper kun med at opgradere **Part**-dataene. I en fremtidig version inkluderes post- og elektroniske adresser.

## <a name="prerequisites"></a>Forudsætninger

Disse forudsætninger er obligatoriske:

+ [Azure-abonnement](https://portal.azure.com/)
+ [Adgang til skabelonen](https://aka.ms/dual-write-gab-adf)
+ Du er eksisterende dobbeltskrivningskunde.

## <a name="prepare-for-the-upgrade"></a>Forberede opgraderingen

+ **Fuldt synkroniseret**: Begge miljøer er synkroniseret fuldstændigt for **Konto (kunde)**, **Kontakt** og **Leverandør**.
+ **Integrationsnøgler**: **Konto (kunde)**, **Kontakt** og **Leverandør** tabeller i kundeengagementapps bruger de integrationsnøgler, der leveres som standard. Hvis du har tilpasset integrationsnøglerne, skal du tilpasse skabelonen.
+ **Partnummer**: Alle **Konto (kunde)**, **Kontakt** og **Leverandør** poster, der skal opgraderes, har et **Part**-nummer. Poster uden et **Part**-nummer ignoreres. Hvis du vil opgradere disse poster, skal du føje et **Part**-nummer til dem, før du starter opgraderingsprocessen.
+ **Systemnedlukning**: Under opgraderingsprocessen skal både Finance and Operations og kundeengagementsmiljøer være offline.
+ **Øjebliksbillede**: Tag øjebliksbilleder af både Finance and Operations og kundeengagementapps. Du kan bruge øjebliksbillederne til at gendanne den forrige tilstand, hvis det er nødvendigt.

## <a name="deployment"></a>Installation

1. Hent skabelonen fra [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).

2. Log på [Microsoft Azure](https://portal.azure.com/).

3. Opret en [ressourcegruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Opret en [lagerkonto](/azure/storage/common/storage-account-create?tabs=azure-portal) i den ressourcegruppe, du har oprettet.

5. Opret en [datafabrik](/azure/data-factory/quickstart-create-data-factory-portal) i den ressourcegruppe, du har oprettet ovenfor.

6. Åbn datafabrikken, og vælg feltet **Forfatter og overvåger**.

7. Vælg **ARM-skabelon** under fanen **Administrer**.

8. Vælg **Importér ARM-skabelon** for at importere **Part**-skabelonen.

9. Importér skabelonen til datafabrikken. Angiv følgende værdier for **Projektdetaljer** og **Forekomstdetaljer**.

    Felt | Værdi
    ---|---
    Abonnement | Azure-abonnement
    Ressourcegruppe | Angiv den samme ressource, som lagerkontoen oprettes under.
    Land/område | Angiv område.
    Navn på fabrik | Angiv fabriksnavnet.
    Hovednøgle til sammenkædet service | Angiv programnøglen.
    Forbindelsesstreng til Azure Blob Storage | Forbindelsesstrengen til Azure Blob Storage.
    Dynamics CRM-sammenkædet serviceadgangskode | Adgangskoden for den brugerkonto, du har angivet som brugernavn.
    FO-sammenkædet Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO-sammenkædet Service_properties_type Properties_tenant | Angiv de lejeroplysninger (domænenavn eller lejer-id), hvor dit program er placeret.
    FO-sammenkædet Service_properties_type Properties_aad ressource-id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO-sammenkædet Service_properties_type Properties_service hoved-id | Angiv programmets klient-id.
    Dynamics CRM-sammenkædet Service_properties_type Properties_username | Det brugernavn, der skal forbindes med Dynamics.

    Du kan finde flere oplysninger i [Manuelt promovere en Resource Manager-skabelon for hvert miljø](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Sammenkædede tjenesteegenskaber](/azure/data-factory/connector-dynamics-ax#linked-service-properties) og [Kopiere data vha. Azure Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Efter installationen skal du validere datasæt, dataflow og tilknyttet tjeneste for datafabrikken.

   ![Datasæt, dataflow og tilknyttet tjeneste](media/data-factory-validate.png)

11. Naviger til **Administrer**. Vælg **Sammenkædet tjeneste** under **Forbindelser**. Vælg **DynamicsCrmLinkedService**. Angiv følgende værdier i formularen **Rediger sammenkædet tjeneste (Dynamics CRM)**:

    Felt | Værdi
    ---|---
    Navn | DynamicsCrmLinkedService
    Betegnelse | Sammenkædede tjenester, der bruges til at oprette forbindelse til CRM-forekomst for at hente data til enheder
    Oprette forbindelse via integrationskørsel | AutoResolvelntegrationRuntime
    Installationstype | Online
    Tjeneste-URI | `https://<organization-name>.crm[x].dynamics.com`
    Godkendelsestype | Office365
    Brugernavn |
    Adgangskode eller Azure Key Vault | Adgangskode
    Adgangskode |

## <a name="run-the-template"></a>Køre skabelonen

1. Stop følgende dobbeltskrivning af **Konto**, **Kontakt** og **Leverandør** ved hjælp af appen Finance and Operations.

    + Debitorer V3 (konti)
    + Debitorer V3 (kontakter)
    + CDS-kontakter V2 (kontakter)
    + CDS-kontakter V2 (kontakter)
    + Kreditor V2 (msdyn_vendor)

2. Kontrollér, at tilknytningerne er fjernet fra `msdy_dualwriteruntimeconfig`-tabellen i Dataverse.

3. Installer [Løsninger til part og globalt adressekartotek for dobbeltskrivning](https://aka.ms/dual-write-gab) fra AppSource.

4. Hvis følgende tabeller indeholder data i appen Finance and Operations, skal du køre **Første synkronisering** for dem.

    + Tiltaleformer
    + Personlige tegntyper
    + Afsluttende hilsner
    + Titler på kontaktpersoner
    + Beslutningstagerrolle
    + Loyalitetsniveauer

5. Deaktiver følgende plugin-trin i kundeengagementsappen.

    + Opdater konto
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto
    + Opdatering af kontakt
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt
    + Opdatering af msdyn_party
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party
    + Opdatering af msdyn_vendor
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor

6. Deaktiver følgende arbejdsflows i kundeengagementsappen:

    + Opret kreditorer i tabellen Konti
    + Opret kreditorer i tabellen Konti
    + Opret kreditorer af typen Person i tabellen Kontakter
    + Opret kreditorer af typen Person i tabellen Kreditorer
    + Opdater kreditorer i tabellen Konti
    + Opdater kreditorer i tabellen Kreditorer
    + Opdater kreditorer af typen Person i tabellen Kontakter
    + Opdater kreditorer af typen Person i tabellen Kreditorer

7. På datafabrikken skal du køre skabelonen ved at vælge **Udløs nu** som vist på følgende billede. Det kan tage et par timer, før denne proces er fuldført, afhængigt af datavolumen.

    ![Udløserkørsel](media/data-factory-trigger.png)

    > [!NOTE]
    > Hvis du har tilpasninger af **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonen.

8. Importér de nye **Part**-poster i Finance and Operations-appen.

    + Download filen `FONewParty.csv` fra Azure Blob Storage. Stien er `partybootstrapping/output/FONewParty.csv`.
    + Konverter filen `FONewParty.csv` til en Excel-fil, og importér Excel-filen til Finance and Operations-appen.  Hvis csv-importen fungerer for dig, kan du importere csv-filen direkte. Det kan tage et par timer at importere, afhængigt af datavolumen. Du kan finde flere oplysninger i [Oversigt over dataimport og eksportjob](../data-import-export-job.md).

    ![Importere Dataverse-partposterne](media/data-factory-import-party.png)

9. Aktivér følgende plugin-trin i kundeengagementsapps:

    + Opdater konto
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto
    + Opdatering af kontakt
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt
    + Opdatering af msdyn_party
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party
    + Opdatering af msdyn_vendor
         + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor

10. I apps til kundeengagement skal du aktivere følgende arbejdsgange, hvis du deaktiverede dem i forrige trin:

    + Opret kreditorer i tabellen Konti
    + Opret kreditorer i tabellen Konti
    + Opret kreditorer af typen Person i tabellen Kontakter
    + Opret kreditorer af typen Person i tabellen Kreditorer
    + Opdater kreditorer i tabellen Konti
    + Opdater kreditorer i tabellen Kreditorer
    + Opdater kreditorer af typen Person i tabellen Kontakter
    + Opdater kreditorer af typen Person i tabellen Kreditorer

11. Kør de **Part**-relaterede kort som beskrevet i [Part- og globalt adressekartotek](party-gab.md).

## <a name="troubleshooting"></a>Fejlfinding

1. Hvis processen mislykkes, skal du køre datafabrikken igen med start fra den mislykkede aktivitet.
2. Nogle filer genereres af datafabrikken, som du kan bruge til datavalideringsformål.
3. Datafabrikken kører på basis af csv-filer, der er kommaseparerede. Hvis der er en feltværdi med komma, kan den forstyrre resultaterne. Du skal fjerne kommaerne.
4. Fanen **Overvågning** indeholder oplysninger om alle trin og data, der er behandlet. Vælg et bestemt trin for at fejlfinde det.

    ![Fanen Overvågning](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Få mere at vide om skabelonen

Du kan finde kommentarer til skabelonen i filen [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).