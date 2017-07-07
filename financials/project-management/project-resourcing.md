---
title: Projektressourcer
description: Dette emne indeholder oplysninger om projektressourcer.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a7275e9ad8d655d0d2ee5ba90a792775dec0cf05
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="project-resourcing"></a>Projektressourcer

[!include[banner](../includes/banner.md)]


Dette emne indeholder oplysninger om projektressourcer.

En udfordring for projektledere og ressourceledere under projektets planlægningsstadie er ressourceallokering, hvor de skal bestemme og reservere den rigtige ressource til at arbejde på et projekt. I Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kan du med ressourcefunktioner for projekter definere roller, der behandles som midlertidige ressourcer, der kan reserveres til en bestemt opgave eller en del af en opgave. Med denne ressourcetype kan projektledere og ressourceledere udføre følgende opgaver:

-   Definere en rolle, der har de nødvendige kompetencer til at gøre det nemt at tilpasse ressourcerne.
-   Brug roller til at definere en indledende opgavetidsplan, der er baseret på reserverede ressourcer.
-   Anslå omkostninger udarbejde og et indledende budget baseret på tildelte roller og ressourcer til et projekt.
-   Bruge roller til at anslå antallet af ressourcetildelinger, der kræves for hver opgave.
-   Vurdere antallet af ressourcer, der kræves til hele livscyklussen for et projekt.
-   Udarbejde et udkast til et arbejdsopgavehierarki (WBS) ved hjælp af de oprindelige ressourcetildelinger.

[![Projektets livscyklus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Efterhånden som projektplanlægningen skrider frem, kan planlagte ressourcer erstattes med bemandingsressourcer. Projektlederen kan også gå tilbage og opdatere ressourcereservationerne under et hvilket som helst af projektstadierne.

## <a name="set-up-project-resources"></a>Konfigurere projektressourcer
Du skal oprette en kalender og knytte den til en medarbejder eller en arbejder. Kalenderen bruges til at planlægge projektet og arbejdstiden for de ressourcer, der er reserveret til projektet. Projektledere kan udføre ressourceudjævning som en del af ressourceoptimering, når de konfigurerer kalenderen. Baseret på kalendertidsplanen kan der sættes begrænsninger på ressourcer. Du kan oprette en kalender på siden **Kalendere**. 

Når du opretter en arbejder som en projektressource, kan du vælge mellem arbejdere, der arbejder i den virksomhed, som du opretter ressourcer for, eller du kan vælge arbejdere fra andre firmaer i organisationen. Disse er interne ressourcer. Nedenstående fremgangsmåder forklarer, hvordan du konfigurerer en arbejder som en projektgrupperessource i virksomheden, og hvordan du opretter en intern projektressource.

### <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurere en arbejder som en projektressource

1.  På siden **Arbejdere** på listen **Arbejdere** skal du vælge den arbejder, som du vil tilføje som en projektressource, og åbne arbejderposten.
2.  I handlingsruden skal du klikke på **Projekt** &gt; **Konfiguration** &gt; **Opsætning af projekt**.
3.  Vælg en kalender, og luk derefter siden.

Du kan også angive standardprojekter for en ressource som en slags foreløbig tildeling. Foreløbige tildelinger kan bruges, når ressourcestyringen eller projektlederen i forvejen ved, hvilke projekter ressourcen skal arbejde på. Foreløbige tildelinger kan også være baseret på anmodning fra en projektsponsor eller kunde. Når du vil tildele et projekt foreløbigt, skal du vælge det relevante projekt på siden **Tildel projekter** under fanen **Projekter** på listen **Resterende projekter**.

### <a name="set-up-an-intercompany-resource"></a>Opret en intern ressource

Når du opretter en arbejder som en intern ressource, skal du fuldføre opsætningen i firmaet, der udlåner, og i firmaet, der låner. 

**I firmaet, der udlåner:**

1.  I Finance and Operations skal du kontrollere, at firmaet, der låner, er markeret, og derefter skal du fuldføre ovenstående procedure, "Konfigurer en arbejder som en projektgrupperessource".
2.  Gå til **Finans** &gt; **Opsætning af bogføring** &gt; **Mellemregning**. Klik på **Ny**.
3.  I feltet **Id for juridisk enhed** skal du firmaet, der udlåner. Udfyld de resterende felter efter behov, og klik derefter på **Gem**.
4.  Gå til **Projektstyring og regnskab**&gt; **Opsætning** &gt; **Priser&gt; **Intern afregningspris**.** **
5.  På formularen **Intern afregningspris** skal du klikke på **Ny**, og i feltet **Udlånt til (juridisk enhed)** skal du vælge det relevante firma.
6.  Hvis du kun vil låne firmaet, der låner, den ressource, du oprettede i starten af dette afsnit i feltet **Ressource** skal du vælge navnet på den ressource, du har oprettet. Hvis du vil gøre alle ressourcer i firmaet tilgængelige for firmaet, der låner, skal du lade feltet **Ressource** stå tomt.
7.  Gå til **Projektstyring og regnskab** &gt; **Opsætning** &gt; **Parametre for projektstyring og regnskab** og under fanen **Intern** skal du angive feltet **Aktivér intern ressourceplanlægning og timesedler** til **Ja**.

**I firmaet, der låner:**

1.  Gå til **Projektstyring og regnskab** &gt; **Projektressourcer** &gt; **Ressourceliste**.
2.  I søgefiltret skal du angive navnet på den ressource, du oprettede i forrige procedure for firmaet, der udlåner, for at kontrollere, at navnet er inkluderet på ressourcelisten for firmaet, der låner.

## <a name="manage-resource-competencies"></a>Administrere ressourcekompetencer
Ressourcekompetencer er en vigtig del af ressourcestyringen. Kompetencer kan grundlæggende bruges til at bestemme de ressourcer, der har den rigtige balance mellem færdigheder, uddannelse, certificering og projekterfaring. Du skal angive disse oplysninger for hver ressource og opdatere dem med jævne mellemrum. På denne måde kan du maksimere mulighederne, når bestemte ressourcekompetencer sammenlignes under tildeling af projektressourcer. [![Eksempler på færdigheder, certificeringer, uddannelse og projekterfaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Følgende procedurer forklarer, hvordan du konfigurerer nogle kompetencer for en ressource. 

Hvis du vil konfigurere kompetencer for en medarbejder, kan du bruge **Arbejdere**-listesiden i Personale eller **Ressourcer**-listesiden i Projektstyring og regnskab. I nedenstående fremgangsmåder bruger vi listesiden **Arbejdere** i Personale.

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
1.  Klik på **Projektstyring og regnskab** &gt; **Arbejdsområder** &gt; **Projektstyring**.
2.  Klik på **Nyt projekt**, og angiv følgende værdier:
    -   **Projekttype** – Tid og materialer
    -   **Projektnavn** – XYZ-opgradering fase 2
    -   **Projektgruppe** – TM\_WIP
    -   **Projektkontrakt-id** – 00000002
3.  Klik på **Opret projekt**.

### <a name="assign-a-resource-to-a-project"></a>Tildel en ressource til et projekt

1.  Klik på **Personale** &gt; **Arbejdere** &gt; **Arbejdere**.
2.  På listen **Arbejdere** skal du vælge posten for den arbejder, som du tidligere har konfigureret kompetencer for, og åbne arbejderposten.
3.  Klik på **Tildel projekter** i gruppen **Konfiguration** under fanen **Projekt** i handlingsruden.
4.  På siden **Ressourcevalidering af projekttildelinger** skal du klikke på siden **Projekter**.
5.  I **Føj projektet til udvalgte projekter** skal du filtrere på projektet XYZ-opgradering fase 2
6.  I ruden **Resterende projekter** skal du vælge et projekt og derefter klikke på pilen for at føje det til ruden **Valgte projekter**.
7.  Luk siden.

Hvis det er nødvendigt, kan du også tildele kategorier til en ressource. Kategoritypen er enten Omkostning eller Indtægter. Dette bestemmes af din organisation. Hvis der ikke er nogen tildelte kategorier for ressourcen, leder Finance and Operations efter standardkategorien på timepriser for omkostninger og indtægter.

### <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurere projektressource- og rollekarakteristika

En projektleder kan bruge projektressourcefunktionaliteten til at oprette de roller, der er nødvendige for projektet. Roller kan bruges, når bekræftede ressourcer stadig er ukendte, når ressourcer reserveres. Roller kan midlertidigt reserveres som planlagte ressourcer, så du kan fortsætte med projektplanlægningsfaserne. 

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarie:** Contoso blev ansat til at udføre et tids- og materialeprojekt, der har et godkendt projektcharter. Juniorprojektlederen er stadig ved at færdiggøre omfanget af projektet. Ressourcestyringen identificerer i øjeblikket bestemte ressourcer, der skal reserveres til arbejde på det nye projekt. En af de roller, projektsponsoren har anmodet om på grund af projektets kritiske natur, er seniorprojektlederen. Ressourcechefen skal anskaffe den nye ressource og definere rollen i systemet i tilfælde af, at juniorprojektlederen kræver ressourceoplysninger under projektplanlægningen. 

Følgende fremgangsmåde viser, hvordan ressourcechefen kan konfigurere seniorprojektlederrollen og knytte ressourceegenskaber til den. Rollen kan senere bruges til at søge efter tilgængelige ressourcer, der svarer til de krævede ressourcekompetencer.

1.  Klik på **Projektstyring og regnskab** &gt; **Konfiguration** &gt; **Ressourcer** &gt; **Konfigurer roller**.
2.  Klik på **Ny**, og angiv følgende værdier:
    -   **Rolle-id** – Seniorprojektleder
    -   **Beskrivelse** – Seniorprojektleder
3.  Klik på **Opret**.
4.  Vælg **Seniorprojektleder**-rollen, og klik derefter på **Konfigurer egenskaber**.
5.  Vælg **Færdighed** i feltet **Karakteristikatype**.
6.  I feltet **Tilgængelige karakteristika** skal du angive den færdighed, du søger efter.
7.  I **Karakteristikatype** feltet skal du vælge **Certifikat**.
8.  I feltet **Tilgængelige karakteristika** skal du angive den certifikattype, du søger efter.
9.  Klik på **OK**, og luk siden.

### <a name="assign-a-project-resource-to-a-project"></a>Tildele en projektressource til et projekt

1.  Klik på **Projektstyring og regnskab** &gt; **Fælles** &gt; **Projekter** &gt; **Alle projekter**, og åbn projektet **XYZ-opgradering fase 2**.
2.  Under fanen **Projektteam og planlægning** skal du klikke på **Tilføj**.
3.  I feltet **Rolle** skal du vælge **Teammedlem**.
4.  Klik på **Reservér fra kalender**.
5.  På siden **Ressourcetilgængelighed** skal du klikke på **Vis indstillinger**.
6.  På siden **Juster visningsindstillinger** skal du angive følgende værdier:
    -   **Viser format for datoområde** – Dag
    -   **Vis beskrivelser af tilgængelighed** – Ja
    -   **Vis resterende kapacitet** – Ja
7.  Vælg en ressource på listen over ressourcer.
8.  Klik på **Definitiv reservation** &gt; **Fuld kapacitet**.
9.  Luk siden.

### <a name="assign-a-resource-to-a-default-role"></a>Tildele en ressource til en standardrolle

For at hjælpe projektledere eller ressourcechefer kan du rulle længere ned i de ressourcer, der kan reserveres til et projekt. Du kan knytte en standardrolle til en eksisterende ressource eller en nyligt erhvervet ressource. Da Daniel f.eks. blev ansat, havde han erfaring og kompetence til at udfylde rollen Forretningsanalytiker. Ressourcechefen tildelte denne rolle som Daniels standardrolle. Derfor tilføjede ressourcechefen Daniel til en pulje af forretningsanalytikere, der er tilgængelige til at arbejde på projekter. 

Under ressourcereservationen kan projektledere filtrere de ressourceroller, der er tilgængelige for arbejde på projekter. De kan bruge disse oplysninger som et kriterium, når de foretager beslutningsanalyse med flere kriterier under ressourceopfyldelsen. De kan også føje andre ressourcekarakteristika til filteret for at søge efter ressourcer, som har særlige kvalifikationer, uddannelse og erfaringer med et givent projekt. 

**Scenarie:** Et godkendt projekt er startet, og rollen som seniorprojektleder blev reserveret som en planlagt ressource i løbet af projektets planlægningsstadie. Ressourcestyringen har nu fået en ressource, der skal opfylde rollen som seniorprojektleder.

1.  Klik på **Projektstyring og regnskab** &gt; **Projektressourcer** &gt; **Ressourceliste**.
2.  Vælg **Daniel Goldschmidt** på listen **Ressourcer**.
3.  Klik på **Projektressource** &gt; **Vedligehold** &gt; **Ressourcerolle**.
4.  Klik på **Ny**, og angiv følgende værdier:
    -   **Gyldig fra** – (den aktuelle dato)
    -   **Udløb** – Aldrig
    -   **Rolle** – Seniorprojektleder
5.  Klik på **Gem**, og luk derefter siden.
6.  Under fanen **Kompetencer** skal du tilføje færdigheden **ProjectMgmt** og **PMP**-certifikatet.

## <a name="set-up-role-based-pricing"></a>Konfigurere rollebaserede priser
Alle omkostninger, salg og overførselspriser kan indstilles for roller.

1.  Klik på **Projektstyring og regnskab** &gt; **Konfiguration** &gt; **Priser** &gt; **Salgspris (time)**.
2.  Klik på **Ny**.
3.  Angiv en ikrafttrædelsesdato.
4.  Vælg en rolle i kolonnen **Rolle**.
5.  I kolonnen **Prissætning** skal du angive en pris for den valgte ressourcerolle.

## <a name="form-a-project-team"></a>Opret et projektteam
Hvis en projektleder vil bruge de roller, der er tidligere angivet i et projekt, skal han eller hun knytte rollerne til projektet. Flere roller kan tildeles til et projekt, og Finance and Operations navngiver automatisk disse roller under reservationen for at forhindre forvirring. Hvis projektlederen f.eks. kræver tre softwareteknikere, oprettes der automatisk tre softwareteknikerroller, der navngives softwaretekniker 1, softwaretekniker 2 og softwaretekniker 3. Hvis rollekarakteristika tidligere var defineret for rollen, anvendes de som et filter under søgninger efter en ressource. Du kan tilføje yderligere karakteristika efter behov for at indsnævre søgningen yderligere. 

Visningsindstillinger kan også tilpasses for at give et bedre overblik over ressourcetilgængelighed. Er der indstillinger, som kan vise tilgængelighed pr. time, dag, uge, måned, kvartal og år. Der er også en indstilling, som kan vise tilgængelig og resterende kapacitet for ressourcer. Denne indstilling er nyttig til tidsstyring, når du skal vurdere ledig tid til aktiviteter eller ressourcetilgængelighed. 

Projektlederen kan vælge en rolle på siden, og hvis der er en tilgængelig ressource, der passer til behovet, kan han eller hun vælge at reservere en ressource, der kan udfylde rollen. Bemærk, at ressourcerne ikke behøver at være reserveret på dette tidspunkt i planlægningen. Når du opretter et arbejdsopgavehierarki, kan du erstatte roller med bemandingsressourcer til projektet. Hvis roller erstattes med bemandingsressourcer i arbejdsopgavehierarkiet, opdaterer ressourcekonfigurationen automatisk projektteamlisten og -planlægningen. 

[![Projektteamliste, der omfatter både roller og faktiske ressourcer](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektlederen har forskellige muligheder for reservation af en ressource til et projekt, f.eks. **Resterende kapacitet**, **Fuld kapacitet**, **Kapacitetsprocent** og **Angiv timer**. Disse reservationsindstillinger kan annulleres når som helst, hvis ressourcetildelinger ændres. Der findes to typer reservationer:

-   **Definitiv reservation** – Ressourcereservationen blev godkendt og bekræftet for arbejde på opgaven for den angivne varighed.
-   **Foreløbig reservation** – Ressourcereservationerne er foreløbig angivet til at arbejde på opgaven for den angivne varighed.

I følgende fremgangsmåde beskrives, hvordan et projektteam oprettes.

### <a name="create-a-project-team"></a>Oprette et projektteam

1.  Vælg et projekt på listesiden **Alle projekter**, og klik derefter på **Rediger**.
2.  Under fanen **Projektteam og planlægning** i feltet **Planlæg slutdato** skal du angive startdato for tidsplanen plus en måned. For eksempel hvis tidsplanens startdato er 24. juni 2017 (24/06/2017), skal du angive **24/07/2017**.
3.  Klik på **Tilføj**.
4.  I ruden **Føj roller til projektet** i feltet **Rolle** skal du vælge **Seniorprojektleder**.
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

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

**Synkronisér ressourcekapacitet akkumuleringer**

Synkroniseringsprocessen er designet til at synkronisere alle oplysninger i ressourcekalenderen. Disse oplysninger omfatter basiskalenderoplysninger om eventuelle ændringer af projektets tabel for ressourcekalenderkapacitet. Hvis der tilføjes nye ressourcer i projektet, hjælper synkroniseringen med at sikre, at de opdaterede kalenderoplysninger er tilgængelige. Denne synkronisering kan udføres når som helst. 

Vi anbefaler, at du bruger en batch. Indstillingerne er tilgængelige i synkroniseringskapacitetsreservationer.

-   Klik på **Projektstyring og regnskab** &gt; **Periodisk** &gt; **Kapacitetssynkronisering** &gt; **Synkronisér ressourcekapacitet akkumuleringer**.

| Indstilling | Betegnelse                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja    | Synkroniser alle ressourcedata med kalender- og basiskalenderoplysninger, og erstat alle oplysninger i projektets ressourcekapacitetskalender.                                                  |
| Nej     | Synkroniser ressourcedata baseret på datointervalkoden og de angivne start- og slutdatoer. Denne indstilling fjerner ikke eksisterende data og opdaterer kun oplysninger for nyligt tilføjede ressourcer. |

[![Synkroniseringsproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Konfigurere roller i WBS-skabeloner
Projektledere kan konfigurere WBS-skabeloner, som de kan anvende, når de opretter et arbejdsopgavehierarki (WBS) til nye projekter. Projektledere kan tilføje roller, når de opretter en skabelon. Benyt følgende fremgangsmåde til at tildele en rolle til en WBS-skabelon.** **

1.  Klik på **Projektstyring og regnskab** &gt; **Konfiguration** &gt; **Projekter** &gt; **Skabeloner til arbejdsopgavehierarki**.
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
<td>Tilføj automatisk planlagte ressourcer ved hjælp af roller, der er knyttet til en opgave. Finance and Operations foreslår automatisk planlagte ressourcer ved hjælp af beslutningsanalyse med flere kriterier, som er baseret på roller. Når roller og tidsforbrug (timer) er angivet for opgaverne i et WBS, og strukturen er blevet frigivet, skal du klikke på <strong>Generér team automatisk</strong>. Det nødvendige antal planlagte ressourcer føjes til WBS og fanen <strong>Projekt og teamplanlægning</strong>.</td>
</tr>
<tr class="odd">
<td>Ressource (rulleliste)</td>
<td>På siden <strong>Start ressourcetildeling</strong> kan du vælge ressourcer, som skal reserveres definitivt eller foreløbigt, baseret på den angivne varighed. Du kan justere visningsindstillingerne og angive varigheden af ressourceaktiviteter. Du kan vælge og tildele ressourcer på arbejdspakkeniveau ved hjælp af følgende indstillinger:
<ul>
<li><strong>Accepter</strong> – Bekræft ændringer af den ressource, der er tildelt en opgave.</li>
<li><strong>Annuller</strong> – Annuller ændringer af den ressource, der er tildelt en opgave.</li>
<li><strong>Tildel automatisk</strong> – Med denne indstilling vælges en tilgængelig bemandingsressource med en matchende rolle til den markerede opgave.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klik på **Projektstyring og regnskab** &gt; **Projekter** &gt; **Alle projekter**.
2.  Vælg **XYZ-opgradering fase 2**-projektet på listen.
3.  Klik på **Plan** &gt; **Aktiviteter** &gt; **Arbejdsopgavehierarki**.
4.  Klik på **Ny** for at føje følgende aktiviteter på niveau et til WBS:
    -   Initiering
    -   Planlægning
    -   Udfører
    -   Overvågning og kontrol
    -   Afslutning

5.  Angiv datoer og tidsforbrug (timer), som vist i følgende skærmbillede.[![Angivelse af datoer og tidsforbrug](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
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
16. Klik på **Tildel foreløbigt** &gt; **Fuld kapacitet**.
17. Klik på **Gem**, og luk siden. 

> [!NOTE] 
> Du modtager ikke en advarsel om, at den angivne ressource nu er 2, fordi antallet af ressourcer forbliver på 1.
18. På siden **Arbejdsopdelingsstruktur** skal du validere ressourcetildelingen på WBS'et og derefter klikke på **Gem**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressourceopfyldelse for planlagte ressourcer
En projektleder kan planlægge nødvendig ressourceroller for et projekt. Ressourcestyringen ser disse planlagte ressourcer som anmodninger på siden **Opfyldelse af ressource** og kan tildele faktiske ressourcer.

1.  Klik på **Projektstyring og regnskab** &gt; **Projekter** &gt; **Alle projekter**.
2.  Vælg **XYZ-opgradering fase 2**-projektet på listen.
3.  Klik på **Projekt**.
4.  Klik på **Rediger**.
5.  Under fanen **Projektteam og planlægning** skal du ** **klikke på **Tilføj**.
6.  I dialogboksen **Tilføj roller** skal du vælg rollen **Softwareudvikler**.
7.  Klik på **Opret**.
8.  Luk projektsiden.
9.  Klik på **Projektstyring og regnskab** &gt; **Projektressourcer** &gt; **Opfyldelse af ressource**.
10. Vælg **Softwareudvikler 1** **XYZ-opgraderingsprojekt fase 2**.
11. Vælg en arbejder, og klik derefter på **Tildel**.
12. Kontroller, at linjen for **Softwareudvikler 1** er blevet fjernet for **XYZ-opgraderingsprojekt fase 2**.
13. Under fanen **Projektteam og planlægning** for projektet **XYZ-opgradering fase 2** skal du kontrollere, at den arbejder, som du valgte i trin 11, er blevet tilføjet som **Softwareudvikler**.

## <a name="requests-for-project-resources"></a>Anmodninger om projektressourcer
Planlægningsfunktionen Projektressource understøtter kun ressourcechefer i at distribuere bemandingsressourcer på opgaver eller projekter. Udfør følgende opgaver for at aktivere denne funktion, eller kontrollér, at de er blevet fuldført.

-   Konfigurer nummerserier.
-   Konfigurer arbejdsgange i Projektstyring og regnskab.
-   Aktivér arbejdsgang for ressourceanmodning.

Når du har kontrolleret eller fuldført ovenstående opgaver, kan du udføre følgende opgaver efter behov.

-   Opret en ressourceanmodning fra en midlertidigt reserveret bemandingsressource.
-   Overvåg ressourceanmodninger.
-   Opfyld ressourceanmodninger.
-   Anmod om en bemandingsressource fra WBS.
-   Reservér ressourcer til et projekt uden en anmodning om en bemandingsressource.

## <a name="monitor-project-teams"></a>Overvåg projektteam
1.  Klik på **Projektstyring og regnskab** &gt; **Projekter** &gt; **Alle projekter**.
2.  På listen over projekter skal du klikke på linket **Projekt-id** for projektet **XYZ-opgradering fase 2**.
3.  På oversigtspanelet **Projektteam og planlægning** skal kontrollere, at projektets ressourcer er angivet korrekt.





