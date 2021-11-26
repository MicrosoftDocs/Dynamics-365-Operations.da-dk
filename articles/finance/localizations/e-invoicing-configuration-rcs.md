---
title: Konfigurere Elektronisk fakturering i RCS (Regulatory Configuration Services)
description: Dette emne forklarer, hvordan du konfigurerer elektronisk fakturering i Dynamics 365 Regulatory Configuration Services (RCS).
author: gionoder
ms.date: 11/08/2021
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
ms.openlocfilehash: 640244612a2a553ec09661635787cb7f8694283b
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779664"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a>Konfigurere Elektronisk fakturering i RCS (Regulatory Configuration Services)

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om konfigurationsfunktionerne til elektronisk fakturering i Dynamics 365 Regulatory Configuration Services (RCS).

Det er via konfigurationsfunktionerne, at elektronisk fakturering hjælper dig med at opfylde forretningsmæssige og lovgivningsmæssige krav til elektroniske fakturaer uden at skulle udføre kodning. Og i de scenarier, hvor elektroniske fakturaer skal godkendes elektronisk af en webtjeneste, kan konfigurationsfunktionerne også hjælpe dig med at opfylde kravene til udveksling af meddelelser med en webtjeneste uden at gøre nogen kode.

## <a name="electronic-reporting"></a>Elektronisk rapportering

Elektronisk rapportering (ER) understøtter elektronisk fakturering.

Tilknytningen af datamodeller og formater er konfigurerbare komponenter, der oprettes og vedligeholdes via ER og bruges i elektronisk fakturering. ER-formatdesigneren bruges til at oprette og vedligeholde filformater. Den bruges til at konfigurere funktioner til elektronisk fakturering.

Du kan finde flere oplysninger under [Oversigt over Elektronisk rapportering (ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Funktionerne Elektronisk fakturering

Funktionerne til elektronisk fakturering er ansvarlige for generering af elektroniske fakturaer via Elektronisk fakturering. De indeholder konfigurationsreglerne og bruger dem til at behandle de data, Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management sender til Elektronisk fakturering og til elektroniske fakturaer.

Funktionerne understøtter også scenarier, hvor overholdelse af filformatspecifikationer er påkrævet, og outputtet er en enkeltstående elektronisk fil. I de fleste tilfælde publiceres filformatspecifikationerne af skattemyndighederne.

Endelig understøtter funktionerne udveksling af meddelelser med eksterne webtjenester, der er tilknyttet enten skattemyndighederne eller af en eller flere godkendte parter, samt anmodninger om godkendelse eller et godkendelsesstempel på den elektroniske faktura.

## <a name="availability-of-electronic-invoicing-features"></a>Tilgængelighed af funktioner til elektronisk fakturering

Tilgængeligheden af funktionerne til elektronisk fakturering afhænger af landet eller området. Selvom nogle funktioner generelt er tilgængelige, er andre en del af forhåndsvisningen.

### <a name="generally-available-features"></a>Generelt tilgængelige funktioner

Følgende tabel viser de funktioner for elektronisk fakturering, der er generelt tilgængelige.

| Land/område | Funktionsnavn                         | Forretningsdokument |
|----------------|--------------------------------------|-------------------|
| Østrig        | Østrigske elektroniske fakturaer (AT)    | Salgsfakturaer og projektfakturaer |
| Belgien        | Belgisk elektronisk faktura (BE)      | Salgsfakturaer og projektfakturaer |
| Brasilien         | Brasiliansk NF-e (BR)                  | Regnskabsdokumentmodel 55, korrektionsbreve, annulleringer og annulleringer |
| Brasilien         | Brasiliansk NFS-e ABRASF Curitiba (BR) | Service regnskabsdokumenter |
| Brasilien         | Brasiliansk NF-e import fra mail (BR) | Regnskabsdokumentmodel 55 |
| Danmark        | Dansk elektronisk faktura (DK)       | Salgsfakturaer og projektfakturaer |
| Egypten          | Egyptisk elektronisk faktura (EG)     | Salgsfakturaer og projektfakturaer |
| Estland        | Estisk elektronisk faktura (EE)     | Salgsfakturaer og projektfakturaer |
| Finland        | Finsk elektronisk faktura (FI)      | Salgsfakturaer og projektfakturaer |
| Frankrig         | Fransk elektronisk faktura (FR)       | Salgsfakturaer og projektfakturaer |
| Tyskland        | Tysk elektronisk faktura (DE)       | Salgsfakturaer og projektfakturaer |
| Italien          | FatturaPA (IT)                       | Salgsfakturaer og projektfakturaer |
| Nederlandene    | Hollandsk elektronisk faktura (NL)        | Salgsfakturaer og projektfakturaer |
| Norge         | Norsk elektronisk faktura (NO)    | Salgsfakturaer og projektfakturaer |
| Spanien          | Spansk elektronisk faktura (ES)      | Salgsfakturaer og projektfakturaer |
| Europa         | PEPPOL Elektronisk faktura            | PEPPOL salgsfakturaer og projektfakturaer |
| Europa         | PEPPOL-kreditorfaktura                | PEPPOL-import af kreditorfakturaer |
| Saudi-Arabien   | Elektronisk faktura for Saudi-Arabien (SA)| Salgsfakturaer og projektfakturaer |

### <a name="preview-features"></a>Prøveversioner

Følgende tabel viser de funktioner for elektronisk fakturering, der er en forhåndsvisning i øjeblikket.

| Land/område | Funktionsnavn                         | Forretningsdokument |
|----------------|--------------------------------------|-------------------|
| Mexico         | Mexicansk CFDI (MX)                    | Salgsfakturaer, følgesedler, lageroverførsler, betalingstillæg og annulleringer |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Konfigurerbare komponenter for funktioner til elektronisk fakturering

Funktionerne til elektronisk fakturering består af følgende grupper konfigurerbare komponenter:

- **Formater**: Formater giver dig mulighed for at konfigurere, hvad Elektronisk fakturering skal generere, når et elektronisk dokument bliver en elektronisk faktura. Formater omfatter formatkonfigurationen for den elektroniske faktura og for filer og meddelelser, der bruges til at sende anmodninger og modtage svar, når kommunikation med en ekstern webtjeneste er påkrævet.
- **Handlinger**: Handlinger giver dig mulighed for at konfigurere, hvordan Elektronisk fakturering genererer transformationen af et elektronisk dokument, som Finance og Supply Chain Management har sendt til en elektronisk faktura.
- **Anvendelsesregler**: Anvendelsesregler giver dig mulighed for at konfigurere den kontekst, som Elektronisk fakturering skal overveje for at behandle en funktion til elektronisk fakturering.
- **Variabler**: Variabler giver dig mulighed for at konfigurere understøttelse af konstruktionen af konfigurationslogikken. Variabler kan bruges som input af værdier til at udføre en bestemt handling. Alternativt kan de arbejde som en udveksling af værdier mellem Finance og Supply Chain Management og Elektronisk fakturering.
- **Tilknytning af elektronisk dokumentmodel**: Ved hjælp af den elektroniske dokumentmodeltilknytning kan du konfigurere ER-modeltilknytningen. Modeltilknytning definerer datatilknytningen for den abstrakte faktura, der er integreret i Elektronisk fakturering, når der sendes elektroniske dokumenter.
- **Kontekstmodel for faktura**: Med modellen til fakturakontekst kan du konfigurere ER-fakturakontekstmodellen og definere rammerne for en funktion til elektronisk fakturering.
- **Svartyper**: Svartyper giver dig mulighed for at konfigurere, hvad Elektronisk fakturering skal opdatere i Finance og Supply Chain Management som et resultat af den elektroniske fakturabehandling.

### <a name="formats"></a>Formater

På følgende lister vises de ER-formatkonfigurationer, der er tilgængelige for funktionerne for elektronisk fakturering.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Østrigske (AT) elektroniske fakturaer: Salgs- og projektfakturaer for Østrig

- OIOUBL-salgsfaktura
- OIOUBL-projektfaktura
- OIOUBL-salgskreditnota
- OIOUBL-projektkreditnota

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belgisk (BE) elektroniske fakturaer: Salgs- og projektfakturaer for Belgien

- UBL-salgsfaktura (BE)
- UBL-projektfaktura (BE)
- UBL-projektkreditnota (BE)
- UBL-salgskreditnota (BE)

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brasiliansk (BR) NF-e: NF-e Federal (Brasilien)

- NF-e indsend Eksportformat (BR)
- NF-e korrektionsbrev, eksportformat (BR)
- NF-e annuller eksportformat (BR)
- NF-e udelad eksportformat (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brasiliansk NFS-e (BR): NFS-e ABRASF Curitiba city

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF Inquire Curitiba (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Dansk (DK) elektronisk faktura: Salgs- og projektfakturaer for Danmark

- OIOUBL-salgsfaktura
- OIOUBL-projektfaktura
- OIOUBL-salgskreditnota
- OIOUBL-projektkreditnota

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Hollandsk (NL) elektronisk faktura: Salgs- og projektfakturaer for Nederlandene

- UBL-salgsfaktura (NL)
- UBL-projektfaktura (NL)
- UBL-projektkreditnota (NL)
- UBL-salgskreditnota (NL)

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Egyptisk (EG) elektroniske fakturaer: Salgs- og projektfakturaer for Egypten

- Salgsfaktura (EG)(Fakturering)
- Projektfaktura (EG)(Fakturering)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Estisk (EE) elektronisk faktura: Salgs- og projektfakturaer for Estland

- Salgsfaktura (EE)
- Projektfaktura (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Finsk (FI) elektronisk faktura: Salgs- og projektfakturaer for Finland

- Salgsfaktura (FI)
- Projektfaktura (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Fransk (FR) elektroniske fakturaer: Salgs- og projektfakturaer for Frankrig

- UBL-salgsfaktura (FR)
- UBL-projektfaktura (FR)
- UBL-projektkreditnota (FR)
- UBL-salgskreditnota (FR)

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Tysk (DE) elektroniske fakturaer: Salgs- og projektfakturaer for Tyskland

- Salgsfaktura (DE)
- Projektfaktura DE

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Italiensk (IT) elektroniske fakturaer: Salgs- og projektfakturaer for Italien

- Salgsfaktura (IT)
- Projektfaktura (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Mexicansk (MX) CFDI: CFDI for Mexico

- CFDI fakturaformat (MX)
- CDFI Følgeseddel (MX)
- CFDI Lageroverførsler (MX)
- CFDI betalingsformat (MX)
- CFDI fakturaformat for annullering (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Norsk (NO) elektroniske fakturaer: Salgs- og projektfakturaer for Norge

- OIOUBL-salgsfaktura
- OIOUBL-projektfaktura
- OIOUBL-salgskreditnota
- OIOUBL-projektkreditnota

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL elektroniske faktura: PEPPOL salgs- og projektfakturaer

- PEPPOL Salgsfaktura
- PEPPOL Projektfaktura
- PEPPOL Salgskreditnota
- PEPPOL Projektkreditnota

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Spansk (ES) elektronisk faktura: Salgs- og projektfakturaer for Spanien

- Salgsfaktura (ES)
- Projektfaktura (ES)

#### <a name="saudi-arabian-sa-electronic-invoice-sales-and-project-invoices-for-saudi-arabia"></a>Saudi-Arabien (SA) elektronisk faktura: Salgs- og projektfakturaer for Saudi-Arabien

- Salgs-e-faktura (SA)
- Projekt-e-faktura (SA)

Ud over de konfigurationer af ER-formater, der som standard er tilgængelige i det format, der skal bruges sammen med tjenesten Elektronisk fakturering, kan du også oprette dine egne konfigurationer af ER-formater. De formatkonfigurationer, der oprettes til brug sammen med funktionerne i Elektronisk fakturering, understøtter dog ikke direkte reference til tabellerne Økonomi eller Supply Chain Management eller nogen af de tilsvarende metadata. Kun referencer til ER-modeltilknytningen understøttes.

### <a name="actions"></a>Handlinger

Følgende tabel indeholder de tilgængelige handlinger, og om de aktuelt er tilgængelige eller stadig i prøveversion.

| Handling                                        | Betegnelse                                                                  | Tilgængelighed         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Transformere document                            | Kør format for elektronisk rapportering for at transformere dokumentet.                   | Generelt tilgængelig  |
| Underskriv xml dokument                             | Signer xml-dokumenter med digital signatur.                                   | Generelt tilgængelig  |
| Signer JSON-dokument til de egyptiske momsmyndigheder | Signer json-dokumenter med digital signatur for egyptiske skattemyndigheder.       | Generelt tilgængelig  |
| Integrer med egyptisk ETA-tjeneste           | Kommuniker med egyptiske skattemyndigheder.                                     | Generelt tilgængelig  |
| Kald brasiliansk SEFAZ-tjeneste                  | Integrer med brasiliansk SeFAZ-tjeneste til indsendelse af regnskabsdokumenter.       | Generelt tilgængelig  |
| Kald mexicansk PAC-tjeneste                      | Integrer med mexicansk PAC-tjeneste til CFDI-overførsel.                      | Som eksempel           |
| Behandle svar                              | Analyser svaret, der er modtaget fra webtjenesteopkaldet.                     | Generelt tilgængelig  |
| Brug MS Power Automate                         | Integrer med det indbyggede flow i Microsoft Power Automate.                       | Som eksempel           |

### <a name="applicability-rules"></a>Anvendelighedsregler

Anvendelsesregler er konfigurerbare udtryk, der defineres på funktionsniveau til elektronisk fakturering. Reglerne er konfigureret til at give en kontekst til udførelse af funktioner for elektronisk fakturering via egenskabssættet for elektronisk fakturering.

Når et forretningsdokument fra Finance eller Supply Chain Management sendes til elektronisk fakturering, indeholder forretningsdokumentet ikke en eksplicit reference, der giver mulighed for, at funktionen Elektronisk fakturering er indstillet til at kalde en bestemt elektronisk faktureringsfunktion for at behandle afsendelsen.

Når forretningsdokumentet er konfigureret korrekt, indeholder det dog de elementer, der er nødvendige for, at elektronisk fakturering kan fortolke, hvilken funktion til elektronisk fakturering der skal vælges, og derefter generere den elektroniske faktura.

Anvendelsesregler giver mulighed for, at den elektroniske faktureringsfunktionalitet kan finde de nøjagtige funktioner for elektronisk fakturering, der skal bruges til behandling af indsendelsen. Dette gøres ved at sammenholde indholdet fra det indsendte forretningsdokument med klausulerne i anvendelsesreglerne.

Der implementeres f.eks. to funktioner til elektronisk fakturering med relaterede anvendelsesregler i egenskabssættet for elektronisk fakturering.

| Elektronisk faktureringsfunktion | Anvendelighedsregler        |
|------------------------------|--------------------------- |
| T                            | <p>Land = BR</p><p>og</p><p>Juridisk enhed = BRMF</p>  |
| B                            | <p>Land = MX</p><p>og</p><p>Juridisk enhed = MXMF</p>  |

Hvis et forretningsdokument fra Finance eller Supply Chain Management indsendes til egenskabssættet for elektronisk fakturering, indeholder forretningsdokumentet følgende attributter angivet som:

- Land = BR
- Juridisk enhed = BRMF

Funktionen Elektronisk fakturering vælger den elektroniske faktureringsfunktion **A**, som bruges til at behandle indsendelsen og generere den elektroniske faktura.

Ligeledes, hvis forretningsdokumentet indeholder:

- Land = MX
- Juridisk enhed = MXMF

Funktionen **B** til elektronisk fakturering er valgt for at generere den elektroniske faktura.

Konfigurationen af regler for anvendelighed kan ikke være tvetydig. Det betyder, at to eller flere funktioner til elektronisk fakturering ikke kan have samme klausul, da det ellers ikke medfører et valg. Hvis der er dobbeltfunktioner til elektronisk fakturering, skal du for at undgå tvetydighed bruge ekstra klausuler til at tillade, at funktionen Elektronisk fakturering bruges til at skelne mellem de to funktioner til elektronisk fakturering.

Se f.eks. funktionen **C** til elektronisk fakturering. Denne funktion er en kopi af funktionen **A** til elektronisk fakturering.

| Elektronisk faktureringsfunktion | Anvendelighedsregler        |
|------------------------------|--------------------------- |
| T                            | <p>Land = BR</p><p>og</p><p>Juridisk enhed = BRMF</p>  |
| K                            | <p>Land = BR</p><p>og</p><p>Juridisk enhed = BRMF</p>  |

I dette eksempel er funktion **C** foran indsendelse af et forretningsdokument, der indeholder følgende:

- Land = BR
- Juridisk enhed = BRMF

Funktionen Elektronisk fakturering kan ikke se, hvilken elektronisk faktureringsfunktion der skal bruges til behandling af indsendelsen, da indsendelserne indeholder nøjagtigt de samme klausuler.

Hvis du vil oprette en forskel mellem de to funktioner via anvendelighedsregler, skal der føjes en ny klausul til en af funktionerne, så funktionssættet Elektronisk fakturering kan vælge den korrekte funktion til elektronisk fakturering.

| Elektronisk faktureringsfunktion | Anvendelighedsregler        |
|------------------------------|--------------------------- |
| T                            | <p>Land = BR</p><p>og</p><p>Juridisk enhed = BRMF</p>  |
| K                            | <p>Land = BR</p><p>og</p><p>Juridisk enhed = BRMF</p><p>og</p><p>Model=55</p>  |

Følgende ressourcer er tilgængelige for at understøtte oprettelse af mere komplekse klausuler:

Logiske operatorer:
- Og
- Eller

Operatortyper:
- Lig med
- Ikke lig med
- Større end
- Mindre end
- Større end eller lig med
- Mindre end eller lig med
- Indeholder
- Begynder med

Datatyper:
- Streng
- Tal
- Boolesk
- Dato
- UUID

Egenskab til gruppering og opdeling af grupperede klausuler.
Eksemplet ser sådan ud.

| Elektronisk faktureringsfunktion | Anvendelighedsregler        |
|------------------------------|--------------------------- |
| K                            | <p>Land = BR</p><p>og</p><p>(Juridisk enhed = BRMF</p><p>eller</p><p>Model=55)</p>  |


## <a name="configuration-providers"></a>Konfigurationsudbydere

Konfigurationsudbydere indeholder funktionerne til elektronisk fakturering og deres ER-komponenter, f.eks. modeltilknytning, formatkonfiguration og kontekstmodel. De udgiver funktioner for elektronisk fakturering og ER-komponenter i det tilknyttede globale lager. Derfra kan andre organisationer hente dem.

Før du konfigurerer funktionerne for elektronisk fakturering via RCS, skal du konfigurere din egen organisation som en konfigurationsudbyder i modulet **Elektronisk rapportering**. Du kan finde flere oplysninger om, hvordan du angiver en konfigurationsudbyder til **Aktiv**, i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Se funktioner for elektronisk fakturering på det globale lager

Du kan gennemse de funktioner for elektronisk fakturering, der er tilgængelige i Global repository for en bestemt konfigurationsudbyder, ved at synkronisere organisationens RCS-forekomst. Når synkroniseringen er fuldført, opdateres listen over tilgængelige funktioner for elektronisk fakturering.

## <a name="importing-electronic-invoicing-features"></a>Importer funktioner til elektronisk fakturering

Før du bruger eller konfigurerer funktionerne til elektronisk fakturering, skal du importere dem til organisationens RCS-forekomst. Importhandlingen opretter en lokal kopi af funktionerne og kopierer alle ER-genstande, som funktionerne bruger (f.eks. formatkonfigurationer og modelkonfigurationer) til din organisations RCS-forekomst.

Du kan importere funktioner til elektronisk fakturering fra enhver konfigurationsudbyder.

## <a name="creating-electronic-invoicing-features"></a>Opret funktioner til elektronisk fakturering

Du kan enten oprette funktion til elektronisk faktura fra bunden, eller du kan hente den fra en eksisterende funktion til elektronisk fakturering.

Når du opretter en funktion til elektronisk fakturering helt fra bunden, skal du manuelt tilføje ER-komponenter (f.eks. funktionsversionskonfigurationer og andre konfigurationer, f.eks. opsætning af funktionsversion og programopsætning). Når du opretter en funktion ved at hente den fra en anden funktion, arver den nye funktion alle konfigurationer fra den oprindelige funktion. 

## <a name="electronic-invoicing-feature-version"></a>Funktionsversionen Elektronisk fakturering

Funktionsversionen Elektronisk fakturering. Når der oprettes en ny version, øges versionsnummeret automatisk. Der kan defineres en "gældende fra"-dato for den nye version.

Funktionsversioner til elektronisk fakturering følger en livscyklus, der har op til tre statusser:

- **Kladde** - Hvis en funktionsversion har denne status, kan du redigere dens konfigurationsattributter og alle dens genstande (f.eks. filformatkonfigurationer).
- **Fuldført** – Hvis en funktionsversion har denne status, er den publiceret til det globale lager, der er tilknyttet din organisation. Du kan ikke længere redigere funktionsversionen eller nogen af ER-komponenterne.
- **Publiceret** – Hvis en funktionsversion har denne status, er den publiceret til Elektronisk fakturering. Du kan ikke længere redigere funktionsversionen eller nogen af ER-komponenterne.

### <a name="feature-configurations"></a>Funktionskonfigurationer

Funktionskonfigurationer indeholder alle de ER-formatkonfigurationer, der bruges af de elektroniske faktureringsfunktioner. Alle de elektroniske filer, som en elektronisk faktureringsfunktion bruger under behandlingen, kommer fra de formatkonfigurationer, der er føjet til funktionskonfigurationerne for den pågældende funktion.

Fra funktionskonfigurationerne kan du få adgang til ER-formatdesigneren, som er det ER-værktøj, der bruges til at oprette formatkonfigurationer.

### <a name="feature-setup"></a>Konfiguration af funktion

Funktionsopsætninger bruges sammen med funktionskonfigurationer. De enkelte funktionsopsætninger omfatter et sæt handlinger, anvendelsesregler og variabler, der giver den forventede funktionalitet, så en funktion til elektronisk fakturering kan opfylde et bestemt krav i forbindelse med den elektroniske faktura.

### <a name="application-setup"></a>Ansøgningsopsætning

Programopsætningen skal knyttes til et tidligere oprettet tilknyttet program.

Ved hjælp af programopsætningen kan du konfigurere den del af en elektronisk faktureringsfunktion, der skal udføres i Finans og Supply Chain Management. Der skal være mindst tre konfigurerbare komponenter uanset funktionen til elektronisk fakturering:

- **Tabelnavn** – Den enhed i Finans og Supply Chain Management, der opbevarer de bogførte fakturaer, og som funktionen til elektronisk fakturering er baseret på.
- **Kontekst** – Navnet på den fakturakontekstmodel, der blev konfigureret via ER.
- **Kontekst** – Navnet på den fakturakontekstmodel, der blev konfigureret via ER.

> [!IMPORTANT]
> Den konfiguration, der er angivet i programopsætningen, kan ses i Finans og Supply Chain Management. Gå til **Organisationsadministration \> Konfiguration \> Parameter for elektroniske dokumenter**. Vælg **Implementer** under fanen **Elektronisk dokument**, og vælg derefter indstillingen **Tilknyttet program**.

### <a name="deploying-feature-versions"></a>Implementere funktionsversioner

I RCS bruger du kommandoen **Implementer** til at måludgive en version af en elektronisk faktureringsfunktion. Vælg **Implementer**, og vælg derefter en af følgende indstillinger for at definere destinationen for installationen: 

- **Servicemiljø** – Når destinationen for installationen er tjenestemiljøet, udgives den elektroniske faktureringsfunktionsversion i tjenestemiljøet. Elektronisk fakturering er derefter klar til at modtage og behandle elektroniske dokumenter, som Finance og Supply Chain Management sender.
- **Tilknyttet program** – Når målet for installationen er det tilknyttede program, skrives den konfiguration, der leveres af programopsætningen, i den forekomst af Finans og Supply Chain Management, som tidligere er knyttet til det.

Kun elektroniske faktureringsfunktionsversioner, der har status **Fuldført**, kan implementeres i enten et servicemiljø eller et tilknyttet program.

### <a name="removing-feature-versions"></a>Fjerne funktionsversioner

I RCS bruger du kommandoen **Fjern installeret** til at fjerne en bestemt elektronisk faktureringsfunktionsversion fra et servicemiljø i Elektronisk fakturering.

> [!IMPORTANT]
> Kommandoen **Fjern installeret** fungerer kun i tjenestemiljøer. Den fjerner ikke elektroniske faktureringsfunktionsversioner fra tilknyttede programmer.

### <a name="rebasing-electronic-invoicing-features"></a>Rebasere funktioner til elektronisk fakturering

Når en funktion til elektronisk fakturering afledes af en anden, opdaterer kommandoen **Rebaser** den afledte funktion med de ændringer, der er indført i den oprindelige funktion.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Udsted elektroniske fakturaer i Finance og Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
