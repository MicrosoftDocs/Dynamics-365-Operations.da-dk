---
title: Funktioner for karrierewebsteder i Attract
description: Denne artikel indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/13/2019
ms.locfileid: "389954"
---
# <a name="career-site-functionality-in-attract"></a>Funktioner for karrierewebsteder i Attract

[!include[banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Microsoft Dynamics 365 for Talent: Attract. I artiklen beskrives også, hvordan du konfigurerer denne funktion.

Attract indeholder ét karrierewebsted for hvert miljø i en lejer. F.eks. hvis en organisation har et miljø til udvikling og et testmiljø, klargøres ét karrierewebsted til udviklingsmiljøet og et andet til testmiljøet. Hvert karrierewebsted er fuldstændigt isoleret og har sit eget system til godkendelse. Job- og kandidatprofiler deles ikke mellem karrierewebstederne.

Som standard er karrierewebstedet offentligt. Derfor kan kandidater få vist alle job, der er markeret som eksterne, uden at skulle logge på. Alle andre handlinger kræver dog, at kandidaterne er logget på.

## <a name="career-site-management"></a>Administration af karrierewebsted

For at angive værdierne for følgende elementer skal brugeren logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** (tandhjulsymbolet) og derefter vælge fanen **Firmaoplysninger**.

-   **Organisationsnavn** - Organisationens navn vises på navigationslinjen øverst i karrierewebstedet. Hvis kandidaterne vælger organisationsnavnet, kommer de til en side over alle ledige job.

-   **Organisationslogo** - Et billede af organisationens logo vises øverst til venstre på karrierewebstedet. Hvis kandidaterne vælger logobilledet, kommer de til en side over alle ledige job.

    >   [!NOTE] 
    >   Logobilledet, der vises på karrierewebstedet, har en fast højde på 20 pixel (px). Det billede, du føjer til Administration, skaleres, så det passer i størrelsen. Afhængigt af billedet kan bredden evt. blive ændret.
 
For at angive værdierne for følgende elementer skal brugeren logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** og derefter vælge fanen **Administration af karrierewebsted**.

-   **Optimering af søgemaskine** – Når denne indstilling er aktiveret, kan der søges i alle offentlige job, der opslås på Attract-karrierewebstedet, ved hjælp af søgemaskiner som Bing og Google.

    >   [!NOTE] 
    >   Der kan være en forsinkelse fra denne indstilling aktiveres, til søgeresultater vises, afhængigt af hvilken søgemaskine du bruger.
         
## <a name="career-site-urls"></a>URL-adresser til karrierewebsteder

Følgende liste indeholder de almindeligt anvendte karrierewebsteders URL-adresser, og hvordan du får adgang til dem.

-   **URL-adresse til startside for karrierewebsted** - Hvis du vil have vist URL-adressen til startsiden for karrierewebstedet, skal du logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** og derefter vælge fanen **Administration af karrierewebsted**.

-   **URL-adresse til ansøgning om individuelt jobopslag** - Når du [slå et eksternt job op](Creating-jobs-Attract.md#postings) for første gang, kan du kopiere linket **Ansøg** fra programmet Attract. URL-adressen til dette link har følgende format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **URL-adresse til individuelt jobopslag** - URL-adressen til jobopslaget er en understreng af URL-adressen til ansøgningen. Den består af alt op til og med jobnummeret. Derfor, for den foregående URL-adresse til ansøgning, er URL-adressen til jobopslaget [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)

## <a name="authentication-options"></a>Godkendelsesindstillinger

Kandidaterne har følgende logonmuligheder for et Attract-karrierewebsted:

-   Personlig konto:

    -   LinkedIn

    -   Microsoft

    -   Google

    -   Facebook

-   Arbejds- eller skolekonto:

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD-logon er kun beregnet til interne kandidater. Derfor fungerer det kun for interne kandidater, der bruger deres firmas Azure AD-legitimationsoplysninger. F.eks. ønsker en kandidat, der aktuelt er medarbejder hos Contoso, Ltd, at ansøge om et job i en ikke-relateret virksomhed, Alpine Ski House. I dette tilfælde kan medarbejderen ikke logge på, hvis han eller hun forsøger at bruge sine Azure AD-legitimationsoplysninger fra Contoso Ltd.

## <a name="create-and-maintain-a-profile"></a>Oprette og vedligeholde en profil

Når kandidater har logget på karrierewebstedet, kan de vælge **Min profil** på navigationslinjen øverst på siden for at oprette og vedligeholde deres profil.
Profilen indeholder personlige oplysninger, oplysninger om arbejdserfaring og uddannelse, dokumenter, links og oplysninger om færdigheder. Når en profil er oprettet, kan den bruges til at ansøge om job, som kandidaten er interesseret i. Profiler hjælper også Attract med at anbefale de rigtige job til kandidater.

>   [!NOTE]
>   Hvis en kandidat bruger et e-mail-id til at logge på ved hjælp af en af godkendelsesudbyder, der er angivet ovenfor, anvendes standardkontaktens e-mail-id, der er knyttet til profilen. Id'et kan dog ændres når som helst og er helt uafhængigt af det første id. Attract bruger altid det kontakt-e-mail-id'et, der skal knyttes til din profil, til al e-mailkommunikation.

## <a name="find-the-right-job"></a>Finde det rette job

På joblistesiden kan kandidaterne søge efter et bestemt job ved at indtaste søgeord. Søgefunktionen leder efter søgeord i stillingsbetegnelser og jobbeskrivelser og viser de relevante job som resultat. Kandidaterne kan filtrere resultaterne når som helst baseret på jobstedet eller jobfunktionen.

Kandidaterne kan også se en række anbefalede job på karrierewebstedet. Hvilke job der anbefales til en kandidat, afhænger af kandidatens tidligere ansøgninger, profil og CV'er.

>   [!NOTE] 
>   Jobanbefalinger vises kun, hvis der er opslået mindst 10 job på karrierewebstedet, og hvis kandidaten har fuldført en profil.

## <a name="apply-for-jobs"></a>Ansøge om job

Når kandidaterne har fundet det rigtige job, kan de ansøge ved hjælp af knappen **Ansøg** på siden med **Jobdetaljer**. På dette tidspunkt kan ansøgerne enten oprette en ny profil eller gennemse oplysningerne i deres eksisterende profil.
De kan også overføre et CV efter behov og derefter sende jobansøgningen.

## <a name="check-application-status"></a>Kontrollere ansøgningsstatus

Når kandidaterne har ansøgt om et eller flere job, kan de vælge **Ansøgninger** på navigationslinjen øverst på siden for at få vist deres åbne og lukkede ansøgninger. Når kandidaterne åbner en af deres ansøgninger, kan de se det aktuelle stadie og evt. ventende handlinger, som de skal udføre. Hvis en kandidat f.eks. skal angive potentielle datoer for en personlig samtale, vises de tilgængelige indstillinger på siden.

## <a name="internal-jobs"></a>Interne job

Job, der er markeret som interne og opslået på Attract-karrierewebstedet, vises i øjeblikket ikke på karrierewebstedet. De er kun tilgængelige via en direkte **Ansøg** URL-adresse, der kan kopieres fra programmet Attract.
