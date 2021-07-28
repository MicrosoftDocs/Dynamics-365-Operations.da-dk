---
title: Reservationspolitik for fleksibel dimension for lagerstedsniveau
description: I dette emne beskrives politikken for lagerreservation, hvor virksomheder, der sælger batchsporede produkter og kører deres logistik som WMS-aktiverede operationer, kan reservere bestemte batches for kundesalgsordrer, selvom det reservationshierarki, der er tilknyttet produkterne, ikke tillader reservation af bestemte batches.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eca0b61e1fa6760bfed1a9f9979deddccf6fb1a5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343768"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Fleksibel reservationspolitik for dimension på lagerstedsniveau

[!include [banner](../includes/banner.md)]

Når et lagerreservationshierarki af typen *Batch under\[lokation\]* er knyttet til produkter, kan virksomheder, der sælger batchsporede produkter og kører logistik som handlinger, der er aktiveret for Microsoft Dynamics 365 Warehouse Management System (WMS), ikke reservere bestemte batches af de pågældende produkter til kundesalgsordrer.

På samme måde kan specifikke id'er ikke reserveres til produkter i salgsordrer, når disse produkter er knyttet til standardreservationshierarkiet.

Dette emne beskriver den politik for lagerreservation, der giver disse virksomheder mulighed for at reservere bestemte batches eller id'er, selv når produkterne er knyttet til et reservationshierarki af typen *Batch under\[lokation\]*.

## <a name="inventory-reservation-hierarchy"></a>Lagerreservationshierarki

I dette afsnit opsummeres det eksisterende lagerreservationshierarki.

Lagerreservationshierarkiet bestemmer, at behovsrækkefølgen i forbindelse med lagringsdimensioner indeholder de obligatoriske dimensioner for lokation, lagersted og lagerstatus. Det vil sige, at de obligatoriske dimensioner alle er dimensioner over lokationsdimensionen i reservationshierarkiet, mens lagerstedslogikken er ansvarlig for at tildele en lokation til de ønskede antal og reservere lokationen. I interaktionerne mellem behovsordren og lagerstedsoperationerne forventes det med andre ord, at behovsordren angiver, hvor ordren skal afsendes fra (dvs. sted og lagersted). Lagerstedet er derefter afhængig af logikken for at finde det påkrævede antal på lagerstedet.

For at afspejle den operationelle model for virksomheden er sporingsdimensionerne (batch- og serienumre) dog underlagt større fleksibilitet. Et lagerreservationshierarki kan tage højde for scenarier, hvor følgende betingelser gælder:

- Virksomheden er afhængig af sin lagerdrift for at administrere plukning af antal, der har batch- eller serienumre, *efter* at antallene er fundet på lagerpladsen i lagerstedet. Denne model kaldes ofte *Batch under\[lokation\]* eller *Serie under\[lokation\]*. Den bruges typisk, når et produkts batch- eller serienummeridentifikation ikke er vigtig for de kunder, der placerer efterspørgslen hos den sælgende virksomhed.
- Virksomheden er afhængig af sin lagerdrift for at administrere plukning af antal, der har batch- eller serienumre, *før* at antallene er fundet på lagerpladsen i lagerstedet. Hvis batch- eller serienumre er en nødvendig del af en kundes ordrespecifikation, registreres de i behovsordren, og den lagerdrift, der finder antallet på lagerstedet, kan ikke ændre dem. Denne model kaldes ofte *Batch over\[lokation\]* eller *Serie over\[lokation\]*. Da dimensionerne over lokationen er de specifikke krav i forbindelse med de behov, der skal opfyldes, tildeles de ikke i lagerstedslogikken. Disse dimensioner **skal** altid angives på behovsordren eller i de tilknyttede reservationer.

I disse scenarier er udfordringen, at der kun kan tildeles ét lagerreservationshierarki til hvert frigivet produkt. For at WMS kan håndtere sporede varer, efter at hierarkitildelingen bestemmer, hvornår batch- eller serienummeret skal reserveres (enten når behovsordren udtages eller under pluk på lagerstedet), kan denne tidsindstilling ikke ændres på ad hoc-basis.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Fleksibel reservation for batchsporede varer

### <a name="business-scenario"></a>Forretningsscenarie

I dette scenario bruger et firma en lagerstrategi, hvor færdigvarer spores efter batchnumre. Dette firma bruger også WMS-arbejdsbyrden. Da denne arbejdsbyrde har en veludviklet logik til planlægning og kørsel af lagerstedspluk- og forsendelsesoperationer for batchaktiverede varer, er de fleste af de færdige varer knyttet til et lagerreservationshierarki af typen *Batch under\[lokation\]*. Fordelen ved denne type driftsopsætning er, at beslutninger (der rent faktisk er reservationsbeslutninger) om, hvilke batches der skal plukkes, og hvor de skal placeres på lagerstedet, udskydes, indtil lagerstedsplukoperationerne er startet. De foretages ikke, når kundeordren afgives.

Selvom reservationshierarkiet *Batch under\[lokation\]* fungerer godt for firmaets forretningsmål, kræver mange af firmaets etablerede kunder samme batch, som de tidligere har købt, når de genbestiller produkter. Derfor vil firmaet søge efter fleksibilitet i den måde, som reglerne for batchreservation håndteres på, så der sker følgende, afhængigt af kundernes behov for den samme vare:

- Et batchnummer kan registreres og reserveres, når ordren udtages af salgsbehandleren, og det kan ikke ændres under lagerdrift og/eller udtages af andre behov. Denne funktionsmåde er en hjælp til at sikre, at det batchnummer, der blev bestilt, sendes til kunden.
- Hvis batchnummeret ikke er vigtigt for kunden, kan lagerdriften bestemme et batchnummer under pluk, efter salgsordreregistrering og reservation er udført.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Tilladelse af reservation af en bestemt batch i salgsordren

For at give plads til den ønskede fleksibilitet i batchreservationens funktionsmåde for varer, der er knyttet til et lagerreservationshierarki af typen *Batch under\[lokation\]*, skal lagerstyringen markere afkrydsningsfeltet **Tillad reservation i behovsordre** for niveauet **Batchnummer** på siden **Lagerreservationshierarkier**.

![Angivelse af fleksibelt lagerreservationshierarki.](media/Flexible-inventory-reservation-hierarchy.png)

Når niveauet **Batchnummer** i hierarkiet vælges, vil alle dimensioner over dette niveau og op gennem niveauet **Lokation** automatisk blive valgt. (Som standard er alle dimensioner over niveauet **Lokation** niveauet forudvalgt). Denne funktionsmåde afspejler den logik, hvor alle dimensioner i intervallet mellem batchnummeret og lokationen også reserveres automatisk, når du reserverer et bestemt batchnummer på ordrelinjen.

> [!NOTE]
> Afkrydsningsfeltet **Tillad reservation i behovsordre** gælder kun for reservationshierarkiniveauer, der er ligger under lagerstedets lokationsdimension.
>
> **Batchnummer** og **id** er de eneste niveauer i hierarkiet, der er åbne for den fleksible reservationspolitik. Du kan med andre ord ikke markere afkrydsningsfeltet **Tillad reservation i behovsordre** for niveauet **Lokation** eller **Serienummer**.
>
> Hvis reservationshierarkiet indeholder serienummerdimensionen (der altid skal være under niveauet **Batchnummer**), og hvis du har aktiveret batchspecifik reservation for batchnummeret, fortsætter systemet med at håndtere serienummerreservation og plukoperationer baseret på de regler, der gælder for reservationspolitikken *Serie under\[lokation\]*.

Du kan på et hvilket som helst tidspunkt tillade batchspecifik reservation for et eksisterende reservationshierarki af typen *Batch under\[lokation\]* i din installation. Denne ændring påvirker ikke reservationer og åbent lagerstedsarbejde, der er oprettet, før ændringen blev foretaget. Det er dog ikke muligt at fjerne markeringen af afkrydsningsfeltet **Tillad reservation i behovsordre**, hvis der findes lagertransaktioner af afgangstypen **Reserveret bestilt**, **Reserveret fysisk** eller **Bestilt** for en eller flere varer, der er tilknyttet det pågældende reservationshierarki.

> [!NOTE]
> Hvis en vares eksisterende reservationshierarki ikke tillader batchspecifikation i ordren, kan du igen tildele det til et reservationshierarki, der tillader batchspecifikation, forudsat at strukturen i hierarkiniveauet er den samme i begge hierarkier. Brug funktionen **Skift reservationshierarki til varer** til at udføre omfordelingen. Denne ændring kan være relevant, når du vil forhindre fleksibel batchreservation af et undersæt af batchsporede varer, men tillade den for resten af produktsortimentet.

Hvis du ikke vil reservere et bestemt batchnummer for varen på en ordrelinje, så gælder standardlogikken for lagerdrift, der er gældende for et reservationshierarki af typen *Batch under\[lokation\]*, stadig, uanset om du har markeret afkrydsningsfeltet **Tillad reservation i behovsordre**.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Reservere et bestemt batchnummer til en kundeordre

Efter en batchsporet vares lagerreservationshierarki af typen *Batch under\[lokation\]* er konfigureret til at tillade reservation af bestemte batchnumre i salgsordrer, kan salgsordrebehandlere udtage kundeordrer på samme vare på en af følgende måder afhængigt af kundens anmodning:

- **Angiv ordredetaljer uden at angive et batchnummer** – denne tilgang skal bruges, når produktets batchspecifikation ikke er vigtig for kunden. Alle eksisterende processer, der er knyttet til håndtering af en ordre af denne type i systemet, ændres ikke. Der kræves ingen yderligere overvejelser fra brugernes side.
- **Angiv ordredetaljer, og reservér et bestemt batchnummer** – denne tilgang skal bruges, når kunden anmoder om en bestemt batch. Kunderne anmoder typisk om en bestemt batch, når de genbestiller et produkt, som de tidligere har købt. Denne type batchspecifik reservation er en såkaldt *ordrebekræftet reservation*.

Følgende regelsæt er gældende, når antal behandles, og et batchnummer bekræftes for en bestemt ordre:

- Hvis der skal kunne foretages reservation af et bestemt batchnummer for en vare i henhold til reservationspolitikken *Batch under\[lokation\]*, skal systemet reservere alle dimensioner til og med lokation. Dette område omfatter typisk id-dimensionen.
- Lokationsvejledninger bruges ikke, når der oprettes plukarbejde for en salgslinje, hvor der bruges ordrebekræftet batchreservation.
- Hverken brugeren eller systemet må ændre batchnummeret under lagerstedsbehandling af arbejde for ordrebekræftede batches. (Denne behandling omfatter undtagelseshåndtering).

I følgende eksempel vises slutpunkt-til-slutpunkt-flowet.

## <a name="example-scenario-batch-number-allocation"></a>Eksempel på scenario: batchnummertildeling

I dette eksempel skal du have installeret demodata, og du skal bruge demodatafirmaet **USMF**.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a>Opret et lagerreservationshierarki for at tillade batchspecifik reservation

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

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a>Indtast oplysninger om salgsordrer

1. Gå til **Salg og marketing** \> **Salgsordrer** \> **Alle salgsordrer**.
2. Vælg **Ny**.
3. Angiv **US-003** i feltet **Debitorkonto** i salgsordrehovedet.
4. Tilføj en linje for den nye vare, og angiv **10** som antal. Sørg for, at feltet **Lagersted** er angivet til **24**.
5. Vælg **Lager** i oversigtspanelet **Salgsordrelinjer**, og vælg derefter **Batchreservation** i gruppen **Vedligehold**. På siden **Batchreservation** vises en liste over batches, der er tilgængelige til reservation for ordrelinjen. I dette eksempel vises antallet **20** for batchnummer **B11** og antallet **10** for batchnummer **B22**. Bemærk, at der ikke kan opnås adgang til siden **Batchreservation** fra en linje, hvis varen på linjen er tilknyttet reservationshierarkiet *Batch under\[lokation\]*, medmindre den er konfigureret til at tillade batchspecifik reservation.

    > [!NOTE]
    > Hvis du vil reservere et bestemt batch til en salgsordre, skal du bruge siden **Batchreservation**.
    >
    > Hvis du angiver batchnummeret direkte på salgsordrelinjen, fungerer systemet, som om du har angivet en bestemt batchværdi for en vare, der er underlagt reservationspolitikken *Batch under\[lokation\]*. Når du gemmer linjen, vil du modtage en advarselsmeddelelse. Hvis du bekræfter, at batchnummeret skal angives direkte på ordrelinjen, håndteres linjen ikke af den almindelige lokationsstyringslogik.
    >
    > Hvis du reserverer antallet fra siden **Reservation**, reserveres der ikke noget bestemt batch, og udførelsen af lagerdrift for linjen følger de regler, der gælder i henhold til reservationspolitikken *Batch under\[lokation\]*.

    Generelt er funktionen og interaktionen med denne side meget lig den måde, der arbejdes og interageres med varer, som har et tilknyttet reservationshierarki af typen *Batch over\[lokation\]*. Der gælder dog følgende undtagelser:

    - Oversigtspanelet **Batchnumre bundet til kildelinje** viser de batchnumre, der er reserveret til ordrelinjen. Batchværdierne i gitteret vises under hele udførelsescyklussen for ordrelinjen, herunder lagerstedets behandlingsstadier. Derimod vises der i oversigtspanelet **Oversigt** en almindelig ordrelinjereservation (dvs. reservation, der udføres for dimensionerne over niveauet **Lokation**) i gitteret op til det punkt, hvor der oprettes lagerstedsarbejde. Arbejdsenheden overtager derefter linjereservationen, og linjereservationen vises ikke længere på siden. Oversigtspanelet **Batchnumre bundet til kildelinje** sikrer, at salgsordrebehandleren kan få vist de batchnumre, der er bundet til kundens ordre på et tidspunkt i løbet livscyklussen op til og med fakturering.
    - Ud over at reservere en bestemt batch kan en bruger manuelt vælge batchens specifikke lokation og id i stedet for at lade systemet vælge dem automatisk. Denne funktion er relateret til designet af den ordrebekræftede batchreservationsmekanisme. Når et batchnummer reserveres for en vare i henhold til reservationspolitikken *Batch under\[lokation\]*, skal systemet som tidligere nævnt reservere alle dimensioner til og med lokation. Lagerstedsarbejdet vil derfor indeholde de samme lagringsdimensioner, der blev reserveret af de brugere, der har arbejdet med ordrerne, og de repræsenterer muligvis ikke altid den varelagringsplacering, der er praktisk eller endda mulig for plukoperationer. Hvis ordrebehandlere er opmærksomme på lagerbegrænsningerne, kan det være en god ide manuelt at vælge de specifikke lokationer og id'er, når de reserverer en batch. I dette tilfælde skal brugeren bruge funktionen **Vis dimensioner** i sidehovedet og tilføje lokationen og id'et i gitteret i oversigtspanelet **Oversigt**.

6. På siden **Batchreservation** skal du vælge linjen for batch **B11** og derefter vælge **Reserver linje**. Der er ingen foruddefineret logik ved tildeling af lokationer og id'er under automatisk reservation. Du kan angive antallet manuelt i feltet **Reservation**. Bemærk, at oversigtspanelet **Batchnumre bundet til kildelinje**, batch **B11** er vist som **Bindende**.

    ![Tilknytning af et bestemt batchnummer til en salgsordrelinje på siden Batchreservation.](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Reservation af antallet i en salgsordrelinje kan udføres på tværs af flere batches. På samme måde kan reservation af samme batch udføres mod flere lokationer og id'er (hvis der er aktiveret id'er for lokationerne).
    >
    > Reservation af en bestemt batch for antallet på en salgsordrelinje kan også være delvis. Det samlede antal på 100 enheder kan f.eks. reserveres, så en bestemt batch bekræftes til 20 enheder, hvorimod 80 enheder er reserveret på lokations- og lagerstedsniveauer for alle tilgængelige batches. I dette tilfælde vil WMS håndtere plukoperationer ved hjælp af to separate arbejdslinjer.

7. Gå til **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**. Vælg din vare, og vælg derefter **Styr lager** \> **Vis** \> **Transaktioner**.

    ![Ordrebekræftet reservation som en lagertransaktionstype.](media/Inventory-transactions-for-order-committed-reservation.png)

8. Gennemse varens lagertransaktioner, der er relateret til reservationen af salgsordrelinjen.

    - En transaktion, hvor feltet **Reference** er angivet til **Salgsordre**, og feltet **Afgang** er angivet til **Reserveret fysisk**, repræsenterer ordrelinjereservationen for lagerdimensionerne over niveauet **Lokation**. Ifølge varens lagerreservationshierarki er disse dimensioner lokation, lagersted og lagerstatus.
    - En transaktion, hvor feltet **Reference** er angivet til **Ordrebekræftet reservation**, og feltet **Afgang** er angivet til **Reserveret fysisk**, repræsenterer ordrelinjereservationen for den specifikke batch og alle lagerdimensionerne over den. Ifølge varens lagerreservationshierarki er disse dimensioner batchnummer og lokation. I dette eksempel er lokationen **Bulk-001**.

9. Vælg **Lagersted** \> **Handlinger** \> **Frigiv til lagersted** i salgsordrehovedet. Ordrelinjen er nu i bølge, og der oprettes en belastning og et arbejde.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Gennemse og behandl lagerstedsarbejde, der har ordrebekræftede batchnumre

1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Lagersted** \> **Arbejdsdetaljer**.

    Det arbejde, der håndterer plukoperationen for batchantal, der er bundet til salgsordrelinjen, har følgende karakteristika:

    - For at kunne oprette arbejde bruger systemet arbejdsskabeloner, men ikke lokationsvejledninger. Alle de standardindstillinger, der er defineret for arbejdsskabeloner, f.eks. det maksimale antal pluklinjer eller en bestemt måleenhed, vil blive anvendt til at bestemme, hvornår der skal oprettes nyt arbejde. De regler, der er knyttet til lokationsvejledninger til identifikation af pluklokationer, tages dog ikke i betragtning, fordi den ordrebekræftede reservation allerede angiver alle lagerdimensionerne. Disse lagerdimensioner omfatter dimensionerne på lagerstedets lagerniveau. Derfor arver arbejdet disse dimensioner, uden at lokationsvejledninger skal benyttes.
    - Batchnummeret vises ikke på pluklinjen (som det er tilfældet for den arbejdslinje, der er oprettet for en vare, der har et tilknyttet reservationshierarki for *Batch over\[lokation\]*). I stedet vises batchnummeret "fra" og alle andre lagringsdimensioner i arbejdslinjens lagertransaktion, der refereres til fra de tilknyttede lagertransaktioner.

        ![Lagersteds lagertransaktion for arbejde, der stammer fra ordrebekræftet reservation.](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Når arbejdet er oprettet, fjernes varens lagertransaktion, hvor feltet **Reference** er angivet til **Ordrebekræftet reservation**. Lagertransaktionen, hvor feltet **Reference** er angivet til **Arbejde**, indeholder nu den fysiske reservation af lagerdimensionerne for alle antal.

        Lagerdrift kan fortsætte med at håndtere udførelsen af arbejdet på sædvanlig vis. Vejledningen på mobilenheden giver dog arbejderen besked på at vælge et bestemt batchnummer. I lagermiljøer med id-styrede lokationer kan en arbejder, når vedkommende når en lokation, der gemmer samme batch med flere id'er, plukke fra et hvilket som helst id, der ikke allerede er reserveret (f.eks. af en anden ordrebekræftet reservation eller arbejde, der stammer fra en reservation af den pågældende type).

        Hvis det bliver for upraktisk at plukke fra den lokation, der er angivet på arbejdslinjen, kan lageroperatøren bruge en af følgende handlinger til at omdirigere plukning af den specifikke batch fra en mere praktisk lokation:

        - Standardhandlingen **Tilsidesæt lokation** på en mobilenhed (hvis lagermedarbejderens indstilling **Tillad tilsidesættelse af pluklokation** er aktiveret)
        - Handlingen **Skift lokation** på siden **Arbejdslistedetaljer**. 

2. Udfør plukning og placering af arbejdet på mobilenheden.

    Antallet **10** for batchnummer **B11** plukkes nu for salgsordrelinjen og placeres på lokationen **Baydoor**. På dette tidspunkt er det klar til at blive læsset på lastbilen og sendt til kundens adresse.

## <a name="flexible-license-plate-reservation"></a>Fleksibel reservation af id

### <a name="business-scenario"></a>Forretningsscenarie

I dette scenario bruger en virksomhed lokationsstyring og arbejdsbehandling og håndterer lastplanlægning på niveauet for individuelle paller/containere uden for Supply Chain Management, før arbejdet oprettes. Disse containere repræsenteres ved id'er i lagerdimensionerne. For denne fremgangsmåde skal bestemte id'er derfor forhåndstildeles salgsordrelinjer, før der udføres plukarbejde. Virksomheden søger efter fleksibilitet i den måde, hvorpå reglerne for id-reservation håndteres, så følgende funktionsmåder finder sted:

- Et id kan registreres og reserveres, når ordren udtages af salgsbehandleren, og det kan ikke ændres af andre behov. Denne funktionsmåde er en hjælp til at sikre, at det id, der blev planlagt, sendes til kunden.
- Hvis id'et ikke allerede er tilknyttet en salgsordrelinje, kan lagermedarbejderne vælge et id under plukarbejdet, når salgsordreregistrering og -reservation er fuldført.

### <a name="turn-on-flexible-license-plate-reservation"></a>Aktivere fleksibel reservation af id

Før du kan bruge fleksibel reservation af id, skal to funktioner være aktiveret i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere statussen for funktionerne og aktivere dem, hvis de skal bruges. Du skal aktivere funktionerne i følgende rækkefølge:

1. **Funktionsnavn:** *Fleksibel reservation for dimension på lagerstedsniveau*
1. **Funktionsnavn:** *Fleksibel reservation af ordrebekræftet id*

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a>Reservere et bestemt id på salgsordren

Hvis du vil aktivere reservation af id på en ordre, skal du markere afkrydsningsfeltet **Tillad reservation på behovsordre** for niveauet **Id** på siden **Lagerreservationshierarkier** for det hierarki, der er knyttet til den relevante vare.

![Siden med lagerreservationshierarkier for et fleksibelt id-reservationshierarki.](media/Flexible-LP-reservation-hierarchy.png)

Du kan aktivere id-reservation på ordren på et hvilket som helst tidspunkt i din installation. Denne ændring påvirker ikke reservationer eller åbent lagerstedsarbejde, der er oprettet, før ændringen blev foretaget. Det er dog ikke muligt at fjerne markeringen af afkrydsningsfeltet **Tillad reservation i behovsordre**, hvis der findes åbne udgående lagertransaktioner med afgangsstatus *I bestilling*, *Reserveret bestilt* eller *Reserveret fysisk* for en eller flere varer, der er tilknyttet det pågældende reservationshierarki.

Selvom afkrydsningsfeltet **Tillad reservation ved behovsordre** er markeret for niveauet **Id**, er det stadig muligt *ikke* at reservere et bestemt id i ordren. I dette tilfælde gælder den standardlagerlogik for lagerstedsoperationer, der er gyldig for reservationshierarkiet.

Hvis du vil reservere en bestemt nummerplade, skal du bruge en [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) som proces. I programmet kan du foretage denne reservation direkte fra en salgsordre ved at bruge indstillingen **Ordrebekræftede reservationer pr. id** til kommandoen **Åbn i Excel**. I de enhedsdata, der åbnes i tilføjelsesprogrammet til Excel, skal du angive følgende reservationsrelaterede data og derefter vælge **Publicer** for at sende dataene tilbage til Supply Chain Management:

- Reference (kun *Salgsordre*-værdien understøttes).
- Ordrenummer (værdien kan afledes af partiet).
- Parti-id
- Nummerplade
- Kvantitet

Hvis du skal reservere et bestemt id for en vare med en batchsporing, skal du bruge siden **Batchreservation** som beskrevet i afsnittet [Angive oplysninger om salgsordre](#sales-order-details).

Når den salgsordrelinje, der bruger en ordrebekræftet reservation af id, behandles af lagerstedshandlinger, bruges lokationsdirektiver ikke.

Hvis et lagersteds arbejdselement består af linjer, der svarer til en hel palle og har id-bekræftede antal, kan du optimere plukprocessen ved hjælp af et menupunkt i en mobilenhed, hvor indstillingen **Håndter efter id** er angivet til *Ja*. En lagermedarbejder kan derefter scanne et id for at fuldføre et pluk i stedet for at skulle scanne varerne fra arbejdet én efter én.

![Menupunktet i mobilenheden, hvor indstillingen Håndter efter id er angivet til Ja.](media/Handle-by-LP-menu-item.png)

Da funktionen **Håndter efter id** ikke understøtter arbejde, der dækker flere paller, er det bedre at have et separat arbejdselement til forskellige id'er. Hvis du vil bruge denne fremgangsmåde, skal du tilføje feltet **Ordre bekræftet id** som en arbejdshovedpause på siden **Arbejdsskabelon**.

> [!NOTE]
> For den ordrebekræftede arbejdsoprettelsesproces tildeles en værdi for "ordrebekræftet lagerdimension" til pluklinjerne, og der vil ikke være mulighed for at få vist id-værdien direkte. Kun *Brugerstyret*-proces understøttes, når du konfigurerer et menupunkt i mobilenheder.

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a>Eksempel på scenario: oprette og behandle en ordrebekræftet id-reservation

Dette scenario viser, hvordan du kan oprette og behandle en ordrebekræftet id-reservation.

### <a name="make-demo-data-available"></a>Gøre demodata tilgængelige

Dette scenario indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er leveret til Supply Chain Management. Hvis du vil arbejde gennem scenariet ved hjælp af de værdier, der vises her, skal du arbejde på et miljø, hvor standarddemodata er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a>Oprette et hierarki for lagerreservationer, der giver mulighed for reservation af id

1. Gå til **Lokationsstyring \> Konfiguration \> Lager \> Reservationshierarki**.
1. Vælg **Ny**.
1. Angiv en værdi i feltet **Navn** (f.eks. *FleksibeltID*).
1. Indtast en beskrivelse i feltet **Beskrivelse** (f.eks. *Fleksibel id-reservation*).
1. Vælg **Batchnummer**, **Serienummer** og **Ejer** på listen **Valgte**.
1. Vælg knappen **Fjern** ![pil tilbage.](media/backward-button.png) For at flytte valgte felter til listen **Tilgængelige**.
1. Vælg **OK**.
1. I rækken med dimensionsniveau for **Id** skal du markere afkrydsningsfeltet **Tillad reservation i behovsordre**. Niveauet **Lokation** vælges automatisk, og du kan ikke fjerne markeringerne i afkrydsningsfeltet for det.
1. Vælg **Gem**.

### <a name="create-two-released-products"></a>Oprette to frigivne produkter

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Nyt frigivet produkt**:

    - **Produktnummer:** *Vare1*
    - **Varenummer:** *Vare1*
    - **Varemodelgruppe:** *FIFO*
    - **Varegruppe:** *Lyd*
    - **Lagringsdimensionsgruppe:** *Ware*
    - **Sporingsdimensionsgruppe:** *Ingen*
    - **Reservationshierarki:** *FleksibeltID*

1. Vælg **OK** for at oprette produktet og lukke dialogboksen.
1. Det nye produkt åbnes. I oversigtspanelet **Lager** skal du i feltet **Enhedsseriegruppe-id** angive *ea*.
1. Gentag de forrige trin for at oprette et andet produkt, der har de samme indstillinger, men angiv felterne **Produktnummer** og **Varenummer** til *Vare2*.
1. I handlingsruden skal du under fanen **Styr lager** i gruppen **Vis** vælge **Disponibel lagerbeholdning**. Vælg derefter **Justering af antal**.
1. Juster den disponible lagerbeholdning af de nye varer som angivet i følgende tabel.

    | Post  | Lagersted | Placering | Nummerplade | Kvantitet |
    |-------|-----------|----------|---------------|----------|
    | Vare1 | 24        | FL-010   | LP01          | 10       |
    | Vare1 | 24        | FL-011   | LP02          | 10       |
    | Vare2 | 24        | FL-010   | LP01          | 5        |
    | Vare2 | 24        | FL-011   | LP02          | 5        |

    > [!NOTE]
    > Du skal oprette de to id'er og bruge lokationer, der giver mulighed for blandede varer, f.eks. *FL-010* og *FL-011*.

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a>Oprette en salgsordre og reservere et bestemt id

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny**.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - **Debitorkonto:** *US-001*
    - **Lagersted:** *24*

1. Vælg **OK** for at lukke dialogboksen **Opret salgsordrer** og åbne den nye salgsordre.
1. I oversigtspanelet **Salgsordrelinjer** skal du tilføje en linje, der har følgende indstillinger:

    - **Varenummer:** *Vare1*
    - **Antal:** *10*

1. Tilføj en anden salgsordrelinje, der har følgende indstillinger:

    - **Varenummer:** *Vare2*
    - **Antal:** *5*

1. Vælg **Gem**.
1. I oversigtspanelet **Linjedetaljer** skal du under fanen **Konfiguration** notere dig **Parti-id**-værdien for hver linje. Disse værdier skal angives under reservation af bestemte id'er.

    > [!NOTE]
    > Hvis du vil reservere et bestemt id, skal du bruge dataenheden **Ordrebekræftede reservationer pr. id**. Hvis du vil reservere et bestemt id for en vare med batchsporing, skal du bruge siden **Batchreservation** som beskrevet i afsnittet [Angive oplysninger om salgsordre](#sales-order-details).
    >
    > Hvis du angiver id'et direkte på salgsordrelinjen og bekræfter det på systemet, bruges behandlingen af lagerstyring ikke for linjen.

1. Vælg **Åbn i Microsoft Office**, vælg **Ordrebekræftede reservationer pr. id**, og download filen.
1. Åbn den downloadede fil i Excel, og vælg **Aktivér redigering** for at aktivere Excel-tilføjelsesprogrammet til at køre.
1. Hvis du kører Excel-tilføjelsesprogrammet for første gang, skal du vælge **Har tillid til dette tilføjelsesprogram**.
1. Hvis du bliver bedt om at logge på, skal du vælge **Log på** og derefter logge på ved hjælp af de samme legitimationsoplysninger, du brugte til at logge på Supply Chain Management.
1. Hvis du vil reservere en vare på et bestemt id, skal du vælge **Ny** i Excel-tilføjelsesprogrammet for at tilføje en reservationslinje og derefter angive følgende værdier:

    - **Parti-id:** Angiv den **Parti-id**-værdi, du har fundet for salgsordrelinjen til *Vare1*.
    - **Id:** *LP02*
    - **ReservedInventoryQuantity:** *10*

1. Vælg **Ny** for at tilføje en anden reservationslinje, og angiv følgende værdier på den:

    - **Parti-id:** Angiv den **Parti-id**-værdi, du har fundet for salgsordrelinjen til *Vare2*.
    - **Id:** *LP02*
    - **ReservedInventoryQuantity:** *5*

1. Vælg **Publicer** i Excel-tilføjelsesprogrammet for at sende dataene tilbage til Supply Chain Management.

    > [!NOTE]
    > Reservationslinjen vises kun i systemet, hvis publiceringen er fuldført uden fejl.

1. Gå tilbage til Supply Chain Management. 
1. Hvis du vil gennemse varens reservation, skal du i oversigtspanelet **Salgsordrelinjer** i menuen **Lager** vælge **Vedligehold \> Reservation**. Bemærk, at for salgsordrelinjen til *Vare1* er lager *10* reserveret, og for salgsordrelinjen til *Vare2* er lager *5* reserveret.
1. Hvis du vil gennemse lagertransaktioner, der er relateret til reservationen af salgsordrelinjen, skal du i oversigtspanelet **Salgsordrelinjer** i menuen **Lager** vælge **Vis \> Transaktioner**. Bemærk, at der er to transaktioner, der er relateret til reservationen: en, hvor **Reference**-feltet er angivet til *Salgsordre*, og en, hvor **Reference**-feltet er angivet til *Ordrebekræftet reservation*.

    > [!NOTE]
    > En transaktion, hvor feltet **Reference** er angivet til *Salgsordre* repræsenterer ordrelinjereservationen for lagerdimensionerne over niveauet **Lokation** (sted, lagersted og lagerstatus). En transaktion, hvor **Reference**-feltet er angivet til *Ordrebekræftet reservation*, repræsenterer ordrelinjereservationen for det specifikke id og den specifikke lokation.

1. Frigiv salgsordren ved i handlingsruden at bruge fanen **Lager**, gruppen **Handlinger** og indstillingen **Frigiv til lagersted**.

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a>Gennemgå og behandle lagerstedsarbejde med ordrebekræftede id'er, der er tildelt

1. Gå til oversigtspanelet **Salgsordrelinjer**, og vælg **Arbejdsdetaljer** i menuen **Lagersted**.

    Når der foretages reservation for et bestemt batch, bruger systemet ikke lokationsdirektiver, når det opretter arbejdet for salgsordren, der bruger id-reservation. Da den ordrebekræftede reservation angiver alle lagerdimensioner, herunder lokationen, skal du ikke bruge lokationsdirektiver, da disse lagerdimensioner kun er angivet i arbejdet. De vises i afsnittet **Fra lagerdimensioner** på siden **Arbejdslagertransaktioner**.

    > [!NOTE]
    > Når arbejdet er oprettet, fjernes varens lagertransaktion, hvor feltet **Reference** er angivet til *Ordrebekræftet reservation*. Lagertransaktionen, hvor feltet **Reference** er angivet til *Arbejde*, indeholder nu den fysiske reservation af lagerdimensionerne for alle antal.

1. På mobilenheden skal du afslutte plukning og placere arbejdet ved hjælp af et menupunkt, hvor afkrydsningsfeltet **Håndter efter id** er markeret.

    > [!NOTE]
    > Med funktionen **Håndter efter id** kan du behandle hele id'et. Hvis du skal behandle en del af id'et, kan du ikke bruge denne funktion.
    >
    > Det anbefales, at du har genereret et separat arbejde for hvert enkelt id. Du kan opnå dette resultat ved at bruge funktionen **Opgaveoverskriften skifter** på siden **Arbejdsskabelon**.

    Id *LP02* plukkes nu til salgsordrelinjer og placeres på lokationen *Lagerport*. På dette tidspunkt er det klar til at blive læsset og sendt til kundens adresse.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Undtagelseshåndtering af lagerstedsarbejde, der har ordrebekræftede batchnumre

Lagerstedsarbejde for plukning af ordrebekræftede batchnumre er underlagt samme standardhåndtering af undtagelser for lagersted og handlinger som almindeligt arbejde. Generelt kan det åbne arbejde eller den åbne arbejdslinje annulleres, den kan afbrydes, fordi en brugerlokation er fuld, den kan være kort plukket, og den kan opdateres på grund af en bevægelse. På samme måde kan den plukkede mængde arbejde, der allerede er udført, reduceres, eller arbejdet kan tilbageføres.

Følgende nøgleregel anvendes til alle disse handlinger af typen undtagelseshåndtering: Det batchnummer, der er reserveret til kunden, kan aldrig erstattes med et andet batchnummer, men lagerdimensionerne (lokation og id) kan ændres via enten en manuel opdatering fra brugerens side eller en automatisk opdatering udført af systemet. Den automatiske opdatering er baseret på den samme tilfældige tildeling af lagringsdimensioner, der anvendes, når en bestemt batch blev reserveret automatisk, men der ikke blev angivet nogen lagerdimensioner.

### <a name="example-scenario"></a>Eksempelscenario

Et eksempel på dette scenario er en situation, hvor tidligere udført arbejde ikke kan plukkes ved hjælp af funktionen **Reducer det antal, der er plukket**. I dette eksempel antages det, at du allerede har udført de trin, der er beskrevet i [Eksempel på scenario: batchnummertildeling](#Example-batch-allocation). Det er en fortsættelse af dette eksempel.

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
<li>Vælg menupunktet <strong>Tilsidesæt lokation</strong> på mobilappen Lokationsstyring, når du starter pluk af arbejde.</li>
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
<td>Ikke anvendelig</td>
</tr>
<tr>
<td>Ingen</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Tilsidesæt lokation</strong> på mobilappen Lokationsstyring, når du starter pluk af arbejde.</li>
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
<td>Ikke anvendelig</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Fuld</strong> på mobilappen Lokationsstyring, når du behandler plukarbejde.</li>
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
<li>Start en flytning på mobilappen Lokationsstyring.</li>
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
<li>Vælg menupunktet <strong>Kort pluk</strong> på mobilappen Lokationsstyring, når du kører plukarbejde.</li>
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
<li>Vælg menupunktet <strong>Kort pluk</strong> på mobilappen Lokationsstyring, når du kører plukarbejde.</li>
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
<li>Vælg menupunktet <strong>Kort pluk</strong> på mobilappen Lokationsstyring, når du kører plukarbejde.</li>
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
<td>Ingen</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Kort pluk</strong> på mobilappen Lokationsstyring, når du kører plukarbejde.</li>
<li>Angiv <strong>0</strong> i feltet <strong>Kort pluk antal</strong> (nul).</li>
<li>I feltet <strong>Årsag</strong> skal du vælge <strong>Kort pluk med manuel omfordeling</strong>.</li>
</ol>
</td>
<td>Handlingen kort pluk mislykkes, og der udløses en fejl.</td>
<td>Ikke relevant</td>
</tr>
<tr>
<td>En arbejdsundtagelse af typen <strong>Kort pluk</strong> er angivet, hvor <strong>Vareomfordeling</strong> = <strong>Manuel</strong>, <strong>Reguler lager</strong> = <strong>Ja</strong>, og <strong>Fjern reservationer</strong> = <strong>Ja</strong>. Derudover er indstillingen <strong>Tillad manuel vareomfordeling</strong> aktiveret for arbejderen.</td>
<td>Ingen</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Kort pluk</strong> på mobilappen Lokationsstyring, når du kører plukarbejde.</li>
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
<td>Ikke anvendelig</td>
<td>
<ol>
<li>Vælg menupunktet <strong>Kort pluk</strong> på mobilappen Lokationsstyring, når du kører plukarbejde.</li>
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

## <a name="see-also"></a>Se også

- [Batchnumre i Lokationsstyring](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [Reservere samme batch for en salgsordre](../sales-marketing/reserve-same-batch-sales-order.md)
- [Plukke den ældste batch på en mobilenhed](pick-oldest-batch.md)
- [Bekræftelse af batch og nummerplade](batch-and-license-plate-confirmation.md)
- [Fejlfinde reservationer i lagerstedsstyring](troubleshoot-warehouse-reservations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]