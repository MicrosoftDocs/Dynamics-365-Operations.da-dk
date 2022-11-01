---
title: Konfigurere Regulatory Configuration Service (RCS)
description: Denne artikel beskriver, hvordan du konfigurerer Regulatory Configuration Service (RCS).
author: gionoder
ms.date: 10/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 32ced98925ee66e02f0b073b4acbd586666ac20c
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710775"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Konfigurere Regulatory Configuration Service (RCS)

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du konfigurerer Regulatory Configuration Service (RCS).

## <a name="turn-on-globalization-features"></a>Slå globaliseringsfunktionerne til

1. Log på din RCS-konto.
2. Vælg felter **Funktionsstyring**.
3. I området **Funktionsstyring** skal du vælge **Globaliseringsfunktioner** på listen og derefter **Aktivér nu**.

Der skal nu vises et felt for arbejdsområdet **Globaliseringsfunktioner** på hoveddashboardet i RCS.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Konfigurere parametre for RCS-integration med elektronisk fakturering

1. Gå til arbejdsområdet **Globaliseringsfunktioner**, og vælg **Parametre til elektronisk rapportering** i sektionen **Relaterede indstillinger**.
2. Første gang du konfigurerer parametrene, vil du blive bedt om at oprette forbindelse til Lifecycle Services (LCS). Vælg **Klik her for at oprette forbindelse til Lifecycle Services**, og når forbindelsen er oprettet, skal du vælge **OK**.

    > [!IMPORTANT]
    > I lande eller områder, hvor dataopbevaring er tvungen, og hvis dit RCS er klargjort i et andet område, hvor LCS er klargjort, kan du modtage følgende forbindelsesfejlmeddelelse i RCS: "Der blev ikke fundet nogen HTTP-ressource, der svarer til URI'en for anmodningen". Vælg **OK**. Du kan modtage en anden fejlmeddelelse i RCS: "Brugertokenet for Dynamics Lifecycle Services kunne ikke genereres for brugeren (). Kontakt din systemadministrator."
    >  
    > Det sker, fordi LCS er en global tjeneste og er klargjort i et område i USA. På grund af dataopbevaringspolitikken kan RCS fra dit aktuelle område ikke oprette forbindelse til LCS. Under disse omstændigheder er der to mulige løsninger:
    > - Slet RCS fra dit aktuelle område, og genopret det i USA-området.
    > - Ignorer fejlene, og fortsæt med opsætningen af elektronisk fakturering. Disse fejl har ingen indflydelse på funktionen Elektronisk fakturering.

3. Angiv det relevante serviceslutpunkt for din Microsoft Azure-geografi som vist i følgende tabel, i feltet **Serviceslutpunkt-URI** under fanen **Elektronisk fakturering**.

    | Datacenter Azure-geografisk område | URI for tjenesteslutpunkt |
    |----------------------------|----------------------|
    | USA              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Storbritannien             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asien                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japan                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Schweiz                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brasilien                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Forenede Arabiske Emirater       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Australien                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Canada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Frankrig                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Indien                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Norge                     | <p>`https://gw.no-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Sydafrika               | <p>`https://gw.za-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Se og indtast i feltet **Program-id** den faste værdi **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Sørg for, at der kun er angivet et Globally Unique Identifier (GUID), og at værdien ikke indeholder andre symboler som f.eks. mellemrum, kommaer, punktummer eller anførselstegn.
4. Angiv id'et for dit Microsoft Dynamics Lifecycle Services-miljø i feltet **LCS-miljø-id**. Denne værdi er referencen til det Finansmiljø eller Supply Chain Management-miljø, du vil bruge sammen med den elektroniske faktureringsservice. Du kan hente dit id ved at logge på [LCS](https://lcs.dynamics.com/), åbne projektet og derefter se i feltet **Miljø-id** under fanen **Administrer miljø** i afsnittet **Miljødetaljer**.

    > [!IMPORTANT]
    > Hvis tilføjelsesprogrammet Elektronisk fakturering er installeret i flere Finansmiljøer eller Supply Chain Management-miljøer i LCS, skal du altid bruge miljø-id'et for det senest installerede miljø. Hvis du beslutter dig for at installere tilføjelsesprogrammet i et nyt miljø, når du har konfigureret og arbejdet med funktionen Elektronisk fakturering, skal du opdatere feltet **LCS-miljø-id** i RCS til den seneste værdi.

5. Vælg **Gem**, og luk derefter siden.

## <a name="configuration-providers"></a>Konfigurationsudbydere

Du kan bruge konfigurationsudbydere til at skelne mellem ejerne af ER-konfigurationer (elektronisk rapportering), der bruges til elektronisk fakturering og ejernes globaliseringsfunktioner. Til alle globaliseringsfunktioner, der leveres af Microsoft og udgives i det globale lager, er konfigurationsudbyderen angivet til **Microsoft** (`http://microsoft.com`).

Du kan kun justere ER-konfigurationer og globaliseringsfunktioner, der tilhører den aktive konfigurationsudbyder. Du kan bruge disse konfigurationer og funktioner som skabeloner til at oprette konfigurationer og funktioner, der tilhører den aktive konfigurationsudbyder, så du kan justere dem.

Opret først konfigurationsudbyderne. Angiv derefter en af dem som aktiv. Du kan ikke angive **Microsoft**-konfigurationsudbyderen som aktiv.

### <a name="create-a-configuration-provider"></a>Oprette en konfigurationsudbyder

1. Gå til arbejdsområdet **Elektronisk rapportering**, og vælg **Konfigurationsudbydere** i sektionen **Relaterede links**.
2. Vælg **Ny**.
3. Angiv et entydigt navn til konfigurationsudbyderen i feltet **Navn**.
4. Angiv konfigurationsudbyderenens URL-adresse i feltet **Internetadresse**.
5. Vælg **Gem**, og luk derefter siden.

### <a name="select-a-configuration-provider-as-active"></a>Vælg en konfigurationsudbyder som aktiv

1. Vælg den konfigurationsudbyder, du vil indstille som aktiv, på listen over konfigurationsudbydere.
2. Vælg **Angiv aktive**.

## <a name="import-er-configurations-from-the-global-repository"></a>Importere ER-konfigurationer fra det globale lager

1. Gå til arbejdsområdet **Elektronisk rapportering**, og vælg **Konfigurationsudbydere** i sektionen **Relaterede links**.
2. Vælg **Microsoft** på listen over konfigurationsudbydere, og vælg derefter **Lagre**.
3. Vælg **Global** og vælg **Åbn** i handlingsruden.
4. Importér følgende ER-modeller:

    - **Kontekstmodel for debitorfaktura**
    - **Fakturamodel**
    - **Regnskabsdokumenter** (om nødvendigt til brasilianske scenarier)
    - **Svarmeddelelsesmodel**

5. Hvis **Tilknytning af fakturamodel** ikke er importeret automatisk, kan du importere den.
6. Luk siden.
