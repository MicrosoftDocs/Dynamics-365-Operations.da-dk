---
title: Start her med serviceadministration i elektronisk fakturering
description: Dette emne beskriver, hvordan du kommer i gang med elektronisk fakturering.
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f77c8fd1696b74f852d04cc0a696d4816ef9af1f
ms.sourcegitcommit: 5033d42a2aac852916d726e40bd98a164d1a837d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/23/2022
ms.locfileid: "7984822"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Start her med serviceadministration i elektronisk fakturering

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre trinene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:

- Du skal have adgang til din Microsoft Dynamics Lifecycle Services-konto (LCS).
- Du skal have et LCS-projekt, der omfatter version 10.0.17 eller en senere version af Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management. Derudover skal disse apps implementeres i en af følgende Azure-geografisk områder:

    - United States
    - Europa
    - Storbritannien
    - Asien

- Du skal have adgang til din Dynamics 365 Regulatory Configuration Services (RCS-konto).
- Du skal aktivere globaliseringsfunktionen for din RCS-konto i modulet Funktionsstyring. Du kan finde flere oplysninger i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md).
- Du skal oprette en Key Vault og en lagerkonto i Azure. Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Installere tilføjelsesprogrammet til mikroservices i Lifecycle Services

1. Log på din LCS-konto, og vælg et LCS-projekt på dashboardet for LCS-projekter.
2. I projektet skal du vælge dit implementeringsmiljø på **Miljøer**-dashboardet. Det miljø, du vælger, skal køre.
3. Under fanen **Power Platform Integration** i feltgruppen **Tilføjelsesprogrammer for miljø** skal du vælge **Installer et nyt tilføjelsesprogram**.
4. Vælg **Elektronisk fakturering**.
5. Angiv i feltet **AAD-program-id** **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Denne værdi er en fast værdi.
6. Angiv lejer-id for din Azure-abonnementskonto i feltet **AAD-lejer-id**. Den Azure Active Directory (Azure AD) lejer, du angiver, skal være den samme lejer, som bruges til RCS.
7. Gennemse vilkår og betingelser, og marker afkrydsningsfeltet.
8. Vælg **Installer**. Installationen kan tage op til flere minutter.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Konfigurere parametre for RCS-integration med elektronisk fakturering

1. Log på din RCS-konto.
2. Gå til arbejdsområdet **Globaliseringsfunktioner**, og vælg **Parametre til elektronisk rapportering** i sektionen **Relaterede indstillinger**.
3. Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel i feltet URI i feltet **Serviceslutpunkt URI** under fanen **elektronisk fakturering**.

    | Datacenter Azure-geografisk område | URI for tjenesteslutpunkt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | United States              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Storbritannien             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asien                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. Kontrollér, at **Applikations-id** er angivet til **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Denne værdi er en fast værdi.
5. Angiv id'et for dit LCS-abonnementsmiljø i feltet **LCS-miljø-id**.
6. Vælg **Gem**, og luk derefter siden.

## <a name="create-key-vault-references"></a>Oprette Key Vault-referencer

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Miljø** skal du vælge feltet **Elektronisk fakturering**.
3. På siden **Miljøopsætninger** skal du vælge **Servicemiljøer** i handlingsruden og derefter vælge **Key Vault-parametre**.
4. Vælg **Ny** for at oprette en Key Vault-reference.
5. Angiv navnet på key vault-referencen i feltet **Navn**. Indtast en beskrivelse i feltet **Beskrivelse**.
6. Indsæt Key Vault-hemmeligheden fra Azure Key Vault i feltet **Key Vault URI**. Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).
7. Vælg **Gem**.

## <a name="create-storage-account-secret"></a>Oprette hemmelig lagerkonto

1. På siden **Miljøopsætninger** skal du vælge **Servicemiljø** > **Key Vault-parametre** i handlingsruden.
2. Vælg en **Key Vault-reference**, og vælg **Tilføj** i sektionen **Certifikater**.
3. Angiv navnet på lagerkontohemmeligheden i feltet **Navn**. Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. I feltet **Type** skal du vælge **Hemmelighed**.
6. Vælg **Gem**, og luk derefter siden.

## <a name="create-a-digital-certificate-secret"></a>Oprette en digital certifikathemmelighed

1. På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden og derefter vælge **Key Vault-parametre**.
2. Vælg en **Key Vault-reference**, og vælg derefter **Tilføj** i sektionen **Certifikater**.
3. Angiv navnet på den digitale certifikathemmelighed i feltet **Navn**. Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).
4. Indtast en beskrivelse i feltet **Beskrivelse**.
5. I **Type**-feltet skal du vælge **Certifikat**.
6. Vælg **Gem**, og luk derefter siden.

## <a name="create-a-service-environment"></a>Opret et servicemiljø

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktionen** i sektionen **Miljø** skal du vælge feltet **Elektronisk fakturering**.
3. På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden.
4. Vælg **Ny** for at oprette et nyt servicemiljø.
5. Angiv navnet på e-faktureringsmiljøet i feltet **Navn**. Indtast en beskrivelse i feltet **Beskrivelse**.
6. Vælg navnet på den hemmelige lagerkonto, der skal bruges til godkendelse af adgang til lagringskontoen, i feltet **Opbevaring af SAS-token**.
7. I afsnittet **Brugere** skal du vælge **Tilføj** for at tilføje en bruger, som har tilladelse til at sende elektroniske fakturaer gennem miljøet, og også oprette forbindelse til lagerkontoen.
8. Angiv **Bruger-id** i feltet for brugerens alias. I feltet **E-mail** skal du angive brugerens e-mailadresse.
9. Vælg **Gem**.
10. Hvis dine lande-/områdespecifikke fakturaer kræver en kæde af certifikater for at anvende en digital signaturer, skal du vælge **Key Vault-parametre** i handlingsruden og derefter vælge **Kæde af certifikater** og følge disse trin.

    1. Vælg **Ny** for at oprette en kæde af certifikater.
    2. Angiv navnet på kæden af certifikater i feltet **Navn**. Indtast en beskrivelse i feltet **Beskrivelse**.
    3. I afsnittet **Certifikater** skal du vælge **Tilføj** for at føje et certifikat til kæden.
    4. Brug knappen **Op** eller **Ned** til at ændre certifikatets placering i kæden.
    5. Vælg **Gem**, og luk derefter siden.
    6. Luk siden.

11. Vælg **Udgiv** i handlingsruden for at publicere miljøet til skyen på siden **Servicemiljø**. Værdien i feltet **Status** ændres til **Publiceret**.

## <a name="create-a-connected-application"></a>Opret en tilsluttet applikation.

1. På siden **Miljøopsætning** skal du vælge **Tilsluttede applikationer** i handlingsruden.
2. Vælg **Ny** for at oprette en tilsluttet applikation.
3. Angiv navnet på den applikation, der skal tilsluttes i feltet **Navn**.
4. I feltet **Applikation** skal du angive URL-adressen til det finans- og Supply Chain Management-miljø, der skal oprettes forbindelse til.
4. I feltet **Lejer** skal du angive den lejer til finans- og Supply Chain Management-miljøet.
5. Vælg **Gem**.
6. Vælg **Check-forbindelse** i handlingsruden for at teste forbindelsen til miljøet. Luk derefter siden.

## <a name="link-connected-applications-to-environments"></a>Sammenkæd tilknyttede applikationer med miljøer

1. På siden **Miljøopsætning** skal du vælge **Ny** for at tildele en tilknyttet applikation til et miljø.
2. Vælg en tilsluttet applikation i feltet **Tilsluttet applikation**.
3. Vælg et servicemiljø i feltet **Servicemiljø**.
4. Vælg **Gem**, og luk derefter siden.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Konfigurere integrationen af elektronisk fakturering i Finance eller Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Aktivere funktionen til integration af elektronisk fakturering

1. Log på din Finance eller Supply Chain Management-forekomst.
2. Gå til arbejdsområdet **Funktionsstyring**, og søg efter funktionen **Integration af elektronisk fakturering**. Hvis denne funktion ikke vises på siden, skal du vælge **Kontroller, om der er opdateringer**.
3. Vælg funktionen, og vælg derefter **Aktivér nu**.

### <a name="set-up-the-service-endpoint-url"></a>Konfigurere URL-adressen til tjenesteslutpunkt

1. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
2. Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel i feltet URL i feltet **Slutpunkt URL** under fanen **elektronisk fakturering**.

    | Datacenter Azure-geografisk område | URI for tjenesteslutpunkt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | United States              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Storbritannien             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asien                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Angiv navnet på det servicemiljø, der er publiceret i elektronisk fakturering, i feltet **Miljø**.
4. Vælg **Gem**, og luk derefter siden.

### <a name="enable-flighting-keys-for-finance-or-supply-chain-management-version-10017"></a>Aktiver Flighting-nøgler til Finans eller Supply Chain Management version 10.0.17

1. Kør følgende SQL-kommando:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Udfør en IISreset-kommando for alle AOS'er.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
