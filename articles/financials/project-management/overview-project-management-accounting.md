---
title: Projektstyring og regnskab
description: "Projektstyrings- og regnskabsfunktioner kan bruges i flere brancher til at yde en service, fremstille et produkt eller opnå et resultat."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cd30c9278c58f8e0ca9b50f67a999708bd64c0a2
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="project-management-and-accounting"></a>Projektstyring og regnskab

[!include[banner](../includes/banner.md)]


Projektstyrings- og regnskabsfunktioner kan bruges i flere brancher til at yde en service, fremstille et produkt eller opnå et resultat.  

Et projekt er en gruppe af aktiviteter, der er udviklet til at yde en service, fremstille et produkt eller opnå et resultat. Projekter forbruger ressourcer og generere økonomiske resultater i form af indtægter eller aktiver.

## <a name="projects-across-industries"></a>Projekter på tværs af brancher
Projektstyring og regnskabsfunktioner kan bruges i flere brancher som vist i følgende illustration. [![Projekter på tværs af brancher](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

I et callcenter kan en billet bruges til at beskrive det sæt handlinger, der er nødvendige for at løse et opkald. Konsulentfirmaer, f.eks. organisationer med ledelsesmæssig eller teknisk rådgivning eller reklamebureauer, ser deres aktiviteter som projekter. I marketing repræsenterer en kampagne en samling af arbejde, der skal leveres. I projektbaseret produktion vedrører en produktionsordre forskelligt arbejde, der skal udføres for at producere nogle færdige varer. Uanset navnet, der bruges til dem, omfatter disse projekter, ressourcer, planer og omkostninger, og projektstyringen og regnskabsfunktionaliteten i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kan hjælpe med planlægning, udførelse og analyse af disse projekter.

## <a name="project-phases"></a>Projektfaser
Selvom følgende procesforløb er rettet mod eksterne projekter eller et projekt, der er fuldført for en eller flere kunder, gælder funktionen også for interne projekter, der udelukkende er omkostningsbaseret. 

![3 projektstadier](./media/3-stages-of-a-project.png) 

Som vist i den foregående illustration kan projektstyring og regnskab inddeles i tre faser:

1.  Start
2.  Udfør
3.  Analysér

## <a name="initiate-the-project"></a>Starte projektet
Under igangsættelsen af projektet forekomme flere vigtige processer. Du kan bruge et projekttilbud til at kommunikere det anslåede forbrug af arbejdskraft, udgifter og materialer til kunden. Du kan registrere faktureringsvilkår, grænser og aftaler i en projektkontrakt. Du kan bruge et arbejdsopgavehierarki (WBS) til at planlægge og vurdere arbejdet. Du kan oprette overslag og budgetter som vejledning til udførelse af projekter. Følgende illustration viser strukturen i et projekt.[![projektstruktur](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Opret projekttilbud

I et projekts første salgsfase kan du bruge et projekttilbud til at give kunden et ikke-bindende tilbud. Et tilbud kan inkludere mange elementer, f.eks. de varer og tjenester, der gives tilbud på, generelle kontaktoplysninger, særlige samhandelsaftaler og rabatter samt eventuelle skatter og tillæg.

Du kan også udstede en garanti for en projekttilbudstransaktion mellem din organisation og kunden. Når projekttilbuddet er oprettet, kan du oprette en garantianmodning for debitoren og sende den til banken. Når banken har godkendt anmodningen, udstedes garantien til kunden. 

Du kan finde flere oplysninger under [Projekttilbud](project-quotations.md).

### <a name="create-project-contracts"></a>Opret projektkontrakter

Når du indgår en kontrakt med en kunde eller anden finansieringskilde om at fuldføre et projekt, skal du først oprette en projektkontrakt. Derefter, når du opretter projektet, skal du tildele det til den tilsvarende kontrakt. Den type projekt, du opretter til en projektkontrakt, afgør, hvilken metode der bruges til fakturering af projektdebitorerne. Du kan ændre en projektkontrakt og det relaterede projekt, men du kan ikke ændre projekttypen. Yderligere oplysninger om projekttyper finder du i afsnittet "Oprette projekter".

Yderligere oplysninger om projektkontrakter finder du i [Projektkontrakter](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Oprette arbejdsopgavehierarkier

Detaljeringsgraden i et WBS afhænger af niveauet af nøjagtighed, der kræves i estimater og niveauet for registrering, der kræves mod disse estimater. Projekter, som har meget lav tolerance for forsinkelser i tidsplan eller omkostninger, kræver normalt en mere detaljeret WBS og kræver også omhyggelig sporing af igangværende arbejder og omkostninger i forhold til WBS. 

Du kan finde flere oplysninger i [Arbejdsopgavehierarkier](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Oprette projektprognoser og budgetter

Du kan bruge prognosebaseret budgettering, hvis organisationen har et operationelt perspektiv og fokuserer på de indtægter og omkostninger, der er udledt af specifikke transaktioner. Du kan imidlertid bruge budgettering, hvis organisationen fokuserer mere på økonomiske beløb. Hver metode har sine fordele. Yderligere oplysninger finder du [Projektprognoser og budgetter](project-forecasts-budgets.md).

### <a name="create-projects"></a>Opret projekter

Du kan oprette seks typer projekter i Microsoft Finance and Operations. Hver enkelt projekttype er angivet forskelligt med hensyn til omkostninger og indtægtsføring. Den projekttype, du vælger, afhænger af formålet med projektet. I følgende tabel beskrives den typiske brug af de enkelte projekttyper.

                                                                                                                                                                         |
| Projekttype      | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tid og materialer | I tids- og materialeprojekter faktureres kunden for alle omkostninger, der påløber et projekt. Dette omkostninger omfatter omkostninger for timer, udgifter, varer og gebyrer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Fastpris       | Fakturaerne i fastprisprojekter består af acontotransaktioner. Et fastprisprojekt faktureres i henhold til en faktureringsplan, der er baseret på en projektkontrakt. Indtægter for et fastprisprojekt kan beregnes og bogføres i løbet af projektet ved hjælp af metoden afsluttet procentdel. Omsætning kan også beregnes og bogføres, når projektet er fuldført, ved hjælp af metoden afsluttet kontrakt. Virksomheder kan ofte have fordel af at bruge værdien af igangværende arbejde (IGVA) til at beregne færdiggørelsesgraden af et projekt eller en gruppe projekter.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Investering        | Investeringsprojekter er projekter, der ikke umiddelbart giver indtjening. De bruges typisk til langfristede interne projekter, hvor omkostningerne skal kapitaliseres. I et investeringsprojekt kan der kun registreres omkostninger til varer, timer og udgifter. Omkostningerne i et investeringsprojekt spores og kontrolleres ved hjælp af estimatfunktionaliteten. Investeringsprojekter kan konfigureres med en valgfri maksimal kapitalisering. Som investeringsprojektet skrider frem, bogfører du dets omkostninger på IGVA-konti, hvor omkostningerne placeres, indtil projektet er afsluttet. Når projektet elimineres, overføres du IGVA-værdien til et anlægsaktiv, en finanskonto eller et nyt projekt. Bemærk! Posteringer på investeringsprojekter vises ikke på siderne **Bogfør omkostninger**, **Periodiser omsætning** eller **Opret fakturaforslag**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Omkostningsprojekt      | Ligesom investeringsprojekter bruges omkostningsprojekter typisk til at holde styr på interne projekter, og der kan kun registreres timer, udgifter, og varer for dem. Omkostningsprojekter er imidlertid normalt af kortere varighed end investeringsprojekter. I modsætning til investeringsprojekter kan omkostningsprojekter desuden ikke kapitaliseres på statuskonti. I stedet bogføres projektposteringerne kun på driftskonti. **BEMÆRK** Posteringer på omkostningsprojekter afspejles ikke på siderne **Bogfør omkostninger**, **Periodiser omsætning** eller **Opret fakturaforslag**. Da omkostningsprojekter typisk bruges til at holde styr på interne projekter, behøver de normalt ikke at være knyttet til en debitorkonto. Hvis din installation kræver, at der oprettes varebehov for indkøbsordrer, skal du dog knytte omkostningsprojekt til en debitor. Denne tilknytning kræves, fordi varebehov administreres som salgsordrelinjer, og systemet kræver, at der angives en debitor. Denne opsætning resulterer imidlertid ikke i, at varebehov automatisk oprettes ud fra en indkøbsordre. For omkostningsprojekter ignoreres indstillingen **Opret varebehov**. Hvis du skal bruge et varebehov i et omkostningsprojekt, kan du oprette det manuelt, når blot en debitor er knyttet til projektet. |
| Intern          | Interne projekter bruges til at følge op på omkostninger for et projekt, der er internt i organisationen. Interne projekter kan levere et planlægningsværktøj til at styre ressourceforbruget. **Bemærk!** Posteringer på interne projekter afspejles ikke på siderne **Periodiser omsætning** eller **Opret fakturaforslag**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Klokkeslæt              | Tidsprojekter bruges til at registrere tid, der er tilknyttet ikke-fakturerbare og ikke-produktive aktiviteter, f.eks. et projekt, der sporer sygedage for arbejdere. Posteringer på tidsprojekter bogføres ikke i finans. De medtages i stedet i rapporterne over brugen af arbejdere. Der kan kun registreres timetransaktioner i tidsprojekter. Du bruger en timekladde eller timeseddel til at registrere disse timer til projektet. Når timerne er registreret, vises de som projektposteringer, men de har ikke tilsvarende bilagsposteringer. **Bemærk!** Posteringer på tidsprojekter afspejles ikke på siderne **Bogfør omkostninger**, **Periodiser omsætning** eller **Opret fakturaforslag**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |


### <a name="assign-workers-categories-and-resources"></a>Tildel arbejdere, kategorier og ressourcer

Du kan planlægge arbejderressourcer baseret på enten krav og tidsplan for et projekt eller på færdigheder og tilgængelighed af arbejdere. Ved hjælp af ressourceplanlægningsfunktionerne kan du gøre effektivt brug af organisationens medarbejdere. Du kan hurtigt finde de mest kvalificerede medarbejdere, der er tilgængelige til at arbejde på projektet. Du kan også nemt se, hvordan disse medarbejdere kan anvendes mere effektivt i løbet af projektet. 

Her er nogle af de måder, du kan bruge ressourceplanlægningsfunktionaliteten på:

-   Bruge oplysningerne om en arbejders attributter, f.eks. uddannelse, færdigheder, certificeringer, projekterfaring og andre attributter, til at se, om arbejderen opfylder kravene til et projekt.
-   Bruge oplysninger om en arbejders kalender og tilgængelighed til at sammenligne arbejderens tidsplan med projektkalenderen.
-   Gennemse kapaciteten for den enkelte medarbejder, og find ud af, hvordan kapaciteten udnyttes. Hvis en medarbejder f.eks. ikke udnyttes fuldt ud, kan vedkommende tildeles til et projekt, der passer til medarbejderens tilgængelighed og attributter.
-   Gennemse en medarbejders tilgængelighed for at sikre, at der ikke er kalenderkonflikter med medarbejderens tildelinger.
-   Gennemse oplysninger om udnyttelse af en medarbejder i enten en oversigtsvisning, (f.eks. efter afdeling eller efter medarbejder), eller en detaljeret visning, (f.eks. efter medarbejdere i en afdeling eller efter ugentlige detaljer for de enkelte medarbejdere).
-   Rediger ressourcetildelinger for forskellige tidsenheder, f.eks. dag, uge eller måned, for at optimere udnyttelsen af medarbejdere.

## <a name="execute-the-project"></a>Udfør projektet
Under udførelse af projekter registrerer teammedlemmer eller ledere arbejde og de udgifter, der påløber, ved hjælp af timesedler, udgiftsrapporter og andre forretningsdokumenter. Projektledere har værktøjer, der giver dem mulighed for at overvåge forbruget af budgetbeløb for projektet. Projektledere kan også bestille, pluk eller fremskaffe materialer til projekter ved hjælp af indkøbsordrer og andre forretningsdokumenter. Fakturaer, der er udarbejdet og godkendt, så kunder kan faktureres for igangværende arbejde. Endelig registreres indtægter under denne proces, der kan påvirke virksomhedens regnskaber.

### <a name="manage-work-breakdown-structures"></a>Administrere arbejdsopgavehierarkier

En WBS er en beskrivelse af det arbejde, der skal udføres for et projekt. En WBS er et hierarki af opgaver. Den repræsenterer ikke kun arbejde for hver opgave, men også opgavens størrelse, omkostninger og varighede. 

Du kan finde flere oplysninger i [Arbejdsopgavehierarkier](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Administrere projektprognoser og -budgetter

Der er to måder at administrere og styre dine projekter på: projektprognoser og projektbudgetter. Du kan bruge prognosebaseret budgettering, hvis organisationen har et operationelt perspektiv og fokuserer på de indtægter og omkostninger, der er udledt af specifikke transaktioner. Du kan imidlertid bruge budgettering, hvis organisationen fokuserer mere på økonomiske beløb.

Yderligere oplysninger finder du [Projektprognoser og budgetter](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Oprette produktionsordrer

En projektrelateret produktionsordre kan knyttes til en salgsordre eller et varebehov vha. metoden for færdigvare eller metoden for forbrugt vare. Hvis produktionsordren desuden blev oprettet manuelt, findes der ingen tilknytning mellem produktionsordren og salgsordren eller varebehovet (ingen tilknytning til ordre). Hvis produktionsordren imidlertid blev oprettet automatisk i forbindelse med udfyldning af en salgsordre eller et varebehov, er der en tilknytning mellem produktionsordren og salgsordren eller varebehovet (tilknytning til ordre). 

Ud fra kombinationer af disse faktorer kan du benytte en af følgende metoder:

-   **Færdigvare/Tilknytning til ordre** – Knyt projektet til en salgsordre eller et vareforbrug. Når du bruger denne metode, bogføres de faktiske projektomkostninger, når salgsordren faktureres, eller når følgesedlen opdateres for varebehovet. Omkostningen vil blive bogført som en færdigvare.
-   **Færdigvare/Ingen tilknytning til ordre** – Faktiske omkostninger kan ikke bogføres, før produktionscyklussen for en vare har status **Afsluttet**. Omkostningen for færdigvaren vil blive bogført som en enkelt postering.
-   **Forbrugt vare/Tilknytning til ordre** – Knyt projektet til et vareforbrug. Hvis du bruger denne metode, kan du få vist de faktiske projektomkostninger, når produktionen har statussen **Igangsat** eller er rapporteret Færdigmeldt. Omkostningerne vil blive bogført som flere posteringer for projektvarer for råmaterialer og timer, der er forbrugt under produktionen. Når følgesedlen opdateres for varebehovet, vil der ikke blive bogført projektomkostninger. Du kan også angive det niveau i styklistehierarkiet, som projekterne i produktionen skal spores til.
-   ****Forbrugt vare/Ingen tilknytning til ordre**** – Knyt projektet til et vareforbrug. Hvis du bruger denne metode, kan du få vist de faktiske projektomkostninger, når produktionen har statussen **Igangsat** eller er rapporteret Færdigmeldt. Omkostningerne vil blive bogført som flere posteringer for projektvarer for råmaterialer og timer, der er forbrugt under produktionen. Du kan også angive, hvilket niveau i styklistehierarkiet, projekterne i produktionen skal spores til.

### <a name="procure-products-and-services"></a>Køb produkter og tjenester

Indkøb og salg af varer er en vigtig aktivitet i mange projektfokuserede forretninger.

#### <a name="purchase-orders-for-projects"></a>indkøbsordrer for projektet

Formålet med indkøbsordren angiver, hvornår indkøbsordren bruges og derfor, hvornår varerne faktureres på et projekt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Formål</th>
<th>Vareforbrug</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Opret en indkøbsordre direkte.</td>
<td>Indkøbsvarer fra en ekstern leverandør til forbrug på et projekt. Du kan oprette indkøbsordren på følgende måder:
<ul>
<li>Fra selve projektet. I dette tilfælde er projektet allerede defineret for indkøbsordren.</li>
<li>Ved at gå til projektindkøbsordren. Du skal både vælge den leverandør og det projekt, som indkøbsordren skal oprettes for.</li>
</ul></td>
<td>Varer er forbrugt, når kreditorfakturaen opdateres.</td>
</tr>
<tr class="even">
<td>Opret en indkøbsordre fra en salgsordre.</td>
<td>Indkøbsvarer, når du opretter en salgsordre fra et projekt.</td>
<td>Varerne er brugt, når salgsordren faktureres til kunden.</td>
</tr>
<tr class="odd">
<td>Opret en indkøbsordre ud fra et varebehov.</td>
<td>Indkøbsvarer, når du opretter et varebehov fra et projekt.</td>
<td>Varerne bruges, når følgesedlen for varebehovet opdateres.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Salgsordrer for projekter

I Projektstyring og regnskab kan du registrere forbruget af varer på flere måder. Du kan sælge eller købe varer fra et projekt, eller du kan reservere varer til et projekt. 

Du kan bestille varer fra firmaets lager til forbrug på et projekt. Eller du kan også købe varer fra en ekstern leverandør. Varer kan forbruges i alle typer projekter med undtagelse af tidsprojekter. 

Den måde, du bestiller varer på, afhænger af, hvor du bestiller dem fra:

-   Hvis du vil bestille varer fra firmaets lager, skal du oprette ordren som et varebehov. Hvis du bruger siden **Varebehov**, kan du konfigurere behovet, så du modtager varer som delleverancer. Derfor kan du udskyde forbruget af et antal varer, indtil du skal bruge varerne.
-   Hvis du vil bestille varer fra en ekstern leverandør, skal du oprette ordren som en indkøbsordre på siden **Indkøbsordre**.

> [!NOTE] 
> Følgesedlen for en projektrelateret salgsordre kan ikke annulleres, hvis varerne allerede er markeret til emballering. 

Følgende tabel indeholder metoderne til bestilling af varer og beskriver, hvordan varerne forbruges.

| Metode            | Formål                                                                                                                                                        | Forbrug af varetransaktioner                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Salgsordre       | Angiv en transaktion direkte i et tids- og materialeprojekt.                                                                                                   | Vareposteringer forbruges, når debitorfakturaen bogføres.                                                                               |
| Lagerkladde | Angiv og vedligehold hurtigt vareposter. Hvis du f.eks. vil angive et varebehov på grundlag af en udskrevet liste, kan du bruge lagerkladden. | Vareposteringer forbruges, når kladden bogføres.                                                                                        |
| Varebehov  | Angiv varer, der ikke skal forbruges med det samme. Denne metode giver dig mulighed for at holde styr på, hvor mange varer der er forbrugt i en enkelt varebehovspost.    | Vareposteringer forbruges, når følgesedlen opdateres. Med andre ord, varebehovet oprettes, når følgesedlen bogføres. |
| Indkøbsordrer   | Indtast posteringer på en af tre steder, afhængigt af indkøbsmetoden.                                                                              | Vareposteringer forbruges, når følgesedlen opdateres, eller når kunden eller leverandøren faktureres.                                      |

### <a name="process-project-invoices"></a>Behandl projektfakturaer

Projekttypen bestemmer, hvilken faktureringsproces der anvendes. Det er kun de to eksterne projekttyper (Tid og materialer og Fast pris), der kan faktureres. Tids- og materialeprojekter og fastprisprojekter er altid knyttet til en projektkontrakt. 

Før du opretter en debitorfaktura for et projekt, kan du oprette en foreløbig faktura eller et fakturaforslag. Du kan vælge projektposteringer, der skal medtages i en projektfaktura, i et fakturaforslag. Du kan derefter se fakturaoplysningerne, før du bogfører projektfakturaen og sender den til kunden eller anden finansieringskilde. 


Yderligere oplysninger om, hvordan du kan behandle projektfakturaer finder du i [Projektfakturering](../accounts-payable/project-invoicing.md).


### <a name="calculate-the-cost-to-complete-a-project"></a>Beregne omkostninger for at færdiggøre et projekt

Når du opretter et estimat, kan du vælge den metode, der bruges til at beregne omkostninger til at færdiggøre projektet. Du vælger en metode i feltet **Metode for færdiggørelsesomkostninger** på siden **Opret estimat**. Den metode, du vælger, anvendes separat for hver omkostningslinje i forkalkulationen. Mens en linje har statussen **Oprettet**, kan du ændre den metode, der er anvendt på siden **Omkostningsestimat**. 

I følgende tabel beskrives metoderne til beregning af kostprisen for at fuldføre et projekt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Samlet omkostning – faktisk</td>
<td>Forkalkulerede omkostninger skal angives manuelt. Efter kolonnen <strong>Samlede omkostninger</strong> eller <strong>Samlet antal</strong> på siden <strong>Omkostningsestimat</strong> er færdig, trækkes de faktiske omkostninger fra de totaler, der er angivet af brugeren. Resultatet er omkostningerne til færdiggørelse af projektet. Typisk spores status for omkostninger ikke baseret på eksempelvis antallet af hotelophold og måltider, der er registreret i hver periode. I stedet. Sporing er normalt baseret på en sammenligning mod totalbeløbet for estimerede timer. Denne metode kræver ikke en budgetmodel, og de samlede omkostninger eller det samlede antal kan ændres manuelt. Når der angives en værdi i kolonnen <strong>Samlede omkostninger</strong> eller <strong>Samlet antal</strong>, sammenligner Finance and Operations sammenligner denne værdi med de faktiske posteringer, der bogføres i perioden, og reducerer derefter værdien i kolonnen <strong>Antal, der skal fuldføres</strong> eller <strong>Færdiggørelsesomkostninger</strong>.</td>
</tr>
<tr class="even">
<td>Samlet budget – faktisk</td>
<td>Faktiske omkostninger sammenlignes mod den budgetmodel, som du vælger til at bestemme omkostningerne. Denne metode bruger en samlet budgetmodel, der omfatter planlagte posteringer. For at få en mere præcis visning af projektet, kan du justere budgetmodellen, når projektet er i gang. Hvis du skal justere budgettet, skal du følge denne generelle proces:
<ol>
<li>Kopiér budgetposteringer til en anden budgetmodel.</li>
<li>Sammenlign budgetposteringer med de faktiske posteringer.</li>
<li>Vedligehold, mindsk eller øg overslagene for den næste periode.</li>
</ol>
Finance and Operations reducerer ikke automatisk de budgetterede skøn. Der er derfor en god ide at bevare en oprindelig budgetmodel for fastprisprojektet for at oprette stamdata til sammenligning, når projektet er fuldført. 
> [!NOTE] Når du vælger denne metode, skal du bruge mindst to budgetmodeller. Én model bør indeholde det oprindelige budget. For den anden model skal du kopiere budgetposteringerne fra en anden model. Denne metode er kun gyldig for fastpris- og investeringsprojekter.</td>
> </tr>
<tr class="odd">
<td>Resterende budget</td>
<td>Denne metode bruger en resterende budgetmodel til at beregne færdiggørelsesomkostningerne for projektet. Når du bruger denne metode, lægges de faktiske omkostninger og de budgetterede beløb i den resterende budgetmodel sammen. Resultatet er samlede omkostninger. Før du bruger denne metode, skal du oprette en resterende budgetmodel for at fratrække posteringer, der er baseret på de faktiske posteringer, som er registreret i systemet. På siden <strong>Budgetmodeller</strong> skal du kontrollere, at felterne er markeret i gruppen <strong>Automatisk prognosereduktion</strong>. Typisk kopieres et resterende budget fra et oprindeligt budget. Når posteringerne indtastes, reduceres posteringerne i det resterende budget. Som projektet skrider frem, kan du trække budgetposteringer på det resterende budget, hvis du finder ud af, at det resterende budget skal justeres. <strong>Bemærk!</strong> Denne metode kan kun anvendes, hvis der er knyttet en budgetmodel til estimatet.</td>
</tr>
<tr class="even">
<td>Som forrige estimat</td>
<td>Der anvendes samme estimatmetode, som den der blev anvendt i forrige periode. Denne metode kræver en budgetmodel, hvis den forrige periode krævede en budgetmodel.</td>
</tr>
<tr class="odd">
<td>Sæt færdiggørelsesomkostninger til nul</td>
<td>Denne metode bruges typisk, før det forkalkulerede projekt elimineres. Denne metode svarer til de samlede estimater med de faktiske posteringer, der er bogført, og rydder kolonnen <strong>Færdiggørelsesomkostninger</strong>. Den resulterende færdiggørelsesgrad er altid 100 %. Feltet <strong>Budgettering</strong> markeres ikke for hver omkostningslinje, du opretter, og det samlede estimat kopieres fra det forrige omkostningsestimat. Det faktiske forbrug i estimatperioden trækkes fra færdiggørelsesomkostningerne for projektet. Denne metode kræver ikke en budgetmodel.</td>
</tr>
<tr class="even">
<td>Fra omkostningsskabelon</td>
<td>Den metode til færdiggørelsesomkostninger, der er angivet i den omkostningsskabelon, der er tilknyttet det valgte forkalkulerede projekt, anvendes.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Analysér projekt
På det mest grundlæggende niveau bruges et projekt til at gruppere transaktioner, der registrerer omkostninger, og derefter bogføre disse omkostninger til Finans. 

Disse transaktioner er generelt resultat af forretningsdokumenter som timesedler, udgiftsrapporter, kreditorfakturaer eller lagerposteringer. Livscyklus for et projekt normalt starter med estimater, prognoser og budgetter, der hjælper med at planlægge og forudse arbejdet og de finansielle virkninger af projektet. Når du analyserer et projekt, kan du ikke bare evaluere de posteringer, der er opstået under projektet, men også nøjagtigheden af dine estimater og prognoser, udnyttelsesgrader af medlemmerne af projektgruppen og projektets samlede succes.

### <a name="analyze-cash-flow"></a>Analysér likviditet

Brug overvågning af pengestrømme til at gennemse både budgetterede pengestrømme og de faktiske pengestrømme for et projekt. Du kan gennemgå pengestrømme, mens et projekt er i gang, eller du kan få vist pengestrømme i et fuldført projekt. 

Når du overvåger pengestrømme, kan du evaluere et enkelt projekt, bruge rapporter til at få vist flere projekter og overføre projektets pengestrømme til budgetterede pengestrømme i finans.

#### <a name="cash-inflow-forecasting"></a>Budgettering af indgående pengestrøm

Baseret på din installation kan du budgettere pengestrømme for et valgt projekt. Hvis projektdatoen f.eks. er 5. marts 2012, og du fakturerer den 31. marts 2012, kan du se her, hvordan du kan forudsige forfaldsdatoen og den forventede betalingsdato for salget:

-   **Projektdato:** 5. marts 2012.
-   **Fakturadato:** 31. marts 2012. Denne dato bestemmes ud fra fakturafrekvens. Til dette eksempel skal du angive fakturafrekvensen til den aktuelle måned. Derfor faktureres alle posteringer, der bogføres i marts måned, på den sidste dag i måneden.
-   **Forfaldsdato:** 14. April 2012. Denne dato bestemmes på basis af de betalingsbetingelser, der blev angivet for projektet. I dette eksempel har du valgt 14 dage som betalingsbetingelse. Derfor føjes 14 dage til fakturadatoen, så der fås en forfaldsdato, der hedder 14. april 2012.
-   **Forventet dato for salgsbetalingen:** 27. april 2012. Denne dato beregnes ved at lægge antallet af dage i feltet **Generelle bufferdage** på siden **Parametre for projektstyring og regnskab** til antallet af dage i feltet **Individuelle bufferdage** på siden **Projektkontrakter** og derefter føje totalen til antallet af dage i feltet **Forfaldsdato**. I dette eksempel har du angivet **3** i feltet **Generelle bufferdage** og **10** i feltet **Individuelle bufferdage**. Derfor føjes 13 dage til forfaldsdatoen, så der fås en forventet betalingsdato for salg, der hedder 27. april 2012.

De generelle bufferdage kan enten erstatte de individuelle bufferdage eller blive føjet til individuelle bufferdage:

-   Hvis du vil bruge de generelle bufferdage som en erstatning for de individuelle bufferdage, skal du angive det gennemsnitlige antal dage mellem forfaldsdatoen og den faktiske betalingsdato for kunder.
-   Hvis du vil føje de generelle bufferdage til individuelle bufferdage, skal du i feltet **Generelle bufferdage** angive dit skøn over antallet af dage mellem den dag, hvor kunden sender betalingen, og den dag, hvor betalingen modtages af din organisation.

Konfigurer individuelle bufferdage i projektets kontrakt. Dagene beregnes både ud fra forfaldsdatoen på salgsfakturaen og din organisations erfaring med en kundes betalingsmønster.

#### <a name="actual-cash-inflow"></a>Faktiske indgående pengestrømme

Faktisk indgående pengestrøm er meget lig budgettering, men du kan starte dine beregninger fra den første fakturadato. Her er et eksempel:

-   **Fakturadato:** 2. marts 2012.
-   **Forfaldsdato:** 16 marts 2012. Betalingsbetingelserne er angivet til 14 dage.
-   **Forventet salgsbetalingsdato:** 29. marts 2012. Beregningen omfatter tre generelle bufferdage og 10 individuelle bufferdage.

#### <a name="cost-forecasting"></a>Omkostningsbudgettering

Baseret på de dage, som er defineret , kan kostbetalingsdatoen afvige fra projektdatoen. I så fald beregnes kostbetalingsdatoen ved at føje antallet af dage fra projektdatoen til antallet af dage i betalingsbetingelserne. 

Projektdatoen i posteringen er f.eks. 5. marts 2012, og følgende betalingsbetingelser er angivet:

-   **Timer:** Aktuel måned (**M**)
-   **Udgifter:** 14 dage (**D14**)
-   **Varer:** 30 dage (**D30**)

Baseret på disse indstillinger følger her kostbetalingsdatoen for hver posteringstype:

-   **Timer:** 31. marts 2012, som er den sidste dag i den valgte måned.
-   **Udgifter:** 19. marts 2012, som er 14 dage efter datoen for posteringen.
-   **Varer:** 4. april 2012, som er 30 dage efter datoen for posteringen.

> [!NOTE] 
> Forfaldsdatoen for købsordren er baseret på kreditorposteringen, når projektets indkøbsordre er oprettet. Forfaldsdatoen bestemmes ikke af standardindstillinger. 

Kostbetalingsdatoen beregnes ikke på basis af bufferdage. Når et projekt er afsluttet, når alle efterkalkulationer og faktureringer er fuldført, bogføres både omkostninger og salg til driftskonti. 

Når alle salgs- og leverandørfakturaer er fuldført, kan du få vist relationen mellem felter på siden **Pengestrøm** og felter på siden **Projektopgørelser**.

| Pengestrømsside | Siden projektopgørelse. |
|----------------|-------------------------|
| Indgående pengestrømme   | Omsætning                 |
| Udgående pengestrømme  | Samlede omkostninger              |
| Nettopengestrømme | Bruttoavance            |

### <a name="review-costs"></a>Gennemgå omkostninger

Du kan overvåge de omkostninger, som organisationen har under et projekt, på siden **Omkostningsstyring**. Ved at sammenligne de oprindelige budgetterede omkostninger for projektet med de aktuelle faktiske omkostninger og de bindende omkostninger kan du bestemme, om projektet er på rette spor, over budgettet eller under budgettet. 

> [!NOTE] 
> Når du bruger siden **Omkostningsstyring** til at få vist den aktuelle status for projektomkostninger, kan du bruge de budgetmodeller, der blev valgt til det oprindelige budget og det resterende budget. Hvis du vælger andre budgetmodeller til beregning af omkostninger, vil resultaterne af beregningen ikke være nøjagtige.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Få vist de resterende budgetterede beløb

Hvis **Resterende budget** er valgt som metode til omkostningskontrol på siden **Parametre for projektstyring og regnskab**, beregner siden **Omkostningsstyring** de omkostninger, der ikke er bogført som faktisk eller markeres som bindende. Specielt mængderne under fanen **Generelt** i den nederste rude på siden **Omkostningsstyring** beregnes på følgende måder:

-   **Faktisk omkostning** – Det samlede beløb, der er blevet brugt på projektet for den valgte omkostningslinje. Det faktiske kostbeløb beregnes på siden **Finansopdateringer**.
-   **Bindende omkostning** – Den yderligere udgiftsmængde, som den juridiske enhed bundet sig til at betale. De specifikke bindende omkostningsbeløb beregnes på siden **Bindende omkostning**.
-   **Resterende budget** – Mængden af det oprindelige budgetterede beløb, der stadig er tilgængeligt for den valgte omkostningslinje. Det resterende budgetbeløb, der er beregnet på siden **Vis Finans**.
-   **Samlede omkostninger** – Summen af faktiske omkostninger, bindende omkostninger og de resterende budgetbeløb.

På siden **Omkostningsstyring** under fanen **Afvigelse** kan du få vist en sammenligning mellem den samlede forventede omkostning og det oprindelige budget. Denne sammenligning viser forskelle mellem disse beløb. Derfor kan du se, hvor dataene ikke stemmer overens. Afvigelsesbeløbene beregnes på følgende måder:

-   **Oprindeligt budget** – Det beløb, der oprindeligt blev budgetteret for den markerede omkostningslinje. Det oprindelige budgetbeløb, der er beregnet på siden **Vis Finans**.
-   **Samlede omkostninger** – Summen af faktiske omkostninger, bindende omkostninger og resterende budget som vist under fanen **Generelt**.
-   **Afvigelse** – Forskellen mellem de samlede omkostninger og det oprindelige budget.
-   **Afvigelse baseret på antal** – Den samlede forskel i beløb mellem den oprindelige prognose og den samlede prognose. Forskellen kan udtrykkes matematisk som (Antal i samlet prognose) x (Oprindelig gennemsnitspris – Samlet gennemsnitspris). Denne beregning gælder kun for projekttimer.
-   **Afvigelse baseret på pris** – Den samlede forskel i beløb mellem den oprindelige prognose og den samlede prognose. Forskellen kan udtrykkes matematisk som (Pris i oprindelig prognose) x (Antal i oprindelig prognose – Antal i samlet prognose). Denne beregning gælder kun for projekttimer.

#### <a name="viewing-the-total-budgeted-amounts"></a>Få vist de samlede budgetbeløb

Hvis **Samlet budget** er valgt som metode til omkostningskontrol på siden **Parametre for projektstyring og regnskab**, beregner siden **Omkostningsstyring** de faktiske omkostninger og de samlede omkostninger i projektet for at hjælpe dig med at finde eventuelle forskelle mellem dem. Specielt på siden **Omkostningsstyring** beregnes beløbene i kolonnerne i den nederste rude under fanen **Generelt** på følgende måder:

-   **Budgetterede omkostninger i alt** – Det samlede budgetterede beløb for den valgte omkostningslinje.
-   **Faktisk omkostning** – De samlede omkostninger, der er påløbet projektet til dato for de valgte omkostningslinjer.
-   **Bindende omkostning** – Det samlede beløb, der er blevet bundet for den valgte omkostningslinje.
-   **Afvigelse** – Forskellen mellem summen af faktiske og bindende omkostninger og de samlede omkostninger. Afvigelsen viser, om der skal specificeres flere omkostninger for det samlede budget.

På siden **Omkostningsstyring** under fanen **Afvigelse** kan du få vist forskellen mellem det samlede budget og det oprindelige budget ved at se følgende felter:

-   **Oprindeligt budget**– Det beløb, der oprindeligt blev budgetteret for omkostningslinjen. Det oprindelige budget, der er beregnet på siden **Vis Finans**.
-   **Budgetterede omkostninger i alt** – De samlede omkostninger, der oprindeligt blev budgetteret for omkostningslinjen. Budgetterede omkostninger i alt beregnes på siden **Vis Finans**.
-   **Afvigelse i** – Afvigelsen for omkostningslinjen. Beløbet beregnes ved at trække totalomkostningen fra det oprindelige budget.
-   **Afvigelse baseret på antal** – Den samlede forskel i beløb mellem det oprindelige budget og det samlede budget. Dette beløb beregnes ved at trække de samlede budgetterede timer fra de oprindeligt budgetterede timer, hvorefter forskellen ganges med den oprindeligt budgetterede kostpris. Forskellen kan udtrykkes matematisk som (Oprindelig budgetteret kostpris) × (Oprindeligt antal budgettimer – Samlet antal budgettimer). Denne beregning gælder kun for projekttimer.
-   **Afvigelse baseret på pris** –- Dette beløb beregnes ved at trække de samlede budgetterede timer fra de oprindeligt budgetterede timer, hvorefter forskellen ganges med det samlede timeforbrug. Forskellen kan udtrykkes matematisk som (Forbrugte timer i alt) × (Oprindeligt antal budgettimer – Samlet antal budgettimer). Denne beregning gælder kun for projekttimer.

### <a name="analyze-utilization"></a>Analysér udnyttelse

Udnyttelsesgraden er den procentdel af tid, hvor en arbejder præsterer fakturerbart arbejde eller produktivt arbejde i en bestemt arbejdsperiode. Fakturerbare timer er de af arbejderens timer, der kan opkræves hos en bestemt kunde. 

En arbejders udnyttelsesgrad beregnes ved at dele antallet af fakturerbare timer med antallet af arbejdstimer i en bestemt periode. Hvis arbejderen f.eks. har 30 fakturerbare timer i en periode, og antallet af arbejdstimer i den samme periode er 40, er arbejderens udnyttelsesgrad 75 %. 

Når du beregner udnyttelsesgraden for en arbejder, kan du enten beregne faktureringsgraden eller effektivitetsgraden:

-   **Faktureringsgrad** – Faktureringsgraden er forskellen mellem fakturerbare timer og ikke-fakturerbare timer eller normtimer.
-   **Effektivitetsgrad** – Forskellen mellem produktive timer og ikke-produktive timer eller normtimer. Produktive timer er de timer, som arbejderen bruger på bidrag til et bestemt projekt. Produktive timer faktureres normalt til kunder undtagen i tilfælde af interne projekter. Ikke-produktive timer faktureres aldrig til en kunde.

Du beregner udnyttelsesgrader på siden **Timeforbrug**. Beregningerne er baseret på standardindstillinger. Disse indstillinger angiver også, hvordan timer beregnes ved at tildele **Udnyttelse** eller **Byrde** til hver enkelt projekttype. Dette gælder for beregninger af faktureringsgrad og af effektivitetsgrad.

-   **Udnyttelse** – Timer, der rapporteres for den valgte projekttype, overvejes altid med hensyn til fakturerbarhed eller effektivitetsudnyttelse.
-   **Byrde** – Timer, der rapporteres for den valgte projekttype, overvejes altid med hensyn til ikke-fakturerbarhed eller ikke-effektivitetsudnyttelse.
-   **Ifølge linjeegenskab** – Linjeegenskaberne for en bestemt timepostering afgør, om timerne betragtes som værende fakturerbare eller som effektivitetsudnyttelse.
-   **Medtages ikke** – Timer medtages ikke i beregningen af fakturerbarhed eller effektivitetsudnyttelse.

På siden **Timeforbrug** kan du, ud over at se den samlede procentsats for udnyttelse for en arbejder eller et projekt, få vist antallet af timer, der indgik i beregningen af udnyttelsesgraden for hver af følgende timetyper:

-   **Ikke-inkluderede timer**– Disse timer medtages ikke i timeudnyttelsesgraden.
-   **Inkluderede timer** – Disse timer beregnes ved at tilføje indirekte tid og direkte tid. Disse timer er inkluderet i udnyttelsesgraden.
-   **Direkte tid** – Hvis du beregner en faktureringsgrad, er disse timer de samme som ikke-fakturerbare timer. Hvis du beregner en effektivitetsprocent, er disse timer de samme som ikke-produktive timer.
-   **Indirekte tid** – Hvis du beregner en faktureringsgrad, er disse timer de samme som fakturerbare timer. Hvis du beregner en effektivitetsprocent, er disse timer de samme som produktive timer.

Når du beregner udnyttelsesgraden for en arbejder, kan du bruge normtimer eller inkluderede timer. Hvis du bruger inkluderede timer, skal du sikre dig, at arbejderne registrerer al deres arbejdstid for timeseddelperioder, da beregningen er udtrykt som en procentdel af timer, der angives. Når du beregner timeudnyttelsesgraden for et projekt, projektkontrakt, kundepost eller kategori, skal du bruge inkluderede timer i beregningen.

### <a name="review-project-statements"></a>Gennemse projektopgørelser

Du kan oprette en projektopgørelse for at få vist et hurtigt øjebliksbillede af status for et projekt. Når du kører en projektopgørelse, kan du angive de kriterier, der skal bruges til at beregne projektopgørelsen ved at foretage valg under fanen **Generelt** på siden **Projektopgørelser**. Du kan vælge at medtage eller udelade følgende oplysninger:

-   Projekttyper
-   Transaktionstyper
-   Projektdato/finansdato
-   Data

Når sætningen er beregnet, kan du få vist følgende oplysninger under de forskellige faner på siden **Projektopgørelse**:

-   **Generelt**– Generelle oplysninger om projektets grundlæggende driftsstruktur.
-   **Drift** – Oplysninger om periodiseret omsætning.
-   **IGVF**– Oplysninger om saldi for igangværende arbejde.
-   **Forbrug**– Oplysninger om forbrug af timer, varer, udgifter og lønposter.
-   **Faktura**– Oplysninger om fakturaer og acontofakturering.
-   **Timesats** – Timesatser for timer, der er bogført til driftskonti.





