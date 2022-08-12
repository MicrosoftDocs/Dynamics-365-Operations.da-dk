---
title: Opgradere til modellen med part- og globalt adressekartotek
description: Denne artikel indeholder en beskrivelse af, hvordan du opgraderer dobbeltskrivningsdata til modellen med part- og globalt adressekartotek.
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 02ab3675db0d78efa1e4e43188d79bb1e763a713
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111812"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Opgradere til modellen med part- og globalt adressekartotek

[!include [banner](../../includes/banner.md)]



[Microsoft Azure Data Factory-skabeloner](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) hjælper dig med at opgradere følgende eksisterende data i dobbeltskrivning til part- det globale adressekartoteks model: Data i **Konto**-, **Kontakt**- og **Leverandør**-tabeller og elektroniske adresser.

Der findes følgende tre Data Factory-skabeloner. De afstemmer dataene fra både programmer til finans og drift og apps til kundeengagement.

- **[Partskabelon](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (opgradering af data til skemaer for leverandør-styklister til part-GAB skema/arm_template.json)** – denne skabelon hjælper med at opgradere oplysninger om **part**- og **kontaktperson**, der er knyttet til **konto**-, **kontakt**- og **kreditordata**.
- **[Skabelon til partpostadresse](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (opgradering af data i dobbeltskrivning til part-GAB-skema/opgradering til part-postadresse - GAB/arm_template.json)** – Denne skabelon hjælper med at opgradere de postadresser, der er tilknyttet **konto**-, **kontaktperson**- og **kreditordata**.
- **[Skabelon til part-elektronisk adresse](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (opgradering af data i dobbeltskrivning til part-GAB-skema/opgradering til part-elektronisk adresse - GAB/arm_template.json)** – Denne skabelon hjælper med at opgradere de elektroniske adresser, der er tilknyttet **konto**-, **kontaktperson**- og **kreditordata**.

I slutningen af processen genereres følgende kommaseparerede værdier (.csv).

| Filnavn | Formål |
|---|---|
| FONewParty.csv | Denne fil opretter nye **Part**-poster i programmet til finans og drift. |
| ImportFONewPostalAddressLocation.csv | Denne fil hjælper med at oprette nye **Postadresseplacering**-poster i programmet til finans og drift. |
| ImportFONewPartyPostalAddress.csv | Denne fil hjælper med at oprette nye **Partpostadresse**-poster i programmet til finans og drift. |
| ImportFONewPostalAddress.csv | Denne fil hjælper med at oprette nye **Postadresse**-poster i programmet til finans og drift. |
| ImportFONewElectronicAddress.csv | Denne fil hjælper med at oprette nye **Elektronisk adresse**-poster i Programmet til finans og drift. |

Denne artikel beskriver, hvordan du bruger Data Factory-skabeloner og opgraderer dine data. Hvis du ikke har tilpasninger, kan du bruge skabelonerne, som de er. Hvis du har tilpasninger af data i **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonerne ved hjælp af vejledningen i denne artikel.

> [!IMPORTANT]
> Der er specielle instruktioner for kørsel af skabeloner for partens postadresse og partens elektroniske adresse. Du skal køre partskabelonen først, derefter skabelonen for partpostadressen og derefter skabelonen for den elektroniske partadresse. Hver skabelon er designet til at blive importeret på en separat datafabrik.

## <a name="prerequisites"></a>Forudsætninger

Der kræves følgende forudsætninger for at opgradere til partmodellen og modellen for det globale adressekartotek:

+ Du skal have et [Azure-abonnement](https://portal.azure.com/).
+ Du skal have adgang til [skabelonerne](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Du skal være eksisterende dobbeltskrivningskunde.

## <a name="prepare-for-the-upgrade"></a>Forberede opgraderingen

En opgradering kræver følgende forberedelse:

+ **Fuld synkronisering:** Både Finans og drift-miljøet og kundeengagement-miljøet er i fuldt synkroniseret tilstand for tabellerne **Konto (Kunde)**, **Kontaktperson** og **Leverandør**.
+ **Integrationsnøgler:** **Konto (kunde)**, **Kontakt** og **Leverandør** tabeller i kundeengagementapps bruger de integrationsnøgler, der leveres som standard. Hvis du har tilpasset integrationsnøglerne, skal du tilpasse skabelonen.
+ **Partnummer:** Alle **Konto (kunde)**-, **kontakt**- og **Leverandør**-poster, der skal opgraderes, har et part-nummer. Poster, der ikke har et partnummer, ignoreres. Hvis du vil opgradere disse poster, skal du føje et part-nummer til dem, før du starter opgraderingsprocessen.
+ **Systemnedlukning:** Under opgraderingsprocessen skal både Finans- og driftsmiljøet og kundeengagementsmiljøet være offline.
+ **Øjebliksbillede:** Tag øjebliksbilleder af både programmer til finans og drift og kundeengagementapps. Du kan bruge øjebliksbillederne til at gendanne den forrige tilstand, hvis det er nødvendigt.

## <a name="deployment"></a>Udrulning

1. Hent skabelonerne fra [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Log på [Azure-portalen](https://portal.azure.com/).
3. Opret en [ressourcegruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Opret en [lagerkonto](/azure/storage/common/storage-account-create?tabs=azure-portal) i den ressourcegruppe, du har oprettet.
5. Opret en [datafabrik](/azure/data-factory/quickstart-create-data-factory-portal) i den ressourcegruppe, du har oprettet.
6. Åbn datafabrikken, og vælg feltet **Forfatter og overvåger**.
7. Vælg **ARM-skabelon** under fanen **Administrer**.
8. Vælg **Importér ARM-skabelon** for at importere **Part**-skabelonen.
9. Importér skabelonen til datafabrikken. Angiv følgende værdier for **Projektdetaljer** og **Forekomstdetaljer**.

    | Felt | Værdi |
    |---|---|
    | Abonnement | Azure-abonnement |
    | Ressourcegruppe | Angiv den samme ressource, som lagerkontoen oprettes under. |
    | Land/område | Området |
    | Navn på fabrik | Navn på fabrik |
    | Hovednøgle til sammenkædet service | App-nøgle |
    | Forbindelsesstreng til Azure Blob Storage | Forbindelsesstreng til Azure Blob Storage |
    | Dynamics CRM-sammenkædet serviceadgangskode | Adgangskoden for den brugerkonto, du har angivet som brugernavn |
    | FO-sammenkædet Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO-sammenkædet Service_properties_type Properties_tenant | Angiv de lejeroplysninger (domænenavn eller lejer-id), hvor dit program er placeret |
    | FO-sammenkædet Service_properties_type Properties_aad ressource-id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO-sammenkædet Service_properties_type Properties_service hoved-id | Programmets klient-id |
    | Dynamics CRM-sammenkædet Service_properties_type Properties_username | Det brugernavn, der skal forbindes med Dynamics 365 |

    Du kan finde flere oplysninger under følgende emner:

    - [Opgradere en Resource Manager-skabelon manuelt for hvert miljø](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Egenskaber for sammenkædet tjeneste](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Kopiere data ved hjælp af Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Efter installationen skal du validere datasæt, dataflow og tilknyttet tjeneste for datafabrikken.

    ![Datasæt, dataflow og tilknyttet tjeneste.](media/data-factory-validate.png)

11. Gå til **Administrer**. Vælg **Sammenkædet tjeneste** under **Forbindelser**. Vælg derefter **DynamicsCrmLinkedService**. Angiv følgende værdier i dialogboksen **Rediger sammenkædet tjeneste (Dynamics CRM)**.

    | Felt | Værdi |
    |---|---|
    | Navn | DynamicsCrmLinkedService |
    | Betegnelse | Sammenkædede tjenester, der bruges til at oprette forbindelse til CRM-forekomst for at hente data til enheder |
    | Oprette forbindelse via integrationskørsel | AutoResolvelntegrationRuntime |
    | Installationstype | Online |
    | Tjeneste-URI | `https://<organization-name>.crm[x].dynamics.com` |
    | Godkendelsestype | Office365 |
    | Brugernavn | |
    | Adgangskode eller Azure Key Vault | Adgangskode |
    | Adgangskode | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Forberede kørsel af Data Factory-skabeloner

Dette afsnit indeholder en beskrivelse af den opsætning, der kræves, før du kører Data Factory-skabelonerne for partpostadresse og part-elektronisk adresse.

### <a name="setup-to-run-the-party-postal-address-template"></a>Opsætning af, hvordan skabelonen til partspostadresse køres

1. Log på kundedementeringsapps, og gå til **Indstillinger** \> **Personlige indstillinger**. Konfigurer derefter på fanen **Generelt** tidszoneindstillingen for systemadministrationskontoen. Tidszonen skal være i Coordinated Universal Time (UTC) for at opdatere datoerne for "gyldig fra" og "gyldig til" for postadresser fra programmer til finans og drift.

    ![Tidszoneindstillingen for systemadministratorkontoen.](media/ADF-1.png)

2. I Data Factory under fanen **Administrer** under **Globale parametre** skal du oprette følgende globale parameter.

    | Tal | Navn | Type | Værdi |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | streng | Denne parameter føjer et serienummer til nyoprettede postadresser som præfiks. Sørg for at angive en streng, der ikke er i konflikt med postadresser i programmer til finans og drift og kundeengagement-apps. Du kan for eksempel bruge **ADF-PAD-**. |

    ![Den globale parameter PostalAddressIdPrefix, der er oprettet under fanen Administrer.](media/ADF-2.png)

3. Vælg **Publicér alle**, når du er færdig.

    ![Knappen Publicér alle.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Opsætning af, hvordan skabelonen til part-elektronikadresse køres

1. I Data Factory under fanen **Administrer** under **Globale parametre** skal du oprette følgende globale parametre.

    | Tal | Navn | Type | Værdi |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Denne parameter bestemmer, hvilke primære systemadresser der erstattes i tilfælde af konflikter. Hvis værdien er **sand**, erstatter den primære adresse i programmer til finans og drift de primære adresser i kundeengagementsapps. Hvis værdien er **falsk**, erstatter den primære adresse i kundeengagementsapps de primære adresser i programmer til finans og drift. |
    | 2 | ElectronicAddressIdPrefix | streng | Denne parameter føjer et serienummer til nyoprettede elektroniske adresser som præfiks. Sørg for at angive en streng, der ikke er i konflikt med elektroniske adresser i programmer til finans og drift og kundeengagement-apps. Du kan for eksempel bruge **ADF-EAD-**. |

    ![Globale parametre for IsFOSource og ElectronicAddressIdPrefix, der er oprettet under fanen Administrer.](media/ADF-4.png)

2. Vælg **Publicér alle**, når du er færdig.

## <a name="run-the-templates"></a>Køre skabelonerne

1. Stop følgende dobbeltskrivningstilknytninger af **Part**, **Konto**, **Kontakt** og **Leverandør**, der bruger programmer til finans og drift:

    + CDS-parter (msdyn_parties) 
    + Debitorer V3 (konti)
    + Debitorer V3 (kontakter)
    + CDS-kontakter V2 (kontakter)
    + CDS-kontakter V2 (kontakter)
    + Kreditor V2 (msdyn_vendor)
    + Kontakter V2 (msdyn_contactforparties)
    + Placeringer af CDS-partpostadresser (msdyn_partypostaladdresses)
    + CDS-postadressehistorik V2 (msdyn_postaladdresses)
    + Placeringer af CDS-postadresser (msdyn_postaladdresscollections)
    + Partkontakter V3 (msdyn_partyelectronicaddresses)

2. Kontrollér, at tilknytningerne er fjernet fra **msdy_dualwriteruntimeconfig** tabellen i Dataverse.
3. Installer [Løsninger til part og globalt adressekartotek for dobbeltskrivning](https://aka.ms/dual-write-gab) fra AppSource.
4. Hvis følgende tabeller indeholder data i programmet til finans og drift, skal du køre **Første synkronisering**.

    + Tiltaleformer
    + Personlige tegntyper
    + Afsluttende hilsner
    + Titler på kontaktpersoner
    + Beslutningstagerrolle
    + Loyalitetsniveauer

5. Deaktiver følgende plugin-trin i kundeengagementsappen:

    + Kontoopdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto

    + Opdatering af kontakt

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt

    + Opdatering af msdyn_party

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party

    + Opdatering af msdyn_vendor

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor

    + Customeraddress

        + Opret

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Oprettelse af customeraddress

        + Opdater

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Opdatering af customeraddress

        + Slet

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: Sletning af customeraddress

    + msdyn_partypostaladdress

        + Opret

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Oprettelse af msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Oprettelse af msdyn_partypostaladdress

        + Opdater

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Opdatering af msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Opdatering af msdyn_partypostaladdress

    + msdyn_postaladdress

        + Opret

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Oprettelse af msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Oprettelse af msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Oprettelse af msdyn_postaladdress

        + Opdater

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Opdatering af msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Opdatering af msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Opret

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Oprettelse af msdyn_partyelectronicaddress

        + Opdater

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Opdatering af msdyn_partyelectronicaddress

        + Slet

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Sletning af msdyn_partyelectronicaddress

6. Deaktiver følgende arbejdsflows i kundeengagementsappen:

    + Opret kreditorer i tabellen Konti
    + Opret kreditorer i tabellen Konti
    + Opret kreditorer af typen Person i tabellen Kontakter
    + Opret kreditorer af typen Person i tabellen Kreditorer
    + Opdater kreditorer i tabellen Konti
    + Opdater kreditorer i tabellen Kreditorer
    + Opdater kreditorer af typen Person i tabellen Kontakter
    + Opdater kreditorer af typen Person i tabellen Kreditorer

7. På datafabrikken skal du køre skabelonen ved at vælge **Udløs nu** som vist på følgende illustration. Det kan tage et par timer, før denne proces er fuldført, afhængigt af datavolumen.

    ![Køre skabelonen.](media/data-factory-trigger.png)

    > [!NOTE]
    > Hvis du har tilpasninger af **Konto**, **Kontakt** og **Leverandør**, skal du redigere skabelonen.

8. Importér de nye **Part**-poster i programmet til finans og drift.

    1. Download filen **FONewParty.csv** fra Azure Blob Storage. Stien er **partybootstrapping/output/FONewParty.csv**.
    2. Konverter filen **FONewParty.csv** til en Excel-fil, og importér Excel-filen til programmet til finans og drift. Hvis CSV-importen fungerer for dig, kan du importere .csv-filen direkte. Det kan tage et par timer, før denne proces er fuldført, afhængigt af datavolumen. Du kan finde flere oplysninger i [Oversigt over dataimport og eksportjob](../data-import-export-job.md).

    ![Importere Dataverse-partposterne.](media/data-factory-import-party.png)

9. På Data Factory skal du køre skabelonen for partpostadresser og elektroniske partadresser én ad hinanden.

    + Partpostadresseskabelonen konfigurerer alle postadresseposter i kundeengagement-appen og knytter dem til de tilsvarende **konto**-, **kontaktperson**- og **kredit**-poster. Der genereres også tre .csv-filer: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv og ImportFONewPostalAddress.csv.
    + Part-elektroniske adresseskabelonen konfigurerer alle elektroniske adresser i kundeengagement-appen og knytter dem til de tilsvarende **konto**-, **kontaktperson**- og **kredit**-poster. Der genereres også en .csv-fil: ImportFONewElectronicAddress.csv.

    ![Køre skabeloner til partspostadresse og partelektroniske adresser.](media/ADF-7.png)

10. Hvis du vil opdatere programmet til finans og drift med disse data, skal du konvertere .csv-filerne til en Excel-projektmappe og [importere den til programmet til finans og drift](../data-import-export-job.md). Hvis CSV-importen fungerer for dig, kan du importere .csv-filer direkte. Det kan tage et par timer, før denne proces er fuldført, afhængigt af volumen.

    ![Vellykket import.](media/ADF-8.png)

11. Aktivér følgende plugin-trin i kundeengagement-app:

    + Kontoopdatering

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Opdatering af konto
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Opdatering af konto

    + Opdatering af kontakt

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Opdatering af kontakt
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Opdatering af kontakt

    + Opdatering af msdyn_party

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Opdatering af msdyn_party

    + Opdatering af msdyn_vendor

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Opdatering af msdyn_vendor

    + msdyn_partypostaladdress

        + Opret

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Oprettelse af msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Oprettelse af msdyn_partypostaladdress

        + Opdater

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Opdatering af msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Opdatering af msdyn_partypostaladdress

    + msdyn_postaladdress

        + Opret

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Oprettelse af msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Oprettelse af msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Oprettelse af msdyn_postaladdress

        + Opdater

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Opdatering af msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Opdatering af msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Opret

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Oprettelse af msdyn_partyelectronicaddress

        + Opdater

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Opdatering af msdyn_partyelectronicaddress

        + Slet

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Sletning af msdyn_partyelectronicaddress

12. I apps til kundeengagement skal du aktivere følgende arbejdsgange, hvis du tidligere har deaktiveret dem:

    + Opret kreditorer i tabellen Konti
    + Opret kreditorer i tabellen Konti
    + Opret kreditorer af typen Person i tabellen Kontakter
    + Opret kreditorer af typen Person i tabellen Kreditorer
    + Opdater kreditorer i tabellen Konti
    + Opdater kreditorer i tabellen Kreditorer
    + Opdater kreditorer af typen Person i tabellen Kontakter
    + Opdater kreditorer af typen Person i tabellen Kreditorer

13. Kør de **Part**-postrelaterede kort som beskrevet i [Part- og globalt adressekartotek](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Forklaring på Data Factory-skabeloner

I dette afsnit gennemgås trinnene i hver Data Factory-skabelon.

### <a name="steps-in-the-party-template"></a>Trin i part-skabelonen

1. Trin 1 til 6 identificerer de firmaer, der er aktiveret til dobbeltskrivning og bygger en filtersætning til dem.
2. Trin 7-1 til og med 7-9 henter data fra både programmet til finans og drift og kundeengagement-app og trindata til opgradering.
3. Trin 8 til 9 sammenligner partnummeret for posterne **Konto**, **Kontakt** og **Leverandør** mellem programmet til finans og drift og kundeengagementsappen. Alle poster, der ikke har et partnummer, ignoreres.
4. Trin 10 genererer to .csv-filer til de partposter, der skal oprettes i kundeengagements-appen og programmet til finans og drift.

    - **FOCDSParty.csv** – Denne fil indeholder alle partposter i begge systemer, uanset om firmaet er aktiveret til dobbeltskrivning.
    - **FONewParty.csv** – Denne fil indeholder et undersæt af de partposter, der er opmærksom på Dataverse (f.eks. konti af typen **Kundeemne**).

5. Trin 11 opretter parterne i kundeengagements-appen.
6. Trin 12 henter de globalt entydige id'er (GUID) for parterne fra kundeengagement-app og tilrettelægger dem, så de kan knyttes til poster for **konto**, **kontaktperson** og **kreditor** i efterfølgende trin.
7. Trin 13 knytter poster for **Konto**, **Kontakt** og **Kreditor** til part-GUID'er.
8. Trin 14-1 til og med 14-3 opdaterer **konto**-, **kontaktperson**- og **leverandør**-posterne i kundeengagement-appen med part-GUID'er.
9. Trin 15-1 til 15-3 forbereder **kontaktperson til part**-poster for **konto**-, **kontaktperson**- og **kreditor**-poster.
10. Trin 16-1 til og med 16-7 henter referencedata, som f.eks. tiltaleformer og personlige tegntyper, og knytter dem til **kontakt for partposter**.
11. Trin 17 flettes med **kontaktperson til part**-poster for **konto**-, **kontaktperson**- og **kreditor**-poster.
12. Trin 18 importerer **Kontakt for partposter** til kundens aftale-app.

### <a name="steps-in-the-party-postal-address-template"></a>Trin i skabelonen til partspostadresse

1. Trin 1-1 til og med 1-10 henter data fra både programmet til finans og drift og kundeengagement-app og trindata til opgradering.
2. Trin 2 af-normaliserer postadressedataene i programmet til finans og drift ved at sammensætte postadressen og partpostadressen.
3. Trin 3 de-duplikerer og fletter konto-, kontakt- og leverandøradressedata fra kundeengagement-appen.
4. Trin 4 opretter .csv-filer til programmet til finans og drift for at oprette nye adressedata, der er baseret på konto-, kontakt- og kreditoradresser.
5. Trin 5-1 opretter .csv-filer til kundeengagement-app, så alle adressedata oprettes baseret på både programmet til finans og drift og kundeengagement-appen.
6. Trin 5-2 konverterer .csv-filerne til finans og drift-importformat til manuel import.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. Trin 6 importerer data fra postadressesamlingen til kundeengagement-app.
8. Trin 7 importerer data fra postadressesamlingen fra kundeengagement-app.
9. Trin 8 opretter kundeadressedata og tilknytter en postadressesamlings-id.
10. Trin 9-1 til og med 9-2 tilknytter part- og postadressesamling-id med postadresser og partpostadresser.
11. Trin 10-1 til og med 10-3 importerer debitoradresser, postadresser og partpostadresser til kundeengagement-app.

### <a name="steps-in-the-party-electronic-address-template"></a>Trin i skabelonen til partelektronikadresse

1. Trin 1-1 til og med 1-5 henter data fra både programmet til finans og drift og kundeengagement-app og trindata til opgradering.
2. Trin 2 konsoliderer elektroniske adresser i kundeengagement-appen fra konto-, kontaktperson- og leverandørenheder.
3. Trin 3 fletter primære elektroniske adressedata fra kundeengagement-app og program til finans og drift.
4. Trin 4 opretter .csv-filer.

    - Opret nye elektroniske adressedata for programmet til finans og drift på baggrund af konto-, kontakt- og leverandøradresser.
    - Opret nye elektroniske adressedata til kundens aftale-app på baggrund af elektroniske adresse-, konto-, kontakt- og leverandøradresser i programmet til finans og drift.

5. Trin 5-1 importerer elektroniske adresser til kundeengagement-app.
6. Trin 5-2 opretter .csv-filer for at opdatere primære adresser til konti og kontaktpersoner i kundeengagement-appen.
7. Trin 6-1 til og med 6-2-importkonti, og kontakt primære adresser til kundeengagement-appen.

## <a name="troubleshooting"></a>Fejlfinding

1. Hvis processen mislykkes, skal du køre data factory igen. Start fra den mislykkede aktivitet.
2. Nogle filer, der genereres af data factory, som du kan bruge til datavalidering.
3. Datafabrikken kører på basis af .csv-filer. Hvis der derfor er en feltværdi med komma, kan den forstyrre resultaterne. Du skal fjerne alle kommaer fra feltværdier.
4. Fanen **Overvågning** indeholder oplysninger om alle trin og data, der er blevet behandlet. Vælg et bestemt trin for at fejlfinde det.

    ![Fanen Overvågning.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Få mere at vide om skabelonen

Du kan finde flere oplysninger om skabelonen i [Kommentarer til filen vigtige oplysninger til Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).

