---
title: Forsyning med LinkedIn Recruiter
description: "Dette emne indeholder oplysninger om brug af maskinel indlæring til at få anbefalinger om job og jobkandidater."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: da-dk
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a>Forsyning med LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn er verdens største talentdatabase og ofte det primære system, som rekrutteringsmedarbejdere bruger til at finde og kommunikere med kandidater og til kandidatkilde til de stillinger, som rekrutteringsmedarbejdere ønsker at besætte. LinkedIn Recruiter-integration med Dynamics 365 for Talent: Attract gør det lettere for brugerne at ansætte og holde dataene synkroniseret mellem de to systemer.

> [!NOTE]
> Du skal bruge tilføjelsesprogrammet til omfattende ansættelser og LinkedIn Recruiter-poster for at kunne bruge LinkedIn Recruiter-integration med Attract.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Konfigurere LinkedIn Recruiter med Attract 

Før du kan bruge funktionerne i LinkedIn Recruiter, skal du konfigurere adgang på kontrakt- eller firmaniveau i din Attract-forekomst. For at gennemføre konfigurationen skal du samarbejde med den bruger, der er administrator på din LinkedIn Recruiter-kontrakt. Udfør følgende trin for at konfigurere LinkedIn Recruiter med Attract.

1.  Log på Attract som administrator, og gå til **Administratorindstillinger**.

2.  Klik i venstre rude på fanen **Integration af LinkedIn**.

[![Attract-administratorvisning til start af LinkedIn Recruiter-integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Klik på **Opret forbindelse** for at starte opsætningen og blive hjulpet gennem LinkedIn-logonprocessen.

4.  Hvis du har poster på flere LinkedIn-kontrakter, skal du vælge den kontrakt, som du vil forbinde med Attract-systemet. Hvis du har en post i kun én LinkedIn-kontrakt, er dette trin ikke nødvendigt.

5.  LinkedIn-widgetten indlæses nu i dine administratorindstillinger med listen over integrationer vist. Under **Recruiter System Connect** skal du klikke på **Request** (Anmod om).

[![Attract-administratorvisning til anmodning om LinkedIn Recruiter-integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Når Attract har anmodet om integration, vises meddelelsen som **Partner ready** (Partnerklar), og integrationen kan aktiveres fra **Recruiter Admin settings** (Recruiter-administratorindstillinger). Hvis du kan se **Notify partner** (Informer partner) på denne side, skal du vente et øjeblik, klikke på **Notify partner** og derefter opdatere siden. Der bør nu stå **Partner ready** (Partnerklar).

[![Attract-administratorvisning til angivelse af Attract-siden af anmodninger, der er fuldført](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

For at fuldføre det næste trin skal du have administratorrettigheder på din LinkedIn Recruiter-kontrakt.

7.  Log på LinkedIn ved hjælp af administratorkontoen, og gå til LinkedIn Recruiter øverst til højre. 

8. I menuen **More** (Flere) øverst på skærmen skal du klikke på **Admin Settings** (Administratorindstillinger) og derefter klikke på fanen **ATS**.

Attract-systemet vises med et par indstillinger, der kan aktiveres.

9. Hvis du kun vil aktivere eksport med 1 klik for **In-ATS indicator** og **In-ATS Profile Widget**, skal du vælge **Company-level access** (Adgang på firmaniveau). Hvis du vil aktivere alle adgangsfunktioner på firmaniveau plus adgang til InMail-historik, Notes-oversigt og InMail-stubprofil, skal du vælge **Contract-level access** (Adgang på kontraktniveau).

10. Slå det ønskede adgangsniveau til fra dine **Admin-ATS**-indstillinger i LinkedIn Recruiter.

[![Aktiver Attract-integration fra LinkedIn Recruiter-administratorvisning](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Gå tilbage til Attract-administratorindstillingerne, og vælg fanen **LinkedIn Integration**. Du kan nu se LinkedIn-widgetindlæsningen, som viser **Enabled** (Aktiveret) og det valgte adgangsniveau aktiveret.

[![LinkedIn Recruiter integration fuldført](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>Bruge LinkedIn Recruiter-funktioner

Når LinkedIn Recruiter-funktionerne er aktiveret af Attract-administratoren, er de tilgængelige for ansættelsesansvarlige og rekrutteringsmedarbejdere. Du kan bruge disse funktioner ved at oprette forbindelse til din LinkedIn-konto under **Brugerindstillinger**. Flere funktioner bliver tilgængelige, når der er forbindelse til både administrator- og brugerindstillinger.

### <a name="in-ats-profile-widget"></a>In-ATS-profilwidget

Du kan få vist kandidatens LinkedIn-profil i Attract. LinkedIn-widgetten viser kandidatprofilen, når ATS-oplysningerne svarer til brugernes LinkedIn-oplysninger.

Hvis du vil se en profil, skal du gå til kandidatprofilen, enten fra et job eller en talentpulje. I kandidatprofilen skal du vælge fanen **LinkedIn**, så profilwidgetten indlæses. Med profilwidgetten skal du angive, om det er det korrekte match. Hvis ikke, skal du finde den rigtige person. Du kan også gemme kandidaten i dine LinkedIn Recruiter-projekter fra denne side.

### <a name="1-click-export"></a>Eksport med 1 klik 

Mens kandidatforsyningen pågår i LinkedIn, kan du eksportere kandidaten med 1 klik til de job, du har åbnet. Udfør følgende trin for at anvende eksport med 1 klik. Før du fuldfører disse trin, skal du kontrollere, at du er tildelt rollen som ansættelsesansvarlig eller rekrutteringsmedarbejder for jobbet, og at jobbet har stadiet **Jobkandidat**.

1.  Opret jobbet, tildel de relevante roller, og aktivér jobbet.

2.  Når jobbet er aktiveret, kan du gå til LinkedIn Recruiter.

3.  Find den kandidat, du søger efter, og gå til vedkommendes profil.

4.  Ved hjælp af søgefeltet i kontaktkortet skal du finde jobbet ved hjælp af titlen eller det job-id, der blev aktiveret i Attract. Hvis du ikke finder jobbet, skal du klikke på **Change ATS** (Skift ATS) for at finde den korrekte forekomst af Attract.

5. Når jobbet er valgt, skal du klikke på **Eksport**. Kandidaten hentes nu af Attract.

6.  Gå til Attract, og åbn det pågældende job. Du kan finde den kandidat, som du lige har eksporteret i stadiet **Jobkandidat** for jobbet.

### <a name="in-ats-indicator"></a>In-ATS indicator 

Når du bruger LinkedIn Recruiter, kan du spore, om en kandidat har ansøgt om andre job i organisationen, se på, hvor de er i forskellige faser af jobansøgninger, og se feedback og kommentarer fra Attract i LinkedIn Recruiter.

1.  Åbn LinkedIn Recruiter, og find den kandidatprofil, du leder efter.

2.  Rul ned for at få vist sektionen **In-ATS** i kandidatens profil.

3.  Du kan bruge denne widget til at få vist alle de oplysninger om kandidaten, der findes i Attract, i LinkedIn Recruiter-visningen.

4.  Vælg fanen **Jobs & Statuses** for at få vist job, som de er en del af, den seneste status, og hvordan de har rykket i forhold til hvert job.

5.  Vælg fanen **Interview Feedback** for at se feedback, som interviewerne har sendt i Attract.

6.  Vælg fanen **Notes** for at få vist noter, der er hentet for denne ansøger i Attract.

### <a name="inmail-history"></a>InMail-historik

LinkedIn InMail-historikken er tilgængelig på kontraktniveau i LinkedIn Recruiter. Når den er aktiveret, kan du få vist hele InMail-historikken for kandidaten. Du kan også se, hvem fra din organisation der har udvekslet InMail med kandidaten, men du ikke kan få vist meddelelserne mellem dem.

Hvis du vil se InMail-historik, skal du gå til en kandidats profil, gå til fanen **LinkedIn** og rulle til bunden af siden for at få vist historikken. Du kan kun få vist InMail-historikken, hvis kandidaten har svaret på din anmodning og valgt at dele deres profil med dig på LinkedIn. Meddelelserne fra InMail synkroniseres med Attract med få timers mellemrum.

### <a name="notes-history"></a>Oversigt over noter 

LinkedIn Notes-historikken er tilgængelig på kontraktniveau i LinkedIn Recruiter. Når den er aktiveret, kan du få vist de noter, der er hentet om kandidaten fra forskellige rekrutteringsmedarbejdere fra din organisation.

Hvis du vil se Notes-historikken, skal du gå til en kandidats profil, gå til fanen **LinkedIn** og rulle til bunden af siden for at få vist historikken. Du kan få vist alle noter om kandidaten fra LinkedIn Recruiter.

### <a name="inmail-stub-profile"></a>InMail-stubprofil

LinkedIn InMail-stubprofilen er tilgængelig på kontraktniveau i LinkedIn Recruiter. Hvis kandidaterne accepterer at dele deres LinkedIn-profiler med enhver bruger i din organisation, kan du spore kandidaterne i Attract, og der bliver oprettet en ny kandidatpost for hver kandidat.

For at få vist listen over kandidater skal du gå til **Talentpuljer** for at få vist en systemoprettet LinkedIn-talentpulje. Denne talentpulje indeholder listen over kandidater og deres stubprofiler som modtaget fra LinkedIn med kandidatens fornavn og efternavn. Kandidatens e-mail-id vises, hvis kandidaten har valgt at dele sin e-mailadresse.

