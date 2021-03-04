---
title: Dimensionshierarki
description: Dette emne indeholder oplysninger om dimensionshierarkier. Du kan bruge et dimensionshierarki til at definere rapporteringsstrukturen, omkostningspolitikker og sikkerhedsopsætning i Omkostningsregnskab.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71ba02fc6be4ab9a7871c10a9f95c474e52ae765
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441477"
---
# <a name="dimension-hierarchy"></a>Dimensionshierarki

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om dimensionshierarkier. Du kan bruge et dimensionshierarki til at definere rapporteringsstrukturen, omkostningspolitikker og sikkerhedsopsætning i Omkostningsregnskab.  

## <a name="overview"></a>Overblik

Dimensionshierarkier bruges forskellige steder i Omkostningsregnskab. Med et dimensionshierarki kan du definere følgende oplysninger:

-  Den rapporteringsstruktur, der passer til organisationens behov
-  Omkostningspolitikker
-  Sikkerhedsopsætningen

Her er et eksempel på et dimensionshierarki.

![Eksempel på et dimensionshierarki](./media/dimension-hierarchy.png)

Du kan oprette et dimensionshierarki for følgende dimensionstyper:

-  Dimensioner for omkostningselement
-  Dimensioner for omkostningsobjekt
-  Statistiske dimensioner

> [!NOTE]
> - Du kan oprette flere dimensionshierarkier for den samme dimension, hvis der kræves forskellige perspektiver.
> - Et dimensionshierarki kan kun knyttes til én dimension.
> - Et dimensionshierarki kan have ubegrænsede niveauer i strukturen. Alle niveauer bliver tilgængelige i arbejdsområdet **Omkostningsstyring**. Når du bruger Microsoft Excel eller Microsoft Power BI til rapporteringsformål, eksporteres kun de første 15 niveauer i dimensionshierarkiet. Denne begrænsning findes, fordi både Excel og Power BI kræver et fast skema.
> - Et dimensionshierarki er ikke datorelateret. Derfor gemmes enhver ændring i et dimensionshierarki til posten med det samme, og du kan ikke sammenligne før- og efter-datoen.

## <a name="dimension-hierarchy-type"></a>Dimensionshierarkitype

Når du opretter et nyt dimensionshierarki, skal du vælge en hierarkitype. Gå til **Omkostningsregnskab** > **Dimensioner** > **Dimensionshierarkier**. Klik på **Ny**, og vælg en dimensionshierarkitype. Du kan vælge enten **Kategoriseringshierarki for dimension** eller **Klassifikationshierarki for dimension**.

### <a name="dimension-categorization-hierarchy"></a>Kategoriseringshierarki for dimension

**Kategoriseringshierarki for dimension**-typen bruges til rapporteringsformål. Den understøtter kun omkostningselementdimensioner. Når du vælger denne type, gælder følgende regler:

-  Et dimensionsmedlem kan tilknyttes mere end én gang i den hierarkiske struktur.
-  Du kan placere et omkostningselements dimensionsmedlem i forskellige noder ved at tildele en omkostningsfunktionsmåde til bladnoden.

### <a name="dimension-classification-hierarchy"></a>Klassifikationshierarki for dimension

**Klassifikationshierarki for dimension**-typen bruges til at definere regler og til rapporteringsformål. Den understøtter alle dimensioner, f.eks. omkostningsobjekter, omkostningselementer og statistiske dimensioner. Når du vælger denne type, kan et dimensionsmedlem kun tilknyttes én gang i den hierarkiske struktur.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Oprette og vedligeholde et dimensionshierarki

Et dimensionshierarki oprettes som en træstruktur, der har node- og bladnoderelationer.

-  En node kan have 1:_n_ undernoder.
-  En node kan ikke have tilknyttet både undernoder og bladnoder.
-  En bladnode kan kun tildeles på det laveste niveau i hierarkiet.

### <a name="example"></a>Eksempel

Et lille firma har følgende organisationsstruktur, hvor Finans og Personale er afdelinger under Administration, og Samling og Emballage er afdelinger under Produktion.

![Eksempel på en organisationsstruktur](./media/dimension-hierarchy-org.png)

En omkostningsobjektdimension repræsenterer alle bærerne i organisationen.

- Dimension for omkostningsobjekt
    - Bærere

Den omkostningsobjektdimension, der repræsenterer alle bærerne, kan konfigureres som vist her.

| Bærere | Betegnelse |
|--------------|-------------|
| CC001        | Personale          |
| CC002        | Finans     |
| CC003        | Skat         |
| CC007        | Kreditor/Debitor       |
| CC005        | Samling    |
| CC006        | Emballage   |

En omkostningselementdimension repræsenterer alle omkostningselementerne i organisationen.

- Dimension for omkostningselement
    - Omkostningselementer

Den omkostningselementdimension, der repræsenterer alle omkostningselementerne, kan konfigureres som vist her.

| Omkostningselementer | Betegnelse |
|---------------|-------------|
| 10001         | Elektricitet |
| 10010         | Rengøring    |
| 10011         | Opvarmning     |
| 40001         | Vareforbrug        |

Et dimensionshierarki, der opfylder de organisatoriske rapporteringskrav, kan konfigureres som vist her.

**Detaljer om dimensionshierarki**

| Navn på dimensionshierarki | Dimension    | Navn på dimensionshierarkitype      | Adgangslistehierarki |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisation             | Bærere | Klassifikationshierarki for dimension | Nr.                    |

Dimensionshierarkiet til rapportering kan konfigureres som vist her.

|                   | Intervaller for dimensionsmedlemmer   |                         |
|-------------------|---------------------------|-------------------------|
| **Noder**         | **Fra dimensionsmedlem** | **Til dimensionsmedlem** |
| Organisation      |                           |                         |
| &nbsp;&nbsp;Administration         |                           |                         |
|&nbsp;&nbsp;&nbsp;&nbsp;Finans   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personale        | CC001                     | CC001                   |
| &nbsp;&nbsp;Produktion    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Emballage | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Samling  | CC006                     | CC006                   |

Et dimensionshierarki, der opfylder kravene i politikken, kan konfigureres som vist her.

**Detaljer om dimensionshierarki**

| Navn på dimensionshierarki | Dimension     | Navn på dimensionshierarkitype      |
|--------------------------|---------------|------------------------------------|
| Funktionalitet af omkostning            | Omkostningselementer | Klassifikationshierarki for dimension |

Dimensionshierarkiet til politikken kan konfigureres som vist her.

|                   | Intervaller for dimensionsmedlemmer   |                         |
|-------------------|---------------------------|-------------------------|
| **Noder**         | **Fra dimensionsmedlem** | **Til dimensionsmedlem** |
| Funktionalitet af omkostning     |                           |                         |
| &nbsp;&nbsp;Fast omkostning    | 10001                     | 10011                   |
|&nbsp;&nbsp;Variabel omkostning | 40001                     | 40010                   |

> [!NOTE]
> Under **Intervaller for dimensionsmedlemmer** kan en node indeholde 1:_n_ dimensionsmedlemsintervaller. Du kan indsætte dimensionsmedlem-id'er, der endnu ikke findes som medlemmer af dimensionen. Denne fremgangsmåde gør hierarkiet fleksibelt i fremtiden.  

### <a name="copy-a-hierarchy"></a>Kopiere et hierarki

Du kan kopiere et aktuelt dimensionshierarki som udgangspunkt for et nyt dimensionshierarki. Denne fremgangsmåde kan være nyttig, hvis du vil sammenligne det forrige dimensionshierarki med det nye.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Omarrangere noder i et hierarki

Du kan flytte en node op og ned inden for dens aktuelle niveau i strukturen. På denne måde kan du ændre rækkefølgen af noder til rapportering i arbejdsområdet **Omkostningsstyring**.

Du kan flytte en node til en ny placering i hierarkiet ved at markere målnoden. Noder kan flyttes på to måder:

- **Flyt under** – Flyt den markerede node fra den aktuelle placering i hierarkiet, og indsæt den **under** den valgte målnode.
- **Flyt efter** – Flyt den markerede node fra den aktuelle placering i hierarkiet, og indsæt den **efter** den valgte node på dens niveau i hierarkiet.

> [!NOTE] 
> Rækkefølgen af noderne vedligeholdes ikke, når du eksporterer data til Excel eller Power BI, fordi disse værktøjer bruger en alfanumerisk sorteringsrækkefølge som standard. Du skal ændre rækkefølgen manuelt.

## <a name="define-dimension-hierarchies-for-reporting"></a>Definere dimensionshierarkier for rapportering

Dimensionshierarkier er vigtige ved rapportering. Du kan bruge dem til at angive den specifikke struktur, som passer til den enkelte organisation. De aggregeringer, som foretages på nodeniveauet i dimensionshierarkiet, gør det muligt for interessenter på alle niveauer i organisationen at se data på alle niveauer.

Dimensionshierarkier er tilgængelige i følgende rapporteringsværktøjer. Denne fremgangsmåde er med til at sikre konsistens i rapporteringsstrukturen.

- Arbejdsområdet **Omkostningsstyring** (klient):

    - Styres af konfigurationen.

- Arbejdsområdet **Omkostningsstyring** (mobilprogram):

    - Styres af konfigurationen.

- Excel

    - Giver mulighed for at vælge bestemte dimensionshierarkier pr. eksportdefinition:

        - Ét dimensionshierarki for omkostningselement (obligatorisk)
        - Ét dimensionshierarki for omkostningselement (valgfrit)
        - Ét statistisk dimensionshierarki (valgfrit)

- Power BI:

    - Alle dimensionshierarkier er tilgængelige.
    
Hvis du opretter rapporter ved hjælp af Excel eller Power BI, eksporteres kun de første 15 niveauer i hierarkierne. Denne begrænsning findes, fordi der kræves et fast skema i Excel og Power BI. Hvis et hierarki har mere end 15 niveauer, eksporteres der ikke flere niveauer. Den normaliserede tabel indeholder en post for hvert dimensionsmedlem i hierarkiet. Der forekommer derfor automatisk aggregering. Denne funktionsmåde er med til at sikre, at saldi på ethvert af de 15 tilgængelige niveauer i hierarkiet stadig er korrekt.

Følgende eksempel viser, hvordan et dimensionshierarki kan se ud i rapporteringsstrukturen.

| Dimensionshierarki for omkostningsobjekt – niveau 1 | Dimensionshierarki for omkostningsobjekt – niveau 2 | Dimensionshierarki for omkostningsobjekt – niveau 3 | Dimensionshierarki for omkostningsobjekt – niveau 4 | Dimensionshierarki for omkostningsobjekt – niveau 15 |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organisation                              | Administration                                     | Finans                                   | CC002                                     |                                            |
| Organisation                              | Administration                                     | Finans                                   | CC003                                     |                                            |
| Organisation                              | Administration                                     | Finans                                   | CC007                                     |                                            |
| Organisation                              | Administration                                     | Personale                                        | CC001                                     |                                            |
| Organisation                              | Produktion                                | Emballage                                 | CC005                                     |                                            |
| Organisation                              | Produktion                                | Samling                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Opdatere de dimensionshierarkier, der bruges til rapportering 

Med tiden skal de dimensionshierarkier, der bruges i de tidligere nævnte rapporteringsværktøjer, opdateres. Du kan opdatere dimensionshierarkier ved at opdatere klienten.

- Arbejdsområdet **Omkostningsstyring** (klient)
- Arbejdsområdet **Omkostningsstyring** (mobilprogram)

Opdateringer til dimensionshierarkier hentes hver 24 timer af et job, der er cachelagret på forhånd. Når de eksporterede data er opdateret, er de opdaterede dimensionshierarkier tilgængelige i følgende værktøjer:

- Excel
- Power BI

> [!NOTE] 
> Du kan manuelt udløse en opdatering af dimensionshierarkiets cache ved at oprette en ny eksport til Excel for det eller de dimensionshierarkier, der skal opdateres.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Definere dimensionshierarkier for omkostningspolitikker

Omkostningsregnskab består af flere politikker, hvor der defineres detaljerede regler. Du skal definere et eller flere dimensionshierarkier for følgende politikker:

- Funktionalitet af omkostning
- Omkostningsfordeling
- Omkostningstildeling
- Omkostningstotaler

Dimensionshierarkier gør det nemt at oprette regler. For at undgå at skulle oprette regler for hvert dimensionsmedlem, kan du drage fordel af de aggregeringer af dimensionsmedlemmer, der leveres af dimensionshierarkiniveauer. Hvis du har overlappende regler, skal du definere specifikke regler, som systemet behandler, når det beregner de faste omkostninger.

### <a name="example-define-a-cost-behavior-policy"></a>Eksempel: Definere en politik for omkostningsfunktionalitet

Der oprettes en ny politik for omkostningsfunktionalitet, og relevante dimensionshierarkier tildeles politikken, som vist her.

**Politik for funktionalitet af omkostning**

| Navn på politik   | Dimensionshierarki for omkostningselement | Dimensionshierarki for omkostningsobjekt | Regnskabsvaluta |
|---------------|----------------------------------|---------------------------------|---------------------|
| Funktionalitet af omkostning | Funktionalitet af omkostning                    | Organisation                    | USD                 |

**Regler**

| Dimensionshierarkinode for omkostningselement | Dimensionshierarkinode for omkostningsobjekt | Fast procentdel | Fast beløb | Gyldig fra | Gyldig til |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Fast omkostning                            | Organisation                         | 100,00           | 0,00         | 1/1/2017   | Aldrig    |
| 10001                                 | Organisation                         | 0,00             | 150,00       | 1/1/2017   | Aldrig    |
| 10001 (\*)                             | Finans                              |                  | 50,00        | 1/1/2017   | Aldrig    |
| Funktionalitet af omkostning eller variabel omkostning (\*\*)   | Organisation                         | 0,00             | 0,00         | 1/1/2017   | Aldrig    |

\* Noden for variable omkostninger er ikke påkrævet. Hvis en omkostning ikke er klassificeret som en fast omkostninger, er den en variabel omkostning.

\*\* Der oprettes en detaljeret regel for kombinationen af omkostningselementmedlem 10001, og alle omkostningsobjektmedlemmer, der samles under Finans-hierarkiniveauet (CC002, CC003, CC007).

De foregående regler viser den fleksibilitet, som dimensionshierarkier giver. Ved at definere regler på højt niveau, kan du minimere vedligeholdelsen. Du kan derefter definere detaljerede regler, som passer til en bestemt forretningsmålsætning.

Hvis de dimensionshierarkier, der bruges i regler, opdateres, sender systemet automatisk opdateringerne videre.

Hvis et niveau af granularitet ikke længere kræves i reglerne, kan du lade reglen udløbe.

F.eks. er en regel for en specifik omkostningsfunktionsmåde for Finans-omkostningsobjektets dimensionshierarkinode ikke længere påkrævet. Derfor kan du klikke på **Lad regel udløbe** for at lade reglen udløbe.

| Dimensionshierarkinode for omkostningselement | Dimensionshierarkinode for omkostningsobjekt | Fast procentdel | Fast beløb | Gyldig fra | Gyldig til  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Fast omkostning                            | Organisation                         | 100,00           | 0.00         | 1/1/2017   | Aldrig     |
| 10001                                 | Organisation                         | 0.00             | 150,00       | 1/1/2017   | Aldrig     |
| 10001                                 | Finans                              |                  | 50,00        | 1/1/2017   | 20/1/2017 |
| Funktionalitet af omkostning eller variabel omkostning        | Organisation                         | 0.00             | 0.00         | 1/1/2017   | Aldrig     |

Alle beregninger af faste omkostninger, der køres efter den 20. januar 2017, anvender ikke længere denne regel.

> [!NOTE] 
> Felterne **Gyldig fra** og **Gyldig til** er dato- og klokkeslætsrelaterede. Du kan lade reglen udløbe og køre en ny beregning af faste omkostninger samme dag.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Definere dimensionshierarkier for sikkerhedsopsætning

Data i Omkostningsregnskab skal gøres tilgængelige for alle ledere, der er ansvarlige for en rapporteringsenhed. I omkostningsregnskabets terminologi repræsenteres en rapporteringsenhed som et omkostningsobjekt eller en række omkostningsobjekter.

Potentielt skal alle ledere kunne få adgang til følsomme forretningsoplysninger som f.eks. indtægter og margener. Det er derfor vigtigt, at du konfigurerer sikkerhed, så lederne kun kan se de data, der er relevante for dem. Af hensyn til datasikkerheden skal du definere dimensionshierarkier.

- Brugen af dimensionshierarkier gælder kun, når den dimensionsværdi, der er valgt i referencen til dimensionshierarkiet, er en omkostningsobjektdimension.
- Der kan kun aktiveres ét dimensionshierarki pr. omkostningsobjektdimensionen i adgangslistehierarkiet.

**Detaljer om dimensionshierarki**

| Navn på dimensionshierarki | Dimension    | Navn på dimensionshierarkitype      | Adgangslistehierarki |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisation             | Bærere | Klassifikationshierarki for dimension | **Ja**               |

Et nyt oversigtspanel **Brugere** er tilgængeligt i hierarkidesigneren. Her kan du indsætte et eller flere bruger-id'er på hver node i hierarkiet.

|                 | Brugere            | Intervaller for dimensionsmedlemmer   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| **Noder**       | **Bruger-id**      | **Fra dimensionsmedlem** | **Til dimensionsmedlem** |
| Organisation    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Administration         | April            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans   | Alicia           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personale        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Produktion    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Emballage | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Samling  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Bogholdere skal tildeles til det øverste niveau i hierarkiet, så de kan se alle poster i omkostningsregnskabet.

Du kan aktivere adgangslistehierarkiet og de tilhørende sikkerhedsindstillinger ved at gå til **Omkostningsregnskab** > **Opsætning** > **Parametre** > **Generelt**. Vælg parameteren **Aktivér læseadgang for dimensionsmedlemmer for omkostningsobjekt**.

Indstillingerne for adgangslistehierarkiet bruges til at styre, hvilke data der vises i følgende områder:

- Arbejdsområdet **Omkostningsstyring** (klient):

    - Data i formularer, der bruges til at gennemgå scenarier

- Arbejdsområdet **Omkostningsstyring** (mobilprogram):

    - Saldi i kort

- Power BI:

    - Data, der vises i Power BI-visualiseringer
    - Data Power BI-visualiseringer, der er integreret i Dynamics 365 Finance-klienten

> [!NOTE] 
> - Før adgangslistehierarkiet kan påvirke dataene i Power BI, skal adgangslistehierarki og sikkerhed på rækkeniveau i Power BI kombineres. Du kan finde flere oplysninger i [Konfigurere sikkerhed for indholdspakke til omkostningsregnskab](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Adgangslistehierarkiet bidrager ikke til at beskytte eksport af data til Excel. Derfor skal dette rapporteringsværktøjet kun bruges af bogholdere og ledere, der skal have fuld adgang til at se dataene.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]