---
title: Dataimport- og -eksportjob
description: Bruge arbejdsområdet Datastyring til at oprette og administrere import af data og eksportere job.
author: Sunil-Garg
manager: AnnBe
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ceb2dfa37b53af83c4faedffa5b312d654c44593
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505788"
---
# <a name="data-import-and-export-jobs"></a>Dataimport- og -eksportjob

[!include [banner](../includes/banner.md)]

Når du vil oprette og administrere dataimport- og -eksportjob i Microsoft Dynamics 365 for Finance and Operations, skal du bruge arbejdsområdet **Datastyring**. Som standard opretter processen til import og eksport af data en midlertidig tabel for hver enhed i måldatabasen. Midlertidige tabeller giver dig mulighed for at kontrollere, rense eller konvertere data, før du flytter dem.

> [!NOTE]
> I dette emne antages det, at du er fortrolig med [dataenheder](data-entities.md).

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

De resterende afsnit i dette emne indeholder flere oplysninger om hvert trin i processen.

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

| Filformat            | Række/kolonneafgrænser                       | XML-typografi                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-Ikke relevant-                     |
| XML                    | \-Ikke relevant-                                      | XML-element XML-attribut |
| Afgrænset, fast bredde | Komma, semikolon, tabulering, lodret streg, kolon | \-Ikke relevant-                     |

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

![Tilknytning af data](./media/dixf-map.png)

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

[!NOTE]
Et import- eller eksportjob kan køres asynkront ved at vælge knappen **Importer** eller **Eksporter**. Asynkron kørsel bruger den asynkron struktur i Finance and Operations, som er forskellig fra batchstrukturen. Dog kan den asynkrone struktur ligesom batchstrukturen underkastes begrænsning, og derfor bliver jobbet muligvis ikke udført straks. Job kan også køres synkront ved at vælge **Importer nu** eller **Eksporter nu**. Dette starter jobbet med det samme og er nyttigt, hvis asynkron kørsel eller et batch ikke starter på grund af begrænsning. Jobbene kan også udføres i et batch ved at vælge **Kør i batch**-indstillingen. Batchressourcer er omfattet af begrænsning, så batchjobbet starter muligvis ikke med det samme. Den asynkrone indstilling er nyttig, når brugere interagerer direkte med brugergrænsefladen og ikke er superbrugere, som kan forstå batchplanlægning. Brug af et batch er en anden mulighed, hvis store mængder skal eksporteres eller importeres. Batchjob kan planlægges til at køre på en bestemt batchgruppe, hvilket giver mulighed for større kontrol set fra et belastningsjusteringsperspektiv. Hvis asynkrone kørsler og batchkørsler begge underlægges begrænsning på grund af høj ressourceudnyttelse i systemet, kan den synkrone version af import/eksport bruges som en øjeblikkelig løsning. Den synkrone mulighed starter med det samme og blokerer brugergrænsefladen, fordi den kører synkront. Browservinduet skal forblive åbent, når der udføres synkrone handlinger.

## <a name="validate-that-the-job-ran-as-expected"></a>Kontroller, at jobbet kørte som forventet
Jobhistorikken er tilgængelig i forbindelse med fejlfinding og undersøgelse på både import- og eksportjob. Kørsler af historiske job er organiseret efter tidsintervaller.

![Jobhistorikintervaller](./media/dixf-job-history.md.png)

Hver jobkørsel indeholder følgende oplysninger:

- Detaljer om udførelse
- Udførelseslog

Oplysningerne om kørslen viser tilstanden for hver dataenhed, som jobbet behandlede. Derfor kan du hurtigt finde følgende oplysninger:

- Hvilke enheder blev behandlet.
- For en enhed, hvor mange poster blev behandlet korrekt, og hvor mange mislykkedes
- De midlertidige poster for hver enhed

Du kan hente de midlertidige data i en fil til eksportjob, eller du kan hente dem som en pakke til import- og eksportjob.

På grundlag af oplysningerne i kørslen, kan du også åbne kørselslogfilen.

## <a name="clean-up-the-staging-tables"></a>Ryd op i de midlertidige tabeller
Du kan rydde op i midlertidige tabeller ved hjælp af funktionen **Oprydning i midlertidige filer** i arbejdsområdet **Datastyring**. Du kan bruge følgende indstillinger til at vælge, hvilke poster der skal slettes fra de midlertidige tabeller:

- **Enhed** – Hvis der kun angives en enhed, slettes alle poster fra den pågældende enheds midlertidig tabel. Vælg denne indstilling for at rydde op i alle dataene for enheden på tværs af alle dataprojekter og alle job.
- **Job-id** – Hvis der kun angives et job-id, slettes alle poster for alle enheder i det valgte job fra de relevante midlertidige tabeller.
- **Dataprojekter** – Hvis der kun er markeret et dataprojekt, slettes alle poster for alle enheder og på tværs af alle job for det valgte dataprojekt.

Du kan også kombinere indstillingerne for yderligere at begrænse det postsæt, der slettes.
