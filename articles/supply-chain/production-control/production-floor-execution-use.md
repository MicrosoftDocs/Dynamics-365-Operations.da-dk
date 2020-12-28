---
title: Sådan bruges grænsefladen til kørsel af produktionsudstyr af arbejdere
description: Dette emne beskriver, hvordan grænsefladen til kørsel af produktionsudstyr anvendes af arbejderne.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 40c6794fdf25da44a75aba4a502a89966c0ec4d0
ms.sourcegitcommit: f27f5d07c040bdca1bcd616f5d3f2320d3b3337e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/15/2020
ms.locfileid: "4424938"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Sådan bruges grænsefladen til kørsel af produktionsudstyr af arbejdere

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Grænsefladen til kørsel af produktionsudstyr er blevet optimeret med berøringsinteraktion. Designet giver en visuel kontrast, der lever op til tilgængelighedskravene i produktionsmiljøer. Det har de samme funktionelle egenskaber som jobkortenheden. Det betyder imidlertid også, at flere job kan startes parallelt fra en jobliste. (Denne egenskab kaldes også *job i bundter*). Arbejderne kan også på en jobliste åbne en guide, der er oprettet i vejledningen til Microsoft Dynamics 365. På denne måde kan de få visuelle instruktioner på en HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Logge på grænsefladen til kørsel af produktionsudstyr som arbejder

Før arbejdere kan begynde at bruge enheden, skal en supervisor eller teknisk personale klargøre den og åbne den korrekte side i Dynamics 365 Supply Chain Management. Du kan finde flere oplysninger om, hvordan du konfigurerer enheden, under [Konfigurere en enhed til at køre grænsefladen på produktionsudstyr](production-floor-execution-setup.md).

Når enheden er blevet forberedt, vises logonsiden. På denne side vises oplysninger om status for job i den lokale arbejdscelle. Disse oplysninger opdateres jævnligt. På siden bruger arbejderne deres badge-id'er, når de logger på. Selvom arbejderne ikke behøver at have en brugerkonto til Supply Chain Management, skal de have en *tidsregistreret arbejder*-konto, som de kan bruge, når de logger på.

![Logonside i grænseflade til kørsel af produktionsudstyr](media/pfei-sign-in-page.png "Logonside i grænseflade til kørsel af produktionsudstyr")

I de resterende afsnit af dette emne beskrives, hvordan arbejderne kan interagere med grænsefladen.

## <a name="all-jobs-tab"></a>Fanen Alle job

Under fanen **Alle job** kan du se en jobliste med alle de produktionsjob, der har statussen *Ikke startet*, *Stoppet* eller *Startet*.

![Fanen Alle job](media/pfei-all-jobs-tab.png "Fanen Alle job")

Joblisten har følgende kolonner. (Tallene svarer til tallene i ovenstående illustration).

1. **Udvælgelseskolonne** – Kolonnen længst til venstre bruger markeringer til at angive job, der er valgt af arbejderen. Arbejderne kan vælge flere job på listen på samme tid. Hvis du vil vælge alle job på listen, skal du markere afkrydsningsfeltet i kolonneoverskriften. Når der vælges et enkelt job, vises oplysninger om jobbet på den nederste del af siden.
1. **Kolonnen Jobstatus** – I denne kolonne bruges symboler til at angive status for hvert job. Job, der ikke har et symbol i denne kolonne, har statussen *Ikke startet*. En grøn trekant angiver job, der har statussen *Startet*. To gule lodrette linjer angiver job, der har statussen *Stoppet*.
1. **Kolonnen Høj prioritet** – I denne kolonne bruges udråbstegn til at angive job med høj prioritet.
1. **Ordre** – Denne kolonne viser produktionsordrenummeret for et job.
1. **Beskrivelse** – I denne kolonne vises en beskrivelse af den handling, som et job er en del af.
1. **Anmodet** – I denne kolonne vises det antal, som et job ifølge planen skal producere.
1. **Påbegyndt** – I denne kolonne vises det antal, der allerede er påbegyndt for et job.
1. **Fuldført** – I denne kolonne vises det antal, der allerede er fuldført for et job.
1. **Kasseret** – I denne kolonne vises det antal, der allerede er kasseret for et job.
1. **Resterende** – I denne kolonne vises det antal, der mangler at blive fuldført for et job.

## <a name="active-jobs-tab"></a>Fanen Aktive job

![Fanen Aktive job](media/pfei-active-jobs-tab.png "Fanen Aktive job")

Joblisten under fanen **Aktive job** har følgende kolonner:

- **Udvælgelseskolonne** – Kolonnen længst til venstre bruger markeringer til at angive job, der er valgt af arbejderen. Arbejderne kan vælge flere job på listen på samme tid. Hvis du vil vælge alle job på listen, skal du markere afkrydsningsfeltet i kolonneoverskriften. Når der vælges et enkelt job, vises oplysninger om jobbet på den nederste del af siden.
- **Ordre** – Denne kolonne viser produktionsordrenummeret for et job.
- **Beskrivelse** – I denne kolonne vises en beskrivelse af den handling, som et job er en del af.
- **Anmodet** – I denne kolonne vises det antal, som et job ifølge planen skal producere.
- **Påbegyndt** – I denne kolonne vises det antal, der allerede er påbegyndt for et job.
- **Fuldført** – I denne kolonne vises det antal, der allerede er fuldført for et job.
- **Kasseret** – I denne kolonne vises det antal, der allerede er kasseret for et job.
- **Resterende** – I denne kolonne vises det antal, der mangler at blive fuldført for et job.

## <a name="starting-and-completing-production-jobs"></a>Start og fuldførelse af produktionsjob

Arbejderne starter et produktionsjob ved at vælge et job under fanen **Alle job** og derefter vælge **Start job** for at åbne dialogboksen **Start job**.

![Dialogboksen Start job](media/pfei-start-job-dialog.png "Dialogboksen Start job")

Arbejderne bruger dialogboksen **Start job** til at bekræfte produktionsantallet og derefter starte jobbet. De kan justere antallet ved at markere feltet **Antal** og derefter bruge det numeriske tastatur, der vises. De vælger derefter **Start** for at begynde at arbejde på jobbet. Dialogboksen **Start job** lukkes, og jobbet føjes til fanen **Aktive job**.

Arbejderne kan starte et job med en hvilken som helst status. Når en arbejder starter et job, der har statussen *Ikke startet*, viser feltet **Antal** i dialogboksen **Start job** det samlede antal som udgangspunkt. Når en arbejder starter et job, der har statussen *Startet* eller **Stoppet**, viser feltet *Antal* som udgangspunkt det resterende antal.

## <a name="reporting-good-quantities"></a>Rapportering af antal gode

Når en arbejder fuldfører eller delvist fuldfører et job, kan han eller hun rapportere antal gode, der er produceret, ved at vælge et job under fanen **Aktive job** og derefter vælge **Rapportér status**. Derefter angiver arbejderen antallet af gode ved at bruge det numeriske tastatur i dialogboksen **Rapportér status**. Antallet er som standard tomt. Når der er angivet et antal, kan arbejderen opdatere status for jobbet til *I gang*, *Stoppet* eller *Fuldført*.

![Dialogboksen Rapportér status](media/pfei-report-progress-dialog.png "Dialogboksen Rapportér status")

## <a name="reporting-scrap"></a>Rapportering af spild

Når en arbejder fuldfører eller delvist fuldfører et job, kan han eller hun rapportere spild ved at vælge et job under fanen **Aktive job** og derefter vælge **Rapportér spild**. Derefter angiver arbejderen spildantallet ved at bruge det numeriske tastatur i dialogboksen **Rapportér spild**. Arbejderen vælger også en årsag (*Ingen*, *Maskine*, *Operatør* eller *Materiale*).

![Dialogboksen Rapportér spild](media/pfei-report-scrap-dialog.png "Dialogboksen Rapportér spild")

## <a name="completing-a-job-and-starting-a-new-job"></a>Fuldførelse af et job og start af et nyt job

Normalt fuldfører arbejderne et job ved at vælge et eller flere aktuelle job under fanen **Aktive job** og derefter vælge **Rapportér status**. Derefter angiver de det antal, der er produceret (antal gode), og indstiller status til *Fuldført*. Hvis der er valgt mere end ét job, bruger arbejderen derefter knapperne **Forrige** og **Næste** til at flytte mellem dem. For at starte et nyt job skal arbejderen vælge det under fanen **Alle job** og derefter vælge **Start job**.

En arbejder kan også starte et nyt job, mens det forrige job stadig er åbent. Arbejderen vælge igen det nye job under fanen **Alle job** og vælger derefter **Start job**. Denne gang indeholder dialogboksen **Start job** dog oplysninger til arbejderen om, at han aktuelt arbejder på et job, som han derfor enten skal stoppe eller fuldføre, før han starter det nye job.

## <a name="working-on-multiple-jobs-in-parallel"></a>Arbejde med flere job parallelt

En arbejder kan arbejde på flere job på samme tid (dvs. parallelt). I dette tilfælde kaldes den samling job, som arbejderen arbejder på, for et *jobbundt*. Arbejderen kan føje nye job til bundtet eller fuldføre et eller flere job i bundtet. I følgende to scenarier vises, hvordan en arbejder kan arbejde på job parallelt.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Scenarie 1: En arbejder, der ikke har aktive job, vil gerne starte to job og arbejde på dem parallelt

Arbejderen vælger de to job under fanen **Alle job** og vælger derefter **Start job**. I dialogboksen **Start job** vises begge valgte job, og arbejderen kan justere antallet for at starte på hvert job. Arbejderen bekræfter derefter dialogboksen og kan starte begge job.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Scenarie 2: En arbejder, der har to aktive job, som er i gang, vil starte et tredje job og arbejde på det parallelt med de to andre

Arbejderen vælger det tredje job under fanen **Alle job** og vælger derefter **Bundt**. I dialogboksen **Bundt** kan arbejderen justere det antal, der skal startes. Arbejderen bekræfter derefter dialogboksen ved at vælge **Bundt**.

## <a name="working-on-indirect-activities"></a>Arbejde på indirekte aktiviteter

Indirekte aktiviteter er aktiviteter, der ikke er direkte relateret til en produktionsordre. Indirekte aktiviteter kan defineres fleksibelt, som beskrevet i [Konfigurere indirekte aktiviteter for tid og fremmøde](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Shannon, som arbejder i produktionsanlægget hos Contoso, ønsker f.eks. at deltage i et firmamøde, og møder betragtes som en indirekte aktivitet. Et af følgende to scenarier er relevant:

- **Shannon arbejder på et eller flere aktive job.** Hun vælger **Aktivitet**, identificerer aktiviteten (møde) og bekræfter sit valg. Der vises en meddelelse om, at hun har igangværende job. Fra meddelelsen kan hun vælge at fuldføre eller stoppe de job, som hun arbejder på, før hun går til mødet.
- **Shannon har ingen aktive job.** Hun vælger **Aktivitet**, identificerer aktiviteten (møde) og bekræfter sit valg. Det er nu registreret, at hun er til møde.

I begge scenarier, går Shannon, efter at have bekræftet sit valg, enten til logonsiden eller en side, hvor hun skal bekræfte, at hun er returneret, når hun er tilbage fra sin indirekte aktivitet. Hvilken side der vises afhænger af konfigurationen af grænsefladen til kørsel af produktionsudstyr. (Yderligere oplysninger finder du i [Konfigurere grænsefladen til kørsel af produktionsudstyr](production-floor-execution-configure.md)).

## <a name="working-on-breaks"></a>Arbejde med pauser

Arbejderne kan registrere pauser. Pauser kan defineres fleksibelt, som det er beskrevet i [Løn på basis af registreringer](pay-based-on-registrations.md).

En arbejder registrerer en pause ved at vælge **Pause** og derefter vælge det kort, der repræsenterer pausetypen (f.eks. frokost). Når arbejderen har bekræftet sit valg, viser enheden enten logonsiden eller en side, hvor arbejderen skal bekræfte, at han eller hun er returneret fra pausen. Hvilken side der vises afhænger af konfigurationen af grænsefladen til kørsel af produktionsudstyr. (Yderligere oplysninger finder du i [Konfigurere grænsefladen til kørsel af produktionsudstyr](production-floor-execution-configure.md)).

## <a name="opening-instructions"></a>Åbningsinstruktioner

Arbejderne kan åbne et dokument, der er knyttet til et job, ved at vælge **Instruktioner**. Knappen **Instruktioner** er kun tilgængelig, hvis der er knyttet et dokument til jobbet i masterdataene. Et dokument, der er vedhæftet til et produkt på siden **Frigivne produkter** i Supply Chain Management, vil f.eks. kunne åbnes af arbejderne i kørselsgrænsefladen til produktionsudstyret.

## <a name="opening-mixed-reality-guides-for-hololens"></a>Åbning af Mixed Reality-guider til HoloLens

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) kan øge arbejdernes muligheder ved hjælp af praktisk læring, som bygger på Mixed Reality. Du kan definere standardiserede processer, hvor trinvise instruktioner indfører arbejderne i de værktøjer og dele, de har brug for, og viser dem, hvordan de kan bruge disse værktøjer i faktiske arbejdssituationer. Her er en oversigt over processen.

1. Hver gang en arbejder åbner en jobliste i kørselsgrænsefladen til produktionsudstyret, finder grænsefladen alle relevante guider til de viste job.
1. Arbejderen vælger **Guides** for at få vist listen over guider.
1. Arbejderen vælger en relevant guide på listen.
1. Grænsefladen til kørsel af produktionsudstyret viser en QR-kode for den valgte guide.
1. Arbejderen ifører sig en HoloLens og ser på QR-koden for at starte guiden.
1. Arbejderen arbejder sig igennem guiden for at lære at udføre opgaven.

Du kan finde flere oplysninger om, hvordan du opretter, tildeler og bruger guider til HoloLens, under [Levere Mixed-Reality-vejledninger til arbejdere i produktion](instruction-guides-in-production-overview.md).
