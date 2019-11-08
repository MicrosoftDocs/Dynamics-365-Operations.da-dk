---
title: Få adgang til funktioner til forhåndsvisning i Microsoft Dynamics 365 Talent
description: Dette emne beskriver, hvordan administratorer kan aktivere funktioner til forhåndsvisning i Microsoft Dynamics 365 Talent, og viser de funktioner, der i øjeblikket er tilgængelige som visningsfunktioner.
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 0f9a83aeea3942d3c56d32956f79490c91565e9e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551586"
---
# <a name="access-preview-features-in-microsoft-dynamics-365-talent"></a>Få adgang til funktioner til forhåndsvisning i Microsoft Dynamics 365 Talent

[!include[banner](../includes/banner.md)]

Som en del af vores fortløbende implementering af HCM-funktioner til styring af menneskelig kapital for Microsoft Dynamics 365 Talent, vil vi give kunderne mulighed for at udnytte nye funktioner, så hurtigt som muligt. Administratorer kan se og bruge funktioner til visning i deres miljøer. Disse funktioner bliver snart almindeligt tilgængelige og har gennemgået omfattende test. Vi mangler kun en sidste runde af kundefeedback og validering, før vi gør dem almindeligt tilgængelige.

Dette emne beskriver, hvordan du kan aktivere funktioner til visning, og viser de funktioner, der i øjeblikket er tilgængelige som visningsfunktioner. Denne liste opdateres, efterhånden som funktioner bliver gjort almindeligt tilgængelige og nye visningsfunktioner frigives. Der gives ikke besked, når der frigives nye funktioner til visning. Funktionerne bliver bare synlige for brugerne. Yderligere oplysninger om de nye funktioner i Talent finder du i [Nyheder eller ændringer i Dynamics 365 Talent](./whats-new.md) og [Dynamics 365 samt Power Platform-produktbemærkninger](https://docs.microsoft.com/business-applications-release-notes).

## <a name="enable-or-disable-preview-features"></a>Aktivere eller deaktivere funktioner i prøveversion

Hvis du vil have adgang til visningsfunktionerne, skal du først aktivere dem i dit miljø. Aktivering eller deaktivering af funktioner til visning er specifik for miljøet.

> [!IMPORTANT]
> Når du slår indstillingen **Prøveversioner** til, aktiverer du visningsfunktioner for alle brugere i organisationen, der arbejder i det pågældende miljø. Når du deaktiverer indstillingen, slår du funktioner til forhåndsvisning fra og gør dem utilgængelige for brugerne. Visningsfunktioner understøttes kun i begrænset omfang i Talent. Der er en mindre grad af beskyttelse af personlige oplysninger og færre sikkerhedsfunktioner, og visningsfunktionerne medtages ikke i Talent-serviceaftalen (SLA). Du bør ikke bruge visningsfunktioner til behandling af personoplysninger (dvs. alle oplysninger, der kan identificere dig) eller til at behandle andre data, der er omfattet af lovbestemte overholdelseskrav.

### <a name="attract"></a>Attract

1. Log på Microsoft Dynamics 365 Talent: Attract.
2. I menuen **Opsætning** (tandhjulsymbolet) i øverste højre hjørne skal du vælge **Administration**.
3. Under fanen **Administration af funktioner** skal du vælge indstillingen ud for **Funktioner i prøveversion**, så den bliver blå, og der står **Til**.

    ![Aktivér funktioner i Attract](./media/attract-enable-preview-features.png)

4. Vælg eller annuller markeringen af individuelle forhåndsvisningsfunktioner. Hvis du ikke gør noget, er alle tilgængelige forhåndsvisningsfunktioner aktiverede.
5. Opdater browseren for at begynde at se de nye funktioner. Alle brugere, der allerede er logget på, kan se funktionerne, næste gang de logger på, eller de kan opdatere deres webbrowser for at få vist funktionerne med det samme.

> [!NOTE]
> Nogle visningsfunktioner kræver muligvis yderligere konfiguration. Følg linkene ud for visningsfunktionen for at fuldføre opsætningen af det.

### <a name="core-hr"></a>Grundlæggende personalefunktioner

1. Log på Talent.
2. Vælg **Systemadministration**, og klik derefter på fanen **Links**.
3. Vælg **Systemparametre** under **Opsætning** på siden **Systemadministration**.
4. Vælg fanen **Funktioner i prøveversion** på siden **Systemparametre**.
5. Vælg indstillingen **Ja** for **Aktivér eksempelvisning for alle brugere**, hvis du gøre visningsfunktionerne tilgængelige.

    ![Aktivere funktioner i Core HR](./media/corehr-enable-preview-features.png)

> [!NOTE]
> For at deaktivere eksempelfunktioner skal du bruge den samme fremgangsmåde, men vælge indstillingen **Nej** for **Aktivér eksempelvisning for alle brugere**. Når du deaktiverer eksempelfunktioner, de bliver utilgængelige for brugerne, og der kan opstå fejl i processer, der er knyttet til funktionerne.

### <a name="onboard"></a>Introducer

Der er i øjeblikket ingen tilgængelige visningsfunktioner for Microsoft Dynamics 365 Talent: Onboard.

## <a name="features-that-are-currently-in-preview"></a>Funktioner, der i øjeblikket findes som eksempelfunktioner

### <a name="attract"></a>Attract

- [Kandidatanbefaling](./intelligent-recommendations.md#candidate-recommendations) – Hvis der til et job er mere end ti ansøgere, der har CV'er eller fuldstændige profiler, vises de ansøgere, der bedst opfylder kravene til et job, i sektionen **Ansøgere, der skal tages i betragtning** på den pågældende jobside.
- [Jobanbefaling](./intelligent-recommendations.md#job-recommendations) – Hvis der er opslået mere end ti job på dit karrierewebsted, leverer Attract jobanbefalinger til jobkandidater.
- [Integration af Broadbean](./posting-jobs-external.md#post-jobs-to-broadbean) – Du kan opslå job fra Attract til Broadbean, et eksternt websted til opslag af job. Når du har aktiveret denne visningsfunktion, skal du fuldføre opsætningen ved at angive dit Broadbean-brugernavn, klient-ID og krypteringstoken.
- [Analyser](./analytic-reports.md) – I analysehubben kan ansættelsesteam bruge nøglemålepunkter til et enkelt job plus samlet metrik på tværs af alle job.
- [EEO](./activities-attract.md) – Med nye aktivitetstyper kan du bruge en foruddefineret formular til at indsamle data for lige ansættelsesmuligheder (EEO) og OFCCP-data (Office of Federal Contract Compliance Program) fra en kandidat. Den foruddefinerede formular kan ikke redigeres.
- [Anbefaling af kundeemne](./intelligent-recommendations.md#prospect-recommendations) – Attract vurderer tidligere ansøgere og aktuelle kandidater og leverer en liste over kundeemner, der er et godt match til dit job.
- [Relevanssøgning](./attract-talent-pools.md#search-and-view-candidate-profiles) – Du kan søge i hele kandidatdatabasen efter specifikke færdigheder, navne eller uddannelsesmæssige baggrunde. Attract søger i hele profilen og fremhæver alle de resultater, der bliver fundet. Attract søger ligeledes i alle de dokumenter, der er tilgængelige for en kandidat, og rangerer søgeresultaterne på en intelligent måde.
- [Aktivitetsmålgruppe](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – Du kan indstille målgruppen for aktiviteter (f.eks. samtale, tidsplan eller tilbagemelding) til **Alle kandidater**, **Interne kandidater** eller **Eksterne kandidater**. Du kan levere brugertilpassede aktiviteter som f.eks. YouTube-videoer, webstedsindhold og Microsoft Forms, til alle kandidater, kun interne kandidater, kun eksterne kandidater eller til ansættelsesteamet.
- [Ansøg med LinkedIn](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – Du kan konfigurere en indstilling på dit Attract-karrierewebsted, så kandidater kan ansøge ved hjælp af LinkedIn. Denne funktion effektiviserer ansøgningsprocessen for dine kandidater ved at lade dem bruge deres LinkedIn-profil til automatisk at udfylde deres ansøgninger på dit karrierewebsted.
- [Kildesporing](./source-tracking.md) – Attract sporer kilden til kandidaternes ansøgninger og giver værdifulde oplysninger, der kan hjælpe dig med at målrette dine rekrutteringstiltag. Du kan også vælge en ansøgningskilde, når du føjer en kandidat til et job eller en talentpulje.
- [Sølvmedaljetager](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – Hvis nogle kandidater matcher din organisation særlig godt, uden at du har tilbudt dem den aktuelle stilling, kan du udpege dem som sølvmedaljetagere. Denne funktion hjælper med at reducere din ansættelsestid, næste gang du har en tilsvarende ledig stilling.

### <a name="core-hr"></a>Grundlæggende personalefunktioner

- [Validering af data i stillingshierarki](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – Du kan validere ledelseshierarkiet for alle cirkulære referencer, der utilsigtet er importeret.
- [Angiv årsagskoder for orlovstyper](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – Du kan angive årsagskoder for orlovstyper.
- [Kræve årsagskoder ved anmodninger om fritid](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – Ud over at angive årsagskoder for orlovstyper kan du kræve årsagskoder for fritidsanmodninger.
- [Udarbejdelse af en transaktionsliste over orlov og fravær til Personale](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – Du kan få vist en liste over orlovs-og fraværsposter, der hjælper med at give indsigt i fritidssaldi .

### <a name="onboard"></a>Introducer

Der er i øjeblikket ingen tilgængelige visningsfunktioner for Onboard.

## <a name="feedback"></a>Tilbagemelding

Vi vil gerne høre fra dig om din oplevelse med disse visningsfunktioner. Vi opfordrer dig til jævnligt at opslå din feedback på følgende websteder, når du bruger disse eller andre funktioner:

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Dette websted er en nyttig ressource, hvor brugere kan diskutere eksempler på brug, stille spørgsmål og få hjælp fra community'et.
- Fortæl os om de funktioner, som du gerne vil have i produktet, eller gør os opmærksom på eventuelle ændringer, som du synes, vi skal foretage af eksisterende funktioner. Du kan komme med ideer til produkter på følgende websteder:

    - [Attract-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Onboard-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

Undgå at medtage personlige oplysninger (oplysninger, der kan identificere dig) i din feedback eller indsendelser af produktanmeldelser. Indsamlede oplysninger kan blive analyseret yderligere, men de bruges ikke til at besvare spørgsmål i henhold til gældende love om beskyttelse af personlige oplysninger. Personlige data, der indsamles særskilt i henhold til disse programmer, er underlagt [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Sæt et bogmærke ved dette emne, og kom tilbage ofte for at holde dig opdateret om nye eksempelfunktioner, efterhånden som vi frigiver dem.

## <a name="see-also"></a>Se også

- [Prøv eller køb Talent-apps](https://dynamics.microsoft.com/talent/overview/)
- [Nyheder](./whats-new.md)
- [Frigivelsesnoter](https://docs.microsoft.com/business-applications-release-notes/index)
- [Få support til Talent](./talent-support.md)
