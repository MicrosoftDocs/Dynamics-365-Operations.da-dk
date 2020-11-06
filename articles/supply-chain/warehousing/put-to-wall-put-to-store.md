---
title: Sæt til væg – læg til butik
description: Dette emne indeholder oplysninger om funktionaliteten Sæt til væg – læg til butik. Denne funktionalitet giver dig mulighed for at håndtere scenarier, hvor du skal konsolidere et produkt til et midlertidig lagring til forpakning, der er baseret på konfigurerbare kriterier. Det er med til at reducere pluktiden, da det giver mulighed for at plukke til en enkelt destinations nummerplade og kan bruge flere læg på lager-placeringer end klyngeplukning.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 12501b90e4b31ec11e3c59784ace9fd9a8b7d934
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017822"
---
# <a name="put-to-wall---put-to-store"></a>Sæt til væg – læg til butik

[!include [banner](../includes/banner.md)]

Funktionaliteten *Sæt til væg – læg til butik* giver dig mulighed for at håndtere scenarier, hvor du skal konsolidere et produkt til midlertidig lagring til forpakning, der er baseret på konfigurerbare kriterier. Da denne funktionalitet giver mulighed for at plukke til en enkelt destinations nummerplade og bruge flere læg på-lager-positioner end klyngepluk, vil firmaer, der afsender til butikker eller håndterer små varer, drage fordel af en formindsket plukperiode.

Arbejdsgangen i denne funktion dirigerer et direkte plukket produkt til en sorteringslokation til distribution i forskellige typer containere. Generelt indeholder hver enkelt sorteringslokation flere sorteringspositioner. Hver enkelt sorteringsposition tildeles efter de kriterier, der er angivet i forretningsprocessen. Typiske kriterier er den endelige destination, forsendelse eller last. Når et produkt ankommer, fordeles det på hver enkelt sorteringsposition, baseret på det antal, der er knyttet til ordren, destinationen, forsendelsen eller lasten. Når en container er fuld eller fuldført, flyttes den til en midlertidig lagringslokation eller et afsendelsessted, hvor der kan håndteres yderligere, afhængigt af forretningsprocessen.

Denne lagerfunktion kaldes også for andre ting, f. eks. læg-på-let og brud åbnes.

## <a name="turn-on-the-outbound-sorting-feature"></a>Aktivere funktionen for udgående sortering

Før du kan bruge funktionaliteten *Sæt til væg – læg til butik* , skal funktionen *Udgående sortering* være aktiveret i systemet. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Udgående sortering*

Funktionen *Udgående sortering* kan bruges sammen med funktionen *Bølgetrinskode for hele organisationen* , hvis den er aktiveret. Du skal også aktivere denne funktion, hvis du vil bruge foruddefinerede koder, der er oprettet i bølgetrinskoder. I arbejdsområdet **Funktionsstyring** vises denne funktion på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Organization wide wave step code*

## <a name="setup"></a>Konfiguration

I denne demonstration bruges standard-Contoso-data og lagerstedet *62*. Nogle tilføjelser, der registreres senere, bruges også.

### <a name="location-type"></a>Lokationstype

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationstyper**.
1. Vælg **Ny** i handlingsruden for at oprette en lokationstype til sortering.
1. Angiv følgende værdier:

    - **Lokationstype:** *SORTER*
    - **Beskrivelse:** *Sorter*

1. Vælg **Gem**.

### <a name="warehouse-management-parameters"></a>Parametre til lokationsstyring

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. Gå til fanen **Generelt** , og angiv feltet **Sorteringslokationstype** til **SORTER** i oversigtspanelet *Lokationstyper*.
1. Vælg **Gem**.

### <a name="location-profile"></a>Lokationsprofil

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.
1. Vælg **Ny** i handlingsruden for at oprette en lokationsprofil for sorteringslokationen.
1. Angiv følgende værdier i overskriften:

    - **Lokationsprofil-id:** *Sorter*
    - **Navn:** *Sorter*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Lokationsformat:** *PAKKE*
    - **Lokationstype:** *SORTER*
    - **Brug sporing af nummerplader:** *Ja*
    - **Tillad blandede varer:** *Ja*
    - **Tillad blandede lagerstatusser:** *Ja*

1. Vælg **Gem**.

### <a name="locations"></a>Lokationer

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationer**.
1. Ryd afkrydsningsfeltet **Generér kontrolcifre for lokation**.
1. I handlingsruden skal du vælge **Ny** og derefter indstille følgende værdier:

    - **Lagersted:** *62*
    - **Lokation:** *Sorter*
    - **Lokationsprofil-id:** *Sorter*

1. Vælg **Gem**.

### <a name="packing-profiles"></a>Pakkeprofiler

1. Gå til **Lokationsstyring \> Konfiguration \> Emballage \> Pakningsprofiler**.
1. I handlingsruden skal du vælge **Ny** og derefter indstille følgende værdier:

    - **Pakkeprofil-id:** *Sorter*
    - **Beskrivelse:** *Sorter*
    - **Politik for containerpakning:** Lad feltet være tomt.
    - **Container-id-tilstand:** *Auto*
    - **Containertype:** *PALLE 48 X 48*
    - **Opret automatisk container ved containerlukning:** Lad feltet være tomt.

1. Vælg **Gem**.

### <a name="wave-step-codes"></a>Bølgetrinskoder

Hvis du har aktiveret funktionen *Bølgetrinskode for hele organisationen* , skal du konfigurere følgende kode.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinkoder**.
1. I handlingsruden skal du vælge **Ny** og derefter indstille følgende værdier:

    - **Kode for bølgetrin:** *Sorter*
    - **Bølgetrinsbeskrivelse:** *Sorter*
    - **Bølgetrinstype:** *Sorteringsskabelon*

1. Vælg **Gem**.

### <a name="outbound-sorting-template"></a>Skabelon til udgående sortering

Sorteringsskabelonen styrer, om der oprettes sorteringspositioner, hvilke kriterier der bruges, og andre attributter for sorteringsprocessen.

1. Gå til **Lokationsstyring \> Konfiguration \> Emballage \> Skabelon til udgående sortering**.
1. Vælg **Ny** i handlingsruden for at oprette en sorteringsskabelon.
1. Angiv følgende værdier i hoveddelen for den nye skabelon:

    - **Id for skabelon til udgående sortering:** *Bølgesortering*
    - **Beskrivelse:** *Bølgesortering*
    - **Type af sorteringsskabelon:** *Bølgebehov*

        Dette felt definerer den proces, som sorteringsskabelonen bruges til. Følgende værdier er tilgængelige:

        - **Bølgebehov** – sorteringsskabelonen bruges til processen *Sæt til væg*. Denne skabelontype bruges til at omgå pakkestationen og behandle lager direkte fra bølgen. Du kan kun bruge denne type, hvis bølgeprocestypen **sortering** er inkluderet i bølgeskabelonen.
        - **Container** – sorteringsskabelonen bruges til processen *Palleopbygning efter pakning*. Denne skabelontype bruges til at behandle containere, der er lukket på den pågældende pakkestation og skal sorteres på paller.

    - **Lagersted:** *62*
    - **Lokation:** *Sorter*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Sorter verifikation:** *Positionsscanning*

        Dette felt definerer den verifikation, der kræves under sorteringen. Følgende værdier er tilgængelige:

        - None
        - Scanning af id
        - Scanning af position

    - **Opret arbejde lukning af position:** *Ja*

        Hvis indstillingen er angivet til *Ja* , når positionen er lukket, oprettes arbejde for at flytte lageret til den endelige afsendelseslokation. Hvis den er indstillet til *Nej* , vil lageret straks blive plukket til ordren, når positionen er lukket.

    - **Positionstildeling:** *Manuel*

        I dette felt defineres typen af positionstildeling. Følgende værdier er tilgængelige:

        - **Manuel** – brugeren skal altid angive, hvilken position lageret skal sorteres til.
        - **Automatisk** – systemet guider automatisk lageret til en position, hvor det kan, baseret på sorteringsskabelonskiftene.

    - **Tildel kriterier for sorteringsposition:** *Brug kun tom position*

        Dette felt styrer, om lageret, der allerede findes på sorteringspositionen, tages højde for, når der tildeles en position til behovet. Følgende værdier er tilgængelige:

        - **Brug kun tom position** – positioner, der allerede har lager tilknyttet, vil blive taget i betragtning
        - **Antag, at position er tom** – alle de varer, der allerede er på positionen, vil blive ignoreret under tildelingen. Alle tilgængelige positioner vil blive brugt.

    - **Kode for bølgetrin:** *Sorter*

        Hvis funktionen *Bølgetrinskode for hele organisationen* er aktiveret, skal bølgetrinskoden *Sortering* også konfigureres i bølgetrinskoder.

    - **Luk automatisk sorteringsposition:** *Ja*

        Hvis denne indstilling er angivet til *Ja* , vil sorteringsplaceringen automatisk blive lukket, når alt det arbejde, der kommer til placeringen, er fuldført.

    - **Antal sorteringspositioner:** *3*

        Dette felt definerer det maksimale antal sorteringspositioner, som systemet opretter.

    - **Sorteringspositionspræfiks:** *SP-*

        Dette felt definerer det præfiks, som systemet tildeler før positionsnummeret.

    - **Luk automatisk pakningsposition:** *Ja*

        Hvis denne indstilling er angivet til *Ja* , pakkes lageret på sorteringsplaceringen i en container, når placeringen lukkes.

    - **Pakkeprofil-id:** *Sorter*

        Dette felt definerer den pakkeprofil, der skal bruges, når sorteringslokationen pakkes i en container.

1. Gå til handlingsruden, og vælg **Rediger forespørgsel** for at angive de kriterier, der bruges til denne sorteringsskabelon.
1. Vælg forespørgselsdialogboksen skal du under fanen **Sortering** vælge **Ny** for at føje en linje og derefter indstille følgende værdier:

    - **Tabel:** *Lastdetaljer*
    - **Afledt tabel:** *Lastdetaljer*
    - **Felt:** *Forsendelses-id*
    - **Søgeretning:** *Stigende*

1. Vælg **OK**.
1. Du kan få vist følgende meddelelse: "Gruppering vil blive nulstillet, vil du fortsætte?" Vælg **Ja**.

    Knappen **Udgående sorteringsskabelonskift** i handlingsruden bliver tilgængelige.

1. I handlingsruden skal du vælge **Udgående sorteringsskabelonskift**.
1. Vælg afkrydsningsfeltet **Gruppér efter felt** for at gruppere efter forsendelses-id.

    Denne indstilling vil oprette én sorteringsposition pr. forsendelse, der er en container i bølgen.

1. Vælg **OK**.

### <a name="wave-process-methods"></a>Metoder til bølgeproces

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.
1. Vælg **Genopret metoder** i handlingsruden.

    Metoden **Sortering** føjes til listen over tilgængelige metoder, og bølgeskabelontypen *Forsendelse* er valgt til den.

### <a name="wave-templates"></a>Bølgeskabeloner

Rediger den bølgeskabelon, der bruges til sortering af bølgebehov.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. I feltet **Bølgeskabelontype** skal du vælge *Forsendelse*.
1. Vælg den eksisterende skabelon **62 Forsendelsesstandard**.
1. Vælg **Rediger** i handlingsruden.
1. I oversigtspanelet **Generelt** skal du foretage følgende ændringer::

    - Angiv indstillingen **Udfør behandling af bølgen ved frigivelse til lagerstedet** til *Nej*.
    - Angiv indstillingen **Tildel til åbne bølger** til *Ja*.

1. Gå til oversigtspanelet **Meoder** , og konfigurer metoden **Sortering** :

    1. I gitteret **Resterende metoder** skal du vælge **Sortering**.
    2. Vælg knappen Højre pil for at flytte **sortering** til gitteret **Valgte metoder**.
    3. I gitteret **Valgte metoder** skal du vælge **sortering**.
    4. Indstil feltet **Bølgetrinskode** til *Sorter*.

1. Vælg **Gem**.

### <a name="mobile-device-menu-items"></a>Menupunkter i mobilenhed

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Navn på menupunkt:** *Sorter*
    - **Titel:** *Sorter*
    - **Tilstand:** *Indirekte*
    - **Brug eksisterende arbejde:** *Nej*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Aktivitetskode:** *Udgående sortering*
    - **Brug proceslinje:** *Ja* (standardværdi)
    - **Id for skabelon til udgående sortering:** *Bølgesortering*

1. Vælg **Gem**.

### <a name="mobile-device-menu"></a>Menu i mobilenhed

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Vælg **Udgående** på listen over menuer.
1. Vælg **Rediger** i handlingsruden.
1. I gitteret **Tilgængelig menuer og menupunkter** skal du finde og vælge menupunktet **Sorter** , du lige har oprettet.
1. Vælg den højre piletast for at flytte **Sorter** til gitteret **Menustruktur**. På denne måde føjer du det menupunktet til menuen **Udgående**.
1. Vælg **Gem**.

### <a name="location-directives"></a>Lokationsvejledninger

Du skal oprette lokationsdirektiver for at styre det arbejde, der oprettes, efter at sorteringen er udført.

1. Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.
1. I feltet **Arbejdsordretype** skal du vælge *Sorteret lagerplukning*.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Sekvens:** *1*
    - **Navn:** *Læg til lagerport*

1. I oversigtspanelet **Lokationsvejledninger** kan du angive følgende værdier:

    - **Arbejdstype:** *Læg på lager*
    - **Lokation:** *6*
    - **Lagersted:** *62*
    - **Vejledningskode:** Lad feltet være tomt.
    - **Flere SKU'er:** *Nej*

1. Vælg **Gem** for at gøre oversigtspanelet **Linjer** tilgængeligt.
1. I oversigtspanelet **Linjer** skal du vælge **Ny** og derefter indstille følgende værdier. Accepter standardværdierne for alle de andre felter.

    - **Løbenummer:** *1*
    - **Fra antal:** *0*
    - **Til antal:** *1000000*

1. Vælg **Gem** for at gøre oversigtspanelet **Handlinger i lokationsvejledning** tilgængeligt.
1. I oversigtspanelet **Handlinger i lokationsvejledninger** skal du vælge **Ny** og derefter indstille følgende værdier: Accepter standardværdierne for alle de andre felter.

    - **Løbenummer:** *1*
    - **Navn:** *Båsedør*

1. Vælg **Gem** for at gøre knappen **Rediger forespørgsel** tilgængelig i oversigtspanelet **Handlinger i lokationsvejledning**.
1. Vælg **Rediger forespørgsel** i oversigtspanelet **Handlinger for lokationsvejledninger**.
1. Gå til dialogboksen til forespørgselseditoren under fanen **Område** , og find den række, hvor feltet **Felt** er indstillet til *Lokation*. Angiv feltet **Kriterier** for denne række til *Lagerport*.
1. Vælg **OK** for at bekræfte redigering.

### <a name="work-classes"></a>Arbejdsklasser

1. Gå til **Lokationsstyring \> Opsætning \> Arbejde \> Arbejdsklasser**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier i overskriften:

    - **Arbejdsklasse-id:** *Sortering*
    - **Beskrivelse:** *Sortering*
    - **Ordretype:** *Sorteret lagerplukning*

1. Vælg **Gem**.

### <a name="work-templates"></a>Arbejdsskabeloner

1. Gå til **Lokationsstyring \> Arbejde \> Arbejdsskabeloner**.
1. I feltet **Arbejdsordretype** skal du vælge *Salgsordrer*.
1. I gitteret skal du vælge arbejdsskabelonen **62 Pluk til pakning**.
1. Vælg **Arbejdshovedpauser** i handlingsruden.
1. Vælg **Rediger** i handlingsruden.
1. På den linje, hvor feltet **feltnavn** er angivet til *Forsendelses-id* , skal du rydde afkrydsningsfeltet **Gruppér efter dette felt**.
1. Vælg **Gem** , og luk derefter dialogboksen **Arbejdshovedpauser**.
1. I feltet **Arbejdsordretype** skal du vælge *Sorteret lagerplukning*.
1. Vælg **Ny** for at oprette en arbejdsskabelon.
1. I sektionen **Oversigt** kan du angive følgende værdier. Accepter standardværdierne for alle de andre felter.

    - **Arbejdsskabelon:** *Sorteret pluk*
    - **Beskrivelse af arbejdsskabelon:** *Sorteret pluk*

1. Vælg **Gem** for at gøre sektionen **Arbejdsskabelondetaljer** tilgængelig.
1. I sektionen **Arbejdsskabelondetaljer** skal du oprette to linjer. Vælg **Ny** , og vælg derefter følgende værdier for linje 1:

    - **Arbejdstype:** *Pluk*
    - **Obligatorisk:** Valgt (= *Ja* )
    - **Arbejdsklasse-id:** *Sortering*

1. Vælg **Ny** igen, og vælg derefter følgende værdier for linje 2:

    - **Arbejdstype:** *Læg på lager*
    - **Obligatorisk:** Valgt (= *Ja* )
    - **Arbejdsklasse-id:** *Sortering*

1. Vælg **Gem**.

## <a name="example-scenario"></a>Eksempelscenario

Dette scenarie simulerer en situation, hvor lagerstedet opbevarer små varer på lokationer og skal pakke dem i kasser, før de leveres, og hvor pakkestationens funktionalitet ikke er korrekt. Medarbejdere plukker ordrer for flere kunder og forskellige adresser samtidigt for at øge plukhastigheden. Når plukningen er fuldført, ankommer arbejderne til sorteringspositionen, hvor de plukkede varer kan sorteres til den rigtige kasse baseret på de krævede kriterier. I dette eksempel bruges forsendelses-id'et til at bestemme det rette felt, da hver forsendelse har en særskilt adresse. Når alle varer fra lasten er pakket og sorteret efter forsendelse, flyttes boksene til det midlertidige lagringsområde og bliver derefter læsset på en lastbil.

Før du starter scenariet, skal du sikre dig, at alle standardlagerfunktioner er konfigureret korrekt for lagerstedet. Standard-Contoso-lagersted *62* bruges til dette formål. Standardkonfigurationer er ikke blevet ændret, ud over hvad der er beskrevet i opsætningen.

### <a name="create-demand"></a>Oprette efterspørgsel

Før du kan få vist funktionaliteten, skal du oprette et behov. I dette scenarie skal du oprette tre salgsordrer for tre forskellige debitorer for at simulere forskellige leveringsadresser. På denne måde kan du oprette tre separate forsendelser.

Før du opretter salgsordrer og forsendelser, skal du sikre, at pluklokationerne har tilstrækkelig lagerbeholdning til alle varerne på ordrerne. Gennemse indstillingerne i lokationsvejledning for at bekræfte de pluklokationer, der skal bruges til salgsordrepluk. Hvis du skal justere lagerbeholdning, kan du oprette manuelle bevægelser, bruge genopfyldning eller anvende en anden proces. Reserver derefter lageret.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette en salgsordre for ordre 1.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre** :

    - **Kunde:** *US-001*
    - **Lagersted:** *62*

1. Vælg **OK**.
1. Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordreordrelinjer**. Angiv følgende værdier:

    - **Varenummer:** *A0001*
    - **Antal:** *5*

1. Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:

    - **Varenummer:** *A0002*
    - **Antal:** *10*

1. Gentag følgende fremgangsmåde for hver salgslinje på ordren for at reservere lager for den:

    1. Gå til oversigtspanelet **Salgsordrelinjer** , og vælg **Reservation** i menuen **Lager**.
    1. På siden **Reservation** skal du vælge **Reserver parti** og derefter lukke siden.
    1. Vælg **Gem**.

1. Vælg **Ny** for at oprette en salgsordre for ordre 2.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre** :

    - **Kunde:** *US-004*
    - **Lagersted:** *62*

1. Vælg **OK**.
1. Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordreordrelinjer**. Angiv følgende værdier:

    - **Varenummer:** *A0001*
    - **Antal:** *7*

1. Vælg **Tilføj linje** for at tilføje en anden linje, og angiv følgende værdier:

    - **Varenummer:** *A0002*
    - **Antal:** *3*

1. Gentag følgende fremgangsmåde for hver salgslinje på ordren for at reservere lager for den:

    1. Gå til oversigtspanelet **Salgsordrelinjer** , og vælg **Reservation** i menuen **Lager**.
    1. På siden **Reservation** skal du vælge **Reserver parti** og derefter lukke siden.
    1. Vælg **Gem**.

1. Vælg **Ny** for at oprette en salgsordre for ordre 3.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre** :

    - **Kunde:** *US-007*
    - **Lagersted:** *62*

1. Vælg **OK**.
1. Der føjes en ny linje til gitteret i oversigtspanelet **Salgsordreordrelinjer**. Angiv følgende værdier:

    - **Varenummer:** *A0001*
    - **Antal:** *8*

1. Følg disse trin for at reservere lager for salgslinjen:

    1. Gå til oversigtspanelet **Salgsordrelinjer** , og vælg **Reservation** i menuen **Lager**.
    1. På siden **Reservation** skal du vælge **Reserver parti** og derefter lukke siden.
    1. Vælg **Gem**.

Gennemfør følgende procedure for at frigive hver salgsordre til lagerstedet. Der vil blive oprettet tre forskellige forsendelser. Du skal derefter tilføje alle tre forsendelser til en ny bølge.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg den første salgsordre, du har oprettet, i gitteret.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    Du modtager en orienterende meddelelse, der viser bølge-id'et og forsendelses-id'et, der blev oprettet.

1. Gentag de forrige trin for at frigive salgsordrer 2 og 3 til lagerstedet. Bemærk, at den oplysningsmeddelelse, du modtager, angiver, at der er føjet en forsendelse til den bølge, der blev oprettet, da du frigav salgsordre 1.
1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg det bølge-id, der er oprettet ud fra frigivelsen af salgsordrerne, for at åbne siden **Bølger**. På denne side vises bølgeoplysningerne. I oversigtspanelet **Bølgelinjer** vises de forsendelser, der er oprettet.

    Du skal nu oprette arbejde for at hente varer fra pluklokationerne til sorteringslokationen.

1. Vælg **Behandl** i handlingsruden.

    Ved bølgebehandling vil sorteringsmetoden bruge sorteringsskabelonen til at tildele lageret til sorteringspositioner. Når bølgebehandling er fuldført, modtager du en orienterende meddelelser, der angiver, at den pågældende bølge er poseret, og at arbejdet er blevet oprettet.

1. I handlingsruden skal du under fanen **Fane** i gruppen **Relaterede oplysninger** vælge **Arbejde** for at få vist det arbejde, der blev oprettet. Notér dig arbejds-id'et.
1. Gå til **Lagerlokation \> Pakning og containerisering \> Positonstildelinger for udgående sortering**.
1. I kolonnen til venstre kan du få vist den udgående sorteringsposition, der er oprettet for de enkelte forsendelser.
1. I oversigtspanelet **Kriterier for sorteringsposition** kan du få vist forsendelses-id'et for den pågældende position.

Der er blevet oprettet et arbejds-id for at hente lageret fra pluklokationerne til sorteringslokationen. Før du kan fuldføre arbejdet, skal du bruge det arbejds-id, der blev oprettet under bølgebehandling.

### <a name="sales-order-picking-to-the-sorting-location"></a>Salgsordrepluk til sorteringslokationen

1. Log på mobilappen som en arbejder på lagerstedet *62*.
1. I hovedmenuen skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **Salgspluk**.
1. Vælg feltet **Id** , og angiv derefter arbejds-id'et fra bølgeprocessen.
1. Bekræft indtastningen.

    Derefter bedes du angive en destinationsnummerplade (NP). Bemærk, at linje 1 fra salgsordre 1 er den, der skal plukkes og føjes til destinationsnummerpladen. Varenummeret, antallet, varebeskrivelsen og pluklokationen vises.

1. I feltet **Mål-NP** skal du angive et nummerplade-id.

    Du skal vælge alle linjer, der er oprettet ud fra den behandlede bølge, på samme nummerplade.

1. Bekræft indtastningen.

    Mobilappen indeholder nu en serie af **Pluk** -sider, der peger på pluklokationen og på varen og det antal, der skal plukkes. Når den plukkede vare føjes til nummerpladen, skal du bekræfte plukarbejdet. Den sidste side er det arbejde, der skal placere de plukkede varer på sorteringslokationen.

1. Bekræft det første plukarbejde.
1. Det næste plukarbejde vises. Bekræft plukningen.
1. Fortsæt for at bekræfte det resterende plukarbejde.
1. Det sidste trin er at fuldføre læg på lager-arbejde. Bekræft læg på lager-aktiviteten til sorteringslokationen.

    Du modtager en meddelelse om, at "arbejde er fuldført".

1. Afslut **Salgsplukning** på mobilappen.

### <a name="sortingput-to-wall"></a>Sortering/sæt til væg

Nu, hvor alt lager er blevet placeret på sorteringslokationen, og at det skal sorteres til den korrekte sorteringsposition.

1. Log på mobilappen.
1. I hovedmenuen skal du vælge **Udgående**.
1. I menuen **Udgående** skal du vælge **Sorter** for at begynde at sortere varerne.
1. I feltet **NP/CON** skal du angive destinationsnummerpladen for det plukkede salgsordrearbejde.
1. Bekræft indtastningen.
1. Angiv det varenummer, der skal sorteres først.
1. Systemet bestemmer den første sorteringsposition, der skal vises. Bekræft sorteringspositionen.
1. Du bliver bedt om at tildele en nummerplade til sorteringspositionen. Vælg feltet **NP** , angiv et id-nummer, og bekræft derefter indtastningen.

    Da sorteringspositionen er relateret til forsendelses-id'et, sorterer du de plukkede varer til en nummerplade, der er specifik for den udgående leverance og salgsordre.

    På næste side vises vare-id, antal, sorteringspositions-id og id-numrene for "fra" (pluk) og "til" (sortering). Oplysningerne på denne side giver dig besked på at sortere den angivne vare og antallet fra pluknummerpladen til sorteringsnummerpladen.

1. Bekræft sorteringspositionen.
1. Sorter varer i den første sorteringsposition. Når du er færdig, sender systemet dig til den næste sorteringsposition.
1. Gentag denne fremgangsmåde for alle plukkede linjer i arbejdsordren. Du skal også bruge denne fremgangsmåde, når der er flere pluklinjer med samme varenummer.

    Efterhånden som du gentager denne proces for alle varer, evaluerer systemet kriterierne fra den næste scannede vare (arbejdslinje) og bestemmer, hvilken sorteringsposition den skal lægges til. Du bliver automatisk bedt om at placere varen på den korrekte sorteringsposition. Afhængigt af bekræftelsesopsætningen bliver du også bedt om at bekræfte denne handling ved at angive positionsnummeret eller id-nummeret.

    > [!NOTE]
    > Hvis automatisk sortering er slået til, er manuel tilsidesættelse ikke tilgængelig.

1. Når du er færdig, skal du i Microsoft Dynamics 365 Supply Chain Management åbne siden **Tildelinger af udgående sorteringsposition** for at gennemse statussen for positionerne.

    - Hvis positionerne lukkes automatisk, skal du vælge **Vis lukkede** for at få vist de lukkede positioner.
    - Bemærk, at transaktioner for sorteringspositioner vises. Varen og det antal, der er behandlet gennem positionen, vises.

    Når du opretter skabelonen for udgående sortering, skal du angive indstillingen til **Luk sorteringsposition automatisk** til *Ja*. Derfor lukkes positionen automatisk, når den sidste forventede lagerbeholdning er sat til den. Sorteringspositionerne er i statussen **Lukket** , og der er oprettet arbejde for at flytte det sorterede lager til lokationen *Lagerport*.

1. Fuldfør det sorterede lagerplukarbejde for at flytte lageret til afsendelsesstedet. Når lageret er klart, skal du sende og bekræfte det.

> [!NOTE]
> I forbindelse med sorteret lagerplukarbejde, der skal behandles korrekt, er der et menupunkt i mobilenheder, der har et arbejdsklasse-id, hvor feltet **Arbejdsordretype** er angivet til *Sorteret lagerpluk* , der skal bruges til flytnings- og læsningsprocessen.

### <a name="manually-close-a-position-optional"></a>Lukke en position manuelt (valgfrit)

Hvis sorteringspositionerne skal lukkes manuelt, skal indstillingen **Luk sorteringsposition automatisk** for skabelon til udgående sortering angives til *Nej* , og lukningen skal foretages, før lageret kan flyttes til lagerportområdet. Positioner kan lukkes på flere forskellige måder:

- Via lagerstedsappen:

    - Brugeren kan scanne en af de varer, der allerede findes på positionen, og derefter vælge **Luk** for at lukke positionen.
    - Hvis brugeren scanner en container, der allerede er sorteret til container, vises en fejlmeddelelse. Brugeren kan dog stadig fortsætte med at lukke positionen.

- På siden **Tildelinger af udgående sorteringsposition** i Microsoft Dynamics 365 Supply Chain Management:

    - Brugeren kan vælge den udgående sorteringspositionspost og derefter vælge **Luk position** i handlingsruden.

## <a name="tips"></a>Tip!

- Varer kan ikke flyttes mellem positioner, når de er blevet tildelt til én. Systemet evaluerer, hvor mange af hver vare der skal gå til en bestemt position.
- Sorteringsskabeloner kan konfigureres til automatisk at oprette containere, når positionerne er lukket. Denne fremgangsmåde opretter en standardcontainer-id-struktur, der er baseret på den angivne pakkeprofil.

> [!IMPORTANT]
> Når der er oprettet et overførselsarbejde ud fra sorteringspositionen, må du ikke annullere arbejdet. Ellers vil positionen og containerne i den blive slettet fra systemet og ikke være tilgængelig til viderebehandling. Lageret vil også blive fjernet.
