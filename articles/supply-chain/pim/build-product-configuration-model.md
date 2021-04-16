---
title: Oversigt over produktkonfiguration
description: Nødvendigheden af at konfigurere produkter for at opfylde særlige krav er ved at blive reglen frem for undtagelsen i både business-to-business og business-forbruger-relationer.
author: cvocph
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, ConfigPartOf
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ba1fcdffec27e848afaf4b821df85240139f41f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812805"
---
# <a name="product-configuration-overview"></a>Oversigt over produktkonfiguration

[!include [banner](../includes/banner.md)]

Nødvendigheden af at konfigurere produkter for at opfylde særlige krav er ved at blive reglen frem for undtagelsen i både business-to-business og business-forbruger-relationer.

En producent, der understøtter konfigurer til ordre-scenarier, har mulighed for at have større fokus på kundernes behov. Desuden kan producenten ved at oplagre halvfærdige varer i form af generiske komponenter i stedet for færdige produkter, reducere den kapital, der er knyttet til lageret.  

En vellykket flytning fra en fremstil til lager-konfiguration til en konfigurer til ordre-konfiguration kræver omhyggelig analyse af produktstrukturerne, identifikation af produktfamilier og komponentisering. Hvis du vil reducere antallet af dele og minimere antallet af varer, der er i gang, er det vigtigt, at du forstår produktgrænsefladerne, og at du designer til genanvendelighed.  

Der er flere modelleringsprincipper for produktkonfiguration, såsom regelbaseret, dimensionsbaseret og begrænsningsbaseret modellering. Undersøgelser viser, at den begrænsningsbaserede metode kan reducere antallet af kildetekstlinjer i modeller med omkring 50 % sammenlignet med andre modelleringsprincipper. Denne metode kan derfor reducere de samlede ejeromkostninger. Ved at flytte fra en regelbaseret model, der er baseret på X ++-kode til en begrænsningsbaseret model, har du ikke længere brug for en udviklingslicens for at vedligeholde produktmodeller.

## <a name="product-configuration"></a>Produktkonfiguration
Industrialiseringen har ført til gode resultater i fremstillingen af funktionsrige produkter af høj kvalitet til rimelige priser. Stordriftsfordele har gjort det muligt for de fleste mennesker i den industrialiserede del af verden til at købe biler, fjernsyn, husholdningsapparater og andre varer, som de fleste af os betragter som en nødvendig del af vores hverdag.  

Efterhånden som mange produkter er blevet handelsvarer, er der opstået et behov for at skelne mellem dem. Producenternes svar på denne udfordring har været at oprette varianter for hvert produkt, så kunderne får flere alternativer. Denne strategi har ført til øget budgetterede udfordringer, og en forøgelse af lageromkostninger og usolgte produkter, der bliver forældede.  

Ved at implementere en konfigurer til ordre-filosofi har producenter mulighed for at imødekomme kundeefterspørgslen efter unikke produkter samtidig med, at de kan reducere eller fjerne forældede lagervarer. Når en fremstil til lager-filosofi flyttes til en konfigurer til ordre-filosofi, er én umiddelbar udfordring, at behovet for korte leveringstider skal afstemmes i forhold til de lave lagerniveauer.  

Nøglen til succes her er nøje analyse af produktsortimentet og at kigge efter mønstre i både produktfunktioner og -processer. Målet er at identificere generiske komponenter, der kan fremstilles af det samme udstyr og kan bruges i alle varianter.  

Den nye produktkonfigurationsfunktion indeholder en brugergrænseflade (UI), der indeholder en visuel oversigt over produktkonfigurationsmodelstrukturen og en deklarativ begrænsningssyntaks, som ikke behøver at blive kompileret. Derfor kan virksomheder, der ønsker at støtte en fremgangsmåde til konfiguration komme nemmere i gang. Som følgende afsnit forklarer, skal en produktdesigner ikke længere understøttes af en udvikler for at opbygge en model til produktkonfiguration, teste den og udgive den til salgsorganisationen.

## <a name="building-a-product-configuration-model"></a>Bygge en produktkonfigurationsmodel
Der er flere måder, hvorpå en bruger kan opbygge en produktkonfigurationsmodel. En mulighed er at følge en rækkefølge og først at oprette alle referencedataene, såsom produktmastere, specifikke produkter og driftsmæssige ressourcer og derefter medtage dem som komponenter, styklistelinjer, ruteoperationer og andre elementer af produktkonfigurationsmodellen. Du kan også vælge en mere iterativ fremgangsmåde ved først at oprette modellen og derefter tilføje referencedata, efterhånden som behovet opstår.

### <a name="components"></a>Komponenter

En produktkonfigurationsmodel består af en eller flere komponenter, der er bundet sammen via underkomponentrelationer. Komponenterne defineres én gang og kan derefter bruges mange gange i en eller flere produktkonfigurationsmodeller. Komponenterne er de vigtigste byggesten i en produktkonfigurationsmodel og vedrører næsten alle oplysninger om modellen.

### <a name="attributes"></a>Egenskaber

Hver komponent har en eller flere attributter, der identificerer dens egenskaber. Attributterne er, hvad brugerne vælger under konfigurationsprocessen. Attributter styrer både relationer inden og uden for komponenter via medtagelse i begrænsninger eller beregninger. Attributterne kan bruges til at bestemme, hvilke fysiske dele det konfigurere produkt vil bestå af gennem de betingelser, der gælder for styklistelinjer. Desuden kan en attribut kontrollere egenskaben for en styklistelinje via en mekanisme for tilknytning. Der findes lignende funktioner for ruteoperationer med hensyn til både medtagelse og egenskabsindstillinger.

>[!NOTE]
> Når du opretter attributtyper, skal du undgå at oprette et stort antal værdier for attributtypedomænet. Hvis du gør det, kan det medføre, at produktkonfiguratoren kører langsommere. 

### <a name="expression-constraints"></a>Udtryksbegrænsninger

Brug af en begrænsningsbaseret produktkonfigurationsmodel indebærer, at der findes nogle begrænsninger, når brugeren vælger værdier for de forskellige attributter. Sådanne begrænsninger kan implementeres som udtryksbegrænsninger ved hjælp af OML (Optimization Modeling Language). En begrænsning kan også implementeres i form af en tabelbegrænsning.

### <a name="table-constraints"></a>Tabelbegrænsninger

Tabelbegrænsninger kan være brugerdefinerede eller systemdefinerede.  

En brugerdefineret tabelbegrænsning bygges af brugeren. Brugeren vælger en kombination af attributtyper, som repræsenterer kolonnerne i tabellen og indtaster derefter værdierne fra domænerne for de valgte attributtyper for at danne rækkerne i tabelbegrænsningen.  

En systemdefineret tabelbegrænsning defineres ved at vælge, hvilken tabel der skal bruges som reference og derefter vælge felter fra denne tabel for at danne kolonnerne i begrænsningen. Rækker af tabelbegrænsningen er rækkerne i Supply Chain Management-tabellen, der findes på konfigurationstidspunktet.  

En tabelbegrænsning indgår i en produktkonfigurationsmodel ved at referere til tabelbegrænsningsdefinitionen og knytte de relevante attributter i modellen til kolonnerne i tabelbegrænsningen.

### <a name="calculations"></a>Beregninger

Beregninger repræsenterer en mekanisme til at udføre aritmetiske operationer i en produktkonfigurationsmodel. En beregning kan f.eks. bestemme længden af en bestemt råvare eller behandlingstiden for en poleringshandling. Beregningerne er nødvendige og indstiller værdien for en målattribut, når alle de attributværdier, der er inkluderet i beregningsudtrykket, bliver tilgængelige.

### <a name="subcomponents"></a>Underkomponenter

Underkomponenter afspejler noderne i produktkonfigurationsmodelstrukturen. For hver underkomponentrelation skal der være angivet en reference til en produktmaster, der har variantkonfigurationsteknologien konfigureret til begrænsningsbaseret konfiguration.

### <a name="user-requirements"></a>Brugerkrav

Et brugerkrav har alle bestanddelene i en underkomponent. Den eneste forskel er, at et brugerkrav ikke er bundet til en produktmaster. Den praktiske virkning af denne forskel er, at alle styklistelinjer eller ruteoperationer, der er defineret i forbindelse med et brugerkrav, skjules i den overordnede komponentstyklistestruktur eller rute. Denne funktionsmåde ligner funktionen for en fantomstykliste.

### <a name="bom-lines"></a>Styklistelinjer

Styklistelinjer er medtaget for at identificere produktionsstyklisten for hver komponent. En styklistelinje skal referere til en vare, og alle vareegenskaber kan angives til en fast værdi eller knyttes til en attribut.

### <a name="route-operations"></a>Ruteoperationer

Ruteoperationer er medtaget for at identificere produktionsruten. En ruteoperation skal referere til en defineret handling, og alle handlingsegenskaber kan indstilles til en fast værdi. Alle egenskaber bortset fra kildeforudsætninger kan knyttes til en attribut i stedet for en værdi.

## <a name="validating-and-testing-a-product-configuration-model"></a>Validere og teste en produktkonfigurationsmodel
Validering af en produktkonfigurationsmodel kan opstå på flere niveauer i modellen og kan derfor omfatte forskellige områder. Det laveste niveau er for en enkelt udtryksbegrænsning. I så fald udføres validering typisk af produktdesigneren for at kontrollere, at udtrykkets syntaks er korrekt.  

På samme måde kan en betingelse for en styklistelinje eller en ruteoperation valideres i isolation.  

Validering kan også gøres for en brugerdefineret tabelbegrænsningsdefinition. I dette tilfælde kan brugeren kontrollere, at de værdier, der er angivet for hvert felt, er inden i domænet for de tilsvarende attributtyper.  

Endelig kan validering gøres til en komplet produktkonfigurationsmodel for at kontrollere, at den fulde syntaks er korrekt, og at alle navngivnings- og modelleringskonventioner er blevet overholdt.

### <a name="testing"></a>Test

Test af en model er næsten som at køre en faktisk konfigurationssession. Brugeren kan gennemgå konfigurationssiderne, og kontrollere, at modelstrukturen understøtter konfigurationsprocessen. Brugeren kan kontrollere, at værdierne for attributternes er korrekte, og at attributbeskrivelserne hjælper brugeren til at vælge de korrekte værdier. Endeligt, når en testsession er afsluttet, forsøger systemet at oprette styklisten og ruten, der svarer til de valgte attributværdier, og viser en fejlmeddelelse, hvis noget går galt.

### <a name="the-configuration-page"></a>Konfigurationssiden

Du kan flytte mellem komponenter ved at klikke på **Næste** eller klikke på en komponent i modeltræet for produktkonfigurationen for at sætte fokus på den.

## <a name="finalizing-a-model-for-configuration"></a>Fuldføre en model til konfiguration
Når en produktkonfigurationsmodel er klar til at blive brugt i konfigurer til ordre-scenarier, skal der oprettes en version. Der er flere indstillinger, der kan forbedre modelleringsoplevelsen.

### <a name="user-interface"></a>Brugergrænseflade

Konfigurationsbrugergrænsefladen kan ændres ved at indføre attributgrupper i en eller flere underkomponenter. En sådan gruppering kan fremhæve relationerne mellem bestemte attributter og hjælpe brugeren med at identificere området af det produkt, der er i fokus.

### <a name="templates"></a>Skabeloner

En eller flere konfigurationsskabeloner kan oprettes for at fremskynde konfigurationsprocessen. Alternativt kan du oprette skabeloner for at fremme specifikke attributkombinationer, f.eks. når en salgskampagne fokuserer på et bestemt sæt produktfunktioner.

### <a name="translations"></a>Oversættelser

Hvis produktet skal sælges i forskellige lande/områder, kan der oprettes oversættelser for al tekst, der vises i konfigurationsbrugergrænsefladen. Denne tekst indeholder ikke kun navn og beskrivelse, men også attributværdier i tekst.

### <a name="versions"></a>Versioner

Det seneste og vigtigste trin i afslutningsprocessen er at oprette en version af produktkonfigurationsmodellen. Versionen repræsenterer relationen mellem produktmasteren, der kan vælges til konfiguration på en ordre- eller tilbudslinje og produktkonfigurationsmodellen. En version skal være godkendt og aktiveret, før den kan bruges i en konfigurationssession.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Udvide en produktkonfigurationsmodel gennem API
En dedikeret API (application programming interface) er blevet implementeret, så partnere og andre, der har en udviklingslicens kan udvide mulighederne i en produktkonfigurationsmodel. Hovedformålet er at etablere en mekanisme, der gør det muligt for partnere og kunder, der bruger den eksisterende Product Builder til at overføre den kode, der er integreret i Product Builder-modeller til API'en. På denne måde kan de overføre deres modeller fra Product Builder til en produktkonfiguration. Men nye partnere og kunder kan også drage fordel af at bruge API til at udvide nye produktkonfigurationsmodeller.

### <a name="pcadaptor-class"></a>PCAdaptor-klasse

API er implementeret ved hjælp af en række **PCAdaptor**-klasser, der viser datastrukturen i produktkonfigurationsmodeller. En forekomst af **PCAdaptor** klassen skal oprettes for hver model, der skal udvides. Når en konfiguration er fuldført, kontrollerer systemet, om der findes en forekomst af denne klasse og kører den, hvis den findes.  

Følgende flowdiagram viser processen.  

[![Rutediagram](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

API-rutediagram til produktkonfiguration

## <a name="product-configuration"></a>Produktkonfiguration
Produktkonfiguration kan udføres fra følgende steder:

-   Salgsordrelinje
-   Salgstilbudslinje
-   Indkøbsordrelinje
-   Produktionsordrelinje
-   Varebehovslinje (projekt)

Formålet med konfigurationen er at oprette en bestemt variant af det produkt, der opfylder kundens krav. Der oprettes et entydigt konfigurations-id for hver ny konfiguration. Dette id giver mulighed for sporing via lageret.

### <a name="multiple-sites-and-intercompany"></a>Flere steder og internt

Hvis konfigurationen skal udføres på et sted eller endda et firma, der afviger fra det sted eller den virksomhed, hvor produktionen skal foregå, oprettes og placeres styklisten og ruten på stedet for leverandøren i leverandørvirksomheden. Produktvarianten vil blive frigivet i alle virksomheder, der er med i forsyningskæden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]