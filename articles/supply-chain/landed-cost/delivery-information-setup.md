---
title: Opsætning af leveringsoplysninger
description: Dette emne beskriver, hvordan du konfigurerer leveringsoplysninger for modulet Landingsomkostninger.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a0b510e4f58ca1cfec940093d118618693c68d38
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694677"
---
# <a name="delivery-information-setup"></a>Opsætning af leveringsoplysninger

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer leveringsoplysninger for modulet **Landingsomkostninger**.

## <a name="shipping-ports"></a>Forsendelseshavne

Forsendelseshavne identificerer, hvor varer sendes fra og til. Der defineres en "til"-havn og en "fra"-havn for hver fragtrute på baggrund af den rejse, der er valgt til det pågældende fragtfartøj. Forsendelseshavne bruges til at opbygge etaper af en rejse og også fragtaktiviteterne. De defineres typisk ved hjælp af navnet på den by og det land eller område, hvor den fysiske havn er beliggende.

Du kan arbejde med forsendelseshavne ved at gå til **Landingsomkostninger \> Opsætning af leveringsoplysninger \> Forsendelseshavne**. Her kan du se, tilføje og fjerne poster for dine forsendelseshavne. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Forsendelseshavn | Angiv et entydigt id-navn/-nummer for forsendelseshavnen. |
| Beskrivelse | Angiv en beskrivelse af forsendelseshavnen. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Sporingskontrolcenter

Du kan bruge center for sporingskontrol til at konfigurere leveringstider, statusopdateringer og informationsflow, der er tilknyttet en fragtrute, efterhånden som forsendelsescontainerne flyttes fra den ene etape til den næste. Når du opretter en sporingskontrolpost, er den knyttet til et bestemt etape af en fragtrejse. Når en fragt opdaterer en etape, opdateres den tilknyttede post og udfyldes som defineret. Du kan opdatere sporingsoplysninger for individuelle fragter fra siden **Alle fragter**.

Du kan åbne sporingskontrolcenteret ved at gå til **Landingsomkostninger \> Opsætning af leveringsoplysninger \> Sporingskontrolcenter**.

Sporingskontrolcenteret viser en af tre sidevisninger, afhængigt af den værdi der er valgt i feltet **Opret type** i listeruden: *Blank*, *Leveringstid* eller *Statusopdatering*. Hver enkelt oprettelsestype opdaterer et særskilt sæt oplysninger, der er knyttet til statussen for en fragt fra oprindelsesstedet til den endelige destination.

### <a name="common-rule-settings"></a>Fælles regelindstillinger

Følgende tabel viser de felter, der er tilgængelige for alle tre oprettelsestyper i sporingskontrolcenteret.

| Felt | Beskrivelse |
|---|---|
| Kildetabel, kildefelt | Disse felter identificerer en kildetabel og et felt i databasen. Reglen indlæser værdien i feltet og bruger den derefter på den måde, der er defineret af andre indstillinger for reglen. |
| Måltabel, målfelt | Disse felter identificerer en destinationstabel og et felt i databasen. Reglen indlæser værdien i feltet og bruger den derefter (eller overskriver den) på den måde, der er defineret af andre indstillinger for reglen. |
| Aktivitet | Dette felt identificerer den type aktivitet, der skal anvendes for en forsendelsescontainer, der er matchet af en regel. |
| Matchkriterie | Dette felt bestemmer, hvordan systemet identificerer et match for en regel. I de enkelte forekomster gennemser systemet dataene i kilde- og destinationstabellerne for at finde ud af, om og hvornår et felt skal opdateres i måltabellen.<p>Kildetabellen er f.eks. *Fragter*, og måltabellen er *Indkøbshoved* eller *Indkøbslinjer*. Tabellen *Fragter* har værdien **Fra havn** som *SAR Hongkong*, og tabellen *Indkøbshoved* har **Fra havn**-værdien *Shanghai*. Der oprettes derefter en regel, der har *SAR Hongkong* som "fra"-havn. I dette tilfælde fungerer værdierne i feltet **Matchkriterier** på følgende måde:</p><ul><li>**Begge** – Målfeltet opdateres ikke, da én af de to havne ikke matcher.</li><li>**Kilde** – Målfeltet opdateres, da kildetabellens "fra"-havn er *SAR Hongkong*.</li><li>**Mål** – Målfeltet opdateres ikke, da destinationstabellens "fra"-havn er *Shanghai* (ikke *SAR Hongkong*).</li></ul> |
| Kopiér handling | De tilgængelige værdier er *Kopi* og *Standard*. Vælg *Kopi* for at kopiere værdien i kildefeltet til destinationsfeltet. Vælg *Standard* for at angive en statisk værdi for destinationsfeltet. |
| Standard | Når feltet **Kopier handling** er angivet til *Standard*, definerer feltet **Standard** standardværdien for destinationsfeltet. Hvis handlingen f.eks. er knyttet til en havneopdatering, og feltet **Kopiér handling** er angivet til *Standard*, identificerer feltet **Standard** en havn. |
| Etape | Dette felt identificerer den etape af rejsen, hvor den angivne handling finder sted, f.eks. pålæsning eller told. |
| Tjenesteudbyder | Hvis der bruges en bestemt serviceudbyder til den aktuelle statusopdatering/etape af rejsen, identificerer dette felt serviceudbyderen. Serviceudbydere defineres på kreditorkontoen. |

### <a name="lead-time-rules"></a>Regler for leveringstid

Leveringstiden er den anslåede tid, som en fragt skal bruge på at fuldføre en defineret etape af en rejse for en fragt. Leveringstiden for hver etape af en rejse bruges til at beregne den forventede leveringsdato for fragten. Denne dato angives derefter i feltet **Bekræftet leveringsdato** på alle indkøbslinjer i fragten.

Du kan bruge regler for leveringstid til at administrere opdateringer af datoer. Aktiviteter genereres automatisk, når der bruges en rejseskabelon til en fragt.

Hvis du vil føje regler for leveringstid til sporingskontrolcenteret, skal du følge disse trin.

1. Udfør ét af følgende trin:

    - Gå til **Landingsomkostninger \> Opsætning af rejse i flere etaper \> Etaper**. Vælg den etape, du vil oprette leveringstider for, og vælg derefter **Sporingskontrolcenter** i handlingsruden. Centeret for sporingskontrol er forudindlæst med oplysninger om den valgte etape.
    - Gå til **Landingsomkostninger \> Opsætning af leveringsoplysninger \> Sporingskontrolcenter**. Derefter skal du manuelt vælge en etape i trin 4 af denne procedure.

1. Angiv feltet **Opret type** til *Leveringstid* i listeruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Hvis du startede fra sporingskontrolcenteret i trin 1, skal du indstille feltet **Etape** til den etape, som du vil oprette en leveringstidsregel for. Hvis du startede fra siden **Etaper** er feltet **Etape** forudindstillet til den etape, du valgte, før du åbnede sporingskontrolcenteret.

    Ud fra værdien i feltet **Etape** angives flere felter automatisk som vist her:

    - **Kildetabel:** *Containeraktiviteter*
    - **Kildefelt:** *Startdato*
    - **Måltabel:** *Containeraktiviteter*
    - **Målfelt:** *Forventet slutdato*

1. Vælg den aktivitet i feltet **Aktivitet**, som den aktuelle regel skal gælde for.
1. I feltet **Leveringstid** skal du angive den leveringstid (i dage), der skal anvendes, når den aktuelle regel udløses.

### <a name="status-update-rules"></a>Regler for statusopdatering

Poster, hvor feltet **Opret type** er angivet til *Statusopdatering*, opdaterer statussen for indkøbsordrelinjer eller status på fragt-, forsendelsescontainer- eller folioniveau. Statusserne kan angives uafhængigt. Du kan bruge dem til at informere brugeren eller afdelingen om stadiet for en fragt (f.eks. dokumenter, der er modtaget, eller varer i transit).

Når feltet **Opret type** er angivet til *Statusopdatering*, indeholder sporingskontrolcenteret et oversigtspanel med **Linjer**, hvor du kan definere et omkostningsområde og den opdaterede status for fragten. Du har f.eks. en linje, hvor feltet **Omkostningsområde** er angivet til *Container*, og feltet **Fragtstatus** er angivet til *Varer i transit*. Hvis det er tilfældet, når en ordre fuldfører det angivne etape, opdateres feltet **Fragtstatus** til forsendelsescontaineren til *Varer i transit*.

Statusopdateringer giver statussen for en fragt gennem alle de fragtlinjer og indkøbsordrelinjer, der er tilknyttet denne fragt. Efterhånden som en fragt bevæger sig gennem sin rejse fra havnen, sejladsen og tolden til destinationslagerstedet, viser feltet **Fragtstatus** i fragtposten en hurtig visning af det stadie, varerne er på.

Hvis du vil føje regler for statusopdatering til sporingskontrolcenteret, skal du følge disse trin.

1. Udfør ét af følgende trin:

    - Gå til **Landingsomkostninger \> Opsætning af rejse i flere etaper \> Etaper**. Vælg den etape, du vil oprette en statusopdatering for, og vælg derefter **Sporingskontrolcenter** i handlingsruden. Centeret for sporingskontrol er forudindlæst med oplysninger om den valgte etape.
    - Gå til **Landingsomkostninger \> Opsætning af leveringsoplysninger \> Sporingskontrolcenter**. Derefter skal du manuelt vælge en etape i trin 4 af denne procedure.

1. Angiv feltet **Opret type** til *Statusopdatering* i listeruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Hvis du startede fra sporingskontrolcenteret i trin 1, skal du indstille feltet **Etape** til den etape, som du vil oprette en statusopdatering for. Hvis du startede fra siden **Etaper** er feltet **Etape** forudindstillet til den etape, du valgte, før du åbnede sporingskontrolcenteret.

    Ud fra værdien i feltet **Etape** angives flere felter automatisk som vist her:

    - **Kildetabel:** *Containeraktiviteter*
    - **Kildefelt:** *Faktisk slutdato*
    - **Måltabel:** Dette felt er tomt.
    - **Målfelt:** Dette felt er tomt.

1. Vælg den aktivitet i feltet **Aktivitet**, som din regel skal gælde for.
1. Angiv statusopdateringerne for hvert omkostningsområde i oversigtspanelet **Linjer**.

### <a name="blank-type-rules"></a>Tomme typeregler

Du bruger poster med værdien **Opret type** som *Tom* til at tilsidesætte eller angive en feltværdi baseret på oplysningerne i et andet felt. Et felt fra Landingsomkostninger vil overskrive data i andre områder af Microsoft Dynamics 365 Supply Chain Management på basis af regler, der er konfigureret i sporingskontrolcenteret.

1. Gå til **Landingsomkostninger \> Opsætning af leveringsoplysninger \> Sporingskontrolcenter**.
1. Angiv feltet **Opret type** til *Tom* i listeruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Definer kilde- og destinationsværdier, matchkriterier, kopihandling og andre relevante parametre efter behov for reglen.

### <a name="required-tracking-control-setup"></a>Nødvendig opsætning af sporingskontrol

For hver rejseskabelon skal der konfigureres to poster i sporingskontrolcenteret. Begge disse poster har **Opret type**-værdien *Tom* og bruges i alle implementeringer af landingsomkostninger. De hjælper dig med at sikre, at den bekræftede dato for indkøb og forventede datoer for varer i transit opdateres for fragt og på relaterede indkøbsordrelinjer på den forventede måde.

Den første post skal bruges til opdatering af indkøbslinjer. Den skal angives med følgende indstillinger:

- **Kildetabel:** *Containeraktiviteter*
- **Kildefelt:** *Forventet slutdato*
- **Måltabel:** *Indkøbslinjer*
- **Målfelt:** *Bekræftet eller leveringsdato*

Den anden post er påkrævet for at opdatere varer i transit-transaktioner. Den skal angives med følgende indstillinger:

- **Kildetabel:** *Containeraktiviteter*
- **Kildefelt:** *Forventet slutdato*
- **Måltabel:** *Varer i transitordre*
- **Målfelt:** *Forventet dato*
