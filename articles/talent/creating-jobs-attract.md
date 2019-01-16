---
title: "Oprette, godkende og bogføre job i Attract"
description: "I dette emne beskrives elementerne i et job i Attract. Det beskrives også, hvordan du opretter et job."
author: josaw
manager: AnnBe
ms.date: 12/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 6c5daa4050d63303f1ac10c24901e5b1182cb62b
ms.contentlocale: da-dk
ms.lasthandoff: 12/23/2018

---

# <a name="create-approve-and-post-jobs-in-attract"></a>Oprette, godkende og bogføre job i Attract

[!include [banner](includes/banner.md)]

I dette emne beskrives elementerne i et job i Microsoft Dynamics 365 for Talent: Attract. Det beskrives også, hvordan du opretter et job.

## <a name="job-creation"></a>Oprettelse af job

Administratorer, rekrutteringsmedarbejdere og ansættelsesansvarlige kan oprette job. Når du opretter et job, bliver du bedt om at vælge din rolle i processen: ansættelsesansvarlig eller rekrutteringsmedarbejder. Når du har valgt en rolle, du bliver bedt om at vælge en processkabelon. Hvis du vælger **Spring over**, bruges standardskabelonen. Du kan finde flere oplysninger om processkabeloner i [Oprette en processkabelon i Attract](./process-templates-attract.md).

Et job i Attract indeholder joboplysninger, et ansættelsesteam, en ansættelsesproces, jobopslag og analyser.

## <a name="job-details"></a>Jobdetaljer

Fanen **Jobdetaljer** indeholder oplysninger om jobbets ansvarsområder og attributter. Felterne for stillingsbetegnelsen, stillingsbeskrivelse og jobstedet er påkrævet. De øvrige felter er valgfrie.

Som standard er feltet **Antal ledige stillinger** indstillet til **1**. Du kan imidlertid ændre værdien. Når der er udarbejdet et jobtilbud, og reduceres værdien i feltet **Antal tilgængelige åbninger**.

Hvis Styring af stillinger er aktiveret i Administration, er opslaget **Opdater stillinger** tilgængeligt. Dette opslag læser JobPosition-enheden i Common Data Service for Apps og returnerer en liste over stillinger, der kan vælges til jobbet. Hvis det antal stillinger, du vælger, overstiger antallet af ledige stillinger, modtager du en advarsel. Der kan også vises en advarsel, hvis en stilling bruges i flere job.

> [!NOTE]
> Styring af stillinger er tilgængelig i tilføjelsesprogrammet til omfattende ansættelser.

Afhængigt af indstillingerne for tilbudsaktiviteten i ansættelsesprocessen kan et stillingsnummer bruges to gange i et tilbud. Du kan finde flere oplysninger under [Ansættelsesproces](./activities-attract.md).

Attract indeholder et standardsæt af **Færdigheder**. Disse færdigheder vises som forslag, når du skriver. Du kan tilføje flere færdigheder ved at angive den nye tekst om færdigheder i feltet og derefter trykke på Enter.

Attract indeholder et standardsæt af **Jobfunktioner**. Du kan tilføje op til tre jobfunktioner yderligere ved at angive den nye jobfunktion i feltet og derefter trykke på Enter.

Attract indeholder et **Firmas branche**-standardsæt. Du kan tilføje op til tre firmabrancher yderligere ved at angive den nye firmabranche i feltet og derefter trykke på Enter.

## <a name="hiring-team"></a>Ansættelsesteam

Fanen **Ansættelsesteam** indeholder listen over de personer, der har med jobbet at gøre. Når der føjes brugere til et ansættelsesteam, skal de tildeles en rolle i teamet. Rollen bestemmer, hvilke data brugerne har adgang til, og hvilke beskeder de modtager. De roller, der kan vælges, er **Rekrutteringsmedarbejder**, **Ansvarlig for ansættelse**, **Delegeret** og **Interviewer**. Du kan finde flere oplysninger om rollerettigheder i dokumentet "Rollestyring". Rekrutteringsmedarbejdere og ansættelsesansvarlige kan udpege en eller flere delegerede, som må arbejde på deres vegne. Du kan finde flere oplysninger om delegerede i [Sikkerheds- og rollestyring i Attract](./security-attract.md).

Ansættelsesteamet kan opdateres, når jobbet er blevet aktiveret.

## <a name="process"></a>Proces

Standardoplysningerne om ansættelsesprocessen er baseret på den processkabelon, der blev valgt, da jobbet blev oprettet. Hvis der ikke var valgt en bestemt skabelon på tidspunktet, bruges standardskabelonen. Når du definerer ansættelsesprocessen, kan du tilføje eller fjerne forskellige stadier undtagen Jobkandidat, Ansøgning og Tilbud. Selvom stadiet Jobkandidat ikke kan fjernes, kan det deaktiveres. Du kan tilføje eller fjerne en eller flere foruddefinerede aktiviteter på hvert stadie.

Du kan finde flere oplysninger om aktiviteter, der kan føjes til ansættelsesprocessen, i [Ansættelsesprocesaktiviteter i Attract](./activities-attract.md).

> [!NOTE]
> Ansættelser via processer kan ikke opdateres, når et job er blevet aktiveret.

## <a name="postings"></a>Opdateringer

Når et job er aktiveret, kan det slås op. Kun rekrutteringsmedarbejdere og administratorer kan oprette jobopslag. Jobbet kan opslås på enten Talent Careers (et Microsoft Dynamics 365 for Talent-karrierewebsted) eller LinkedIn. 

> [!NOTE]
> Der er tre ting, der er vigtige at bemærke om, hvordan job opslås på LinkedIn.
> 1. Job, der opslås på LinkedIn, opslås som "Begrænsede lister"-job. Begrænsede listejob kan ikke opgraderes på tværs af LinkedIn-webstedet. Hvis du vil opgradere begrænsede listejob, der er slået op på LinkedIn, fra Attract, skal du arbejde med LinkedIn for at aktivere "Job-wrapping". Se nedenstående links, og kontakt LinkedIn support for at få yderligere oplysninger.
>
>    [Begrænsede lister kontra Premium-jobmuligheder til job-wrapping](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping)
>
>    [Ofte stillede spørgsmål om job-wrapping](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)
>
> 1. Når du slår job op på LinkedIn, overfører Attract Microsoft 365 organisationens navn til jobbet. LinkedIn sammenkæder jobbene med en virksomhed på LinkedIn-siden baseret på navnet på den organisation, der overføres. Hvis jobbet står ved den forkerte virksomhed på LinkedIn, kan du kontrollere, at Microsoft 365-organisationens navn svarer til virksomhedsnavnet på LinkedIn.  
>
>    [Rediger adresse, kontakt og meget mere](https://docs.microsoft.com/en-us/office365/admin/manage/change-address-contact-and-more)
>
>    Hvis du har problemer efter dette trin, skal du kontakte LinkedIn support. 
> 
> 1. Det kan tage op til 24 timer, før job, der er slået op på LinkedIn, bliver synlige for ansøgerne på LinkedIn, på grund af LinkedIns aktuelle proces for jobopslag.

Attract-teamet skaber løbende partnerskaber med jobsamlingswebsteder. Denne liste udvides over tid.

Du kan finde flere oplysninger om jobopslag i [Funktioner for karrierewebsteder i Attract](./career-site.md).

> [!NOTE]
> Jobopslagsfunktionerne er kun tilgængelige i tilføjelsesprogrammet til omfattende ansættelser til Attract.

## <a name="activate"></a>Aktivér

Når et job er aktiveret, kan det slås op, og jobkandidater og ansøgere kan føjes til det. Muligheden for at tilføje kandidater til et job angives i Jobkandidat-aktiviteten i ansættelsesprocessen.

> [!NOTE]
> Ansættelser via processer kan ikke opdateres, når et job er blevet aktiveret.

## <a name="prospects-and-applicants"></a>Jobkandidater og ansøgere

Muligheden for at tilføje kandidater til et job angives i [Jobkandidat-aktiviteten](./activities-attract.md#prospect-activity) i ansættelsesprocessen. Denne indstilling skal konfigureres, før du aktiverer jobbet. Når et job er aktiveret, kan jobkandidater og ansøgere føjes til det.

## <a name="approvals"></a>Godkendelser

Job i Attract kan sendes til godkendelse. Ikke alle job skal godkendes. Kravet angives på skabelonniveau. Godkendelser er som standard slået fra i skabelonen. Hvis du vil konfigurere godkendelser, skal du gå til en processkabelon og indstille feltet **Godkendelse** til Standard. Vælg derefter skabelonen, når du opretter jobbet.

Når et job er gemt, kan det sendes til godkendelse. Følgende tabel indeholder statusserne for et dokument, der bruger godkendelser.

| Status   | Status                                                               |
|----------|---------------------------------------------------------------------|
| Udkast    | Jobbet er blevet gemt, men er endnu ikke er sendt til en arbejdsgang. |
| Afventer  | Jobbet er sendt til godkendere.                            |
| Godkendt | Jobbet er blevet godkendt, men er endnu ikke aktiveret.            |
| Afvist | Jobbet er blevet afvist og kan ikke aktiveres.               |
| Aktive   | Jobbet er godkendt og aktiveret.                            |

Du kan filtrere på jobstatusser på joblisten.

Godkendelser kan sendes til enhver Azure AD-bruger (Microsoft Azure Active Directory) i firmaet. Godkendelserne sendes parallelt til alle personer, der er angivet som godkendere. Når et job er godkendt, kan det aktiveres.

De personer, der er angivet som godkendere, modtager en besked i Attract med oplysning om, at et element skal godkendes. Der vises også en godkendelsesbesked i sektionen **Tildelt til dig** i dashboardet. Når nogen accepterer eller godkender et job, modtager ansættelsesteamet en besked. Endelig modtager teamet en besked, når jobbet er godkendt.

## <a name="create-a-job"></a>Oprette et job

Følg denne fremgangsmåde for at oprette et job.

1. Gå til **Job**.
2. Vælg **Ny**.
3. I feltet **Stillingsbetegnelse** skal du angive jobbetegnelsen. Angiv din rolle i feltet **Rolle**.
4. I feltet **Skabelon** skal du vælge en skabelon. Du kan også vælge **Spring over**. Hvis du vælger **Spring over**, bruges den skabelon, der er markeret som standardskabelon.

    Hvis dokumentet skal gennemgå en godkendelsesproces, skal du vælge en skabelon, hvor feltet **Godkendelsesproces** er indstillet til **Standard**.

5. Angiv detaljerne for jobbet under fanen **Detaljer**. Felterne **Stilling**, **Stillingsbeskrivelse** og **Sted** er obligatoriske.
6. Vælg **Gem**.
7. Under fanen **Ansættelsesteam** skal du tilføje en ansættelsesansvarlig, rekrutteringsmedarbejder eller interviewer.
8. Vælg **Gem**.
9. Under fanen **Proces** skal du tilføje eller fjerne stadier efter behov:

    - For at tilføje et stadie skal du vælge **+ Nyt stadie**.
    - Hvis du vil fjerne et stadie, skal du placere markøren over stadiet, der skal fjernes, og derefter vælge den papirkurvsknap, der vises.

        > [!NOTE]
        > Stadierne Jobkandidat, Ansøgning og Tilbud kan ikke fjernes.

10. Tilføj eller fjern aktiviteter efter behov:

    - Hvis du vil tilføje en aktivitet, skal du trække den fra listen til højre til det relevante stadie. Du kan også dobbeltklikke på aktiviteten og derefter vælge det stadie, den skal føjes til.
    - Hvis du vil fjerne en aktivitet, skal du udvide aktiviteten og derefter vælge papirkurvsknappen i overskriften til aktiviteten.

11. Vælg **Gem**.
12. Hvis du har valgt at bruge en godkendelsesproces, skal du følge disse trin:

    1. Vælg **+ Tilføj godkender**, og angiv derefter en bruger, der har en Azure AD-konto. Du kan tilføje flere godkendere.
    2. Vælg **Send til godkendere**.

    Feltet **Jobstatus** for jobbet indstilles til **Afventer**. Når værdien i feltet **Jobstatus** ændres til **Godkendt**, kan jobbet aktiveres.

13. For at aktivere jobbet skal du vælge **Aktivér**.
14. Du kan slå jobbet op ved at gå til **Opslag** og derefter vælge **Slå op nu** på Talent-karrierewebstedet eller LinkedIn.

