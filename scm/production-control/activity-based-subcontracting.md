---
title: Aktivitetsbaseret underleverance
description: "I dette emne beskrives det i detaljer, hvordan du bruger aktiviteter udført af underleverandør i et produktionsflow for lean produktion."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Aktivitetsbaseret underleverance

I dette emne beskrives det i detaljer, hvordan du bruger aktiviteter udført af underleverandør i et produktionsflow for lean produktion.

I Microsoft Dynamics 365 for operationer, der er to metoder til underleverance: produktionsordrer og lean produktion. Det arbejde, der er underleverandører er udformet som en tjeneste, der er relateret til en aktivitet i et produktionsflow indgangsvinkel lean produktion. En særlig type kostprisgruppetype, som hedder **direkte outsourcing** er indført, og de tjenester, der er underleverandører er ikke længere en del af en stykliste (BOM). Omkostningsregnskabet for arbejde udført af underleverandør er fuldt integreret i efterkalkulationsarket løsning til lean produktion.

## <a name="production-flows-that-involve-subcontractors"></a>Produktionsflow, der vedrører underleverandører
Det grundlæggende princip i et produktionsflow ændres ikke, når aktiviteter, der er givet i underentreprise. Materiale, der stadig flyder mellem lokationer, procesaktiviteter konvertere materiale til produkter og overførselsaktiviteter flytte materiale eller produkter fra én placering til en anden. Du kan udforme placeringer og arbejde celler som administreret kreditor ved at tildele kreditorkontoen til et lagersted eller en ressource i en ressourcegruppe.  

Baseret på disse muligheder, kræver ikke lean produktion specifikke funktioner for at understøtte strømmen af materialer og produkter. Alle mulige scenarier, der vedrører kreditorer, som udbydere af produktions- eller transport services kan modelleres baseret på arkitekturen af produktionsflow og -aktiviteter.  

For eksempel fungerer en underleverandør uden for et supermarked, der er placeret i underleverandøren. Når materialehåndteringsenheder er blevet tømt på underleverandøren, returneres kanban-kort til cellen assembly sammen med næste leverance. Supermarked på underleverandøren genopfyldes derefter. Overførsler til og fra underleverandøren kan modelleres som eksplicit overførselsaktiviteter til at understøtte et pluk og leveringsproces. Hvis en eksplicit registrering ikke er påkrævet for at understøtte fysisk transport, udelades overførselsaktiviteter.  

En underleverandør kan bruges til at indlæse balance den samlede kapacitet af produktionsflowet. For eksempel er et produktionsflow udformet ved hjælp af planlagte kanban-regler. Planlæggeren bruger kanban planlægning bord til at planlægge og indlæse niveau både arbejdsceller efter behov. Planlæggeren overvåger også konsoliderede forsyning tidsplanen for supermarked på den **levering plan** side. Flere underleverandører kan modelleres i en eller flere produktionsflow, og der kan være flere kanban-regler, der kan bruges til at levere det samme produkt til det samme sted gennem forskellige aktiviteter. Planlæggeren kan konvertere kanbans til en alternativ kanban-regel til at omplanlægge en kanban, der oprindeligt blev oprettet til intern produktion til en anden proces. Faktisk har underleverandørens arten af arbejdscellen ingen indvirkning på produktionsflowet. Det samme arbejde gælder for to parallelle interne arbejdsceller eller to underleverandørens celler.   

Ligesom enhver anden aktivitet i et produktionsflow, aktiviteter udført af underleverandør kan forbruge og levere fremkomne, ikke-lagerførte (igangværende arbejde \[via\]), og halvfærdige materialer og produkter. I alle tilfælde er processer til planlægning og udførelse af aktiviteter udført af underleverandør det samme. Desuden behandle disse på samme måde som processer for interne arbejde.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Købsprocessen for aktiviteter udført af underleverandør (tjenester)
Købsprocessen for aktiviteter udført af underleverandør er baseret på det fysiske flow til materiale, som er registreret af kanban-job-status, for eksempel, Start eller Afslut. Det økonomiske flow, for eksempel udgifter til arbejde udført af underleverandør, er en sekundær retning, der følger efter det fysiske flow. Købet er på samme tid, en uafhængig proces, der giver mulighed for manuel regulering af købsdokumenter på hvert trin. Her er købsprocessen for aktiviteter udført af underleverandør:

1.  Opret en købsaftale. Købsaftalen er oprettet for tjenesten og forbundet med aktiviteten i produktionsflowet.
2.  Oprette en indkøbsordre. En aftræksordre til køb kan oprettes for den tjeneste, der er baseret på de planlagte kanban-job. Job for den samme tjeneste kan grupperes indkøbsordrelinjer pr. dag, uge eller måned. Købsordrelinjerne kan oprettes når som helst, når der oprettes kanban-job. Også kan oprettes indkøbsordrelinjer efter kendsgerning. Denne indstilling vælges normalt, hvis en underleverandør, der leverer tjenester uden yderligere varsel, baseret på de kanbans eller kanban-kort, der modtager underleverandøren. I så fald kan afvigelser mellem indkøbsordren og fakturaen minimeres.
3.  Generere kanban-kort, materialer og en plukliste, der sendes til underleverandøren at forberede til behandling. Præparatet, som er baseret på den nærmere udformning af produktionsflowet, udføres på kanban-området i forbindelse med procesaktiviteter ved hjælp af pluklisten, og funktionen forberedelse. Også udføres forberedelse på kanban-området til overførselsjob ved hjælp af pluklisten, og start eller afslutning. For fremkomne materiale kan begge processer dokumenteres ved en WMS plukning og forsendelse proces. Du kan oprette en fragtseddel efter behov.
4.  Generere kanban-håndteringsenheder og kanban-kort. Efter behandling returneres kort fra underleverandøren. Kortene, der omfatter normalt en følgeseddel, der angiver det fysiske materiale, der er leveret. En henvisning til de leverede tjenester er ikke påkrævet. Modtagelse af det materiale eller produkt hos kunden er registreret på kanban-området, afhængigt af kanban-kort. (Enten kanban-området i forbindelse med procesaktiviteter eller kanban-området til overførselsjob bruges, afhængigt af de aktiviteter, der er modelleret.).
5.  Oprette en modtagelse rådgivende. Den rådgivende tilgang kan bruges til at erstatte en følgeseddel slip dokument for de modtagne ydelser. Råd om modtagelse kan genereres baseret på afsluttede kanban-job for underleverandører aktivitet for en valgt periode. Råd om oprettes for hver sag-tilgang til relaterede indkøbsordrelinjen. Rådgivende modtagelsen kan udskrives og sendes til underleverandøren som bekræftelse af modtagelsen.
6.  Oprette en faktura.

Processen afsluttes, når underleverandøren, der er faktureret i en periode. Faktura-match sker mod råd om kvittering, der er oprettet. Da modtagelsen meddelelserne repræsenterer den nøjagtige fysiske tilgang af materiale, forenklet trevejs-sammenholdelse.

## <a name="configuring-activities-for-subcontracting"></a>Konfiguration af aktiviteter til underleverance
I følgende afsnit beskrives, hvordan du konfigurerer aktiviteter til underleverance.

### <a name="subcontracted-services"></a>Underleverandørtjenester

Betaling-element, der bruges i aktivitetsbaseret underleverance skal være et produkt, der har følgende egenskaber:

-   **Produkttype:** Service
-   **Lagermodelgruppen:** ikke er på lager

Dette krav gennemtvinger brugen af først i første FIFO-lagermodellen. **Bemærk:** kostprisberegningen produkter kræver, at standardkostprisen for tjenesten defineres. Der kræves en købsaftale med leverandøren. Ellers kan tjenesten ikke bruges til aktivitetsbaseret underleverance.

### <a name="subcontracted-process-activities"></a>Aktiviteter udført af underleverandør

Følg disse trin for at konfigurere en procesaktivitet som en aktivitet, der er underleverandører.

1.  Konfigurere en arbejdscelle for underleverandører. Hvis du vil konfigurere en arbejdscelle, som givet i underentreprise, skal du oprette en ressource af den **leverandør** skrive og knytte den til arbejdscellen (ressourcegruppen). En omkostningsart til kørsel af den **direkte outsourcing** skal have tildelt kostprisgruppetype arbejdscellen. Omkostningsarter til opsætning og mængde er ikke påkrævet.
2.  Når en procesaktivitet oprettet og knyttet til en underleverandør arbejdscelle, skal du konfigurere en tjeneste til aktiviteten, før produktionsflowversionen, der kan aktiveres. Du kan udføre dette trin på den **aktivitet****oplysninger om** side. For aktiviteter, der er knyttet til en underleverandør arbejdscelle, den **Service vilkår** i oversigtspanelet vises. I dette oversigtspanel kan du tilføje standardservice, som gælder for alle varer i output. Hvis varer bestemt output kræver forskellige tjenester eller parametre for beregning af forskellige service (eksempelvis en anden service-forhold), kan du tilføje andre tjenester til aktiviteten.

## <a name="subcontracted-transfer-activities"></a>Underleverandørens overførselsaktiviteter
En overførselsaktivitet er konfigureret som en underleverandør aktivitet, afhængigt af den **Fragtet af** for overførselsaktivitet. Følgende valgmuligheder er tilgængelige:

-   **Afsender** – aktiviteten er givet i underentreprise, hvis overførslen fra lagerstedet administreres af en leverandør (som defineret af en egenskab for lagerstedet). Alle valgte købsaftaler for tjenester skal have den samme leverandør-ID som lagerstedet.
-   **Modtager** – aktiviteten er givet i underentreprise, hvis flytning til lagerstedet administreres af en leverandør (som defineret af en egenskab for lagerstedet). Alle valgte købsaftaler for tjenester skal have den samme leverandør-ID som lagerstedet.
-   **Luftfartsselskab** – aktiviteten er givet i underentreprise til en leverandør, der leverer tjenesten. For at være gyldig, et luftfartsselskab skal oprettes for logistik og skal have et tildelt kreditorkontoen.

For aktiviteter, skal du konfigurere en standardtjeneste til underleverandører overførselsaktiviteter på den **Service vilkår** oversigtspanelet af den **aktivitet****oplysninger om** side.

## <a name="service-quantity-calculation"></a>Beregning af ydelsesmængde
Hele købsprocessen er baseret på en Varereference for en tjeneste. Referencen element måles i en enhed af en tjeneste. Tjenester er normalt måles i antallet tjenester (enheder) eller i gang. Hvis du vil beregne antallet service, baseret på registrerede afslutningen af kanban-job, kan du bruge følgende metoder:

-   **Beregning, der er baseret på antallet af job** – et kanban-job er lig med *n* enheder af tjenesten, uanset det antal, der leveres. Ét job svarer til en materialehåndteringsenhed i lean produktion. Denne beregningsmetode gælder for alle tjenester, der har en fast pris pr. håndteringsenhed. Denne metode anvendes derfor normalt for at overføre aktiviteter. Det kan dog ligeledes anvendelse på aktiviteter, der behandler hele tilgang af materialehåndteringsenheder.
-   **Beregning, der er baseret på antallet** – ydelsesmængden er i forhold til det antal, der er planlagt/leveret. Ved beregning af det angivne produktantal, kan fejl mængder enten medtages eller ej. Denne beregningsmetode gælder for alle de tilfælde, hvor service prisen pr. enhed af forarbejdede produkt er aftalt.
-   **Beregning, der er baseret på aktivitetstiden** – de teoretiske aktivitetstider beregnes baseret på en behandlingstid for aktiviteten, samlet behandlet antal og gennemløbsforhold af det forarbejdede produkt. Denne beregningsmetode gælder for tjenester, der betales pr. time og har en afvigelse i gang pr. produkt.

## <a name="cost-accounting-of-subcontracted-services"></a>Omkostningsregnskab for servicer fra underleverandør
Når der bogføres modtagelsen rådgivende eller kreditorfølgesedlen på en indkøbsordre, der er oprettet af et produktionsflow (med andre ord, en indkøbsordre, der blev oprettet på grundlag af kanban-job for aktiviteter udført af underleverandør), er værdien af modtagelsen efterkalkuleret i IGVA-konti i produktionsflowet. Afvigelser af fakturaer, figurerer også til produktionsflowet. En omkostningsart for arbejde udført af underleverandør er indført. Denne omkostningsart Aktiver gennemsigtige sporing af værdien af arbejde udført af underleverandør, der er allokeret til IGVA og forbruges pr. periode.  

Den efterkalkuleret efterkalkulation af lean produktion i slutningen af en efterkalkulationsversion periode beregner faktiske afvigelser for de produkter, der er fremstillet af produktionsflowet efterkalkulationsarket periode.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modellering overførsler som aktiviteter udført af underleverandør
Personer ofte overveje at transport ikke-produktive og Forestil dig, at det tilføjer nogen værdi. Men når omkostningerne for underleverandørers sammenlignes med interne produktionsomkostninger, omkostningerne ved transport af yderligere aktiviteter skal tages i betragtning. Et produktionsflow, der strækker sig over flere lokationer og kræver trafikbetjening skal modellen transport omkostningerne som en del af omkostningerne ved levering af produkterne til kunden. 

Aktivitetsbaseret underleverance i lean produktion, kan du integrere luftfartsselskaber og transport af kreditorer, der flytter materialer og produkter mellem placeringen af et produktionsflow. Ved at udforme en overførselsaktivitet, kan du tildele et luftfartsselskab eller en kreditor. Overføre aktiviteter/job er baseret på en aftale om service og køb, og du kan oprette indkøbsordrer og råd om tilgang, baseret på de faktiske overførsel af sager. Denne funktionalitet er det samme som funktionalitet for aktiviteter udført af underleverandør.  

Derfor tjenesten Dynamics 365 for operationer, der nu understøtter styklisteberegning, der omfatter transportydelser, oprettelse af relaterede indkøbsordrer, integreret tilgang registrering og integration af transport omkostninger til efterkalkulation af produktionsflow.


