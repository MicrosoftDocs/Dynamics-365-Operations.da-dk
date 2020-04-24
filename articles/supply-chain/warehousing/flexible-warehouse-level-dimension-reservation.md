---
title: Reservationspolitik for fleksibel dimension for lagerstedsniveau
description: I dette emne beskrives politikken for lagerreservation, hvor virksomheder, der sælger batchsporede produkter og kører deres logistik som WMS-aktiverede operationer, kan reservere bestemte batches for kundesalgsordrer, selvom det reservationshierarki, der er tilknyttet produkterne, ikke tillader reservation af bestemte batches.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0fe9ed9f2bebe8683f3b8bb37b33e8a63b9521f6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205661"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Reservationspolitik for fleksibel dimension for lagerstedsniveau

[!include [banner](../includes/banner.md)]

Når et lagerreservationshierarki af typen "Batch under\[lokation\]" er knyttet til produkter, kan virksomheder, der sælger batchsporede produkter og kører logistik som handlinger, der er aktiveret for Microsoft Dynamics 365 Warehouse Management System (WMS), ikke reservere bestemte batches af de pågældende produkter til kundesalgsordrer. Dette emne beskriver den politik for lagerreservation, der giver disse virksomheder mulighed for at reservere bestemte batches, selv når produkterne er knyttet til et reservationshierarki af typen "batch-under\[lokation\]".

## <a name="inventory-reservation-hierarchy"></a>Lagerreservationshierarki

I dette afsnit opsummeres det eksisterende lagerreservationshierarki. Der fokuseres på den måde, batchsporede og seriesporede varer håndteres på.

Lagerreservationshierarkiet bestemmer, at med hensyn til lagringsdimensioner er det behovsordren, der har de obligatoriske dimensioner for websted, lagersted og lagerstatus, hvorimod lagerstedets logik er ansvarlig for at tildele en lokation til de ønskede antal og reserve lokationen. I interaktionerne mellem behovsordren og lagerstedsoperationerne forventes det med andre ord, at behovsordren angiver, hvor ordren skal afsendes fra (dvs. hvilket sted og lagersted). Lagerstedet er derefter afhængig af logikken for at finde det påkrævede antal på lagerstedet.

For at afspejle den operationelle model for virksomheden er sporingsdimensionerne (batch- og serienumre) dog underlagt større fleksibilitet. Et lagerreservationshierarki kan tage højde for scenarier, hvor følgende betingelser gælder:

- Virksomheden er afhængig af sin lagerdrift for at administrere plukning af antal, der har batch- eller serienumre, efter at antallene er fundet på lagerpladsen i lagerstedet. Denne model kaldes ofte *Batch-under\[lokation\]*. Den bruges typisk, når et produkts batch- eller serienummeridentifikation ikke er vigtig for de kunder, der placerer efterspørgslen hos den sælgende virksomhed.
- Hvis batch- eller serienumre er en del af en kundes ordrespecifikation, og de registreres i behovsordren, er den lagerdrift, der finder antal på lagerstedet, begrænset af de specifikt ønskede numre, og de kan ikke ændres. Denne model kaldes ofte *Batch-over\[lokation\]*.

I disse scenarier er udfordringen, at der kun kan tildeles ét lagerreservationshierarki til hvert frigivet produkt. For at WMS kan håndtere sporede varer, efter at hierarkitildelingen bestemmer, hvornår batch- eller serienummeret skal reserveres (enten når behovsordren udtages eller under pluk på lagerstedet), kan denne tidsindstilling ikke ændres på ad hoc-basis.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Fleksibel reservation for batchsporede varer

### <a name="business-scenario"></a>Forretningsscenarie

I dette scenario bruger et firma en lagerstrategi, hvor færdigvarer spores efter batchnumre. Dette firma bruger også WMS-arbejdsbyrden. Da denne arbejdsbyrde har en veludviklet logik til planlægning og kørsel af lagerstedspluk- og forsendelsesoperationer for batchaktiverede varer, er de fleste af de færdige varer knyttet til et lagerreservationshierarki af typen "Batch-under\[lokation\]". Fordelen ved denne type driftsopsætning er, at beslutninger (der rent faktisk er reservationsbeslutninger) om, hvilke batches der skal plukkes, og hvor de skal placeres på lagerstedet, udskydes, indtil lagerstedsplukoperationerne er startet. De foretages ikke, når kundeordren afgives.

Selvom reservationshierarkiet "Batch-under\[lokation\]" fungerer godt for firmaets forretningsmål, kræver mange af firmaets etablerede kunder samme batch, som de tidligere har købt, når de genbestiller produkter. Derfor vil firmaet søge efter fleksibilitet i den måde, som reglerne for batchreservation håndteres på, så der sker følgende, afhængigt af kundernes behov for den samme vare:

- Et batchnummer kan registreres og reserveres, når ordren udtages af salgsbehandleren, og det kan ikke ændres under lagerdrift og/eller udtages af andre behov. Denne funktionsmåde er en hjælp til at sikre, at det batchnummer, der blev bestilt, sendes til kunden.
- Hvis batchnummeret ikke er vigtigt for kunden, kan lagerdriften bestemme et batchnummer under pluk, efter salgsordreregistrering og reservation er udført.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Tilladelse af reservation af en bestemt batch i salgsordren

For at give plads til den ønskede fleksibilitet i batchreservationens funktionsmåde for varer, der er knyttet til et lagerreservationshierarki af typen "Batch-under\[lokation\]", skal lagerstyringen markere afkrydsningsfeltet **Tillad reservation i behovsordre** for niveauet **Batchnummer** på siden **Lagerreservationshierarkier**.

![Angivelse af fleksibelt lagerreservationshierarki](media/Flexible-inventory-reservation-hierarchy.png)

Når niveauet **Batchnummer** i hierarkiet vælges, vil alle dimensioner over dette niveau og op gennem niveauet **Lokation** automatisk blive valgt. (Som standard er alle dimensioner over niveauet **Lokation** niveauet forudvalgt). Denne funktionsmåde afspejler den logik, hvor alle dimensioner i intervallet mellem batchnummeret og lokationen også reserveres automatisk, når du reserverer et bestemt batchnummer på ordrelinjen.

> [!NOTE]
> Afkrydsningsfeltet **Tillad reservation i behovsordre** gælder kun for reservationshierarkiniveauer, der er ligger under lagerstedets lokationsdimension.
>
> **Batchnummer** er det eneste niveau i hierarkiet, der er åbent for den fleksible reservationspolitik. Du kan med andre ord ikke markere afkrydsningsfeltet **Tillad reservation i behovsordre** for niveauet **Lokation**, **Nummerplade** eller **Serienummer**.
>
> Hvis reservationshierarkiet indeholder serienummerdimensionen (der altid skal være under niveauet **Batchnummer**), og hvis du har aktiveret batchspecifik reservation for batchnummeret, fortsætter systemet med at håndtere serienummerreservation og plukoperationer baseret på de regler, der gælder for reservationspolitikken "Serie-under\[lokation\]".

Du kan på et hvilket som helst tidspunkt tillade batchspecifik reservation for et eksisterende reservationshierarki af typen "Batch-under\[lokation\]" i din installation. Denne ændring påvirker ikke reservationer og åbent lagerstedsarbejde, der er oprettet, før ændringen blev foretaget. Det er dog ikke muligt at fjerne markeringen af afkrydsningsfeltet **Tillad reservation i behovsordre**, hvis der findes lagertransaktioner af afgangstypen **Reserveret bestilt**, **Reserveret fysisk** eller **Bestilt** for en eller flere varer, der er tilknyttet det pågældende reservationshierarki.

> [!NOTE]
> Hvis en vares eksisterende reservationshierarki ikke tillader batchspecifikation i ordren, kan du igen tildele det til et reservationshierarki, der tillader batchspecifikation, forudsat at strukturen i hierarkiniveauet er den samme i begge hierarkier. Brug funktionen **Skift reservationshierarki til varer** til at udføre omfordelingen. Denne ændring kan være relevant, når du vil forhindre fleksibel batchreservation af et undersæt af batchsporede varer, men tillade den for resten af produktsortimentet.

Hvis du ikke vil reservere et bestemt batchnummer for varen på en ordrelinje, så gælder standardlogikken for lagerdrift, der er gældende for et reservationshierarki af typen "Batch-under\[lokation\]", stadig, uanset om du har markeret afkrydsningsfeltet **Tillad reservation i behovsordre**.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Reservere et bestemt batchnummer til en kundeordre

Efter en batchsporet vares lagerreservationshierarki af typen "Batch-under\[lokation\]" er konfigureret til at tillade reservation af bestemte batchnumre i salgsordrer, kan salgsordrebehandlere udtage kundeordrer på samme vare på en af følgende måder afhængigt af kundens anmodning:

- **Angiv ordredetaljer uden at angive et batchnummer** – denne tilgang skal bruges, når produktets batchspecifikation ikke er vigtig for kunden. Alle eksisterende processer, der er knyttet til håndtering af en ordre af denne type i systemet, ændres ikke. Der kræves ingen yderligere overvejelser fra brugernes side.
- **Angiv ordredetaljer, og reservér et bestemt batchnummer** – denne tilgang skal bruges, når kunden anmoder om en bestemt batch. Kunderne anmoder typisk om en bestemt batch, når de genbestiller et produkt, som de tidligere har købt. Denne type batchspecifik reservation er en såkaldt *ordrebekræftet reservation*.

Følgende regelsæt er gældende, når antal behandles, og et batchnummer bekræftes for en bestemt ordre:

- Hvis der skal kunne foretages reservation af et bestemt batchnummer for en vare i henhold til reservationspolitikken "Batch-under\[lokation\], skal systemet reservere alle dimensioner til og med lokation. Dette område omfatter typisk id-dimensionen.
- Lokationsvejledninger bruges ikke, når der oprettes plukarbejde for en salgslinje, hvor der bruges ordrebekræftet batchreservation.
- Hverken brugeren eller systemet må ændre batchnummeret under lagerstedsbehandling af arbejde for ordrebekræftede batches. (Denne behandling omfatter undtagelseshåndtering).

I følgende eksempel vises slutpunkt-til-slutpunkt-flowet.

## <a name="example-scenario"></a>Eksempelscenario

I dette eksempel skal du have installeret demodata, og du skal bruge demodatafirmaet **USMF**.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a>Opret et lagerreservationshierarki for at tillade batchspecifik reservation

1. Gå til **Lokationsstyring** \> **Opsætning** \> **Lager \> Reservationshierarki**.
2. Vælg **Ny**.
3. Angiv et navn i feltet **Navn** (f.eks. **Batchfleks**).
4. Indtast en beskrivelse i feltet **Beskrivelse** (f.eks. **Batch under fleksibel**).
5. I feltet **Valgt** skal du vælge **Serienummer** og **Ejer** og derefter vælge den venstre pileknap for at flytte dem til feltet **Tilgængelig**.
6. Vælg **OK**.
7. I rækken med dimensionsniveau for **Batchnummer** skal du markere afkrydsningsfeltet **Tillad reservation i behovsordre**. Niveauerne **Nummerplade** og **Lokation** vælges automatisk, og du kan ikke fjerne markeringerne i afkrydsningsfelterne for dem.
8. Vælg **Gem**.

### <a name="create-a-new-released-product"></a>Opret et nyt frigivet produkt

1. Angiv produktets tre masterdataparametre ved hjælp af følgende værdier:

    - Vælg **Artikler** i feltet **Lagringsdimensionsgruppe**.
    - Vælg **Batch-fy** i feltet **Sporingsdimensionsgruppe**.
    - I feltet **Reservationshierarki** skal du vælge **Batchfleks**.

2. Opret to batchnumre f.eks. **B11** og **B22**.
3. Føj vareantal til disponibel lagerbeholdning ved hjælp af følgende værdier.

    | Lagersted | Batchnummer | Adresse | Nummerplade | Mængde |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Ingen          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a>Indtast oplysninger om salgsordrer

1. Gå til **Salg og marketing** \> **Salgsordrer** \> **Alle salgsordrer**.
2. Vælg **Ny**.
3. Angiv **US-003** i feltet **Debitorkonto** i salgsordrehovedet.
4. Tilføj en linje for den nye vare, og angiv **10** som antal. Sørg for, at feltet **Lagersted** er angivet til **24**.
5. Vælg **Lager** i oversigtspanelet **Salgsordrelinjer**, og vælg derefter **Batchreservation** i gruppen **Vedligehold**. På siden **Batchreservation** vises en liste over batches, der er tilgængelige til reservation for ordrelinjen. I dette eksempel vises antallet **20** for batchnummer **B11** og antallet **10** for batchnummer **B22**. Bemærk, at der ikke kan opnås adgang til siden **Batchreservation** fra en linje, hvis varen på linjen er tilknyttet reservationshierarkiet "Batch-under\[lokation\]", medmindre den er konfigureret til at tillade batchspecifik reservation.

    > [!NOTE]
    > Hvis du vil reservere et bestemt batch til en salgsordre, skal du bruge siden **Batchreservation**.
    >
    > Hvis du angiver batchnummeret direkte på salgsordrelinjen, fungerer systemet, som om du har angivet en bestemt batchværdi for en vare, der er underlagt reservationspolitikken "Batch-under\[lokation\]". Når du gemmer linjen, vil du modtage en advarselsmeddelelse. Hvis du bekræfter, at batchnummeret skal angives direkte på ordrelinjen, håndteres linjen ikke af den almindelige lokationsstyringslogik.
    >
    > Hvis du reserverer antallet fra siden **Reservation**, reserveres der ikke noget bestemt batch, og udførelsen af lagerdrift for linjen følger de regler, der gælder i henhold til reservationspolitikken "Batch-under\[lokation\]".

    Generelt er funktionen og interaktionen med denne side meget lig den måde, der arbejdes og interageres med varer, som har et tilknyttet reservationshierarki af typen "Batch-over\[lokation\]". Der gælder dog følgende undtagelser:

    - Oversigtspanelet **Batchnumre bundet til kildelinje** viser de batchnumre, der er reserveret til ordrelinjen. Batchværdierne i gitteret vises under hele udførelsescyklussen for ordrelinjen, herunder lagerstedets behandlingsstadier. Derimod vises der i oversigtspanelet **Oversigt** en almindelig ordrelinjereservation (dvs. reservation, der udføres for dimensionerne over niveauet **Lokation**) i gitteret op til det punkt, hvor der oprettes lagerstedsarbejde. Arbejdsenheden overtager derefter linjereservationen, og linjereservationen vises ikke længere på siden. Oversigtspanelet **Batchnumre bundet til kildelinje** sikrer, at salgsordrebehandleren kan få vist de batchnumre, der er bundet til kundens ordre på et tidspunkt i løbet livscyklussen op til og med fakturering.
    - Ud over at reservere en bestemt batch kan en bruger manuelt vælge batchens specifikke lokation og id i stedet for at lade systemet vælge dem automatisk. Denne funktion er relateret til designet af den ordrebekræftede batchreservationsmekanisme. Når et batchnummer reserveres for en vare i henhold til reservationspolitikken "Batch-under\[lokation\], skal systemet som tidligere nævnt reservere alle dimensioner til og med lokation. Lagerstedsarbejdet vil derfor indeholde de samme lagringsdimensioner, der blev reserveret af de brugere, der har arbejdet med ordrerne, og de repræsenterer muligvis ikke altid den varelagringsplacering, der er praktisk eller endda mulig for plukoperationer. Hvis ordrebehandlere er opmærksomme på lagerbegrænsningerne, kan det være en god ide manuelt at vælge de specifikke lokationer og id'er, når de reserverer en batch. I dette tilfælde skal brugeren bruge funktionen **Vis dimensioner** i sidehovedet og tilføje lokationen og id'et i gitteret i oversigtspanelet **Oversigt**.

6. På siden **Batchreservation** skal du vælge linjen for batch **B11** og derefter vælge **Reserver linje**. Der er ingen foruddefineret logik ved tildeling af lokationer og id'er under automatisk reservation. Du kan angive antallet manuelt i feltet **Reservation**. Bemærk, at oversigtspanelet **Batchnumre bundet til kildelinje**, batch **B11** er vist som **Bindende**.

    ![Tilknytning af et bestemt batchnummer til en salgsordrelinje på siden Batchreservation](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Reservation af antallet i en salgsordrelinje kan udføres på tværs af flere batches. På samme måde kan reservation af samme batch udføres mod flere lokationer og id'er (hvis der er aktiveret id'er for lokationerne).
    >
    > Reservation af en bestemt batch for antallet på en salgsordrelinje kan også være delvis. Det samlede antal på 100 enheder kan f.eks. reserveres, så en bestemt batch bekræftes til 20 enheder, hvorimod 80 enheder er reserveret på lokations- og lagerstedsniveauer for alle tilgængelige batches. I dette tilfælde vil WMS håndtere plukoperationer ved hjælp af to separate arbejdslinjer.

7. Gå til **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**. Vælg din vare, og vælg derefter **Styr lager** \> **Vis** \> **Transaktioner**.

    ![Ordrebekræftet reservation som en lagertransaktionstype](media/Inventory-transactions-for-order-committed-reservation.png)

8. Gennemse varens lagertransaktioner, der er relateret til reservationen af salgsordrelinjen.

    - En transaktion, hvor feltet **Reference** er angivet til **Salgsordre**, og feltet **Afgang** er angivet til **Reserveret fysisk**, repræsenterer ordrelinjereservationen for lagerdimensionerne over niveauet **Lokation**. Ifølge varens lagerreservationshierarki er disse dimensioner lokation, lagersted og lagerstatus.
    - En transaktion, hvor feltet **Reference** er angivet til **Ordrebekræftet reservation**, og feltet **Afgang** er angivet til **Reserveret fysisk**, repræsenterer ordrelinjereservationen for den specifikke batch og alle lagerdimensionerne over den. Ifølge varens lagerreservationshierarki er disse dimensioner batchnummer og lokation. I dette eksempel er lokationen **Bulk-001**.

9. Vælg **Lagersted** \> **Handlinger** \> **Frigiv til lagersted** i salgsordrehovedet. Ordrelinjen er nu i bølge, og der oprettes en belastning og et arbejde.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Gennemse og behandl lagerstedsarbejde, der har ordrebekræftede batchnumre

1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Lagersted** \> **Arbejdsdetaljer**.

    Det arbejde, der håndterer plukoperationen for batchantal, der er bundet til salgsordrelinjen, har følgende karakteristika:

    - For at kunne oprette arbejde bruger systemet arbejdsskabeloner, men ikke lokationsvejledninger. Alle de standardindstillinger, der er defineret for arbejdsskabeloner, f.eks. det maksimale antal pluklinjer eller en bestemt måleenhed, vil blive anvendt til at bestemme, hvornår der skal oprettes nyt arbejde. De regler, der er knyttet til lokationsvejledninger til identifikation af pluklokationer, tages dog ikke i betragtning, fordi den ordrebekræftede reservation allerede angiver alle lagerdimensionerne. Disse lagerdimensioner omfatter dimensionerne på lagerstedets lagerniveau. Derfor arver arbejdet disse dimensioner, uden at lokationsvejledninger skal benyttes.
    - Batchnummeret vises ikke på pluklinjen (som det er tilfældet for den arbejdslinje, der er oprettet for en vare, der har et tilknyttet reservationshierarki for "Batch-over\[lokation\]"). I stedet vises batchnummeret "fra" og alle andre lagringsdimensioner i arbejdslinjens lagertransaktion, der refereres til fra de tilknyttede lagertransaktioner.

        ![Lagersteds lagertransaktion for arbejde, der stammer fra ordrebekræftet reservation](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Når arbejdet er oprettet, fjernes varens lagertransaktion, hvor feltet **Reference** er angivet til **Ordrebekræftet reservation**. Lagertransaktionen, hvor feltet **Reference** er angivet til **Arbejde**, indeholder nu den fysiske reservation af lagerdimensionerne for alle antal.

        Lagerdrift kan fortsætte med at håndtere udførelsen af arbejdet på sædvanlig vis. Vejledningen på mobilenheden giver dog arbejderen besked på at vælge et bestemt batchnummer. I lagermiljøer med id-styrede lokationer kan en arbejder, når vedkommende når en lokation, der gemmer samme batch med flere id'er, plukke fra et hvilket som helst id, der ikke allerede er reserveret (f.eks. af en anden ordrebekræftet reservation eller arbejde, der stammer fra en reservation af den pågældende type).

        Hvis det bliver for upraktisk at plukke fra den lokation, der er angivet på arbejdslinjen, kan lageroperatøren bruge en af følgende handlinger til at omdirigere plukning af den specifikke batch fra en mere praktisk lokation:

        - Standardhandlingen **Tilsidesæt lokation** på en mobilenhed (hvis lagermedarbejderens indstilling **Tillad tilsidesættelse af pluklokation** er aktiveret)
        - Handlingen **Skift lokation** på siden **Arbejdslistedetaljer**. 

2. Udfør plukning og placering af arbejdet på mobilenheden.

    Antallet **10** for batchnummer **B11** plukkes nu for salgsordrelinjen og placeres på lokationen **Baydoor**. På dette tidspunkt er det klar til at blive læsset på lastbilen og sendt til kundens adresse.

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a>Undtagelseshåndtering af lagerstedsarbejde, der har ordrebekræftede batchnumre

Lagerstedsarbejde for plukning af ordrebekræftede batchnumre er underlagt samme standardhåndtering af undtagelser for lagersted og handlinger som almindeligt arbejde. Generelt kan det åbne arbejde eller den åbne arbejdslinje annulleres, den kan afbrydes, fordi en brugerlokation er fuld, den kan være kort plukket, og den kan opdateres på grund af en bevægelse. På samme måde kan den plukkede mængde arbejde, der allerede er udført, reduceres, eller arbejdet kan tilbageføres.

Følgende nøgleregel anvendes til alle disse handlinger af typen undtagelseshåndtering: Det batchnummer, der er reserveret til kunden, kan aldrig erstattes med et andet batchnummer, men lagerdimensionerne (lokation og id) kan ændres via enten en manuel opdatering fra brugerens side eller en automatisk opdatering udført af systemet. Den automatiske opdatering er baseret på den samme tilfældige tildeling af lagringsdimensioner, der anvendes, når en bestemt batch blev reserveret automatisk, men der ikke blev angivet nogen lagerdimensioner.

### <a name="example-scenario"></a>Eksempelscenario

Et eksempel på dette scenario er en situation, hvor tidligere udført arbejde ikke kan plukkes ved hjælp af funktionen **Reducer det antal, der er plukket**. I dette eksempel fortsættes det foregående eksempel i dette emne.

1. Gå til **Lokationsstyring** \> **Laster** \> **Aktive laster**.
2. Vælg den last, der blev oprettet i forbindelse med forsendelsen af salgsordren.
3. Vælg **Reducer det antal, der er plukket** i oversigtspanelet **Indlæs ordrelinjer**.
4. Vælg **FL-001** i feltet **Flyt til lokation** på siden **Reducer det antal, der er plukket**.
5. Vælg **LP33** i feltet **Flyt til nummerplade**.
6. Angiv **10** i feltet **Lagerantal, hvor plukning skal fortrydes**.
7. Vælg **OK**.

Følgende er resultatet af handlingen til fortrydelse af plukning:

- Status for det tidligere lukkede arbejde angives til **Annulleret**.
- Der oprettes nyt arbejde af typen **Lagerbevægelser** for det ikke-plukkede antal på **10** for batchnummer **B11**. Dette arbejde repræsenterer bevægelsen fra lokationen **Baydoor** til id **LP33** på lokation **FL-001**. Status er angivet til **Lukket**.
- Systemet reserverer igen det batchnummer, der oprindeligt blev bestilt, og tildeler lokation og id'er. (Denne proces svarer til at køre funktionen **Reserver linje** for ordrelinjen for et bestemt batchnummer). Derfor vises **B11** som bekræftet i oversigtspanelet **Batchnumre bundet til kildelinje** på siden **Batchreservation**, og feltet **Reservation** indeholder antallet **10** for batchnummer **B11**. Desuden angives feltet **Lokation** til **FL-001**, og feltet **Nummerplade** angives til **LP11**. (Du kan føje disse felter til gitteret, hvis de ikke er synlige).

Følgende tabeller indeholder en oversigt, der viser, hvordan systemet håndterer ordrebekræftet batchreservation for specifikke lagerstedshandlinger. Hvis du vil fortolke indholdet i tabellerne, skal du antage, at hver lagerstedshandling køres i konteksten af det eksisterende lagerarbejde, der stammer fra en ordrebekræftet batchreservation, eller at udførelsen af de enkelte lagerhandlinger påvirker arbejde af den pågældende type.

> [!NOTE]
> I disse tabeller angiver kolonnen "Batchantal er tilgængeligt", om der findes et tilgængeligt batchantal ud over det antal, der enten allerede er reserveret for de aktuelle ordrebekræftede reservationer, eller som allerede er reserveret af det lagerstedsarbejde, der stammer fra reservationer af den pågældende type.

#### <a name="override-the-pick-location-on-the-open-work"></a>Tilsidesæt pluklokationen for det åbne arbejde

<table>
<thead>
<tr>
<th>Vigtig opsætningsparameter</th>
<th>Batchantal er tilgængeligt</th>
<th>Vigtige brugertrin</th>
<th>Lagerstedsarbejde</th>
<th>Ordrebekræftet batchreservation</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Indstillingen <strong>Tillad tilsidesættelse af pluklokation</strong> er aktiveret for arbejderen.</td>
<td>Ja</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Tilsidesæt lokation</strong> på WMA (mobilappen for lagerstedet), når du starter pluk af arbejde.</li>
<li>Vælg <strong>Foreslå</strong>.</li>
<li>Bekræft den nye lokation, der foreslås, på basis af tilgængeligheden af batchantal.</li>
</ol>
</td>
<td>Følgende handlinger finder sted i det aktuelle arbejde:
<ul>
<li>Lokationen på pluklinjen opdateres til den nye lokation. (Hvis lokaliteten er id-styret, tildeles et tilfældigt id til lagerbeholdningstransaktionen, og arbejderen kan plukke fra et hvilken som helst id, der har tilgængeligt antal).</li>
<li>Hvis antallet findes på mere end ét id på den nye lokation, opdeles den oprindelige pluklinje i flere linjer, så den svarer til hvert enkelt id.</li>
</ul>
</td>
<td>Ikke relevant</td>
</tr>
<tr>
<td>Nr.</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Tilsidesæt lokation</strong> på WMA, når du starter pluk af arbejde.</li>
<li>Angiv en lokation manuelt.</li>
</ol>
</td>
<td>Handlingen <strong>Tilsidesæt lokation</strong> er ikke mulig. Det mislykkes, og der udløses en fejl.</td>
<td>Ikke relevant</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Knappen Fuld – opdel en arbejdslinje på grund af overløb på brugerens lokation

<table>
<thead>
<tr>
<th>Vigtig opsætningsparameter</th>
<th>Batchantal er tilgængeligt</th>
<th>Vigtige brugertrin</th>
<th>Lagerstedsarbejde</th>
<th>Ordrebekræftet batchreservation</th>
</tr>
</thead>
<tbody>
<tr>
<td>Indstillingen <strong>Tillad opdeling af arbejde</strong> er aktiveret for menupunktet mobilenhed.</td>
<td>Ikke relevant</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Fuld</strong> på WMA, når du behandler plukarbejde.</li>
<li>I feltet <strong>Plukantal</strong> skal du angive en del af antallet af det krævede pluk for at angive den fulde kapacitet.</li>
</ol>
</td>
<td>
<ul>
<li>I det aktuelle arbejde opdateres antallet med det resterende antal, der skal plukkes.</li>
<li>Nyt arbejde for det plukkede antal oprettes og lukkes.</li>
</ul></td>
<td>Ikke relevant</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Reducer det plukkede antal af fuldført arbejde (fra en last)

<table>
<thead>
<tr>
<th>Vigtig opsætningsparameter</th>
<th>Batchantal er tilgængeligt</th>
<th>Vigtige brugertrin</th>
<th>Lagerstedsarbejde</th>
<th>Ordrebekræftet batchreservation</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Ikke relevant</td>
<td>Ja</td>
<td>
<ol>
<li>Åbn siden <strong>Reducer det antal, der er plukket</strong> antal fra lastlinjen.</li>
<li>Angiv hele antallet, plukning skal fortrydes for.</li>
<li>Vælg en "flyt til"-lokation/id.</li>
</ol>
</td>
<td>
<ul> 
<li>Arbejde, der er tilknyttet lastlinjen, annulleres.</li>
<li>Nyt arbejde for lagerbevægelsen oprettes og lukkes.</li>
</ul>
</td>
<td>Antallet reserveres igen for samme batch. Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</td>
</tr>
<tr>
<td>Nr.</td>
<td>Se den forrige række.</td>
<td>Se den forrige række.</td>
<td>Antallet reserveres igen for samme batch og for samme lokation og id (hvis lokationen er id-styret), der blev angivet under annullering af pluk.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Flyt en vare inden for et lagersted

> [!NOTE]
> Denne lagerstedshandling gælder kun for flytning af typen **Arbejdsoprettelsesproces**, ikke for bevægelse efter skabelon.

<table>
<thead>
<tr>
<th>Vigtig opsætningsparameter</th>
<th>Batchantal er tilgængeligt</th>
<th>Vigtige brugertrin</th>
<th>Lagerstedsarbejde</th>
<th>Ordrebekræftet batchreservation</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Indstillingen <strong>Tillad flytning af lager med tilknyttet arbejde</strong> er aktiveret for arbejderen.</td>
<td>Ja</td>
<td>
<ol>
<li>Start en bevægelse på WMA.</li>
<li>Angiv "fra"- og "til"-lokationer.</li>
</ol></td>
<td>
<ul>
<li>I alt eksisterende arbejde, der påvirkes af flytningen, opdateres plukpladsen til den nye "til"-lokation.</li>
<li>Nyt arbejde for lagerbevægelsen oprettes og lukkes.</li>
</ul>
</td>
<td>Alle eksisterende reservationer, der påvirkes af antalsbevægelsen fra den angivne lokation, reserveres igen for samme batch. Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</td>
</tr>
<tr>
<td>Nr.</td>
<td>Se den forrige række.</td>
<td>Se den forrige række.</td>
<td>Alle eksisterende reservationer, der påvirkes af antalsbevægelsen fra den angivne lokation, reserveres igen for den samme batch og for den nye "til"-lokation og det nye id (hvis lokationen er id-styret).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Tilbagefør det plukkede antal af fuldført arbejde (fra en belastning eller en bølge)

<table>
<thead>
<tr>
<th>Vigtig opsætningsparameter</th>
<th>Batchantal er tilgængeligt</th>
<th>Vigtige brugertrin</th>
<th>Lagerstedsarbejde</th>
<th>Ordrebekræftet batchreservation</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Ikke relevant</td>
<td>Ja</td>
<td>
<ol>
<li>Åbn siden <strong>Tilbagefør arbejde</strong>.</li>
<li>Vælg indstillingen <strong>Efterlad varer på aktuel lokation</strong> på siden med anmodning.</li>
</ol>
</td>
<td>Alt arbejde, der er tilknyttet lasten, annulleres.</td>
<td>Antallet reserveres igen for samme batch. Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</td>
</tr>
<tr>
<td>Nr.</td>
<td>Se den forrige række.</td>
<td>Se den forrige række.</td>
<td>Antallet reserveres igen for den samme batch og for den lokation og det id, hvor antallet blev placeret ved tilbageførsel.</td>
</tr>
<tr>
<td>Ja</td>
<td>
<ol>
<li>Åbn siden <strong>Tilbagefør arbejde</strong>.</li>
<li>Vælg indstillingen <strong>Tildel varer til denne lokation</strong> på siden med anmodning.</li>
</ol>
</td>
<td>
<ul>
<li>Det aktuelle arbejde er annulleret.</li>
<li>Nyt arbejde for lagerbevægelsen oprettes og lukkes.</li>
</ul>
</td>
<td>Antallet reserveres igen for samme batch. Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</td>
</tr>
<tr>
<td>Nr.</td>
<td>Se den forrige række.</td>
<td>Se den forrige række.</td>
<td>Antallet reserveres igen for den samme batch og for den lokation og det id, som antallet blev tildelt ved tilbageførsel.</td>
</tr>
<tr>
<td>Ja/nej</td>
<td>
<ol>
<li>Åbn siden <strong>Tilbagefør arbejde</strong>.</li>
<li>Vælg indstillingen <strong>Flyt varer til denne lokation</strong> på siden med anmodning.</li>
</ol>
</td>
<td>Tilbageførsel understøttes ikke.</td>
<td>Ikke relevant</td>
</tr>
<tr>
<td>Ja/nej</td>
<td>
<ol>
<li>Åbn siden <strong>Tilbagefør arbejde</strong>.</li>
<li>Vælg indstillingen <strong>Flyt varer på basis af lokationsvejledninger</strong> på siden med anmodning.</li>
</ol>
</td>
<td>Tilbageførsel understøttes ikke. </td>
<td>Ikke relevant</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Kort pluk et antal – Registrer antallet som fysisk ikke fundet ved lokationen/id'et, når du udfører plukarbejde

<table>
<thead>
<tr>
<th>Vigtig opsætningsparameter</th>
<th>Batchantal er tilgængeligt</th>
<th>Vigtige brugertrin</th>
<th>Lagerstedsarbejde</th>
<th>Ordrebekræftet batchreservation</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Ingen</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Nej</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Kort pluk</strong> på WMA, når du kører plukarbejde.</li>
<li>Angiv <strong>0</strong> i feltet <strong>Pluk antal</strong> (nul).</li>
<li>I feltet <strong>Årsag</strong> skal du angive <strong>Ingen omfordeling</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Det aktuelle arbejde er lukket, og det plukkede antal er 0 (nul).</li>
<li>Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</li>
</ul>
</td>
<td>Antallet reserveres igen for samme batch. Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</td>
</tr>
<tr>
<td>Nr.</td>
<td>Se den forrige række.</td>
<td>
<ul>
<li>Handlingen kort pluk mislykkes, og der udløses en fejl.</li>
<li>Det aktuelle arbejde forbliver åbent.</li>
</ul>
</td>
<td>Ikke relevant</td>
</tr>
<tr>
<td rowspan='2'>En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Ingen</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Kort pluk</strong> på WMA, når du kører plukarbejde.</li>
<li>Angiv <strong>0</strong> i feltet <strong>Pluk antal</strong> (nul).</li>
<li>I feltet <strong>Årsag</strong> skal du angive <strong>Ingen omfordeling</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Det aktuelle arbejde er lukket, og det plukkede antal er 0 (nul).</li>
<li>Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</li>
</ul>
</td>
<td>Alle eksisterende reservationer, der påvirkes af antalsreguleringen i den kort plukkede lokation, reserveres igen for samme batch. Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</td>
</tr>
<tr>
<td>Nr.</td>
<td>Se den forrige række.</td>
<td>Se den forrige række.</td>
<td>Alle eksisterende reservationer, der påvirkes af antalsreguleringen i den kort plukkede lokation, fjernes.</td>
</tr>
<tr>
<td>En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Nej/Ja</strong>. Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</td>
<td>Ja</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Kort pluk</strong> på WMA, når du kører plukarbejde.</li>
<li>Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</li>
<li>I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</li>
<li>Vælg lokationen/id'et på listen.</li>
</ol>
</td>
<td>
<ul>
<li>Følgende handlinger finder sted i det aktuelle arbejde:
<ul>
<li>Pluklinjen er lukket, og det plukkede antal er 0 (nul).</li>
<li>Læg på lager-linjen annulleres.</li>
<li>Der oprettes en ny pluklinje. Den bruger den lokation/det ud, som brugeren har valgt.</li>
<li>Der oprettes en ny læg på lager-linje.</li>
</ul>
</li>
<li>Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</li>
</ul>
</td>
<td>Ikke relevant</td>
</tr>
<tr>
<td>En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Nej</strong>. Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</td>
<td>Nr.</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Kort pluk</strong> på WMA, når du kører plukarbejde.</li>
<li>Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</li>
<li>I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</li>
</ol>
</td>
<td>Handlingen kort pluk mislykkes, og der udløses en fejl.</td>
<td>Ikke relevant</td>
</tr>
<tr>
<td>En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja</strong>. Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</td>
<td>Nr.</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Kort pluk</strong> på WMA, når du kører plukarbejde.</li>
<li>Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</li>
<li>I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</li>
<li>Vælg lokationen/id'et på listen.</li>
</ol>
</td>
<td>
<ul>
<li>Følgende handlinger finder sted i det aktuelle arbejde:
<ul>
<li>Pluklinjen er lukket, og det plukkede antal er 0 (nul).</li>
<li>Læg på lager-linjen annulleres.</li>
</ul>
</li>
<li>Der oprettes en lagertransaktion af typen <strong>Optælling</strong>, og afgangstypen <strong>Solgt</strong> oprettes for at repræsentere reguleringen.</li>
</ul>
</td>
<td>Alle eksisterende reservationer, der påvirkes af antalsreguleringen i den kort plukkede lokation/id, fjernes.</td>
</tr>
<tr>
<td>En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Automatisk</strong>, <strong>Reguler lager</strong> = <strong>Ja/Nej</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja/Nej</strong>.</td>
<td>Ikke relevant</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Kort pluk</strong> på WMA, når du kører plukarbejde.</li>
<li>Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</li>
<li>I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med automatisk omfordeling</strong>.</li>
</ol>
</td>
<td>Kort pluk, der involverer automatisk omfordeling, understøttes ikke.</td>
<td>Kort pluk, der involverer automatisk omfordeling, understøttes ikke.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Skift status for lagerbeholdning

> [!NOTE]
> Lagerstedshandlingen kan udføres fra flere indgangspunkter. Det eksempel, der vises her, bruger handlingen **Ændring af lagerstatus** på siden **Disponibel efter lokation**.

<table>
<thead>
<tr>
<th>Vigtig opsætningsparameter</th>
<th>Batchantal er tilgængeligt</th>
<th>Vigtige brugertrin</th>
<th>Lagerstedsarbejde</th>
<th>Ordrebekræftet batchreservation</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Under fanen <strong>Lagersted</strong> i posten <strong>Lagersted</strong> er feltet <strong>Fjern reservationer og afmærkninger</strong> angivet til <strong>Reservationer</strong> eller <strong>Afmærkninger og reservationer</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Vælg en bestemt lokation.</li>
<li>Vælg en linje med en bestemt vare, lokation og id (hvis lokationen er id-styret).</li>
<li>Vælg <strong>Ændring af lagerstatus</strong>.</li>
<li>Angiv feltet <strong>Lagerstatus</strong> til <strong>Blokering</strong>.</li>
</ol>
</td>
<td>Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</td>
<td>
<ul>
<li>Antallet reserveres igen for samme batch. Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</li>
<li>To lagertransaktioner af typen <strong>Ændring af lagerstatus</strong> type oprettes for at repræsentere ændringen i lagerstatusdimensionen.</li>
<li>Der oprettes en lagertransaktion af typen <strong>Lagerblokering</strong> og afgangstypen <strong>Reserveret fysisk</strong> oprettes for at repræsentere reservationen af det blokerede antal.</li>
</ul>
</td>
</tr>
<tr>
<td>Nr.</td>
<td>Se den forrige række.</td>
<td>Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</td>
<td>
<ul>
<li>Reservationen fjernes.</li>
<li>To lagertransaktioner af typen <strong>Ændring af lagerstatus</strong> type oprettes for at repræsentere ændringen i lagerstatusdimensionen.</li>
<li>Der oprettes en lagertransaktion af typen <strong>Lagerblokering</strong> og afgangstypen <strong>Reserveret fysisk</strong> oprettes for at repræsentere reservationen af det blokerede antal.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>Under fanen <strong>Lagersted</strong> i posten <strong>Lagersted</strong> er feltet <strong>Fjern reservationer og afmærkninger</strong> angivet til <strong>Ingen</strong>.</td>
<td>Ja</td>
<td>
<ol>
<li>Vælg en bestemt lokation.</li>
<li>Vælg en linje med en bestemt vare, lokation og id (hvis lokationen er id-styret).</li>
<li>Vælg <strong>Ændring af lagerstatus</strong>.</li>
<li>Angiv feltet <strong>Lagerstatus</strong> til <strong>Blokering</strong>.</li>
</ol>
</td>
<td>Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</td>
<td>Antallet reserveres igen for samme batch. Systemet tildeler tilfældigt en lokation og et id (hvis lokationen er id-styret), hvor antallet er tilgængeligt.</td>
</tr>
<tr>
<td>Nr.</td>
<td>Se den forrige række.</td>
<td>Ændringer i lagerstatus er ikke tilladt for antal, der er reserveret til arbejde.</td>
<td>Ændringer i lagerstatus er ikke tilladt.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Begrænsninger

- Reservationsfunktionaliteten for fleksibel dimension for lagerstedsniveau understøtter ikke følgende funktioner:

    - Styring af fastvægt
    - Fysisk negativt lager
    - Reservation i forhold til bestilt forsyning
    - Flytteordrer og pluk af råvarer

- Der er begrænsninger for containerkonsolideringsreglen for pakning efter vejledningsenhed. I forbindelse med ordrebekræftede reservationer anbefales det, at du ikke bruger skabeloner til containerbuild, hvor feltet **Pakning efter vejledningsenhed** er aktiveret. I det aktuelle design bruges lokationsvejledninger ikke, når der oprettes lagerstedsarbejde. Derfor er det kun den laveste enhed i enhedsseriegruppen (lagerenheden), der anvendes under containeriseringsbølgetrinnet.
