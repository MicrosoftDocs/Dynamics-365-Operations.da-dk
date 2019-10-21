---
title: Konfigurere lønintegration mellem Talent og Dayforce
description: Dette emne forklarer, hvordan du kan konfigurere integration mellem Microsoft Dynamics 365 Talent og Ceridian Dayforce, så du kan behandle en lønkørsel.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec1d14cb14ab709dfc1bead4be0785904efcce4e
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251033"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a>Konfigurere lønintegrationen mellem Talent og Dayforce

[!include [banner](includes/banner.md)]

Integration mellem Microsoft Dynamics 365 Talent og Ceridian Dayforce er baseret på flere konfigurationstrin, der er beskrevet i dette emne. Du skal konfigurere integrationen i både Talent og Dayforce, før du kan behandle en lønkørsel.

Når du bruger en tjeneste, f.eks. Dayforce, til at fuldføre lønkørsler, skal du aktivere integrationen i Talent. Integrationen kræver bestemte data fra Talent. Du skal derfor kontrollere, at data, der er knyttet til Dayforce, er konfigureret i Talent på en måde, der understøtter integrationen. Integrationen bruger følgende brede kategorier af data.

- Personaledata
- Kompensationsdata
- Lønoplysninger, f.eks. løncyklusser, betalingsperioder og lønkoder
- Arbejderdata

Dette emne beskrives de trin, du skal udføre for at aktivere integrationen. Det forklarer også typerne af data og oplysninger om konfigurationen, der kræves til integrationen.

## <a name="enable-the-integration"></a>Aktivere integrationen.

I Talent skal du aktivere integrationen og angive konfigurationsoplysningerne for at oprette forbindelse til Dayforce. Hvis den finanspostering, der er oprettet, skal importeres til Microsoft Dynamics 365 Finance, skal du også konfigurere en Microsoft Azure-lagerkonto og angive Azure-lagerets forbindelsesstreng i Finance.

Følg disse trin for at aktivere integrationen i Talent.

1. På siden **Systemadministration** skal du vælge **Integrationskonfiguration**.
2. Angiv det sikre FTP-slutpunkt og den sikre FTP-mappesti.
3. Angiv brugernavnet og adgangskoden for den bruger, der skal have adgang til det sikre FTP-slutpunkt og den sikre mappesti.
4. Test forbindelsen, som krævet, og angiv indstillingen **Aktivér lønintegration** til **Ja**.

Når integrationen er aktiveret, oprettes dataeksportpakken og -filerne, og hyppigheden angives. Du kan ændre denne frekvens efter behov.

Yderligere oplysninger om Azure-lagerkonti og Azure-lagerforbindelsesstrenge finder du i følgende Azure-emner:

- [Om Azure-lagerkonti](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Konfigurere forbindelsesstrenge for Azure-datalager](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a>Tekniske oplysninger ved aktivering af lønintegration

Aktivering af lønintegration har to primære effekter:

- Der oprettes et dataeksport projekt ved navn "Lønintegrationseksport". Dette projekt indeholder de objekter og felter, der kræves til lønintegration. Hvis du vil undersøge projektet, skal du gå til **Systemadministration**, vælge feltet **Datastyring** og derefter åbne dataprojektet på listen over projekter.
- Dette batchjob udfører dataeksportprojektet, krypterer den resulterende datapakke og overfører datapakkefilen til det SFTP-slutpunkt, der er konfigureret på skærmen **Integrationskonfiguration**.

> [!NOTE]
> Den datapakke, der overføres til SFTP-slutpunktet, krypteres ved hjælp af en nøgle, der er entydig for pakken. Nøglen er i en Azure Key Vault, der kun kan åbnes af Ceridian. Det er ikke muligt at dekryptere og undersøge datapakkens indhold. Hvis du har brug for at undersøge indholdet af datapakken, skal du eksportere dataprojektet "Lønintegrationseksport" manuelt, download det og derefter åbne det. Manuel eksport anvender ikke kryptering eller overførsel af pakken.

## <a name="configure-your-data"></a>Konfigurere dine data 

Hvis du vil behandle løn, skal du konfigurere personaledata i Talent. Du skal angive virksomhedens data, f.eks. job og stillinger, sammen med frynsegoder og kompensationsoplysninger. Disse oplysninger indeholder oplysningerne om ansættelse, løn og fradrag, der kræves for at generere løn for medarbejderen.

### <a name="human-resource-data"></a>Personaledata

#### <a name="benefits"></a>Frynsegoder 

Personale indeholder en række værktøjer til konfiguration og vedligeholdelse af frynsegoder, fradrag og arbejderkompensationsplaner, som en organisation tilbyder eller behandler for sine ansatte.

Når du opretter frynsegoder, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.

##### <a name="benefit-plans"></a>Frynsegodeplaner

- Plan (påkrævet)
- Type (påkrævet)
- Løneffekt (påkrævet)
- Opkræv restancer
- Fradragsmetode
- Prioriteret fradrag
- Grænseperiode
- Beløb for grænse

##### <a name="benefits"></a>Frynsegoder

- Plan (påkrævet)
- Type (påkrævet)
- Mulighed (påkrævet)
- Frynsegode-id (påkrævet)
- Frekvens
- Basis
- Beløb eller sats
- Lønkode

##### <a name="supported-frequencies"></a>Understøttede frekvenser 

- Ugentlig
- Pr. 14 dage
- To gange om måneden
- Månedlig

##### <a name="supported-bases"></a>Understøttede grundlag 

- Fast beløb
- Procentdel af løn
- Produktive timer

Dayforce opretter følgende fradrag, der er baseret på den løneffekt, der er defineret på frynsegodeplanen.

| Valg i Talent        | Resultat i Dayforce                            |
|----------------------------|-----------------------------------------------|
| None                       | Der oprettes ikke noget fradrag.                      |
| Kun fradrag             | Der oprettes et medarbejderfradrag.             |
| Kun bidrag          | Der oprettes et arbejdsgiverfradrag.             |
| Fradrag og bidrag | Der oprettes medarbejder- og arbejdsgiverfradrag. |

Du kan finde flere oplysninger om, hvordan du definerer og administrerer et frynsegodeprogram under følgende emner:

- [Levere et frynsegodeprogram for medarbejdere](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Oprette et nyt frynsegode](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Definere regler og politikker for frynsegodeberettigelse](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Tilmelde og fjerne frynsegoder fra arbejdere](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Kompensation 

Kompensationsstyring bruges til at styre fordelingen af grundløn og bonusser. En medarbejders faste grundløn og kvalifikationstillæg styres gennem faste lønstrukturer. Betalingen af incitamentsløn som f.eks. bonusudbetalinger, præstationsbonusser, aktieoptioner og tildelte aktier samt engangsbonusser styres ved hjælp af variable lønstrukturer.

Dayforce anvendes kompensationsoplysninger til at beregne en medarbejders timesats eller årlige sats. Konverteringer af planer for fast løn og lønsats er påkrævet. Medarbejderne skal være knyttet til en plan for fast løn.

Du kan finde flere oplysninger om kompensationsplaner under følgende emner:

- [Oprette faste kompensationsordninger](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Oprette planer for variabel kompensation](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Udarbejde løn-/kompensationsstruktur og -planer](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Proceskompensation](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [Definere kompensationsproces og beregne resultater](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Melde en medarbejder til en fast lønplan](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Melde en medarbejder til en variabel lønplan](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Job 

Et job er en samling af de opgaver og ansvarsområder, der kræves af en person, der udfører et job. Du kan finde flere oplysninger under følgende emner:

- [Konfiguration af komponenter i et job](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [Definere nye job](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Stillinger

En stilling er en individuel forekomst af et job. For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef". En stilling findes i en afdeling. Der kan kun knyttes én arbejder til hver stilling.

Hav følgende data og konfiguration i tankerne, når du konfigurerer stillinger:

- Stilling (påkrævet)
- Beskrivelse (påkrævet)
- Job (påkrævet)
- Afdeling (påkrævet)
- Stillingstype (påkrævet)
- Fuldtidsækvivalent
- Normaltimer på årsbasis (påkrævet)
- Betalt af juridiske enhed (påkrævet)
- Betalingscyklus (påkrævet)
- Økonomisk standarddimension – bærer (påkrævet)
- Arbejdertildeling – arbejder, tildelingsstart, tildelingsslut, årsagskode

Hvis flere stillinger i den samme afdeling er knyttet til samme job, konsolideres de til en enkelt stilling i Dayforce.

Du kan finde flere oplysninger under følgende emner:

- [Organisere dine medarbejdere ved hjælp af afdelinger, jobs og stillinger](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Konfigurere stillinger](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Afdelinger

En afdeling er en driftsenhed, der repræsenterer en kategori eller et funktionsområde i en organisation. En afdeling er ansvarlig for et bestemt område i organisationen, såsom salg, regnskab eller personale. Du kan bruge afdelinger til at rapportere om funktionsområder. Afdelinger kan have ansvar for driftsregnskabet.

Du kan finde flere oplysninger under følgende emner:

- [Oprette en afdeling og knytte den til afdelingshierarkiet](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Definere nye afdelinger](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Betalingscyklusser og lønperioder

En betalingscyklus bestemmer, hvor ofte løn køres,og de specifikke dage, hvor arbejdere betales. En løncyklus kan f.eks. være månedlig, og medarbejdere betales måske på den sidste dag i måneden. En løncyklus kan også være ugentligt, og medarbejdere betales måske tirsdag efter slutningen af lønperioden. Løncyklusser tildeles til stillinger for at styre, hvornår arbejdere i disse stillinger bliver betalt.

Når du opretter betalingscyklusser, kan du generere lønperioder for hver cyklus. Hver lønperiode omfatter en standardbetalingsdato, der er baseret på oplysninger, du angiver. Du kan dog redigere standardbetalingsdatoen i en lønperiode til at tillade undtagelser, f.eks. når betalingsdatoen falder på en helligdag.

Følgende oplysninger bruges i Dayforce:

- Betalingscyklus (påkrævet)
- Hyppighed for betalingscyklus (påkrævet)
- Periodens startdato (første lønperiode påkrævet)
- Standardbetalingsdato (første lønperiode påkrævet)

Oplysningerne er integreret med Dayforce som løngrupper og adskilles af et land eller område for hver løncyklus. Mindst én periode skal genereres før integration. Dayforce genererer løngruppekalendere og betalingsdatoer, der er baseret på startdatoen for den første lønperiode og den standardbetalingsdato, der er angivet i Talent.

#### <a name="earning-codes"></a>Lønkoder

Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager. Koderne har forskellige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab.

Følgende oplysninger bruges i Dayforce:

- Lønkode (påkrævet)
- Betegnelse
- Måleenhed
- Produktiv

### <a name="worker-data"></a>Arbejderdata

Posterne for de forskellige typer arbejdere, du beskæftiger, er vigtige for dine personale- og lønsystemer. De oplysninger, du angiver, kan bruges til at spore arbejdere og personoplysninger.

Du kan vedligeholde følgende oplysninger for arbejdere:

- **Basis** – Vedligehold grundlæggende oplysninger om en arbejder, f.eks. kontaktoplysninger, demografiske oplysninger, identifikationsoplysninger, oplysninger om familie, status for militærtjeneste, oplysninger om udstationering og personlige kontaktpersoner og kontaktpersoner i nødsituationer.
- **Beskæftigelse** – Vedligehold oplysninger om en arbejders beskæftigelse, f.eks. firma- eller organisationstilhørsforhold, stillingstildeling, start- og slutdatoer, arbejdstilladelse, vilkår for ansættelse, pension, ferie og flytteoplysninger.
- **Orlov og fravær** – Vedligehold oplysninger om en arbejders fravær, f.eks. arbejdskalendere, fraværstransaktioner og fraværsopsætning.
- **Kompensation og løn** – Vedligehold oplysninger om en arbejders kompensationsplaner og lønoplysninger, f.eks. tilmelding til planer, priser, ydeevne, provision, skatteoplysninger, pensionering og skattefradrag.

Når du angiver arbejderoplysninger, skal du huske på følgende data og konfigurationer, der bruges i Dayforce.

#### <a name="general-information"></a>Generelle oplysninger

- Personalenummer (påkrævet)
- Fornavn (påkrævet)
- Efternavn (påkrævet)
- Mellemnavn
- Anciennitetsdato
- Kendt som

#### <a name="personal-information"></a>Personlige oplysninger

- Ægteskabelig status (påkrævet)
- Fødselsdato (påkrævet)
- Køn (påkrævet)
- Handicappet
- Land eller område for nationalitet (kun for Mexico)

#### <a name="address-information"></a>Adresseoplysninger

- Primær (påkrævet)
- Land/område (påkrævet)
- Postnummer (påkrævet)
- Gadenummer (påkrævet) (kun for Mexico)
- Bygningskomplement (kun for Mexico)
- By (påkrævet)
- Stat (påkrævet)
- Region (påkrævet)

#### <a name="contact-information"></a>Kontaktoplysninger 

- Primær (påkrævet)
- Kontaktpersonens nummer (påkrævet)
- Forlængelse

#### <a name="payroll-information-and-earning-codes"></a>Lønoplysninger og lønkoder

Medarbejdere kan tildeles en bestemt løn med en given betalingshyppighed og have en foretrukken betalingsmetode. Følgende felter bruges i Dayforce til at sikre, at disse præferencer og indstillinger bruges.

##### <a name="earning-codes"></a>Lønkoder

- Stilling (påkrævet)
- Lønkode (påkrævet)
- Frekvens (påkrævet)
- Beløb (påkrævet)

##### <a name="payroll-information"></a>Lønoplysninger

- Betalingsmetode
- Økonomisk område (påkrævet)
- Id for medarbejderfrynsegoder
- Nationalt id-nummer (påkrævet)
- Tjenestenummer hos militær
- Skifte-id (påkrævet)
- Skattenummer (påkrævet)
- Fagforenings-id (påkrævet)
- Arbejdsdags-id (påkrævet)
- Arbejdstilladelsesnummer

> [!NOTE]
> For betalingsmetoden understøtter Mexico **Kontant**, **Check** (firmaets fysiske check), og **Elektronisk betaling**. Hvis der ikke er angivet nogen betalingsmetode, bruges **Check** som standard.

#### <a name="employment-details"></a>Detaljer om ansættelse

Detaljeret ansættelseshistorik bruges som vigtige oplysninger til at udlede statusser for en medarbejders ansættelse, fratrædelse og genansættelse i Dayforce. Dayforce understøtter kun én aktiv ansættelsespost ad gangen.

- Startdato for ansættelse (påkrævet)
- Slutdato for ansættelse
- Igangsæt dato
- Justeret startdato
- Fratrædelsesdato (kræves ved fratrædelse)
- Fratrædelsesårsag (kræves ved fratrædelse)

Vigtige datoer for en medarbejders udledes ved hjælp af følgende oplysninger.

| Talent                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Den seneste ansættelsesdato | Historikpost for ansættelsesstart for aktuel ikke-afsluttet ansættelse                                 |
| Fratrædelsesdato      | Historikpost for fratrædelsesdato for aktuel ikke-afsluttet ansættelse                                 |
| Igangsæt dato            | Historikpost for justeret startdato, startdato eller startdato for ansættelse for aktuel ikke-aktiv ansættelse |
| Oprindelig ansættelsesdato    | Historikpost for ansættelsesstart for tidligste ansættelse                                               |

#### <a name="compensation"></a>Kompensation

En fast lønstruktur skal tilknyttes hver medarbejders primære stilling gennem hele ansættelsesperioden. Denne periode starter på den dato, hvor medarbejderen blev ansat (eller ansættelsesstartdatoen) og fortsætter, indtil fratrædelsen.

- Ikrafttrædelsesdato (påkrævet)
- Udløbsdato
- Lønsats (påkrævet)
- Konverteringer af lønsats (påkrævet)
- Årlig ækvivalent (påkrævet)
- Timebaseret ækvivalent (påkrævet)

Hvis en timeansat medarbejder har flere stillinger, indlæses den faste løn for den primære stilling i Dayforce, som basissats/-løn på medarbejderniveau. For ikke-primære stillinger gemmes timesatsen i den tilsvarende position i Dayforce.

Hvis en funktionær har flere stillinger, afledes den kumulative timesats og årlig gage på tværs af alle aktive stillinger og bruges som basissats/-gage på medarbejderniveau.

#### <a name="identification-numbers"></a>Identifikationsnumre

##### <a name="social-security-identifier"></a>Social Security-identifikator 

Alle medarbejdere skal have én primær identifikator. Identifikatoren skal være af **SSN**-identifikationstypen I Dayforce afledes den automatisk som medarbejderens Social Security-identifikator, der er påkrævet ved ansættelse.

- Primær (påkrævet)
- Identifikationstype = "SSN"
- Udstedt den
- Udløbsdato

Medarbejdere kan angive flere identifikationsnumre af **SSN**-identifikationstypen. Men det er kun den post, der er markeret som **Primær**, som er integreret i Dayforce, uanset om nummeret er aktivt eller udløbet.

#### <a name="bank-accounts-and-disbursements"></a>Bankkonto og udbetalinger

Gyldige bankkontooplysninger skal angives for enhver medarbejder, der vælger at blive betalt via bankkontooverførsler.

| Talent                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Bankkontonummer (påkrævet) |                                                                                                             |
| SWIFT-kode (påkrævet)          | Feltet **Bank-id** bruges ved behandling af løn i Mexico.                                                             |
| Afdelingsnummer (påkrævet)       |                                                                                                             |
| Bankkontotype (påkrævet)   | Feltet **Kontotype** bruges ved behandling af løn i Mexico. Understøttede værdier omfatter **Check** og **Løn**. |

> [!NOTE]
> Medarbejdere, der vælger at betales via bankkontooverførsler, skal angive et link til en restbeløbskonto, der hører under en juridisk enhed, som har primær adresse i Mexico og er knyttet til en gyldig bankkonto fra en mexicansk bank. Alle andre restbeløbskonti ignoreres.

#### <a name="address-information"></a>Adresseoplysninger

Alle medarbejdere skal have én primær placering. I Dayforce bruges denne placering til at bestemme medarbejderens primære opholdssted til skattemæssige formål.

- Primær (påkrævet)
- Land/område (påkrævet)
- Postnummer (påkrævet)
- Gade (påkrævet)
- Gadenummer (påkrævet)
- Bygningskomplement
- By (påkrævet)
- Stat (påkrævet)
- Region (påkrævet)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Konfigurere dataene for at generere løn i USA og Canada

Hvis du genererer løn for medarbejdere i USA og Canada, skal følgende elementer konfigureres:

- Der kræves afdelinger til stillinger.
- Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.

> [!NOTE] 
> Du kan konfigurere Talent til at kræve, at der angives en afdeling for stillinger. For at gøre dette skal du gå til **Personalets delte stillinger > Stillinger > Kræv afdelinger for stillinger**. Det anbefales, at denne indstilling gennemtvinges i forbindelse med integrationen.

### <a name="job-types"></a>Jobtyper

Jobtyper bruges til at gruppere lignende job i kategorier. Jobtyper kræves for at behandle løn i USA og Canada. Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede. Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.

Der kræves følgende jobtyper og beskrivelser.

| Jobtype   | Betegnelse |
|------------|-------------|
| Pr. time     | Pr. time      |
| Funktionærløn   | Funktionærløn    |

### <a name="position-types"></a>Stillingstyper 

Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet. Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.

Der kræves følgende stillingstyper og beskrivelser.

| Stillingstype   | Betegnelse        |
|-----------------|--------------------|
| Fuld tid       | Fuldtidsmedarbejder |
| Deltid       | Deltidsmedarbejder |

### <a name="reason-codes"></a>Årsagskoder

Årsagskoder indeholder oplysninger om status for en medarbejder. Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.

Der kræves følgende årsagskoder og beskrivelser.

| Årsagskode    | Betegnelse      | Anvendelige scenarier |
|----------------|------------------|----------------------|
| OPSIGELSE    | Opsigelse      | Lad arbejder fratræde     |
| OPHØR    | Ophør      | Lad arbejder fratræde     |
| PENSION     | Pension       | Lad arbejder fratræde     |
| ANDET          | Andre årsager    | Lad arbejder fratræde     |
| DØDSFALD          | Dødsfald            | Lad arbejder fratræde     |
| LEAVEOFABSENCE | Orlov | Lad arbejder fratræde     |
| CONTRACTEND    | Kontraktudløb  | Lad arbejder fratræde     |
| SALARYCHANGE   | Ændring af løn | Kompensation         |

### <a name="marital-status"></a>Ægteskabelig status

Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.

Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.

| Talent                 | Dayforce             |
|------------------------|----------------------|
| Gift                | Gift              |
| Enlig                 | Enlig               |
| Enke/enkemand                | Enke/enkemand              |
| Fraskilt               | Fraskilt             |
| Registreret partnerskab | Registreret partnerskab |
| None                   | None                 |
| Samlever             | Samlever           |

### <a name="gender"></a>Køn

Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.

Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.

| Talent       | Dayforce        |
|--------------|-----------------|
| Mand         | Mand            |
| Kvinde       | Kvinde          |
| Ikke-specifik | *Understøttes ikke* |

### <a name="earning-codes"></a>Lønkoder

Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager. Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab. Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.

#### <a name="supported-frequencies"></a>Understøttede frekvenser

- Alt
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adresser

Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende. Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.

| Talent          | Dayforce              |
|-----------------|-----------------------|
| Land/område  | Landekode          |
| Postnummer | Postnummer           |
| Status           | Statskode            |
| Bynavn            | Bynavn                  |
| Region          | Område (kommune) |
| Gade          | Adresselinje 1        |

### <a name="tax-regions"></a>Skatteområder

Skatteområder bruges til at bestemme den relevante skat, der skal anvendes ved løngenerering. Skatteområder er tilknyttet Dayforce som placeringsadresser. Standardskatteområder skal knyttes til arbejderens aktive stilling. 

- Skatteområde (påkrævet)
- Land/område (påkrævet)
- Stat (påkrævet)
- Region 
- By (påkrævet)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Konfigurere dataene for at generere løn i Mexico

Hvis du genererer løn for medarbejdere i Mexico skal følgende elementer konfigureres:

- Der kræves afdelinger til stillinger.
- Bærere skal angives som økonomiske dimensioner og skal være det første element i standardstrengen for økonomisk dimension.

### <a name="job-types"></a>Jobtyper

Jobtyper bruges til at gruppere lignende job i kategorier. Jobtyper kræves for at behandle løn i Mexico. Eksempler på jobtyper omfatter fuldtids og deltids eller fastlønnede og timelønnede. Jobtyper knyttes til Dayforce som lønarter, der angiver, om en medarbejder er hver timelønnet eller fastansat.

Der kræves følgende jobtyper og beskrivelser.

| Jobtype   | Betegnelse |
|------------|-------------|
| Pr. time     | MX Pr. time   |
| Funktionærløn   | MX Funktionærløn |

### <a name="position-types"></a>Stillingstyper 

Du bruge stillingstyper til at beskrive, om stillingen er fuld tid, deltid eller noget andet. Stillingstyper knyttes til Dayforce som lønklasser, der angiver, om en medarbejder er på fuld tid eller deltid.

Der kræves følgende stillingstyper og beskrivelser.

| Stillingstype   | Betegnelse        |
|-----------------|--------------------|
| Fuld tid       | Fuldtidsmedarbejder |
| Deltid       | Deltidsmedarbejder |

### <a name="reason-codes"></a>Årsagskoder

Årsagskoder indeholder oplysninger om status for en medarbejder. Årsagskoder er tilknyttet Dayforce som statusårsager, der angiver årsagen til ændringer af status for en medarbejders stilling eller ansættelsesstatus.

Der kræves følgende årsagskoder og beskrivelser.

| Årsagskode            | Betegnelse                    | Anvendelige scenarier |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | Afgang før første løn | Lad arbejder fratræde     |
| OPSIGELSE            | Opsigelse                    | Lad arbejder fratræde     |
| PENSION                | Pension                        | Lad arbejder fratræde     |
| OPHØR            | Ophør                    | Lad arbejder fratræde     |
| PENSION             | Pension                     | Lad arbejder fratræde     |
| FRAVÆRENDE               | Fraværende                       | Lad arbejder fratræde     |
| ANDET                  | Andre årsager                  | Lad arbejder fratræde     |
| LUKNING                | Virksomhedslukning               | Lad arbejder fratræde     |
| DØDSFALD                  | Dødsfald                          | Lad arbejder fratræde     |
| LEAVEOFABSENCE         | Orlov               | Lad arbejder fratræde     |
| CONTRACTEND            | Kontraktudløb                | Lad arbejder fratræde     |
| SALARYCHANGE           | Ændring af løn               | Kompensation         |

### <a name="terms-of-employment"></a>Ansættelsesvilkår

Ansættelsesvilkår bruges til at oprette kategorier for ansættelsesvilkår. Vilkårene knyttes til Dayforce som beskæftigelsesindikatorværdier.

Følgende begreber for beskæftigelse og beskrivelser er påkrævet.

| Ansættelsesvilkår   | Betegnelse |
|-----------------------|-------------|
| Regulær               | Regulær     |
| Direkte                | Direkte      |
| Turnustjeneste            | Turnustjeneste  |
| Permanent             | Permanent   |

### <a name="marital-status"></a>Ægteskabelig status

Ægteskabelige statusværdier knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.

Følgende tabel viser, hvordan ægteskabelige statusværdier knyttes til Dayforce.

| Talent                 | Dayforce                  |
|------------------------|---------------------------|
| Gift                | Gift                   |
| Enlig                 | Enlig                    |
| Enke/enkemand                | Enke/enkemand                   |
| Fraskilt               | Fraskilt                  |
| Registreret partnerskab | Registreret partnerskab      |
| None                   | *Understøttes ikke af Mexico* |
| Samlever             | *Understøttes ikke af Mexico* |

### <a name="gender"></a>Køn

Kønsbetegnelse knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.

Følgende tabel viser, hvordan kønsbetegnelser knyttes til Dayforce.

| Talent       | Dayforce                  |
|--------------|---------------------------|
| Mand         | Mand                      |
| Kvinde       | Kvinde                    |
| Ikke-specifik | *Understøttes ikke af Mexico* |

### <a name="payment-method"></a>Betalingsmetode

Betalingsmetoder giver medarbejderen og virksomheden en måde til at beskrive, hvordan medarbejdere skal betales. Betalingsmåder knyttes til Dayforce og oversættes efter behov til de accepterede værdier ved integration.

Følgende tabel viser, hvordan betalingsmetoder knyttes til Dayforce.

| Talent             | Dayforce                  |
|--------------------|---------------------------|
| Indløsning               | Indløsning                      |
| Elektronisk betaling | Ompostering                  |
| Check              | Check                    |
| Bankanvisning         | *Understøttes ikke af Mexico* |
| Andre              | *Understøttes ikke af Mexico* |

### <a name="bank-account-type"></a>Bankkontotype

Bankkontotyper bruges til elektroniske betalinger til medarbejdere. Bankkontotyper knyttes til Dayforce som overførselskontooplysninger. Bankkontotyperne oversættes efter behov til de accepterede værdier ved integration.

| Talent            | Dayforce                  |
|-------------------|---------------------------|
| Checkkonto  | CheckingAccount           |
| Lønkonto   | PayrollAccount            |
| Opsparingskonto   | *Understøttes ikke af Mexico* |
| BankGirot-konto | *Understøttes ikke af Mexico* |
| PlusGirot-konto | *Understøttes ikke af Mexico* |

### <a name="earning-codes"></a>Lønkoder

Lønkoder identificerer entydigt alle typer af løn, som arbejderne modtager. Koderne dækker adskillige parametre, der vedrører løn, f.eks. konteringsregler, skattelovgivning, rapporteringskrav og bruttoficeringsegenskab. Hvis der bruges en ikke-understøttet frekvens, bruges frekvensen **Hver betaling** som standard for beregningen.

#### <a name="supported-frequencies"></a>Understøttede frekvenser

- Alt
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adresser

Identifikation af specifikke koder for land eller region, stat og område (kommune) kræver specifikke formater, som Dayforce og udbydere af i landet/ i regionen kan genkende. Selvom formatet for byer er fleksibelt, skal hver by være tilknyttet en tilstand.

| Talent              | Dayforce              |
|---------------------|-----------------------|
| Land/område      | Landekode          |
| Postnummer     | Postnummer           |
| Status               | Statskode            |
| Bynavn                | Bynavn                  |
| Region              | Område (kommune) |
| Gade              | Adresselinje 1        |
| Gadenummer       | Adresselinje 2        |
| Bygningskomplement | Adresselinje 5        |

### <a name="passport-number"></a>Pasnummer

Medarbejdere kan erklære pasoplysninger. Disse oplysninger er af identifikationstypen **Pas** og er integreret i Dayforce som en del af en medarbejders Mexico-specifikke oplysninger.

- Identifikationstype = "Pas"
- Udstedt den
- Udløbsdato

Medarbejdere kan angive flere identifikationsnumre af **Pas**-identifikationstypen. Men det er kun den aktuelle aktive paspost, der integreres i Dayforce. Hvis alle pasposter er udløbet, integreres det pas, der senest blev udstedt, i Dayforce.
