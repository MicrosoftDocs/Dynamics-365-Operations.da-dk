---
title: Komponenter til elektronisk fakturering i administration
description: Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af Elektronisk fakturering.
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840022"
---
# <a name="electronic-invoicing-administration-components"></a>Komponenter til elektronisk fakturering i administration

[!include [banner](../includes/banner.md)]


Dette emne indeholder oplysninger om de komponenter, der er knyttet til administration af Elektronisk fakturering. Det indeholder også oplysninger om, hvordan du konfigurerer Elektronisk fakturering.

## <a name="azure"></a>Azure

Bruges Microsoft Azure til at oprette Key Vault og lagerkontoen. Brug derefter hemmeligheder i konfigurationen af Elektronisk fakturering.

## <a name="lifecycle-services"></a>Lifecycle Services

Brug Microsoft Dynamics Lifecycle Services (LCS) til at aktivere mikroservices til dit LCS-implementeringsprojekt.

> [!NOTE]
> Installationen af mikroservice i LCS kræver mindst en virtuel maskine på niveau 2. Du kan finde flere oplysninger om miljøplanlægning under [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) er den grænseflade, der anvendes til konfigurering af Elektronisk fakturering. Ressourcer som f.eks. miljøer og funktioner til elektronisk fakturering oprettes, vedligeholdes og er hostet i RCS. Når ressourcerne er klar, publiceres de til Elektronisk faktureringstjeneste.

Vedrørende RCS-tilmelding se [Regulatory services](https://marketing.configure.global.dynamics.com/).

Du kan finde flere oplysninger om RCS i [Regulatory Configuration Services (RCS) – globaliseringsfunktioner](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Integration med elektronisk fakturering 

Før du kan bruge RCS til at konfigurere elektroniske fakturaer, skal du konfigurere RCS til at tillade kommunikation med Elektronisk fakturering. Du fuldfører denne konfiguration under fanen **Elektronisk fakturering** på siden **Elektroniske rapporteringsparametre**.

#### <a name="service-endpoint"></a>Tjenesteslutpunkt

Elektronisk fakturering er tilgængelig i flere geografiske Azure-datacentre. Følgende tabel viser tilgængeligheden pr. region.

| Datacenter Azure-geografisk område |
|----------------------------|
| Det østlige USA                    |
| Det vestlige USA                    |
| Det nordlige Europa                   |
| Det vestlige Europa                    |

### <a name="service-environments"></a>Tjenestemiljøer

Tjenestemiljøer er logiske partitioner, der er oprettet for at understøtte udførelsen af funktionerne for elektronisk fakturering i Elektronisk fakturering. Sikkerhedsfunktionerne og de digitale certifikater, og de nye styreformer (dvs. adgangsrettigheder), skal konfigureres på tjenestemiljøniveau.

Kunder kan oprette lige så mange tjenestemiljøer, de ønsker. Alle de tjenestemiljøer, som en kunde opretter, er uafhængige af hinanden.

Tjenestemiljøer skal oprettes og vedligeholdes i RCS. Når tjenestemiljøerne er klar, skal de publiceres til Elektronisk fakturering.

#### <a name="service-environment-status"></a>Status for tjenestemiljø

Tjenestemiljøer kan administreres via status. De mulige indstillinger er:

- **Ikke udgivet** – Miljøet er oprettet, men det er endnu ikke udgivet.
- **Publiceret** – Miljøet er udgivet til Elektronisk fakturering.
- **Ændret** – Attributterne i et udgivet miljø er ændret, men ændringerne er endnu ikke publiceret.

#### <a name="customer-secrets"></a>Kundehemmeligheder

Tjenesten til elektronisk fakturering er ansvarlig for at opbevare af alle dine virksomhedsdata i de Azure-ressourcer, der ejes af din virksomhed. Hvis du vil sikre dig, at tjenesten fungerer korrekt, og at alle de virksomhedsdata, der kræves til og oprettes af Elektronisk fakturering, tilgås korrekt, skal du oprette to hovedressourcer i Azure:

- En Azure Storage-konto (Blob-lager) der kan opbevare elektroniske fakturaer
- En Azure Key Vault, der kan opbevare certifikater og URI'en (Uniform Resource Identifier) for lagerkontoen

> [!NOTE]
> En dedikeret Key Vault og kundelagerkonto skal tildeles specifikt til brug sammen med Elektronisk fakturering.

Du kan finde flere oplysninger i [Oprette en Azure-lagerkonto og Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).

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

Hvis du vil konfigurere tjenesteslutpunktet, skal du gå til **Organisationsadministration \> Opsætning \> Elektronisk dokumentparameter** og derefter på fanen **Overførelsestjenester** i feltet **URL-adressen til Elektronisk fakturering** angive URL-adressen i tabellen, som beskrevet i afsnittet **Serviceslutpunkt**.

#### <a name="environments"></a>Miljøer

Det miljønavn, der angives i Finance og Supply Chain Management, henviser til navnet på det miljø, der oprettes i RCS og udgives i Elektronisk fakturering.

Miljøet skal konfigureres under fanen **Overførselstjenester** på **Elektronisk dokumentparameter**, så alle anmodninger om udstedelse af elektroniske fakturaer indeholder det miljø, hvor Elektronisk fakturering kan bestemme, hvilken funktion til elektronisk fakturering der skal behandle anmodningen.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Konfiguration af elektroniske fakturaer i RCS](e-invoicing-configuration-rcs.md)
- [Udsted elektroniske fakturaer i Finance og Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
