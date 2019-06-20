---
title: Klargøre Talent
description: Dette emne fører dig gennem processen med at klargøre et nyt miljø til Microsoft Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 05/15/2019
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
ms.openlocfilehash: 03edb5d626f221863f45804ce84168692c2bd1f3
ms.sourcegitcommit: 3c4e59f55af2eafb3adbae3bb0091e4f6caacc8b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576915"
---
# <a name="provision-talent"></a>Klargøre Talent

[!include [banner](includes/banner.md)]

Dette emne fører dig gennem processen med at klargøre et nyt produktionsmiljø til Microsoft Dynamics 365 for Talent. Det antages i emnet, at du har købt Talent via en Cloud Solution Provider (CSP) eller EA-aftale (Enterprise Architecture). Hvis du har en eksisterende Microsoft Dynamics 365-licens, der allerede indeholder Talent-serviceplanen, og du ikke kan udføre trinnene i dette emne, kan du kontakte Support.

For at komme i gang skal den globale administrator logge på [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og oprette et nyt Talent-projekt. Medmindre et problem med licensering forhindrer klargøring af Talent, skulle der ikke være brug for hjælp fra Support- eller DSE-medarbejdere (Dynamics Service Engineering).

## <a name="create-an-lcs-project"></a>Oprette et LCS-projekt
Når du vil bruge LCS til at administrere dine Talent-miljøer, skal du først oprette et LCS-projekt.

1. Log på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjælp af den konto, som du brugte til dit abonnement på Talent.
2. Markér plustegnet (**+**) for at oprette et projekt.
3. Vælg **Microsoft Dynamics 365 for Talent** som produktnavn og -version.
4. Vælg **Dynamics 365 for Talent**-metoden.
5. Vælg **Opret**.

Du kan finde oplysninger om, hvordan du kommer i gang med Talent, i den **Talent**-metode, du oprettede i det nye projekt. Når du er færdig med at oprette projektet, skal du udføre følgende procedure for at klargøre Talent-miljøet.

## <a name="provision-a-talent-project"></a>Klargøre et Talent-projekt
Når du har oprettet et LCS-projekt, kan du klargøre Talent i et miljø.

1. I LCS-projektet skal du vælge feltet **Administration af Talent-app**.
2. Angiv, om dette er en sandkasse- eller produktionsforekomst af Talent. De tidlige visningsfunktioner kan være tilgængelige i sandkasseforekomster med henblik på hurtig feedback og test. 
3. Vælg indstillingen **Inkluder demodata**, hvis du ønsker, at dit miljø skal medtage det demodatasæt, der bruges af Testdrev til Talent-oplevelsen. Dette er en fordel for langsigtede demo- eller uddannelsesmiljøer og skal aldrig bruges til produktionsmiljøer.  Bemærk, at du skal vælge denne indstilling ved første installation. Du kan ikke efterfølgende opdatere en eksisterende installation.
4. Talent klargøres altid i et Microsoft PowerApps-miljø for at aktivere PowerApps-integration og -udvidelse. Læs afsnittet "Valg af et PowerApps miljø" i dette emne, før du fortsætter. Hvis du ikke allerede har et PowerApps-miljø, skal du vælge "Administrer miljøer i LCS" eller navigere til administrationscentret for PowerApps. Følg derefter trinnene for at [Oprette et PowerApps-miljø](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment).

    > [!NOTE]
    > For at få vist eksisterende miljøer eller oprette nye miljøer skal den lejeradministrator, der klargør Talent, være tildelt til PowerApps P2-licensen. Hvis organisationen ikke har en PowerApps P2-licens, kan du få en fra din Cloud Solution Provider eller fra [PowerApps-prissætningssiden](https://powerapps.microsoft.com/en-us/pricing/).

5. Vælg det miljø, du vil klargøre Talent til.
6. Vælg **Ja** for at acceptere vilkårene og begynde installationen.

    Det nye miljø vises på listen over miljøer i navigationsruden til venstre. Men du kan ikke begynde at bruge miljøet, før installationsstatus er opdateret til **Installeret**. Denne proces tager typisk få minutter. Hvis klargøringsprocessen mislykkes, skal du kontakte Support.

7. Vælg **Log på Talent** for at bruge det nye miljø.

    > [!NOTE]
    > Hvis du endnu ikke har godkendt de endelige krav, kan du installere en testforekomst af Talent i projektet. Du kan derefter bruge denne forekomst til at teste din løsning, indtil du kan godkende den. Hvis du bruger det nye miljø til test, skal du gentage denne procedure for at oprette et produktionsmiljø.

    > Da kun to LCS-miljøer er tilladt som en del af Talent-abonnementet, kan du også overveje at benytte dig af et gratis 60-dages [Talent-forsøgsmiljø](https://dynamics.microsoft.com/en-us/talent/overview/). Selvom et forsøgsmiljø ejes af den bruger, der har anmodet om det, kan andre brugere inviteres gennem systemadministrationsoplevelsen i det centrale HR-miljø. Forsøgsmiljøer indeholder fiktive data, der kan bruges til at udforske programmet på en sikker måde. De ikke er beregnet til brug som produktionsmiljøer. Bemærk, at når et forsøgsmiljø udløber efter 60 dage, slettes alle data i det, og de kan ikke gendannes. Du kan tilmelde dig til et nyt forsøgsmiljø, når det eksisterende miljø udløber.

## <a name="select-a-powerapps-environment"></a>Vælg et PowerApps-miljø

Integrationen mellem Talent- og PowerApps-miljøerne gør det muligt for dig at integrere og udvide brugen af Talent-data ved hjælp af PowerApps-værktøjer. Forståelse af formålet med PowerApps-miljøer vil ikke blot hjælpe dig med at udvikle apps med henblik på at udvide Talent, men vil også hjælpe dig med at vælge det korrekte miljø i forbindelse med klargøringen af Talent. Du kan finde flere oplysninger om PowerApps-miljøer, herunder omfanget af miljøet, adgang til miljøet og oprettelse og valg af et miljø, under [Annoncering af PowerApps-miljøer](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Brug følgende retningslinjer til fastsættelse af, hvilket PowerApps-miljø til Talent skal installeres i: 

1. I LCS skal du vælge **Administrer miljøer** eller gå direkte til PowerApps Administrationscenter, hvor du kan få vist eksisterende miljøer og oprette nye miljøer.
2. Der er knyttet et enkelt Talent-miljø til et enkelt PowerApps-miljø.
3. Et PowerApps-miljø "indeholder" Talent-programmet sammen med de tilsvarende PowerApps-, Flow- og Common Data Service-programmer. Hvis PowerApps-miljøet slettes, så slettes apps i det samtidig. Under klargøring af et Talent-miljø kan enten "Prøveversion" eller "Produktion" klargøres. Vælg den ønskede type miljø baseret på, hvordan miljøet skal bruges. 
4. Dataintegration og teststrategier, såsom Sandkasse, UAT eller Produktion, bør tages i betragtning. Vi anbefaler, at du overvejer de forskellige konsekvenser af din installation, da det ikke er let at ændre tilknytningen af Talent-miljøer til et PowerApps-miljø senere.
5. Følgende PowerApps-miljøer kan ikke bruges til Talent og filtreres fra valglisten i LCS:
 
    - **Power Apps-standardmiljøer** ‑ Selvom hver lejer automatisk klargøres med et PowerApps-standardmiljø, anbefales det ikke at bruge dem sammen med Talent, da alle lejerbrugere har adgang til PowerApps-miljøet og derfor utilsigtet kan beskadige produktionsdata i forbindelse med test og gennemsyn af PowerApps- eller Flow-integrationer.
   
    - **Testmiljøer** ‑ Disse miljøer oprettes med en udløbsdato og udløber efter dette tidspunkt, hvilket resulterer i, at dit miljø og enhver Talent-forekomst, der er indeholdt heri, automatisk bliver fjernet.
   
    - **Ikke-understøttede områder** - I øjeblikket understøttes Talent kun i følgende områder: USA, Europa, Det Forenede Kongerige eller Australien.
  
6. Når du har besluttet, hvilket miljø der er bedst at anvende, kan du fortsætte klargøringsprocessen. 
 
## <a name="grant-access-to-the-environment"></a>Give adgang til miljøet
Som standard har den globale administrator, der oprettede miljøet, adgang til det. Men andre programbrugere skal eksplicit tildeles adgang. For at give adgang skal du tilføje brugere og tildele de relevante roller til dem i det centrale Core HR-miljø. Den globale administrator, der installerede Talent, skal også starte både Attract og Onboard-programmerne for at fuldføre initialiseringen og aktivere adgang for andre lejerbrugere.  Før dette er gjort, kan andre brugere ikke få adgang til Attract- og Onboard-programmer, men får adgangsfejl. Du kan finde flere oplysninger under [Opret nye brugere](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tildel sikkerhedsroller til brugere](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
