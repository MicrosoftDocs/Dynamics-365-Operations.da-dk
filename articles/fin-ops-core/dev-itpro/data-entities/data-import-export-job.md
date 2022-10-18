---
title: Oversigt over dataimport- og -eksportjob
description: Bruge arbejdsområdet Datastyring til at oprette og administrere import af data og eksportere job.
author: peakerbl
ms.date: 08/26/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfd06c30ae09a175862810a0c85399358a65fdb0
ms.sourcegitcommit: 43a0fb019bc67c00c39c2778343ba89924c3322c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/12/2022
ms.locfileid: "9671452"
---
# <a name="data-import-and-export-jobs-overview"></a>Oversigt over dataimport- og -eksportjob

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Når du vil oprette og administrere dataimport- og -eksportjob, skal du bruge arbejdsområdet **Datastyring**. Som standard opretter processen til import og eksport af data en midlertidig tabel for hver enhed i måldatabasen. Midlertidige tabeller giver dig mulighed for at kontrollere, rense eller konvertere data, før du flytter dem.

> [!NOTE]
> Denne artikel antager, at du er fortrolig med [dataenheder](data-entities.md).

## <a name="data-importexport-process"></a>Dataimport og -eksportproces
Her er trinnene til import eller eksport af data.

1. Opret et import- eller eksportjob, hvor du kan udføre følgende opgaver:

    - Definer projektkategorien.
    - Identificer de enheder, der skal importeres eller eksporteres.
    - Angiv jobbets dataformat.
    - Anbring enhederne i rækkefølge, så de behandles i logiske grupper og i en rækkefølge, der giver mening.
    - Bestem, om der skal bruges midlertidige tabeller.

2. Kontroller, at kildedataene og måldataene er tilknyttet korrekt.
3. Kontroller sikkerheden i dit import- eller eksportjob.
4. Kør import- eller eksportjobbet.
5. Kontroller, at jobbet kørte som forventet ved at gennemse jobhistorikken.
6. Ryd op i de midlertidige tabeller.

De resterende afsnit i denne artikel indeholder flere oplysninger om hvert trin i processen.

> [!NOTE]
> For at opdatere formen til dataimport og -eksport, så den viser den seneste status, skal du bruge ikonet for opdatering. Opdatering på browserniveau anbefales ikke, fordi det afbryder alle import- eller eksportjob, der ikke køres i batch.

## <a name="create-an-import-or-export-job"></a>Oprette et import- eller eksportjob
Et dataimport eller -eksportjob kan køres én gang eller mange gange.

### <a name="define-the-project-category"></a>Definer projektkategorien
Vi anbefaler, at du giver dig tid til at vælge en relevant projektkategori til dit import- eller eksportjob. Projektkategorier kan hjælpe dig med at administrere relaterede job.

### <a name="identify-the-entities-to-import-or-export"></a>Identificer de enheder, der skal importeres eller eksporteres
Du kan føje bestemte objekter til et import- eller eksportjob eller vælge en skabelon, der skal anvendes. Skabeloner udfylder et job med en liste over enheder. Indstillingen **Anvend skabelon** er tilgængelig, når du har give jobbet et navn og gemmer jobbet.

### <a name="set-the-data-format-for-the-job"></a>Angiv jobbets dataformat
Når du vælger en enhed, skal du vælge formatet for de data, der skal eksporteres eller importeres. Du kan definere formater ved hjælp af feltet **Opsætning af datakilder**. Et dataformat for kilden er en kombination af **Type**, **Filformat**, **Rækkeafgrænser** og **Kolonneafgrænser**. Der findes også andre attributter, men disse er dem, der er vigtige at forstå. Følgende tabel viser de gyldige kombinationer.

> [!NOTE]
> Excel-filformatet er ikke aktuelt tilgængeligt i Datastyringsarbejdsområdet til Government Community Cloud (GCC).

| Filformat            | Række/kolonneafgrænser                       | XML-typografi                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-Ikke relevant-                     |
| XML                    | \-Ikke relevant-                                      | XML-element XML-attribut |
| Afgrænset, fast bredde | Komma, semikolon, tabulering, lodret streg, kolon | \-Ikke relevant-                     |

> [!NOTE]
> Det er vigtigt at vælge den korrekte værdi for **Rækkeafgrænser**, **Kolonneafgrænser** og **Tekstoperator**, hvis indstillingen **Filformat** er angivet til **Afgrænset**. Sørg for, at dine data ikke indeholder det tegn, der bruges som afgrænser eller operator, da dette kan resultere i fejl under import og eksport.

> [!NOTE]
> I forbindelse med XML-baserede filformater skal du sørge for kun at bruge juridiske tegn. Yderligere oplysninger om gyldige tegn finder du i [Gyldige tegn i XML 1.0](https://www.w3.org/TR/2006/REC-xml-20060816/Overview.html#charsets/). I XML 1.0 må der ikke være kontroltegn med undtagelse af faner, returneringer af omst., og linjeangivelser. Eksempler på ugyldige tegn er kantede kantede parenteser, kantede parenteser og skråstreger. 

Brug Unicode i stedet for en bestemt kodeside til at importere eller eksportere data. På den måde får du de mest ensartede resultater, og datastyringsjob undgås, fordi de inkluderer Unicode-tegn. De systemdefinerede kildedataformater, der bruger Unicode, har alle **Unicode** i kildenavnet. Unicode-formatet anvendes ved at vælge en Unicode-kodningsside med ANSI-kode som **Kodeside** i fanen **Regionale indstillinger**. Vælg en af følgende kodesider for Unicode:

| Tegntabel | Vist navn                |
|-----------|-----------------------------|
| 1200      | Unicode                     |
| 12000     | Unicode (UTF-32)            |
| 12001     | Unicode (UTF-32 Big-Endian) |
| 1201      | Unicode (Big-Endian)        |
| 65000     | Unicode (UTF-7)             |
| 65001     | Unicode (UTF-8)             |

Yderligere oplysninger om kodesider finder du under [Identifikation af kodeside](/windows/win32/intl/code-page-identifiers/).

### <a name="sequence-the-entities"></a>Anbring enhederne i rækkefølge
Enheder kan sorteres i en dataskabelon eller i import- og eksportjob. Når du kører et job, der indeholder mere end én dataenhed, skal du sikre dig, at dataenhederne er i korrekt rækkefølge. Du anbringer primært enheder rækkefølge, så du kan løse eventuelle funktionelle afhængigheder mellem enheder. Hvis enheder ikke har funktionelle afhængigheder, kan de planlægges til parallel import eller eksport. 

#### <a name="execution-units-levels-and-sequences"></a>Kørsel af enheder, niveauer og nummerserier
Afviklingsenheden, niveauet i afviklingsenheden og rækkefølgen af en enhed hjælper med til at kontrollere den rækkefølge, data eksporteres eller importeres i.

- Enheder i forskellige afviklingsenheder behandles parallelt.
- I hver afviklingsenhed behandles enheder parallelt, hvis de har samme niveau.
- På hvert niveau behandles enheder i henhold til deres sekvensnummer på det pågældende niveau.
- Når et niveau er blevet behandlet, behandles den næste niveau.

#### <a name="resequencing"></a>Fornyet rækkefølge
Du ønsker at sætte dine enheder i en fornyet rækkefølge i følgende situationer:

- Hvis der kun bruges ét datajob til alle dine ændringer, kan du bruge indstillingerne til fornyet rækkefølge til at optimere udførelsestiden for hele jobbet. I disse tilfælde, kan du bruge udførelsesenheden til at repræsentere modulet, niveauet til at repræsentere funktionsområdet i modulet, og rækkefølgen til at repræsenterer enheden. Når du bruger denne metode, kan du arbejde parallelt på tværs af moduler, men du kan stadig arbejde i rækkefølge i et modul. For at sikre, at parallelle operationer gennemføres, skal du overveje alle afhængigheder.
- Hvis der bruges flere datajob (f.eks. et job for hvert modul), kan du bruge rækkefølge til at påvirke niveauet og rækkefølgen af enheder for optimal udførelse.
- Hvis der ikke er nogen afhængigheder overhovedet, kan du sætte enheder i rækkefølge ved forskellige udførelsesenheder for at få maksimal optimering.

Menuen **Fornyet rækkefølge** er tilgængelig, når flere enheder er markeret. Du kan skabe en fornyet rækkefølge baseret på udførelsesenhed, niveau eller indstillinger for rækkefølge. Du kan angive et interval til fornyet rækkefølge af de enheder, der er valgt. Enheden, niveauet og/eller løbenummeret, der er valgt for hver enhed, opdateres med det angivne interval.

#### <a name="sorting"></a>Sortering
Du kan bruge indstillingen **Sorter efter** til at få enhedslisten i indstilling for at få vist listen i rækkefølge.

### <a name="truncating"></a>Afkortning
Ved importprojekter kan du vælge at afkorte poster i enhederne før importen. Dette er nyttigt, hvis posterne skal importeres til et tomt sæt tabeller. Denne indstilling er som standard slået fra.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Kontroller, at kildedataene og måldataene tilknyttes korrekt
Tilknytningen er en funktion, der gælder for både import- og eksportjob.

- I forbindelse med et importjob beskriver tilknytningen, hvilke kolonner i kildefilen, der bliver til kolonnerne i den midlertidige tabel. Systemet kan derfor afgøre, hvilke kolonnedata i kildefilen der skal kopieres til hvilken kolonne i den midlertidige tabel.
- I forbindelse med et eksportjob beskriver tilknytningen, hvilke kolonner i den midlertidige tabel (det vil sige kilden), der bliver til kolonnerne i målfilen.

Hvis kolonnenavnene i den midlertidige tabel og filen matcher hinanden, opretter systemet automatisk tilknytning, der er baseret på navnene. Men hvis navnene er forskellige, tilknyttes kolonnerne ikke automatisk. I så fald skal du fuldføre tilknytningen ved at vælge indstillingen **Vis tilknytning** på enheden i datajobbet.

Der er to visninger af tilknytningen: **Visualisering af tilknytning**, som er standardvisningen, og **Oplysninger om tilknytning**. En rød stjerne (\*) identificerer de påkrævede felter i enheden. Disse felter skal tilknyttes, før du kan arbejde med enheden. Du kan fjerne tilknytningen af andre felter, som du ønsker, når du arbejder med enheden. Hvis du vil fjerne tilknytningen af et felt, skal du vælge feltet i enten kolonnen **Enhed** eller kolonnen **Kilde** og derefter vælge **Slet udvælgelse**. Vælg **Save** for at gemme dine ændringer, og luk derefter siden for at gå tilbage til projektet. Du kan bruge den samme proces til at redigere felttilknytningen fra kilde til midlertidig fil, når du har importeret.

Du kan oprette en tilknytning på siden ved at vælge **Generér kildetilknytning**. En genereret tilknytning fungerer som en automatisk tilknytning. Du skal derfor manuelt tilknytte eventuelle ikke-tilknyttede felter.

![Tilknytning af data.](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Kontroller sikkerheden i dit import- eller eksportjob
Adgangen til arbejdsområdet **Datastyring** kan begrænses, så brugere, der ikke er administratorer, kun har adgang til bestemte datajob. Adgang til et datajob indebærer fuld adgang til udførelseshistorikken for jobbet og adgang til de midlertidige tabeller. Du skal derfor sikre dig, at relevante adgangskontroller er på plads, når du opretter et datajob.

### <a name="secure-a-job-by-roles-and-users"></a>Sikre et job efter roller og brugere
Brug menuen **Gældende roller** til at begrænse jobbet til en eller flere sikkerhedsroller. Kun brugere i disse roller har adgang til jobbet.

Du kan også begrænse et job til specifikke brugere. Når du sikrer et job efter brugere i stedet for efter roller, er der mere kontrol, hvis flere brugere er tildelt en rolle.

### <a name="secure-a-job-by-legal-entity"></a>Sikre et job efter juridisk enhed
Datajob er af natur globale. Hvis et datajob derfor blev oprettet og brugt i en juridisk enhed, vil jobbet være synligt i andre juridiske enheder i systemet. Denne standardindstilling kan være at foretrække i visse anvendelsesscenarier. F.eks. kan en organisation, der importerer fakturaer ved hjælp af dataenheder, sende data til en centraliseret fakturabehandlingsgruppe, der er ansvarlig for administration af fakturafejl for alle afdelinger i organisationen. I dette scenarie er det nyttigt for det centraliserede fakturabehandlingsteam at have adgang til fakturaimportjob fra alle juridiske enheder. Derfor opfylder standardfunktionsmåden kravene fra perspektivet for en juridisk enhed.

Men en organisation ønsker muligvis at have fakturabehandlingsteams pr. juridisk enhed. I så fald skal et team i en juridisk enhed kun have adgang til fakturaimportjobbet i sin egen juridiske enhed. For at opfylde disse krav, kan du konfigurere adgangskontrol baseret på juridisk enhed for datajob ved hjælp af menuen **Anvendelige juridiske enheder** i datajobbet. Når konfigurationen er fuldført, kan brugere kun se job, der er tilgængelige i den juridiske enhed, de aktuelt er logget på. Hvis de vil se job fra en anden juridisk enhed, skal brugerne skifte til den pågældende juridiske enhed.

Et job kan sikres efter roller, brugere og juridisk enhed på samme tid.

## <a name="run-the-import-or-export-job"></a>Kør import- eller eksportjob
Du kan køre et job én gang ved at vælge knappen **Import** eller **Eksport**, når du har defineret jobbet. Du kan konfigurere et tilbagevendende job ved at vælge **Opret tilbagevendende datajob**.

> [!NOTE]
> Et import- eller eksportjob kan køres ved at vælge knappen **Importer** eller **Eksporter**. Dette planlægger, at et batchjob kun skal køres én gang. Jobbet kan muligvis ikke køres med det samme, hvis batchtjenesten begrænser det pga. belastningen af batchtjenesten. Job kan også køres synkront ved at vælge **Importer nu** eller **Eksporter nu**. Dette starter jobbet med det samme og er nyttigt, hvis et batch ikke starter på grund af begrænsning. Jobbene kan også planlægges til at blive kørt på et senere tidspunkt. Det kan du gøre ved at vælge indstillingen **Kør i batch**. Batchressourcer er omfattet af begrænsning, så batchjobbet starter muligvis ikke med det samme. Det anbefales, at du bruger en batch, fordi det også vil hjælpe med store mængder data, der skal importeres eller eksporteres. Batchjob kan planlægges til at køre på en bestemt batchgruppe, hvilket giver mulighed for større kontrol set fra et belastningsjusteringsperspektiv.

## <a name="validate-that-the-job-ran-as-expected"></a>Kontroller, at jobbet kørte som forventet
Jobhistorikken er tilgængelig i forbindelse med fejlfinding og undersøgelse på både import- og eksportjob. Kørsler af historiske job er organiseret efter tidsintervaller.

![Jobhistorikintervaller.](./media/dixf-job-history.md.png)

Hver jobkørsel indeholder følgende oplysninger:

- Detaljer om udførelse
- Udførelseslog

Oplysningerne om kørslen viser tilstanden for hver dataenhed, som jobbet behandlede. Derfor kan du hurtigt finde følgende oplysninger:

- Hvilke enheder blev behandlet.
- For en enhed, hvor mange poster der blev behandlet korrekt, og hvor mange der mislykkedes.
- De midlertidige poster for hver enhed.

Du kan hente de midlertidige data i en fil til eksportjob, eller du kan hente dem som en pakke til import- og eksportjob.

På grundlag af oplysningerne i kørslen, kan du også åbne kørselslogfilen.

## <a name="parallel-imports"></a>Parallel import
For at gøre det hurtigere at importere data kan parallel behandling af en filimport aktiveres, hvis enheden understøtter parallel import. Hvis du vil konfigurere parallel import for en enhed, skal du følge disse trin.

1. Gå til **Systemadministration \> Arbejdsområder \> Datastyring**.
2. I afsnittet **Import/eksport** skal du vælge feltet **Rammeparametre** for at åbne siden **Rammeparametre for dataimport/-eksport**.
3. Under fanen **Indstillinger for enhed** skal du vælge **Konfigurer udførelsesparametre for enhed** for at åbne siden **Udførelsesparametre for enhedsimport**.
4. Angiv følgende felter for at konfigurere parallel import for en enhed:

    - I feltet **Enhed** skal du vælge enheden.
    - I feltet **Antal poster for importtærskel** skal du angive grænsen for antallet af poster til import. Dette bestemmer det antal poster, der skal behandles af en tråd. Hvis en fil har 10.000 poster, vil et postantal på 2500 med et opgaveantal på 4 betyde, at hver tråd behandler 2500 poster.
    - Angiv antallet af importopgaver i feltet **Antal importopgaver**. Dette må ikke overstige det maksimale antal batchtråde, der er tildelt batchbehandling i **Systemadministration \>Serverkonfiguration**.

## <a name="job-history-clean-up"></a>Oprydning i jobhistorik 
Funktionen til oprydning i jobhistorik i datastyring skal bruges til at planlægge en regelmæssig oprydning af udførelseshistorikken. Denne funktionalitet erstatter den tidligere oprydningsfunktion til midlertidig tabel, som nu udfases. Følgende tabeller vil blive ryddet op af oprydningsprocessen.

-   Alle midlertidige tabeller

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

Funktionen **Oprydning i kørselsoversigt** skal være aktiveret i funktionsstyring, og derefter er der adgang til den fra **Datastyring \> Oprydning i jobhistorik**.

### <a name="scheduling-parameters"></a>Planlægningsparametre

Når oprydningsprocessen planlægges, skal følgende parametre angives for at definere oprydningskriterierne.

-   **Antal dage, historikken skal bevares** – Denne indstilling bruges til at kontrollere den mængde udførelseshistorik, der skal bibeholdes. Det er angivet i antal dage. Når oprydningsjobbet er planlagt som et tilbagevendende batchjob, fungerer denne indstilling som en tidsramme, der bevæger sig kontinuerligt, og som altid efterlader historikken intakt i det angivne antal dage, mens resten slettes. Standarden er 7 dage.

-   **Antal timer til at udføre jobbet** – Afhængigt af den mængde historik, der skal ryddes op, kan den samlede udførelsestid for oprydningsjobbet variere fra et par minutter til et par timer. Dette parameter skal angives til det antal timer, som jobbet skal udføre. Når oprydningsjobbet er blevet udført i det angivne antal timer, afsluttes jobbet, og oprydningen fortsættes, næste gang det køres på grundlag af gentagelsesplanen.

    Der kan angives en maksimal gennemførelsestid ved at angive en maksimumgrænse for det antal timer, jobbet skal køre, ved hjælp af denne indstilling. Oprydningslogikken går gennem ét jobudførelses-id ad gangen i en kronologisk arrangeret sekvens, med det ældste først for oprydning af relateret udførelseshistorik. Det vil stoppe plukning af nye udførelses-id'er til oprydning, når den resterende udførelsesvarighed er inden for de sidste 10 % af den angivne varighed. I nogle tilfælde forventes det, at oprydningsjobbet fortsætter ud over den angivne maksimale tid. Dette afhænger i høj grad af antallet af poster, der skal slettes for det aktuelle udførelses-id, som blev startet, før tærsklen på 10 % blev nået. Den oprydning, der blev startet, skal være fuldført for at sikre dataintegriteten, hvilket betyder, at oprydning vil fortsætte på trods af overskridelse af den angivne grænse. Når dette er gennemført, bliver nye udførelses-id'er ikke opsamlet, og oprydningsjobbet er fuldført. Den resterende udførelseshistorik, der ikke blev ryddet op på grund af manglende gennemførelsestid, vil blive medtaget, næste gang oprydningsjobbet er planlagt. Standard- og minimumværdien for denne indstilling er angivet til 2 timer.

-   **Tilbagevendende batch** – Oprydningsjobbet kan køres som en manuel engangsudførelse, eller det kan også planlægges til tilbagevendende udførelse i batch. Batchen kan planlægges ved hjælp af indstillingerne **Kør i baggrunden**, som er standardbatchopsætning.

> [!NOTE]
> Hvis posterne i de midlertidige tabeller ikke er fuldstændig renset, skal du sikre dig, at oprydningsjobbet er planlagt til at skulle køre som en gentagelse. Som forklaret ovenfor vil jobbet i enhver oprydningskørsel alene fjerne så mange kørsels-id'er, som det er muligt inden for de opgivne maksimum timer. For at fortsætte oprydningen af eventuelle tilbageværende midlertidige poster, skal jobbet planlægges til at køre med jævne mellemrum.

## <a name="job-history-clean-up-and-archival"></a>Oprydning og arkivering af jobhistorik 
Funktionen til oprydning og arkivering af jobhistorik erstatter de tidligere versioner af oprydningsfunktionen. I dette afsnit forklares disse nye funktioner.

En af de vigtigste ændringer i oprydningsfunktionen er brugen af systembatchjobbet til oprydning af historikken. Brugen af systembatchjobbet giver programmer til finans og drift mulighed for automatisk planlægning og kørsel af oprydningsbatchjobbet, så snart systemet er klart. Det er ikke længere nødvendigt at planlægge batchjobbet manuelt. I denne standardkørselstilstand køres batchjobbet hver time fra og med midnat, og kørselshistorikken bevares for de seneste 7 dage. Den slettede oversigt arkiveres, så den kan hentes senere. Fra og med version 10.0.20 er denne funktion altid aktiveret.

Den anden ændring i oprydningsprocessen er arkiveringen af den slettede kørselshistorik. Oprydningsjobbet arkiverer de slettede poster i det blob-lager, som DIXF bruger til almindelige integrationer. Den arkiverede fil vil være i DIXF-pakkeformatet og vil være tilgængelig i 7 dage i blob'en, hvor den kan hentes. Standardvarigheden på 7 dage for den arkiverede fil kan ændres til højst 90 dage i parametrene.

### <a name="changing-the-default-settings"></a>Ændre standardindstillingerne
Denne funktionalitet er aktuelt i prøveversion og skal aktiveres eksplicit ved at aktivere flightet DMFEnableExecutionHistoryCleanupSystemJob. Funktionen til midlertidig oprydning skal også være aktiveret i funktionsstyring.

Hvis du vil ændre standardindstillingen for varigheden for den arkiverede fil, skal du gå til arbejdsområdet Dataadministration og vælge **Oprydning i jobhistorik**. Angiv **Dage, som pakken skal bevares i blob** til en værdi mellem 7 og 90 (inklusive). Dette vil træde i kraft for de arkiver, der oprettes, efter at denne ændring blev foretaget.

### <a name="downloading-the-archived-package"></a>Hente den arkiverede pakke
Denne funktionalitet er aktuelt i prøveversion og skal aktiveres eksplicit ved at aktivere flightet DMFEnableExecutionHistoryCleanupSystemJob. Funktionen til midlertidig oprydning skal også være aktiveret i funktionsstyring.

Hvis du vil hente den arkiverede kørselshistorik, skal du gå til arbejdsområdet Dataadministration og vælge **Oprydning i jobhistorik**. Vælg **Historik for sikkerhedskopiering af pakke** for at åbne historikformularen. I denne formular vises listen over alle arkiverede pakker. Du kan vælge og hente et arkiv ved at vælge **Download pakke**. Den hentede pakke vil være i DIXF-pakkeformat og indeholde følgende filer:

-   Fil fra midlertidig enhedstabel
-   DMFDEFINITIONGROUPEXECUTION
-   DMFDEFINITIONGROUPEXECUTIONHISTORY
-   DMFEXECUTION
-   DMFSTAGINGEXECUTIONERRORS
-   DMFSTAGINGLOG
-   DMFSTAGINGLOGDETAILS
-   DMFSTAGINGVALIDATIONLOG



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

