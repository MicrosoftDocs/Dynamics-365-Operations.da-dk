---
title: Introduktion til tilføjelsesprogrammet til elektronisk fakturering serviceadministration
description: Dette emne beskriver, hvordan du kommer i gang med tilføjelsesprogrammet til elektronisk fakturering.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104358"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Introduktion til tilføjelsesprogrammet til elektronisk fakturering serviceadministration

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Forudsætninger

Før du kan fuldføre trinene i dette emne, skal du kontrollere, at følgende forudsætninger er opfyldt:

- Du skal have adgang til din Microsoft Dynamics Lifecycle Services-konto (LCS).
- Du skal have et LCS-projekt, der omfatter version 10.0.13 eller en senere version af Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Derudover skal disse apps implementeres i en af følgende Azure-geografisk områder:

    - Det østlige USA
    - Det vestlige USA
    - Det nordlige Europa
    - Det vestlige Europa

- Du skal have adgang til din Dynamics 365 Regulatory Configuration Services (RCS-konto).
- Du skal aktivere globaliseringsfunktionen for din RCS-konto i modulet Funktionsstyring. Du kan finde flere oplysninger i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md).
- Du skal oprette en Key Vault og en lagerkonto i Azure. Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Installere tilføjelsesprogrammet til mikroservices i Lifecycle Services

1. Log på din LCS-konto.
2. Vælg feltet **Prøveversion af funktionsstyring**.
3. I afsnittet **Funktioner til offentlig visning** skal du vælge en **e-faktureringstjeneste**.
4. Kontroller, at indstillingen **Prøveversion af funktion aktiveret** er indstillet til **Ja**.

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>Konfigurer parametre for RCS-integration med tilføjelsesprogrammet til elektronisk fakturering.

1. Log på din RCS-konto.
2. Gå til arbejdsområdet **Elektronisk rapportering**, og vælg **Parametre til elektronisk rapportering** i sektionen **Relaterede links**.
3. Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel i feltet URI i feltet **Serviceslutpunkt URI** under fanen **e-faktureringsservice**.

    | Datacenter Azure-geografisk område | URI for tjenesteslutpunkt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Det østlige USA                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Det vestlige USA                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Det nordlige Europa                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Det vestlige Europa                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Kontrollér, at **Applikations-id** er angivet til **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Denne værdi er en fast værdi.
5. Angiv id'et for din LCS-abonnementskonto i feltet **LCS-miljø-id**.
6. Vælg **Gem**, og luk derefter siden.

## <a name="create-key-vault-secret"></a>Oprette Key Vault-hemmelighed

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Miljøer** skal du vælge feltet **e-fakturering**.
3. På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden og derefter vælge **Key Vault-parametre**.
4. Vælg **Ny** for at oprette en key vault-hemmelighed.
5. Angiv navnet på key vault-hemmeligheden i feltet **Navn**. Indtast en beskrivelse i feltet **Beskrivelse**.
6. Indsæt hemmeligheden fra Azure Key Vault i feltet **Key Vault URI**.
7. Vælg **Gem**.

## <a name="create-storage-account-secret"></a>Oprette hemmelig lagerkonto

1. Vælg **Tilføj** i afsnittet **Certifikater** på siden **Nøgleparametre**.
2. Angiv det samme for lagerkontohemmeligheden i feltet **Navn**. Indtast en beskrivelse i feltet **Beskrivelse**.
3. I **Type**-feltet skal du vælge **Certifikat**.
4. Vælg **Gem**, og luk derefter siden.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Opret et miljø for tilføjelsesprogrammet til elektronisk fakturering

1. Log på din RCS-konto.
2. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Miljøer** skal du vælge feltet **e-fakturering**.

## <a name="create-a-service-environment"></a>Opret et servicemiljø

1. På siden **Miljøopsætninger** skal du vælge **Servicemiljø** i handlingsruden.
2. Vælg **Ny** for at oprette et nyt servicemiljø.
3. Angiv navnet på e-faktureringsmiljøet i feltet **Navn**. Indtast en beskrivelse i feltet **Beskrivelse**.
4. Vælg navnet på det certifikat, der skal bruges til godkendelse af adgang til lagringskontoen, i feltet **Opbevaring af SAS-token**.
5. I afsnittet **Brugere** skal du vælge **Tilføj** for at tilføje en bruger, som har tilladelse til at sende elektroniske fakturaer gennem miljøet, og også oprette forbindelse til lagerkontoen.
6. Angiv **Bruger-id** i feltet for brugerens alias. I feltet **E-mail** skal du angive brugerens e-mailadresse.
7. Vælg **Gem**.
8. Hvis dine lande-/områdespecifikke fakturaer kræver en kæde af certifikater for at anvende en digital signaturer, skal du vælge **Key Vault-parametre** i handlingsruden og derefter vælge **Kæde af certifikater** og følge disse trin.

    1. Vælg **Ny** for at oprette en kæde af certifikater.
    2. Angiv navnet på kæden af certifikater i feltet **Navn**. Indtast en beskrivelse i feltet **Beskrivelse**.
    3. I afsnittet **Certifikater** skal du vælge **Tilføj** for at føje et certifikat til kæden.
    4. Brug knappen **Op** eller **Ned** til at ændre certifikatets placering i kæden.
    5. Vælg **Gem**, og luk derefter siden.
    6. Luk siden.
9. Vælg **Udgiv** i handlingsruden for at publicere miljøet til skyen på siden **Servicemiljø**. Værdien i feltet **Status** ændres til **Publiceret**.

## <a name="create-a-connected-application"></a>Opret en tilsluttet applikation.

1. På siden **Miljøopsætninger** skal du vælge **Tilsluttede applikationer** i handlingsruden.
2. Vælg **Ny** for at oprette en tilsluttet applikation.
3. Angiv navnet på den applikation, der skal tilsluttes i feltet **Navn**.
4. I feltet **Applikation** skal du angive URL-adressen til det finans- og Supply Chain Management-miljø, der skal oprettes forbindelse til.
4. I feltet **Lejer** skal du angive den lejer til finans- og Supply Chain Management-miljøet.
5. Vælg **Gem**.
6. Vælg **Check-forbindelse** i handlingsruden for at teste forbindelsen til miljøet. Luk derefter siden.

## <a name="link-connected-applications-to-environments"></a>Sammenkæd tilknyttede applikationer med miljøer

1. På siden **Miljøopsætninger** skal du vælge **Ny** for at tildele en tilknyttet applikation til et miljø.
2. Vælg en tilsluttet applikation i feltet **Tilsluttet applikation**.
3. Vælg et servicemiljø i feltet **Servicemiljø**.
4. Vælg **Gem**, og luk derefter siden.

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Konfigurer integrationen af tilføjelsesprogrammet til elektronisk fakturering i Finance og Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Aktivere funktionen til integration af tilføjelsesprogrammet til elektronisk fakturering

1. Log på din Finance eller Supply Chain Management-forekomst.
2. Gå til arbejdsområdet **Funktionsstyring**, og søg efter funktionen **Integration af tilføjelsesprogrammet til elektronisk fakturering**. Hvis denne funktion ikke vises på siden, skal du vælge **Kontroller, om der er opdateringer**.
3. Vælg funktionen, og vælg derefter **Aktivér nu**.

### <a name="set-up-the-service-endpoint-url"></a>Konfigurere URL-adressen til tjenesteslutpunkt

1. Gå til **Organisationsadministration \> Konfiguration \> Parametre for elektroniske dokumenter**.
2. Angiv det relevante serviceslutpunkt for din Azure-geografi som vist i følgende tabel, i feltet URL i feltet **Serviceslutpunkt URL** under fanen **Indsendelsestjeneste**.

    | Datacenter Azure-geografisk område | URL for tjenesteslutpunkt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Det østlige USA                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Det vestlige USA                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Det nordlige Europa                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Det vestlige Europa                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. Angiv navnet på tilføjelsesprogrammet elektronisk faktureringsmiljøet i feltet **Miljø**.
4. Vælg **Gem**, og luk derefter siden.
