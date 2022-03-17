---
title: Sådan bruges grænsefladen til kørsel af produktionsudstyr af arbejdere
description: Dette emne beskriver, hvordan grænsefladen til kørsel af produktionsudstyr anvendes af arbejderne.
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: a677eb71f97a953c625a1f667b055e5b7696fbe6
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384413"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Sådan bruges grænsefladen til kørsel af produktionsudstyr af arbejdere

[!include [banner](../includes/banner.md)]

Grænsefladen til kørsel af produktionsudstyr er blevet optimeret med berøringsinteraktion. Designet giver en visuel kontrast, der lever op til tilgængelighedskravene i produktionsmiljøer. Det har de samme funktionelle egenskaber som jobkortenheden. Det betyder imidlertid også, at flere job kan startes parallelt fra en jobliste. (Denne egenskab kaldes også *job i bundter*). Arbejderne kan også på en jobliste åbne en guide, der er oprettet i vejledningen til Microsoft Dynamics 365. På denne måde kan de få visuelle instruktioner på en HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Logge på grænsefladen til kørsel af produktionsudstyr som arbejder

Før arbejdere kan begynde at bruge enheden, skal en supervisor eller teknisk personale klargøre den og åbne den korrekte side i Dynamics 365 Supply Chain Management. Du kan finde flere oplysninger om, hvordan du konfigurerer enheden, under [Konfigurere en enhed til at køre grænsefladen på produktionsudstyr](production-floor-execution-setup.md).

Når enheden er blevet forberedt, vises logonsiden. På denne side vises oplysninger om status for job i den lokale arbejdscelle. Disse oplysninger opdateres jævnligt. På siden bruger arbejderne deres badge-id'er, når de logger på. Selvom arbejderne ikke behøver at have en brugerkonto til Supply Chain Management, skal de have en *tidsregistreret arbejder*-konto, som de kan bruge, når de logger på.

![Logonside i grænseflade til kørsel af produktionsudstyr.](media/pfei-sign-in-page.png "Logonside i grænseflade til kørsel af produktionsudstyr")

I de resterende afsnit af dette emne beskrives, hvordan arbejderne kan interagere med grænsefladen.

## <a name="all-jobs-tab"></a>Fanen Alle job

Under fanen **Alle job** kan du se en jobliste med alle de produktionsjob, der har statussen *Ikke startet*, *Stoppet* eller *Startet*. (Dette fanenavn kan tilpasses og kan være forskelligt for dit system).

![Fanen Alle job.](media/pfei-all-jobs-tab.png "Fanen Alle job")

Joblisten har følgende kolonner. Tallene svarer til tallene i ovenstående illustration.

1. **Udvælgelseskolonne** – Kolonnen længst til venstre bruger markeringer til at angive job, der er valgt af arbejderen. Arbejderne kan vælge flere job på listen på samme tid. Hvis du vil vælge alle job på listen, skal du markere afkrydsningsfeltet i kolonneoverskriften. Når der vælges et enkelt job, vises oplysninger om jobbet på den nederste del af siden.
1. **Kolonnen Jobstatus** – I denne kolonne bruges symboler til at angive status for hvert job. Job, der ikke har et symbol i denne kolonne, har statussen *Ikke startet*. En grøn trekant angiver job, der har statussen *Startet*. To gule lodrette linjer angiver job, der har statussen *Stoppet*.
1. **Kolonnen Høj prioritet** – I denne kolonne bruges udråbstegn til at angive job med høj prioritet.
1. **Ordre** – Denne kolonne viser produktionsordrenummeret for et job.
1. **Beskrivelse** – I denne kolonne vises en beskrivelse af den handling, som et job er en del af.
1. **Anmodet** – I denne kolonne vises det antal, som et job ifølge planen skal producere.
1. **Påbegyndt** – I denne kolonne vises det antal, der allerede er påbegyndt for et job.
1. **Fuldført** – I denne kolonne vises det antal, der allerede er fuldført for et job.
1. **Kasseret** – I denne kolonne vises det antal, der allerede er kasseret for et job.
1. **Resterende** – I denne kolonne vises det antal, der mangler at blive fuldført for et job.

## <a name="active-jobs-tab"></a>Fanen Aktive job

Fanerne **Aktive job** viser en liste over alle job, som arbejderen, der er logget på, allerede har startet. (Dette fanenavn kan tilpasses og kan være forskelligt for dit system).

![Fanen Aktive job.](media/pfei-active-jobs-tab.png "Fanen Aktive job")

Listen med aktive job har følgende kolonner:

- **Udvælgelseskolonne** – Kolonnen længst til venstre bruger markeringer til at angive job, der er valgt af arbejderen. Arbejderne kan vælge flere job på listen på samme tid. Hvis du vil vælge alle job på listen, skal du markere afkrydsningsfeltet i kolonneoverskriften. Når der vælges et enkelt job, vises oplysninger om jobbet på den nederste del af siden.
- **Ordre** – Denne kolonne viser produktionsordrenummeret for et job.
- **Beskrivelse** – I denne kolonne vises en beskrivelse af den handling, som et job er en del af.
- **Anmodet** – I denne kolonne vises det antal, som et job ifølge planen skal producere.
- **Påbegyndt** – I denne kolonne vises det antal, der allerede er påbegyndt for et job.
- **Fuldført** – I denne kolonne vises det antal, der allerede er fuldført for et job.
- **Kasseret** – I denne kolonne vises det antal, der allerede er kasseret for et job.
- **Resterende** – I denne kolonne vises det antal, der mangler at blive fuldført for et job.

## <a name="my-jobs-tab"></a>Fanen Mine job

Fanen **Mine job** giver arbejderne mulighed for nemt at se alle ikke-startede og ikke-færdigmeldte job, der er tildelt specifikt til dem. Den er nyttig i firmaer, hvor job nogle gange eller altid tildeles bestemte arbejdere (personale) i stedet for andre typer ressourcer (f.eks. maskiner). 

Planlægningssystemet tildeler automatisk hvert produktionsjob til en bestemt ressourcepost, og hver ressourcepost har en type (f.eks. maskine eller personale). Når du konfigurerer en medarbejder som produktionsarbejder, kan du knytte arbejderkontoen til en entydig personalepost. 

Under fanen **Mine job** vises alle ikke-startede og ikke-færdigmeldte job, der er tildelt personaleposten for den arbejder, der er logget på, hvis en arbejder er logget på. Der vises aldrig job, der er tildelt til en maskine eller en anden type ressource, heller ikke selvom den arbejder, der er logget på, er begyndt at arbejde på disse job.

Hvis du vil have vist alle job, der er startet af den arbejder, der er logget på, uanset den type ressource, som hvert job er tildelt, skal du bruge fanen **Aktive job**. Hvis du vil have vist alle ikke-færdigmeldte job, der svarer til konfigurationen af det lokale jobfilter, uanset arbejderens status eller startstatus, skal du bruge fanen **Alle job**.

![Fanen Mine job.](media/pfei-my-jobs-tab.png "Fanen Mine job")

## <a name="my-machine-tab"></a>Fanen Min maskine

Fanen **Min maskine** giver arbejderne mulighed for at vælge et aktiv, der er tilknyttet en maskinressource i filtersættet på fanen **Alle job**. Arbejderen kan derefter få vist tilstanden for det valgte aktiv ved at aflæse værdier for op til fire valgte tællere og lister over seneste vedligeholdelssanmodninger og registrerede nedetider. Arbejderen kan også anmode om vedligeholdelse for det valgte aktiv og registrere og redigere maskinnedetiden. (Dette fanenavn kan tilpasses og kan være forskelligt for dit system).
 
![Fanen Min maskine.](media/pfei-my-machine-tab.png "Fanen Min maskine")

Fanen **Min maskine** indeholder følgende kolonner. Tallene svarer til tallene i ovenstående illustration.

1. **Maskinaktiv** – Vælg det maskinaktiv, du vil spore. Begynd at skrive et navn, der skal vælges på en liste over tilsvarende aktiver, eller vælg forstørrelsesglassikonet for at vælge mellem alle de aktiver, der er tilknyttet ressourcerne i filteret for joblisten, på en liste.

    > [!NOTE]
    > Brugere af Supply Chain Management kan tildele en ressource til hvert aktiv efter behov ved hjælp af siden **Alle aktiver** (på fanen **Anlægsaktiv** ved hjælp af rullelisten **Ressource**). Du kan finde flere oplysninger under [Opret et aktiv](../asset-management/objects/create-an-object.md).

1. **Indstillinger** – Vælg tandhjulsikonet for at åbne en dialogboks, hvor du kan vælge, hvilke tællere der skal vises for det valgte maskinaktiv. Værdierne for disse tællere vises øverst på fanen **Aktivstyring**. Menuen **Indstillinger** (vist i følgende skærmbillede) giver dig mulighed for at aktivere op til fire tællere. For hver tæller, du vil aktivere, skal du bruge opslagsfeltet øverst i felterne til at vælge en tæller. Opslagsfeltet viser alle de tællere, der er tilknyttet aktivet, som er valgt øverst på siden **Aktivstyring**. Indstil hver tæller til enten at overvåge den **samlede** værdi eller den seneste **faktiske** værdi for tælleren. Hvis du f.eks. angiver en tæller, der sporer, hvor mange timer maskinen har kørt, skal du angive den til **Samlet**. Hvis du angiver en tæller for at måle den seneste opdaterede temperatur eller måling, skal du angive den til **Faktisk**. Vælg **OK** for at gemme dine indstillinger og lukke dialogboksen.

    ![Indstillinger under fanen Min maskine.](media/pfei-my-machine-tab-settings.png "Indstillinger under fanen Min maskine")

1. **Anmod om vedligeholdelse** – Vælg denne knap for at åbne en dialogboks, hvor du kan oprette en vedligeholdelsesanmodning. Du kan angive en beskrivelse og et notat. En bruger af Supply Chain Management vil blive gjort opmærksom på anmodningen, som derefter vil kunne konvertere vedligeholdelsesanmodningen til en arbejdsordre for vedligeholdelse.
1. **Registrér nedetid** – Vælg denne knap for at åbne en dialogboks, hvor du kan registrere maskinnedetid. Du kan vælge en årsagskode og angive en dato/tidsperiode for nedetiden. Registreringen af maskinnedetid bruges til at beregne effektiviteten af maskinaktivet.
1. **Vis eller rediger** – Vælg denne knap for at åbne en dialogboks, hvor du kan redigere eller få vist eksisterende nedetidsposter.

## <a name="starting-and-completing-production-jobs"></a>Start og fuldførelse af produktionsjob

Arbejderne starter et produktionsjob ved at vælge et job under fanen **Alle job** og derefter vælge **Start job** for at åbne dialogboksen **Start job**.

![Dialogboksen Start job.](media/pfei-start-job-dialog.png "Dialogboksen Start job")

Arbejderne bruger dialogboksen **Start job** til at bekræfte produktionsantallet og derefter starte jobbet. De kan justere antallet ved at markere feltet **Antal** og derefter bruge det numeriske tastatur, der vises. De vælger derefter **Start** for at begynde at arbejde på jobbet. Dialogboksen **Start job** lukkes, og jobbet føjes til fanen **Aktive job**.

Arbejderne kan starte et job med en hvilken som helst status. Når en arbejder starter et job, der har statussen *Ikke startet*, viser feltet **Antal** i dialogboksen **Start job** det samlede antal som udgangspunkt. Når en arbejder starter et job, der har statussen *Startet* eller **Stoppet**, viser feltet *Antal* som udgangspunkt det resterende antal.

## <a name="reporting-good-quantities"></a>Rapportering af antal gode

Når en arbejder fuldfører eller delvist fuldfører et job, kan han eller hun rapportere antal gode, der er produceret, ved at vælge et job under fanen **Aktive job** og derefter vælge **Rapportér status**. Derefter angiver arbejderen antallet af gode ved at bruge det numeriske tastatur i dialogboksen **Rapportér status**. Antallet er som standard tomt. Når der er angivet et antal, kan arbejderen opdatere status for jobbet til *I gang*, *Stoppet* eller *Fuldført*.

![Dialogboksen Rapportér status.](media/pfei-report-progress-dialog.png "Dialogboksen Rapportér status")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Rapportering af antal gode på batchordrer, der har samprodukter og biprodukter

Medarbejdere kan bruge grænsefladen til produktionsudførelse til at rapportere status for batchordrer. Denne rapportering inkluderer rapportering af samprodukter og biprodukter.

Visse producenter, særligt i forarbejdningsindustrien, bruger batchordrer til at administrere deres produktionsprocesser. Batchordrer oprettes ud fra formler, og disse formler kan defineres, så de har samprodukter og biprodukter som output. Når der rapporteres feedback på disse batchordrer, skal outputbeløbet registreres på formelvarerne samt på samprodukterne og biprodukterne.

Når en arbejder fuldfører eller delvist fuldfører arbejdet med en batchordre, kan der rapporteres antal gode eller kasserede varer for hvert produkt, der er defineret som output for ordren. Produkter, der er defineret som output for en batchordre, kan være af typen *Formel*, *Samprodukt* eller *Biprodukt*.

Hvis en arbejder vil rapportere gode antal på produkterne, skal han eller hun vælge et job under fanen **Aktive job** og derefter vælge **Rapportér status**.

I dialogboksen **Rapportér status** kan arbejderen derefter vælge mellem de produkter, der er defineret som output for den batchordre, der skal rapporteres om. Arbejderen kan vælge et eller flere produkter på listen og derefter vælge **Rapportér status**. Antallet for hvert produkt er som standard tomt, og arbejderen kan bruge det numeriske tastatur til at angive antallet. Arbejderen kan bruge knapperne **Forrige** og **Næste** til at flytte mellem de valgte produkter. Når antallet er angivet for hvert produkt, kan arbejderen opdatere status for jobbet til *I gang*, *Stoppet* eller *Fuldført*.

![Rapportere samprodukter og biprodukter.](media/report-co-by-products.png "Rapportere samprodukter og biprodukter")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Rapportering af batchordrer til planlægningsvarer

Når en arbejder fuldfører et job i en batchordre for en planlægningsvare, rapporterer de kun antal på samprodukter og biprodukter, da planlægningsvarer ikke indeholder en vare af typen *Formel*.

### <a name="reporting-co-product-variation"></a>Rapportering af varianter af samprodukter

Hvis der oprettes en batchordre ud fra en formelversion, hvor indstillingen **Variationer af samprodukter** angives til *Ja*, kan arbejderen rapportere om samprodukter, der ikke er en del af definitionen for batchordrerne. Denne funktionalitet bruges i scenarier, hvor der kan forekomme uventet produktoutput i produktionsprocessen.

I dette tilfælde kan arbejderen angive det samprodukt og det antal, der skal rapporteres, ved at vælge **Variationer af samprodukter** i dialogboksen til rapportering af status. Arbejderen kan derefter vælge mellem alle de frigivne produkter, der er defineret som samprodukter.

### <a name="reporting-catch-weight-items"></a>Rapportering af fastvægtvarer

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Medarbejdere kan bruge grænsefladen til produktionsudførelse til at rapportere status for batchordrer, der er oprettet til fastvægtvarer. Batchordrer oprettes ud fra formler, som kan defineres til at have fastvægtvarer som formelvarer, samprodukter og biprodukter. En formel kan også defineres, så den indeholder formellinjer til ingredienser, der er defineret for fastvægt. Fastvægtvarer bruger to måleenheder til at spore lagerbeholdning: fastvægtantal og lagerantal. I fødevarebranchen kan kød i kasser f.eks. defineres som en fastvægtvare, hvor fastvægtantallet bruges til at spore antallet af kasser, og lagerantallet bruges til at spore kassernes vægt.

## <a name="reporting-scrap"></a>Rapportering af spild

Når en arbejder fuldfører eller delvist fuldfører et job, kan han eller hun rapportere spild ved at vælge et job under fanen **Aktive job** og derefter vælge **Rapportér spild**. Derefter angiver arbejderen spildantallet ved at bruge det numeriske tastatur i dialogboksen **Rapportér spild**. Arbejderen vælger også en årsag (*Ingen*, *Maskine*, *Operatør* eller *Materiale*).

![Dialogboksen Rapportér spild.](media/pfei-report-scrap-dialog.png "Dialogboksen Rapportér spild")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>Justere materialeforbrug og foretage materialereservationer

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Arbejderne kan justere materialeforbruget for hvert produktionsjob. Denne funktionalitet bruges i scenarier, hvor det faktiske antal materialer, der blev forbrugt af et produktionsjob, var mere eller mindre end det planlagte antal. Den skal derfor reguleres for at holde lagerniveauerne aktuelle.

Arbejderne kan også foretage reservationer af batch- og serienumre for materialer. Denne funktionalitet bruges i scenarier, hvor en arbejder manuelt skal angive, hvilke materialebatch- eller serienumre der er brugt, for at opfylde kravene til materialesporing.

Arbejderne kan angive det antal, der skal reguleres, ved at vælge **Juster materiale**. Knappen er tilgængelig følgende steder:

- I dialogboksen **Rapportér spild**
- I dialogboksen **Rapportér status**
- På værktøjslinjen til højre

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>Justere materialeforbruget fra dialogboksene Rapportér spild og Rapportér status

Når en arbejder angiver det antal, der skal rapporteres, i dialogboksen **Rapportér status** eller **Rapportér spild**, bliver knappen **Juster materiale** tilgængelig. Når brugeren vælger denne knap, vises dialogboksen **Juster materiale**. I denne dialogboks vises de varer, der er planlagt til forbrug, når det gode eller kasserede antal rapporteres for jobbet.

I dialogboksen viser listen følgende oplysninger:

- **Produktnummer** – Produktvarianten og produktmasteren.
- **Produktnavn** – Navnet på produktet.
- **Forslag** – Forkalkuleret antal materialer, der vil blive forbrugt, når der rapporteres status eller spild for det angivne antal til jobbet.
- **Forbrug** – Det faktiske antal materialer, der vil blive forbrugt, når der rapporteres status eller spild for det angivne antal til jobbet.
- **Reserveret** – Det antal materialer, der er fysisk reserveret på lageret.
- **Enhed** – Styklisteenheden.

I dialogboksens højre side vises følgende oplysninger:

- **Produktnummer** – Produktvarianten og produktmasteren.
- **Forkalkuleret** – Det forkalkulerede antal, der skal forbruges.
- **Startet** – Det antal, der er startet på produktionsjobbet.
- **Resterende mængde** – Af det forkalkulerede antal er det antallet, der mangler at blive forbrugt.
- **Frigivet antal** – Det antal, der er forbrugt.

Følgende opgaver kan udføres:

- Arbejderen kan angive det antal, der skal reguleres for et materiale, ved at vælge **Juster forbrug**. Når antallet er bekræftet, opdateres antallet i kolonnen **Forbrug** med det justerede antal.
- Når arbejderen vælger **Juster materiale**, oprettes der en produktionspluklistekladde. Denne kladde indeholder samme varer og antal som listen **Juster materiale**.
- Når arbejderen justerer et antal i dialogboksen **Juster materiale**, opdateres feltet **Forslag** på den tilsvarende kladdelinje med det samme antal. Hvis arbejderen vælger **Annuller** i dialogboksen **Juster materiale**, slettes pluklisten.
- Hvis arbejderen vælger **OK**, slettes pluklisten ikke. Den bogføres, når jobbet rapporteres i dialogboksen **Rapportér spild** eller **Rapportér status**.
- Hvis arbejderen vælger **Annuller** i dialogboksen **Rapportér status** eller **Rapportér spild**, slettes pluklisten.

### <a name="adjust-material-from-the-toolbar-on-the-right"></a>Justere materiale fra værktøjslinjen til højre

Knappen **Juster materiale** kan konfigureres, så den vises på værktøjslinjen til højre. (Du kan finde flere oplysninger i [Designe grænsefladen til produktionsudførelse](production-floor-execution-tabs.md)). En arbejder kan vælge **Juster materiale** for et igangværende produktionsjob. I dette tilfælde vises dialogboksen **Juster materiale**, hvor arbejderen kan foretage de ønskede justeringer. Når dialogboksen åbnes, oprettes der en produktionsplukliste, der indeholder linjer til de justerede antal for produktionsordren. Hvis arbejderen vælger **Bogfør nu**, bekræftes reguleringen, og pluklisten bogføres. Hvis arbejderen vælger **Annuller**, slettes pluklisten uden regulering.

### <a name="adjust-material-consumption-for-catch-weight-items"></a>Justere materialeforbruget for fastvægtvarer

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Arbejdere kan justere materialeforbruget for fastvægtvarer. Denne funktionalitet bruges i scenarier, hvor det faktiske antal af fastvægtmateriale, der blev forbrugt af et produktionsjob, var mere eller mindre end det planlagte antal. Den skal derfor reguleres for at holde lagerniveauerne aktuelle. Når en arbejder justerer forbruget af en fastvægtvare, kan de både justere fastvægtantallet og lagerantallet. Hvis et produktionsjob f.eks. er planlagt til at forbruge fem kasser med en forkalkuleret vægt på 2 kilo pr. kasse, kan arbejderen justere både antal kasser, der skal forbruges, og kassernes vægt. Systemet validerer, at den angivne vægt af kasserne ligger inden for den definerede minimum- og maksimumgrænse, der er defineret for det frigivne produkt.

### <a name="reserve-materials"></a>Reservere materialer

I dialogboksen **Juster materiale** kan en arbejder foretage og justere materialereservationer ved at vælge **Reservér materiale**. I dialogboksen **Reservér materiale** vises den fysisk disponible lagerbeholdning for varen for hver lagrings- og sporingsdimension.

Hvis materialet er aktiveret for processerne for avancerede lagersteder, viser listen kun den fysisk tilgængelige lagerbeholdning for materialets produktionsindlagringslokation. Produktionsindlagringslokationen defineres på den ressource, hvor produktionsjobbet er planlagt. Hvis varenummeret er batch- eller serienummerkontrolleret, vises hele oversigten over de fysisk tilgængelige batch- og serienumre. Arbejderen kan vælge **Reservér materiale** for at angive et antal, der skal reserveres. Hvis en eksisterende reservation skal fjernes, kan arbejderen vælge **Fjern reservation**.

Du kan finde flere oplysninger om, hvordan du konfigurerer produktionsindlagringslokationen, i følgende blogpost: [Konfigurere produktionsindlagringslokation](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production).

> [!NOTE]
> De reservationer, en arbejder foretager i dialogboksen **Reservér materiale**, bevares , når arbejderen vælger **Annuller** i dialogboksen **Rapportér status** eller **Rapportér spild**.
>
> Det er ikke muligt at justere reservationer for fastvægtvarer.

## <a name="completing-a-job-and-starting-a-new-job"></a>Fuldførelse af et job og start af et nyt job

Normalt fuldfører arbejderne et job ved at vælge et eller flere aktuelle job under fanen **Aktive job** og derefter vælge **Rapportér status**. Derefter angiver de det antal, der er produceret (antal gode), og indstiller status til *Fuldført*. Hvis der er valgt mere end ét job, bruger arbejderen derefter knapperne **Forrige** og **Næste** til at flytte mellem dem. For at starte et nyt job skal arbejderen vælge det under fanen **Alle job** og derefter vælge **Start job**.

En arbejder kan også starte et nyt job, mens det forrige job stadig er åbent. Arbejderen vælge igen det nye job under fanen **Alle job** og vælger derefter **Start job**. Denne gang indeholder dialogboksen **Start job** dog oplysninger til arbejderen om, at han aktuelt arbejder på et job, som han derfor enten skal stoppe eller fuldføre, før han starter det nye job.

## <a name="working-on-multiple-jobs-in-parallel"></a>Arbejde med flere job parallelt

En arbejder kan arbejde på flere job på samme tid (dvs. parallelt). I dette tilfælde kaldes den samling job, som arbejderen arbejder på, for et *jobbundt*. Arbejderen kan føje nye job til bundtet eller fuldføre et eller flere job i bundtet. I følgende to scenarier vises, hvordan en arbejder kan arbejde på job parallelt.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Scenarie 1: En arbejder, der ikke har aktive job, vil gerne starte to job og arbejde på dem parallelt

Arbejderen vælger de to job under fanen **Alle job** og vælger derefter **Start job**. I dialogboksen **Start job** vises begge valgte job, og arbejderen kan justere antallet for at starte på hvert job. Arbejderen bekræfter derefter dialogboksen og kan starte begge job.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Scenarie 2: En arbejder, der har to aktive job, som er i gang, vil starte et tredje job og arbejde på det parallelt med de to andre

Arbejderen vælger det tredje job under fanen **Alle job** og vælger derefter **Bundt**. I dialogboksen **Bundt** kan arbejderen justere det antal, der skal startes. Arbejderen bekræfter derefter dialogboksen ved at vælge **Bundt**.

## <a name="working-on-indirect-activities"></a>Arbejde på indirekte aktiviteter

Indirekte aktiviteter er aktiviteter, der ikke er direkte relateret til en produktionsordre. Indirekte aktiviteter kan defineres fleksibelt, som beskrevet i [Konfigurere indirekte aktiviteter for tid og fremmøde](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Shannon, som arbejder i produktionsanlægget hos Contoso, ønsker f.eks. at deltage i et firmamøde, og møder betragtes som en indirekte aktivitet. Et af følgende to scenarier er relevant:

- **Shannon arbejder på et eller flere aktive job.** Hun vælger **Aktivitet**, identificerer aktiviteten (møde) og bekræfter sit valg. Der vises en meddelelse om, at hun har igangværende job. Fra meddelelsen kan hun vælge at fuldføre eller stoppe de job, som hun arbejder på, før hun går til mødet.
- **Shannon har ingen aktive job.** Hun vælger **Aktivitet**, identificerer aktiviteten (møde) og bekræfter sit valg. Det er nu registreret, at hun er til møde.

I begge scenarier, går Shannon, efter at have bekræftet sit valg, enten til logonsiden eller en side, hvor hun skal bekræfte, at hun er returneret, når hun er tilbage fra sin indirekte aktivitet. Hvilken side der vises afhænger af konfigurationen af grænsefladen til kørsel af produktionsudstyr. (Yderligere oplysninger finder du i [Konfigurere grænsefladen til kørsel af produktionsudstyr](production-floor-execution-configure.md)).

## <a name="registering-breaks"></a>Registrere pauser

Arbejderne kan registrere pauser. Pauser kan defineres fleksibelt, som det er beskrevet i [Løn på basis af registreringer](pay-based-on-registrations.md).

En arbejder registrerer en pause ved at vælge **Pause** og derefter vælge det kort, der repræsenterer pausetypen (f.eks. frokost). Når arbejderen har bekræftet sit valg, viser enheden enten logonsiden eller en side, hvor arbejderen skal bekræfte, at han eller hun er returneret fra pausen. Hvilken side der vises afhænger af konfigurationen af grænsefladen til kørsel af produktionsudstyr. (Yderligere oplysninger finder du i [Konfigurere grænsefladen til kørsel af produktionsudstyr](production-floor-execution-configure.md)).

## <a name="opening-instructions"></a>Åbningsinstruktioner

Arbejderne kan åbne et dokument, der er knyttet til et job, ved at vælge **Instruktioner**. Knappen **Instruktioner** er kun tilgængelig, hvis der er knyttet et dokument til jobbet i masterdataene. Et dokument, der er vedhæftet til et produkt på siden **Frigivne produkter** i Supply Chain Management, vil f.eks. kunne åbnes af arbejderne i kørselsgrænsefladen til produktionsudstyret.

## <a name="opening-mixed-reality-guides-for-hololens"></a>Åbning af Mixed Reality-guider til HoloLens

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) kan øge arbejdernes muligheder ved hjælp af praktisk læring, som bygger på Mixed Reality. Du kan definere standardiserede processer, hvor trinvise instruktioner indfører arbejderne i de værktøjer og dele, de har brug for, og viser dem, hvordan de kan bruge disse værktøjer i faktiske arbejdssituationer. Her er en oversigt over processen.

1. Hver gang en arbejder åbner en jobliste i kørselsgrænsefladen til produktionsudstyret, finder grænsefladen alle relevante guider til de viste job.
1. Arbejderen vælger **Guides** for at få vist listen over guider.
1. Arbejderen vælger en relevant guide på listen.
1. Grænsefladen til kørsel af produktionsudstyret viser en QR-kode for den valgte guide.
1. Arbejderen ifører sig en HoloLens og ser på QR-koden for at starte guiden.
1. Arbejderen arbejder sig igennem guiden for at lære at udføre opgaven.

Du kan finde flere oplysninger om, hvordan du opretter, tildeler og bruger guider til HoloLens, under [Levere Mixed-Reality-vejledninger til arbejdere i produktion](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
