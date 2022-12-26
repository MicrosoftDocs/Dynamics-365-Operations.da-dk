---
title: Proaktive kvalitetsopdateringer
description: Denne artikel indeholder oplysninger om proaktiv levering af kvalitetsopdateringer.
author: rashmansur
ms.date: 11/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7d8de017c54a13a9935d74d33a57813922c9f823
ms.sourcegitcommit: 8aee31d6dffabe13969dd5b9de4e0bf95f53e67e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887124"
---
# <a name="proactive-quality-updates"></a>Proaktive kvalitetsopdateringer

[!include[banner](../includes/banner.md)]

I løbet af de seneste flere år har Microsoft gjort fortløbende, hvad vi kalder [Én version](../../dev-itpro/lifecycle-services/oneversion-overview.md). Udgangspunktet for én version er simpel: Jo tættere på vi kan være på at have alle kunder på samme softwareversion, jo højere kvalitet kan vi levere. Vi finder og løser problemer én gang, og vi gør disse løsninger hurtigere til kundernes behov.

Denne forudsætning er bekræftet af resultaterne: lavere hændelser tæller på tværs af vores produkter. Når kunder ikke findes på samme version, ser vi konsistent, at de er påvirket af problemer, som en løsning allerede er tilgængelig for. Vi har allerede gjort store fremskridt med Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations og Dynamics 365 Commerce – og takket være de seneste tekniske fremskridt – er det nu muligt at tage næste trin. Følgende oplysninger viser, hvad vi vil gøre, hvad vi allerede har gjort for at sætte stadiet, og hvordan og hvornår vi vil introducere de nye egenskaber uden problemer.

## <a name="what-you-need-to-know"></a>Hvad du skal vide

- Proaktive kvalitetsopdateringer (PQU) anvendes på månedlig basis.
- Undtagelser til proaktive kvalitetsopdateringer er tilladt for kunder, der reguleres af de amerikanske fødevaremyndigheder FDA (Food and Drug Administration).
- Proaktive kvalitetsopdateringer vil aldrig nedgradere miljøet eller automatisk opgradere fra én serviceopdateringsversion til en anden. 
- Microsoft bestemmer, hvordan proaktive kvalitetsopdateringer skal administreres for regulerede miljøer og for selvstændige og myndigheders kunder i skyer.
- Beskeder, der vedrører proaktive kvalitetsopdateringer, bogføres i [Microsoft 365-meddelelsescenteret](https://admin.microsoft.com/AdminPortal/).
- Fem dage før en proaktiv kvalitetsopdatering anvendes på et miljø, får kunderne besked om, at opdateringen finder sted.
- Kunder kan ikke annullere eller udskyde proaktive kvalitetsopdateringer.
- Proaktive kvalitetsopdateringer installeres i det områdespecifikke [vindue til planlagt vedligeholdelse](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
- Kvalitetsopdateringer er udviklet til at have lav risiko for at skabe problemer eller tilbageskridt, og dette understøttes af Microsoft-data.
- Microsoft anbefaler målrettet test af bestemte problemer eller bestemte hotfixes, der er relateret til en proaktiv kvalitetsopdatering.
- ALLE sandkasser, med undtagelse af dem, der har en tidsbegrænset undtagelse af lovmæssige årsager, vil blive klarmeldt 7. januar 2023.
- Start af produktions- og proaktive kvalitetsopdateringer fra 21. januar 2023. 
- Modtagelse af produktion starter kun for Lifecycle Services-projekter, hvor der er startet sandkasse(r) og indtil videre modtager proaktive kvalitetsopdateringer med regelmæssig cadence for alle understøttede serviceopdateringsversioner. Dette gælder kun kundemiljøer, hvor der ikke er angivet undtagelser af lovmæssige eller andre juridiske årsager.
- Se herunder for at få en komplet plan over proaktive kvalitetsopdateringer til sandkasse- og produktionsmiljøer i løbet af 2023.
- Hver serviceopdatering har mindst ét løbende eller igangværende PQU-tog, der skal startes. Når dine miljøer er klar til PQU-processen, modtager du muligvis en forudplanlagt proaktiv kvalitetsopdatering af dem alle, når du går til en ny version af serviceopdateringen. Kontroller planen for at fastlægge, hvornår en PQU for en serviceopdatering planlægges, hvis du planlægger opgradering til en nyere version af serviceopdateringen. 

> [!Note]
> Standardpræstationstest (tier4), test af premium-performance (tier5) og produktionsmiljøer vil modtage PQU'er i weekender. 

## <a name="focus-on-quality-updates"></a>Fokus på kvalitetsopdateringer

Vi leverer i øjeblikket syv [serviceopdateringer](public-preview-releases.md) pr. år. Version 10.0.29 er f.eks. en serviceopdatering. Indtil for nylig var der otte opdateringer pr. år. Men vi har afbrudt én opdatering som svar på kundefeedback, der ønsker at undgå ændringer i slutningen af kalenderåret.

Vi ændrer ikke cadencen for serviceopdateringerne. I stedet er næste trin fremad i versionen fokuseret på *kvalitetsopdateringer*. Kvalitetsopdateringer er akkumulerede builds af hotfixes. De inkluderer ikke nye funktioner. På et givet tidspunkt spredes hele gruppen af kunder mellem de tre eller fire seneste serviceopdateringer. Ved en given serviceopdatering kan versioner af forskellige kvalitetsopdateringsversioner dog bruges i gruppen, afhængigt af de datoer, hvor personerne blev implementeret. I næste trin udsender vi proaktivt kvalitetsopdateringer. Vi bruger allerede denne model til vores Dataverse-baserede programmer og har set de forventede resultater af forbedret kvalitet og reduceret supporthændelser.

En reduktion af defekter kan naturligvis reducere eller eliminere behovet for kvalitetsopdateringer. Vi har flere initiativ i fly for at reducere de defekter, der kræver kvalitetsopdateringer. Selv når nyttelast reduceres i kvalitetsopdateringen, vil konsistens på tværs af kundebasen forbedre understøttelsen, hurtigere få forbedringer til kunderne og reducere antallet af kunder, der i forvejen oplever problemer, der allerede findes løsninger for.

## <a name="making-proactive-distribution-possible"></a>Gøre proaktiv distribution mulig

Der er allerede implementeret flere forskud, som giver mulighed for proaktiv levering af kvalitetsopdateringer:

- **Opdatering af nedetid ved nul** – Hvis du vil køre mere hyppige miljøer, er det vigtigt, at tilgængeligheden af ressourcer i miljøet reduceres, så Dynamics 365 Service Level Agreements bevares. Der blev oprindeligt introduceret opdatering af Ved nul-nedetid for at forbedre den månedlige programrettelse af operativsystemet ved hjælp af en cluster failover for at aktivere det opdaterede billede med minimale afbrydelser. Mekanismen til anvendelse af opdateringer bliver udvidet, så den er endnu mindre afbrydende, og den dækker både programrettelse af operativsystemet og implementering af kvalitetsopdatering.

    For interaktive brugere kan en aktiv session blive afbrudt, og forsøge at fortsætte til det nu opdaterede miljø. Med introduktionen af [prioriteret batchplanlægning](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) vil batchplanlægning og batchafvikling blive genoprettet og genoptaget umiddelbart efter opdateringen. Der findes prioriteret batchplanlægning for kunderne, før de begynder at deltage i proaktiv distribution af kvalitetsopdateringer til deres produktionsmiljøer.

- **Mørke timer** – Der er defineret mørke timer for hver Azure-region, og der vil forekomme næsten nul-nedetidsopdateringer i løbet af perioden med mørke timer.

## <a name="the-proactive-update-process"></a>Den proaktive opdateringsproces

Implementering af proaktive kvalitetsopdateringer vil følge en sikker implementeringsproces (SDP). SDP'ens specifikke oplysninger udvikler sig, men kvalitetsopdateringer vil først blive implementeret i sandboksmiljøer. Efterhånden som procentdelen af installerede sandbokse stiger, vil implementering i produktionsmiljøer begynde. Lyttesystemer vil overvåge system telemetry og Livesite-hændelser og stopper rollout af en bestemt version, hvis der registreres regression. Kunderne vil stadig kunne trække kvalitetsopdateringerne før proaktiv implementering, hvis det er nødvendigt.

De aktuelle data for frigivelsesstyring viser, at mindre end 3 procent af generne introduceres i kvalitetsopdateringer. Med øget fokus på eliminering af genstigning og et udvidet SDP vil den potentielle virkning af genvurdering være betydeligt lavere end den kvalitetsvind, der opnås, hvis de bliver implementeret overordnet på kunderne.

## <a name="process-changes"></a>Behandl ændringer

Der implementeres et sæt procesændringer før aktiveringen af proaktiv implementering af kvalitetsopdatering:

- **Skema** – Værktøj sikrer, at kvalitetsopdaterings builds kun omfatter skemaændringer, der kan anvendes, mens tjenesten er online. Denne indfaldsvinkel hjælper med at bevare muligheden for at anvende opdateringen med nedetid tæt på nul.
- **Udvidet antal ændringer** - Aktuelt er der allerede et ekstra procestrin til godkendelse af ændringer, så de medtages i en kvalitetsopdatering. Den trinvise reduktion i det ekstra trin øges for at reducere regressionsmulighederne. Det er ikke tilladt at ændre noget i kvalitetsopdateringerne, og den øgede ændring er med til at sikre, at vi opfylder dette mål.
- **Synlighed** – Der sendes beskeder via Administration, Lifecycle Services (LCS) og andre tilgængelige kanaler om kommende proaktive kvalitetsopdateringer. Desuden vil supportteams og hændelsesemner have synlighed for, hvor kvalitetsopdateringer er blevet implementeret proaktivt.

    > [!NOTE]
    > Microsoft Communications-teamet undersøger løbende forringet ydeevne af mailværktøjet, der forhindrer levering af mailbeskeder. Fortsæt med at overvåge Microsoft 365 Meddelelsescenter for onboarding- og beskedrelaterede meddelelser.

- **Fejlsikret via flighting** – Flighting bruges til ændringer af beskyttelseskode, hvor det er relevant i en kvalitetsopdateringsrettelse eller ved hjælp af den eksisterende funktions-flighting, der er relevant for rettelsen. Hvis der kræves en reserve eller et deaktiveret skift efter en proaktiv installation, kan den udføres via flighting-systemet for at undgå yderligere fejl.
- **Synkroniseringsangivelse for sandkasse** – Den fortløbende opdatering til en isoleret sandkasse, der er valgt sammen med produktionen, understøttes ikke på dette tidspunkt. Alle trin 2- og trin 3-sandkasser modtager proaktive opdateringer mindst 7 dage før produktionsmiljøet i et Lifecycle Services-projekt. Igen gælder dette kun kundemiljøer, hvor der ikke er angivet undtagelser af lovmæssige eller andre juridiske årsager.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Hvad er rullelisten for kvalitetsopdateringer?

Distributionen af proaktive kvalitetsopdateringer til sandkasse-miljøer begyndte i september 2022 for Azure-kunder i skyen. Senest den 1. januar 2023 afslutter vi 99 % af alle sandkasser for proaktive kvalitetsopdateringer.

Der tillades kun undtagelser til den proaktive opdaterede distributionsproces for FDA-regulerede kunder. Vi arbejder stadig med, hvordan regulerede miljøer og regulerede og offentlige skykunder skal håndteres. 

Da kunderne jævnligt modtager mindre nyttelast, forventer vi, at processen med aktuelle arbejde bliver simplere. Vi vil justere frekvensen for opdateringsinstallation, efterhånden som vi viser, hvordan vi kan køre processen uden afbrydelser. Denne proces fungerer allerede effektivt for vores Dataverse-platform og programmer og leverer de forventede forbedringer af servicekvaliteten. Vi gør det samme i forbindelse med finans- og driftsprogrammer.


## <a name="when-will-quality-updates-start-for-production-environments"></a>Hvornår starter kvalitetsopdateringerne for produktionsmiljøer?
I løbet af de første få måneder af 2023 med start 15. januar starter vi med at starte produktionsmiljøer for proaktive opdateringer og øge procentdelen af produktionsmiljøer, der modtager proaktive opdateringer. Vi vil kun mål for et produktionsmiljø i et Lifecycle Services-projekt, hvor der allerede er modtaget sandkassemiljøer, for at modtage proaktive opdateringer. Inden en opdatering får kunder med produktionsmiljøer, der er under start, besked via meddelelsescenter eller Lifecycle Services-banner. Se herunder for at få en komplet plan over proaktive kvalitetsopdateringer til sandkasse- og produktionsmiljøer i løbet af 2023.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Hvad er planlægningen for proaktive sandkassekvalitetsopdateringer?
Du kan finde oplysninger om de mørke timer for hver region i [Hvad er de planlagte vedligeholdelsesvinduer efter region?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a> Proaktiv udgivelses af kvalitetsopdatering: 10.0.29
**App version: 10.0.1326.70**  
**Tilsvarende seneste KB-artikel: 750332**

| Station | Områder | Fuldført tidsplan | Kommende sandkasseplan|
|---|---|---|---|
| Station 1 | Det centrale Canada, det østlige Canada, det centrale Frankrig, det centrale Indien, det østlige Norge, det vestlige Schweiz | 14. oktober til 17. oktober 2022, 2. november til 5. november 2022, 13. november til 16. november 2022, 5. december til 8. december 2022 | 2. januar til 5. januar 2023 |
| Station 2 | Det sydlige Frankrig, det sydlige Indien, det vestlige Norge, det nordlige Schweiz, det nordlige Sydafrika, det østlige Australien, det sydlige Storbritannien, de nordlige Forenede Arabiske Emirater, det østlige Japan, det sydøstlige Australien, det sydøstlige Asien | 15. oktober til 18. oktober 2022, 2. november til 5. november 2022, 13. november til 16. november 2022, 5. december til 8. december 2022 | 2. januar til 5. januar 2023 |
| Station 3 | Østasien, det vestlige Storbritannien, det vestlige Japan, det sydlige Brasilien, det vestlige Europa, det østlige USA, de centrale Forenede Arabiske Emirater | 16. oktober til 19. oktober 2022, 2. november til 5. november 2022, 13. november til 16. november 2022, 5. december til 8. december 2022 | 2. januar til 5. januar 2023 |
| Station 4 | Nordeuropa, det centrale USA, det vestlige USA | 17. oktober til 20. oktober 2022, 2. november til 5. november 2022, 15. november til 18. november 2022, 5. december til 8. december 2022 | 2. januar til 5. januar 2023 |
| Station 5 | DoD, Government Community Cloud (GCC), Kina | Ikke planlagt | Ikke planlagt |

### <a name="proactive-quality-update-release-10030"></a><a name="schedule"></a> Proaktiv udgivelses af kvalitetsopdatering: 10.0.30
**App-version: 10.0.1362.77**
**Tilsvarende seneste KB-artikel: 767597**

| Station | Områder | Fuldført tidsplan | Kommende sandkasseplan |
|---|---|---|---|
| Station 1 | Det centrale Canada, det østlige Canada, det centrale Frankrig, det centrale Indien, det østlige Norge, det vestlige Schweiz | 1. december til 4. december 2022 |  13. december til 16. december 2022 | 
| Station 2 | Det sydlige Frankrig, det sydlige Indien, det vestlige Norge, det nordlige Schweiz, det nordlige Sydafrika, det østlige Australien, det sydlige Storbritannien, de nordlige Forenede Arabiske Emirater, det østlige Japan, det sydøstlige Australien, det sydøstlige Asien | 2. december til 5. december 2022 |  13. december til 16. december 2022 | 
| Station 3 | Østasien, det vestlige Storbritannien, det vestlige Japan, det sydlige Brasilien, Det nordlige Europa, det østlige USA, Det centrale Forenede Arabiske Emirater | 3. december til 6. december 2022 |  13. december til 16. december 2022 | 
| Station 4 | Det vestlige Europa, Det centrale USA, Det vestlige USA | 4. december til 7. december 2022 |  13. december til 16. december 2022 | 
| Station 5 | DoD, Government Community Cloud (GCC), Kina | Ikke planlagt | Ikke planlagt |

### <a name="proactive-quality-update-calendar-year-2023-schedule"></a><a name="schedule"></a> Plan for proaktiv kvalitetsopdatering Kalenderår 2023

#### <a name="stations-to-region-mapping"></a><a name="Stations-Regions"></a> Områdetilknytning

| Stationer | Områder |
|---|---|
| Station 1 | Endnu ikke fastlagt |
| Station 2 | Det centrale Canada, det østlige Canada, det centrale Frankrig, det centrale Indien, det østlige Norge, det vestlige Schweiz |
| Station 3 | Det sydlige Frankrig, det sydlige Indien, det vestlige Norge, det nordlige Schweiz, det nordlige Sydafrika, det østlige Australien, det sydlige Storbritannien, de nordlige Forenede Arabiske Emirater, det østlige Japan, det sydøstlige Australien, det sydøstlige Asien |
| Station 4 | Østasien, det vestlige Storbritannien, det vestlige Japan, det sydlige Brasilien, Det nordlige Europa, det østlige USA, Det centrale Forenede Arabiske Emirater |
| Station 5 | Det vestlige Europa, Det centrale USA, Det vestlige USA |
| Station 6 | DoD, Government Community Cloud (GCC), Kina |


> [!IMPORTANT]
> Dette er en plan på højt niveau for år 2023. Se eksemplet nedenfor for at få en mere tilsnende plan for januar 10.0.30 Release-2. Den nøjagtige plan og appversion opdateres 7 dage før starten på et kvalitetsopdateringstog.

> [!Note]
> Kun de startede produktionsmiljøer modtager opdateringen for 10.0.30 Release-2-uddannelse, modtagelsesmiljøer modtager eksplicit kommunikation.

| Træning af kvalitetsopdatering | Frigiv afskæring | Træn varighed |
|---|---|---|
| 10.0.30 Release-2 | 16. december 2022 | 2. januar til 29. januar 2023 |
| 10.0.30 Release-3 | 13. januar 2023 | 30. januar til 25. februar 2023 |
| 10.0.30 Release-4 | 24. februar 2023 | 6. marts til 8. april 2023 |
| 10.0.31 Release-1 | 3. februar 2023 | 13. februar 2023 til 18. marts 2023|
| 10.0.31 Release-2 | 3. marts 2023 | 13. marts til 15. april 2023|
| 10.0.31 Release-3 | 14. april 2023 | 24. april 2023 til 27. maj 2023|
| 10.0.32 Release-1 | 31. marts 2023 | 10. april 2023 til 13. maj 2023|
| 10.0.32 Release-2 | 28. april 2023 | 8. maj 2023 til 10. juni 2023|
| 10.0.32 Release-3 | 26. maj 2023 | 5. juni 2023 til 8. juli 2023|
| 10.0.33 Release-1 | 28. april 2023 | 8. maj 2023 til 10. juni 2023|
| 10.0.33 Release-2 | 26. maj 2023 | 5. juni 2023 til 8. juli 2023|
| 10.0.33 Release-3 | 14. juli 2023 | 24. august 2023 til 26. august 2023|
| 10.0.34 Release-1 | 23. juni 2023 | 3. juli 2023 til 5. august 2023|
| 10.0.34 Release-2 | 21. juli 2023 | 31. juli 2023 til 2. september 2023|
| 10.0.34 Release-3 | 1. september 2023 | 11. september 2023 til 14. oktober 2023|
| 10.0.35 Release-1 | 28. juli 2023 | 7. august 2023 til 9. september 2023|
| 10.0.35 Release-2 | 25. august 2023 | 4. september 2023 til 7. oktober 2023|
| 10.0.35 Release-3 | 20. oktober 2023 | 30. december 2023 til 16. december 2023|
| 10.0.36 Release-1 | 29. september 2023 | 9. oktober 2023 til 11. november 2023|
| 10.0.36 Release-2 | 27. oktober 2023 | 6. november 2023 til 16. december 2023|
| 10.0.36 Release-3 | 12. januar 2024 | 22. januar 2023 til 24. februar 2024|
| 10.0.37 Release-1 | 3. november 2023 | 13. november 2023 til 6. januar 2024|
| 10.0.37 Release-2 | 30. december 2023 | 8. januar 2024 til 10. februar 2024|
| 10.0.37 Release-3 | 27. januar 2024 | 5. februar 2024 til 9. marts 2024|
| 10.0.37 Release-4 | 23. februar 2024 | 4. marts 2024 til 6. april 2024|

### <a name="proactive-quality-update-upcoming-10030-release-2-train-schedule"></a><a name="schedule"></a> Proaktiv kvalitetsopdatering kommende 10.0.30 Release-2-træningsplan
**App version: 10.0.1362.99**

| Stationer | Kommende sandkasseplan | Kommende produktionsplan |
|---|---|---|
| Station 1 | IT | IT |
| Station 2 | 2. januar til 5. januar 2023 | 21. januar til 22. januar 2023 |
| Station 3 | 3. januar til 6. januar 2023 | 28. januar til 29. januar 2023 |
| Station 4 | 9. januar til 12. januar 2023 | IT |
| Station 5 | 16. januar til 19. januar 2023 | IT |
| Station 6 | IT | IT |

> [!IMPORTANT] 
> Fem dage i forvejen opdaterer Microsoft den foregående plan og sender en besked til det sæt miljøer, der er planlagt til at modtage disse kvalitetsopdateringer. Den foregående plan gælder kun for miljøer, der er blevet gjort besked om en forestående opdatering. Du kan finde oplysninger om de mørke timer for hver region i [Hvad er de planlagte vedligeholdelsesvinduer efter region?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
>
> For hver regionsgruppe, eller *station*, hvor en kvalitetsopdatering aktuelt er planlagt til at blive rullet ud, viser planen et interval på fire dage. Kvalitetsopdateringer starter kun med sandboksmiljøer. Efterhånden som procentdelen af installerede sandbokse stiger, vil implementering i produktionsmiljøer begynde med avancerede beskeder til kunderne.
> 
> Kvalitetsopdateringerne finder altid sted på en rulleplan, hvor vi kan opstille et sæt miljøer pr. plan og færdiggøre alle sæt ved udgangen af den fjerde dag for en station. Men det betyder ikke, at en miljøopdatering dækker fire dage. Det betyder blot, at vi ikke på forhånd kan fastlægge, hvilke miljøer der skal opdateres på en given dag inden for intervallet på fire dage. Alle opdateringer udføres i mørketimer med nedetid på næsten nul. Opdateringerne afsluttes automatisk i vinduet med mørke timer i et bestemt område.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Hvordan håndteres de mørke timer for kunder, der har én finans- og operationsappforekomst, men er aktive i flere tidszoner? 
Der findes ingen særlige planer uden for de mørke timer, hvor der findes en forekomst af finansierings- og driftsapps, da vi planlægger at udrulle kvalitetsopdateringer på en minimalt afbrydende måde med [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Hvad er den aktuelle udrulning for proaktive kvalitetsopdateringer?
Proaktive kvalitetsopdateringer afsendes i øjeblikket en gang om måneden for hver understøttet version af en serviceopdatering. Der rykkes kun én opdatering pr. måned for udvalgte sandboksmiljøer, medmindre kunderne flytter til en ny version af serviceopdateringen. I dette tilfælde kan de få en foruddefineret PQU som del af et eksisterende tog til den nye serviceopdatering. Når den globale udrulning er fuldført i 2023, øges frekvensen af disse opdateringer. Du modtager altid mindst én måneds opsigelsesvarsel, når der sker en ændring i forsendelses-cadence.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Hvordan vil Microsoft sikre kvaliteten af disse opdateringer?
Microsoft gør det muligt at holde release-pipelinen effektiv nok til at levere små nyttelast til at holde valideringsomkostningen lav. Alle ret i en kvalitetsopdatering gennemgår en omhyggelig og sikker implementeringsproces, der hjælper med at forbedre kvaliteten og pålideligheden, hvilket reducerer kundens indflydelse. Installation sker i stadier i sandbox-miljøer først, efterfulgt af produktion. Trindelte installationer giver mulighed for passende overvågning for at finde ud af, om yderligere implementering er sikker. Vi stopper udrulningen, hvis der registreres problemer med hver enkelt gruppe kunder, der implementeres, og sikrer, at hvert trin i rullen har tilstrækkelig tid til, at problemerne kan opstå. Ved hver kommende kvalitetsopdatering vil vi give overblik over planen via opdateringer af offentlig dokumentation og e-mails, så kunderne kan planlægge for fremtiden.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Kan kunder forsinke, ændre eller sætte en kvalitetsopdatering på pause?
Nej. Hovedmålet med kvalitetsopdateringer er at sikre grundlæggende oplysninger som sikkerhed, beskyttelse af personlige oplysninger, pålidelighed, tilgængelighed og ydeevne bliver løbende forbedret for vores kunder. Hvis en opdatering forsinkes eller pauser, er sikkerhed, tilgængelighed og pålidelighed i fare.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Hvordan kan man kende sættet af ændringer, der blev ind i en kvalitetsopdatering af nyttelast?
Benyt nedenstående fremgangsmåde for at identificere listen over ændringer, der går ind i en kvalitetsopdatering af nyttelast. 

Brug kvalitetsopdateringstræning 10.0.28 og den relaterede appversion 10.0.1265.89.

1. I Lifecycle Services skal du åbne siden **Miljøoplysninger** for sandkassen. 
2. I afsnittet **Tilgængelige opdateringer** skal du vælge **Vis opdatering** for den seneste build til kvalitetsopdatering. 
3. Eksportér build til en CSV eller Microsoft Excel-fil.
4. Filtrer den eksporterede fil, og vælg den **Build-version**, der er mindre end eller lig med build-nummer 10.0.1265.89. Du skulle kunne se deltanyttelasten.
 
> [!NOTE]
> Eksporten til en CSV- eller Excel-fil skal finde sted, før miljøet opdateres. Ellers kan du bruge et miljø med en lignende konfiguration, der ikke har opdateringen installeret, og følge trinnene ovenfor.

[![Eksempel på miljø med kvalitetsopdatering.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Hvad er processen, hvis der bliver fundet et kritisk problem efter en kvalitetsopdatering?
Et vigtigt problem eller nyt område er en eller flere hændelser, der typisk medfører, at flere kunder får en forringet erfaring med en eller flere af vores tjenester. Disse problemer kan medføre ikke-planlagt nedetid, herunder utilgængeligheden, forringelse af ydeevne og interferens med servicestyring. Hvis der er en bred indflydelse på kunderne, fordi sådanne genvurderinger har betydning, stopper vi med at rulle ud af en kvalitetsopdatering, indtil vi kan kommunikere og løse problemet. Den næste kvalitetsopdatering vil typisk have den nødvendige rettelse til at fortsætte nedrulningen.

Hvis det påvirkes af et enkelt kundemiljø, kan du kontakte Microsoft support for at åbne en flybillet. På baggrund af berettigelse stopper vi rullen for kvalitetsopdateringen til alle andre miljøer i det pågældende projekt, indtil problemet reduceres.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lifecycle-services"></a>Kan kunder stadig anvende hotfix-opdateringer fra Lifecycle Services manuelt?
Ja. For at sikre løbende paritet med den måde, hotfixes fungerer på, kan der stadig anvendes hotfix-opdateringer til kundemiljøer i Lifecycle Services. Det er dog vigtigt at bemærke, at hotfixes, der implementeres som del af en kvalitetsopdatering, gennemgår standard SDP, før opdateringen implementeres. Dette reducerer risikoen for regressioner på grund af højere kvalitet. Det anbefales, at du vælger en kvalitetsopdatering via manuel brug af hotfixes for at forbedre pålideligheden.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Kan kunder proaktivt installere en kvalitetsopdatering selv før planen?
Ja. Du kan installere en kvalitetsopdatering proaktivt. Microsoft springer opdateringen over, hvis den aktuelle build-version for miljøet er den samme som eller højere end den aktuelle kvalitetsopdatering.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Hvis et miljø har en kommende planlagt månedlig serviceopdatering inden for en uge, modtager det så stadig kvalitetsopdateringer?
- Der anvendes ikke kvalitetsopdateringer til produktionsmiljøer, hvis der er en forestående serviceopdatering planlagt inden for en uge fra det tidspunkt, hvor kvalitetsopdateringen er planlagt til at finde sted.
- Hvis et sandbox-miljø har samme eller højere build-version end den forestående kvalitetsopdatering, springes det over.
- Hvis et produktionsmiljø har samme eller højere build-version end den forestående kvalitetsopdatering, springes det over.
- Hvis en sandkasse har samme eller højere build-version på grund af en kvalitetsopdatering eller en manuel opdatering af produktionen, vil produktionen stadig få den planlagte version af den månedlige serviceopdatering. Hvis det planlagte produktionsmiljø ikke skal opdateres til versionen af serviceopdateringen, kan du midlertidigt afbryde serviceopdateringen fra Lifecycle Services. 
- Det anbefales, at du bruger den seneste kvalitetsopdatering til at teste dine ændringer til en kommende serviceopdatering for at opnå større stabilitet og resultater.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Hvis der for et miljø er en kommende planlagt aktion og en planlagt kvalitetsopdatering i samme vedligeholdelsesvindue, modtager det stadig kvalitetsopdateringen?
Hvis der er et indhold med en planlagt aktion, f.eks. PITR (Point In Time Restore), omplanlægges kvalitetsopdateringen til det næste tilgængelige vedligeholdelsesvindue i vinduet med fire dage. Du kan finde flere oplysninger om de planen i [Hvad er planen for proaktive kvalitetsopdateringer?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kan et miljø ændres til tidligere tilstand, hvis der er problemer, efter at der er anvendt en kvalitetsopdatering?
Når der er anvendt en kvalitetsopdatering, er der ingen tilbageførsel under nogen omstændigheder. Der findes kun indstillinger for programrettelser, der kan reducere problemer.

## <a name="what-about-fda-regulation-and-gxp"></a>Hvad med FDA-regulering og GxP?
Planen for kunder, der er underlagt FDA-validering og -regulering, er stadig dynamisk. Forvent flere opdateringer i dette område snart. I øjeblikket er alle sådanne kunder undtaget fra kvalitetsopdateringer. Du kan sikre, at en kunde lever op til FDA-reglerne ved at besøge [Microsoft Azure GxP-tilbud](/azure/compliance/offerings/offering-gxp).

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Hvilke versioner af serviceopdateringer understøttes for disse kvalitetsopdateringer?
Kunder på alle understøttede versioner af serviceopdateringer er kvalificeret til kvalitetsopdateringer. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retail-sdk"></a>Implementeringer af økonomi- og operationsapps med detailkomponenter kræver typisk ekstra arbejde, udover at de skal implementere MPOS igen. Hvordan påvirker disse kvalitetsopdateringer Retail SDK? 
Da arten af hotfixes i sig selv ikke ændres i betalingsbelastningen af kvalitetsopdateringerne, forventer vi ikke på dette tidspunkt yderligere indflydelse, der specifikt vedrører detailkomponenter.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Har det indflydelse på CHE (Cloud Hosted Environments)? 
CHE-miljøer har ikke noget område til kvalitetsopdateringer, da de ligger uden for Microsoft-purview.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Er der nogen integrationsproblemer med Microsoft Dataverse? 
Der er ingen kendte integrationsproblemer for kvalitetsopdateringer med Dataverse.

