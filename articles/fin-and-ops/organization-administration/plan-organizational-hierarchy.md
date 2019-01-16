---
title: "Planlægge dit organisationshierarki"
description: "Før du opretter organisationer og organisationshierarkier, skal du være sikker på, at du forstår, hvordan du bedst udformer en model af din virksomhed."
author: sericks007
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 633d85333a510cec9cee2721e6e2330a47b6c78c
ms.contentlocale: da-dk
ms.lasthandoff: 12/18/2018

---

# <a name="plan-your-organizational-hierarchy"></a>Planlægge dit organisationshierarki

[!include [banner](../includes/banner.md)]

Før du opretter organisationer og organisationshierarkier i Microsoft Dynamics 365 for Finance and Operations, skal du sørge for at planlægge, hvordan din virksomhed udformes. Organisationsmodellen har en væsentlig indvirkning på implementeringen af Finance and Operations og på forretningsprocesserne.

Organisationshierarkier repræsenterer relationerne mellem de organisationer, som et firma består af. Derfor er strukturen i din virksomhed den vigtigste overvejelser, når du udformer organisationer. Vi anbefaler, at der defineres organisationsstrukturer baseret på feedback fra ledere og overordnede chefer fra funktionsområder, som f.eks. økonomi og regnskab, personale, drift, indkøb, salg og marketing.

Det er også vigtigt at overveje forholdet mellem organisationshierarkiet og økonomiske dimensioner, når du planlægger hierarkier. Du kan angive flere organisationshierarkier, der skal repræsentere forskellige visninger af din virksomhed. Ved hjælp af økonomiske dimensioner kan du oprette rapporter, der er baseret på disse visninger. Sammen med din Microsoft Dynamics 365 for Finance and Operations-partner kan du oprette hierarkier, der opfylder både organisatoriske og lovpligtige rapporteringsbehov.

> [!NOTE]
> Selvom du kan bruge økonomiske dimensioner til at repræsentere juridiske enheder uden at oprette de juridiske enheder i Finance and Operations, er økonomiske dimensioner ikke designet til at opfylde de driftsmæssige eller virksomhedsmæssige behov for de juridiske enheder. Funktionen for regnskab mellem enheder i Finance and Operations er kun udviklet i forbindelse med de regnskabsposter, der oprettes ved hver transaktion.

> [!IMPORTANT]
> Du skal ikke beslutte, hvordan organisationer skal udformes, kun baseret på oplysningerne i denne artikel. Denne dokumentation er en vejledning. Du kan samarbejde med din Finance and Operations-partner for at få yderligere vejledning. Jeres Finance and Operations-partner har erfaring fra flere forskellige brancher og på tværs af kundebasen.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Beslutte, om interne organisationer skal udformes som juridiske enheder eller driftsenheder

Du skal have mindst én juridisk enhed til at repræsentere din virksomhed i Finance and Operations. En juridisk enhed kan indgå juridisk bindende kontrakter og skal udarbejde regnskaber med afrapportering af deres præstation.

Juridiske enheder kan bruges til transaktionsmeddelelser virksomhed eller til konsolidering i Finance and Operations. Det betyder, at en juridisk enhed i Finance and Operations ikke nødvendigvis repræsenterer en reel enhed i virksomheden. En virksomhed, der deltager i transaktioner, kan f.eks. eje juridiske enheder for datterselskaber. I dette scenarie kræves der en juridisk enhed transaktioner, og en virtuel juridisk enhed kræves for at konsolidere resultaterne og saldiene for juridiske enheder for datterselskaber.

Interne organisationer i virksomheden, f.eks. regionale kontorer, kan repræsenteres som yderligere juridiske enheder eller driftsenheder i den primære juridiske enhed. Det kræves ikke, at en driftsenhed er en juridisk defineret organisation. Driftsenheder bruges til at styre økonomiske ressourcer og driftsprocesser i virksomheden. Afdelinger og bærere er f.eks. driftsenheder.

Nogle funktioner i Finance and Operations fungerer forskelligt, afhængigt af om organisationen er en juridisk enhed eller en driftsenhed. Du skal nøje overveje de funktioner, der er beskrevet nedenfor, når du tager din beslutning.

### <a name="master-data"></a>Masterdata

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Nogle masterdata, f.eks. kunder, betalingsbetingelser, skattemyndigheder og lokationsspecifikke bestilling af lager, skal konfigureres for hver juridiske enhed. Nogle masterdata, f.eks. brugere, produkter og de fleste personaledata, deles af alle juridiske enheder.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Masterdata deles af driftsenheder.

### <a name="module-parameters"></a>Modulparametre

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Parametre for moduler som Debitorparametre, Kreditorparametre og parametre for kontant- og bankstyring skal angives pr. juridisk enhed. Da opsætningen af modulet for juridiske enheder er forskellig, kan alle datterselskaber overholde lokale lovbestemte krav og forretningspraksis. En juridisk enhed med professionelle serviceydelser og en juridisk produktionsenhed kan f.eks. have forskellige modulparametre, selvom de refererer til samme moderselskab.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Modulparametrene deles mellem driftsenheder.

### <a name="data-security"></a>Datasikkerhed

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

De fleste data sikres automatisk af firma-id. Et firma-id er en entydig identifikator for de data, der er knyttet til en juridisk enhed. Et firma kan kun være tilknyttet én juridisk enhed, og en juridisk enhed kan kun være tilknyttet ét firma. Brugere kan kun få adgang til data for de selskaber, som de har adgang til. Du behøver ikke at tilpasse Finance and Operations for at sikre data pr. firma-id.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Data kan sikres pr. driftsenhed ved at oprette brugerdefinerede datasikkerhedspolitikker. Sikkerhedspolitikker bruges til at begrænse adgangen til data. Antag f.eks., at en bruger kun har tilladelse til at oprette indkøbsordrer i en bestemt driftsenhed. Du kan oprette datasikkerhedspolitikker for at forhindre brugeren i at få adgang til indkøbsordredata fra andre driftsenheder. Omfanget af transaktioner og antallet af sikkerhedspolitikker kan påvirke ydeevnen. Når du udformer sikkerhedspolitikker, skal du være opmærksom på ydeevne.

### <a name="ledgers"></a>Finans

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Der kræves en finanskonto, der indeholder en kontoplan, regnskabsvaluta, rapporteringsvaluta og regnskabskalender, for hver juridisk enhed. Der kan kun oprettes en balance for en juridisk enhed. Hovedkonti, dimensioner, kontostrukturer, kontoplaner og kontoregler kan bruges af flere juridiske enheder.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

En driftsenhed ikke have sine egne finansoplysninger. Hvis dine interne organisationer ikke kræver entydige poster, kan du udforme dem som driftsenheder. Finansoplysninger konfigureres for den overordnede juridiske enhed i hierarkiet. Opgørelser over indtægter kan oprettes for driftsenheder inden for en juridisk enhed eller for den overordnede juridiske enhed.

### <a name="fiscal-calendars"></a>Regnskabskalendere

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

De enkelte juridiske enheder har sin egen regnskabskalender. Hvis dine interne organisationer bruger forskellige regnskabsår og regnskabskalendere, skal du udforme organisationerne som juridiske enheder.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Driftsenheder skal dele en regnskabskalender. Hvis dine interne organisationer kan bruge de samme regnskabsår og regnskabskalendere, kan du udforme organisationerne som driftsenheder.

### <a name="consolidation"></a>Konsolidering

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Du skal konsolidere de økonomiske resultater for regionale kontorer i et enkelt konsolideret regnskab for at udarbejde regnskaber.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Konsolidering er ikke påkrævet, fordi dataene allerede deles mellem driftsenheder.

### <a name="centralized-payments"></a>Centraliserede betalinger

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Centraliserede betalinger skal konfigureres, så fakturaer for alle underordnede juridiske enheder kan betales til eller fra en enkelt overordnet juridisk enhed.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Centraliserede betalinger er ikke nødvendige, fordi alle fakturaer er registreret i en enkelt juridisk enhed.

### <a name="intercompany-transactions"></a>Interne transaktioner

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Interne salgsordrer, indkøbsordrer, betalinger eller indtægter kan anvendes på hinanden. Du behøver ikke at bruge kladdebilag. Du kan se interne transaktioner på niveauet for underfinanskonti (Debitor, Kreditor). I følgende eksempler illustreres det, hvordan interne transaktioner skal håndteres.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Eksempel 1: Hovedkvarteret leverer tjenester til regionale kontorer og skal pålægge de regionale kontorer udgifterne til disse tjenester.

Hvis du udformer det regionale kontor som en juridisk enhed, har du følgende muligheder:

- Hovedkvarteret opretter en kladdepostering for at krydspålægge det regionale kontor udgiften. Transaktionerne kan ikke være aldersfordelte.
- Hovedkvarteret sender en indkøbsordre for tjenesterne til det regionale kontor. Der oprettes automatisk en salgsordre i den juridiske enhed til det regionale kontor med posteringer i interne underfinanskonti.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Eksempel 2: Hovedkvarteret fremskaffer og betaler for den serviceydelse, der leveres til et regionalt kontor

Hvis du udformer det regionale kontor som en juridisk enhed, har du følgende muligheder:

- Fakturaen og betalingen følger de lovgivningsmæssige krav for hovedkvarteret. Hovedkvarteret kan oprette en kladdepostering for at krydspålægge det regionale kontor udgiften. Transaktionerne kan ikke være aldersfordelte.
- Fakturaen og betalingen følger de lovgivningsmæssige krav for hovedkvarteret. Hovedkvarteret kan oprette en transaktion for interne underfinanskonti.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Interne transaktioner mellem driftsenheder understøttes kun via kladdebilag. En driftsenhed kan ikke udstede eller modtage en indkøbsordre, en salgsordre eller en faktura fra en anden driftsenhed i samme juridiske enhed. Du kan ikke se interne transaktioner på niveauet for underfinanskonti (Debitor, Kreditor). I følgende eksempler illustreres det, hvordan interne transaktioner skal håndteres.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Eksempel 1: Hovedkvarteret leverer tjenester til regionale kontorer og skal pålægge de regionale kontorer udgifterne til disse tjenester.

Hvis du udformer det regionale kontor som en driftsenhed, angiver hovedkvarteret en udgiftspost, som pålægges det regionale kontor.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Eksempel 2: Hovedkvarteret fremskaffer og betaler for den serviceydelse, der leveres til et regionalt kontor

Hvis du udformer det regionale kontor som en driftsenhed, følger fakturaen og betalingen de lovgivningsmæssige krav for hovedkvarteret. Fakturaen kan pålægges det regionale kontor. I resultatopgørelsen skal du bruge en udlignende økonomisk dimension til at rapportere omkostninger for det regionale kontor.

### <a name="local-tax-requirements"></a>Lokale skattekrav

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

En juridisk enhed er underlagt myndighedernes skattelovgivning i det land/område, hvor den juridiske enhed er registreret. En juridisk enhed, der er registreret i Danmark, er f.eks. underlagt danske skattelove og bestemmelser. I Finance and Operations kan en juridisk enhed kun høre under ét land/område. Det land/område, du har valgt til den primære adresse for den juridiske enhed, bestemmer, hvilke lande-/områdespecifikke funktioner der er tilgængelige for den pågældende juridiske enhed. Hvis den juridiske enheds primære adresse f.eks. er i Danmark, bliver funktioner, der er relateret til danske skattelove og bestemmelser, tilgængelige. Hvis dine organisationer er i forskellige lande/områder og kræver forskellige lokale skatteindstillinger, skal du derfor konfigurere organisationerne som særskilte juridiske enheder.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Driftsenheder hører under samme land/område som den overordnede juridiske enhed. Driftsenheder i samme juridiske enhed ikke kan have forskellige lande-/områdespecifikke krav. Hvis dine organisationer er i samme land/område og bruger de samme indstillinger for skat, kan du oprette dem som driftsenheder.

### <a name="statutory-reporting-for-a-countryregion"></a>Lovpligtig rapportering for et land/område

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

For lande/områder, der understøttes i Finance and Operations, kan de fleste lovpligtige rapporter oprettes. Du kan finde oplysninger om, hvilke rapporter der er tilgængelige for hvert land/område i [Microsoft Dynamics-lokaliseringsportalen](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC) til Finance and Operations. (Logon til CustomerSource er påkrævet).

> [!NOTE]
> I Finance and Operations giver et posteringslag i finansmodulet dig mulighed for at angive reguleringsposter i et moderselskab, der bruger en anden regnskabsstandard end det underordnede selskab. I en virksomhed, der bruger almindeligt accepteret regnskabspraksis i Storbritannien (UK GAAP), kan du f.eks. angive reguleringsposter i posteringslaget. Disse poster kan konsolideres til et moderselskab, der bruger almindeligt accepterede regnskabsprincipper (GAAP) i USA. Reguleringsposterne påvirker ikke UK GAAP-rapportering.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Lovpligtige rapporter skal oprettes ved hjælp af et andet program. Du skal sikre, at data er hentet i Finance and Operations for at understøtte kravene i hver driftsenhed, hvor de adskiller sig fra kravene til hovedkvarter.

### <a name="currency"></a>Valuta

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Hvis dine organisationer skal bruge forskellige funktionelle valutaer, skal du udforme organisationerne som juridiske enheder. Funktionelle valutaer defineres pr. juridisk enhed. Du kan dog angive posteringer i flere valutaer.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Hvis dine organisationer kan bruge en enkelt funktionel valuta, kan du udforme organisationerne som driftsenheder. Driftsenheder skal dele en funktionel valuta. Du kan dog angive posteringer og oprette rapporter i flere valutaer.

### <a name="year-end-closing"></a>Ultimo ved årsafslutning

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Hvis lovgivningen og regnskabsmæssig praksis varierer i de lande/områder, hvor dine organisationer er placeret, kan du kræve forskellige procedurer til årsafslutning for de enkelte organisationer. Det betyder, at du skal udforme organisationerne som juridiske enheder. Hver juridiske enhed har sine egne procedurer til årsafslutning.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Hvis lovgivningen og regnskabsmæssig praksis er den samme i de lande/områder, hvor dine organisationer er placeret, kan du bruge et enkelt sæt procedurer til årsafslutning. Det betyder, at du kan udforme organisationerne som driftsenheder. Alle driftsenheder skal bruge samme procedure til årsafslutningen.

### <a name="number-sequences"></a>Nummerserier

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Der kan oprettes nummerserier for nogle referencer pr. juridiske enhed. Nogle nummerserier kan deles.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Der kan oprettes nummerserier for nogle referencer pr. driftsenhed. Nogle nummerserier kan deles.

### <a name="products"></a>Produkter

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Produktdefinitioner er delte, og de skal frigives til individuelle juridiske enheder, før de kan føjes til transaktioner. Hver juridiske enhed har sit eget sæt frigivne produkter, der kan medtages i transaktionsdokumenter. Hvis dine interne organisationer skal bruge forskellige produktsæt, skal du udforme organisationerne som juridiske enheder.

> [!NOTE]
> Produktdefinitioner deles, men i hver juridiske enhed, hvor et produkt er blevet frigivet, kan du angive forskellige parametre for salg, køb og oplagring for varen på de enkelte lagersteder.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Alle driftsenheder deler samme produktsæt. Hvis dine interne organisationer kan dele det samme produktsæt, kan du udforme organisationerne som driftsenheder.

### <a name="inquiry-and-reporting"></a>Forespørgsel og rapportering

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisationen er udformet som en juridisk enhed

Du skal manuelt ændre virksomheder for at angive transaktioner og udføre forespørgsler i flere juridiske enheder. På grund af begrænsninger som følge af datasikkerhed kan konsolideret forespørgsel og rapportering være ressource- og tidskrævende.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisationen er udformet som en driftsenhed

Du behøver ikke at ændre virksomheder for at få adgang til data fra flere driftsenheder. Det er nemmere og hurtigere at udføre konsolideret forespørgsel og rapportering samt individuelle regionale forespørgsler.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Best practices for opstilling af modeller for organisationer og hierarkier

Overvej følgende bedste fremgangsmåder, når du implementerer et organisationshierarki:

- Opret en afdeling, som udgør modellen for skæringspunktet mellem en juridisk enhed og en virksomhedsenhed. Du kan derefter rulle data op fra en afdeling til en juridisk enhed for lovpligtig rapportering og fra en afdeling til en virksomhedsenhed for intern rapportering. Afdelinger kan bruges som driftscentre. Hvis du bruger afdelinger, behøver du ikke at bruge juridiske enheder og virksomhedsenheder som dimensioner i kontostrukturen. Du kan nøjes med at bruge afdelinger som en dimension. Du skal dog bruge både bærere og afdelinger som dimensioner i kontostrukturen, hvis bærere kun bruges til akkumulering af omkostninger, og afdelinger bruges til indtægtsføring.
- Modellér flere hierarkier for driftsenheder, hvis I har komplicerede behov for driftsrapportering.
- I en juridisk enhed skal du ikke udforme flere hierarkier til samme hierarkiformål.
- Opret ikke et hierarki til hvert formål. Du kan sædvanligvis bruge samme hierarki til flere formål. Samme hierarki over driftsenheder kan f.eks. tildeles alle politikrelaterede formål.
- Opret balancerede hierarkier. I et hierarki defineres alle noder, der har samme afstand til rodnoden, som et niveau. I et balanceret hierarki kan der kun forekomme én type driftsenhed på hvert niveau, og afstanden fra rodnoden til hvert niveau er den samme. Hvis der er mellemliggende niveauer mellem en afdeling og en juridisk enhed eller en virksomhedsenhed, kan det være nødvendigt at bruge pladsholderorganisationer, for at skabe et balanceret hierarki.
- Modellér ikke et separat hierarki af driftsenheder, hvis strukturen for juridiske enheder også er virksomhedens driftsstruktur. Et hierarki med en kombination af juridiske enheder og driftsenheder kan bruges til begge formål.
- Før du modellerer større omstruktureringsscenarier, skal du bruge hierarkiets ikrafttrædelsesdatoer til at udføre en effektanalyse og en valideringstest.
- Brug kladdetilstand til at ændre et hierarki, før du udgiver en ny version i et produktionsmiljø.
- Begræns antallet af personer, der har rettigheder til at tilføje eller fjerne organisationer fra et hierarki i et produktionsmiljø. Et lavere antal reducerer risikoen for, at der kan forekomme dyre fejl, der kræver, at der gennemføres rettelser.

