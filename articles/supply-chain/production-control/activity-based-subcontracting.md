---
title: Aktivitetsbaseret underleverandørarbejde
description: I dette emne beskrives det i detaljer, hvordan du bruger aktiviteter udført af underleverandør i et produktionsflow til lean manufacturing.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35ec47a13d9119c755702e019d09c76e1281b4a6
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250197"
---
# <a name="activity-based-subcontracting"></a>Aktivitetsbaseret underleverandørarbejde

[!include [banner](../includes/banner.md)]

I dette emne beskrives det i detaljer, hvordan du bruger aktiviteter udført af underleverandør i et produktionsflow til lean manufacturing.

I Microsoft Dynamics 365 Supply Chain Management er der to metoder til underleverandørarbejde: produktionsordrer og lean manufacturing. Med lean manufacturing-metoden er underleverandørarbejdet udformet som en tjeneste, der er relateret til en aktivitet i et produktionsflow. En særlig kostprisgruppetype, **Direkte outsourcing**, er blevet indført, og de tjenester, der udføres af underleverandører, er ikke længere en del af en stykliste (BOM). Omkostningsregnskabet for arbejde udført af underleverandør er fuldt integreret i efterkalkulationsløsningen til lean manufacturing.

## <a name="production-flows-that-involve-subcontractors"></a>Produktionsflows, der vedrører underleverandører
Det grundlæggende princip i et produktionsflow ændres ikke, når aktiviteter gives i underentreprise. Materiale flyder stadig mellem lokaliteter, procesaktiviteter konverterer materiale til produkter og overførselsaktiviteter flytter materiale eller produkter fra ét sted til et andet. Du kan modellere steder og arbejdsceller som kreditoradministreret ved at tildele kreditorkontoen til et lagersted eller en ressource i en ressourcegruppe.  

På basis af disse muligheder kræver lean manufacturing ikke specifikke funktioner for at understøtte strømmen af materialer og produkter. Alle mulige scenarier, der vedrører kreditorer som udbydere af produktions- eller transporttjenester, kan modelleres ud fra arkitekturen af produktionsflowet og -aktiviteter.  

For eksempel arbejder en underleverandør for et supermarked i nærheden af underleverandøren. Når materialehåndteringsenheder er blevet tømt hos underleverandøren, returneres kanban-kort til assemblycellen sammen med næste forsendelse. Supermarkedet hos underleverandøren genopfyldes derefter. Overførsler til og fra underleverandøren kan modelleres som eksplicitte overførselsaktiviteter for at understøtte en pluk- og forsendelsesproces. Hvis en eksplicit registrering ikke er påkrævet for at understøtte den fysiske transport, kan overførselsaktiviteterne udelades.  

En underleverandør kan bruges til at justere belastningen af produktionsflowets samlede kapacitet. For eksempel modelleres et produktionsflow ved hjælp af planlagte kanban-regler. Planlæggeren bruger kanban-planlægningsområdet til at planlægge og afbalancere begge arbejdsceller efter behov. Planlæggeren overvåger også den konsoliderede forsyningstidsplan for supermarkedet på siden **Forsyningsplan**. Flere underleverandører kan modelleres i et eller flere produktionsflow, og der kan være flere kanban-regler, der kan bruges til at levere det samme produkt til det samme sted gennem forskellige aktiviteter. Planlæggeren kan konvertere kanbans til en alternativ kanban-regel for at omplanlægge en kanban, der oprindeligt blev oprettet til intern produktion til en anden proces. Faktisk har arbejdscellens art af underleverandør ingen indvirkning på produktionsflowet. Det samme arbejdsprincip gælder for to parallelle interne arbejdsceller eller to underleverandørceller.   

Som ved enhver anden aktivitet i et produktionsflow kan aktiviteter udført af underleverandør forbruge og levere lagerført, ikke-lagerførte (igangværende arbejde \[IGVF\]) og halvfærdige materialer og produkter. I alle tilfælde er processer til planlægning og udførelse af aktiviteter udført af underleverandør de samme. Desuden behandler disse det samme som processerne for internt arbejde.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Indkøbsproces for aktiviteter udført af underleverandør (tjenester)
Købsprocessen for aktiviteter udført af underleverandør er baseret på det fysiske flow af materiale, som er registreret af kanban-job-status, for eksempel, Start eller Afsluttet. Det økonomiske flow, for eksempel omkostninger ved arbejde udført af underleverandør, er et sekundær flow, der efterfølger det fysiske flow. Samtidig er indkøbsprocessen en uafhængig proces, der giver mulighed for manuel regulering af købsdokumenterne på hvert trin. Her er indkøbsprocessen for aktiviteter udført af underleverandør:

1.  Oprette en købsaftale. Købsaftalen oprettes for tjenesten og forbindes med aktiviteten i produktionsflowet.
2.  Oprette en indkøbsordre. En aftræksindkøbsordre kan oprettes for tjenesten baseret på de planlagte kanban-job. Job for den samme tjeneste kan grupperes som indkøbsordrelinjer pr. dag, uge eller måned. Købsordrelinjerne kan oprettes når som helst, når kanban-jobbene er oprettet. Indkøbsordrelinjer kan også oprettes efter faktoren. Denne mulighed vælges normalt, hvis en underleverandør leverer tjenester uden yderligere varsel, baseret på de kanbans eller kanban-kort, som underleverandøren modtager. I så fald kan afvigelser mellem indkøbsordren og fakturaen minimeres.
3.  Generere kanban-kort, materialer og en plukliste, der sendes til underleverandøren med henblik på forberedelse af behandling. Baseret på den nærmere modellering af produktionsflowet udføres forberedelsen på kanban-området i forbindelse med procesaktiviteter ved hjælp af pluklisten og forberedelsesfunktionen. Forberedelse kan også udføres på kanban-området for overførselsjob ved hjælp af pluklisten og start eller afslutning. For lagerført materiale kan begge processer understøttes med en WMS-pluk- og forsendelsesproces. Du kan oprette en fragtseddel ved behov.
4.  Generere kanban-håndteringsenheder og kanban-kort. Efter behandlingen returneres kort fra underleverandøren. Kortene omfatter normalt en følgeseddel, der angiver det fysiske materiale, der er leveret. En reference til de leverede tjenester er ikke påkrævet. Modtagelse af materialet eller produktet hos kunden registreres på kanban-området, afhængigt af kanban-kortene. (Enten bruges kanban-området i forbindelse med procesaktiviteter eller kanban-området til overførselsjob, afhængigt af de aktiviteter, der er modelleret).
5.  Oprette en modtagelsesadvisering. Modtagelsesadviseringen kan bruges til at erstatte en følgeseddel for de modtagne tjenesteydelser. Modtagelsesadviseringer kan genereres baseret på afsluttede kanban-job for underleverandøraktiviteten for en valgt periode. For hver jobtilgang oprettes adviseringer for den relaterede indkøbsordrelinje. Modtagelsesadviseringen kan udskrives og sendes til underleverandøren som bekræftelse af modtagelsen.
6.  Generere en faktura.

Processen afsluttes, når underleverandøren faktureres for en periode. Fakturasammenholdelsen sker mod de modtagelsesadviseringer, der er oprettet. Da modtagelsesadviseringerne repræsenterer den nøjagtige fysiske tilgang af materiale, forenkler det trevejs-sammenholdelsen.

## <a name="configuring-activities-for-subcontracting"></a>Konfiguration af aktiviteter til underleverandørarbejde
I følgende afsnit beskrives, hvordan du konfigurerer aktiviteter til underleverandørarbejde.

### <a name="subcontracted-services"></a>Underleverandørtjenester

Det betalingselement, der bruges i aktivitetsbaseret underleverandørarbejde, skal være et produkt, der har følgende egenskaber:

-   **Produkttype:** Tjeneste
-   **Lagermodelgruppe:** Ikke på lager

Dette krav gennemtvinger brugen af FIFO-lagermodellen (FIFO – First In, First Out). **Bemærk:** Kostprisberegningen af produkterne kræver, at standardkostprisen for tjenesten defineres. Der kræves en købsaftale med leverandøren. Ellers kan tjenesten ikke bruges til aktivitetsbaseret underleverandørarbejde.

### <a name="subcontracted-process-activities"></a>Procesaktiviteter udført af underleverandør

Følg disse trin for at konfigurere en procesaktivitet som en aktivitet udført af underleverandør.

1.  Konfigurer en underleverandørarbejdscelle. Hvis du vil konfigurere en arbejdscelle som udført af underleverandør skal du oprette en ressource af typen **Leverandør** og knytte den til arbejdscellen (ressourcegruppen). En kørselsomkostningsart for kostprisgruppetypen **Direkte outsourcing** skal tildeles til arbejdscellen. Omkostningskategorierne til opsætning og antal er ikke påkrævet.
2.  Når en procesaktivitet er oprettet og knyttet til en underleverandørarbejdscelle, skal du konfigurere en tjeneste til aktiviteten, før produktionsflowversionen kan aktiveres. Du kan udføre dette trin på siden **Aktivitets** **detaljer**. For aktiviteter, der er knyttet til en underleverandørarbejdscelle, vises oversigtspanelet **Servicebetingelser**. I dette oversigtspanel skal du tilføje en standardservice, som gælder for alle slutvarer. Hvis bestemte slutvarer kræver andre services eller andre parametre for beregning af servicen (eksempelvis en anden servicegrad), kan du tilføje andre services til aktiviteten.

## <a name="subcontracted-transfer-activities"></a>Overførselsaktiviteter udført af underleverandør
En overførselsaktivitet konfigureres som en underleverandøraktivitet, afhængigt af indstillingen **Fragtet af** for overførselsaktiviteten. Følgende valgmuligheder er tilgængelige:

-   **Afsender** – Aktiviteten gives i underentreprise, hvis overførslen fra lagerstedet administreres af en leverandør (som defineret af en egenskab for lagerstedet). Alle valgte købsaftaler for tjenester skal have det samme leverandør-ID som lagerstedet.
-   **Modtager** – Aktiviteten gives i underentreprise, hvis overførslen til lagerstedet administreres af en leverandør (som defineret af en egenskab for lagerstedet). Alle valgte købsaftaler for tjenester skal have det samme leverandør-ID som lagerstedet.
-   **Fragtmand** – Aktiviteten gives i underentreprise til den leverandør, der leverer tjenesten. For at være gyldig skal en fragtmand oprettes for lokationsstyring og skal have en tildelt kreditorkonto.

For procesaktiviteter skal du konfigurere en standardtjeneste til overførselsaktiviteter udført af underleverandør i oversigtspanelet **Servicebetingelser** på siden **Aktivitets** **detaljer**.

## <a name="service-quantity-calculation"></a>Beregning af ydelsesmængde
Hele indkøbsprocessen er baseret på en varereference for en tjeneste. Varereferencen måles i en måleenhed for en tjeneste. Tjenester måles normalt i antal tjenester (enheder) eller i tid. Hvis du vil beregne ydelsesmængden baseret på den registrerede afslutning af kanban-job, kan du bruge følgende metoder:

-   **Beregning, der er baseret på antallet af job** – Ét kanban-job er lig med *n* enheder af tjenesten, uanset det produktantal der leveres. Ét job svarer til én materialehåndteringsenhed i lean manufacturing. Denne beregningsmetode gælder for alle tjenester, der har en fast pris pr. håndteringsenhed. Denne metode anvendes derfor normalt til overførselsaktiviteter. Den kan dog ligeledes anvendelse på aktiviteter, der behandler hele materialehåndteringsenheder.
-   **Beregning, der er baseret på produktantallet** – Ydelsesmængden beregnes i forhold til det produktantal, der er planlagt/leveret. Ved beregning af det leverede produktantal kan fejlantal enten medtages eller ej. Denne beregningsmetode gælder for alle de tilfælde, hvor serviceprisen pr. enhed af det forarbejdede produkt er aftalt.
-   **Beregning, der er baseret på aktivitetstiden** – De teoretiske aktivitetstider beregnes baseret på behandlingstiden for aktiviteten, samlet behandlet antal og gennemløbsforhold for det forarbejdede produkt. Denne beregningsmetode gælder for tjenester, der betales pr. time og har en tidsmæssig afvigelse pr. forarbejdet produkt.

## <a name="cost-accounting-of-subcontracted-services"></a>Omkostningsregnskab for servicer fra underleverandør
Når modtagelsesadviseringen eller kreditorfølgesedlen for en indkøbsordre, der er oprettet til et produktionsflow (med andre ord, en indkøbsordre, der blev oprettet på grundlag af kanban-job for aktiviteter udført af underleverandør), bogføres, efterkalkuleres værdien af modtagelsen på IGVA-konti i produktionsflowet. Afvigelser i fakturaer efterkalkuleres også til produktionsflowet. En omkostningsart for arbejde udført af underleverandør er indført. Denne omkostningsart aktiverer gennemsigtig sporing af værdien af arbejde udført af underleverandør, der er allokeret til IGVF og forbrugt pr. periode.  

Det efterkalkulerede varetræk for lean manufacturing i slutningen af en efterkalkulationsperiode beregner faktiske afvigelser for de produkter, der er fremstillet af produktionsflowet i efterkalkulationsperioden.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modellering overføres som aktiviteter udført af underleverandør
Folk betragter ofte transport som ikke-produktivt og mener, at det ikke tilføjer nogen værdi. Men når omkostningerne ved underleverandørarbejde sammenlignes med interne produktionsomkostninger, skal omkostningerne ved yderligere transportaktiviteter tages i betragtning. Et produktionsflow, der strækker sig over flere lokationer og kræver transporttjenester, skal modellere transportomkostningerne som en del af omkostningerne ved levering af produkterne til kunden. 

Med aktivitetsbaseret underleverandørarbejde i lean manufacturing kan du integrere fragtmænd og transportleverandører, der flytter materialer og produkter mellem et produktionsflows lokationer. Ved at modellere en overførselsaktivitet kan du tildele en fragtmand eller en leverandør. Overførselsaktiviteterne/jobbet er baseret på en aftale om service og køb, og du kan oprette indkøbsordrer og modtagelsesadviseringer baseret på de faktiske overførselsjob. Denne funktionalitet er den samme som funktionaliteten for procesaktiviteter udført af underleverandør.  

Supply Chain Management understøtter nu styklisteberegning, der omfatter transportydelser, oprettelse af relaterede indkøbsordrer, integreret registrering af modtagelser og integration af transportomkostninger i efterkalkulation af produktionsflow.



