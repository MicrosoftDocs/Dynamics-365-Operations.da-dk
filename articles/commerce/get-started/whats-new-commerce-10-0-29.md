---
title: Forhåndsversion af Dynamics 365 Commerce 10.0.29 (oktober 2022)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Commerce 10.0.29.
author: josaw1
ms.date: 08/02/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c1f85fcd8f79106a3af93489d3bef608b9840bf3
ms.sourcegitcommit: 91f58a9863f4e8f30ac787c2a9771c1ff6a05f72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/03/2022
ms.locfileid: "9224232"
---
# <a name="preview-of-dynamics-365-commerce-10029-october-2022"></a>Forhåndsversion af Dynamics 365 Commerce 10.0.29 (oktober 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel viser funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Commerce forhåndsversion 10.0.29. Denne version har et build-nummer på 10.0.1326 og er tilgængelig i følgende plan:

- **Forhåndsversion:** august 2022
- **Generel tilgængelighed af version (selv-opdatering):** september 2022
- **Generel tilgængelighed af version (automatisk opdatering):** oktober 2022

## <a name="features-included-in-this-release"></a>Funktioner, der er inkluderet i denne version

Følgende tabel anfører de funktioner, der er inkluderet i denne version. Vi opdaterer muligvis denne artikel for at medtage funktioner i det build, som er foretaget, efter denne artikel blev udgivet.

| Funktionsområde | Funktion | Flere oplysninger | Aktiveret af   |
|---------|------------------|----------------|--------------| 
| B2B | [Aktivere support af salgsaftale på tværs af kanaler](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | Denne funktion gør det muligt for business-to-business-salgsorganisationer (B2B) at bruge salgsaftaler i Commerce headquarters til at definere kontraktbaseret prissætning for deres indkøbere. Når en B2B-køber bruger e-handelswebstedet, anvendes den kontraktbaserede prissætning, der er konfigureret for B2B-køberorganisationen, automatisk for hele produktregistrerings-, indkøbs- og betalingsprocessen. | Administration af funktioner<p>*Support af salgsaftale på tværs af handelskanaler* |
| Customer Service | [Aktivér kundeservice med Dynamics 365 Omnikanal til Customer Service](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | En førsteklasses supportoplevelse for kunder er nøglen til at give en personlig og tilfredsstillende handelserfaring for forbrugere. Der findes i øjeblikket flere berøringspunkter for handel, f.eks. fysiske butikker, onlinekanaler og sociale kanaler. Forbrugere forventer en personlig supportoplevelse på alle disse berøringspunkter. Denne funktion hjælper dig med at øge konverteringer af indkøbsvogn til salg, øge personlig kontakt med forbrugere og forbedre kundeservice ved at integrere med Dynamics 365 Omnikanal til Customer Service. | Aktiveres af administratorer/beslutningstagere |
| E-commerce | Understøttelse af produktsammenligning i e-handel | Gør det muligt for køberne at sammenligne produkter på tværs af en lang række kategorier, så de kan træffe den rigtige købsbeslutning for sig selv. Denne funktion er tilgængelig både for business-to-consumer (B2C) og B2B-websteder. | Webstedsgenerator | 
| Gavekort | Understøttelse af tabeller med detailgavekort til deling af data på tværs af virksomheder | Dynamics headquarters understøtter muligheden for at aktivere deling af data på tværs af virksomheder for bestemte tabeller i Dynamics-arkitekturen. I denne funktion tilføjer Dynamics 365 Commerce understøttelse af tabeller med detailgavekort til deling af data på tværs af virksomheder. Derfor kan et gavekort i ét firma nu få dataene duplikeret til et andet firma i miljøet. Ændringer, der foretages i tabellen med oprindelige firmagavekort, deles med tabellen med duplikerede firmagavekort. | Udviklere |
| Ydeevne | Fjerne RTS-afhængighed for scenarier med "rediger kunde" | Høj tilgængelighed og høj ydeevne er standardforventninger til POS- og e-handelskanaler. For at imødekomme disse forventninger behøver Dynamics 365 Commerce-kanaler ikke længere at være afhængige af realtidskommunikation med Commerce headquarters, når kundeoplysninger redigeres. Muligheden for at redigere kundeoplysninger asynkront for asynkrone og ikke-asynkrone kunder kan være med til at reducere antallet af opkald i realtid til Commerce headquarters. | Aktiveres af administratorer/beslutningstagere |

## <a name="feature-state-changes-in-this-release"></a>Ændringer af funktionstilstand i denne version

I følgende tabel vises de funktioner, der blev obligatoriske eller som standard var slået til i version 10.0.29. Alle disse funktioner vil automatisk være aktiveret for systemet, så snart du opdaterer til version 10.0.29. Obligatoriske funktioner kan ikke deaktiveres, men funktioner, der er aktiveret som standard, kan stadig deaktiveres ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabellen indeholder også funktioner, der tidligere var med i offentlig forhåndsversion, men som er blevet generelt tilgængelige i version 10.0.29. Denne ændring angiver, at funktionerne nu anbefales til brug i produktionsmiljøer. Disse funktioner er som standard deaktiverede, hvis intet andet er angivet. Hvis du vil bruge en af disse funktioner, skal du bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere dem.

| Funktion | Stilling | Ny funktionstilstand |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(Brasilien) Commerce-funktionalitet, der er specifik for Brasilien | Til som standard |
| RetailAdvancedGTETaxAdjustmentFeature | (Indien) Anvend GST beregnet for detailtransaktioner i Retail POS i detailopgørelser | Til som standard |
| RetailChronologicalInvoicePostingFeature_IT | (Italien) Aktivér detailfakturaer, der er bogført uden kronologisk rækkefølge | Til som standard |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (Mexico) Rabatregulering i Retail CFDI Global | Til som standard |
| RetailFiscalIntegrationConfigurationEnhancementFeature | Tilsidesættelser af teknisk profil for regnskabsintegration | Til som standard |
| RetailFiscalIntegrationConnectorLocationFeature | Direkte regnskabsintegration fra POS-kasseapparater | Til som standard |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | Sikkerhedskopiering af lokallager for regnskabsmæssig integration | Til som standard |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | Udskudt registrering af dokumenter | Til som standard |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | Regnskabsregistreringstilstand for POS-kasseapparater | Til som standard |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (Indien) Beregn GST ud fra fakturaadresse for e-handelsordrer | Til som standard |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (Polen) Standardstatus for salgsdokument for detailfakturaer | Til som standard |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (Mexico) Afrunding af genberegning af momsbasisbeløb i Retail CFDI-global. | Til som standard |
| RetailSupplementaryInvoiceFeature | Aktivér supplerende fakturaer for cash and carry-transaktioner, der er fuldført i detailbutikker | Til som standard |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  Aktivér lagerbuffere og lagerniveauer    |  Til som standard|
|RetailInboundOutboundInventoryValidationFeature|   Aktivér validering i POS-handlinger for indgående og udgående lager   |   Til som standard   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  Udvidet lagerberegningslogik på e-handels-kanalsiden |   Til som standard   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    Lagerreguleringer i POS   |  Til som standard  |
| RetailMultiplePickupDeliveryModeFeature |  Understøttelse af flere leveringsmåder ved afhentning     |   Obligatorisk    |
|  RetailProductAvailabilityOptimizationFeature |   Optimeret beregning af produkttilgængelighed  |  Obligatorisk |
|   RetailPricingDataManagerV2Feature   |   Forbedr performance for commerce-prissætningsprogram |   Obligatorisk |
|  RetailPricingPreventUnintendedRecalculationFeature   | Undgå utilsigtet prisberegning for handelsordrer    |  Obligatorisk  |
| RetailTeamsIntegration    |   Aktivér Microsoft Teams-integration| Obligatorisk   |  
| ConsumerEFDSyncProcessFeature_BR | (Brasilien) NFC-e synkron behandling | Til som standard |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | Understøttelse af interne og eksterne forbindelser i regnskabsintegrationsstrukturen | Obligatorisk |
| RetailTaxRegistrationIdEnableFeature_BR | (Brasilien) Søg efter debitorer i Retail POS efter momsregistreringsnumre | Obligatorisk |
| RetailTaxRegistrationIdEnableFeature_IN | (Indien) Søg efter debitorer i Retail POS efter momsregistreringsnumre | Obligatorisk |
| RetailTaxRegistrationIdEnableFeature_IT | (Italien) Administration af kundeoplysninger i Retail POS | Obligatorisk |
| RetailTaxRegistrationIdEnableFeature_PL | (Polen) Administration af kundeoplysninger i Retail POS | Obligatorisk |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (Detail-GST for Indien) Opdater kreditnotaer med referencer til oprindelige fakturaer | Obligatorisk |
| RetailUserDefinedCertificateProfileFeature | Brugerdefinerede certifikatprofiler til detailbutikker | Obligatorisk |
  

## <a name="additional-resources"></a>Yderligere ressourcer

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformsopdateringer til Finans- og driftsapps

Microsoft Dynamics 365 Commerce 10.0.29 inkluderer platformopdateringer. Du kan få mere vide i [Platformsopdateringer til version 10.0.29 af Finans- og driftsapps (oktober 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). 

### <a name="bug-fixes"></a>Fejlrettelser

Du kan finde flere oplysninger om de fejlrettelser, der er inkluderet i hver af de opdateringer, som er del af version 10.0.29, ved at logge på Lifecycle Services (LCS) og se [KB-artiklen](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 2

Vil du gerne vide mere om kommende og de senest frigivne funktioner i en af vores forretningsapps eller platforme?

Undersøg [Dynamics 365 og brancheskyer: 2022 frigivelsesplan bølge 2](/dynamics365-release-plan/2022wave2/). Vi har samlet alle oplysninger fra start til slut og top til bund i et enkelt dokument, som du kan bruge til planlægning.

### <a name="removed-and-deprecated-features"></a>Fjernede og udfasede funktioner

Artiklen om [fjernede eller udfasede funktioner i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) beskriver funktioner, der er blevet fjernet eller udfaset for Commerce.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Før en funktion fjernes fra produktet, vil du få besked om udfasning i artiklen [Fjernede eller udfasede funktioner i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 måneder, inden de fjernes.

For ændringer, der kun påvirker kompileringstiden, men som er binære, som er kompatible med sandkasse- og produktionsmiljøer, vil tidsrummet for udfasningen være mindre end 12 måneder. Det er typisk funktionelle opdateringer, der skal foretages i compileren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
