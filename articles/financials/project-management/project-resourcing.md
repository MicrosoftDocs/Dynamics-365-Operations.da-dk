---
title: Projektressourcer
description: Dette emne indeholder oplysninger om projektressourcer.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8139134ed230cc1525c698fadb20309afee0a68f
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="project-resourcing"></a>Projektressourcer

[!include[banner](../includes/banner.md)]

Dette emne indeholder oplysninger om projektressourcer.

En udfordring for projektledere og ressourceledere under projektets planlægningsstadie er ressourceallokering, hvor de skal bestemme og reservere den rigtige ressource til at arbejde på et projekt. I Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition kan du med ressourcefunktioner for projekter definere roller, der behandles som midlertidige ressourcer, der kan reserveres til en bestemt opgave eller en del af en opgave. Med denne ressourcetype kan projektledere og ressourceledere udføre følgende opgaver:

- Definere en rolle, der har de nødvendige kompetencer, så det er nemt at tilpasse ressourcerne.
- Brug roller til at definere en indledende opgavetidsplan, der er baseret på reserverede ressourcer.
- Anslå omkostninger udarbejde og et indledende budget baseret på tildelte roller og ressourcer til et projekt.
- Bruge roller til at anslå antallet af ressourcetildelinger, der kræves for hver opgave.
- Vurdere antallet af ressourcer, der kræves til hele livscyklussen for et projekt.
- Udarbejde et udkast til et arbejdsopgavehierarki (WBS) ved hjælp af de oprindelige ressourcetildelinger.

[![Projektets livscyklus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Efterhånden som projektplanlægningen skrider frem, kan planlagte ressourcer erstattes med bemandingsressourcer. Projektlederen kan også gå tilbage og opdatere ressourcereservationerne under et hvilket som helst projektstadie.

## <a name="set-up-project-resources"></a>Konfigurere projektressourcer
Du skal oprette en kalender og knytte den til en medarbejder eller en arbejder. Kalenderen bruges til at planlægge projektet og arbejdstiden for de ressourcer, der er reserveret til projektet. Projektledere kan udføre ressourceudjævning som en del af ressourceoptimering, når de konfigurerer kalenderen. Baseret på kalendertidsplanen kan der sættes begrænsninger på ressourcer. Du kan oprette en kalender på siden **Kalendere**.

Når du konfigurerer en arbejder som en projektressource, kan du vælge mellem arbejdere, der arbejder i det firma, du konfigurerer ressourcer til. Du kan også vælge arbejdere fra andre firmaer i organisationen. Disse arbejdere kaldes interne ressourcer.

Nedenstående fremgangsmåder forklarer, hvordan du konfigurerer en arbejder som en projektressource i virksomheden, og hvordan du opretter en intern projektressource.

### <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurere en arbejder som en projektressource

1. På siden **Arbejdere** på listen **Arbejdere** skal du vælge den arbejder, som du vil tilføje som en projektressource, og åbne arbejderposten.
2. I handlingsruden skal du vælge **Projekt** &gt; **Konfiguration** &gt; **Opsætning af projekt**.
3. Vælg en kalender, og luk derefter siden.

Du kan også angive standardprojekter for en ressource som en slags foreløbig tildeling. Foreløbige tildelinger kan bruges, når ressourcestyringen eller projektlederen i forvejen ved, hvilke projekter ressourcen skal arbejde på. Foreløbige tildelinger kan også være baseret på anmodning fra en projektsponsor eller kunde. Når du vil tildele et projekt foreløbigt, skal du vælge det relevante projekt på siden **Tildel projekter** under fanen **Projekter** på listen **Resterende projekter**.

### <a name="set-up-an-intercompany-resource"></a>Opret en intern ressource

Når du opretter en arbejder som en intern ressource, skal du fuldføre opsætningen både i firmaet, der udlåner, og i firmaet, der låner.

**I firmaet, der udlåner**

1. I Finance and Operations skal du kontrollere, at firmaet, der låner, er markeret, og derefter skal du fuldføre proceduren i det forrige afsnit, "Konfigurere en arbejder som en projektressource".
2. På siden **Mellemregning** skal du vælge **Ny**.
3. I feltet **Id for juridisk enhed** skal du vælge firmaet, der udlåner. Udfyld de resterende felter efter behov, og vælg derefter **Gem**.
4. På siden **Intern afregningspris** skal du vælge **Ny**.
5. I feltet **Udlånt til (juridisk enhed)** skal du vælge det relevante firma.
6. Hvis du kun vil låne firmaet, der låner, den ressource, du oprettede i starten af dette afsnit i feltet **Ressource** skal du vælge navnet på den ressource, du har oprettet. Hvis du vil gøre alle ressourcer i firmaet tilgængelige for firmaet, der låner, skal du lade feltet **Ressource** stå tomt.
7. På siden **Parametre for projektstyring og regnskab** under fanen **Intern** skal du angive indstillingen **Aktivér intern ressourceplanlægning og timesedler** til **Ja**.

**I firmaet, der låner**

- På siden **Liste over ressourcer** skal du i søgefiltret angive navnet på den ressource, du oprettede for firmaet, der udlåner, for at kontrollere, at navnet er inkluderet på ressourcelisten for firmaet, der låner.

## <a name="manage-resource-competencies"></a>Administrere ressourcekompetencer
Ressourcekompetencer er en vigtig del af ressourcestyringen. Kompetencer kan grundlæggende bruges til at bestemme de ressourcer, der har den rigtige balance mellem færdigheder, uddannelse, certificering og projekterfaring. Du skal angive disse oplysninger for hver ressource og opdatere dem med jævne mellemrum. På denne måde kan du maksimere mulighederne, når bestemte ressourcekompetencer sammenlignes under tildeling af projektressourcer.

[![Eksempler på færdigheder, certificeringer, uddannelse og projekterfaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Følgende procedurer forklarer, hvordan du konfigurerer nogle kompetencer for en ressource.

Hvis du vil konfigurere kompetencer for en medarbejder, kan du bruge **Arbejdere**-listesiden i Personale eller **Ressourcer**-listesiden i Projektstyring og regnskab. I nedenstående fremgangsmåder bruger vi listesiden **Arbejdere** i Personale.

### <a name="set-up-competencies-certificates"></a>Konfigurere kompetencer: Certifikater

1. På siden med listen **Arbejdere** skal du vælge linjen for den arbejder, som du vil tilføje certifikatoplysninger for.
2. I handlingsruden under fanen **Arbejder** i gruppen **Kompetencer** skal du vælge **Certifikater**.
3. Vælg **Ny**, og i feltet **Certifikattype** skal du derefter vælge **PMP**.
4. I feltet **Startdato** skal du vælge **10/1/2015** og vælge **Gem**.

### <a name="set-up-competencies-skills"></a>Konfigurere kompetencer: Færdigheder

1. På listesiden **Arbejdere** skal du sørge for, at den arbejder, som du brugte i den forrige procedure stadig er markeret. I handlingsruden under fanen **Arbejder** i gruppen **Kompetencer** skal du derefter klikke på **Færdigheder**.
2. Vælg **Ny**.
3. Vælg **Projektstyring** i feltet **Færdighed**.
4. Vælg et niveau i feltet **Niveau** skal du vælge **5 Ekspert**.
5. I feltet **Niveaudato** skal du vælge **1-/14/2014**.
6. I feltet **Års erfaring** skal du angive **10**.
7. Vælg **Gem**, og luk derefter siden.

## <a name="create-a-new-project"></a>Opret et nyt projekt
1. På siden **Projektstyring** skal du vælge **Nyt projekt** og angive følgende værdier:

    - **Projekttype:** Tid og materialer
    - **Projektnavn:** XYZ-opgradering fase 2
    - **Projektgruppe:** TM\_WIP
    - **Projektkontrakt-id:** 00000002

2. Vælg **Opret projekt**.

### <a name="assign-a-resource-to-a-project"></a>Tildel en ressource til et projekt

1. På siden **Arbejdere** på listen **Arbejdere** skal du vælge posten for den arbejder, som du tidligere har konfigureret kompetencer for, og åbne arbejderposten.
2. Vælg **Tildel projekter** i gruppen **Konfiguration** under fanen **Projekt** i handlingsruden.
3. På siden **Ressourcevalidering af projekttildelinger** under fanen **Projekter** skal du i feltet **Føj projektet til udvalgte projekter** filtrere på projektet **XYZ-opgradering fase 2**.
4. I ruden **Resterende projekter** skal du vælge et projekt og derefter vælge pileknappen for at føje det til ruden **Valgte projekter**.

Du kan også tildele kategorier til en ressource, hvis det er nødvendigt. Kategoritypen er enten **Omkostning** eller **Indtægter**. Kategoritypen bestemmes af din organisation. Hvis der ikke er nogen kategorier tildelt til en ressource, leder Finance and Operations efter standardkategorien på timepriser for omkostninger og indtægter.

### <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurere projektressource- og rollekarakteristika

En projektleder kan bruge projektressourcefunktionaliteten til at oprette de roller, der er nødvendige for projektet. Roller kan bruges, hvis bekræftede ressourcer stadig er ukendte, når ressourcer reserveres. Roller kan midlertidigt reserveres som planlagte ressourcer, så du kan fortsætte med projektplanlægningsfaserne.

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarie:** Contoso blev ansat til at udføre et tids- og materialeprojekt, der har et godkendt projektcharter. Juniorprojektlederen er stadig ved at færdiggøre omfanget af projektet. Ressourcestyringen identificerer i øjeblikket bestemte ressourcer, der skal reserveres til arbejde på det nye projekt. På grund af projektets kritiske natur har projektsponsoren anmodet om, at en af rollerne er seniorprojektleder. Ressourcechefen skal anskaffe den nye ressource og definere rollen i systemet i tilfælde af, at juniorprojektlederen kræver ressourceoplysninger under projektplanlægningen.

Følgende fremgangsmåde viser, hvordan ressourcechefen kan konfigurere seniorprojektlederrollen og knytte ressourceegenskaber til den. Rollen kan senere bruges til at søge efter tilgængelige ressourcer, der svarer til de krævede ressourcekompetencer.

1. På siden **Konfigurer roller** skal du vælge **Ny** og angive følgende værdier:

    - **Rolle-id:** Seniorprojektleder
    - **Beskrivelse:** Seniorprojektleder

2. Vælg **Opret**.
3. Vælg rollen **Seniorprojektleder**, og vælg derefter **Konfigurer egenskaber**.
4. Vælg **Færdighed** i feltet **Karakteristikatype**.
5. I feltet **Tilgængelige karakteristika** skal du angive den færdighed, du søger efter.
6. I **Karakteristikatype** feltet skal du vælge **Certifikat**.
7. I feltet **Tilgængelige karakteristika** skal du angive den certifikattype, du søger efter.

### <a name="assign-a-project-resource-to-a-project"></a>Tildele en projektressource til et projekt

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgradering fase 2**.
2. Under fanen **Projektteam og planlægning** skal vælge **Tilføj**.
3. I feltet **Rolle** skal du vælge **Teammedlem**.
4. Vælg **Reservér fra kalender**.
5. På siden **Ressourcetilgængelighed** skal du vælge **Vis indstillinger**.
6. På siden **Juster visningsindstillinger** skal du angive følgende værdier:

    - **Viser format for datoområde:** Dag
    - **Vis beskrivelser af tilgængelighed:** Ja
    - **Vis resterende kapacitet:** Ja

7. Vælg en ressource på listen over ressourcer.
8. Vælg **Definitiv reservation** og **Fuld kapacitet**.


### <a name="assign-a-resource-to-a-default-role"></a>Tildele en ressource til en standardrolle

Som en hjælp kan projektledere eller ressourcechefer rulle længere ned i de ressourcer, der kan reserveres til et projekt. Du kan knytte en standardrolle til en eksisterende ressource eller en nyligt erhvervet ressource. Da Daniel f.eks. blev ansat, havde han erfaring og kompetence til at udfylde rollen Forretningsanalytiker. Ressourcechefen tildelte denne rolle som Daniels standardrolle. Derfor tilføjede ressourcechefen Daniel til en pulje af forretningsanalytikere, der er tilgængelige til at arbejde på projekter.

Under ressourcereservationen kan projektledere filtrere de ressourceroller, der er tilgængelige for arbejde på projekter. De kan bruge disse oplysninger som et kriterium, når de foretager beslutningsanalyse med flere kriterier under ressourceopfyldelsen. De kan også føje andre ressourcekarakteristika til filteret for at søge efter ressourcer, som har særlige kvalifikationer, uddannelse og erfaringer med et givent projekt.

**Scenarie:** Et godkendt projekt er startet, og rollen som seniorprojektleder blev reserveret som en planlagt ressource i løbet af projektets planlægningsstadie. Ressourcestyringen har nu fået en ressource, der skal opfylde rollen som seniorprojektleder.

1. Vælg **Daniel Goldschmidt** på siden **Liste over ressourcer**.
2. På siden **Ressourcerolle** skal du vælge **Ny** og angive følgende værdier:

    - **Gyldig fra:** Angiv den aktuelle dato.
    - **Udløb:** Angiv **Aldrig**.
    - **Rolle:** Angiv **Seniorprojektleder**.

3. Vælg **Gem**, og luk derefter siden.
4. Under fanen **Kompetencer** skal du tilføje færdigheden **ProjectMgmt** og **PMP**-certifikatet.

## <a name="set-up-role-based-pricing"></a>Konfigurere rollebaserede priser
Alle omkostninger, salg og overførselspriser kan indstilles for roller.

1. På siden **Salgspris (time)** skal du vælge **Ny**, og angive en ikrafttrædelsesdato.
2. Vælg en rolle i kolonnen **Rolle**.
3. I kolonnen **Prissætning** skal du angive en pris for den valgte ressourcerolle.

## <a name="form-a-project-team"></a>Opret et projektteam
Hvis en projektleder vil bruge de roller, der er tidligere angivet i et projekt, skal han eller hun knytte rollerne til projektet. Der kan tildeles flere roller til et projekt. For at undgå forvirring, mærker Finance and Operations automatisk disse roller under reservation. Hvis projektlederen f.eks. kræver tre softwareteknikere, oprettes der automatisk tre softwareteknikerroller, der navngives **softwaretekniker 1**, **softwaretekniker 2** og **softwaretekniker 3**. Hvis rollekarakteristika tidligere var defineret for rollen, anvendes de som et filter under søgninger efter en ressource. Du kan tilføje yderligere karakteristika efter behov for at indsnævre søgningen yderligere.

Visningsindstillinger kan også tilpasses for at give et bedre overblik over ressourcetilgængelighed. Er der indstillinger, som kan vise tilgængelighed pr. time, dag, uge, måned, kvartal og år. Der er også en indstilling, som kan vise tilgængelig og resterende kapacitet for ressourcer. Denne indstilling er nyttig til tidsstyring, når du skal vurdere ledig tid til aktiviteter eller ressourcetilgængelighed.

Projektlederen kan vælge en rolle på siden, og hvis der er en tilgængelig ressource, der passer til behovet, kan han eller hun vælge at reservere en ressource, der kan udfylde rollen. Bemærk, at ressourcerne ikke behøver at være reserveret på dette tidspunkt i planlægningen. Når du opretter et arbejdsopgavehierarki, kan du erstatte roller med bemandingsressourcer til projektet. Hvis roller erstattes med bemandingsressourcer i arbejdsopgavehierarkiet, opdaterer ressourcekonfigurationen automatisk projektteamlisten og -planlægningen.

[![Projektteamliste, der omfatter både roller og faktiske ressourcer](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektlederen har forskellige muligheder for reservation af en ressource til et projekt, f.eks. **Resterende kapacitet**, **Fuld kapacitet**, **Kapacitetsprocent** og **Angiv timer**. Disse reservationsindstillinger kan annulleres når som helst, hvis ressourcetildelinger ændres. Der findes to typer reservationer:

- **Definitiv reservation** – Ressourcereservationen blev godkendt og bekræftet for arbejde på opgaven for den angivne varighed.
- **Foreløbig reservation** – Ressourcereservationerne er foreløbig angivet til at arbejde på opgaven for den angivne varighed.

I følgende fremgangsmåde beskrives, hvordan et projektteam oprettes.

### <a name="create-a-project-team"></a>Oprette et projektteam

1. Vælg et projekt på listesiden **Alle projekter**, og vælg derefter **Rediger**.
2. Under fanen **Projektteam og planlægning** i feltet **Planlæg slutdato** skal du angive startdato for tidsplanen plus en måned. For eksempel hvis tidsplanens startdato er 24. juni 2017 (24/06/2017), skal du angive **24/07/2017**.
3. Vælg **Tilføj**.
4. I ruden **Føj roller til projektet** i feltet **Rolle** skal du vælge **Seniorprojektleder**.
5. Vælg **Påkrævede kompetencer**.
6. På siden **Vælg egenskaber** er de karakteristika, som du tidligere har angivet for seniorprojektlederrollen markeret som standard. Vælg **OK**.
7. På siden **Føj roller til projekt** i feltet **Antal ressourcer** skal du angive **1**.
8. I feltet **Ressource** viser opslaget alle ressourcer, der har de nødvendige kompetencer. Vælg **Daniel Goldschmidt**, og vælg derefter **Opret**.
9. Vælg **Tilføj** på siden **Projekt**.
10. I ruden **Føj roller til projektet** i feltet **Rolle** skal du vælge **Teammedlem**. Angiv **5** i feltet **Antal ressourcer**.
11. Vælg **Opret**.
12. På siden **Projekter** skal du vælge **Opfyld ressource**.

## <a name="resource-capacity-synchronization"></a>Synkronisering af ressourcekapacitet
Processerne til ressourcesynkronisering hjælper med at sikre, at oplysningerne til kalenderen og basiskalenderen videreføres til ressourceplanlægning for projektet. Hvis kalenderen ændres, foretager processerne de nødvendige opdateringer af planlægningen af projektressourcerne. Processerne forbedrer også ydeevnen, da kalenderens ressourceoplysninger synkroniseres på forhånd. Opdateringer til oplysninger om ressourceplanlægning udføres derfor hurtigere. Vi anbefaler, at du planlægger processerne som en batch i stedet for én ad gangen. Ellers er der risiko for, at nogen vil glemme inklusive-datoerne, hvor oplysningerne sidst blev synkroniseret. Hvis inklusive-datoer ikke bruges, kan der opstå mellemrum under synkronisering af datoer.

![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synkronisér ressourcekapacitet, opkøb

Synkroniseringsprocessen er designet til at synkronisere alle oplysninger i ressourcekalenderen. Disse oplysninger omfatter basiskalenderoplysninger om eventuelle ændringer af projektets tabel for ressourcekalenderkapacitet. Hvis der tilføjes nye ressourcer i projektet, hjælper synkroniseringen med at sikre, at de opdaterede kalenderoplysninger er tilgængelige. Denne synkronisering kan udføres når som helst.

Vi anbefaler, at du bruger en batch. Indstillingerne er tilgængelige under synkronisering af kapacitetsreservationer.

1. Vælg **Projektstyring og regnskab** &gt; **Periodisk** &gt; **Kapacitetssynkronisering** &gt; **Synkronisér ressourcekapacitet akkumuleringer**.
2. Angiv indstillingerne i følgende tabel.

    | Indstilling      | Betegnelse |
    |-------------|-------------|
    | Periodekode | Vælg datointervalkoden for Finans for at angive start- og slutdatoer for synkroniseringsprocessen for ressourcekapacitet akkumuleringer. |
    | Igangsæt dato  | Angiv startdatoen for synkroniseringsprocessen for ressourcekapacitet akkumuleringer. |
    | Slutdato    | Angiv slutdatoen for synkroniseringsprocessen for ressourcekapacitet akkumuleringer. |

[![Synkroniseringsproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Konfigurere roller i WBS-skabeloner
Projektledere kan konfigurere WBS-skabeloner, som de kan anvende, når de opretter et arbejdsopgavehierarki (WBS) til nye projekter. Projektledere kan tilføje roller, når de opretter en skabelon. Benyt følgende fremgangsmåde til at tildele en rolle til en WBS-skabelon. 

1. Vælg **Projektstyring og regnskab** &gt; **Konfiguration** &gt; **Projekter** &gt; **Skabeloner til arbejdsopgavehierarki**.
2. Vælg **Detaljer** for en valgt WBS-skabelon.
3. Markér en opgave på listen, og vælg derefter en rolle, der skal tildeles opgaven, i feltet **Rolle**.

### <a name="work-with-a-wbs"></a>Arbejde med et WBS

Du kan oprette et nyt WBS, eller du kan kopiere et WBS fra en eksisterende WBS-skabelon. En projektleder kan nemt administrere ressourcerne ved at tildele roller til nye opgaver i WBS'et. Roller kan erstattes, enten når der er skaffet en ressource, eller når der er identificeret en bekræftet ressource til at arbejde på opgaven. Denne fleksibilitet gør det muligt for projektledere at udføre følgende opgaver:

- Identificere det antal ressourcer, der kræves til WBS-arbejdspakker.
- Forkalkulere projektomkostninger.
- Bestemme et foreløbigt budget.
- Anslå varighed af aktivitet, baseret på roller og ressourcer.
- Udvikle nogle projektstyringsplaner, baseret på de tilgængelige projektoplysninger.

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
<td>Tilføj automatisk planlagte ressourcer ved hjælp af roller, der er knyttet til en opgave. Finance and Operations foreslår automatisk planlagte ressourcer ved hjælp af beslutningsanalyse med flere kriterier, som er baseret på roller. Når roller og tidsforbrug (timer) er angivet for opgaverne i et WBS, og efter strukturen er blevet frigivet, skal du vælge <strong>Generér team automatisk</strong>. Det nødvendige antal planlagte ressourcer føjes til WBS og fanen <strong>Projekt og teamplanlægning</strong>.</td>
</tr>
<tr class="odd">
<td>Ressource (rulleliste)</td>
<td>På siden <strong>Start ressourcetildeling</strong> kan du vælge ressourcer, som skal reserveres definitivt eller foreløbigt, baseret på den angivne varighed. Du kan justere visningsindstillingerne og angive varigheden af ressourceaktiviteter. Du kan vælge og tildele ressourcer på arbejdspakkeniveau ved hjælp af følgende indstillinger:
<ul>
<li><strong>Accepter</strong> – Bekræft ændringer af den ressource, der er tildelt en opgave.</li>
<li><strong>Annuller</strong> – Annuller ændringer af den ressource, der er tildelt en opgave.</li>
<li><strong>Tildel automatisk</strong> – En tilgængelig bemandingsressource, der har en matchende rolle, vælges automatisk og tildeles til den markerede opgave.</li>
</ul></td>
</tr>
</tbody>
</table>

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgradering fase 2**.
2. Vælg **Plan** &gt; **Aktiviteter** &gt; **Arbejdsopgavehierarki**.
3. Vælg **Ny** for at føje følgende aktiviteter på niveau et til WBS:

    - Initiering
    - Planlægning
    - Udfører
    - Overvågning og kontrol
    - Afslut

4. Angiv datoerne og tidsforbruget (timer), som vist i følgende illustration.

    [![Angivelse af datoer og indsats](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Vælg opgavelinjen **Initiering**, og vælg derefter **Seniorprojektleder** i feltet **Rolle**.
6. Vælg **Publicer**.
7. På samme linje i feltet **Ressource** skal du vælge **Daniel Goldschmidt**, og derefter vælge **Godkend**.
8. Vælg opgavelinjen **Planlægning**, og vælg derefter **Forretningsanalytiker** i feltet **Rolle**.
9. Vælg **Publicer**, og vælg derefter **Generér team automatisk**.
10. Vælg **Ja** i den dialogboks, der vises.
11. I feltet **Ressource** skal du kontrollere, at værdien er **Forretningsanalytiker 1**.
12. For ressourcen **Forretningsanalytiker 1** skal du åbne opslaget og vælge **Start ressourcetildeling**. Vælg derefter en arbejder til opgaven.
13. Vælg **Tildel foreløbigt** &gt; **Fuld kapacitet**.

    > [!NOTE] 
    > Du modtager ikke en advarsel om, at den angivne ressource nu er 2, fordi antallet af ressourcer forbliver på 1.

14. På siden **Arbejdsopdelingsstruktur** skal du validere ressourcetildelingen på WBS'et og derefter vælge **Gem**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressourceopfyldelse for planlagte ressourcer
En projektleder kan planlægge nødvendig ressourceroller for et projekt. Ressourcestyringen ser disse planlagte ressourcer som anmodninger på siden **Opfyldelse af ressource** og kan tildele faktiske ressourcer.

1. På siden **Alle projekter** skal du vælge projektet **XYZ-opgradering fase 2**.
2. Vælg **Projekt**, og vælg derefter **Rediger**.
3. Under fanen **Projektteam og planlægning** skal vælge **Tilføj**.
4. I dialogboksen **Tilføj roller** skal du vælg rollen **Softwareudvikler**.
5. Vælg **Opret**, og luk derefter projektsiden.
6. På siden **Opfyldelse af ressource** skal du vælge **Softwareudvikler 1** til projektet **XYZ-opgraderingsprojekt fase 2**.
7. Vælg en arbejder, og vælg derefter **Tildel**.
8. Kontroller, at linjen for **Softwareudvikler 1** er blevet fjernet for **XYZ-opgraderingsprojekt fase 2**.
9. Under fanen **Projektteam og planlægning** for projektet **XYZ-opgradering fase 2** skal du kontrollere, at den arbejder, som du valgte i det forrige trin, er blevet tilføjet som **Softwareudvikler**.

## <a name="requests-for-project-resources"></a>Anmodninger om projektressourcer
Planlægningsfunktionen projektressource giver kun ressourcechefer mulighed for at distribuere bemandingsressourcer på opgaver eller projekter. Udfør følgende opgaver for at aktivere denne funktion, eller kontrollér, at de er blevet fuldført:

- Konfigurer nummerserier.
- Konfigurer arbejdsgange i Projektstyring og regnskab.
- Aktivér arbejdsgange for ressourceanmodning

Når de foregående opgaver er fuldført, kan du udføre følgende opgaver efter behov:

- Opret en ressourceanmodning fra en midlertidigt reserveret bemandingsressource.
- Overvåg ressourceanmodninger.
- Opfyld ressourceanmodninger.
- Anmod om en bemandingsressource fra et WBS.
- Reservér ressourcer til et projekt uden at have en anmodning om en bemandingsressource.

## <a name="monitor-project-teams"></a>Overvåg projektteam
1. På siden **Alle projekter** skal du vælge linket **Projekt-id** for projektet **XYZ-opgradering fase 2**.
2. På oversigtspanelet **Projektteam og planlægning** skal kontrollere, at projektets ressourcer er angivet korrekt.

