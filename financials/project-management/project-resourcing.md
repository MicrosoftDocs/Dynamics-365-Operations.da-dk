---
title: Projektressourcer
description: Dette emne indeholder oplysninger om finansiere projektet.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Projektressourcer

Dette emne indeholder oplysninger om finansiere projektet.

En udfordring for projektledere og ressourceledere under projektet planlægningsstadiet er ressourceallokering, hvor de skal finde ud af, og reservere den rigtige ressource til at arbejde på et projekt. I Microsoft Dynamics 365 for operationer kan resourcing muligheder for projekter du definere roller, der behandles som midlertidige ressourcer, der kan reserveres til en bestemt engagement eller en del af en Forlovelse. Med denne ressourcetype kan projektledere og ressourceledere udføre følgende opgaver:

-   Definere en rolle, der har de nødvendige kompetencer til at gøre det nemt at tilpasse ressourcerne.
-   Bruge roller til at definere en tidsplan for første kontakt, der er baseret på reserverede ressourcer.
-   Anslå omkostninger udarbejde og et indledende budget baseret på tildelte roller og ressourcer til et projekt.
-   Bruge roller til at anslå antallet af reservationer for ressourcen, der kræves for hver aftale.
-   Vurdere antallet af ressourcer, der kræves til hele livscyklussen for et projekt.
-   Udarbejde et udkast til et arbejdsopgavehierarki (WBS) ved hjælp af de oprindelige ressourcetildelinger.

[![Projektets livscyklus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Som indtægt projektplanlægning, kan planlagte ressourcer erstattes med medarbejdere ressourcer. Projektlederen kan også gå tilbage og opdatere resourcing reservationerne under nogen af projektstadier.

## <a name="set-up-project-resources"></a>Konfigurere projektressourcer
Du skal oprette en kalender og knytte den til en medarbejder eller en arbejder. Kalenderen bruges til at planlægge projektet og arbejdstid for de ressourcer, der er reserveret til projektet. Projektledere kan udføre ressourceudjævning som en del af ressourceoptimering, når de konfigurerer kalenderen. Baseret på kalendertidsplanen kan der sættes begrænsninger på ressourcer. Du kan oprette en kalender på den **kalendere** side. 

Når du opretter en arbejder som en projektgrupperessource, kan du vælge mellem arbejdere, der arbejder i virksomheden, som du opretter ressourcer eller du kan vælge arbejdstagere fra andre firmaer i organisationen. Disse er interne ressourcer. Følgende fremgangsmåder forklarer, hvordan du konfigurerer en arbejder som en projektgrupperessource i virksomheden, og hvordan du opretter en intern projektressource.

### <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurere en arbejder som en projektressource

1.  På den **arbejdere** side i den **arbejdere** skal du vælge den arbejder, som du vil tilføje som en projektgrupperessource, og Åbn arbejderposten.
2.  I handlingsruden, skal du klikke på **projekt**&gt;**Setup**&gt;**Project-installationsprogrammet**.
3.  Vælg en kalender, og luk derefter siden.

Du kan også angive standardprojekter for en ressource som en slags foreløbig tildeling. Foreløbige tildelinger kan bruges, når ressourcestyringen eller projektlederen i forvejen ved, hvilke projekter ressourcen skal arbejde på. Foreløbige tildelinger kan også være baseret på anmodning fra en projektsponsor eller kunde. Når du vil tildele et projekt foreløbigt, skal du vælge det relevante projekt på siden **Tildel projekter** under fanen **Projekter** på listen **Resterende projekter**.

### <a name="set-up-an-intercompany-resource"></a>Oprette en intern ressource

Når du opretter en arbejder som en intern ressource, skal du fuldføre opsætningen i den långivende virksomhed og lån-virksomhed. 

**I det långivende regnskab:**

1.  I Dynamics 365 for operationer, kontrollere, at den långivende virksomhed er markeret og derefter fuldføre ovenstående procedure, "Konfigurere en arbejder som en projektgrupperessource."
2.  Gå til ** Finans **&gt; ** opsætning af finanskontering **&gt;**mellemregning**. Click **New**.
3.  I den ** juridiske enheds-ID ** skal du vælge den långivende virksomhed. Udfyld de resterende felter efter behov, og klik derefter på **Gem**.
4.  Gå til ** projektstyring og regnskab **&gt; ** opsætning **&gt;**priser ** &gt;**afregningspris**.** **
5.  På den ** afregningspris ** skal du klikke på **ny**, og i den ** juridiske låneenhed ** skal du vælge det relevante firma.
6.  Hvis du vil kun låne lån virksomheden den ressource, du oprettede i starten af dette afsnit i den **ressource** skal du vælge navnet på den ressource, du har oprettet. Hvis du vil gøre alle ressourcer i virksomheden tilgængelig for firmaet lån, lade den ** ressource ** stå tomt.
7.  Gå til ** projektstyring og regnskab **&gt; ** opsætning **&gt;**projektstyring og regnskabsparametre**, og på den ** interne ** fanen, skal du angive den ** aktivere intern ressourceplanlægning og timesedler ** til **Ja**.

**I firmaet lån:**

1.  Gå til **projektstyring og regnskab**&gt;**Project ressourcer**&gt;**ressourcelisten**.
2.  Angiv navnet på den ressource, du oprettede i forrige procedure at kontrollere, at navnet er inkluderet på ressourcelisten for firmaet lån långivende firmaet i filteret search.

## <a name="manage-resource-competencies"></a>Administrere ressourcekompetencer
Ressource-kompetencer er en vigtig del af Ressourcestyring. Kompetencer kan grundlæggende bruges til at bestemme de ressourcer, der har den rigtige balance mellem færdigheder, uddannelse, certificering og projekterfaring. Du skal angive disse oplysninger for hver ressource og opdatere dem med jævne mellemrum. På denne måde kan du maksimere mulighederne, når bestemte ressourcekompetencer sammenlignes under tildeling af projektressourcer. [![Eksempler på færdigheder, certificeringer, uddannelse og projekterfaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Følgende procedurer forklarer, hvordan du konfigurerer nogle kompetencer for en ressource. 

Hvis du vil konfigurere kompetencer for en medarbejder, kan du bruge **Arbejdere**-listesiden i Personale eller **Ressourcer**-listesiden i Projektstyring og regnskab. Følgende procedurer, den **arbejdere** bruges listeside i Personale.

### <a name="set-up-competencies-certificates"></a>Konfigurere kompetencer: Certifikater

1.  På **Arbejdere**-listesiden skal du vælge linjen for den arbejder, som du vil tilføje certifikatoplysninger for.
2.  I handlingsruden under fanen **Arbejder** i gruppen **Kompetencer** skal du klikke på **Certifikater**.
3.  Klik på **Ny**.
4.  I **Certifikattype** feltet skal du vælge **PMP**.
5.  I feltet **Startdato** skal du vælge **10/1/2015**.
6.  Klik på **Gem**, og luk derefter siden.

### <a name="set-up-competencies-skills"></a>Konfigurere kompetencer: Færdigheder

1.  På listesiden **Arbejdere** skal du sørge for, at den arbejder, som du brugte i den forrige procedure stadig er markeret. I handlingsruden under fanen **Arbejder** i gruppen **Kompetencer** skal du derefter klikke på **Færdigheder**.
2.  Klik på **Ny**.
3.  Vælg **Projektstyring** i feltet **Færdighed**.
4.  Vælg et niveau i feltet **Niveau** skal du vælge **5 Ekspert**.
5.  I feltet **Niveaudato** skal du vælge **1-/14/2014**.
6.  I feltet **Års erfaring** skal du angive **10**.
7.  Klik på **Gem**, og luk derefter siden.

## <a name="create-a-new-project"></a>Opret et nyt projekt
1.  Klik på **projektstyring og regnskab**&gt;**arbejdsområder**&gt;**Project management**.
2.  Klik på **Nyt projekt**, og angiv følgende værdier:
    -   **Projekttypen** - tids- og materialeprojekter
    -   **Projektets navn** -XYZ opgradere fase 2
    -   **Projektgruppe** -TM\_via
    -   **Projekt kontrakt-ID** -00000002
3.  Klik på **Opret projekt**.

### <a name="assign-a-resource-to-a-project"></a>Tildel en ressource til et projekt

1.  Klik på **personale**&gt;**arbejdere**&gt;**arbejdere**.
2.  På listen **Arbejdere** skal du vælge posten for den arbejder, som du tidligere har konfigureret kompetencer for, og åbne arbejderposten.
3.  Klik på **Tildel projekter** i gruppen **Konfiguration** under fanen **Projekt** i handlingsruden.
4.  På siden **Ressourcevalidering af projekttildelinger** skal du klikke på siden **Projekter**.
5.  I den **føje projektet til udvalgte projekter**, filter på projektet, XYZ opgradere fase 2
6.  I ruden **Resterende projekter** skal du vælge et projekt og derefter klikke på pilen for at føje det til ruden **Valgte projekter**.
7.  Luk siden.

Hvis det er nødvendigt, kan du også tildele kategorier til en ressource. Kategoritypen er enten Omkostning eller Indtægter. Dette bestemmes af din organisation. Hvis der er nogen tildelte kategorier for ressourcen, ser Dynamics 365 for operationer af standardkategorien på time priser for omkostninger og indtægter.

### <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurere projektressource- og rollekarakteristika

En projektleder kan bruge projektressourcefunktionaliteten til at oprette de roller, der er nødvendige for projektet. Roller kan bruges, når bekræftede ressourcer er stadig ukendt, når du skal reservere ressourcer. Roller kan midlertidigt reserveret som planlagt ressourcer, så du kan fortsætte med trin for projektplanlægning. 

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarie:** Contoso blev ansat til at udføre et tids- og materialeprojekt, der har et godkendt projektcharter. Juniorprojektlederen er stadig ved at færdiggøre omfanget af projektet. Resource manager i øjeblikket identificerer bestemte ressourcer, der reserveres for at arbejde på det nye projekt. En af de roller, projektsponsor har skrevet, på grund af kritiske arten af projektet, er en erfaren projektleder. Resource manager skal hente den nye ressource og definere rollen i systemet i tilfælde af, at nyansatte projektlederen kræver ressourceoplysninger under planlægning af projekter. 

Følgende fremgangsmåde viser, hvordan resource manager kan konfigurere rollen Senior project manager og knytte ressource egenskaber til den. Rollen kan senere bruges til at søge efter tilgængelige ressourcer, der svarer til de krævede ressourcekompetencer.

1.  Klik på **projektstyring og regnskab**&gt;**Setup**&gt;**ressourcer**&gt;**installation roller**.
2.  Klik på **Ny**, og angiv følgende værdier:
    -   **Rolle-ID** -Senior projektleder
    -   **Beskrivelse** -Senior projektleder
3.  Klik på **Opret**.
4.  Vælg **Seniorprojektleder**-rollen, og klik derefter på **Konfigurer egenskaber**.
5.  Vælg **Færdighed** i feltet **Karakteristikatype**.
6.  I feltet **Tilgængelige karakteristika** skal du angive den færdighed, du søger efter.
7.  I **Karakteristikatype** feltet skal du vælge **Certifikat**.
8.  I feltet **Tilgængelige karakteristika** skal du angive den certifikattype, du søger efter.
9.  Klik på **OK**, og luk siden.

### <a name="assign-a-project-resource-to-a-project"></a>Tildele en projektressource til et projekt

1.  Klik på **projektstyring og regnskab**&gt;**almindelige**&gt;**projekter**&gt;**alle projekter**, og Åbn den **XYZ opgradere fase 2** projekt.
2.  Under fanen **Projektteam og planlægning** skal du klikke på **Tilføj**.
3.  I feltet **Rolle** skal du vælge **Teammedlem**.
4.  Klik på **Reservér fra kalender**.
5.  På siden **Ressourcetilgængelighed** skal du klikke på **Vis indstillinger**.
6.  På siden **Juster visningsindstillinger** skal du angive følgende værdier:
    -   **Formatet for dato områdevisning** - dag
    -   **Få vist beskrivelser af tilgængelighed** - Ja
    -   **Vis resterende kapacitet** - Ja
7.  Vælg en ressource på listen over ressourcer.
8.  Klik på **definitivt**&gt;**fuld kapacitet**.
9.  Luk siden.

### <a name="assign-a-resource-to-a-default-role"></a>Tildele en ressource til en standardrolle

For at hjælpe ledere af projektet eller ressourcen, kan du rulle længere ned på de ressourcer, der kan reserveres til et projekt. Du kan knytte en standardrolle til en eksisterende ressource eller en nyligt erhvervet ressource. For eksempel når Daniel blev ansat, havde han erfaring og kompetence til at udfylde rollen Business analytiker. Ressourcestyring tildelt rollen som Daniels standardrollen. Derfor tilføjes resource manager Daniel en pulje af virksomhedsanalytikere, der er tilgængelige til at arbejde på projekter. 

Projektledere kan filtrere ressourcerne rolle, der er tilgængelige til at arbejde på projekter under resource reservation. De kan bruge disse oplysninger som et kriterium, når de foretager beslutningsanalyse med flere kriterier under ressourceopfyldelsen. De kan også føje andre ressourcekarakteristika til filteret for at søge efter ressourcer, som har særlige kvalifikationer, uddannelse og erfaringer med et givent projekt. 

**Scenarie:** et godkendt projekt er startet, og rollen Senior project manager er reserveret som en ressource, der er planlagt under projektet planlægningsstadiet. Ressourcestyringen har nu fået en ressource, der skal opfylde rollen som seniorprojektleder.

1.  Klik på **projektstyring og regnskab**&gt;**Project ressourcer**&gt;**ressourcelisten**.
2.  Vælg **Daniel Goldschmidt** på listen **Ressourcer**.
3.  Klik på **Project ressourcen**&gt;**Vedligehold**&gt;**ressourcerollen**.
4.  Klik på **Ny**, og angiv følgende værdier:
    -   **Effektive** - (dags dato)
    -   **Udløb af** - aldrig
    -   **Rolle** -Senior projektleder
5.  Klik på **Gem**, og luk derefter siden.
6.  Under fanen **Kompetencer** skal du tilføje færdigheden **ProjectMgmt** og **PMP**-certifikatet.

## <a name="set-up-role-based-pricing"></a>Konfigurere rollebaserede priser
Alle omkostninger, salg og overførselspriser kan indstilles for roller.

1.  Klik på **projektstyring og regnskab**&gt;**Setup**&gt;**priser**&gt;**salgspris (time)**.
2.  Click **New**.
3.  Angiv en ikrafttrædelsesdato.
4.  Vælg en rolle i kolonnen **Rolle**.
5.  I kolonnen **Prissætning** skal du angive en pris for den valgte ressourcerolle.

## <a name="form-a-project-team"></a>Formen af en projektgruppe
Hvis du vil bruge de roller, der er tidligere angivet i et projekt, skal en projektleder knytte roller til projektet. Kan tildeles flere roller for et projekt, og disse roller Dynamics 365 for operationer etiketter automatisk under reservation for at undgå forvirring. For eksempel hvis projektlederen kræver tre software ingeniører, tre Software engineering roller, der har software engineering 1, oprettes softwareingeniør 2 og software engineering 3 som deres etiketter automatisk. Hvis rollekarakteristika tidligere var defineret for rollen, anvendes de som et filter under søgninger efter en ressource. Du kan tilføje yderligere karakteristika efter behov for at indsnævre søgningen yderligere. 

Visningsindstillinger kan også tilpasses for at give et bedre overblik over ressourcetilgængelighed. Er der indstillinger, som kan vise tilgængelighed pr. time, dag, uge, måned, kvartal og år. Der er også en indstilling, som kan vise tilgængelig og resterende kapacitet for ressourcer. Denne indstilling er nyttig til tidsstyring, når du skal vurdere ledig tid til aktiviteter eller ressourcetilgængelighed. 

Projektlederen kan Vælg en rolle på siden og derefter, hvis der er en tilgængelig ressource, der passer til behovet, vælge for at reservere en ressource for at udfylde rollen. Bemærk, at der ikke har ressourcerne, der skal reserveres på dette tidspunkt under planlægningen. Når du opretter en WBS, kan du erstatte roller med medarbejdere ressourcer til projektet. Hvis roller er erstattet med medarbejdere ressourcer i WBS, opdaterer ressource-installationsprogrammet automatisk projektgruppen notering og planlægning. 

[![Projektgruppe, der omfatter både roller og faktiske ressourcer](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektlederen har forskellige muligheder for reservation af en ressource til et projekt, f.eks. **Resterende kapacitet**, **Fuld kapacitet**, **Kapacitetsprocent** og **Angiv timer**. Disse reservationsindstillinger kan annulleres når som helst, hvis ressourcetildelinger ændres. Der findes to typer reservationer:

-   **Hård bog** – ressourcereservation er godkendte og bekræftede for at arbejde på engagement for den angivne varighed.
-   **Blød bog** – ressource reservationerne foreløbigt var indstillet til at arbejde med engagement for den angivne varighed.

I følgende fremgangsmåde beskrives, hvordan et projektteam oprettes.

### <a name="create-a-project-team"></a>Oprette et projektteam

1.  Vælg et projekt på listesiden **Alle projekter**, og klik derefter på **Rediger**.
2.  På den **team og planlægning af** under fanen den **slutdatoen for planen** skal du angive den tidsplan startdato plus en måned. For eksempel hvis tidsplanen startdato er 24 juni 2017 (24/06/2017), Angiv **07/24/2017**.
3.  Click **Add**.
4.  I ruden **Føj roller til projektet** i feltet **Rolle **skal du vælge **Seniorprojektleder**.
5.  Klik på **Påkrævede kompetencer**.
6.  På siden **Vælg egenskaber** er de karakteristika, som du tidligere har angivet for seniorprojektlederrollen markeret som standard. Klik på **OK**.
7.  På siden **Føj roller til projekt** i feltet **Antal ressourcer** skal du angive **1**.
8.  I feltet **Ressource** viser opslaget alle ressourcer, der har de nødvendige kompetencer. Vælg **Daniel Goldschmidt**, og klik derefter på **Opret**.
9.  Klik på **Tilføj** på siden **Projekt**.
10. I ruden **Føj roller til projektet** i feltet **Rolle** skal du vælge **Teammedlem**. Angiv **5** i feltet **Antal ressourcer**.
11. Klik på **Opret**.
12. På siden **Projekter** skal du klikke på **Opfyld ressource**.

## <a name="resource-capacity-synchronization"></a>Synkronisering af ressourcekapacitet
Processerne til ressourcesynkronisering hjælper med at sikre, at kalender- og basiskalenderoplysninger videreføres til ressourceplanlægning for projektet. Hvis kalenderen ændres, foretager processerne de nødvendige opdateringer af planlægningen af projektressourcerne. Processerne hjælper også med at forbedre performance, fordi kalenderens ressourceoplysninger er synkroniseret på forhånd, så opdateringer af ressourceplanlægningsoplysninger udføres hurtigere. Vi anbefaler, at du planlægger processerne som en batch i stedet for én ad gangen. Ellers er der risiko for, at nogen vil glemme inklusive-datoerne, hvor oplysningerne sidst blev synkroniseret. Hvis inklusive-datoer ikke bruges, kan der opstå mellemrum under synkronisering af datoer.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Synkronisering af kalender](./media/projectresourcing04-1024x471.jpg)

**Synchronize resource capacity roll-ups**

Synkroniseringsprocessen er designet til at synkronisere alle oplysninger i ressourcekalenderen. Disse oplysninger omfatter basiskalenderoplysninger om eventuelle ændringer af projektets tabel for ressourcekalenderkapacitet. Hvis der tilføjes nye ressourcer i projektet, sikrer synkronisering, at den opdaterede kalenderoplysninger er tilgængelig. Denne synkronisering kan udføres når som helst. 

Vi anbefaler, at du bruger en batch. Indstillingerne er tilgængelige i synkroniseringskapacitetsreservationer.

-   Klik på **projektstyring og regnskab**&gt;**periodisk**&gt;**kapacitet synkronisering**&gt;**synkronisere ressourcer kapacitet akkumuleringerne**.

| Indstilling | Betegnelse                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja    | Synkroniser alle ressourcedata med kalender- og basiskalenderoplysninger, og erstat alle oplysninger i projektets ressourcekapacitetskalender.                                                  |
| Nej     | Synkroniser ressourcedata baseret på datointervalkoden og de angivne start- og slutdatoer. Denne indstilling fjerner ikke eksisterende data og opdaterer kun oplysninger for nyligt tilføjede ressourcer. |

[![Synkroniseringsprocessen](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Konfigurere roller i WBS-skabeloner
Projektledere kan konfigurere WBS-skabeloner, som de kan anvende, når de opretter et arbejdsopgavehierarki (WBS) til nye projekter. Projektledere kan tilføje roller, når de opretter en skabelon. Benyt følgende fremgangsmåde til at tildele en rolle til et WBS-template.* * **

1.  Klik på **projektstyring og regnskab**&gt;**Setup**&gt;**projekter**&gt;**skabeloner til arbejdsopgavehierarki**.
2.  Klik på **Detaljer** for en valgt WBS-skabelon.
3.  Markér en opgave på listen, og vælg derefter en rolle, der skal tildeles opgaven, i feltet **Rolle**.

### <a name="work-with-a-wbs"></a>Arbejde med et WBS

Du kan oprette et nyt WBS, eller du kan kopiere et WBS fra en eksisterende WBS-skabelon. En projektleder kan nemt administrere ressourcerne ved at tildele roller til nye opgaver i WBS'et. Roller kan erstattes, når der er skaffet en ressource, eller når der er identificeret en bekræftet ressource til at arbejde på opgaven. Denne fleksibilitet gør det muligt for projektledere at udføre følgende opgaver:

-   Identificere det antal ressourcer, der kræves til WBS-arbejdspakker.
-   Forkalkulere projektomkostninger.
-   Bestemme et foreløbigt budget.
-   Anslå varighed af aktivitet, baseret på roller og ressourcer.
-   Udvikle nogle projektstyringsplaner, baseret på de tilgængelige projektoplysninger.

Yderligere indstillinger er tilføjet i WBS for at forbedre brugen af ressourcefunktionaliteten.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Indstilling</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressourcetildelinger</td>
<td>Se de tildelte ressourcer, datoer, antallet af timer og reservationstypen for opgaver i WBS'et.</td>
</tr>
<tr class="even">
<td>Generér team automatisk</td>
<td>Tilføj automatisk planlagte ressourcer ved hjælp af roller, der er knyttet til en opgave. Dynamics 365 for operationer foreslås automatisk planlagte ressourcer ved hjælp af flere kriterier beslutning analyse, der er baseret på roller. Når roller og tidsforbrug (timer) er angivet for opgaverne i et WBS, og strukturen er blevet frigivet, skal du klikke på <strong>Generér team automatisk</strong>. Det nødvendige antal planlagte ressourcer føjes til WBS og fanen <strong>Projekt og teamplanlægning</strong>.</td>
</tr>
<tr class="odd">
<td>Ressource (rulleliste)</td>
<td>På siden <strong>Start ressourcetildeling</strong> kan du vælge ressourcer, som skal reserveres definitivt eller foreløbigt, baseret på den angivne varighed. Du kan justere visningsindstillingerne og angive varigheden af ressourceaktiviteter. Du kan vælge og tildele ressourcer på arbejdspakkeniveau ved hjælp af følgende indstillinger:
<ul>
<li><strong>Accepter</strong> – Bekræft ændringer af den ressource, der er tildelt en opgave.</li>
<li><strong>Annuller</strong> – Annuller ændringer af den ressource, der er tildelt en opgave.</li>
<li><strong>Tildel automatisk</strong> – med denne indstilling vælges en tilgængelig medarbejdere ressource med en tilsvarende rolle til den markerede opgave.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klik på **projektstyring og regnskab**&gt;**projekter**&gt;**alle projekter**.
2.  Vælg **XYZ-opgradering fase 2**-projektet på listen.
3.  Klik på **Plan**&gt;**aktiviteter**&gt;**arbejdsopdelingsstruktur**.
4.  Klik på **Ny** for at føje følgende aktiviteter på niveau et til WBS:
    -   Initiering
    -   Planlægning
    -   Udfører
    -   Overvågning og kontrol
    -   Afslutning

5.  Angive datoer og tidsforbrug (timer), som vist i følgende skærmbillede. [![Angivelse af datoer og indsats](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Vælg opgavelinjen **Initiering**, og vælg derefter **Seniorprojektleder** i feltet **Rolle**.
7.  Klik på **Publicer**.
8.  På samme linje i feltet **Ressource** skal du vælge **Daniel Goldschmidt**.
9.  Klik på **Acceptér**.
10. Vælg opgavelinjen **Planlægning**, og vælg derefter **Forretningsanalytiker** i feltet **Rolle**.
11. Klik på **Publicer**, og klik derefter på **Generér team automatisk**.
12. Klik på **Ja** i den dialogboks, der åbnes.
13. I feltet **Ressource** skal du kontrollere, at værdien er **Forretningsanalytiker 1**.
14. For ressourcen **Forretningsanalytiker 1** skal du åbne opslaget og klikke på **Start ressourcetildelingsform**.
15. Vælg en arbejder til opgaven.
16. Klik på **blød Tildel**&gt;**fuld kapacitet**.
17. Klik på **Gem**, og luk siden. 

> [!NOTE] 
> Du modtager ikke en advarsel om, at den angivne ressource er nu 2, fordi antallet ressourcer, der forbliver på 1.
18. På siden **Arbejdsopdelingsstruktur** skal du validere ressourcetildelingen på WBS'et og derefter klikke på **Gem**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressourceopfyldelse for planlagte ressourcer
En projektleder kan planlægge nødvendig ressourceroller for et projekt. Ressourcestyringen ser disse planlagte ressourcer som anmodninger på siden **Opfyldelse af ressource** og kan tildele faktiske ressourcer.

1.  Klik på **projektstyring og regnskab**&gt;**projekter**&gt;**alle projekter**.
2.  Vælg **XYZ-opgradering fase 2**-projektet på listen.
3.  Klik på **Projekt**.
4.  Klik på **Rediger**.
5.  På den **team og planlægning af** under fanen ** ** Klik **Tilføj**.
6.  I dialogboksen **Tilføj roller** skal du vælg rollen **Softwareudvikler**.
7.  Klik på **Opret**.
8.  Luk projektsiden.
9.  Klik på **projektstyring og regnskab**&gt;**Project ressourcer**&gt;**ressource fulfillment**.
10. Vælg **Softwareudvikler 1** **XYZ-opgraderingsprojekt fase 2**.
11. Vælg en arbejder, og klik derefter på **Tildel**.
12. Kontroller, at linjen for **Softwareudvikler 1** er blevet fjernet for **XYZ-opgraderingsprojekt fase 2**.
13. Under fanen **Projektteam og planlægning** for projektet **XYZ-opgradering fase 2** skal du kontrollere, at den arbejder, som du valgte i trin 11, er blevet tilføjet som **Softwareudvikler**.

## <a name="requests-for-project-resources"></a>Anmodninger om projektets ressourcer
Planlægningsfunktionen project ressourcen understøtter kun ressourceledere for at distribuere medarbejdere ressourcer på forpligtelser eller projekter. Udføre følgende opgaver for at aktivere denne funktion, eller Kontroller, at de er færdige.

-   Konfigurer nummerserier.
-   Konfigurere mellemregning arbejdsgange og projektstyring.
-   Aktivere ressource anmodning arbejdsgang.

Når du har kontrolleret eller gennemført ovenstående opgaver, kan du udføre følgende opgaver efter behov.

-   Oprette en ressource-anmodning fra en midlertidigt reserveret ressource medarbejdere.
-   Overvåge ressource-anmodninger.
-   Udføre ressource-anmodninger.
-   Anmode om en ressource, der er medarbejdere fra WBS.
-   Reservere ressourcer til et projekt uden en anmodning om en medarbejdere ressource.

## <a name="monitor-project-teams"></a>Overvågning projektgrupper
1.  Klik på **projektstyring og regnskab**&gt;**projekter**&gt;**alle projekter**.
2.  På listen over projekter skal du klikke på linket **Projekt-id** for projektet **XYZ-opgradering fase 2**.
3.  På oversigtspanelet **Projektteam og planlægning** skal kontrollere, at projektets ressourcer er angivet korrekt.



