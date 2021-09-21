---
title: Komponenter til elektronisk fakturering i administration
description: Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af Elektronisk fakturering.
author: gionoder
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d187e8a03552258099d7021ff056d0726ea60ca1
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463875"
---
# <a name="electronic-invoicing-administration-components"></a>Komponenter til elektronisk fakturering i administration

[!include [banner](../includes/banner.md)]


Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af Elektronisk fakturering. Det indeholder også oplysninger om, hvordan du konfigurerer Elektronisk fakturering.

## <a name="azure"></a>Azure

Brug Microsoft Azure til at oprette hemmeligheder for Key Vault og konfigurere lagerkontoen. Brug derefter nøgleboksene og lagringskontoen SAS-token i konfigurationen af elektronisk fakturering.

## <a name="lifecycle-services"></a>Lifecycle Services

Brug Microsoft Dynamics Lifecycle Services (LCS) for at aktivere tilføjelsesprogrammet til elektronisk fakturering til dit LCS-implementeringsprojekt.

> [!NOTE]
> Installationen af tilføjelsesprogram i LCS kræver mindst **Miljø på niveau 2**. Du kan finde flere oplysninger om miljøplanlægning under [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) er den grænseflade, der anvendes til konfigurering af Elektronisk fakturering. Ressourcer som f.eks. miljøer og funktioner til elektronisk fakturering oprettes, vedligeholdes og er hostet i RCS. Når ressourcerne er klar, publiceres de til Elektronisk faktureringstjeneste.

Vedrørende RCS-tilmelding se [Regulatory services](https://marketing.configure.global.dynamics.com/).

Du kan finde flere oplysninger om RCS i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Integration med elektronisk fakturering 

Før du kan bruge RCS til at konfigurere elektroniske fakturaer, skal du konfigurere RCS til at tillade kommunikation med Elektronisk fakturering. Du fuldfører denne konfiguration under fanen **Elektronisk fakturering** på siden **Elektroniske rapporteringsparametre**.

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>Tjenesteslutpunkt

Elektronisk fakturering er tilgængelig i flere geografiske Azure-datacentre. Følgende tabel viser tilgængeligheden pr. region.


| Datacenter Azure-geografisk område | URI for tjenesteslutpunkt                                                       |
|----------------------------|----------------------------------------------------------------------------|
| United States              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| Europa                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Storbritannien             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Asien                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>Tjenestemiljøer

Tjenestemiljøer er logiske partitioner, der er oprettet for at understøtte udførelsen af funktionerne for global fakturering i Elektronisk fakturering. Sikkerhedsfunktionerne og de digitale certifikater, og de nye styreformer (dvs. adgangsrettigheder), skal konfigureres på tjenestemiljøniveau.

Kunder kan oprette lige så mange tjenestemiljøer, de ønsker. Alle de tjenestemiljøer, som en kunde opretter, er uafhængige af hinanden.

Tjenestemiljøer skal oprettes og vedligeholdes i RCS. Når tjenestemiljøerne er klar, skal de publiceres til Elektronisk fakturering.

#### <a name="service-environment-status"></a>Status for tjenestemiljø

Tjenestemiljøer kan administreres via status. De mulige indstillinger er:

- **Ikke udgivet** – Miljøet er oprettet, men det er endnu ikke udgivet.
- **Publiceret** – Miljøet er udgivet til Elektronisk fakturering.
- **Ændret** – Attributterne i et udgivet miljø er ændret, men ændringerne er endnu ikke publiceret.

#### <a name="customer-secrets"></a>Kundehemmeligheder

Tjenesten til elektronisk fakturering er ansvarlig for at opbevare af alle dine virksomhedsdata i de Azure-ressourcer, der ejes af din virksomhed. Hvis du vil sikre dig, at tjenesten fungerer korrekt, og at alle de virksomhedsdata, der kræves til og oprettes af Elektronisk fakturering, tilgås korrekt, skal du oprette to hovedressourcer i Azure:

- En Azure-lagerkonto (Blob-lager), der lagrer elektroniske dokumenter, herunder elektroniske fakturaer, resultater af dokumenttransformationer og svar fra eksterne webtjenester.
- En Azure Key Vault, der opbevarer certifikater og URI'en (Uniform Resource Identifier) for lagerkontoen (SAS-token).


En dedikeret Key Vault og kundelagerkonto skal tildeles specifikt til brug sammen med Elektronisk fakturering. Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og en Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

Hvis du vil overvåge sundheden af Key Vault og modtage advarsler, skal du konfigurere Azure Monitor til Key Vault. Ved at aktivere logføring af Key Vault kan du overvåge, hvordan, hvornår og hvem der tilgår Key Vaults. Du kan finde flere oplysninger i [Overvågning og advarsler for Azure Key Vault](/azure/key-vault/general/alert), og [Hvordan du aktiverer logning af Key Vault](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Som bedste praksis skal hemmeligheder jævnligt ombyttes. Yderligere oplysninger finder du i [Dokumentation af hemmeligheder](/azure/key-vault/secrets/).

#### <a name="users"></a>Brugere

De enkelte tjenestemiljøer skal indeholde en oversigt over de brugere, der kan oprette forbindelse fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i Elektronisk fakturering.

#### <a name="publication"></a>Publikation

Når tjenestemiljøerne er klar, skal de publiceres til Elektronisk fakturering, før de kan bruges. Der er kun publicerede miljøer tilgængelige i Finans og Supply Chain Management. Desuden skal et servicemiljø publiceres, før eventuelle opdateringer af attributterne i programmet træder i kraft for den elektroniske faktureringstjeneste.

### <a name="connected-applications"></a>Tilsluttede ansøgninger

Tilknyttede applikationer er de forekomster af Finans og Supply Chain Management, som du muligvis vil have kontakt til via RCS. Udover applikationens URL-adresse og dens lejer indeholder en tilknyttet applikation de legitimationsoplysninger, der gør det muligt for RCS at oprette forbindelse til miljøet.

Via de tilknyttede applikationer kan du konfigurere en del af funktionen til elektronisk fakturering i Finans og Supply Chain Management, så hele funktionen til elektronisk fakturering fungerer.

## <a name="finance-and-supply-chain-management"></a>Finance og Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Integration med elektronisk fakturering

Før du kan bruge Finans og Supply Chain Management til at udstede elektroniske fakturaer via Elektronisk fakturering, skal det være konfigureret, så der kan kommunikeres med tjenesten.

#### <a name="electronic-invoicing-integration-feature"></a>Funktion til integration af elektronisk fakturering

Hvis du vil aktivere kommunikation mellem Finance og Supply Chain Management og Elektronisk fakturering, skal du aktivere funktionen **Integration af Elektronisk fakturering** i arbejdsområdet **Funktionsstyring**.

#### <a name="service-endpoint"></a>Tjenesteslutpunkt

Tjenesteslutpunktet er den URL-adresse, hvor Elektronisk fakturering er placeret. Før du kan udstede elektroniske fakturaer, skal tjenesteslutpunktet konfigureres i Finans og Supply Chain Management for at tillade kommunikation med tjenesten.

Hvis du vil konfigurere tjenesteslutpunktet, skal du gå til **Organisationsadministration \> Opsætning \> Elektronisk dokumentparametre** og derefter på fanen **Overførelsestjenester** i feltet **URL-adressen til tilføjelsesprogrammet til elektronisk fakturering** angive URL-adressen i tabellen, som beskrevet tidligere i afsnittet [Serviceslutpunkt](#svc-endpoint-uris).

#### <a name="environments"></a>Miljøer

Det miljønavn, der angives i Finance og Supply Chain Management, henviser til navnet på det miljø, der oprettes i RCS og udgives i Elektronisk fakturering.

Miljøet skal være konfigureret under fanen **Elektronisk fakturering** på siden **Parametre for elektronisk dokument**. På den måde indeholder alle anmodninger om udstedelse af elektroniske fakturaer det miljø, hvor elektronisk fakturering kan bestemme, hvilken funktion til elektronisk fakturering der skal behandle anmodningen.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfiguration af elektroniske fakturaer i RCS](e-invoicing-configuration-rcs.md)
- [Udsted elektroniske fakturaer i Finance og Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
