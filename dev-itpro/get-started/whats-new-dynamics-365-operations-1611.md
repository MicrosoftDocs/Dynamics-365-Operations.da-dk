---
title: "Nyheder eller ændringer i Dynamics 365 for Operations-version 1611 (november 2016)"
description: "Dette emne beskriver funktioner, der er nye eller ændrede i Dynamics 365 for Operations version 1611."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, UnifiedOperations
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 7fd8180bb3ae4ebf5a8dd4446ccd19e65cb6708d
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Nyheder eller ændringer i Dynamics 365 for Operations-version 1611 (november 2016)

[!include[banner](../includes/banner.md)]


Dette emne beskriver funktioner, der er nye eller ændrede i Dynamics 365 for Operations version 1611.

<a name="cost-accounting"></a>Driftsregnskab
---------------

<table>




<thead>
<tr class="header">
<th>Hvad du kan gøre</th>
<th>Hvorfor dette er vigtigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Definere omkostningselementdimensioner og importere omkostningselementers dimensionsmedlemmer.</td>
<td>Omkostningselementer bruges i Driftsregnskab til at kategorisere omkostninger og dokumentere strømmen af omkostninger. De primære omkostningselementer importeres enten via en Microsoft Dynamics 365 for Operations-dataconnector for at hente hovedkonti direkte fra Operations eller via en generisk dataconnector, hvor du henter hovedkonti via Microsoft Excel fra enhver anden type kildesystem. Når hovedkonti er importeret til omkostningsregnskab, bruges de som dimensionsmedlemmer af omkostningselementet. De sekundære omkostningselementer er brugerdefinerede og anvendes i fordelinger til dokumenter af strømmen af omkostninger.</td>
</tr>
<tr class="even">
<td>Tilknytte dimensioner for omkostningselement.</td>
<td>Hvis hovedkonti på tværs af juridiske enheder ikke kan deles på grund af lovbestemte regnskabsmæssige krav, kan du tilknytte dem, når du importerer dem til omkostningsregnskab for at få en holistisk visning på tværs af organisationen.</td>
</tr>
<tr class="odd">
<td>Definere omkostningsobjektdimensioner og importere omkostningsobjekters dimensionsmedlemmer.</td>
<td>Omkostningsobjekter er en hvilken som helst type objekt, som omkostninger er tildelt. Typiske omkostningsobjekter omfatter produkter, projekter, ressourcer, afdelinger, bærere og geografiske områder. Du kan enten bruge en Microsoft Dynamics-365 for Operations dataconnector til at få økonomiske dimensioner og værdier fra Operations eller bruge en generisk dataconnector, hvor du kan få dimensioner og værdier via Microsoft Excel fra enhver anden type kildesystem. Hvis du bruger den finansielle bærerdimension som objektdimension, er alle bærere, der importeres, dimensionsmedlemmer til omkostningsobjektet.</td>
</tr>
<tr class="even">
<td>Definere eller importere statistiske dimensioner.</td>
<td>Statistiske dimensionsmedlemmer måles i ikke-monetære enheder, såsom maskintimer og antallet af medarbejdere. De bruges i opgørelser eller som grundlag for distributioner og fordelinger.</td>
</tr>
<tr class="odd">
<td>Oprette skabeloner til providere af statistiske målinger.</td>
<td>En skabelon til provider af statistisk måling bruges til at transformere Dynamics 365 for Operations-data til statistiske målinger. Skabelonen tilknyttes derefter et bestemt statistisk dimensionsmedlem. Skabelonerne er forudfiltreret, så de viser kun de tabeller, der er knyttet til økonomiske dimensioner.</td>
</tr>
<tr class="even">
<td>Oprette finansposter for omkostningsregnskab.</td>
<td>Finanspost for omkostningsregnskab er en agnostisk Finans, der bruger sin egen kalender og valuta. Det spiller en vigtig rolle i behandlingen af alle omkostningsposteringer. Eksempelvis klassificerer et omkostningsregnskab for Finans omkostninger baseret på egne omkostningselementer og samler omkostninger baseret på egne objektdimensioner. Du kan oprette så mange finansomkostningsregnskaber, som du har brug for til rapportering på forskellige måder.</td>
</tr>
<tr class="odd">
<td>Oprette kontrolenheder for omkostninger.</td>
<td>Omkostningskontrolenheder udgør omkostningsstruktur og definerer flowet af omkostninger i omkostningsregnskabet Finans. De skal være forbundet med omkostningsobjektdimensioner for at repræsentere omkostningsobjektdimensioner i Finans.</td>
</tr>
<tr class="even">
<td>Behandle finansposter.</td>
<td>For at kunne måle den faktiske performance skal du have data. Dataene importeres ved hjælp af de forbindelser, du definerer for omkostningsregnskabet Finans. Når du behandler finansposterne, importeres dataene trinvist.</td>
</tr>
<tr class="odd">
<td>Behandle budgetposter.</td>
<td>For at kunne måle budgetperformance skal du have data. Dataene importeres ved hjælp af de forbindelser, du definerer for omkostningsregnskabet Finans. Når du behandler budgetposterne, importeres dataene trinvist.</td>
</tr>
<tr class="even">
<td>Oprette og anvende politikker for omkostningsfunktionalitet.</td>
<td>Du kan bruge en politik for omkostningsfunktionalitet til at klassificere omkostninger som faste, variable eller delvist variable. En politik er baseret på regler og datorelaterede. Alle omkostninger er som standard markeret som ikke-klassificeret, indtil du anvender en politik for omkostningsfunktionalitet og beregner virkningerne af reglen. Efter beregning bliver omkostningerne klassificeret.</td>
</tr>
<tr class="odd">
<td>Spore omkostninger.</td>
<td>For at hjælpe dig med at forstå virkningen af politikker for omkostninger kan omkostningsregnskab spore omkostninger til kildeværdierne og anvendte regler, som de kommer fra. Denne funktionalitet giver fuld sporbarhed af, hvornår omkostninger fandt sted, hvilke typer omkostninger der opstod, og hvilke funktionsregler der blev anvendt for omkostninger.</td>
</tr>
<tr class="even">
<td>Definere dimensionshierarkier.</td>
<td>Du kan oprette dimensionshierarkier for til en kategorisering eller klassificering. For eksempel kan du definere et hierarki af kategorisering, der er baseret på en omkostningselementdimension og dens medlemmer. Du kan også definere et hierarki af klassifikation, der er baseret på en omkostningsobjektdimension og dens medlemmer. Rapporteringsstrukturer bruges i følgende situationer:
<ul>
<li>Du definerer fordelinger, omkostningssatser og regler for omkostningstotaler.</li>
<li>Du kan få vist opgørelser ved hjælp af arbejdsområdet.</li>
<li>Du kan definere adgang for at få vist aggregerede data.</li>
<li>Du kan få vist data i Excel.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Oprette opgørelser, kan ses i arbejdsområdet.</td>
<td>Du kan bruge arbejdsområdet til at få et hurtigt overblik over de faktiske og budgetterede omkostninger samt afvigelser. Du kan filtrere data efter periode eller omkostningsniveau. Arbejdsområdet er udviklet til ledere, der er ansvarlig for omkostningsstyring. Det overholder de adgangsregler, der er defineret for dimensionshierarkier.</td>
</tr>
<tr class="even">
<td>Oprette rapporter ved hjælp af Excel. <strong>Bemærk:</strong> Du skal køre Microsoft Excel 2016.</td>
<td>Du kan eksportere data omkostningsregnskabets data direkte til Excel via dataenheder og bruge Microsoft PivotTable til at oprette rapporter.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Udgiftsstyring
| Hvad du kan gøre                                                            | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Omfordele fratrådte medarbejderes kreditkorttransaktioner.                     | Nogle gange, når en medarbejder er fratrådt, bliver hans eller hendes Active Directory-domæneservices-konto (AD DS) deaktiveret ved import af aktive kreditkorttransaktioner, der skal udgiftsføres. Tidligere kunne du tildele en delegeret for udgiftsregistrering eller vedhæfte kreditkorttransaktionerne til en udgiftsrapport. Du kan nu bruge siden **Kreditkorttransaktioner** til at tildele medarbejderen en kreditkorttransaktion, hvor den tilknyttede medarbejder er fratrådt. Når du gentildeleren en kreditkorttransaktion, kan transaktionen vælges til en udgiftsrapport og betales gennem den almindelige proces for refusion af udgiftsrapport. |
| Ændre kreditkortoplysningerne til udgifter for ventende og tidligere medarbejdere. | Du kan ændre udgiftsprocessens kreditkortoplysninger for ventende medarbejdere og tidligere medarbejdere. Tidligere kunne du kun ændre kreditkortoplysningerne for udgifter, hvis arbejderen er en aktiv medarbejder.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Kopiere en udgiftsrapport.                                                    | Du kan nu kopiere en eksisterende udgift, når du opretter en ny udgift på samme udgiftsrapport. Du kan kopiere en udgiftsrapport og alle de tilknyttede ikke–kreditkortudgifter til en ny udgiftsrapport. Du skal stadig udføre eventuelle nødvendige specificeringer og vedhæfte krævede kvitteringer, baseret på definerede udgiftspolitikker og kategorier. Du kan føje kreditkorttransaktioner til udgiftsrapporten ved at vælge at tilføje ikke-afstemte udgifter.                                                                                                                                                                                                                        |
| Masseredigere udgifter.                                                        | Nogle kreditkorttransaktioner kan ikke knyttes til en udgiftskategori, eller de kan være forkert tilknyttet, når de importeres. I så fald skal medarbejdere manuelt ændre den tilknyttede udgiftskategori. Når du administrerer ikke-afstemte udgifter, du kan nu masseredigere udgiftskategorien for de valgte udgifter. Desuden, når du administrerer valgte udgifter for en bestemt udgiftsrapport, kan du masseredigere projektet og yderligere oplysninger.                                                                                                                                                                                    |
| Ændre valutakursen for kreditkorttransaktioner.                     | Den faktiske valutakurs, der bruges til en kreditkorttransaktion, kan afvige fra den valutakurs, der er angivet i systemet. Tidligere kunne medarbejdere ikke ændre valutakursen for nogen transaktion med kreditkort, der blev importeret til Udgiftsstyring. Nu kan du angive en parameter på siden **Parametre for udgiftsstyring**, så valutakursen kan ændres for kreditkorttransaktioner.                                                                                                                                                                                                                                            |
| Oprette antikorruptionsattest for udgifter.                            | Nogle medarbejdere i en organisation kan have aktivitet med regeringsembedsmænd, og visse udgifter, der opstår som en del heraf, kan opfattes som bestikkelse. I Udgiftsstyring kan du nu oprette en antikorruptionsattest, der vises for valgte udgiftskategorier såsom måltider og gaver. Medarbejdere skal vælge, om udgifter, der er angivet for antikorruptionsattest, opfylder de kriterier, der er defineret af organisationens politikker.                                                                                                                                                                                     |
| Forhindre manuel angivelse af udgifter for specifikke udgiftskategorier.          | En udgiftskategori kan konfigureres til at repræsentere en kreditkorttransaktion, hvor kategorien ikke kan ændres. Et eksempel er et gebyr for sen betaling med kreditkortet. Du kan nu oprette en udgiftskategori, som kun tillader udgifter at blive oprettet gennem import. Denne funktion forhindrer medarbejdere i manuel oprettelse af en udgift for kategorien. Den tillader heller ikke ændring af kategorien for transaktioner, der er blevet importeret, og som bruger denne kategori.                                                                                                                                                                                   |
| Vedhæfte en kvittering til flere udgifter.                                     | En kvittering, der er overført til Udgiftsstyring, kan være relateret til flere udgifter. Tidligere skulle en kvittering, der var relateret til flere udgifter, overføres én gang for hver udgift. Du kan nu vedhæfte en kvittering til en udgift, der allerede er overført, og knytte den til en anden udgift i samme udgiftsrapport. Hvis du overfører en kvittering til hovedet i udgiftsrapporten, kan du også vælge en eller flere linjer, hvor kvitteringen skal vedhæftes.                                                                                                                                                                                        |
| Oprette udgifter, der er dateret i fremtiden.                                              | Når du f.eks. kopierer en udgiftsrapport, kan posteringsdatoen for en udgift have en fremtidig dato. Tidligere versioner giver ikke mulighed for udgifter, der er dateret i fremtiden. Du kan nu oprette og gemme udgifter, der har en fremtidig dato. Men du kan ikke sende en udgift, der er dateret i fremtiden.                                                                                                                                                                                                                                                                                                                                                                                 |
| Konfigurere momsudgifter for et område.                              | Udgifter, der påløber i forskellige delstater/provinser, kan være underlagt forskellige momssatser i nogle lande/områder. Du kan nu angive konfigurationer af momsudgifter på områdeniveau, ikke bare på niveauet for landet/området. Hvis du lader feltet **Delstat eller provins** stå tomt på siden **Momskonfiguration** , gælder momsgruppen for alle delstater/provinser i det angivne land/område.                                                                                                                                                                                                                                       |
| Konfigurere udgiftskreditkorttyper.                                          | Tidligere var der ingen side, hvor du kunne oprette nye kreditkorttyper, såsom Visa, MasterCard eller AMEX, som kan bruges sammen med Udgiftsstyring. Du kan nu oprette typer af kreditkort til brug sammen med Udgiftsstyring. Siden er placeret i området **Konfiguration** i sektionen **Beregninger og koder**.                                                                                                                                                                                                                                                                                                                                                 |
| Definere en arbejdsgang i flere niveauer for udgiftsrapporter.                 | En ny arbejdsgang for udgiftsrapporter understøtter en godkendelsesproces med flere niveauer. Medarbejderne angiver foreløbige godkendere og endelige godkendere, når de opretter udgiftsrapporten. Arbejdsgangen dirigerer derefter udgiftsrapporten til de foreløbige godkendere først. Når udgiftsrapporten er godkendt på dette niveau, sender arbejdsgangen den til endelig godkendelse hos de endelige godkendere.                                                                                                                                                                                                                                                                                          |
| Oprette og vedligeholde udgifter, der ikke er knyttet til en udgiftsrapport.    | Brugeren kan nu oprette udgifter og vedligeholde dem (for eksempel ved at vedhæfte eller specificere kvitteringer eller tildele gæster) uden først at oprette en udgiftsrapport. En eller flere udgifter kan vælges og føjes til en ny udgiftsrapport, så de kan sendes til godkendelse. En ny side til vedligeholdelse af udgifter er tilgængelig i **Udgiftsstyring** &gt; **Mine udgifter** &gt; **Udgifter**.                                                                                                                                                                                                                                                       |

## <a name="financial-management"></a>Økonomistyring
<table>




<thead>
<tr class="header">
<th>Hvad du kan gøre</th>
<th>Hvorfor dette er vigtigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Spore vurderinger af anlægsaktiver ved hjælp af en enkelt "bog" som koncept.</td>
<td>Tidligere blev to særskilte typer vurdering brugt til at spore anlægsaktivværdier: værdimodeller og afskrivningsmodeller. Disse to begreber er blevet flettet ind i et enkelt værdiansættelsesbegreb, der hedder bøger, i den aktuelle version. Bøger har alle funktioner i både værdimodeller og afskrivningsmodeller. For eksempel kan du deaktivere bogføring til Finans. Bøger, der ikke bogføres i Finans, bruges typisk til virksomhedens regnskabsaflæggelse. Typisk bruges bøger, der ikke bogføres i finansmodulet, til momsrapporteringen.</td>
</tr>
<tr class="even">
<td>Udføre finansårsafslutning for flere juridiske enheder.</td>
<td>For at gøre processen hurtigere ved årsafslutningen kan du nu køre den for flere juridiske enheder fra en delt årsafslutningsside. Grupper af juridiske enheder kan defineres sammen med indstillinger, der skal opbevares fra år til år. Andre forbedringer af brugervenligheden er også foretaget i forbindelse med ultimo ved årsafslutningen.</td>
</tr>
<tr class="odd">
<td>Drag fordel af forbedringer til værdiregulering af udenlandsk valuta i Finans.</td>
<td>Der er foretaget følgende forbedringer i finansprocessen til værdiregulering af udenlandsk valuta:
<ul>
<li>En valutakurstype er føjet til hovedkontoen. Denne valutakurstype bruges til at bestemme valutakursen under værdiregulering af valuta. Hvis der ikke er defineret nogen valutakurstype, fortsætter processen med at bruge den valutakurstype, der er defineret i Finans.</li>
<li>Det er nu nemmere at vælge et interval af hovedkonti og valutaer til at køre værdireguleringsprocessen.</li>
<li>Værdiregulering kan køres for flere juridiske enheder.</li>
<li>Systemet har nu en oversigt over hver værdireguleringsproces, der blev udført, som det er tilfældet for debitor- og kreditorværdireguleringsprocesser.</li>
<li>Når du kører processen, kan du nu få vist resultaterne af værdireguleringen. Eksemplet viser resultaterne for alle juridiske enheder, som processen blev kørt for. Derefter kan du bogføre de juridiske enheder, eller en delmængde af dem, fra eksemplet. Du kan også eksportere resultaterne i eksemplet til Excel.</li>
</ul></td>
</tr>
<tr class="even">
<td>Vise transaktioner for flere posteringslag.</td>
<td>På listesiden <strong>Råbalance</strong> og i rapporten <strong>Dimensionsfordeling</strong> kan du nu vælge flere posteringslag, der er føjet til Finans. Når du vælger flere posteringslag, medtages reguleringer for de posteringslag i saldi på listesiden eller rapporten.</td>
</tr>
<tr class="odd">
<td>Vedhæfte vejledende dokumentation i skabelonen for afslutning på regnskabsperiode.</td>
<td>Tidligere kunne du vedhæfte dokumentation, når en opgave var fuldført. For eksempel kunne du vedhæfte en rapport, der var genereret. Nu kan du også vedhæfte et dokument med vejledning til skabelonen. Dette dokumentet kopieres derefter til hver opgave i tidsplanen for regnskabsperioden, så opgaveansvarlige kan få vist oplysninger om, hvordan opgaven skal udføres.</td>
</tr>
<tr class="even">
<td>Definere opsætningen af mellemregning fra en delt side.</td>
<td><strong>Konfigurationssiden for mellemregning</strong> er nu delt, så en organisation kan definere alle par af juridiske enheder, der kan agere med hinanden. Desuden kan du nu indtaste en transaktion i den oprindelige juridiske enhed, men ikke fra den juridiske destinationsenhed. Hvis den ene juridiske enhed kan indlede en mellempostering, skal det reciprokke par være defineret. Derfor er den juridiske destinationsenhed også angivet som en oprindelig juridisk enhed.</td>
</tr>
<tr class="odd">
<td>Indsende berettigelsesdokumenter for budgetplaner.</td>
<td>Du kan oprette en berettigelsesskabelon som supplerende dokumentation for de anmodede budgetbeløb. Brugere kan udfylde oplysninger om skabelonen og knytte skabelonen til budgetplanen, så den kan bruges under godkendelsesprocessen.</td>
</tr>
<tr class="even">
<td>Aktivere avancerede regler for budgetregisterposter.</td>
<td>Hvis avancerede regler konfigureres i finansmodulet, kan disse regler bruges til nye poster og overførsler i budgetregisteret.</td>
</tr>
<tr class="odd">
<td>Drage fordel af forbedret synlighed for forudbetaling af faktureringsaktivitet.</td>
<td>Den nye listeside <strong>Åbne forudbetalinger</strong> giver et øjebliksbillede af status for forudbetaling af faktureringsaktivitet. Siden giver kreditorafdelingen oplysninger om de indkøbsordrer, der har resterende forudbetalingsværdier, der skal faktureres, fakturerede værdier, der skal betales, og betalte fakturaværdier, der skal anvendes på almindelige fakturaer. Desuden gør forbedringer af automatisk anvendelse af forudbetalingsfakturaer på almindelige fakturaer det nemmere for faktureringsmedarbejdere at indtaste data mere effektivt.</td>
</tr>
<tr class="even">
<td>Bruge arbejdsområdet for <strong>kreditorsamarbejdsfakturering</strong>.</td>
<td>I det nye <strong>Fakturering</strong>-arbejdsområde i området <strong>Kreditorsamarbejde</strong> har eksterne leverandører sikker adgang til deres egne fakturaoplysninger. Kreditorer kan for eksempel se, om fakturaen er betalt, og sende deres egen faktura. Denne ændring fremmer en mere effektiv og rettidig kommunikation med eksterne leverandører. Derfor har faktureringsfuldmægtige færre afbrydelser.</td>
</tr>
<tr class="odd">
<td>Skifte juridiske enheder under fakturapostering.</td>
<td>Forbedringer gør det muligt at ændre fakturaer for flere juridiske enheder hurtigt til andre juridiske enheder fra siderne til fakturering. Denne funktion kan spare tid, fordi medarbejderne ikke længere skal logge ud af den aktuelle juridiske enhed og logge på en anden juridisk enhed. På både siden <strong>Global fakturajournal</strong> og siden <strong>Kreditorfakturaer</strong> kan brugerne ændre den juridiske enhed under dataindtastning.</td>
</tr>
<tr class="even">
<td>Understøtte elektroniske filer til det interne amerikanske skattevæsens (IRS) 1099 Combined Federal/State-indberetningsprogram</td>
<td>Når den <strong>amerikanske</strong> konfigurationsnøgle er aktiveret, giver den elektroniske indsendelse af 1099-processen yderligere funktionalitet, der opfylder IRS-forordninger for det kombinerede forbunds-/delstatsprogram. IRS etablerede dette program, så det kan videresende oplysninger elektronisk til deltagende delstater.</td>
</tr>
<tr class="odd">
<td>Forbedrede udligninger</td>
<td>Forbedringer gør udligninger mere effektive, da fuldmægtige kan tillade, at flere ikke-bogførte betalinger udlignes mod den samme faktura.</td>
</tr>
<tr class="even">
<td>Visning på tværs af firmaer</td>
<td>Centrale medarbejdere kan nu se forfaldne fakturaer på tværs af firmaer. <strong>Kreditorbetalinger</strong>- og <strong>Debitorbetalinger</strong>-arbejdsområder giver nu bedre indsigt i og kontrol over forfaldne fakturaer ved hjælp af en metode til visning og filtrering på tværs af firmaer, der indgår i et organisationshierarki til centraliserede betalinger.</td>
</tr>
<tr class="odd">
<td>Bruge <strong>Bankstyring</strong>-arbejdsområdet.</td>
<td>I det nye <strong>Bankstyring</strong>-arbejdsområde får du hjælp til at holde styr på bankkonti og saldi for juridiske enheder. Nuværende og ventende saldi er umiddelbart tilgængelige for alle konti, og du kan rulle tilbage fra saldiene i de detaljerede transaktionsbilag. Du kan også se historiske saldodata for hver bankkonto eller en oversigt over alle bankkonti i firmaet i både kortsigtede og langsigtede visninger. Du kan få bedre indsigt i bankkontoafstemningen, fordi datoen for den seneste afstemning er rapporteret for hver bankkonto, og der er også en indikator for afstemninger, der er i gang.</td>
</tr>
<tr class="even">
<td>Importere elektroniske bankkontoudtog for alle juridiske enheder i et enkelt trin.</td>
<td>Nu kan du importere elektroniske bankkontoudtog for alle juridiske enheder i et enkelt trin. Bankkontoudtogsfiler kan indeholde opgørelser fra mange bankkonti og juridiske enheder, og zip-filer kan indeholde flere bankkontoudtogsfiler. Ved hjælp af en enkelt importproces kan du starte afstemningen for alle rapporterede bankkonti i alle juridiske enheder. Denne er med til at spare tid, fordi du ikke behøver at skifte mellem virksomheder og flere importer af kontoudtog. Du kan også automatisk køre matchende regler mod alle importerede kontoudtog i de enkelte firmaer.</td>
</tr>
<tr class="odd">
<td>Sporing af vurdering</td>
<td>Et enkelt anlægsaktiv kan have flere vurderinger for forskellige regnskabsstandarder og kan også bogføre de posteringer, der er knyttet, til Finans. Disse vurderinger blev tidligere registreret i værdimodeller eller afskrivningsmodeller. Nu kan du spore disse vurderinger, som nu kaldes bøger, ved hjælp af et fælles sæt af kladder, forespørgsler og rapporter. Den samlede oplevelse forenkler implementering og reducerer antallet af grænseflader, som kræves af periodiske processer.</td>
</tr>
<tr class="even">
<td>Drage fordel af forbedret kørsel af afskrivning på tværs af regnskaber.</td>
<td>Nu kan du starte en afskrivning af aktiver på tværs af alle de juridiske enheder fra en enkelt side. Du kan også automatisk bogføre kladder, når de er oprettet. Du kan sende oprettelse og bogføring af kladder til batchafvikling, så afskrivningen kører i baggrunden. Disse forbedringer øger effektiviteten, fordi du ikke behøver at starte individuelle afskrivninger separat for hvert regnskab. Udvidelsen kan også forbedre den centrale styring af anlægsaktiverne.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Styring af menneskelig kapital
| Hvad du kan gøre                                                                                | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Oprette en performancekladde.                                                                  | Før du afslutter din evaluering, indsamler du som medarbejder ofte oplysninger om aktiviteter eller hændelser, der bidrog til din succes som medarbejder i evalueringsperioden. Du kan føje en post til performancekladden for at dokumentere disse aktiviteter og hændelser. Du kan også forbinde disse aktiviteter og hændelser til et mål eller en performancegennemgang for at give yderligere oplysninger til korrekturlæseren.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Oprette mere detaljerede mål.                                                                    | Du har mere kontrol over indholdet på de mål, du har angivet. Du kan oprette målinger for mål, sammenkæde performancejournalposter til mål samt vedhæfte og få vist dokumenter. Du kan gemme mål som skabeloner og genbruge dem til hurtig konfiguration.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Oprette mere detaljeret gennemgang af performance.                                                      | Performanceevalueringer, som formelt kaldes diskussioner, er nu fleksible nok til at understøtte både løbende feedback og mere formelle evalueringer. Du kan indlæse aktive mål og bogføre kommentarer om dem og tilføje sektioner for en gennemgang af dine kompetencer. Der findes yderligere sektioner, hvor du kan tilføje eller få vist mål, performancejournalposter, vedhæftede filer og godkendelser, der er relateret til evalueringen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Knytte flere stillingshierarkier til arbejdsgange.                                      | Du kan knytte en arbejdsgang til et stillingshierarki. Du kan også ændre trinene i arbejdsgangen for at optimere godkendelsesprocessen, så den passer til virksomhedens behov. Derfor kan du definere en effektiv godkendelsesstruktur, der passer til forskellige rapporteringsrelationer, der bruges i din organisation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Arbejdsgangunderstøttelse til at indtaste personlige identifikationsnumre (pinkoder) i medarbejderselvbetjening. | Arbejdsgangmulighed for personaleforhold (HR) er blevet udvidet og omfatter nu understøttelse af pinkoder. Medarbejdere kan tilføje og redigere deres pinkode for at øge effektiviteten. Dog kan HR-medarbejdere efterse, om disse oplysninger er komplette og korrekte, før de kan føje dem til medarbejderens post.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Oprette skabeloner for målet og bruge dem til at tilføje nye mål.                                          | Du kan oprette skabeloner for mål for mål, der deles af mange medarbejdere i virksomheden. Medarbejdere kan tilføje deres egne mål fra en skabelon, ledere kan tilføje mål for deres team fra en skabelon, og HR-teammedlemmer kan tilføje mål for medarbejdere på tværs af virksomheden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Oprette målgrupper og bruge dem til at tilføje nye mål.                                             | Du kan føje målskabeloner til en gruppe og bruge gruppen til at oprette et eller flere mål for en medarbejder, et team, en stilling, en afdeling eller firmaet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Få mere kontrol over evalueringsprocessen.                                                     | Du kan bruge en arbejdsgang til at styre valideringsprocessen. Du kan oprette valideringsskabeloner og bruge dem til at oprette valideringer. Du kan også tilføje vurderinger i en validering.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Bruge evalueringsperioder til at definere tidsrum for evalueringen.                                    | Du kan definere en tidsperiode for en performanceevaluering, så start- og slutdatoer angives automatisk for evalueringen. Du kan dog ændre standarddatoer efter behov.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Få adgang til fem nye Power BI-indholdspakker til Personale                                     | De nye indholdspakker giver personaleorganisationer og personaleledere mulighed for at analysere følgende: Nøgletal om arbejdsstyrke • Demografiske opdelinger på alder, køn og civilstand • Sammenligning af frafaldsrater år for år og en liste over de årsager, medarbejdere har givet for at forlade organisationen • Visning af en liste over ledige stillinger, samt en sammenligning af åbne og besatte stillinger Kompensation og frynsegoder • Sammenligning mellem timelønnede og fastansatte medarbejdere • Visning af antallet af medarbejdere, der er tilmeldt tilgængelige frynsegoder • Visning af medarbejdere efter ansættelsestype Rekruttering • Analyse af ansøgere baseret på antallet af ansøgere, hvor de kommer fra, og hvilke stillinger de ansøger om Organisatorisk uddannelse • Kursustilmelding ved lokalitet • Kursusdeltagelse efter status • Liste over medarbejdere, der er tilmeldt kurser Medarbejderkompetencer og -udvikling • Liste over medarbejdernes færdigheder • Opdeling af færdighedstyper efter teammedlem |

## <a name="localizations"></a>Lokaliseringer
<table>




<thead>
<tr class="header">
<th>Hvad du kan gøre</th>
<th>Hvorfor dette er vigtigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Forskellige sprogversioner er tilgængelige for 18 lande:
<ul>
<li>Østrig</li>
<li>Belgien</li>
<li>Brasilien</li>
<li>Kina</li>
<li>Tjekkiet</li>
<li>Estland</li>
<li>Finland</li>
<li>Ungarn</li>
<li>Italien</li>
<li>Letland</li>
<li>Litauen</li>
<li>Norge</li>
<li>Polen</li>
<li>Saudi-Arabien</li>
<li>Spanien</li>
<li>Sverige</li>
<li>Schweiz</li>
<li>Thailand</li>
</ul>
Følgende lande kræver også detaillokalisering. Detaillokalisering for disse lande er ikke fuldført og er kun planlagt for H1 CY2017:
<ul>
<li>Brasilien</li>
<li>Tjekkiet</li>
<li>Estland</li>
<li>Ungarn</li>
<li>Letland</li>
<li>Litauen</li>
<li>Malaysia</li>
<li>Polen</li>
<li>Sverige</li>
</ul></td>
<td>Dynamics 365 for Operations er tilgængelig i 18 ekstra lande. Lovpligtige elektroniske rapporteringsfunktioner er blevet konverteret til konfigurationer af elektronisk rapportering (ER) som en del af vores bestræbelser på at gøre lokalisering lettere og mere konfigurerbar, og nogle lovpligtige rapporter til Microsoft SQL Server Reporting Services (SSRS) er blevet konverteret til ER-konfigurationer, der bruger Excel-skabeloner. Disse konverterede funktioner er nævnt specifikt senere i denne tabel.</td>
</tr>
<tr class="even">
<td>Japan – Gruppere anlægsaktiver, når du udskriver form 26 og dens vedhæftede tabeller.</td>
<td>Formen 26 skal indsendes til hver by, hvor virksomheden opererer. For at spare tid, når du udskriver form 26, kan anlægsaktiver automatisk grupperes og sorteres efter sted.</td>
</tr>
<tr class="odd">
<td>Japan – Se beløbene for accelereret og yderligere afskrivning på profilen.</td>
<td>Profilen kan give en præcis vurdering af beløbene for accelereret og yderligere afskrivning.</td>
</tr>
<tr class="even">
<td>Japan – Beregne a-skat progressivt.</td>
<td>Den japanske regering kræver, at du beregner a-skat progressivt, baseret på det betalingsbeløbet.</td>
</tr>
<tr class="odd">
<td>Japan – Importere postnummerfilen for store virksomheder i bestemte bygninger.</td>
<td>Postnummerfilen, som myndigheden giver for store virksomheder i bestemte bygninger kan importeres til systemet. Adressen kan derefter afledes af postnumre.</td>
</tr>
<tr class="even">
<td>Japan – Konfigurer en inaktiv periode for anlægsaktiver.</td>
<td>Med inaktive perioder kan brugeren afbryde afskrivning af anlægsaktiver i en bestemt periode. Denne funktion kræves af lovgivningen.</td>
</tr>
<tr class="odd">
<td>Europa – Konfigurere et momsregistreringsnummer for en parts adresse ved hjælp af registrerings-id-struktur.</td>
<td>Du kan konfigurere et momsregistreringsnummer for en parts adresse ved hjælp af registrerings-id-strukturen og en ny <strong>Moms-id</strong>-registreringskategori.</td>
</tr>
<tr class="even">
<td>Finland – Konfigurere et tolddebitornummer for en parts adresse ved hjælp af registrerings-id-strukturen.</td>
<td>Du kan konfigurere et tolddebitornummer for en parts adresse ved hjælp af registrerings-id-strukturen og den nye <strong>Toldmyndighedens debitor-id</strong>-registreringskategori.</td>
</tr>
<tr class="odd">
<td>Frankrig – Udskrive debitorfakturaer i et layout, der er specifikt for Frankrig.</td>
<td>Udskrift af debitorfaktura justeres i forhold til behov, der er specifikke for Frankrig.</td>
</tr>
<tr class="even">
<td>Frankrin – Gennemtvinge kronologisk nummerering af dokumenter efter regnskabsperiode.</td>
<td>For at opfylde krav, der er specifikke for Frankrig, til nummerering af debitorfakturaer, er det muligt at konfigurere nummerserier for debitorfakturaer pr. regnskabsperiode.</td>
</tr>
<tr class="odd">
<td>Østrig-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>EU-listesystem - XML-format for Østrig</li>
<li>Intrastat-format for Østrig</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Østrig</li>
<li>ISO20022 Direct Debit-betalingsformat for Østrig</li>
<li>Østrisk EDIFACT-PAYMUL-format</li>
<li>Momsopgørelse for Østrig</li>
</ul></td>
</tr>
<tr class="even">
<td>Belgien-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>BLWI-format for Belgien</li>
<li>EU-listesystem - XML-format for Belgien</li>
<li>Anlægsaktivrapport for Belgien</li>
<li>Intervat-format for Belgien</li>
<li>Intrastat-format for Belgien</li>
<li>Fakturaomsætningsrapport for Belgien</li>
<li>Eksportformat til finanstransaktion for Belgien</li>
<li>SWIFT kreditorbetalingsformat for Belgien</li>
<li>Importformat til CODA-bankkontoudtog for Belgien</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Belgien</li>
<li>ISO20022 Direct Debit-betalingsformat for Belgien</li>
</ul></td>
</tr>
<tr class="odd">
<td>Brasilien-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>GIA SP for Brasilien</li>
<li>GIA ST for Brasilien</li>
</ul></td>
</tr>
<tr class="even">
<td>Tjekkiet-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>EU-listesystem - XML-format for Tjekkiet.</li>
<li>Intrastat-format for Tjekkiet</li>
<li>Momsopgørelse for Tjekkiet</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kina-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>Aldersfordelt kunderapportformat for Kina</li>
<li>Analyserapportformat til kundens skyldige beløb for Kina</li>
<li>Aldersfordelt saldoliste for kreditorer for Kina</li>
<li>Analyserapportformat til kreditors skyldige beløb for Kina</li>
<li>Aldersfordelingsanalyse af debitorbetalingsformat for Kina</li>
<li>Rapportformat til debitorsaldo for Kina</li>
<li>Saldorapportformat til finanskonto for Kina</li>
<li>Rapportformat til kreditorsaldo for Kina</li>
<li>GBT-fil for Kina</li>
<li>Format for Golden Tax-eksportfil</li>
<li>Variansrapportformat til produktionsforbrug for Kina</li>
</ul></td>
</tr>
<tr class="even">
<td>Estland-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>EU-listesystem - XML-format for Estland</li>
<li>Intrastat-format for Estland</li>
<li>Lageromklassificeringsopgørelse for Estland</li>
<li> ISO20022-kreditoverførsel som betalingsformat for Estland</li>
<li>Meddelelsesrapport til debitor-/kreditorsaldo for Estland</li>
<li>Momsopgørelse for Estland</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finland-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>EU-listesystem, TXT-format for Finland</li>
<li>Intrastat-format for Finland</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Finland</li>
</ul></td>
</tr>
<tr class="even">
<td>Ungarn-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>EU-listesystem - XML-format for Ungarn</li>
<li>Intrastat-format for Ungarn</li>
<li>Intrastat-forenklet format til Ungarn</li>
<li>Eksportformat for fakturaliste til Ungarn</li>
<li>Momsopgørelse for Ungarn</li>
<li>Specificeret momsopgørelse for Ungarn</li>
<li>Lageropgørelse for Ungarn</li>
<li>MultiCash-betalingsformat for Ungarn</li>
</ul></td>
</tr>
<tr class="odd">
<td>Italien-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>Intrastat-format for Italien</li>
<li>Projektfakturaformat for Italien</li>
<li>Salgsfakturaformat for Italien</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Italien</li>
<li>ISO20022 Direct Debit-betalingsformat for Italien</li>
<li>RIBA-rykkerremitteringsformat for Italien</li>
<li>Rapport over indenlandsk momstransaktion for Italien</li>
<li>Sortlistningsrapport for Italien</li>
<li>Modello770-rapport for Italien</li>
<li>Rapport om årlig momsindberetning for Italien</li>
</ul></td>
</tr>
<tr class="even">
<td>Letland-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>Rapport over brugen af kasseboner (LV)</li>
<li>EU-listesystem, XML-format for Letland</li>
<li>EU-listesystemrettelser, XML-format for Letland</li>
<li>Intrastat-format (A) for Letland</li>
<li>Intrastat-format (B) for Letland</li>
<li>Lageroptællingsliste for Letland</li>
<li>Lageroptællingsopgørelse for Letland</li>
<li>Flytning af lager for Letland</li>
<li>Følgeseddel til intern overførsel for Letland</li>
<li>Lagergenklassificeringsdokument for Letland</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Letland</li>
<li>Momsopgørelse for Letland</li>
</ul></td>
</tr>
<tr class="odd">
<td>Litauen-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>EU-listesystem - XML-format for Litauen</li>
<li>Intrastat-format for Litauen</li>
<li>Lageropgørelse for Litauen</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Litauen</li>
<li>Rapport over intern afstemning af debitor/kreditor for Litauen</li>
<li>Momsopgørelse for Litauen</li>
</ul></td>
</tr>
<tr class="even">
<td>Norge-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>Rykkerbrevsformat for Norge</li>
<li>AutoGiro-betalingsformat for Norge</li>
<li>AvtaleGiro-kundebetalingsformat for Norge</li>
<li>eFaktura-kundebetalingsformat for Norge</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Norge</li>
<li>NETS-betalingsformat for Norge</li>
</ul></td>
</tr>
<tr class="odd">
<td>Polen-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>Intrastat-format for Polen</li>
<li>Lagerdokumenter for Polen</li>
<li>Lagergenklassificeringsdokument for Polen</li>
<li>MultiCash-betalingsformat for Polen</li>
<li>Udenlandsk MultiCash-betalingsformat for Polen</li>
<li>Bekræftelsesrapport til debitor-/kreditorsaldo for Polen</li>
</ul></td>
</tr>
<tr class="even">
<td>Saudi-Arabien-lokalisering – ER-konfigurationer</td>
<td>Bank LC diverse Gebyrfordelingsformat for Saudi-Arabien</td>
</tr>
<tr class="odd">
<td>Spanien-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>EU-listesystem, TXT-format for Spanien</li>
<li>Intrastat-format for Spanien</li>
<li>Projektfakturaformat for Spanien</li>
<li>Salgsfakturaformat for Spanien</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Spanien</li>
<li>ISO20022 Direct Debit-betalingsformat for Spanien</li>
<li>Spansk momsregistreringsformat</li>
<li>Oversigtsformat i spansk momsregistreringsbog</li>
<li>Rapport 347-eksport til ASCII for Spanien</li>
<li>Rapport 347 for Spanien</li>
</ul></td>
</tr>
<tr class="even">
<td>Sverige-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>Intrastat-format for Sverige</li>
<li>Bankgirot Autogiro-kundebetalingsformat for Sverige</li>
<li>Bankgirot-kreditorbetalingsformat for Sverige</li>
<li>SWIFT-kreditorbetalingsformat for Sverige</li>
<li>SIE-eksportformat for Sverige</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Sverige</li>
</ul></td>
</tr>
<tr class="odd">
<td>Schweiz-lokalisering – ER-konfigurationer</td>
<td><ul>
<li>DebitDirect-betalingsformat for Schweiz</li>
<li>LSV Direct Debit-betalingsformat for Schweiz</li>
<li>ISO20022-kreditoverførsel som betalingsformat for Schweiz</li>
<li>ISO20022 Direct Debit-betalingsformat for Schweiz</li>
<li>Importformat til ESR-bankkontoudtog for Schweiz</li>
</ul></td>
</tr>
<tr class="even">
<td>Tyskland – Eksportér kreditorbetalinger i DTAZV-format</td>
<td>Tyskland kræver behandling af DTAZV med fremmede formatangivelse, som repræsenterer en kreditoverførselsmeddelelse (kreditorbetaling) i overensstemmelse med specifikationen for betalinger på tværs af landegrænsen fra Tyskland til en konto i en udenlandsk bank eller til en indenlandsk bank i fremmed valuta. 
</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Elektronisk rapportering

| Hvad du kan gøre                                                                                                                                                                                                                                                                                     | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurere ER-rapporter til at indsætte data i flere formater, fra dokumentstyringslager til elektroniske meddelelser, der genereres.                                                                                                                                                              | ER-rapporter kan indsætte data i elektroniske meddelelser, der genereres fra dokumentstyringslageret. Derfor kan vedhæftede filer i et forretningsdokument føjes til elektroniske meddelelser, der er oprettet for det pågældende dokument i overensstemmelse med juridiske krav. Disse vedhæftede filer kan i øjeblikket tilføjes i MIME-format til en XML-meddelelse, der genereres. De vedhæftede filer kan i stedet tilføjes i Base64-format til en binær meddelelse, der genereres.                                                                      |
| Konfigurere ER-rapporter til at generere elektroniske dokumenter i Excel-, Microsoft Word- eller PDF-format.                                                                                                                                                                                                      | Med én konfiguration kan ER-rapporter generere elektroniske dokumenter i tre forskellige formater: OpenXML-regneark (Excel), Word- og XML-formulardataformat (XFDF) (PDF). Brugerne kan vælge et format ved at tilføje en formatskabelon i en ER-rapport som et Excel-, Word- eller PDF-dokument.                                                                                                                                                                                                                                                                       |
| Konfigurere ER-rapporter til at indsætte data i sidehoveder og sidefødder af elektroniske dokumenter, der genereres i regnearksformatet OpenXML, og styre sideskift.                                                                                                                               | ER-rapporter kan angive forretningsdata i sidehoveder og sidefødder og også styre, hvor der indsættes sideskift. Rapporterne kan derfor understøtte statiske øverste og nederste afsnit for sider af elektroniske dokumenter, der genereres. De kan også understøtte bestemt sideopdeling af dokumenterne, så de er i overensstemmelse med lovgivningsmæssige krav.                                                                                                                                                                                                             |
| Konfigurere destinationen for ER-rapporter, så output sendes som mail, og virksomhedens data og ER-logik (udtryk) kan bruges til at angive mailadressen, der skal bruges på kørselstidspunktet.                                                                                                    | Tidligere, når du har konfigureret en ER-destination, kunne outputmodtageren af mailadressen defineres i designfasen. Du kan nu konfigurere et udtryk i ER-formatet. Dette udtryk kan derefter vælges i en destination som kilden til mailadressen for hver formatkonfiguration og hver outputkomponent (mappe eller fil) separat. Derfor, når en ER-rapport kører, kan hver fil, der oprettes, blive sendt til en anden modtager, og mailadressen kan defineres ud fra ER-logik og forretningsdata. |
| Konfigurere destinationen for ER-rapporter, så output sendes til Microsoft SharePoint-mappen som enten en ny navngivet fil eller en ny version af den eksisterende fil, så forretningsdata kan bruges i Microsoft Power BI-strukturen som enten et datasæt eller en rapport.                 | Når du konfigurerer ER-rapporter, kan du nu nemt (uden kodning) forberede de anmodede forretningsdata, så de kan bruges af Power BI-strukturen. Når du kører disse ER-rapporter, kan du give Power BI-strukturen relevante forretningsdata og/eller Excel-rapporter, der allerede er tilgængelige. Hvis du planlægger, at rapporten køres i tilbagevendende tilstand, kan du oprette planlagt aktivering af forretnings data fra Dynamics 365 for Operations til Power BI for at understøtte tidsplanen for opdatering af Power BI-baserede rapporter.                             |
| Konfigurere ER-rapporter til at bruge den del af det elektroniske dokument, der allerede er oprettet som en datakilde, for at generere resten af dokumentet.                                                                                                                                             | Du kan konfigurere ER-rapporter, som opretter output i tekstformat til dokumentets linjeoptælling. Disse oplysninger kan derefter bruges i andre dele af dokumentet til at oprette linjer, der indeholder en oversigt over detaljerne. De kortfattede oplysninger (totaler og tal) kan beregnes og udskrives på de elektroniske dokumenter, der oprettes, uden at kræve yderligere transformationer af data. Derfor forbedrer denne funktion ydeevnen for udførelsen af rapporter og hjælper med at lette fremtidig vedligeholdelse af det konfigurerede ER-format.    |
| Konfigurere ER-rapporter til at angive filtypenavnet for elektroniske dokumenter, der genereres i tekstformat.                                                                                                                                                                                 | Du kan konfigurere ER-rapporter til at oprette output i tekstformat, så de kan gemmes som en fil med et bestemt filtypenavn. Du kan konfigurere udvidelser såsom .csv og .prn efter formatspecifikationen ud over standardfiltypenavnet .txt.                                                                                                                                                                                                                                                                             |
| Oprette nye ER-rapporter, der er baseret på en bestemt version af en ER-model.                                                                                                                                                                                                                          | Når du har oprettet et nyt ER-format, kunne der tidligere kun anvendes den nyeste version af den valgte ER-model som formatets datakildeplacering. Nu kan du vælge enhver tilgængelig version af den valgte ER-model. Med denne funktion kan du vedligeholde ER-rapporterne for indeværende år og designe en ny version af ER-modellen for næste år parallelt.                                                                                                                                                                                          |
| Søge i datakilder og formater/modeller efter tekst eller udvalgt artefakt med et enkelt klik. Proaktivt løse rebaseringskonflikter og løse konflikter mellem konfigurationer. Konfigurere ER-rapporter til at oprette flere valideringsmeddelelser for fejl, der opdages, før kørsel af rapporten er stoppet. | Flere forbedringer af brugeroplevelsen i ER-strukturen hjælper brugerne med at arbejde med ER effektivt og hurtigt.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Vise arbejdsområdet **ER** på Power BI-rapporter.                                                                                                                                                                                                                                                      | Brugerne kan konfigurere siden **ER-arbejdsområde**, så den omfatter nye menupunkter og dynamiske felter, der kører Power BI-baserede-rapporter.                                                                                                                                                                                                                                                                                                                                                                                                                       |

## <a name="payroll"></a>Løn
<table>




<thead>
<tr class="header">
<th>Hvad du kan gøre</th>
<th>Hvorfor dette er vigtigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Konfigurere betalingsposter og behandle løn ved hjælp af funktioner, der svarer til funktionerne i <strong>Løn</strong>-modulet i Microsoft Dynamics AX 2012 R3.</td>
<td>Du kan nu konfigurere og behandle amerikansk løn ved hjælp af et sæt af funktioner, der svarer til den funktion, der er angivet i AX 2012 R3.
<ul>
<li>Du kan konfigurere løncyklusser og lønperioder, arbejdscyklusser og arbejdsperioder, lønkoder og lønkodegrupper, tidsplaner, orlovstyper og planer for periodisering af frynsegoder.</li>
<li>Du kan også oprette obligatoriske fradrag for både frynsegoder og skatter og registrere lønoplysninger for stillinger og arbejdere med henblik på rapportering og analyse.</li>
<li>Du kan også oprette og administrere fradrag for udlæg i udestående fordringer og afgifter samt eventuelle tilknyttede administrationsgebyrer.</li>
</ul></td>
</tr>
<tr class="even">
<td>Overvåge og behandle din lønperiodeproces ved hjælp af det nye <strong>Lønadministration-</strong>arbejdsområde.</td>
<td>Nu kan du nemt overvåge din lønudbetaling. Lønadministratorer kan hurtigt se optjenings- og lønopgørelser, der kræver deres opmærksomhed, så lønkørsel bliver fuldstændig og nøjagtig. I arbejdsområdet <strong>Lønadministration </strong>kan brugerne overvåge og køre komplette processer fra et enkelt arbejdsområde.</td>
</tr>
<tr class="odd">
<td>Generere positive lønfiler for løncheck.</td>
<td>Der er en ny udvidelse af Kontant- og bankstyrings positive lønfunktion til lønbetalinger. Separate menupunkter er blevet tilføjet i hele kerneprocessen for at aktivere isoleret konfiguration, der er specifik for løn. Funktionaliteten er identisk med kernefunktionen til positiv løn, der blev udgivet i Microsoft Dynamics AX programversion 7.0.1 (maj 2016). På grund af denne udvidelse er løndata fuldstændigt isoleret fra resten af dine positive lønposteringer. Denne isolation hjælper med at sikre, at kun lønbrugere kan få adgang til at se data, der er relateret til løn.</td>
</tr>
<tr class="even">
<td>Importere lønopgørelseslinjerne fra en ekstern kilde ved hjælp af den nye dataenhed Post på lønopgørelsen.</td>
<td>En vigtig ny dataenhed muliggør integration med eksterne tids- og lønberegningssystemer. Dataenheden importerer lønopgørelseslinjer og udfører hele den samme standardlogik, som brugeren har indtastet direkte på lønopgørelsen. Efter importen er linjerne automatisk knyttet til det rette lønopgørelsesdokument. Hvis der ikke findes et passende lønopgørelsesdokument, oprettes der automatisk et dokument.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Planlægning
| Hvad du kan gøre                                                                                                                                                                                                      | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Angive standardordreindstillinger for køb og salg, baseret på en aktiv produktdimension i produktmasteren. Derfor kan du definere standardordreindstillingerne for lagerenheden (SKU) eller en delvis SKU. | Du kan angive standardordreindstillinger for en produktdimension eller en kombination af produktdimensioner. **Eksempel** Du sælger et produkt, der hedder Polo T-shirt. Dette produkt fås i to farver: grøn og blå. Det fås også i to størrelser: small og medium. Aktive produktdimensioner til Polo T-shirt er farve og størrelse. Du kan blokere køb af alle grønne Polo-T-shirts, uanset deres størrelse. |

## <a name="product-master-data"></a>Produktmasterdata
<table>




<thead>
<tr class="header">
<th>Hvad du kan gøre</th>
<th>Hvorfor dette er vigtigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Konfigurere alle standardindstillinger for ordre og lokationsspecifikke ordreindstillinger på samme tid, fra én side.</td>
<td>Denne funktion giver et bedre overblik over vareindstillinger.</td>
</tr>
<tr class="even">
<td>Oprette en nomenklatur for produktvariantnumre.</td>
<td>Du kan medtage elementer som produktdimensioner, attributter og tegn i dine produktvariantnumre. Du kan hurtigt finde en bestemt produktvariant, når du opretter en salgsordre eller indkøbsordre.</td>
</tr>
<tr class="odd">
<td>Søge efter produkter og produktvarianter i salgs- og købsscenarier.</td>
<td>Når du opretter en salgslinje eller en indkøbslinje, kan du søge efter produkter ved hjælp af produktdimensioner og alle produktnumre undtagen varenumre til globale handel (GTIN) og stregkoder. Denne søgning er en fuldtekstsøgning, der erstatter den eksisterende "Begynder med"-søgning, der bruges i opslagslisten for salg og køb. Denne funktion kan finde grupper af produkter, som har lignende egenskaber, eller et enkelt produkt, der har unikke egenskaber. Du kan aktivere denne funktion ved at vælge <strong>Aktivér opslag for produktsøgning</strong>-parameteren på siden <strong>Søgeparametre</strong>.</td>
</tr>
<tr class="even">
<td>Angive produktvarianten direkte, når du opretter en salgs- eller købstransaktion. Du kan også vælge den på en liste over gyldige dimensionskombinationer.</td>
<td>Denne funktion er en forbedring af produktiviteten. <strong>Eksempel</strong> Du sælger et produkt, der hedder Polo T-shirt. Dette produkt fås i to farver: grøn og blå. Det fås også i to størrelser: small og medium. Aktive produktdimensioner til Polo T-shirt er farve og størrelse. Når du angiver en salgslinje for Polo T-shirt med grøn farve og størrelsen Small, behøver du ikke at indtaste data i felterne <strong>Varenummer,</strong>, <strong>Farve</strong> og <strong>Størrelse</strong>. Du kan oprette linjen ved at følge ét af disse trin:
<ul>
<li>I feltet <strong>Varenummer</strong> skal du angive produktvariantnummeret, værdien af en farve eller størrelsen. I opslaget skal du finde den specifikke variant, som du vil sælge, og oprette salgslinjen.</li>
<li>Angiv et varenummer i feltet <strong>Varenummer</strong>. Gå til et hvilket som helst produktdimensionsfelt. I <strong>Produktdimension</strong>-opslaget kan du se alle de frigivne dimensionskombinationer, der gælder for Polo T-shirt. Du kan vælge den produktvariant, som du vil sælge, i ét trin.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Angive, om produktnumre vises på transaktionssider.</td>
<td>Transaktionssider som salgsordrer og indkøbsordrer viser kun felterne <strong>Varenummer</strong> og <strong>Produktnavn</strong>. Du kan se feltet <strong>Produktnummer</strong> ved at vælge <strong>Vis produktnumre på formularer</strong>-parameteren under <strong>Parametre for administration af produktoplysninger</strong>.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Projektstyring og regnskab
| Hvad du kan gøre                                                                                                           | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bruge senere valg, når du bogfører fakturaforslag i en batch.                                                            | Projektrevisorer kan konfigurere et batchjob til automatisk at opsamle fakturaforslag til bogføring, hvis disse forslag opfylder de kriterier, der er angivet i batchjobbet. Denne funktion forbedrer automatiseringen af bogføring af faktura, da batchjobbet kan køre kontinuerligt og automatisk opsamler forslag til bogføring. |
| Oprette analyser i Power BI Desktop.                                                                                     | Business intelligence (BI) indhold til projektrelaterede og ressourcerelaterede data kan oprettes let i Power BI Desktop.                                                                                                                                                                                                       |
| Bruge forudbetalinger af købsordre og inkludere dem korrekt i projektestimatprocessen.                               | For projektindkøbsordrer skal forudbetalinger behandles, inden en betaling kan frigives til kreditorer. Disse forudbetalingsfakturaer vises nu i projektestimat-/anerkendelsesprocessen for projekter af typen **Fast pris**.                                                                                           |
| Få adgang til og administrere omkostnings- og indtægtsestimater og varebehov direkte fra en opgave i arbejdsopgavehierarkiet. | Du kan administrere omkostningsestimater, indtægtsestimater og varebehov for et bestemt WBS-opgave i dialogboksen med oplysninger for opgaven i WBS-planlægnings-visning.                                                                                                                                                                 |
| Vælge en finansieringskilde på gebyrkladder.                                                                                    | Hvis kontrakten for et projekt indeholder flere finansieringskilder, kan du vælge en bestemt finansieringskilde, når gebyrerne bogføres. Hvis du ikke vælger en bestemt finansieringskilde, bruges de finansieringsregler, der er angivet i kontrakten, til at tildele gebyret.                                                                   |
| Åbne projektopgørelser i Excel.                                                                                         | Nye dataenheder for finansopdateringer og budgetopdateringer kan åbne projektopgørelsesdata i Microsoft Excel og oprette analyser ved hjælp af funktionerne i Excel.                                                                                                                                                                           |
| Bruge kun én konfigurationsnøgle til at aktivere funktioner til projektstyring og regnskab (PMA).                       | Projektrelaterede konfigurationsnøgler er blevet erstattet af én projektkonfigurationsnøgle, der aktiverer PMA-funktionalitet.                                                                                                                                                                                                       |

## <a name="retail-and-commerce"></a>Detail og handel
### <a name="advanced-warehouse-management-in-a-retail-store"></a>Avanceret lokationsstyring i en detailbutik

Detailhandlere kan bruge den avancerede lokationsstyring som løsning i deres butikker og foretage de nødvendige opdateringer til de POS-funktioner for at understøtte den. Processer af den håndholdte løsning skulle fungere i en butik, som de gør på andre lagersteder. Alle aktuelle processer for Retail butikslagerstyring og eventuelle POS-processer, der opretter eller opdaterer lagerposteringer, opdateres, så de bruger de særlige krav til WHS-kompatible lagersteder.

| Hvad du kan gøre                                                                       | Hvorfor dette er vigtigt                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bruge POS til at søge efter disponibel beholdning i WHS-kompatible lagre.                     | Når du slår op i lager, bør processen fungere på samme måde som før. Opslaget bør viser det disponible antal på lagerstedsniveau og ikke tage højre for lokation, lagerstatus eller dimensioner for id-nummer. |
| Bruge POS til at behandle en produktkvittering for en overflytningsordre i et WHS-baseret lager. | Du kan modtage flytteordrer på POS for WHS-aktiverede butikker og varer. Brugeren skal kunne vælge de lokationer, hvor der modtages, og bør være i stand til at angive id-numre til automatisk at udfylde tilgangslinjerne.    |
| Bruge POS til at behandle en produktkvittering for en købsordre i et WHS-baseret lager. | Du kan modtage købsordrer på POS for WHS-aktiverede butikker og varer. Brugeren skal kunne vælge de lokationer, hvor der modtages, og bør være i stand til at angive id-numre til automatisk at udfylde tilgangslinjerne.    |
| Bruge POS til at behandle en forsendelse af varer fra et WHS-aktiveret lager.               | Du kan registrere overførsler fra POS for WHS-aktiverede butikker og varer. Brugeren skal kunne vælge de lokationer, der skal leveres fra, lagerstatus skal genereres automatisk, og id-numre skal ignoreres.         |

### <a name="enable-seamless-omni-channel-commerce"></a>Aktivere problemfri handel via alle kanaler

Problemfri handel via alle kanaler er administration og ordrebehandling på tværs af fysiske butikker, online udstillingsvinduer, call centre og mobile handelsoplevelser. I denne version er der foretaget følgende investeringer på dette område:

-   Forbedringer til udgivelsen af e‑handels udstillingsvinduer
-   En ny forbrugerrettet mobilapp, der giver mulighed for opdagelse af produktet, kontoadministration og online indkøb

| Hvad du kan gøre                                                                                                                                                                                                                                                                   | Hvorfor dette er vigtigt                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Forbruger: Den aktuelle udgave af forbrugernes app har følgende funktioner: produktsøgning, kategorisøgning, Føj til indkøbsvogn og gæstekasse. Detailhandlere kan også anvende deres firmas branding på appen og derefter pakke den til Android- og iOS-appbutikker. | Detailhandlere kan nemt oprette en forbrugerapp, der giver kunderne mulighed for at ose, søge efter produkter og få leveret produkter som gæst fra deres mobilenheder.                      |
| Kundens ønskeliste til c‑handels online udstillingsvinduer                                                                                                                                                                                                                             | Uafhængige softwareleverandører (ISV'er) kan bruge kontrolelementet ønskeliste, så brugerne kan oprette og administrere flere lister i deres online udstillingsvindue og vise/bruge disse lister i POS. |
| Asynkron kundeoprettelse via e-handels online udstillingsvinduer                                                                                                                                                                                                                  | Softwareproducenter kan nu oprette debitorkonti, selvom Commerce Data Exchange: Real-time Service ikke er tilgængelig.                                                                        |
| Udgive kanalprodukter fra detailserver til tredjeparts udstillingsvinduer.                                                                                                                                                                                                           | Detailserver understøtter nu service til service-godkendelse. Softwareproducenter kan drage fordel af kanalproduktudgivelse fra detailserver til tredjeparts udstillingsvinduer.               |

### <a name="extensibility"></a>Udvidelsesmuligheder

-   Commerce Runtime-projekter er nu forseglet fra Retail SDK.
-   Nemmere implementering og servicering gennem komponentinddelte Microsoft-komponentpakker og ISV-pakker for POS, detailserver, databaser, betalings- og hardwarestationer.

| Hvad du kan gøre                                                                                                                 | Hvorfor dette er vigtigt                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CRT/Detailserver: Detailhandlere eller softwareproducenter kan udvide CRT gennem udvidelseskroge. Indbyggede kodeændringer understøttes ikke længere. | For at aktivere løbende integration og implementering bør indbyggede kodeændringer helt undgås. Desuden for at understøtte nem optagelse af hotfix uden kodefletning og installation af CRT-komponenter. |

### <a name="personalized-product-recommendations"></a>Tilpassede produktanbefalinger

| Hvad du kan gøre                                                                                                                                                                                                                                                                        | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Se tilpassede produktanbefalinger på flere kontaktpunkter på POS for at afgøre, hvad en kunde kan være interesseret i baseret på vedkommendes købshistorik, varer på deres ønskeseddel og varer, som andre kunder har købt online og i fysiske butikker | For detailhandlere med store kataloger hjælper tilpassede anbefalinger kunden med opdagelse af produkter, og giver butiksmedarbejderne adgang til intelligent clienteling. Gennem fremvisning af produkter, der er målrettet mod en kundes interesser og købsvaner, kan produktanbefalinger hjælpe detailhandlere med mersalg, og de kan forbedre fastholdelsen af kunderne. I Microsoft Dynamics 365 for Retail er produktanbefalinger understøttet af Cognitive Services og Microsoft Azure Machine Learning. |

### <a name="pos-task-recorder"></a>POS-arbejdsrutineoptager

| Hvad du kan gøre                                                                                                                                                                                                  | Hvorfor dette er vigtigt                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Forhandlere kan bruge POS-arbejdsrutineoptager til at producere undervisningsmateriale, BPM-diagrammer (Forretningsmodeldesigner), og generere indhold i Hjælp for at forbedre produktiviteten og opnå bedre analyse og design af programmer. | For at aktivere løbende integration og implementering bør indbyggede ændringer helt undgås. Desuden for at understøtte nem optagelse af hotfix uden kodefletning og installation af CRT-komponenter. |
| POS-hjælp i realtid.                                                                                                                                                                                           | Kasseassistent/chef kan få hjælp i realtid fra POS på forretningsproces uden at skifte kontekst.                                                                                                           |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Butikssystem: give en problemfri lokal butikoplevelse

Butikssystem er et installationsvalg for detailhandlere, der hjælper med at drive et sæt butikshandlinger, enten i en lokal butik, offentlig Microsoft-sky eller kundens egen private sky. I denne version er omfanget kun internt. For at give bedre understøttelse af miljøer, der har langsom og upålidelig netværksforbindelse, skal vi give detailhandlere mulighed for at implementere kanaldatabasen og detailserveren i butikken. De kan derefter fortsætte med at køre deres kerneforretningsscenarier, selv når der ingen forbindelse er til hovedkvarteret (HK). Baseret på de forskellige datapunkter, som omfatter tekniske teamdiskussioner, kundeundersøgelsesresultater og konkurrentanalyse, har vi identificeret følgende løsningsomfang som ideelt for vores målkunder:

-   En selvbetjeningspakke er tilgængelig for butikssystem.
-   Standardinstallationen er en installation med én boks, men brugerdefineret installation er tilladt.
-   Nem installation/selvbetjening.
-   Detailserver og butikkens database er i butikken, sammen med tjenesten Async Client.
-   Detailserver i butikken kommunikerer direkte med AOS i HK for butikssystemet.
-   Understøtte tværgående terminalscenarier, hvor der er ingen forbindelse til HK.
-   Retail Modern POS og Cloud POS kommunikerer altid med detailserver i butikken.
-   Understøtte Retail Modern POS og Cloud POS hvor der er ingen forbindelse til HK.
-   Understøtte en Retail Modern POS-specifik offlinedatabase (isoleret til hver forekomst af Retail Modern POS), hvor der er ingen forbindelse til HK.
-   Godkendelse er kun baseret på service-til-service for butikssystem.
-   Realtidsserviceopkald understøttes ikke, hvis der er ingen forbindelse til internettet.
-   Direkte databasetilslutning af Retail Modern POS til kanaldatabase understøttes ikke.
-   Aktivere telemetri/overvågning.

| Hvad du kan gøre                                                                                                                                       | Hvorfor dette er vigtigt                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| En detailhandler downloader butikssystemets selvbetjente installationsprogram fra siden med kanaldatabasen i Dynamics AX HQ og downloader konfigurationsfilen.   | Forhandleren kan uden problemer downloade selvbetjeningspakken.                                          |
| En detailhandler installerer butikssystem ved hjælp af installationsprogrammet med selvbetjening.                                                                                 | Detailhandler kan installere butikssystem ved hjælp af selvbetjeningspakken.                                |
| IT-chefen konfigurerer butikssystemet i Dynamics 365 for Operations (kanaldatabase, kanalprofil, butik og installerbar pakke).             | IT-chefen kan konfigurere butikssystemet nemt og effektivt.                                       |
| En detailhandler betjener Retail Modern POS i den lokale butik og foretager handlinger i realtid såsom udstedelse af gavekort, når der er forbindelse. | Forhandleren kan udføre handlinger i realtid fra butikssystemet, når der er forbindelse.                |
| En forhandler kan synkronisere data fra det lokale butikssystem til hovedkvarteret, når der er forbindelse.                                                      | Forhandleren kan synkronisere til og fra butikssystemet, når der er forbindelse.                              |
| En forhandler kan have sikker kommunikation mellem det lokale butikssystem og hovedkvarteret.                                                                 | Forhandleren kan kommunikere sikkert fra butikssystemet, når der er forbindelse.                     |
| IT-chefen og Microsoft Operations kan overvåge og rapportere på det lokale butikssystem (diagnosticering og rapportering af ændringer).                   | IT-chefen og Microsoft Operations kan overvåge butikssystemet sikkert og foretage fejlfinding effektivt. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>Universel Windows-platformsapp til Retail Modern POS

Retail Modern POS er i øjeblikket kun tilgængelig som et Windows 8.1-program til stationære computere og tablets og som Cloud POS til pc- eller tabletbrowsere. I denne version bliver Retail Modern POS konverteret til en universel Windows-platformsapp (UWP). Denne ændring gør det muligt for Retail Modern POS at køre på alle Windows 10-enheder (pc, tablet eller telefon) og endda skifte mellem visninger for Continuum-aktiverede enheder.

| Hvad du kan gøre                                                   | Hvorfor dette er vigtigt                                                                                     |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Aktivere vigtig POS-funktionalitet for enheder med lille formfaktor. | Detail POS-funktionalitet er tilgængelig for telefoner og andre enheder med lille formfaktor, der kører Windows 10. |

## <a name="supply-chain-management"></a>Supply Chain Management
### <a name="consignment-inventory"></a>Konsignationslager

| Hvad du kan gøre                                                                                                                                                                | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Som leverandør kan du gemme råvarer på kundens lagersted. Som kunde kan du udskyde det faktiske køb, indtil råvarerne skal bruges til produktion. | En lagerbeholdning af råvarer kan medføre alvorlige omkostninger. Ved hjælp af konsignationslager kan en leverandør opbevare råvarer på kundens lagersted. Kunden kan derefter udskyde det faktiske køb, indtil råvarerne skal bruges til produktion. Råvarer bestilles og modtages ved hjælp af en genopfyldningsordre til konsignation. Denne genopfyldningsordre registrerer fysiske transaktioner, men påvirker ikke finansmodulet. Hvis du vil skelne mellem kundeejede lagervarer og leverandørejede lagervarer, kan du bruge dimensionen Lagerejer. Ændringen af ejerskabet til lageret håndteres af en journalproces, der håndterer overdragelse af ejendomsretten til råvarer fra det lager, der ejes af leverandøren, til det lager, der ejes af kunden. Denne proces udløser en oprettelse af en indkøbsordre og en produktkvittering. **Bemærk:** Denne funktion er begrænset til indgående konsignation af råvarer til produktion. Den er ikke integreret med Lokationsstyring (WHS) og Transportstyring (TMS). |
| Som leverandør kan du få oplysninger om mængden konsignationslager, der er overført til kunden.                                                                      | Når en kunde skal faktureres, skal leverandøren bruge oplysninger om de råvarer, der blev købt fra konsignationslager, og købsdatoen. Leverandøren kan også overvåge den disponible lagerbeholdning hos kunden ved hjælp af grænsefladen for leverandørsamarbejde.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Flytte leverandørejet lager ved hjælp af en overførselskladde.                                                                                                                       | For at spore den fysiske placering af det lager, der ejes af leverandøren, skal du kunne registrere placeringen i systemet. Med en overførselskladde kan du registrere fysisk flytning af lageret, f.eks bevægelser fra én lokation i et lagersted til en anden lokation i det pågældende lagersted.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Justere leverandørejet lager ved hjælp af en optællingskladde.                                                                                                                     | Det er vigtigt, at du holder systemets disponible lagerbeholdning synkroniseret med det faktiske fysiske lager. Det lager, der ejes af leverandøren, kan justeres ind og ud ved hjælp af optællingsprocesser som justering af antal og optællingskladdeprocesser.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Få mere at vide om understøttelse af konsignation i Dynamics 365 for Operations                                                                                                         | Find flere oplysninger om understøttelse af konsignationsprocesser i [Konsignation](/dynamics365/unified-operations/supply-chain/inventory/consignment), [Konfigurere konsignation](/dynamics365/unified-operations/supply-chain/inventory/set-up-consignment), [Oprette en genopfyldningsordre til konsignation (opgaveguide)](http://ax.help.dynamics.com/en/wiki/create-a-consignment-replenishment-order/) og [Ændre ejerskabet af konsignationslager baseret på produktionsbehov (opgaveguide)](http://ax.help.dynamics.com/en/wiki/change-the-ownership-of-consignment-inventory-based-on-production-demand/).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Kreditorsamarbejde (tidligere kendt som leverandørportalen)

| Hvad du kan gøre                                                                      | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Få leverandører til at svare på hver købsordrelinje og foreslå ændringer.           | I nogle tilfælde vil leverandører acceptere nogle indkøbsordrelinjer, men afvise andre. Leverandører kan nu styre indkøbsordrelinjer individuelt. Hver linje kan afvises, accepteres eller godkendes med ændringer. Leverandører kan for eksempel ændre leveringsdatoen, opdele levering og antal eller foreslå en alternativ vare.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Få leverandører til at administrere oplysninger om kontaktperson.                                 | Leverandører kan vedligeholde oplysninger om kontaktperson for deres virksomhed. Oplysningerne omfatter navne, mailadresser og telefonnumre. Der gives adgang til denne funktion via en dedikeret sikkerhedsrolle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Dele dokumenter, der er relateret til indkøbsordrer, med leverandører.                    | Når du skal dele et dokument med en leverandør, såsom et dokument om krav, er det praktisk at knytte dokumentet til den relevante indkøbsordre. Leverandøren kan derefter dele noter og vedhæftede filer med kunden ved at knytte dokumentet til hans eller hendes svar på indkøbsordren. Dokumentstyring er den underliggende understøttende struktur, og kun noter og vedhæftede filer, der er klassificeret som "ekstern", kan deles med leverandører.                                                                                                                                                                                                                                                                                                                              |
| Klargøre nye kreditorbrugere.                                                          | Hvis dine kreditorer bruger grænsefladen for kreditorsamarbejde, har de en problemfri måde at anmode om nye brugerkonti på, når nye kontakter kræver adgang til kreditorsamarbejde. Indkøbsmedarbejderne kan sende en anmodning om en brugerkonto for en kontaktperson i kreditororganisationen. En kreditors kontaktperson, der allerede er bruger af kreditorsamarbejde, kan også sende denne type anmodning. Denne anmodning opretter til sidst en ny bruger i Dynamics 365 for Operations, der har kreditorspecifikke sikkerhedsroller. Det letter også en anmodning til Microsoft Azure B2B-portalen om at klargøre brugeren med en ny brugerkonto i Azure Active Directory (Azure AD). Kreditorer kan også anmode om, at specifikke kreditorbrugerkonti deaktiveres, eller sikkerhedsroller ændres. |
| Få mere at vide om understøttelse af kreditorsamarbejde i Dynamics 365 for Operations. | Find flere oplysninger om kreditorsamarbejde i [Leverandørsamarbejde med eksterne leverandører](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-external-vendors), [Kreditorsamarbejde med kunder](/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations), [Administrere brugere af kreditorsamarbejde](/dynamics365/unified-operations/supply-chain/procurement/manage-vendor-collaboration-users), [Konfigurere og vedligeholde kreditorsamarbejde](/dynamics365/unified-operations/supply-chain/procurement/set-up-maintain-vendor-collaboration) og [Arbejdsområde for kreditorsamarbejdsfakturering](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace).                                                         |

### <a name="intercompany-order-processing"></a>Intern ordrebehandling

<table>




<thead>
<tr class="header">
<th>Hvad du kan gøre</th>
<th>Hvorfor dette er vigtigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Definere direkte på salgsordrelinjer, hvor behovet skal anskaffes fra, og hvordan det skal anskaffes. <strong>Eksempel</strong> Opret en salgsordrelinje, og angiv direkte levering som leveringstypen. Den primære kreditor føjes til salgsordrelinjen som forsyningspunkt.</td>
<td>Flow for ordretagning er blevet forbedret betydeligt. Du kan nu definere direkte på salgsordrelinjer, hvor behovet skal anskaffes fra, og hvordan det skal anskaffes. Du behøver ikke længere vente på, at alle linjer er blevet føjet til salgsordren. Med nye muligheder på salgsordrelinjer kan du angive leveringstypen, når du angiver en leverandør. Når du knytter en leverandør til salgsordrelinjer, oprettes ordrekæder til levering fra leverandøren.
<ul>
<li>Leverandøren kan være en intern kreditor, der bruger en intern indkøbsordre og salgsordre, eller det kan være en ekstern leverandør, der bruger en ekstern indkøbsordre.</li>
<li>Leveringstypen kan være <strong>Direkte levering</strong> eller <strong>Lager</strong>. <strong>Lager</strong>-leveringstypen angiver, at leverandøren skal levere til det lokale lager, inden der leveres til kunden.</li>
</ul></td>
</tr>
<tr class="even">
<td>Oprette et ordretilsagn direkte fra salgsordrelinjer. <strong>Eksempel</strong> Opret en salgsordrelinje, der leveres fra en intern kreditor. Gå fra linjen. Leveringsdatoer beregnes i henhold til tilgængelighed i forsyningsfirmaet.</td>
<td>Når du opretter salgsordrelinjer, der bruger de nye forsyningsoplysninger, beregnes leveringsdatoer i henhold til <strong>Leveringsdato</strong>-kontrolelementet. Hvis der f.eks. vælges en intern kreditor, beregnes tilgængelighed i forsyningsvirksomheden. På denne måde oprettes ordrekæder automatisk sammen med salgsordrelinjer. Denne funktionalitet er med til at sikre, at leveringsdatoer bliver synlige i forsyningsvirksomheden, så profiler for disponibel til tilsagn kan håndtere de forventede behov direkte, når salgsordrer oprettes.</td>
</tr>
<tr class="odd">
<td>Gennemse tilgængelighed på tværs af alle forsyningssteder, og vælg den bedste forsyningsmulighed.</td>
<td>Siden <strong>Leveringsalternativer</strong> er blevet ændret, og har nu værdifulde oplysninger om alle godkendte interne og eksterne leverandører. Disse oplysninger omfatter forsyningsindstillinger for leverandørindkøb. Når du vælger en leveringsmåde, beregner systemet mulige leveringsdatoer. Uden problemer kan du vælge den bedste løsning for kunden og anvende denne indstilling for hver salgsordrelinje.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Lagerstedets forbedringer til distributionscentre i store mængder

| Hvad du kan gøre                                                              | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Oprette arbejde, når varer er pakket på en pakkestation.               | Denne funktion er nyttig, når der er flere processer efter manuelt pakkearbejde (f.eks. palletisering, kvalitetskontrol, konsolidering af leverancer eller ændringer til dockingstationer). Den nye **Plukning af pakket container**-arbejdstype kan udforme disse opgaver ved hjælp af separate arbejdslinjer. Nu kan du udforme pakkestationer for at generere arbejde efter pakning. Dette arbejde kan bruges til at organisere flytning af pakket lager.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Gruppere containere på pakkestationen.                                     | Denne funktion gør det muligt for flere pakker at være grupperet i samme container eller id-nummer på pakkestationen. E-handel/engroshandler kan f.eks gruppere 100 enkeltvist emballerede pakker til en enkelt container (f.eks. en palle eller et bur). Denne container kan derefter flyttes, stadieinddeles eller indlæses via en enkelt arbejdsinstruktion, der genereres af en arbejder ved at scanne en enkelt stregkode (id-nummer) for den grupperede container. Dette minimerer arbejdstransaktioner til at flytte mange mindre pakkede containere. Yderligere oplysninger finder du i [Oprette et menupunkt for mobilenhed til konsolidering af id](http://ax.help.dynamics.com/en/wiki/create-a-mobile-device-menu-item-for-license-plate-consolidation/)                                                                                                                                                                                                                                                                                                                                                                                            |
| Oprette en politik om frigivelse for pakkede containere.                               | Arbejde, der udløses af containerfrigivelse, kan oprettes enten automatisk eller manuelt. Når det sker automatisk, oprettes arbejde under containerlukning ved hjælp af lokationsvejledning og arbejdsskabelon som struktur. Når frigivelsen er manuel, kan pakkeren beslutte, om arbejdet skal genereres for en enkelt container eller for en gruppe af containere. Denne funktion reducerer risikoen for, at lukkede containere plukkes og flyttes, før de er klar til at blive flyttet fra pakkestationen. Gør det også muligt for ikke-systemstyret grupperet frigivelse.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Omfordeling af kort pluk                                                   | Der er tilføjet understøttelse af kort pluk-processer for at hjælpe en kollega, der ikke kan plukke varerne og ønsker at opfylde ordren, når den vare, der skal bruges, er disponibel på en anden lokation. Det er muligt at bruge en automatisk omfordelingsproces, som bruger samme lokationsvejledninger til at hente varerne, hvis de er disponible på en anden lokation. Når manuel omfordeling bruges, kan mobilenheden vise en liste over lokationer med det disponible antal. Lagermedarbejderen kan derefter vælge, hvilken lokation lageret skal bruges fra. Disse to metoder kan angives individuelt eller som en enkelt kommando i menuen for lagerarbejder. Når manuel omfordeling bruges, kan lagermedarbejderen vælge antallet af kortplukkede varer fra flere lokationer. Yderligere oplysninger finder du i [Konfigurer vareomfordeling for kort plukning (opgaveguide)](http://ax.help.dynamics.com/en/wiki/set-up-short-picking-item-reallocation/).                                                                                                                                                                                          |
| Flytte lager med tilknyttet arbejde.                             | Nu kan du flytte lager med tilknyttet arbejde. Denne funktion kan være nyttig, hvis for eksempel en arbejder vil rydde plads i modtagelsesområde og flytte registrerede paller, der venter på at blive flyttet til en anden indgående lokation. Dokken ryddes og kan modtage en ekstra last af varer, og det lager, der er flyttet, opdateres med nye læg-på-lager-oplysninger. Denne funktion kan også bruges til at frigøre plads på plukpladser ved at flytte det lager, der har arbejde tilknyttet, og skabe plads til genopfyldning. Du kan også bruge den til at flytte laster fra en midlertidig lokation til en anden uden at miste det læssearbejde, der er genereret. På denne måde kan funktionen hjælpe med at optimere den tid, det tager at læsse lastbiler, når de ankommer. Du kan flytte lager, der er reserveret til salgsordrer, flytteordreafgange, flytteordretilgange og indkøbsordrer. Flytning forhindres, hvis den vil skabe linjer, der skal opdeles. Hvis du f.eks. har en arbejdslinje for 100 stk. af en vare, kan du nøjes med at flytte 30 stk. af varen til en anden lokation. |
| Flette id-numre, der har tilknyttet arbejde.                    | Du kan flette id-numre, der har tilknyttet udgående arbejde. For eksempel når et pluk er inddelt i flere stykker arbejde, kan det være nyttigt at tillade id-numre at blive flettet, når de er leveret til den midlertidige lokation. Id-numre kan kun konsolideres, hvis de er på samme lokation, er medlemmer af den samme last og har samme forsendelsesoplysninger.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Fryse plukarbejde, der er knyttet til genopfyldning på linjeniveau. | Du kan nu fryse arbejde på linjeniveau i stedet for på overskriftsniveau, så arbejdere kan opfylde pluklinjer, der ikke er frosset ved behovsgenopfyldning. En grossist, der har store salgsordrer, eller en detailhandler, der har store salgsordrer eller flytteordrer til genopfyldning, kan derfor starte plukarbejde på alle linjer, der ikke er omfattet af genopfyldningsarbejde. Pluk- og genopfyldningsarbejdet kan derefter udføres parallelt. Denne funktion kan konfigureres, så du kan vælge, om du vil fryse på overskriftsniveau eller linjeniveau. Du kan også bruge begge metoder og oprette en arbejdsskabelon til hver metode. Overskrift-/linjekonfiguration angives på arbejdsskabeloner, men du kan ændre den direkte på det arbejde, der er genereret.                                                                                                                                                                                                                                                                                                                                                                      |
| Annullere arbejde ved hjælp af mobilenheden.                                      | Nu kan du annullere arbejde ved hjælp af mobilenheden, med eller uden behovsgenopfyldning. Tidligere skulle du bruge Rich Client. Hvis du vil aktivere denne funktion, skal du oprette et menupunkt til mobilenheden, der er indstillet til tilstanden **Indirekte** og aktivitetskoden **Annuller arbejde**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |

### <a name="warehouse-operation-enhancements"></a>Forbedringer af lagerstedets funktionalitet

| Hvad du kan gøre                    | Hvorfor dette er vigtigt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modellere forskellige containertyper.   | Du kan bruge forskellige containertyper på lagerstedet til at optimere opbevaring og af andre årsager. Den nye containertypeenhed har de fysiske egenskaber af typen container. Du kan nu knytte id-numre til en bestemt containertype og bruge lagergrænser for lokation. For eksempel kan du bruge denne funktion til at styre, hvor mange paller (eller andre containertyper) du tillader på en specifik lokation. Containertyper er også føjet til enhedsseriegrupper for at tilføje standardcontainertyper for modtagelsesprocessen. Containertyper kan bruges sammen med indgående og udgående lokationsvejledninger. De kan også bruges i visningen af disponibel lagerbeholdning til at afgøre, hvor mange containertyper der aktuelt er på lager. Du kan finde flere oplysninger i blogindlægget [Brug af id-numre, der er knyttet til en containertype, med henblik på at understøtte lokationsstyringsprocesser](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/). Selvom dette blogindlæg beskriver en opdatering til Microsoft Dynamics AX 2012, er samme understøttelse nu føjet til Dynamics 365 for Operations.                                                                                                                                                                                                                                                                                                                         |
| Tilbageføre forsendelser.                 | På et lagersted skal du kunne håndtere sene ændringer. For eksempel kan nogle varer være beskadiget, så du ikke kan levere dem. En kunde kan også foretage en sen anmodning om at annullere eller ændre en ordre. I Dynamics 365 for Operations er det muligt at tilbageføre en forsendelse. Derfor kan du annullere en følgeseddel, så du kan opdatere den med de korrekte antal senere. På samme måde kan du på den indgående strøm annullere produktkvitteringer så der kan oprettes en opdateret version.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Bruge paller, som har forskellige varer. | Du kan nu modtage og registrere en "blandet" palle. En blandet palle består af forskellige varer, der er monteret på én palle til en eller flere indkøbsordrer eller linjer. Alle registreringer kan opsummeres i ét mål-id. Denne proces er aktiveret via lagerstedets mobilenhed. For eksempel når pallen af blandede varer ankommer til lagerstedet kan den modtagende medarbejder identificere varerne og mængderne på pallen, før pallen flyttes til de dedikerede læg-på-lager-lokationer. Læg-på-lager-lokationer er identificeret ved arbejdsskabeloner og lokationsvejledninger. Hvis læg-på-lager-lokationer er spredt over flere varer, der har faste lokationer, opretter denne funktion lige så mange læggearbejdslinjer, som der er forskellige varer på den blandede palle. Denne funktion gør registrering og læg-på-lager af de modtagne blandede varepaller hurtigere og mere fleksibel. Yderligere oplysninger finder du i blogindlægget [Modtage og registrere en palle med blandede kildedokumentlinjer ved hjælp af ét id-nummer](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) og oplysninger om understøttelse af blandet palle i [bekendtgørelsen af vores seneste kumulative opdatering](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). Selvom dette blogindlæg beskriver en opdatering til AX 2012, er samme understøttelse nu føjet til Dynamics 365 for Operations. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Mindre funktionsforbedringer i Supply Chain Management

<table>




<thead>
<tr class="header">
<th>Hvad du kan gøre</th>
<th>Hvorfor dette er vigtigt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bruge nye dataenheder til at importere og eksportere data.</td>
<td>Du kan importere og eksportere data ved hjælp af disse dataenheder:
<ul>
<li>Fragtfaktura</li>
<li>Aggregeret disponibelt lager efter lagersted og lagerstatus</li>
<li>Lagergebyrer</li>
<li>Tilbud</li>
</ul></td>
</tr>
<tr class="even">
<td>Bruge det forbedrede Gantt-kontrolelementet til at udvikle interaktive planlægningsscenarier.</td>
<td>Det forbedrede Gantt-kontrolelement kan udvikle nye interaktive planlægningsscenarier og levere forbedrede API'er, der kan bruges til at tilpasse udseendet af aktiviteter. Her er nogle af de nye API'er:
<ul>
<li>Lodret træk og slip af aktiviteter</li>
<li>Tilføje/fjerne aktiviteter</li>
<li>Vise eksempel på reserverede perioder i oversigtslinje</li>
<li>Ændre farve og typografi på aktivitetskanter</li>
<li>Skifte baggrund, farve og typografi på tekst i gitter</li>
</ul></td>
</tr>
<tr class="odd">
<td>Bedre håndtere materiale og ressourceplanlægning.</td>
<td>Der er foretaget nogle forbedringer af materiale- og ressourceplanlægning:
<ul>
<li>Afgangsmargen håndteres nu, når en vare er på lager.</li>
<li>Overskrive leveringsdatoen, når du autoriserer planlagte ordrer.</li>
<li>Prioritere opfyldelse af ordrer over sikkerhedslager.</li>
<li>Forhindre planlægning af planlagte ordrer i fortiden.</li>
</ul></td>
</tr>
<tr class="even">
<td>Rapportere faktisk forbrug for produktion og se lagerstatus.</td>
<td>Du kan få vist faktisk forbrug til produktion. Desuden er det nye <strong>Vis lagerstatus</strong>-afkrydsningsfelt blevet føjet til <strong>Bevægelse</strong> i menupunktet <strong>Arbejdsoprettelse</strong>, så du kan få vist lagerstatus.</td>
</tr>
<tr class="odd">
<td>Beregne volumetrisk vægt, hvis satserne for fragtmanden er baseret på volumetrisk vægt.</td>
<td>Et nyt TMS-satsprogram, der er baseret på volumetrisk vægt, er blevet tilføjet, så du kan beregne volumetrisk vægt.</td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Se også
--------

[Nyheder eller ændringer](whats-new-changed.md)




