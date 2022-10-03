---
title: Proaktive kvalitetsopdateringer
description: Denne artikel indeholder oplysninger om proaktiv levering af kvalitetsopdateringer.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c2d26b7c5e110d05806c064e15a3ad2af34d0fbd
ms.sourcegitcommit: fde2867524b6a851628185cbdeee60a6ad918d08
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/26/2022
ms.locfileid: "9592040"
---
# <a name="proactive-quality-updates"></a>Proaktive kvalitetsopdateringer

[!include[banner](../includes/banner.md)]

I løbet af de seneste flere år har Microsoft gjort fortløbende, hvad vi kalder [Én version](../../dev-itpro/lifecycle-services/oneversion-overview.md). Udgangspunktet for én version er simpel: Jo tættere på vi kan være på at have alle kunder på samme softwareversion, jo højere kvalitet kan vi levere. Vi finder og løser problemer én gang, og vi gør disse løsninger hurtigere til kundernes behov.

Denne forudsætning er bekræftet af resultaterne: lavere hændelser tæller på tværs af vores produkter. Når kunder ikke findes på samme version, ser vi konsistent, at de er påvirket af problemer, som en løsning allerede er tilgængelig for. Vi har allerede gjort store fremskridt med Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations og Dynamics 365 Commerce – og takket være de seneste tekniske fremskridt – er det nu muligt at tage næste trin. Følgende oplysninger viser, hvad vi vil gøre, hvad vi allerede har gjort for at sætte stadiet, og hvordan og hvornår vi vil introducere de nye egenskaber uden problemer.

## <a name="focus-on-quality-updates"></a>Fokus på kvalitetsopdateringer

Vi leverer i øjeblikket syv [serviceopdateringer](public-preview-releases.md) pr. år. Version 10.0.29 er f.eks. en serviceopdatering. Indtil for nylig var der otte opdateringer pr. år. Men vi har afbrudt én opdatering som svar på kundefeedback, der ønsker at undgå ændringer i slutningen af kalenderåret.

Vi ændrer ikke cadencen for serviceopdateringerne. I stedet er næste trin fremad i versionen fokuseret på *kvalitetsopdateringer*. Kvalitetsopdateringer er akkumulerede builds af hotfixes. De inkluderer ikke nye funktioner. På et givet tidspunkt spredes hele gruppen af kunder mellem de tre eller fire seneste serviceopdateringer. Ved en given serviceopdatering kan versioner af forskellige kvalitetsopdateringsversioner dog bruges i gruppen, afhængigt af de datoer, hvor personerne blev implementeret. I næste trin udsender vi proaktivt kvalitetsopdateringer. Vi bruger allerede denne model til vores Dataverse-baserede programmer og har set de forventede resultater af forbedret kvalitet og reduceret supporthændelser.

En reduktion af defekter kan naturligvis reducere eller eliminere behovet for kvalitetsopdateringer. Vi har flere initiativ i fly for at reducere de defekter, der kræver kvalitetsopdateringer. Selv når nyttelast reduceres i kvalitetsopdateringen, vil konsistens på tværs af kundebasen forbedre understøttelsen, hurtigere få forbedringer til kunderne og reducere antallet af kunder, der i forvejen oplever problemer, der allerede findes løsninger for.

## <a name="making-proactive-distribution-possible"></a>Gøre proaktiv distribution mulig

Der er allerede implementeret flere forskud, som giver mulighed for proaktiv levering af kvalitetsopdateringer:

- **Opdatering af nedetid ved nul** – Hvis du vil køre mere hyppige miljøer, er det vigtigt, at tilgængeligheden af ressourcer i miljøet reduceres, så Dynamics 365 Service Level Agreements bevares. Der blev oprindeligt introduceret opdatering af Ved nul-nedetid for at forbedre den månedlige programrettelse af operativsystemet ved hjælp af en cluster failover for at aktivere det opdaterede billede med minimale afbrydelser. Mekanismen til anvendelse af opdateringer bliver udvidet, så den er endnu mindre afbrydende, og den dækker både programrettelse af operativsystemet og implementering af kvalitetsopdatering.

    For interaktive brugere kan en aktiv session blive afbrudt, og forsøge at fortsætte til det nu opdaterede miljø. Med introduktionen af [prioriteret batchplanlægning](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md), der nu er tilgængeligt på basis af tilvalg, vil batchplanlægning og batchafvikling blive genoprettet og genoptaget umiddelbart efter opdateringen. Der findes prioriteret batchplanlægning for kunderne, før de begynder at deltage i proaktiv distribution af kvalitetsopdateringer til deres produktionsmiljøer.

- **Mørke timer** – Der er defineret mørke timer for hver Azure-region, og der vil forekomme næsten nul-nedetidsopdateringer i løbet af perioden med mørke timer.

## <a name="the-proactive-update-process"></a>Den proaktive opdateringsproces

Implementering af proaktive kvalitetsopdateringer vil følge en sikker implementeringsproces (SDP). SDP'ens specifikke oplysninger udvikler sig, men kvalitetsopdateringer vil først blive implementeret i sandboksmiljøer. Processen starter med miljøer, hvor der kan installeres før tid. Efterhånden som procentdelen af installerede sandbokse stiger, vil implementering i produktionsmiljøer begynde. Processen starter igen med miljøer, hvor der kan installeres før tid. Lyttesystemer vil overvåge system telemetry og Livesite-hændelser og stopper rollout af en bestemt version, hvis der registreres regression. Kunderne vil stadig kunne trække kvalitetsopdateringerne før proaktiv implementering, hvis det er nødvendigt.

De aktuelle data for frigivelsesstyring viser, at mindre end 3 procent af generne introduceres i kvalitetsopdateringer. Med øget fokus på eliminering af genstigning og et udvidet SDP vil den potentielle virkning af genvurdering være betydeligt lavere end den kvalitetsvind, der opnås, hvis de bliver implementeret overordnet på kunderne.

## <a name="process-changes"></a>Behandl ændringer

Der implementeres et sæt procesændringer før aktiveringen af proaktiv implementering af kvalitetsopdatering:

- **Skema** – Værktøj sikrer, at kvalitetsopdaterings builds kun omfatter skemaændringer, der kan anvendes, mens tjenesten er online. Denne indfaldsvinkel hjælper med at bevare muligheden for at anvende opdateringen med nedetid tæt på nul.
- **Udvidet antal ændringer** - Aktuelt er der allerede et ekstra procestrin til godkendelse af ændringer, så de medtages i en kvalitetsopdatering. Den trinvise reduktion i det ekstra trin øges for at reducere regressionsmulighederne. Det er ikke tilladt at ændre noget i kvalitetsopdateringerne, og den øgede ændring er med til at sikre, at vi opfylder dette mål.
- **Synlighed** – Vi sender beskeder via e-mail og Lifecycle Services (LCS) om kommende proaktive kvalitetsopdateringer. Desuden vil supportteams og hændelsesemner have synlighed for, hvor kvalitetsopdateringer er blevet implementeret proaktivt.
- **Fejlsikret via flighting** – Flighting bruges til ændringer af beskyttelseskode, hvor det er relevant i en kvalitetsopdateringsrettelse eller ved hjælp af den eksisterende funktions-flighting, der er relevant for rettelsen. Hvis der kræves en reserve eller et deaktiveret skift efter en proaktiv installation, kan den udføres via flighting-systemet for at undgå yderligere fejl.
- **Synkroniseringsangivelse for sandkasse** – Mindre end 20 procent af kunderne har i dag flere sandbokse, og én sandboks anvendes, hvor versionen matcher produktionen, som en hjælp ved fejlfinding. Hvis en kunde bruger en sandkasse til at teste en nyere version end produktionen, vil denne sandkasse modtage kvalitetsopdateringer til den nyere version.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Hvad er rullelisten for kvalitetsopdateringer?

Distributionen af proaktive kvalitetsopdateringer til sandkasse-miljøer forventes at begynde i slutningen af september eller oktober 2022 for Azure-kunder i skyen. Forsøgsmiljøer begynder også at modtage proaktiv opdateringsinstallation på det tidspunkt. I september vil der blive sendt en besked til hver kunde for at informere dem om den forventede tidsplan for deres miljøer. Der tillades kun undtagelser til den proaktive opdaterede distributionsproces for FDA-regulerede kunder. Vi arbejder stadig med, hvordan regulerede miljøer og regulerede og offentlige skykunder skal håndteres.

I løbet af de næste seks måneder vil vi øge procentdelen af sandboksmiljøer, der modtager proaktive opdateringer, indtil alle angivne miljøer er medtaget, og de skrider frem til opdatering af produktionsmiljøer. I løbet af perioden overvåger vi for at sikre, at installationsprocessen fungerer uden problemer, og at vi igen får brug for ikke-forstyrrende nyttelast.

Da kunderne jævnligt modtager mindre nyttelast, forventer vi, at processen med aktuelle arbejde bliver simplere. Vi vil justere frekvensen for opdateringsinstallation, efterhånden som vi viser, hvordan vi kan køre processen uden afbrydelser. Denne proces fungerer allerede effektivt for vores Dataverse-platform og programmer og leverer de forventede forbedringer af servicekvaliteten. Vi gør det samme i forbindelse med finans- og driftsprogrammer.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Hvornår starter kvalitetsopdateringerne for produktionsmiljøer?
På dette tidspunkt er kvalitetsopdateringer kun målsandbokse. Dette område opdateres med en startdato for produktionsmiljøer, når der er mere konkrete data og måleværdier fra proaktive opdateringer for sandkasser til målere af parathed til produktion.

## <a name="what-is-the-schedule-for-sandbox-quality-updates"></a>Hvad er planlægningen for kvalitetsopdateringer?
Du kan finde oplysninger om de mørke timer for hver region i [Hvad er planen for proaktive kvalitetsopdateringer?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-is-the-schedule-for-proactive-quality-updates).

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Hvordan håndteres de mørke timer for kunder, der har én finans- og operationsappforekomst, men er aktive i flere tidszoner? 
Der findes ingen særlige planer uden for de mørke timer, hvor der findes en forekomst af finansierings- og driftsapps, da vi planlægger at udrulle kvalitetsopdateringer på en minimalt afbrydende måde med [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Hvordan vil Microsoft sikre kvaliteten af disse opdateringer?
Microsoft gør det muligt at holde release-pipelinen effektiv nok til at levere små nyttelast til at holde valideringsomkostningen lav. Alle ret i en kvalitetsopdatering gennemgår en omhyggelig og sikker implementeringsproces, der hjælper med at forbedre kvaliteten og pålideligheden, hvilket reducerer kundens indflydelse. Installation sker i stadier i sandbox-miljøer først, efterfulgt af produktion. Trindelte installationer giver mulighed for passende overvågning for at finde ud af, om yderligere implementering er sikker. Vi stopper udrulningen, hvis der registreres problemer med hver enkelt gruppe kunder, der implementeres, og sikrer, at hvert trin i rullen har tilstrækkelig tid til, at problemerne kan opstå. Ved hver kommende kvalitetsopdatering vil vi give overblik over planen via opdateringer af offentlig dokumentation og e-mails, så kunderne kan planlægge for fremtiden.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Kan kunder forsinke, ændre eller sætte en kvalitetsopdatering på pause?
Nej. Hovedmålet med kvalitetsopdateringer er at sikre grundlæggende oplysninger som sikkerhed, beskyttelse af personlige oplysninger, pålidelighed, tilgængelighed og ydeevne bliver løbende forbedret for vores kunder. Hvis en opdatering forsinkes eller pauser, er sikkerhed, tilgængelighed og pålidelighed i fare.

## <a name="how-can-one-know-the-set-of-changes-that-went-into-a-quality-update-payload"></a>Hvordan kan man kende sættet af ændringer, der blev ind i en kvalitetsopdatering af nyttelast?
Du kan se på alle KB-artiklerne i en kvalitetsopdatering baseret på siden **Miljødetaljer** i LCS ved at navigere til afsnittet **Kvalitetsopdatering**. 

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Hvad er processen, hvis der bliver fundet et kritisk problem efter en kvalitetsopdatering?
Et vigtigt problem eller nyt område er en eller flere hændelser, der typisk medfører, at flere kunder får en forringet erfaring med en eller flere af vores tjenester. Disse problemer kan medføre ikke-planlagt nedetid, herunder utilgængeligheden, forringelse af ydeevne og interferens med servicestyring. Hvis der er en bred indflydelse på kunderne, fordi sådanne genvurderinger har betydning, stopper vi med at rulle ud af en kvalitetsopdatering, indtil vi kan kommunikere og løse problemet. Den næste kvalitetsopdatering vil typisk have den nødvendige rettelse til at fortsætte nedrulningen.

Hvis det påvirkes af et enkelt kundemiljø, kan du kontakte Microsoft support for at åbne en flybillet. På baggrund af berettigelse stopper vi rullen for kvalitetsopdateringen til alle andre miljøer i det pågældende projekt, indtil problemet reduceres.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Kan kunder stadig anvende hotfix-opdateringer fra LCS manuelt?
Ja. For at sikre løbende paritet med den måde, hotfixes fungerer på, kan der stadig anvendes hotfix-opdateringer til kundemiljøer i LCS. Det er dog vigtigt at bemærke, at hotfixes, der implementeres som del af en kvalitetsopdatering, gennemgår standard SDP, før opdateringen implementeres. Dette reducerer risikoen for regressioner på grund af højere kvalitet. Det anbefales, at du vælger en kvalitetsopdatering via manuel brug af hotfixes for at forbedre pålideligheden.

## <a name="can-customers-self-install-a-quality-update-build-by-themselves-ahead-of-the-schedule"></a>Kan kunder installere en kvalitetsopdatering selv før planen?
Ja. Du kan installere en kvalitetsopdatering proaktivt. Microsoft springer opdateringen over, hvis den aktuelle build-version for miljøet er den samme som eller højere end den aktuelle kvalitetsopdatering.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Hvis et miljø har en kommende planlagt månedlig serviceopdatering inden for en uge, modtager det så stadig kvalitetsopdateringer?
- Der anvendes ikke kvalitetsopdateringer, hvis der er en forestående serviceopdatering planlagt inden for en uge fra det tidspunkt, hvor kvalitetsopdateringen er planlagt til at finde sted.
- Hvis et sandbox-miljø har samme eller højere build-version end den forestående kvalitetsopdatering, springes det over.
- Hvis et produktionsmiljø har samme eller højere build-version end den forestående kvalitetsopdatering, springes det over.
- Hvis en sandkasse har samme eller højere build-version på grund af en kvalitetsopdatering eller en manuel opdatering af produktionen, vil produktionen stadig få den planlagte version af den månedlige serviceopdatering. Hvis det planlagte produktionsmiljø ikke skal opdateres til versionen af serviceopdateringen, kan du midlertidigt afbryde serviceopdateringen fra LCS. 
- Det anbefales, at du bruger den seneste kvalitetsopdatering til at teste dine ændringer til en kommende serviceopdatering for at opnå større stabilitet og resultater.

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kan et miljø ændres til tidligere tilstand, hvis der er problemer, efter at der er anvendt en kvalitetsopdatering?
Når der er anvendt en kvalitetsopdatering, er der ingen tilbageførsel under nogen omstændigheder. Der findes kun indstillinger for programrettelser, der kan reducere problemer.

## <a name="what-about-fda-regulation-and-gpx"></a>Hvad med FDA-regulering og GPX?
Planen for kunder, der er underlagt FDA-validering og -regulering, er stadig dynamisk. Forvent flere opdateringer i dette område snart. I øjeblikket er alle sådanne kunder undtaget fra kvalitetsopdateringer.

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Hvilke versioner af serviceopdateringer understøttes for disse kvalitetsopdateringer?
Kunder på versioner, der er N-2 ikke vil modtage kvalitetsopdateringer. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Implementeringer af økonomi- og operationsapps med detailkomponenter kræver typisk ekstra arbejde, udover at de skal implementere MPOS igen. Hvordan påvirker disse kvalitetsopdateringer RetailSDK? 
Da arten af hotfixes i sig selv ikke ændres i betalingsbelastningen af kvalitetsopdateringerne, forventer vi ikke på dette tidspunkt yderligere indflydelse, der specifikt vedrører detailkomponenter.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che-"></a>Har det indflydelse på CHE (Cloud Hosted Environments)? ? 
Nej.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Er der nogen integrationsproblemer med Microsoft Dataverse? 
Nej.

