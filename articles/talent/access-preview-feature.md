---
title: Få adgang til funktioner til forhåndsvisning i Talent
description: Dette emne beskriver, hvordan administratorer kan aktivere funktioner til visning, og viser de funktioner, der i øjeblikket er tilgængelige som visningsfunktioner.
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: cd738cafc97477182e574ee0f363fdcf1df7da7a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303719"
---
# <a name="access-preview-features-in-talent"></a>Få adgang til funktioner til forhåndsvisning i Talent

[!include[banner](../includes/banner.md)]

Som en del af vores fortløbende implementering af produktegenskaber vil vi give kunderne mulighed for at udnytte nye funktioner, så hurtigt som muligt. Administratorer kan se og bruge funktioner til visning i deres miljøer. Disse funktioner bliver snart almindeligt tilgængelige og har gennemgået omfattende test. Vi mangler kun en sidste runde af kundefeedback og validering, før vi generelt frigiver dem.

Dette emne beskriver, hvordan administratorer kan aktivere funktioner til visning, og viser de funktioner, der i øjeblikket er tilgængelige som visningsfunktioner. Denne liste opdateres, efterhånden som funktioner bliver gjort almindeligt tilgængelige og nye visningsfunktioner frigives. Der gives ikke besked, når der frigives nye funktioner til visning. Funktionerne bliver bare synlige for brugerne.

## <a name="enable-or-disable-preview-features"></a>Aktivere eller deaktivere funktioner til visning

Du kan bruge indstillingen **Prøveversioner** i Microsoft Dynamics 365 for Talent Administration til at aktivere eller deaktivere funktioner til visning. Indstillingen er som standard slået fra. Handlingen med at aktivere eller deaktivere funktioner til visning er specifik for miljøet.

> [!IMPORTANT]
> Ved at slå indstillingen **Prøveversioner** til aktiverer du visningsfunktioner for alle brugere i organisationen, der arbejder i det pågældende miljø. Ved at deaktivere indstillingen deaktiverer du funktioner til visning og gør dem utilgængelige for brugerne. Visningsfunktioner understøttes kun i begrænset omfang i Talent. Der er en mindre grad af beskyttelse af personlige oplysninger og færre sikkerhedsfunktioner, og visningsfunktionerne medtages ikke i Talent-serviceaftalen. Du bør ikke bruge visningsfunktioner til behandling af personoplysninger (dvs. alle oplysninger, der kan identificere dig) eller til at behandle andre data, der er omfattet af lovbestemte overholdelseskrav.

### <a name="enable-or-disable-preview-features-for-your-organization"></a>Aktivere eller deaktivere funktioner til visning for organisationen

#### <a name="attract"></a>Tiltræk

1. Log på Microsoft Dynamics 365 for Talent: Attract.
2. I menuen **Opsætning** (tandhjulsymbolet) i øverste højre hjørne skal du vælge **Administratorindstillinger**.
3. Under fanen **Administration af funktioner** skal du vælge indstillingen ud for **Funktioner i prøveversioner**, så den bliver blå.
4. Du kan vælge at styre individuelle funktioner ved at aktivere/deaktivere bestemte funktioner på denne side.
5. Opdater browseren for at begynde at se de nye funktioner. (Alle brugere, der allerede er logget på, kan se funktionerne, næste gang de logger på, eller de kan opdatere deres webbrowser for at få vist funktionerne med det samme).

#### <a name="core-hr"></a>Grundlæggende personalefunktioner

1. Log på Talent. Det grundlæggende arbejdsområde for personale, hvor du skal udføre de resterende trin, åbnes. 
2. Vælg **Systemadministration \> Links til systemparametre**.
3. På siden **Systemparametre** under fanen **Funktioner i prøveversioner** skal du vælge **Ja** i indstillingen **Aktivér eksempelvisning for alle brugere** for at gøre eksempelfunktioner tilgængelige.

> [!NOTE]
> For at deaktivere eksempelfunktioner skal du bruge den samme grundlæggende fremgangsmåde. Når du deaktiverer eksempelfunktioner, de bliver utilgængelige for brugerne, og der kan opstå fejl i processer, der er knyttet til funktionerne.

## <a name="features-that-are-currently-in-preview"></a>Funktioner, der i øjeblikket findes som eksempelfunktioner

### <a name="attract"></a>Tiltræk

- **Relevante kandidater i et Job** – Rekrutteringsmedarbejdere og ansættelsesansvarlige kan nemt se, hvilke ansøgere der kan være de mest relevante til jobbet på tværs af alle ansøgere. De 5 højst prioriterede ansøgere vises ud fra relevansen af deres CV/profil i forhold til jobbeskrivelsen.
- **Relevante job** – Kandidaterne kan nu se en liste over andre job, der er relevante for dem, baseret på deres CV/profil og jobbeskrivelserne.  I øjeblikket vises dette til kandidaterne, når de ansøger, som forslag til andre muligheder.
- **Understøttelse af EEO/OFCCP** – Nye aktivitetstyper muliggør brugen af en foruddefineret formular til indsamling af data for lige ansættelsesmuligheder (EEO) og OFCCP-data (Office of Federal Contract Compliance Program) fra kandidaten.  Dette er en foruddefineret formular, som ikke kan redigeres.

    > [!NOTE]
    > Job, der er slået op, kan kun ses af kunder, der abonnerer på en eller flere LinkedIn-joboversigtsprodukter. Ellers kan kunderne kun se et job, hvis de eksplicit søger efter det. Der er en forsinkelse, når job slås op på LinkedIn. Det kan tage et par timer, før et job vises, når det er opslået fra Attract.

- **Kandidatansøgning** – Både interne og eksterne kandidater kan nu ansøge direkte fra jobsiden på karrierewebstedet.
- **Offer Management** – Brugerne kan nu oprette tilbudsbreve fra skabeloner, der indeholder pladsholdere. Efterhånden som kandidaterne avancerer til jobtilbudsstadiet, kan rekrutteringsmedarbejder eller ansættelsesansvarlige bruge tilbudsværktøjet til at forberede en ansøgers formelle tilbud via skabeloner, sende tilbuddet til intern godkendelse og endelig sende tilbuddet til kandidaten til underskrivning. Der vil blive tilføjet mange nye funktioner til tilbudsværktøjet med tiden, og eksempelversionen vil blive opdateret med disse funktioner, når vi er klar til at frigive dem som eksempelfunktioner.

### <a name="core-hr"></a>Grundlæggende personalefunktioner

- **Åben tilmelding** – Med Åben tilmelding som frynsegode får medarbejderne en enkel selvbetjeningsoplevelse, når de skal vælge deres frynsegoder. Personaleadministratorer kan konfigurere processen for frynsegodet åben tilmelding for organisationen og tilmeldingsoplevelsen for medarbejdere ved hjælp af en automatiseret løsning, der er nem at følge.

## <a name="feedback"></a>Tilbagemelding

Uanset om din feedback er positiv eller negativ, vil vi gerne høre fra dig om din brug af eksempelfunktionerne. Vi opfordrer dig til jævnligt at opslå din feedback på følgende websteder, når du bruger disse eller andre funktioner.

- [Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Dette websted er en nyttig ressource, hvor brugere kan diskutere eksempler på brug, stille spørgsmål og få hjælp fra community'et.
- Du kan bruge følgende websteder til at komme med produktideer. Fortæl os om de funktioner, som du gerne vil have i produktet, og også eventuelle ændringer, du synes, skal foretages af eksisterende funktioner.

    - [Attract-ideer](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Grundlæggende personalefunktioner](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

Medtag ikke personlige oplysninger (oplysninger, der kan identificere dig) i din feedback eller indsendelser af produktanmeldelser. Oplysninger, der indsamles, kan blive analyseret yderligere, og de bruges ikke til at besvare spørgsmål i henhold til gældende love om beskyttelse af personlige oplysninger. Personlige data, der indsamles særskilt i henhold til disse programmer, er underlagt [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Sæt et bogmærke ved dette emne, og kom tilbage ofte for at holde dig opdateret om nye eksempelfunktioner, efterhånden som vi frigiver dem.
