---
title: Klargøring af Human Resources
description: Dette emne forklarer processen for klargøring af et nyt produktionsmiljø til Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ce30b64bc7c3889347bec94186614bd6cc337f4
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625356"
---
# <a name="provision-human-resources"></a>Klargøring af Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dette emne forklarer processen for klargøring af et nyt produktionsmiljø til Microsoft Dynamics 365 Human Resources. 

## <a name="prerequisites"></a>Forudsætninger

Inden klargøringen af et nyt produktionsmiljø, skal følgende forudsætninger være opfyldt:

- Du har købt Human Resources via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture). Hvis du har en eksisterende Microsoft Dynamics 365-licens, der allerede indeholder Human Resources-serviceplanen, og du ikke kan udføre trinnene i dette emne, kan du kontakte Support.

- Den globale administrator er logget på [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og har oprettet et nyt Human Resources-projekt. 

## <a name="provision-a-human-resources-trial-environment"></a>Klargøre et Human Resources-testmiljø

>[!NOTE]
> Fra og med april 2022 vil testmiljøerne i Human Resources ikke være tilgængelige i det enkeltstående program. Potentielle kunder, der er interesseret i at evaluere Human Resources-funktionerne i programmer til finans og drift, kan gøre dette ved hjælp af den gratis 30-dages prøve sammen med demodataene. Dynamics 365 Finance inkluderer de Human Resources-funktioner, der er hentet til finansinfrastrukturen via fletning af det enkeltstående program. Du kan finde flere oplysninger [Fletning af HR-tilbud samler funktioner for kunder](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Yderligere oplysninger om Dynamics 365 Finance-prøver finder du i den trinvise [vejledning](../fin-ops-core/fin-ops/get-started/before-you-buy.md). 


Før du klargør dit første sandkasse- eller produktionsmiljø, kan det være en god ide at klargøre et [Human Resources-testmiljø](https://go.microsoft.com/fwlink/p/?LinkId=2115962) for at validere funktionen Human Resources. Forsøgsmiljøer indeholder fiktive data, der kan bruges til at udforske programmet på en sikker måde. Selvom et forsøgsmiljø ejes af den bruger, der har anmodet om det, kan andre brugere inviteres gennem systemadministrationsoplevelsen i Human Resources. 

Forsøgsmiljøer giver mulighed for at evaluere personalefunktioner for personer, der ikke allerede har adgang til et Human Resources-miljø. Hvis du klargør et testmiljø, og den godkendte bruger allerede har adgang til et eller flere eksisterende Human Resources-miljøer, bliver brugeren omdirigeret til det eksisterende miljø eller listen over miljøer.

Testmiljøer er ikke beregnet til brug som produktionsmiljøer. De er begrænset til en 30-dages prøveperiode. Når prøveperioden udløber, slettes miljøet og alle data i det, og de kan ikke gendannes. Miljøet kan ikke konverteres til et sandkasse- eller produktionsmiljø. Du kan tilmelde dig til et nyt forsøgsmiljø, når det eksisterende miljø udløber.

Når du opretter et testmiljø i Personale, oprettes der også et Power Apps-forsøgsmiljø i lejeren, som er knyttet til Personale-miljøet. Miljøet, Power Apps, der kaldes "TestDrive", har samme forsøgsperiode som personalemiljøet.

> [!NOTE]
> Klargøring af et testmiljø i Personale mislykkes, hvis den godkendte bruger ikke har rettigheder til at oprette Power Apps-forsøgsmiljøer. Brugeren skal være medtaget i den brugergruppe, der kan oprette testmiljøer i Power Platform-administrationen. Du kan finde flere oplysninger under [Styre, hvem der kan oprette og administrere miljøer i Power Platform-administrationen](/power-platform/admin/control-environment-creation).

## <a name="plan-human-resources-environments"></a>Planlægge miljøer i Human Resources

Før du opretter dit første miljø med Human Resources, skal du planlægge miljøets behov nøje for dit projekt. Et basisabonnement på Human Resources omfatter to miljøer: et produktionsmiljø og et sandkassemiljø. Afhængigt af, hvor kompleks projektet er, kan det være nødvendigt at købe flere sandkassemiljøer for at understøtte projektaktiviteter. 

Overvejelser i forbindelse med yderligere miljøer:

- **Overflytning af data**: Du skal muligvis overveje et ekstra miljø, når der skal bruges dataoverførselsaktiviteter, så dit sandkassemiljø kan bruges til testformål i hele projektet. Et ekstra miljø gør det muligt at fortsætte dataoverflytningsaktiviteter, mens test- og konfigurationsaktiviteter finder sted samtidigt i et andet miljø.
- **Integration**: Du skal muligvis overveje et yderligere miljø for at konfigurere og teste integration. Dette kan omfatte oprindelige integrationer, f.eks. Ceridian Dayforce eller LinkedIn Talent Hub-integrationer, eller brugerdefinerede integrationer, som f.eks. integration med løn, sporingssystemer for ansøgere eller benefit-systemer og -leverandører.
- **Kursus**: Du har muligvis brug for et separat miljø, der er konfigureret med et sæt kursusdata, for at medarbejderne kan bruge det nye system. 
- **Projekt i flere faser**: Du kan have brug for et yderligere miljø for at understøtte konfiguration, overflytning af data, test eller andre aktiviteter i en projektfase, der er planlagt efter projektets første start.

 > [!IMPORTANT]
 > Når du overvejer dit miljø, anbefales følgende:
 > - Brug produktionsmiljøet gennem hele projektet som GOLD-konfigurationsmiljø. Det er vigtigt, fordi du ikke kan kopiere et sandkassemiljø til et produktionsmiljø. Når du går i gang, vil dit GOLD-miljø derfor være dit produktionsmiljø, og du vil udføre de komplette aktiviteter i dette miljø.</br></br>
 > - Brug sandkassen eller et andet miljø til at køre en model af overgangen, før du udgiver. Det kan du gøre ved at opdatere produktionsmiljøet med din GOLD-konfiguration i dit sandkassemiljø.</br></br>
 > - Opbevar en detaljeret tjeckliste for overgangen, som omfatter de enkelte datapakker, der skal bruges til at overflytte de endelige data til produktionsmiljøet i løbet af overgangen til udgivelsen.</br></br>
 > - Brug sandkassemiljøet gennem hele projektet som TEST-miljø. Hvis du har brug for flere miljøer, kan organisationen købe dem for yderligere omkostninger.</br></br>

## <a name="create-an-lcs-project"></a>Oprette et LCS-projekt

Når du vil bruge LCS til at administrere dine Human Resources-miljøer, skal du først oprette et LCS-projekt.

1. Log på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjælp af den konto, som du brugte til dit abonnement på Human Resources.

   > [!NOTE]
   > For at sikre en vellykket klargøring skal den konto, du bruger til klargøring af Human Resources-miljøet, enten tildeles rollen **Systemadministrator** eller **Systemtilpasser** i det Power Apps-miljø, der er tilknyttet Human Resources-miljøet. Se [Konfigurere brugersikkerhed for ressourcer](/power-platform/admin/database-security) for at få flere oplysninger om tildeling af sikkerhedsroller til brugere i Power Platform.

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
    
3. Vælg indstillingen **Inkluder demodata**, hvis du ønsker, at dit miljø skal medtage det demodatasæt, der bruges af prøvemiljøet for Human Resources. Demodata er en fordel for langsigtede demo- eller uddannelsesmiljøer og skal aldrig bruges til produktionsmiljøer. Du skal vælge denne indstilling ved første installation. Du kan ikke opdatere en eksisterende installation senere.

4. Human Resources klargøres altid i et Microsoft Power Apps-miljø for at aktivere Power Apps-integration og -udvidelse. Læs afsnittet "Valg af et Power Apps-miljø" i denne artikel, før du fortsætter. Hvis du ikke allerede har et Power Apps-miljø, skal du vælge "Administrer miljøer i LCS" eller navigere til Power Apps Administration. Følg derefter trinnene for at [Oprette et Power Apps-miljø](/powerapps/administrator/create-environment).

5. Vælg det miljø, du vil klargøre Human Resources til.

6. Vælg **Ja** for at acceptere vilkårene og begynde installationen.

   Det nye miljø vises på listen over miljøer i navigationsruden til venstre. Men du kan ikke begynde at bruge miljøet, før installationsstatus er opdateret til **Installeret**. Denne proces tager typisk få minutter. Hvis klargøringsprocessen mislykkes, skal du kontakte Support.

7. Vælg **Log på Human Resources** for at bruge det nye miljø.

    > [!NOTE]
    > Hvis du endnu ikke har godkendt de endelige krav, kan du installere en testforekomst af Human Resources i projektet. Du kan derefter bruge denne forekomst til at teste din løsning, indtil du kan godkende den. Hvis du bruger det nye miljø til test, skal du gentage denne procedure for at oprette et produktionsmiljø.

## <a name="select-a-power-apps-environment"></a>Vælg et Power Apps-miljø

Du kan integrere og udvide brugen af Human Resources-data ved hjælp af Power Apps-værktøjer. Du kan finde oplysninger om Power Apps-miljøer, herunder omfanget af miljøet, adgang til miljøet og oprettelse og valg af et miljø, under [Annoncering af Power Apps-miljøer](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Brug følgende retningslinjer til fastsættelse af, hvilket Power Apps-miljø som Human Resources skal installeres i: 

1. I LCS skal du vælge **Administrer miljøer**. Du kan også gå direkte til Power Apps Administration, hvor du kan se eksisterende miljøer og oprette nye miljøer.

2. Der er knyttet et enkelt Human Resources-miljø til et enkelt Power Apps-miljø.

3. Et Power Apps-miljø indeholder Human Resources sammen med de tilsvarende Power Apps-, Power Automate- og Dataverse-programmer. Hvis Power Apps-miljøet slettes, så slettes apps i det samtidig. Under klargøring af et Human Resources-miljø kan enten et **Prøveversion**- eller **Produktion**-miljø klargøres. Vælg den ønskede type miljø baseret på, hvordan miljøet skal bruges. 

4. Dataintegration og teststrategier, såsom Sandkasse, UAT eller Produktion, bør tages i betragtning. Overvej nøje de forskellige konsekvenser af din installation, da det ikke er let at ændre tilknytningen af Human Resources-miljøer til et Power Apps-miljø.

5. Følgende Power Apps-miljøer kan ikke anvendes til Human Resources. De filtreres fra valglisten i LCS:
 
    - **Standardmiljøer i Power Apps** – Mens hver enkelt lejer automatisk er klargjort med et Power Apps-standardmiljø, anbefales det, at du ikke bruger dem sammen med Human Resources. Alle lejerbrugere kan få adgang til Power Apps-miljøet og utilsigtet beskadige produktionsdata, når de tester og udforsker dem med Power Apps- eller Power Automate-integrationer.
   
    - **Prøvemiljøer** - Disse miljøer oprettes med en udløbsdato. Ved udløb fjernes dit miljø og eventuelle forekomster af Human Resources, der er indeholdt i det, automatisk.
   
    - **Ikke-understøttede geografier** – Miljøet skal være placeret i en understøttet geografi. Yderligere oplysninger finder du i [Understøttede geografier](hr-admin-setup-provision.md#supported-geographies).

6. Funktioner til dobbeltskrivning for integration af Human Resources-data i Power Apps-miljøet kan kun bruges, hvis indstillingen **Aktivér Dynamics 365-apps** er valgt for miljøet. Se [Startside for dobbeltskrivning](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md) for at få flere oplysninger om dobbeltskrivning.

    > [!NOTE]
    > Indstillingen **Aktivér Dynamics 365-apps** skal være valgt, når Power Apps-miljøet oprettes. Hvis indstillingen ikke er valgt på det tidspunkt, hvor der klargøres, kan du ikke bruge dobbeltskrivning til integration af data mellem Dynamics 365 Human Resources og Power Apps-miljøet eller til at installere Dynamics 365-apps som f.eks. Dynamics 365 Sales og Field Service i miljøet. Denne indstilling kan ikke tilbageføres. Du kan finde flere oplysninger under [Nogle vigtige overvejelser, når du opretter et nyt miljø](//power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment), på Power Platform-dokumentationswebstedet.

7. Når du har besluttet, hvilket miljø der er bedst at anvende, kan du fortsætte klargøringsprocessen. 

### <a name="supported-geographies"></a>Understøttede geografier

Human Resources understøtter i øjeblikket følgende geografier:

- United States
- Europa
- Storbritannien
- Australien
- Canada
- Asien 

Når du opretter et Human Resources-miljø, vælger du et Power Apps-miljø, der skal knyttes til Human Resources-miljøet. Derefter klargøres Human Resources-miljøet i samme Azure-geografi som det valgte Power Apps-miljø. Du kan vælge, hvor Human Resources-miljøet og databasen skal befinde sig fysisk, ved at vælge den geografi, når du opretter det Power Apps-miljø, der skal knyttes til Human Resources-miljøet.

Du kan vælge den *geografi* i Azure, hvor miljøet klargøres, men du kan ikke vælge det specifikke *område* i Azure. Automatisering bestemmer det specifikke område i den geografi, hvor miljøet oprettes, for at optimere belastningsjustering og ydeevne. Du kan finde oplysninger om geografier og områder i Azure i dokumentationen om [Azure-geografier](https://azure.microsoft.com/global-infrastructure/geographies).

Dataene til Human Resources-miljøet vil altid være indeholdt i den Azure-geografi, hvor de oprettes. De vil dog ikke altid være opbevaret i samme Azure-område. Med henblik på katastrofeberedskab replikeres dataene både i det primære Azure-område og i et sekundært failover-område inden for geografien.

 > [!NOTE]
 > Overflytning af et Human Resources-miljø fra et Azure-område til et andet område understøttes ikke.

## <a name="grant-access-to-the-environment"></a>Give adgang til miljøet

Som standard har den globale administrator, der oprettede miljøet, adgang til det. Du skal eksplicit tildele andre programbrugere adgang. Du skal tilføje brugere og tildele dem de relevante roller i Human Resources-miljøet. Du kan finde flere oplysninger under [Opret nye brugere](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tildel sikkerhedsroller til brugere](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
