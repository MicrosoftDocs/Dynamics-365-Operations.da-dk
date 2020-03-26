---
title: Klargøre Talent
description: Dette emne fører dig gennem processen med at klargøre et nyt miljø til Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: d7c4a8174007384370ae320b3874e104c04b71a5
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124698"
---
# <a name="provision-talent"></a>Klargøre Talent

Dette emne fører dig gennem processen med at klargøre et nyt produktionsmiljø til Microsoft Dynamics 365 Talent. Det antages i emnet, at du har købt Talent via en Cloud Solution Provider (CSP) eller EA-aftale (Enterprise Architecture). Hvis du har en eksisterende Microsoft Dynamics 365-licens, der allerede indeholder Talent-serviceplanen, og du ikke kan udføre trinnene i dette emne, kan du kontakte Support.

For at komme i gang skal den globale administrator logge på [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og oprette et nyt Talent-projekt. Medmindre et problem med licensering forhindrer klargøring af Talent, skulle der ikke være brug for hjælp fra Support- eller DSE-medarbejdere (Dynamics Service Engineering).

## <a name="create-an-lcs-project"></a>Oprette et LCS-projekt
Når du vil bruge LCS til at administrere dine Talent-miljøer, skal du først oprette et LCS-projekt.

1. Log på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjælp af den konto, som du brugte til dit abonnement på Talent.

2. Markér plustegnet (**+**) for at oprette et projekt.

3. Vælg **Microsoft Dynamics 365 Talent** som produktnavn og -version.

4. Vælg **Dynamics 365 Talent**-metoden.

5. Vælg **Opret**. 

Du kan finde oplysninger om, hvordan du kommer i gang med Talent, i den **Talent**-metode, du oprettede i det nye projekt. Når du er færdig med at oprette projektet, skal du udføre følgende procedure for at klargøre Talent-miljøet.

## <a name="provision-a-talent-project"></a>Klargøre et Talent-projekt

Når du har oprettet et LCS-projekt, kan du klargøre Talent i et miljø.

1. I LCS-projektet skal du vælge feltet **Administration af Talent-app**.

2. Angiv, om dette er en sandkasse- eller produktionsforekomst af Talent. De tidlige visningsfunktioner kan være tilgængelige i sandkasseforekomster med henblik på hurtig feedback og test. 

    > [!NOTE]
    > Talent-forekomsttypen kan ikke ændres, når den først er angivet. Kontrollér, at den korrekte forekomsttype er valgt, før du fortsætter.

    > [!NOTE]
    > Talent-forekomsttypen er adskilt fra den forekomsttype for Microsoft Power Apps-miljøet, som du angiver i Power Apps Administration.

3. Vælg indstillingen **Inkluder demodata**, hvis du ønsker, at dit miljø skal medtage det demodatasæt, der bruges af Testdrev til Talent-oplevelsen. Dette er en fordel for langsigtede demo- eller uddannelsesmiljøer og skal aldrig bruges til produktionsmiljøer.  Bemærk, at du skal vælge denne indstilling ved første installation. Du kan ikke efterfølgende opdatere en eksisterende installation.

4. Talent klargøres altid i et Microsoft Power Apps-miljø for at aktivere Power Apps-integration og -udvidelse. Læs afsnittet "Valg af et Power Apps-miljø" i dette emne, før du fortsætter. Hvis du ikke allerede har et Power Apps-miljø, skal du vælge "Administrer miljøer i LCS" eller navigere til Power Apps Administration. Følg derefter trinnene for at [Oprette et Power Apps-miljø](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Vælg det miljø, du vil klargøre Talent til.

6. Vælg **Ja** for at acceptere vilkårene og begynde installationen.

    Det nye miljø vises på listen over miljøer i navigationsruden til venstre. Men du kan ikke begynde at bruge miljøet, før installationsstatus er opdateret til **Installeret**. Denne proces tager typisk få minutter. Hvis klargøringsprocessen mislykkes, skal du kontakte Support.

7. Vælg **Log på Talent** for at bruge det nye miljø.

    > [!NOTE]
    > Hvis du endnu ikke har godkendt de endelige krav, kan du installere en testforekomst af Talent i projektet. Du kan derefter bruge denne forekomst til at teste din løsning, indtil du kan godkende den. Hvis du bruger det nye miljø til test, skal du gentage denne procedure for at oprette et produktionsmiljø.

    > Da kun to LCS-miljøer er tilladt som en del af Talent-abonnementet, kan du også overveje at benytte dig af et gratis 60-dages [Talent-forsøgsmiljø](https://dynamics.microsoft.com/talent/overview/). Selvom et forsøgsmiljø ejes af den bruger, der har anmodet om det, kan andre brugere inviteres gennem systemadministrationsoplevelsen i Personale. Forsøgsmiljøer indeholder fiktive data, der kan bruges til at udforske programmet på en sikker måde. De ikke er beregnet til brug som produktionsmiljøer. Bemærk, at når et forsøgsmiljø udløber efter 60 dage, slettes alle data i det, og de kan ikke gendannes. Du kan tilmelde dig til et nyt forsøgsmiljø, når det eksisterende miljø udløber.

## <a name="select-a-power-apps-environment"></a>Vælg et Power Apps-miljø

Integrationen mellem Talent- og Power Apps-miljøerne gør det muligt for dig at integrere og udvide brugen af Talent-data ved hjælp af Power Apps-værktøjer. Forståelse af formålet med Power Apps-miljøer vil ikke blot hjælpe dig med at udvikle apps med henblik på at udvide Talent, men vil også hjælpe dig med at vælge det korrekte miljø i forbindelse med klargøringen af Talent. Du kan finde oplysninger om Power Apps-miljøer, herunder omfanget af miljøet, adgang til miljøet og oprettelse og valg af et miljø, under [Annoncering af Power Apps-miljøer](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Brug følgende retningslinjer til fastsættelse af, hvilket Power Apps-miljø som Talent skal installeres i: 

1. I LCS skal du vælge **Administrer miljøer** eller gå direkte til Power Apps Administration, hvor du kan få vist eksisterende miljøer og oprette nye miljøer.

2. Der er knyttet et enkelt Talent-miljø til et enkelt Power Apps-miljø.

3. Et Power Apps-miljø indeholder Talent sammen med de tilsvarende Power Apps-, Power Automate- og Common Data Service-programmer. Hvis Power Apps-miljøet slettes, så slettes apps i det samtidig. Under klargøring af et Talent-miljø kan enten et **Prøveversion**- eller **Produktion**-miljø klargøres. Vælg den ønskede type miljø baseret på, hvordan miljøet skal bruges. 

4. Dataintegration og teststrategier, såsom Sandkasse, UAT eller Produktion, bør tages i betragtning. Vi anbefaler, at du overvejer de forskellige konsekvenser af din installation, da det ikke er let at ændre tilknytningen af Talent-miljøer til et Power Apps-miljø senere.

5. Følgende Power Apps-miljøer kan ikke bruges til Talent og filtreres fra valglisten i LCS:
 
    - **Power Apps-standardmiljøer** ‑ Selvom hver lejer automatisk klargøres med et Power Apps-standardmiljø, anbefales det ikke at bruge dem sammen med Talent, da alle lejerbrugere har adgang til Power Apps-miljøet og derfor utilsigtet kan beskadige produktionsdata i forbindelse med test og gennemsyn af Power Apps- eller Power Automate-integrationer.
   
    - **Testmiljøer** ‑ Disse miljøer oprettes med en udløbsdato og udløber efter dette tidspunkt, hvilket resulterer i, at dit miljø og enhver Talent-forekomst, der er indeholdt heri, automatisk bliver fjernet.
   
    - **Ikke-understøttede områder** - I øjeblikket understøttes Talent kun i følgende områder: USA, Europa, Storbritannien, Australien, Canada og Asien.
  
6. Når du har besluttet, hvilket miljø der er bedst at anvende, kan du fortsætte klargøringsprocessen. 
 
## <a name="grant-access-to-the-environment"></a>Give adgang til miljøet

Som standard har den globale administrator, der oprettede miljøet, adgang til det. Men andre programbrugere skal eksplicit tildeles adgang. For at give adgang skal du tilføje brugere og tildele dem de relevante roller i Personale-miljøet. Den globale administrator, der installerede Talent, skal også starte både Attract og Onboard for at fuldføre initialiseringen og aktivere adgang for andre lejerbrugere.  Før dette er gjort, kan andre brugere ikke få adgang til Attract og Onboard, men får adgangsfejl. Du kan finde flere oplysninger under [Opret nye brugere](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tildel sikkerhedsroller til brugere](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
