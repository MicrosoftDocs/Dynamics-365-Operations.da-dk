---
title: Klargør Human Resources
description: Denne artikel fører dig gennem processen med at klargøre et nyt produktionsmiljø til Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1a57180c60be4b4686c274aecbf86f0bc6c8b2fb
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111867"
---
# <a name="provision-human-resources"></a>Klargør Human Resources

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikel fører dig gennem processen med at klargøre et nyt produktionsmiljø til Microsoft Dynamics 365 Human Resources. Det antages i artiklen, at du har købt Human Resources via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture). Hvis du har en eksisterende Microsoft Dynamics 365-licens, der allerede indeholder Human Resources-serviceplanen, og du ikke kan udføre trinnene i denne artikel, kan du kontakte Support.

For at komme i gang skal den globale administrator logge på [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og oprette et nyt Human Resources-projekt. Medmindre et problem med licensering forhindrer klargøring af Human Resources, skulle der ikke være brug for hjælp fra Support- eller DSE-medarbejdere (Dynamics Service Engineering).

## <a name="plan-human-resources-environments"></a>Planlægge miljøer i Human Resources

Før du opretter dit første miljø med Human Resources, skal du planlægge miljøets behov nøje for dit projekt. Et basisabonnement på Human Resources omfatter to miljøer: et produktionsmiljø og et sandkassemiljø. Afhængigt af, hvor kompleks projektet er, kan det være nødvendigt at købe flere sandkassemiljøer for at understøtte projektaktiviteter. 

Overvejelser i forbindelse med yderligere miljøer omfatter, men det er ikke begrænset til, følgende:

- **Overflytning af data**: Du skal muligvis overveje et ekstra miljø, når der skal bruges dataoverførselsaktiviteter, så dit sandkassemiljø kan bruges til testformål i hele projektet. Et ekstra miljø gør det muligt at fortsætte dataoverflytningsaktiviteter, mens test- og konfigurationsaktiviteter finder sted samtidigt i et andet miljø.
- **Integration**: Du skal muligvis overveje et yderligere miljø for at konfigurere og teste integration. Dette kan omfatte oprindelige integrationer, f.eks. Ceridian Dayforce LinkedIn Talent Hub-integrationer, eller brugerdefinerede integrationer, som f.eks. integration med løn, sporingssystemer for ansøgere eller benefit-systemer og -leverandører.
- **Kursus**: Du har muligvis brug for et separat miljø, der er konfigureret med et sæt kursusdata, for at medarbejderne kan bruge det nye system. 
- **Projekt i flere faser**: Du kan have brug for et yderligere miljø for at understøtte konfiguration, overflytning af data, test eller andre aktiviteter i en projektfase, der er planlagt efter projektets første start.

 > [!IMPORTANT]
 > Det anbefales, at du bruger produktionsmiljøet i hele projektet som GOLD-konfigurationsmiljø. Det er vigtigt, fordi du ikke kan kopiere et sandkassemiljø til et produktionsmiljø. Når du går i gang, vil dit GOLD-miljø derfor være dit produktionsmiljø, og du vil udføre de komplette aktiviteter i dette miljø.</br></br>
 > Det anbefales, at du bruger din sandkasse eller et andet miljø til at udføre en overgang, før du går i gang. Det kan du gøre ved at opdatere produktionsmiljøet med din GOLD-konfiguration i dit sandkassemiljø.</br></br>
 > Det anbefales, at du opbevarer en detaljeret checkliste til overgang, som indeholder hver af de datapakker, der skal bruges til at overflytte de endelige data til produktionsmiljøet i forbindelse med den faktiske overgang.</br></br>
 > Det anbefales også, at du bruger sandkassemiljøet i hele projektet som TEST-miljø. Hvis du har brug for flere miljøer, kan organisationen købe dem for yderligere omkostninger.</br></br>

## <a name="create-an-lcs-project"></a>Oprette et LCS-projekt

Når du vil bruge LCS til at administrere dine Human Resources-miljøer, skal du først oprette et LCS-projekt.

1. Log på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjælp af den konto, som du brugte til dit abonnement på Human Resources.

2. Markér plustegnet (**+**) for at oprette et projekt.

3. Vælg **Microsoft Dynamics 365 Human Resources** som produktnavn og -version.

4. Vælg **Dynamics 365 Human Resources**-metoden.

5. Vælg **Opret**.

Du kan finde oplysninger om, hvordan du kommer i gang med Human Resources, i den **Human Resources**-metode, du oprettede i det nye projekt. Når du er færdig med at oprette projektet, skal du udføre følgende procedure for at klargøre Human Resources-miljøet.

## <a name="provision-a-human-resources-project"></a>Klargøring af et Human Resources-projekt

Når du har oprettet et LCS-projekt, kan du klargøre Human Resources i et miljø.

1. I LCS-projektet skal du vælge feltet **Administration af Human Resources-app**.

2. Angiv, om dette miljø er en sandkasse- eller produktionsforekomst af Human Resources. De tidlige visningsfunktioner kan være tilgængelige i sandkasseforekomster med henblik på hurtig feedback og test.
   
    > [!NOTE]
    > Human Resources-forekomsttypen kan ikke ændres, når den først er angivet. Kontrollér, at den korrekte forekomsttype er valgt, før du fortsætter.</br></br>
    > Human Resources-forekomsttypen er adskilt fra den forekomsttype for Microsoft Power Apps-miljøet, som du angiver i Power Apps Administration.
    
3. Vælg indstillingen **Inkluder demodata**, hvis du ønsker, at dit miljø skal medtage det demodatasæt, der bruges af Testdrev til Human Resources-oplevelsen. Demodata er en fordel for langsigtede demo- eller uddannelsesmiljøer og skal aldrig bruges til produktionsmiljøer. Du skal vælge denne indstilling ved første installation. Du kan ikke opdatere en eksisterende installation senere.

4. Human Resources klargøres altid i et Microsoft Power Apps-miljø for at aktivere Power Apps-integration og -udvidelse. Læs afsnittet "Valg af et Power Apps-miljø" i denne artikel, før du fortsætter. Hvis du ikke allerede har et Power Apps-miljø, skal du vælge "Administrer miljøer i LCS" eller navigere til Power Apps Administration. Følg derefter trinnene for at [Oprette et Power Apps-miljø](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Vælg det miljø, du vil klargøre Human Resources til.

6. Vælg **Ja** for at acceptere vilkårene og begynde installationen.

   Det nye miljø vises på listen over miljøer i navigationsruden til venstre. Men du kan ikke begynde at bruge miljøet, før installationsstatus er opdateret til **Installeret**. Denne proces tager typisk få minutter. Hvis klargøringsprocessen mislykkes, skal du kontakte Support.

7. Vælg **Log på Human Resources** for at bruge det nye miljø.

    > [!NOTE]
    > Hvis du endnu ikke har godkendt de endelige krav, kan du installere en testforekomst af Human Resources i projektet. Du kan derefter bruge denne forekomst til at teste din løsning, indtil du kan godkende den. Hvis du bruger det nye miljø til test, skal du gentage denne procedure for at oprette et produktionsmiljø.

    > Du kan overveje at udnytte et gratis [Human Resources-prøvemiljø](https://go.microsoft.com/fwlink/p/?LinkId=2115962) i 60 dage. Selvom et forsøgsmiljø ejes af den bruger, der har anmodet om det, kan andre brugere inviteres gennem systemadministrationsoplevelsen i Human Resources. Forsøgsmiljøer indeholder fiktive data, der kan bruges til at udforske programmet på en sikker måde. De ikke er beregnet til brug som produktionsmiljøer. Bemærk, at når et forsøgsmiljø udløber efter 60 dage, slettes alle data i det, og de kan ikke gendannes. Du kan tilmelde dig til et nyt forsøgsmiljø, når det eksisterende miljø udløber.

## <a name="select-a-power-apps-environment"></a>Vælg et Power Apps-miljø

Du kan integrere og udvide brugen af Human Resources-data ved hjælp af Power Apps-værktøjer. Du kan finde oplysninger om Power Apps-miljøer, herunder omfanget af miljøet, adgang til miljøet og oprettelse og valg af et miljø, under [Annoncering af Power Apps-miljøer](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Brug følgende retningslinjer til fastsættelse af, hvilket Power Apps-miljø som Human Resources skal installeres i: 

1. I LCS skal du vælge **Administrer miljøer**. Du kan også gå direkte til Power Apps Administration, hvor du kan se eksisterende miljøer og oprette nye miljøer.

2. Der er knyttet et enkelt Human Resources-miljø til et enkelt Power Apps-miljø.

3. Et Power Apps-miljø indeholder Human Resources sammen med de tilsvarende Power Apps-, Power Automate- og Dataverse-programmer. Hvis Power Apps-miljøet slettes, så slettes apps i det samtidig. Under klargøring af et Human Resources-miljø kan enten et **Prøveversion**- eller **Produktion**-miljø klargøres. Vælg den ønskede type miljø baseret på, hvordan miljøet skal bruges. 

4. Dataintegration og teststrategier, såsom Sandkasse, UAT eller Produktion, bør tages i betragtning. Overvej nøje de forskellige konsekvenser af din installation, da det ikke er let at ændre tilknytningen af Human Resources-miljøer til et Power Apps-miljø.

5. Du kan ikke bruge følgende Power Apps-miljøer til Human Resources. De filtreres fra valglisten i LCS:
 
    - **Standardmiljøer i Power Apps** – Mens hver enkelt lejer automatisk er klargjort med et Power Apps-standardmiljø, anbefales det, at du ikke bruger dem sammen med Human Resources. Alle lejerbrugere kan få adgang til Power Apps-miljøet og utilsigtet beskadige produktionsdata, når de tester og udforsker dem med Power Apps- eller Power Automate-integrationer.
   
    - **Prøvemiljøer** - Disse miljøer oprettes med en udløbsdato. Ved udløb fjernes dit miljø og eventuelle forekomster af Human Resources, der er indeholdt i det, automatisk.
   
    - **Ikke-understøttede områder** - I øjeblikket understøttes Human Resources kun i følgende områder: USA, Europa, Storbritannien, Australien, Canada og Asien.

    > [!NOTE]
    > Human Resources-miljøet klargøres i det samme område, som Power Apps-miljøet klargøres. Overflytning af et Human Resources-miljø til et andet område understøttes ikke.

6. Når du har besluttet, hvilket miljø der er bedst at anvende, kan du fortsætte klargøringsprocessen. 
 
## <a name="grant-access-to-the-environment"></a>Give adgang til miljøet

Som standard har den globale administrator, der oprettede miljøet, adgang til det. Du skal eksplicit tildele andre programbrugere adgang. Du skal tilføje brugere og tildele dem de relevante roller i Human Resources-miljøet. Den globale administrator, der installerede Human Resources, skal også starte både Attract og Onboard for at fuldføre initialiseringen og aktivere adgang for andre lejerbrugere. Før dette er gjort, kan andre brugere ikke få adgang til Attract og Onboard, men får adgangsfejl. Du kan finde flere oplysninger under [Opret nye brugere](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tildel sikkerhedsroller til brugere](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]