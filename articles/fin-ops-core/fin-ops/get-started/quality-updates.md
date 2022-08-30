---
title: Proaktive kvalitetsopdateringer
description: Denne artikel indeholder oplysninger om proaktiv levering af kvalitetsopdateringer.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338130"
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
- **Version reserve** - Flybillet bruges til at gruppere alle ændringer i en proaktiv kvalitetsopdatering. Hvis reservesystem er påkrævet efter en proaktiv implementering, kan det ske via flysystemet.
- **Synkroniseringsangivelse for sandkasse** – Mindre end 20 procent af kunderne har i dag flere sandbokse, og én sandboks anvendes, hvor versionen matcher produktionen, som en hjælp ved fejlfinding. I den nærmeste tid vil vi introducere kundernes mulighed for at angive et sandkassemiljø, der ikke bør modtage den proaktive implementering af kvalitetsopdatering sammen med andre sandkasser, men som i stedet skal modtage det senere sammen med produktionsmiljøet. Bemærk, at hvis en kunde bruger en sandkasse til at teste en nyere version end produktionen, vil denne sandkasse modtage kvalitetsopdateringer til den nyere version.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Hvornår starter proaktive kvalitetsopdateringer?

Distributionen af proaktive kvalitetsopdateringer til sandkasse-miljøer forventes at begynde i slutningen af september eller oktober 2022 for Azure-kunder i skyen. Forsøgsmiljøer begynder også at modtage proaktiv opdateringsinstallation på det tidspunkt. I september vil der blive sendt en besked til hver kunde for at informere dem om den forventede tidsplan for deres miljøer. Der tillades kun undtagelser til den proaktive opdaterede distributionsproces for FDA-regulerede kunder. Vi arbejder stadig med, hvordan regulerede miljøer og regulerede og offentlige skykunder skal håndteres.

I løbet af de næste seks måneder vil vi øge procentdelen af sandboksmiljøer, der modtager proaktive opdateringer, indtil alle angivne miljøer er medtaget, og de skrider frem til opdatering af produktionsmiljøer. I løbet af perioden overvåger vi for at sikre, at installationsprocessen fungerer uden problemer, og at vi igen får brug for ikke-forstyrrende nyttelast.

Da kunderne jævnligt modtager mindre nyttelast, forventer vi, at processen med aktuelle arbejde bliver simplere. Vi vil justere frekvensen for opdateringsinstallation, efterhånden som vi viser, hvordan vi kan køre processen uden afbrydelser. Denne proces fungerer allerede effektivt for vores Dataverse-platform og programmer og leverer de forventede forbedringer af servicekvaliteten. Vi gør det samme i forbindelse med finans- og driftsprogrammer.
