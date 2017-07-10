---
title: Opgradere Dynamics AX 2012 til Dynamics 365 for Finance and Operations, Enterprise edition
description: "Dette emne beskriver den proces, som kunder, der aktuelt kører Microsoft Dynamics AX 2012, kan bruge til at flytte deres data og kode til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: da-dk
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Opgradere Microsoft Dynamics AX 2012 til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition

[!include[banner](../includes/banner.md)]

I platformsopdatering 8, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, findes en opgraderingssti, som kunder, der aktuelt kører Microsoft Dynamics AX 2012, kan bruge til at flytte data og kode til Finance and Operations. Opgraderingsprocessen bygger på følgende elementer:

- Værktøjer til overførsel af eksisterende brugerdefineret programkode fra AX 2012.
- En dataopgradering, som du kan bruge til at overføre din database. Derfor kan du opgradere hele din transaktionshistorik.

## <a name="overview"></a>Overblik

Den overordnede opgraderingsproces kan visualiseres som tre overordnede faser: analyse, kørsel og validering.

I følgende diagram vises processen for hele opgraderingen og de aktiviteter, der regnes for en del af hver fase. 

![Opgraderingsproces](./media/upgrade-process.png)

## <a name="analyze"></a>Analyser

Aktiviteterne i analysefasen hjælper dig med at estimere den indsats, der kræves til opgradering. De hjælper dig også med at forberede en projektplan. Disse aktiviteter kan udføres, før du køber Finance and Operations. De hjælper dig med at træffe en velbegrundet købsbeslutning ved at angive et datapunkt om tidsforbrug og ressourcer, der kræves.

### <a name="sign-up-for-a-public-preview-in-lcs"></a>Tilmelde dig en offentlig prøveversion i LCS

Du kan udføre analyseaktiviteter, før du køber Finance and Operations, ved at tilmelde dig en offentlig prøveversion. Med den offentlige prøveversion kan du installere dine egne Finance and Operations-miljøer. Den giver også adgang til de værktøjer i Microsoft Dynamics Lifecycle Services (LCS), der bruges til at vurdere dit AX 2012-miljø og din eksisterende brugerdefinerede kode.

Hvis du har et eksisterende LCS-projekt til AX 2012, skal du stadig tilmelde dig et yderligere nyt projekt til evaluering af Finance and Operations.

Oplysninger om, hvordan du får en offentlig prøveversion for debitorer, findes på https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Oplysninger om, hvordan du får en offentlig prøveversion for partnere, findes på https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Vær opmærksom på, at denne offentlige prøveversion adskiller sig fra en [30-dages prøveversionen](https://aka.ms/D365OperationTrials). 30-dages prøveversioner giver en installeret forekomst af Finance and Operations, du kan bruge til at udforske og evaluere programmet. Analyseaktiviteter kræver dog fulde LCS-funktioner og -værktøjer.

### <a name="select-the-upgrade-methodology"></a>Vælge opgraderingsmetoden
I dit nye LCS-projekt skal du angive projektmetoden til **Opgradere AX 2012 til Dynamics 365 for Operations**. Denne metode er beregnet specifikt til AX 2012-kunder, der opgraderer. Den beskriver de tre faser detaljeret og har links til al den understøttende dokumentation om processen.

![Opgraderingsmetode(./media/methodology.png)
 
### <a name="run-the-upgrade-analyzer"></a>Køre opgraderingsanalysen
Værktøjet til opgraderingsanalyse kører i dit AX 2012-miljø og identificerer de opgaver, du skal udføre for at klargøre AX 2012-miljøet, så opgraderingen bliver nemmere og mindre dyr:

- **Dataoprydningen** – Denne proces identificerer data, du kan fjerne uden at forårsage tab af funktionalitet. Værktøjet identificerer forskellige typer af data, du kan reducere ved at køre en oprydningsproces. For hver type af data gives en forklaring på virkningen af oprydningen. Du kan derefter afgøre, om du vil køre oprydningsprocessen. En del af omkostningerne til dit abonnement på Finance and Operations er baseret på databasestørrelse. Derfor kan du ved at reducere størrelsen reducere denne komponent i abonnementsomkostningerne og også minimere den tid, der kræves til opgraderingsprocessens opstart. En mindre database sikrer en hurtigere opgradering.
- **SQL-konfiguration** – Denne proces gennemgår SQL-konfigurationen og anbefaler optimering. Ved at sikre, at SQL fungerer optimalt, er denne proces med til at reducere den tid, der kræves til opgraderingsprocessens opstart.
- **Forældede funktioner** – Denne proces identificerer funktioner, som du bruger i øjeblikket, men som ikke er tilgængelige i Finance and Operations. Processen kan derfor tidligt opdage huller i funktionaliteten. Den giver også forslag til alternativer.

Desuden, som en del af dette trin, skal du installere KBXXXXXXX i AX 2012-miljøet. Dette hotfix indeholder en føropgraderingskontrolliste. Du kan bruge denne kontrolliste til at indtaste data, der kræves til opgraderingsproceduren, i AX 2012-miljøet. I en opgave på føropgraderingskontrollisten kan du f.eks. angive Microsoft Azure Active Directory-logonoplysninger (AD Azure) for hver aktuelle AX 2012-bruger, så hver bruger kan logge på Finance and Operations.

Resultatet af dette trin bliver arbejdsstrømmen i opgraderingsprojektplanen for systemadministratorer i AX 2012.

Yderligere oplysninger finder du i [Analyse: bruge opgraderingsanalyse til planlægning af overførselsarbejde](upgrade-analyzer-tool.md).

### <a name="run-the-code-upgrade-estimation-tools"></a>Køre estimeringsværktøjerne til opgradering af kode
Dette trin tager din kode fra AX 2012, konverterer den til det nye format og giver feedback om konflikter, som en udvikler skal løse senere. Dette trin er udgangspunktet for estimering af omkostningerne ved kodeopgraderingen.

For at fuldføre dette trin skal du eksportere din kode fra AX 2012 som en modellagereksport og overføre den til LCS-opgraderingsværktøjet. Værktøjet til kodeopgradering giver en opgraderet version af din kode og en rapport om de resterende konflikter, der skal løses. Udvikleren kan derefter gennemgå både opgraderingskoden og rapporten for at bestemme den indsats, der kræves med henblik på at opgradere din kodebase.

Resultatet af dette trin bliver arbejdsstrømmen i opgraderingsprojektplanen for Microsoft Dynamics AX-udviklere.

Yderligere oplysninger finder du i [Analyse: anslå indsatsen for at opgradere kode](analyze-code-upgrade.md).

### <a name="deploy-a-demo-environment"></a>Installere et demomiljø
Demomiljøer er standardmiljøer, der indeholder demonstrationsdata (ikke dine egne data) og standardkode (nogen tilpasninger). Det anbefales, at du installerer et demomiljø for at evaluere de nye funktioner og udføre en grundlæggende Gab-analyse af tilpasning af standardprocesser, der bruges i AX 2012, men kan være ændret i Finance and Operations. Du kan enten installere disse demomiljøer i Azure eller hente dem som en virtuel maskine (VM), som du kan køre på din egen hardware. Hvis du installerer dem i Azure, skal du angive dit Azure-abonnement, fordi du stadig bruger et offentligt prøveversionsprojekt og endnu ikke har købt et abonnement til Finance and Operations.

Resultatet af dette trin bliver arbejdsstrømmen i opgraderingsprojektplanen for dine funktionsbrugere eller virksomhedsbrugere.

Yderligere oplysninger finder du i [Analyse: Installere et sandkassemiljø](analysis-sandbox.md)

### <a name="create-a-project-plan"></a>Oprette en projektplan
En skabelon til en projektplan findes i opgraderingsmetoden. I dette trin bruges outputtet fra de forrige trin i analysefasen til at udfylde projektplanen for opgraderingsprojektet. Projektplanen indeholder også alle testoplysninger: dataopgraderingstest, overgangstest, funktionelle gentagelser af testgennemløb og detaljer om de forskellige ressourcetildelinger for disse opgaver.

På dette stadium indeholder projektplanen et datapunkt, der kan give dig indsigt i den tid og omkostning, som en opgradering til Finance and Operations omfatter.

## <a name="execute"></a>Udfør
Under udførelsesfasen kan du arbejde dig gennem de opgaver, du har planlagt i analysefasen. Før du kan gå til udførelsesfasen, skal du købe Finance and Operations, og du skal have tilgængelige ressourcer, der kan arbejde på opgraderingen.

### <a name="switch-to-the-lcs-implementation-project"></a>Skifte til LCS-implementeringsprojektet
Det offentlige prøveversionsprojekt, som du brugte i analysefasen, har tjent sit formål. Du kan nu slette det. Til de resterende trin skal du kun bruge den projektplan, du oprettede i det sidste trin af analysefasen.

Når du køber et abonnement på Finance and Operations, får du vist detaljer om, hvordan du bliver tilmeldt et nyt LCS-projekt. Dette projekt kaldes et implementeringsprojekt og bliver det nye permanente LCS-projekt for dit abonnement, så længe du har dette abonnement. Dette projekt er forskelligt fra det offentlige prøveversionsprojekt, da det administreres af Microsoft. Dette har projektet følgende egenskaber:

- Alle miljøer i projektet har Azure som vært.
- Abonnementet på Azure, der er tilknyttet projektet, administreres af Microsoft. Derfor er der ingen særskilt fakturering for Azure omkostninger. Omkostningerne er dækket af abonnementet på Finance and Operations.
- Produktionsmiljøet i projektet vedligeholdes af Microsoft. Derfor køres kodeinstallationer, opgraderinger og vedligeholdelse af infrastrukturen direkte af Microsoft, ikke af dine medarbejdere. 

### <a name="perform-the-ax-2012-preparation-tasks"></a>Udføre AX 2012-forberedelsesopgaverne
Udfør de opgaver, der blev opdaget af opgraderingens analyseværktøj, og som er beskrevet i projektplanen for opgradering. Din Microsoft Dynamics AX-systemadministrator og -databaseadministrator (DBA) skal udføre disse opgaver.

[Opgradering af data fra AX 2012 til Dynamics 365 for Operations – Føropgraderingskontrolliste i AX 2012](prepare-data-upgrade.md)

### <a name="perform-code-upgrade"></a>Udføre opgradering af kode
Udfør de opgaver, der blev planlagt under estimeringstrinnet til opgradering af kode i analysefasen. Dine udviklere skal udføre disse opgaver.

Fra dette punkt og fremad bør du fastfryse kodeændringer i AX 2012. Der må kun tillades nødstilfælde af kodeændringer i AX 2012. Hvis der foretages en ændring, skal den overføres manuelt til den nye kodebase.

### <a name="develop-new-code"></a>Udvikle ny kode
Udfør opgaver fra den Gab-analyse af tilpasning, der blev udført under trinnet "Installere et demomiljø" i analysefasen. Disse opgaver vil sandsynligvis være en blanding af funktionelle opgaver, der definerer konfigurations- og udviklingsopgaver for tilpasninger, der er relateret til nye funktioner, der hentes op.

### <a name="data-upgrade-development-environment"></a>Dataopgradering (udviklingsmiljø)
Når dine kodeopgraderingsopgaver er fuldført, kan du opgradere AX 2012-databasen til Finance and Operations for første gang. Denne første opgradering sker i et udviklingsmiljø, så du lettere kan afhjælpe eller fejlfinde eventuelle problemer, der findes på dette stadie. I et udviklingsmiljø kan der straks foretages fejlfinding af et problem, kode kan reguleres, og opgraderingen kan køres igen på få minutter. Miljøer med større sandkasse giver ikke denne smidighed, og det tager flere timer at fejlfinde og afhjælpe problemer, opdatere koden, installere den opdaterede kode og køre opgraderingen igen.

Følgende illustration viser processen. Du skal sikkerhedskopiere AX 2012-databasen, overføre den til Azure, gendanne den i Finance and Operations-miljøet og derefter køre dataopgraderingen.

![Dataopgradering i et udviklingsmiljø](./media/data-upgrade-dev.png)
 
Opgradering af data sker via en særlig type installationspakke. Den samme mekanisme bruges til at installere ny Finance and Operations-kode fra ét miljø til et andet miljø.

Den underliggende struktur, der bruges til at konvertere dataene i databasen under denne proces, er stort set den samme som opgraderingsstrukturen i AX 2012, der er baseret på X ++ batchjob, der kører **ReleaseUpdatexxx** klasser.

Yderligere oplysninger finder du i [Dataopgradering fra AX 2012 til Dynamics 365 for Operations i et udviklingsmiljø](data-upgrade-2012.md).

### <a name="data-upgrade-sandbox-environments"></a>Opgradering af data (sandkassemiljø)
Når dataopgraderingen i et udviklingsmiljø er fuldført, kan den samme proces køres i et sandkassemiljø. Sandkassemiljøet er det miljø, hvor virksomhedsbrugere og funktionelle teammedlemmer kan teste forretningsprocesser ved hjælp af opgraderede AX 2012-data og kode.

I følgende illustration vises processen for kørsel af dataopgraderingen i et sandkassemiljø. Forskellen her er, at værktøjet bacpac bruges i stedet for en traditionel SQL-sikkerhedskopi. Dette værktøj kræves for at konvertere mellem Microsoft SQL Server og Azure SQL-databasen. Det er et SQL-standardværktøj, som ikke er specifikt for Finance and Operations.

![Opgradering af data i et sandkassemiljø](./media/data-upgrade-sandbox.png)

Yderligere oplysninger finder du i [Dataopgradering fra AX 2012 til Dynamics 365 for Operations i et sandkassemiljø](upgrade-data-sandbox.md).
 
## <a name="validate"></a>Kontroller
Når du går ind i valideringsfasen, har du tilgængelige miljøer, der indeholder din opgraderede brugerdefinerede kode og dine opgraderede data. Denne fase beskriver processen til validering og test af, om det opgraderede miljø fungerer som ønsket. Processen med at forberede udgivelsen beskrives også.

### <a name="perform-cutover-testing-and-create-a-cutover-plan"></a>Foretage overgangstest og oprette en overgangsplan
Betegnelsen _overgang_ bruges til at beskrive den sidste proces for publicering af det nye system. Denne proces består af de opgaver, der opstår, når AX 2012 er slået fra, og før Finance and Operations er aktiveret. 

Formålet med testen er at afprøve overgangsprocessen. På denne måde er du med til at sikre, at alle, der er involveret i den faktiske overgang til publicering, får en problemfri oplevelse.

Der findes to primære arbejdsstrømme:

- **Teknisk arbejdsstrøm** – Denne arbejdsstrøm er den proces, der kører dataopgraderingen. Virksomheden gennemtvinger en grænse for mængden af nedetid, der er tilladt. I denne nedetid vil hverken AX 2012 eller Finance and Operations være tilgængelig. Den tekniske arbejdsstrøm skal eventuelt tilpasse ydeevnen af dataopgraderingsproceduren for at imødekomme en virksomheds nedetidsgrænse. 
- **Funktionel arbejdsstrøm** – Efter dataopgraderingen kræves flere konfigurationsopgaver i Finance and Operations-miljøet. Alle disse opgaver skal dokumenteres og kvantificeres, og en ressource skal tildeles dem, fordi de skal passe til de tekniske opgaver i virksomhedens nedetidsgrænse.

Der er flere oplysninger i 
- [Validere: Overgangstest](upgrade-cutover-testing.md)
- [Validere: Valideringsproces for app](app-validation-process.md)

### <a name="functional-test-pass"></a>Funktionelt testgennemløb
Udfør et fuldt funktionelt testgennemløb af alle forretningsprocesser. Dette testgennemløb er en omfattende gentest af alle forretningsprocesser, der involverer Finance and Operations. Disse forretningsprocesser omfatter både gamle processer, der blev overført fra AX 2012, og nye processer, der omfatter nye funktioner, der er indført for første gang i Finance and Operations. 

Afhængig af kodekvalitet kan afhjælpning af problemer og gentest måske kræve flere gentagelser af det funktionelle testgennemløb. Når et problem er løst, skal du vil genteste alle processer, der er involveret, for at sikre, at downstream- eller upstream-processen ikke er påvirket af ændringen.

Yderligere oplysninger finder du i [Validere: Funktionel test](upgrade-functional-validation.md).

### <a name="pre-go-live-checklist"></a>Kontrolliste før udgivelse
Kontrollisten før udgivelse er en anbefalet procedure, der kan hjælpe med at reducere risikoen for fejl under den endelige overgang til udgivelse. En uge før publicering skal du stoppe for konfigurationsændringer i AX 2012 (dvs. under \<modul\>\Setup). Denne begrænsning for ændringer i konfigurationen er blot proceduremæssig. Microsoft Dynamics AX-systemadministratorer skal være enige om at sætte ændringer af denne type på hold på dette tidspunkt.

Det anbefales, at du også fastfryser kodeændringer i Finance and Operations-kodebasen. Ingen yderligere ændringer bør tillades, medmindre de er evalueret og har vist sig ikke at blokere for publicering.  

Efter konfigurationsbegrænsning og fastfrysning af kode er på plads, skal dataopgradering køres en sidste gang inden overgangen. På denne måde kan du sikre dig, at alt stadig fungerer som forventet. 

Yderligere oplysninger finder du i [Validere: Klargøring til udgivelse](upgrade-go-live-prep.md).



### <a name="supported-upgrade-paths"></a>Understøttede opgraderingsstier
Fra og med juni 2017 er opgradering til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, version 0617 understøttet fra Microsoft Dynamics AX 2012 R3. Alle samlede opdateringer af AX 2012 R3 understøttes.

Microsoft Dynamics AX 2012 R2 og Microsoft Dynamics AX 2012 RTM understøttes ikke i øjeblikket. Der tilføjes understøttelse senere i 2017.

Kun opgradering til den skyinstallerede version af Finance and Operations understøttes. Opgradering til den lokale version understøttes ikke. Understøttelse af opgradering til den lokale version tilføjes senere i 2017.

