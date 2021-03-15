---
title: Administrationskomponenter til tilføjelsesprogrammet til elektronisk fakturering
description: Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af tilføjelsesprogrammet Elektronisk fakturering.
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104360"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Administrationskomponenter til tilføjelsesprogrammet til elektronisk fakturering

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af tilføjelsesprogrammet Elektronisk fakturering. Det indeholder også oplysninger om, hvordan du konfigurerer tilføjelsesprogrammet Elektronisk fakturering.

## <a name="azure"></a>Azure

Bruges Microsoft Azure til at oprette Key Vault og lagerkontoen. Brug derefter hemmeligheder i konfigurationen af tilføjelsesprogrammet Elektronisk fakturering.

## <a name="lifecycle-services"></a>Lifecycle Services

Brug Microsoft Dynamics Lifecycle Services (LCS) for at aktivere tilføjelsesprogrammet til mikroservices til dit LCS-implementeringsprojekt.

I LCS skal du vælge **Prøveversion af funktionsstyring** og derefter aktivere funktionen **e-faktureringstjeneste**.

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) er den grænseflade, der anvendes til konfigurering af tilføjelsesprogrammet Elektronisk fakturering. Ressourcer som f.eks. miljøer og funktioner til elektronisk fakturering oprettes, vedligeholdes og er hostet i RCS. Når ressourcerne er klar, publiceres de til tilføjelsesprogrammet Elektronisk faktureringstjeneste.

Du kan finde flere oplysninger om RCS i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md)

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Integration til tilføjelsesprogrammet til elektronisk fakturering

Før du kan bruge RCS til at konfigurere elektroniske fakturaer, skal du konfigurere RCS til at tillade kommunikation med tilføjelsesprogrammet Elektronisk fakturering. Du fuldfører denne konfiguration under fanen **Tilføjelsesprogram til Elektronisk fakturering** på siden **Elektroniske rapporteringsparametre**.

#### <a name="service-endpoint"></a>Tjenesteslutpunkt

URL-adressen for slutpunktet til tilføjelsesprogrammet Elektronisk fakturering kan variere alt efter Datacenter Azure-geografisk område. Følgende tabel viser tilgængeligheden pr. region:

| Datacenter Azure-geografisk område | URL for tjenesteslutpunkt                                                       |
|----------------------------|----------------------------------------------------------------------------|
| Det østlige USA                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| Det vestlige USA                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| Det nordlige Europa                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| Det vestlige Europa                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a>Program-id

Applikations-id er id for tilføjelsesprogrammet Elektronisk fakturering. Her er værdien fastsat: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

#### <a name="lcs-environment-id"></a>LCS miljø-id

LCS miljø-id er id for organisationens LCS-abonnement.

### <a name="service-environments"></a>Tjenestemiljøer

Tjenestemiljøer er logiske partitioner, der er oprettet for at understøtte udførelsen af funktionerne for elektronisk fakturering i tilføjelsesprogrammet Elektronisk fakturering. Sikkerhedsfunktionerne og de digitale certifikater, og de nye styreformer (dvs. adgangsrettigheder), skal konfigureres på tjenestemiljøniveau.

Kunder kan oprette lige så mange tjenestemiljøer, de ønsker. Alle de tjenestemiljøer, som en kunde opretter, er uafhængige af hinanden.

Tjenestemiljøer skal oprettes og vedligeholdes i RCS. Når tjenestemiljøerne er klar, skal de publiceres til tilføjelsesprogrammet Elektronisk faktureringstjeneste.

#### <a name="service-environment-status"></a>Status for tjenestemiljø

Tjenestemiljøer kan administreres via status. De mulige indstillinger er:

- **Ikke udgivet** – Miljøet er oprettet, men det er endnu ikke udgivet.
- **Udgivet** – Miljøet er udgivet i tilføjelsesprogrammet Elektronisk fakturering.
- **Ændret** – Attributterne i et udgivet miljø er ændret, men ændringerne er endnu ikke publiceret.

#### <a name="customer-secrets"></a>Kundehemmeligheder

Tjenesten for tilføjelsesprogrammet til elektronisk fakturering er ansvarlig for at opbevare af alle dine virksomhedsdata i de Azure-ressourcer, der ejes af din virksomhed. Hvis du vil sikre dig, at tjenesten fungerer korrekt, og at alle de virksomhedsdata, der kræves til og oprettes af tilføjelsesprogrammet til elektronisk fakturering, kun tilgås af tilføjelsesprogrammet, skal du oprette to hovedressourcer i Azure:

- En Azure Storage-konto (Blob-lager) der kan opbevare elektroniske fakturaer
- En Azure Key Vault, der kan opbevare certifikater og URI'en (Uniform Resource Identifier) for lagerkontoen

> [!NOTE]
> En dedikeret Key Vault og kundelagerkonto skal tildeles specifikt til brug sammen med tilføjelsesprogrammet til elektronisk fakturering.

Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

#### <a name="users"></a>Brugere

De enkelte tjenestemiljøer skal indeholde en oversigt over de brugere, der kan oprette forbindelse fra Dynamics 365 Finance og Dynamics 365 Supply Chain Management i tilføjelsesprogrammet Elektronisk fakturering.

#### <a name="publication"></a>Publikation

Når tjenestemiljøerne er klar, skal de publiceres til tilføjelsesprogrammet Elektronisk faktureringstjeneste, før de kan bruges. Der er kun publicerede miljøer tilgængelige i Finans og Supply Chain Management. Desuden skal et servicemiljø publiceres, før eventuelle opdateringer af attributterne i programmet træder i kraft for den elektroniske faktureringstjeneste.

### <a name="connected-applications"></a>Tilsluttede ansøgninger

Tilknyttede applikationer er de forekomster af Finans og Supply Chain Management, som du muligvis vil have kontakt til via RCS. Udover applikationens URL-adresse og dens lejer indeholder en tilknyttet applikation de legitimationsoplysninger, der gør det muligt for RCS at oprette forbindelse til miljøet.

Via de tilknyttede applikationer kan du konfigurere en del af funktionen til elektronisk fakturering i Finans og Supply Chain Management, så hele funktionen til elektronisk fakturering fungerer.

## <a name="finance-and-supply-chain-management"></a>Finance og Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>Integration til tilføjelsesprogrammet til elektronisk fakturering

Før du kan bruge Finans og Supply Chain Management til at udstede elektroniske fakturaer via tilføjelsesprogrammet Elektronisk fakturering, skal tilføjelsesprogrammet være konfigureret, så der kan kommunikeres med tjenesten.

#### <a name="electronic-invoicing-add-on-integration-feature"></a>Funktionen i tilføjelsesprogrammet til elektronisk fakturering

Hvis du vil aktivere kommunikation mellem Finans og Supply Chain Management og **tilføjelsesprogrammet Elektronisk fakturering**, skal du aktivere funktionen til integration af tilføjelsesprogrammet Elektronisk fakturering i arbejdsområdet til **funktionsstyring**.

#### <a name="service-endpoint"></a>Tjenesteslutpunkt

Tjenesteslutpunktet er den URL-adresse, hvor tilføjelsesprogrammet Elektronisk fakturering er placeret. Før du kan udstede elektroniske fakturaer, skal tjenesteslutpunktet konfigureres i Finans og Supply Chain Management for at tillade kommunikation med tjenesten.

Hvis du vil konfigurere tjenesteslutpunktet, skal du gå til **Organisationsadministration \> Opsætning \> Elektronisk dokumentparameter** og derefter på fanen **Overførelsestjenester** i feltet **URL-adressen til tilføjelsesprogrammet til elektronisk fakturering** angive URL-adressen i tabellen, som beskrevet i afsnittet **Serviceslutpunkt**.

#### <a name="environments"></a>Miljøer

Det miljønavn, der angives i Finans og Supply Chain Management, henviser til navnet på det miljø, der oprettes i RCS og udgives i tilføjelsesprogrammet Elektronisk fakturering.

Miljøet skal konfigureres under fanen **Overførselstjenester** på **Elektronisk dokumentparameter**, så alle anmodninger om udstedelse af elektroniske fakturaer indeholder det miljø, hvor tilføjelsesprogrammet Elektronisk fakturering kan bestemme, hvilken funktion til elektronisk fakturering der skal behandle anmodningen.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfiguration af elektroniske fakturaer i RCS](e-invoicing-configuration-rcs.md)
- [Udsted elektroniske fakturaer i Finance og Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]