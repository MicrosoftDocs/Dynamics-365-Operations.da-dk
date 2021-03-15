---
title: Oversigt over tilføjelsesprogrammet til elektronisk fakturering
description: Dette emne indeholder oplysninger om tilføjelsesprogrammet til elektronisk fakturering i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 01/22/2021
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
ms.openlocfilehash: 2c35b810151349384f105d9ac1d93e1885031450
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104202"
---
# <a name="electronic-invoicing-add-on-overview"></a>Oversigt over tilføjelsesprogrammet til elektronisk fakturering

[!include [banner](../includes/banner.md)]

Tilføjelsesprogrammet til elektronisk fakturering til Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management er en hyperskalerbar tjeneste til flere lejere, der giver mulighed for konfigurerbar behandling af elektroniske fakturadokumenter og konfigurerbar dokumentudveksling. Reglerne for behandling og integration er fuldt konfigurerbare, og logikken køres uden for Finance og Supply Chain Management. Tjenesten er primært rettet mod e-fakturabehandling i virksomhed-til-myndighed-scenarier, men den kan tilpasses og konfigureres til andre formål.

Tilføjelsesprogrammet til elektronisk fakturering kan hjælpe dig med at opnå følgende mål:

- Hurtig og nem implementering af lande-/områdespecifikke krav
- Standardiserede implementeringer af en løsning til tilføjelsesprogrammet til elektronisk fakturering
- Forbedret sporing af dokumenthistorik
- Kortere implementeringscyklus
- Reducerede samlede ejeromkostninger (TCO)
- Konfigurationer, der nemt kan justeres uden behov for nødvendige kodeændringer
- Enklere konfigurationspakke
- Indbygget eksport, import og integration samt nemme udvidelsesmuligheder i behandlingen af e-fakturadokumenter
- Nem genbrug af de samme konfigurationer for eksport, import og integration på tværs af virksomheder

Hvis du vil bruge tilføjelsesprogrammet til elektronisk fakturering, skal du installere det fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS). Derefter skal du følge installationsproceduren for at aktivere integrationen med Finance eller Supply Chain Management. Du kan finde flere oplysninger i [Kom i gang med tilføjelsesprogrammet til elektronisk fakturering](e-invoicing-get-started.md).

## <a name="service-availability"></a><a name="availability"></a>Tilgængelighed af tjeneste

I øjeblikket er tilføjelsesprogrammet Elektronisk fakturering tilgængelig for debitorer via programmet forhåndsvisning, og i næste fase vil tjenesten være generelt tilgængelig. Da funktioner, der adresserer lande-/områdespecifikke krav, kan være begrænset i forskellige faser af udgivelsen, skal du altid kontrollere den nyeste dokumentation, der fremhæver dækningen og omfanget af understøttede lande-/områdespecifikke løsninger.

Tilføjelsesprogrammet til elektronisk fakturering er udrullet i følgende geografiske Azure-områder:

- United States
- Europa

> [!NOTE]
> Tilføjelsesprogrammet til elektronisk fakturering understøtter ikke udrulninger i det lokale miljø.

## <a name="extended-configurability"></a>Udvidet konfigurerbarhed

Tilføjelsesprogrammet til elektronisk fakturering kan bruges i scenarier, hvor du skal oprette og sende et elektronisk dokument til de udpegede parter. Det er specialdesignet til at køre et konfigurerbart flow til behandling af handlinger baseret på modtagne data. De indstillinger for konfigurerbarhed, der er tilgængelige i Finance og Supply Chain Management, er begrænset til ændring af dokumenter. Tjenesten udvider disse indstillinger ved at tilføje de konfigurerbare integrationer, der er tilgængelige i den. Desuden vil alle de funktioner til elektroniske fakturaer, der tidligere var tilgængelige, f.eks. brasiliansk Nota fiscal eletrônica (NF-e), mexicansk Comprobante Fiscal Digital por Internet (CFDI) eller andre vesteuropæiske funktioner som Universal Business Language (UBL)/Pan-European Public Procurement OnLine (PEPPOL), der bruges til eksport og import og til at muliggøre integration med eksterne webtjenester.

## <a name="feature-highlights"></a>Fremhævning af funktioner

- Køreklar integration med Finance og Supply Chain Management
- Ensartet brugeroplevelse i forbindelse med konfiguration og overvågning af e-fakturaprocessen for alle lande eller områder
- Hurtigere, nemmere og mere økonomisk implementering af løsninger til tilføjelsesprogrammet til elektronisk fakturering i nye lande eller områder
- Konfiguration af tjenesten ved hjælp af RCS (Regulatory Configuration Service) og funktionsopsætninger for globalisering
- Transformation af forretningsdata til flere e-fakturaformater (XML, JavaScript Object Notation \[JSON\], TXT og kommaseparerede værdier \[CSV\]) ved hjælp af de konfigurationer, der er defineret i RCS:

    - Elektroniske rapporteringsformater, der er tilgængelige for lande eller områder, hvor det ikke er muligt at konfigurere en transformation til e-fakturaer

- Konfigurerbar indsendelse af e-fakturaer til eksterne webtjenester, herunder certificeringshåndtering via digitale signaturer:

    - Indbygget og konfigurerbar integration, der nemt kan udvides, med yderligere indhold til flere lande/områder

    > [!NOTE]
    > I øjeblikket understøttes et begrænset antal direkte indsendelser. Du kan finde flere oplysninger i afsnittet [Tilgængelighed af tjeneste](#availability) tidligere i dette emne. Support vil blive udvidet i fremtiden.

- Håndtering af svar fra webtjenester, herunder konfigurerbar håndtering af undtagelsesmeddelelser
- Understøttelse af elektroniske signaturer (f.eks. ved at bruge XMLDSig-signeringsalgoritmen)
- Batchbehandling af e-fakturameddelelser

## <a name="architecture-and-data-flow"></a>Arkitektur og dataflow

Når tilføjelsesprogrammet til elektronisk fakturering er installeret fra LCS, og den nødvendige konfiguration er fuldført i alle nødvendige programmer, oprettes der en sikker forbindelse. Tjenesten er i øjeblikket placeret i datacentre i USA og Europa. Tjenestens placering kan derfor være forskellig fra placeringen af den relaterede Finance- og Supply Chain Management-instans. Når du har fuldført konfigurationen af tilføjelsesprogrammet til elektronisk fakturering og slår integrationen til, når der sendes en elektronisk faktura, sendes masterdata og transaktionsdata, der er knyttet til et bestemt dokument, til tilføjelsesprogrammet til elektronisk fakturering.

> [!NOTE]
> Hvis din elektroniske faktura eller et andet dokument indeholder personlige data, skal du kontrollere, at brugen af denne funktion opfylder den generelle forordning om databeskyttelse (GDPR) og andre forordninger, der vedrører overførsel af personlige data.

### <a name="high-level-description-of-the-data-flow"></a>Kort beskrivelse af dataflowet

1. Klienten sender et godkendt forretningsdokument til tjenesten.
2. På baggrund af de oplysninger om kontekst, der modtages fra klienten, vælger tjenesten det gældende behandlingsflow.
3. Tjenesten kører behandlingshandlingerne. Disse handlinger kan omfatte transformation af forretningsdokumentet til en elektronisk faktura, anvendelse af en elektronisk signatur og indsendelse af dokumentet til en ekstern webtjeneste.
4. Alle modtagne og behandlede dokumenter gemmes i kundens Azure Blob Storage.
5. Alle lejerhemmeligheder og -certifikater, der blev brugt til behandling, gemmes i kundens Azure Key Vault.
6. Tjenesten leverer oplysninger efter behov til klienten om status for behandling af det forretningsdokument, der er sendt.
7. Klienten modtager oplysninger om den fuldførte udførelse af behandlingen og gør alle logoplysninger tilgængelige. Det dokument, der blev oprettet eller modtaget under flowbehandlingen, tilvejebringes også.

I følgende illustration vises dataflowet til og fra tilføjelsesprogrammet til elektronisk fakturering.

![Dataflow for tilføjelsesprogrammet til elektronisk fakturering](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Aktivering og brug af tilføjelsesprogrammet Elektronisk fakturering kan kræve, at der sendes begrænsede data, herunder organisationens momsregistrerings-id. Dette vil blive overført til tredjepartsorganer, der er godkendt af skattemyndighederne, med det formål at sende elektroniske fakturaer i de foruddefinerede formater, der kræves til integration med myndighedernes webtjenester. De data, der importeres fra disse eksterne systemer til denne Dynamics 365-onlinetjeneste, er underlagt vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=512132). Yderligere oplysninger finder du i sektionerne med Erklæring om beskyttelse af personlige oplysninger i dokumentationen for den lande- eller områdespecifikke funktion.

## <a name="additional-resources"></a>Yderligere ressourcer
- [Administration af tjeneste](e-invoicing-service-administration.md)
- [Konfiguration af elektroniske fakturaer i RCS](e-invoicing-configuration-rcs.md)
- [Udsted elektroniske fakturaer i Finance og Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]