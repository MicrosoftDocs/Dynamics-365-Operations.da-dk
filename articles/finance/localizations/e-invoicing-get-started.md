---
title: Kom i gang med tilføjelsesprogrammet til elektronisk fakturering
description: Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7b2a3aae43d42060c7fcd9e1ea3db814fc5d8f22
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039840"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Kom i gang med tilføjelsesprogrammet til elektronisk fakturering

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger, der hjælper dig med at komme i gang med tilføjelsesprogrammet til elektronisk fakturering. Det fører dig først gennem konfigurationstrinnene i Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) og Dynamics 365 Finance. Derefter beskrives processen til indsendelse af dokumenter via tjenesten ved hjælp af Dynamics 365 Finance eller Dynamics 365 Supply Chain Management. Du får også at vide, hvordan du fortolker indsendelsesloggene.

## <a name="availability"></a>Tilgængelighed

Tilføjelsesprogrammet til elektronisk fakturering er som udgangspunkt tilgængeligt for flere lande/områder. Tilføjelsesprogrammet understøtter oprettelse af elektroniske fakturaer og indsendelse af følgende forretningsdokumenter:

| Land/område  | Forretningsdokument                          |
|-----------------|--------------------------------------------|
| Østrig         | Salgs- og projektfakturaer                 |
| Belgien         | Salgs- og projektfakturaer                 |
| Brasilien          | Elektronisk regnskabsdokumentmodel 55 (NF-e) |
| Danmark         | Salgs- og projektfakturaer                 |
| Estland         | Salgs- og projektfakturaer                 |
| Finland         | Salgs- og projektfakturaer                 |
| Frankrig          | Salgs- og projektfakturaer                 |
| Tyskland         | Salgs- og projektfakturaer                 |
| Italien           | Salgs- og projektfakturaer                 |
| Mexico          | CFDI-faktura                               |
| Nederlandene     | Salgs- og projektfakturaer                 |
| Norge          | Salgs- og projektfakturaer                 |
| Spanien           | Salgs- og projektfakturaer                 |
| Europa          | PEPPOL Salgs- og projektfakturaer          |
    
## <a name="licensing"></a>Licensering

Du kan bruge tilføjelsesprogrammet til elektronisk fakturering sammen med din aktuelle licens. Der kræves ikke yderligere licenser for at bruge tjenesten.

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre trinene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:

- Adgang til din LCS-konto.
- Et LCS-implementeringsprojekt, der omfatter Finance eller Supply Chain Management version 10.0.13 eller nyere.
- Adgang til din RCS-konto.
- Slå globaliseringsfunktionen for din RCS-konto til via modulet **Funktionsstyring**. Du kan finde flere oplysninger i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md)
- Opret en Key Vault-ressource og en lagerkonto i Azure. Du kan finde flere oplysninger i [Oprette en Azure Storage-konto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Overblik

Følgende illustration viser de fem vigtigste trin, du skal fuldføre i dette emne.

![Oversigt over de fem trin i dette emne](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Konfiguration af Azure-ressourcer:** Konfigurer Azure Storage og overførslen af digitale certifikater i Azure Key Vault.
2. **LCS-konfiguration:** Installér tilføjelsesprogrammet til mikrotjenester.
3. **RCS-konfiguration:** Konfigurer miljøet, brugeradgangen og e-faktureringsfunktionerne.
4. **Klientkonfiguration:** Konfigurer forbindelsen mellem klienten og tilføjelsesprogrammet til elektronisk fakturering, og deaktiver de gamle funktioner til indsendelse og modtagelse af svar for elektroniske dokumenter.
5. **Send fakturaer:** Send elektroniske dokumenter ved hjælp af tilføjelsesprogrammet til elektronisk fakturering, og modtag svar.

> [!NOTE]
> Visse konfigurationstrin i dette emne er almindelige og lande-/områdeagnostiske. De trin og konfiguationsprocedurer, der er lande-/områdespecifikke, er beskrevet i lande-/områdespecifikke emner.

## <a name="lcs-setup"></a>LCS-opsætning

1. Log på din LCS-konto.
2. Vælg feltet **Styring af prøveversionsfunktion** , og i **Funktioner i offentlige prøveversioner** -feltgruppen skal du vælge **BusinessDocumentSubmission**.
3. Markér feltet **Prøveversionsfunktion aktiveret**.
4. Vælg LCS-implementeringsprojektet. Projektet skal køre, før du kan vælge det
5. Vælg **Installér et nyt tilføjelsesprogram** i oversigtspanelet **Tilføjelsesprogrammer for miljø**.
6. Vælg **Indsendelse af forretningsdokumenter**.
7. I dialogboksen **Konfigurer tilføjelsesprogram** skal du angive **091c98b0-a1c9-4b02-b62c-7753395ccabe** i feltet **AAD-program-id**. Denne værdi er en fast værdi.
8. Angiv id'et for din Azure-abonnementskonto i feltet **AAD-lejer-id**.

    ![Dialogboksen Konfigurer tilføjelsesprogram i LCS](media/e-invoicing-services-get-started-lcs-addin-setup.png)

9. Markér afkrydsningsfeltet for at acceptere vilkår og betingelser.
10. Vælg **Installer**.

## <a name="rcs-setup"></a>RCS-opsætning

Under RCS-opsætningen skal du udføre disse opgaver:

1. Konfigurer Key Vault i RCS.
2. Konfigurer RCS-integrationen med serveren for tilføjelsesprogrammet til elektronisk fakturering.
3. Opret et miljø for tilføjelsesprogrammet til elektronisk fakturering for din organisation.

### <a name="set-up-the-key-vault-in-rcs"></a>Konfigurere Key Vault i RCS

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Miljøer** skal du vælge feltet **e-fakturering**.
3. Vælg **Tjenestemiljøer**.

    ![Vælge Tjenestemiljøer](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> Indstillingen **Tilsluttede programmer** giver adgang til den automatiske konfiguration af tilføjelsesprogrammet til elektronisk fakturering i Finance eller Supply Management via RCS. I øjeblikket er denne funktion dog stadig under udvikling.

4. Gå til handlingsruden, og vælg **Parametre for Key Vault**.

    ![Vælge parameter for Key Vault](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. Vælg **Ny** i handlingsruden for at tilføje en Key Vault.
6. I feltet **URI for Key Vault** skal du angive attributværdien **DNS-navn** på den Key Vault-ressource, du har konfigureret i Azure. Du kan finde flere oplysninger om, hvor du kan finde værdien **DNS-navn** i [Oprette en Azure Storage-konto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

    ![Feltet URI for Key Vault](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. I oversigtspanelet **Certifikater** skal du vælge **Tilføj** for at angive alle de digitale certifikatnavne og Key Vault-hemmeligheder, der skal bruges til at oprette forbindelser, der er tillid til. I kolonnen **Type** kan du angive, om den er et certifikat eller en hemmelighed. Begge værdisæt er konfigureret på Key Vault-ressourcen i Azure.

    ![Tilføje certifikater](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Hvis din lande-/områdespecifikke faktura kræver en kæde af certifikater for at anvende en digital signatur, skal du vælge **Kæde af certifikater** i handlingsruden og derefter angive den rækkefølge af certifikater eller Key Vault-hemmeligheder, der udgør kæden.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>Konfigurere RCS-integrationen med serveren for tilføjelsesprogrammet til elektronisk fakturering

1. Gå til arbejdsområdet **Globaliseringsfunktioner** , og vælg **Parametre til elektronisk rapportering** i sektionen **Relaterede indstillinger**.
2. Vælg **Klik her for at oprette forbindelse til Lifecycle Services**. Hvis du ikke vil oprette forbindelse til LCS, skal du vælge **Annuller**.
3. Under fanen **e-faktureringstjenester** skal du angive værdien i overensstemmelse med de tilgængelige geografiske områder i feltet **Serviceslutpunkt-URI** : `https://businessdocumentsubmission.us.operations365.dynamics.com/` eller `https://businessdocumentsubmission.eu.operations365.dynamics.com/`.
4. Kontrollér, at feltet **Program-id** viser id'et **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Denne værdi er en fast værdi.
5. Angiv id'et for din LCS-abonnementskonto i feltet **LCS-miljø-id**.

![Angive parametre til tilføjelsesprogram til elektronisk fakturering](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Tilføje et miljø for tilføjelsesprogram til elektronisk fakturering

Du kan oprette forskellige miljøer for tilføjelsesprogrammet til elektronisk fakturering, f.eks. udvikler-, test- eller produktionsmiljøer.

1. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Miljøer** skal du vælge feltet **e-fakturering**.
2. Vælg **Ny** for at oprette et miljø.
3. I feltet **Lagerkonto for SAS-token** skal du angive navnet på den Key Vault-hemmelighed, du har konfigureret i Key Vault i RCS.

    ![Feltet Lagerkonto for SAS-token](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. Vælg **Ny** i oversigtspanelet **Brugere** for at tildele brugere adgang til dette miljø.

    ![Tilføje tjenestebrugere](media/e-invoicing-services-get-started-enter-service-users.png)

5. Vælg **Udgiv** i handlingsruden for at publicere miljøet til tilføjelsesprogrammet til elektronisk fakturering.

    ![Knappen Publicer](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>Konfiguration af e-faktureringsfunktion

"E-faktureringsfunktionen" er det generiske navn på den ressource, der er konfigureret og publiceret til at bruge serveren for tilføjelsesprogrammet til elektronisk fakturering. Konfigurationen af e-faktureringsfunktionen kombinerer bl.a. brugen af konfigurationsformater til elektronisk rapportering (ER) for til at oprette konfigurerbare eksport- og importfiler samt brugen af handlinger og handlingsflow for at muliggøre oprettelsen af regler til at sende anmodninger, importere svar og fortolke indholdet i svar.

På grund af variationer i fakturaformater og handlingsflow er funktionsopsætningen for e-fakturering lande-/områdeafhængig.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Konfigurere integrationen af tilføjelsesprogrammet til elektronisk fakturering i Finance eller Supply Chain Management 

Under denne konfiguration skal du fuldføre følgende opgaver:

1. Åbne funktionen flighted
2. Aktivér funktionen til integration af tilføjelsesprogrammet til elektronisk fakturering for at muliggøre integration med Finance.
3. Konfigurer URL-adressen til slutpunktet til tilføjelsesprogrammet til elektronisk fakturering.
4. Importér de ER-konfigurationer, der er relateret til den lande-/områdespecifikke e-faktureringsfunktion.
5. Aktivér den gældende lande-/regionsspecifikke e-faktureringsfunktion.
6. Importér ER-konfigurationerne, og konfigurer de svartyper, der kræves for at opdatere dit lande-/områdespecifikke fakturadokument som følge af indsendelsesprocessen.

### <a name="open-flighted-feature"></a>Åbne funktionen flighted
Funktionen til integration af elektroniske fakturaer er aktiveret via flighting. Flighting er et begreb, der gør det muligt have en funktion SLÅET TIL eller SLÅET FRA som standard. Følgende trin aktiverer en flight i et ikke-produktionsmiljø. 

1. Kør følgende SQL-kommando:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Når du har foretaget ovenstående ændring, skal du udføre en IISReset på alle AOS'er.

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Aktivere funktionen til integration af tilføjelsesprogrammet til elektronisk fakturering

1. Log på Finance eller Supply Chain Management.
2. Gå til arbejdsområdet **Funktionsstyring** , og søg efter den nye funktion **Konfigurerbar integration for tilføjelsesprogrammet til elektronisk fakturering**. Hvis funktionen stadig ikke vises på siden Funktionsstyring, skal du køre funktionen **Søg efter opdateringer**.
3. Vælg funktionen, og vælg derefter **Aktivér nu**.

### <a name="set-up-the-service-endpoint-url"></a>Konfigurere URL-adressen til tjenesteslutpunkt

1. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
2. På fanen **Indsendelsestjeneste** skal du angive `https://businessdocumentsubmission.us.operations365.dynamics.com/` i feltet **URL-adresse til tjenesteslutpunkt**.
3. I feltet **Miljø** skal du angive navnet på det miljø for tilføjelsesprogrammet til elektronisk fakturering, som du oprettede under RCS-konfigurationen.

![Angive tjenesteparametre](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>Importere ER-konfigurationerne

Hvis forretningsdata skal indsamles og sendes til tilføjelsesprogrammet til elektronisk fakturering, skal du importere ER-datamodellen og konfigurationen af ER-datamodellen, der er relateret til den lande-/områdespecifikke e-faktureringsfunktion, du vil bruge.

1. Gå til arbejdsområdet **Elektronisk rapportering** , og vælg feltet **Microsoft** i sektionen **Konfigurationsudbydere**. Kontrollér, at denne konfigurationsudbyder er angivet til **Aktiv**. Du kan finde flere oplysninger om, hvordan du angiver en udbyder til **Aktiv** , i [Oprette konfigurationsudbydere og markere dem som aktive](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Vælg **Lagre**.
4. Vælg **Global ressource** , og vælg derefter **Åben**.
5. Vælg **Klik her for at oprette forbindelse til Lifecycle Services** i dialogboksen **Opret forbindelse til Lifecycle Services**.
6. Du skal importere den relevante datamodel, datamodeltilknytning og de relevante dataformater afhængigt af det land eller område, hvor du vil bruge e-faktureringsfunktionen. Du kan finde flere oplysninger om de ER-konfigurationer, du skal importere, i det lande-/områdespecifikke emne "Kom i gang med tilføjelsesprogrammet til elektronisk fakturering".
7. Importér **Debitorfakturakontekstmodel**. Denne model indeholder yderligere parametre, der bl.a. beskriver det miljø i Finance, der bruges til tilføjelsesprogrammet til elektronisk fakturering, når der sendes forretningsdata.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Aktivere lande-/områdespecifikke e-faktureringsfunktioner

Hvis du vil aktivere lande-/områdespecifikke e-faktureringsfunktioner, så de fungerer sammen med tilføjelsesprogrammet til elektronisk fakturering, skal du aktivere funktionen i hver juridiske enhed, hvor du vil bruge den. Derefter kan den gamle integration af elektronisk fakturering ikke længere bruges, og integrationen med det nye tilføjelsesprogram til elektronisk fakturering er aktiveret.

1. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
2. Markér afkrydsningsfeltet **Aktiveret** på fanen **Funktioner** i den række, der er relateret til din lande-/områdespecifikke e-faktureringsfunktion. Du kan finde flere oplysninger om, hvilken funktion du skal aktivere, i det lande-/områdespecifikke emne "Kom i gang med tilføjelsesprogrammet til elektronisk fakturering".

![Aktivere e-faktureringsfunktionen](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Hvis du har flere juridiske enheder, der er konfigureret til forskellige lande eller områder, kan du aktivere den lande-/områdespecifikke e-faktureringsfunktion for hver juridiske enhed.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>Importere ER-konfigurationer og konfigurere svartyperne for at opdatere dit lande-/områdespecifikke fakturadokument

Hvis det indsendte fakturadokument kræver en opdatering efter svaret på indsendelsen til de offentlige autorisationstjenester, skal du importere en speciel ER-datamodel og konfigurationer for at aktivere statussen på det fakturadokument eller de andre felter, der skal opdateres.

1. Gå til arbejdsområdet **Elektronisk rapportering** , og vælg feltet **Microsoft** i sektionen **Konfigurationsudbydere**.
2. Vælg **Lagre**.
3. Vælg **Global ressource** , og vælg derefter **Åben**.
4. Importér **Svarmeddelelsesmodel** , **Format til import af svarmeddelelse** , **Tilknytning af svarmeddelelsesmodel til destination**  og **Format til import af filindhold**.
5. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
6. Vælg **Tilføj** på fanen **Elektronisk dokument** for at angive navnet på den tabel, der er relateret til det lande-/områdespecifikke fakturadokument. Du kan finde flere oplysninger om, hvilke tabelnavne du skal vælge, i det lande-/områdespecifikke emne "Kom i gang med tilføjelsesprogrammet til elektronisk fakturering".
7. Vælg **Svartyper** for at konfigurere svartyperne. Du kan finde flere oplysninger om, hvilke tabelnavne du skal vælge, i det lande-/områdespecifikke emne "Kom i gang med tilføjelsesprogrammet til elektronisk fakturering".

![Konfigurere svartyper](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>Navne på e-faktureringsfunktioner efter land/område 
I følgende tabel beskrives andre e-faktureringsfunktioner, der kan downloades fra det globale lager til elektronisk rapportering for at oprette elektroniske fakturaer.
I RCS kan du downloade de e-faktureringsfunktioner, der er angivet i denne tabel, ER-konfigurationerne og de tilgængelige konfigurationer for e-faktureringsfunktioner.
I Finance kan du aktivere de relaterede funktionsreferencer på siden **Parametre for elektroniske dokumenter** for at udstede elektroniske fakturaer for disse lande/områder. Du kan finde flere oplysninger i sektionen [Aktivere lande-/områdespecifikke e-faktureringsfunktioner](#region-specific) tidligere i dette emne.

| Funktionsnavn                      | Betegnelse                                 | ER-konfigurationer                                                                                                  | Konfigurationer                                                                                                                                                         | Land/område  | Funktionsreference      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Østrigske elektroniske fakturaer (AT) | Salgs- og projektfakturaer for Østrig      | - OIOUBL-salgsfaktura <br>- OIOUBL-projektfaktura <br>- OIOUBL-salgskreditnota <br>- OIOUBL-projektkreditnota | - Oprettelse af salgsfakturaer (AT) <br>- Oprettelse af projektfakturaer (AT) <br>- Oprettelse af salgskreditnota (AT) <br>- Oprettelse af projektkreditnota (AT)         | Østrig         | EUR-00023              |
| Belgisk elektronisk faktura (BE)   | Salgs- og projektfakturaer for Belgien      | - UBL-salgsfaktura (BE) <br>- UBL-projektfaktura (BE) <br>- UBL-projektkreditnota (BE) <br>- UBL-salgskreditnota (BE) | - Oprettelse af salgsfakturaer (BE)<br>- Oprettelse af projektfakturaer (BE) <br>- Oprettelse af salgskreditnota (BE) <br>- Oprettelse af projektkreditnota (BE)         | Belgien         | EUR-00023              |
| Dansk elektronisk faktura (DK)    | Salgs- og projektfakturaer for Danmark      | - OIOUBL-salgsfaktura <br>- OIOUBL-projektfaktura <br>- OIOUBL-salgskreditnota <br>- OIOUBL-projektkreditnota | - Oprettelse af salgsfakturaer (DK) <br>- Oprettelse af projektfakturaer (DK) <br>- Oprettelse af salgskreditnota (DK)<br>- Oprettelse af projektkreditnota (DK)         | Danmark         | EUR-00023<br> DK-00001 |
| Hollandsk elektronisk faktura (NL)     | Salgs- og projektfakturaer for Nederlandene  | - UBL-salgsfaktura (NL) <br>- UBL-projektfaktura (NL) <br>- UBL-salgskreditnota (NL) <br>- UBL-projektkreditnota (NL) | - Oprettelse af salgsfakturaer (NL) <br> - Oprettelse af projektfakturaer (NL) <br> - Oprettelse af salgskreditnota (NL) <br>- Oprettelse af projektkreditnota (NL)          | Nederlandene | EUR-00023              |
| Estisk elektronisk faktura (EE)  | Salgs- og projektfakturaer for Estland      | - Salgsfaktura (EE) <br> - Projektfaktura (EE)                                                                     | - Oprettelse af salgsfakturaer (EE) <br>- Oprettelse af projektfakturaer (EE)                                                                                           | Estland         | EUR-00023              |
| Finsk elektronisk faktura (FI)   | Salgs- og projektfakturaer for Finland      | - Salgsfaktura (FI) <br>- Oprettelse af projektfakturaer (FI)                                                          | - Oprettelse af salgsfakturaer (FI) <br>- Oprettelse af projektfakturaer (FI)                                                                                           | Finland         | EUR-00023              |
| Fransk elektronisk faktura (FR)    | Salgs- og projektfakturaer for Frankrig    | - UBL-salgsfaktura (FR) <br> - UBL-projektfaktura (FR) <br> - UBL-salgskreditnota (FR) <br>- UBL-projektkreditnota (FR) | - Oprettelse af salgsfakturaer (FR) <br> - Oprettelse af projektfakturaer (FR) <br>- Oprettelse af salgskreditnota (FR) <br>- Oprettelse af projektkreditnota (FR)         | Frankrig          | EUR-00023              |
| Tysk elektronisk faktura (DE)    | Salgs- og projektfakturaer for Tyskland      |- Salgsfaktura (DE) <br> - Projektfaktura (<DE>)                                                                     | - Oprettelse af salgsfakturaer (DE) <br>- Oprettelse af projektfakturaer (DE)                                                                                           | Tyskland         | EUR-00023              |
| Norsk elektronisk faktura (NO) | Salgs- og projektfakturaer for Norge       | - OIOUBL-salgsfaktura <br>- OIOUBL-projektfaktura <br>- OIOUBL-salgskreditnota <br>- OIOUBL-projektkreditnota | - Oprettelse af salgsfakturaer (NO) <br>- Oprettelse af projektfakturaer (NO) <br>- Oprettelse af salgskreditnota (NO) <br>- Oprettelse af projektkreditnota (NO)          | Norge          | EUR-00023<br> NO-00010 |
| Spansk elektronisk faktura (ES)   | Salgs- og projektfakturaer for Spanien        | - Salgsfaktura (ES) <br>- Projektfaktura (ES)                                                                     | - Oprettelse af salgsfakturaer (ES) <br>- Oprettelse af projektfakturaer (ES)                                                                                           | Spanien           | EUR-00023 <br>ES-00025 |
| Italiensk elektronisk faktura (IT)   | Salgs- og projektfakturaer for Italien        | - (Prøveversion) Salgs- og projektfaktura (IT) <br> - Projektfaktura (IT)                                                           | - Salgsfaktura <br> - Projektfaktura                                                                                                                           | Italien           | EUR-00023 <br>IT-00036 |
| PEPPOL Elektronisk faktura         | PEPPOL Oprettelse af salgs- og projektfakturaer | - PEPPOL Salgsfaktura <br>- PEPPOL Projektfaktura <br>- PEPPOL Salgskreditnota <br> - PEPPOL Projektkreditnota | - PEPPOL Oprettelse af salgsfakturaer <br>- PEPPOL Oprettelse af projektfakturaer <br>- PEPPOL Oprettelse af salgskreditnota <br>- PEPPOL Oprettelse af projektkreditnota |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Behandling af elektroniske fakturaer i Finance og Supply Chain Management

Under behandlingen skal du udføre disse opgaver:

1. Send et forretningsdokument (faktura) ved hjælp af tilføjelsesprogrammet til elektronisk fakturering.
2. Få vist loggene for udførelse af indsendelse.

### <a name="submit-business-documents"></a>Sende forretningsdokumenter

Under den almindelige indsendelsesproces er kommunikationen mellem klienten og tilføjelsesprogrammet til elektronisk fakturering tovejs. Målet er at udføre to hovedopgaver under indsendelse af elektroniske dokumenter:

1. Send alle elektroniske dokumenter, der afventer indsendelse fra Finance, og som har den korrekte status for indsendelse og opfylder udvælgelseskriterierne.
2. Importér det svar, som tilføjelsesprogrammet til elektronisk fakturering returnerer for tidligere sendte elektroniske dokumenter, i Finance. Efter importen fortolkes svarene, og statussen på forretningsdokumenterne opdateres i overensstemmelse hermed.

Du kan sende forretningsdokumenter enten manuelt eller baseret på kravene for din tidsplan.

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Send elektroniske dokumenter**.
2. Ved den første indsendelse af et dokument skal du altid angive indstillingen **Send dokumenter igen** til **Nej**. Hvis du skal sende et dokument igen via tjenesten, skal du angive denne indstilling til **Ja**.
3. I oversigtspanelet **Poster, der skal indgå** skal du vælge **Filter** for at åbne dialogboksen **Forespørgsel** , hvor du kan oprette en forespørgsel for at vælge de dokumenter, der skal sendes.

![Dialogboksen Send elektroniske dokumenter](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Filterforespørgsel

1. I dialogboksen **Forespørgsel** skal du på fanen **Område** angive filterkriterierne via felterne **Tabel** , **Afledt tabel** , **Felt** og **Kriterier**.
2. Vælg **Tilføj** for at tilføje så mange yderligere kriterier, du skal bruge for at vælge forretningsdokumenterne.

    ![Konfigurere filterkriterier for indsendelse](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Vælg **OK** for at lukke dialogboksen **Forespørgsel**.
4. Vælg **OK** for at sende de valgte forretningsdokumenter til tilføjelsesprogrammet til elektronisk fakturering.

    > [!NOTE]
    > I løbet af første forsøg på at sende et dokument via tjenesten bliver du bedt om at bekræfte forbindelsen med tilføjelsesprogrammet til elektronisk fakturering. Vælg **Klik her for at oprette forbindelse til tjenesten til indsendelse af elektroniske dokumenter**.
    >
    > ![Meddelelsesboks til at oprette forbindelse til indsendelse af elektroniske dokumenter](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Hvis forbindelsen er oprettet, modtager du en bekræftelsesmeddelelse.
    >
    > ![Bekræftelse af forbindelsen til tilføjelsesprogrammet til elektronisk fakturering](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Luk dialogboksen.

> [!NOTE]
> Efter hver indsendelse viser Handlingscenter antallet af sendte dokumenter.
>
> ![Handlingscentermeddelelser](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Indsendelse pr. batch

I stedet for at sende dokumenter manuelt kan du automatisere indsendelsesprocessen og køre den i baggrunden baseret på en konfigureret hyppighed af batchkørsel.

1. I dialogboksen **Send elektroniske dokumenter** skal du i oversigtspanelet **Kør i baggrunden** angive indstillingen **Batchbehandling** til **Ja**.
2. Konfigurer hyppigheden af batchkørsel på fanen **Gentagelse**.

![Konfigurere indsendelse pr. batch](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Få vist alle indsendelseslogge

1. Gå til **Organisationsadministration \> Periodisk \> Elektroniske dokumenter \> Indsendelseslog for elektroniske dokumenter**.
2. Vælg den dokumenttype, der skal filtreres efter, i feltet **Dokumenttype**.

    ![Vælge den dokumenttype, der skal vises indsendelseslogge for](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > Den værdi, der vises i kolonnen **Indsendelsesstatus** , repræsenterer den status, der er relateret til fuldførelsen af selve indsendelsesprocessen. Den angiver, om flowet for handlinger, der er konfigureret i RCS, blev kørt indtil afslutningen, uanset om det elektroniske dokument er godkendt eller afvist. Den værdi, der vises i kolonnen **Indsendelsesstatus** , repræsenterer ikke status for det sendte dokument. Du kan få vist statussen for det sendte dokument (dvs. om dokumentet blev godkendt eller afvist) i oversigtspanelet **Handlingslog for behandling** i oplysningerne om indsendelseslog, som beskrevet herefter.

3. Vælg **Forespørgsler \> Indsendelsesoplysninger** i handlingsruden.
4. Få vist logoplysningerne om indsendelse.

    ![Logoplysninger om indsendelse](media/e-invoicing-services-get-started-view-submission-log-form.png)

De resultater, der vises i indsendelsesloggen, afhænger af, hvordan e-faktureringsfunktionen er defineret i RCS. Uanset konfigurationen har indsendelsesloggen dog altid tre oversigtspaneler:

- **Behandling af handlinger** – I dette oversigtspanel vises udførelsesloggen for de handlinger, der er konfigureret i den funktionsversion, som blev konfigureret i RCS. Kolonnen **Status** viser, om handlingen blev kørt korrekt.
- **Handlingsfiler** – I dette oversigtspanel vises de midlertidige filer, der blev oprettet under udførelse af handlingerne. Du kan vælge **Vis** for at downloade filen og få vist indholdet.
- **Handlingslog for behandling** – I dette oversigtspanel vises resultaterne af kommunikationen mellem tilføjelsesprogrammet til elektronisk fakturering og destinationswebtjenesten. Den viser også, hvad der blev returneret af webtjenestebehandlingen.

## <a name="related-topics"></a>Relaterede emner

- [Oversigt over tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-service-overview.md)
- [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Brasilien](e-invoicing-bra-get-started.md)
- [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Mexico](e-invoicing-mex-get-started.md)
- [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering for Italien](e-invoicing-ita-get-started.md)
- [Konfigurere tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-setup.md)
