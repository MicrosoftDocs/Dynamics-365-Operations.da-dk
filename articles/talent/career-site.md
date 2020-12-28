---
title: Konfigurer dit karrierewebsted i Attract
description: Dette emne indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Microsoft Dynamics 365 Talent - Attract.
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: d4a1e7c19ccec6ae32e46ec7d58604b162418953
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460650"
---
# <a name="set-up-your-career-site-in-attract"></a>Konfigurer dit karrierewebsted i Attract

[!include [banner](includes/banner.md)]

Denne artikel indeholder en oversigt over funktioner for kandidater på karrierewebstedet i Microsoft Dynamics 365 Talent: Attract. I artiklen beskrives også, hvordan du konfigurerer denne funktion.

Attract indeholder ét karrierewebsted for hvert miljø i en lejer. F.eks. hvis en organisation har et miljø til udvikling og et testmiljø, klargøres ét karrierewebsted til udviklingsmiljøet og et andet til testmiljøet. Hvert karrierewebsted er fuldstændigt isoleret og har sit eget system til godkendelse. Job- og kandidatprofiler deles ikke mellem karrierewebstederne.

Som standard er karrierewebstedet offentligt. Derfor kan kandidater få vist alle job, der er markeret som eksterne, uden at skulle logge på. Alle andre handlinger kræver dog, at kandidaterne er logget på.

## <a name="career-site-management"></a>Administration af karrierewebsted

For at angive værdierne for følgende elementer skal brugeren logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** (tandhjulsymbolet) og derefter vælge fanen **Firmaoplysninger**.

-   **Organisationsnavn** - Organisationens navn vises på navigationslinjen øverst i karrierewebstedet. Hvis kandidaterne vælger organisationsnavnet, kommer de til en side over alle ledige job.

-   **Organisationslogo** - Et billede af organisationens logo vises øverst til venstre på karrierewebstedet. Hvis kandidaterne vælger logobilledet, kommer de til en side over alle ledige job.

    > [!NOTE] 
    > Logobilledet, der vises på karrierewebstedet, har en fast højde på 20 pixel (px). Billedet, du tilføjer under administration, skaleres, så det passer i størrelsen. Afhængigt af billedet kan bredden evt. blive ændret.
 
For at angive værdierne for følgende elementer skal brugeren logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** og derefter vælge fanen **Administration af karrierewebsted**.

-   **Optimering af søgemaskine** – Når denne indstilling er aktiveret, kan der søges i alle offentlige job, der opslås på Attract-karrierewebstedet, ved hjælp af søgemaskiner som Bing og Google. 

    > [!NOTE] 
    > Der kan være en forsinkelse fra denne indstilling aktiveres, til søgeresultater vises, afhængigt af hvilken søgemaskine du bruger.
    
-   **Vilkår og betingelser** – Når den er aktiveret, skal alle kandidater godkende organisationens vilkår og betingelser, når de ansøger om et job. Attract-administratoren kan både konfigurere sin egen samtykketekst og linket til sine vilkår og betingelser. 

        
## <a name="career-site-urls"></a>URL-adresser til karrierewebsteder

Følgende liste indeholder de almindeligt anvendte karrierewebsteders URL-adresser, og hvordan du får adgang til dem.

-   **URL-adresse til startside for karrierewebsted** - Hvis du vil have vist URL-adressen til startsiden for karrierewebstedet, skal du logge på Attract som administrator, vælge **Administration** i menuen **Indstillinger** og derefter vælge fanen **Administration af karrierewebsted**.

-   **URL-adresse til ansøgning om individuelt jobopslag** - Når du [slår et eksternt job op](Creating-jobs-Attract.md#postings) for første gang, kan du kopiere linket **Ansøg** fra Attract. URL-adressen til dette link har følgende format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

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

Kandidater skal logge på ved hjælp af Azure AD, hvis det job de kigger på eller ansøger om, er angivet som værende udelukkende internt.

## <a name="create-and-maintain-a-profile"></a>Oprette og vedligeholde en profil

Når kandidater har logget på karrierewebstedet, kan de vælge **Min profil** på navigationslinjen øverst på siden for at oprette og vedligeholde deres profil.
Profilen indeholder personlige oplysninger, oplysninger om arbejdserfaring og uddannelse, dokumenter, links og oplysninger om færdigheder. Når en profil er oprettet, kan den bruges til at ansøge om job, som kandidaten er interesseret i. Profiler hjælper også Attract med at anbefale de rigtige job til kandidater.

> [!NOTE]
> Hvis en kandidat bruger et e-mail-id til at logge på ved hjælp af en af godkendelsesudbyder, der er angivet ovenfor, anvendes standardkontaktens e-mail-id, der er knyttet til profilen. Id'et kan dog ændres når som helst og er helt uafhængigt af det første id. Attract bruger altid det kontakt-e-mail-id'et, der skal knyttes til din profil, til al e-mailkommunikation.

## <a name="find-the-right-job"></a>Finde det rette job

På joblistesiden kan kandidaterne søge efter et bestemt job ved at indtaste søgeord. Søgefunktionen leder efter søgeord i stillingsbetegnelser og jobbeskrivelser og viser de relevante job som resultat. Kandidaterne kan filtrere resultaterne når som helst baseret på jobstedet eller jobfunktionen.

Kandidaterne kan også se en række anbefalede job på karrierewebstedet. Hvilke job der anbefales til en kandidat, afhænger af kandidatens tidligere ansøgninger, profil og CV'er.

> [!NOTE] 
> Jobanbefalinger vises kun, hvis der er opslået mindst 10 job på karrierewebstedet, og hvis kandidaten har fuldført en profil.

Interne kandidater kan også se, hvem den ansættelsesansvarlige og/eller rekrutteringsmedarbejderen for et job er, i tilfælde af at de ønsker at kontakte de pågældende medlemmer af ansættelsesteamet. Eksterne kandidater kan derimod ikke se medlemmerne af ansættelsesteamet ved nogen som helst jobs.

## <a name="contact-the-hiring-team"></a>Kontakt ansættelsesteamet
Alene interne kandidater kan kontakte ansættelsesteamet. Denne begrænsning gælder for alle jobs, uanset om de kun er til interne ansøgere, eller de er blevet slået op offentligt.

Kandidaterne ønsker muligvis at kontakte ansættelsesteamet for at udtrykke deres interesse i et opslået job eller lære mere om det. De kan kontakte alle de oplyste medlemmer af ansættelsesteamet (den ansættelsesansvarlige eller rekrutteringsmedarbejdere). De kan endvidere vælge at vedhæfte et CV til beskeden, eller de kan vælge et eksisterende CV, som de tidligere har uploadet som en del af deres profil.

Når den interne kandidat har valgt, hvilke medlemmer af ansættelsesteamet denne ønsker at kontakte, sender Attract en e-mail til de pågældende personer på kandidatens vegne. Samtidig hermed tilføjes kandidatens profil til stadiet **Kandidatemne**, såfremt dette stadie er tilgængeligt for det pågældende job. På **Kandidatemne**-stadiet kan rekrutteringsmedarbejdere eller de ansættelsesansvarlige se de kandidater, der har kontaktet dem. De kan også se kandidaternes profiler og opfordre potentielle kandidater til at ansøge.

Kandidaterne kan søge et job, som de allerede har kontaktet medlemmer af ansættelsesteamet omkring. Når kandidaterne har ansøgt, kan de ikke længere kontakte ansættelsesteamet via karrierewebstedet.

## <a name="apply-for-jobs"></a>Ansøge om job

Når kandidaterne har fundet det rigtige job, kan de ansøge ved hjælp af knappen **Ansøg** på siden med **Jobdetaljer**. På dette tidspunkt kan ansøgerne enten oprette en ny profil eller gennemse oplysningerne i deres eksisterende profil.
De kan også overføre et CV efter behov og derefter sende jobansøgningen.

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a>Gør det muligt at søge jobs med LinkedIn-profiler

Du kan gøre det nemt for kandidaterne at søge dine stillinger ved at konfigurere Attract til at give dem mulighed for at søge via LinkedIn.

> [!NOTE] 
> Du skal have en eller flere rekrutteringslicenser fra LinkedIn, før du kan give kandidaterne mulighed for at ansøge via LinkedIn.

1. Log på Attract som administrator.
2. Vælg knappen **Indstillinger** (tandhjulssymbolet) i øverste højre hjørne af siden, og vælg dernæst **Administration**.
3. Vælg fanen **LinkedIn-integration**, og opret forbindelse til en LinkedIn Recruiter-konto.
4. I afsnittet **LinkedIn Recruiter System Connect-integration** skal du under indstillingen **Ansøg via LinkedIn** vælge **Aktiver**.

Når du har aktiveret indstillingen, kan kandidater ansøge ved at anvende deres eksisterende LinkedIn-profildata. Når kandidaterne ansøger ved at vælge knappen **Ansøg via LinkedIn**, anmodes de om at godkende med LinkedIn, såfremt de ikke allerede er logget ind. Efter de har godkendt, erstatter deres LinkedIn-profil alle de eksisterende profildata, der fremgår af ansøgningssiden. Kandidaterne kan redigere deres oplysninger efter behov og derefter indsende ansøgningen. Såfremt en kandidat navigerer væk fra siden uden at søge jobbet, opdateres deres profildata ikke i Attract.

## <a name="check-application-status"></a>Kontrollere ansøgningsstatus

Når kandidaterne har ansøgt om et eller flere job, kan de vælge **Ansøgninger** på navigationslinjen øverst på siden for at få vist deres åbne og lukkede ansøgninger. Når kandidaterne åbner en af deres ansøgninger, kan de se det aktuelle stadie og evt. ventende handlinger, som de skal udføre. Hvis en kandidat f.eks. skal angive potentielle datoer for en personlig samtale, vises de tilgængelige indstillinger på siden.

## <a name="internal-jobs"></a>Interne job

Job, der er markeret som interne og opslået på Attract-karrierewebstedet, vises i øjeblikket ikke på karrierewebstedet. De er kun tilgængelige via en direkte **Ansøg** URL-adresse, der kan kopieres fra programmet Attract.
