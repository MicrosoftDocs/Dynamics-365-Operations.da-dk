---
title: Pakke containere til forsendelse
description: I denne artikel beskrives den pakningsproces, der giver dig mulighed for at validere lagervarer og pakke dem i containere.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 118b1c79d23cd1b5044ede9aa9c469409cd22166
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708777"
---
# <a name="pack-containers-for-shipment"></a>Pakke containere til forsendelse

[!include [banner](../../includes/banner.md)]

Med containerpakningsproces kan du validere lagervarer og pakke dem i containere. I løbet af denne proces plukker lagermedarbejderne typisk lagervarer fra masselagerområder og flytter dem til et pakkeområde. Der er flere lagerarbejdere, der kontrollerer varens antal og typer, og tildeler dem til de relevante containerstørrelser. Når en container er helt pakket, bliver den lukket og flyttet den til forsendelsesområdet, hvor den klargøres til afsendelse.

Containere repræsenterer fysiske strukturer, som varer er pakket i, og du kan spore containeroplysninger i systemet. Disse oplysninger kan være nyttige under transportplanlægning, især hvis du beregner forsendelsesgebyrer baseret på containere. Inden du afsender, kan du få vist antallet af containere, der bruges i en forsendelse, de anvendte containeretyper og de fysiske dimensioner for hver container (f.eks. den samlede volumen og vægt).

Flere relaterede udgående lagerstedsegenskaber kan bruges sammen med containere. Du kan finde flere oplysninger i følgende artikler:

- [Bølgecontainerisering](wave-containerization.md)
- [Udgående sortering](outbound-sorting.md)
- [Forsendelse af småpakker](small-parcel-shipping.md)
- [Bekræft og flyt](confirm-and-transfer.md)
- [Angive forskellige dimensioner for pakning og lagring](packing-vs-storage-dimensions.md)
- [Pakkearbejde til pakning af udgående containere og behandling af forsendelser](packing-work.md)
- [Pakke containere med Warehouse Management-mobilappen](warehouse-app-packing-containers.md)
- [Eksempelscenario – Pakke containere med Warehouse Management-mobilappen](warehouse-app-pack-containers-scenario.md)
- [Udskrive containerlabels](print-container-labels.md)

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Konfigurere lagerstedet til at bruge manuelle pakkehandlinger

Du kan organisere udgående operationer på to grundlæggende måder:

- **Bølgeoprettelse og -behandling** – Arbejdere plukker varer ud fra udgående lagerstedsarbejde. Derefter lægger de varerne direkte på en udgående forsendelseslokation, hvor de er klar til at blive sendt med det samme. Du kan finde oplysninger om konfiguration og brug af denne proces i [Bølgeoprettelse og -behandling](wave-processing.md).
- **Manuel pakning på pakkestationer** – Denne proces har endnu en operation mellem pluk- og forsendelsesoperationerne. I stedet for at placere lageret på en *lagerport som afsendelseslokation*, placerer arbejderne lageret i en *pakkelokation*. Derefter administrerer de pakningsprocessen på pakkestationen ved hjælp af **Pak**-siden i webklienten. Du skal dog først forberede systemet, som det beskrives i dette afsnit.

### <a name="set-up-warehouse-locations-for-packing"></a>Konfigurere lagerstedslokationer til pakning

Du skal have mindst én pakkelokation, hvor arbejdere skal placere lagervarer, så de kan pakkes i containere. Yderligere oplysninger om oprettelse af lagerstedslokationer finder du i [Konfigurere lokationer i et WMS-aktiveret lagersted](tasks\configure-locations-wms-enabled-warehouse.md). I følgende underafsnit beskrives, hvordan du kan oprette og konfigurere pakkelokationer.

#### <a name="set-up-location-types-for-packing"></a>Konfigurere lokationstyper til pakkearbejde

Du skal definere en *lokationstype* for pakkelokationerne. Lokationstyper kan bruges til at filtrere indstillinger for at styre de forskellige lagerstedsstyringsprocesser. Navnet på hver lokationstype beskriver typisk noget om, hvordan lokationstypen skal anvendes. Den lokationstype, du konfigurerer her, skal være tilknyttet hver af de lokationer, der bruges til pakkeoperationer.

Følg disse trin for at konfigurere en lokationstype.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationstyper**.
1. I handlingsruden skal du vælge **Ny** for at føje en lokationstype til gitteret.
1. Angiv følgende felter for den nye lokationstype:

    - **Lokationstype** – Angiv et navn til lokationstypen. De enkelte navne skal være entydige og skal beskrive noget om, hvordan lokationstypen er beregnet til brug.
    - **Beskrivelse** – Indtast en kort beskrivelse af lokationstypen.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Oplyse systemet om pakkelokationstypen

Når du har oprettet en lokationstype, skal du konfigurere systemet til at genkende den som den lokationstype, der skal bruges til pakkeoperationer.

Benyt følgende fremgangsmåde for at angive den lokationstype, der bruges til pakkeoperationer.

1. Gå til **Lokationsstyring \> Opsætning \> Parametre til lokationsstyring**.
2. I oversigtspanelet **Lokationstyper** under fanen **Generelt** skal du angive feltet **Pakkelokationstype** til den lokationstype, du vil bruge til at identificere pakkestationer.

> [!NOTE]
> Hvis du opgraderer fra en version af Microsoft Dynamics AX, er status *Under pakning* fjernet fra forsendelser og laster, fordi den ikke fungerer konsistent og forårsagede overflødige data. Derfor er listesiderne **I forsendelser** og **Laster under pakning** udfaset. Containere, der skal pakkes, spores på lokationsniveau.
>
> I tidligere versioner har du defineret pakkelokationen ved hjælp af feltet **Profil-id for pakkelokation** under fanen **Pakning** på siden **Parametre til lokationsstyring** for at angive en *lokationsprofil*. I den aktuelle version bruger du feltet **Pakkelokationstype** under fanen **Generelt** på siden **Parametre til lokationsstyring** til at angive en *lokationstype* som beskrevet i denne artikel. Det nye felt passer bedre til processen til identifikation af midlertidige lokationer og endelige afsendelseslokationer.
>
> Selvom du kan fortsætte med at bruge det gamle felt **Profil-id for pakkelokation**, anbefales det, at du begynder at bruge det nye felt **Pakkelokationstype** i stedet, da det gamle felt til sidst udfases.
>
> Hvis du fjerner markeringen i det gamle felt **Profil-id for pakkelokation** og derefter gemmer siden, deaktiveres feltet permanent. For installationer, hvor feltet **Profil-id for pakkelokation** aldrig har været brugt, vil det altid være deaktiveret. Når du har ryddet indstillingen af feltet **Profil-id for pakkelokation**, skal du bruge de indstillinger, der er beskrevet i denne artikel, til at oprette og identificere din pakkelokation.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Konfigurere lokationsprofiler til pakkelokationer

Hver *lokationsprofil* fastlægger oplysninger og regler, der gælder for de tilknyttede lokationer. Da du skal bruge mindst én lokation til pakning, skal du oprette en lokationsprofil til den ud over en lokationstype. Hver profil kan bruges af et vilkårligt antal lokationer. Lokationer, der bruges til pakning, skal være konfigureret til sporing af id'er.

Benyt følgende fremgangsmåde for at konfigurere en lokationsprofil for en pakkelokation.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Lagersted \> Lokationsprofiler**.
1. Vælg enten en eksisterende profil i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny.
1. Udfyld følgende felter i hovedet for den nye eller valgte profil:

    - **Lokationsprofil-id** – Angiv et entydigt id for profilen.
    - **Navn** – Angiv et sigende navn til profilen.

1. I oversigtspanelet **Generelt** skal du indstille følgende felter:

    - **Lokationsformat** – Vælg det lokationsformat, der skal bruges til den aktuelle lokation. Lokationsformater er et navngivningssystem, der bruges til at oprette entydige og konsekvente navne for de forskellige placeringspositioner på et lagersted. Hvis du ikke allerede har det format, du skal bruge, kan du oprette det ved at gå til **Lagerstedsstyring \> Opsætning \> Lagersted \> Lokationsformater**. Yderligere oplysninger finder du i afsnittet [Konfigurere lokationer i et WMS-aktiveret lagersted](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Lokationstype** – Vælg den lokationstype, der er konfigureret som pakkelokationstype på siden **Parametre til lokationsstyring**, som beskrevet tidligere i denne artikel.
    - **Brug nummerpladesporing** – I forbindelse med pakkelokationer skal du angive denne indstilling til *Ja*. Systemet skal kunne spore nummerplade-id'er på pakkelokationer, så det kan styre pakningsprocessen.
    - **Tillad negativt lager** – I forbindelse med pakkelokationer skal du angive denne indstilling til *Nej*.
    - **Tillad blandede varer** – I forbindelse med pakkelokationer skal du angive denne indstilling til *Ja*. Denne indstilling er påkrævet, da mange forskellige varenumre typisk kommer til pakkelokationerne samtidig.
    - **Tillad blandet lagerstatus** – I forbindelse med pakkelokationer skal du angive denne indstilling til *Ja*. Denne indstilling er påkrævet, da varer med forskellige lagerstatus typisk kommer til pakkelokationerne samtidig.
    - **Tillad blandet lagerbatchnumre** – I forbindelse med pakkelokationer skal du angive denne indstilling til *Ja*. Den angives automatisk til *Ja*, når **Tillad blandede varer** er angivet til *Ja*.

#### <a name="set-up-packing-locations"></a>Konfigurere pakkelokationer

Du skal have mindst én *lokation*, hvor arbejdere skal placere lagervarer, der skal pakkes i containere.

Følg disse trin for at tilføje en pakkelokation.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lokationer**.
1. Vælg **Ny** i handlingsruden for at tilføje en lokation.
1. Angiv følgende felter til den nye lokation:

    - **Lagersted** – Vælg det lagersted, hvor pakkelokationen skal være.
    - **Lokation** – Angiv et navn til den nye lokation.
    - **Lokationsprofil-id** – Sørg for at angive det id, du oprettede i forrige afsnit.

## <a name="set-up-the-packing-process"></a>Konfigurere pakkeprocessen

I dette afsnit beskrives, hvordan du konfigurerer indstillinger, der aktiverer pakkeprocessen, og hvordan arbejdere kan pakke lageret i containere.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Konfigurere politik for containerpakning

Hver *politik for containerpakning* definerer, hvordan en container skal behandles. Hver gang du opretter en ny container, skal du også vælge en politik for containerpakning, som skal anvendes på den.

Følg disse trin for at konfigurere en politik for containerpakning:

1. Gå til **Lokationsstyring \> Konfiguration \> Containere \> Politikker for containerpakning**.
1. Vælg enten en eksisterende politik i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny.
1. Udfyld følgende felter i hovedet for den nye eller valgte politik:

    - **Politik for containerpakning** – Angiv et entydigt navn til politikken.
    - **Beskrivelse** – Angiv et sigende navn til politikken.

1. På fanen **Oversigt** kan du angive følgende felter. Disse felter giver dig mulighed for at angive, hvilke handlinger der skal udføres, når containeren lukkes, om der skal arbejdes med eller uden arbejdsoprettelse, og hvornår containeren skal frigives fra pakkestationen.

    - **Lagersted** – Vælg det lagersted, hvor pakkepolitikken skal anvendes.
    - **Standardlokation for endelig forsendelse** – Angiv containerens foretrukne lokation, når den er lukket. Dette felt er kun tilgængeligt, når feltet **Frigivelsespolitik for container** er indstillet til *Gør disponibel ved endelig afsendelseslokation*.
    - **Standardlokation for sortering** – Dette felt bruges sammen med den [udgående sorteringsfunktionalitet](outbound-sorting.md).
    - **Vægtenhed** – Vælg den standardmåleenhed, der skal bruges, når en container lukkes og manifesteres. Denne måleenhed vil typisk være den måleenhed, der bruges af en vægt på pakkepladsen. Dette felt gælder politikker med eller uden oprettelse af arbejde.
    - **Lukningspolitik for containere** – Vælg en af følgende indstillinger for at definere, hvad der skal ske, når containeren lukkes:

        - *Automatisk frigivelse* – Containeren betragtes som frigivet fra pakkestationen, og den handling, der er angivet i feltet **Frigivelsespolitik for container**, udløses.
        - *Forsinket frigivelse* – Containeren frigives ikke med det samme fra pakkestation. En lagerarbejder skal manuelt frigive den senere.
        - *Valgfrit* – Mens en arbejder lukker containeren, kan de vælge, om containeren skal frigives.

        Hvis pakkestationen primært håndterer enkeltcontainere, som leveres direkte til kunderne, er den mest naturlige måde at frigive containerne med det samme. Hvis pakkestationen håndterer forsendelser, der består af flere containere eller paller, er det sandsynligvis bedst at udskyde frigivelsen, indtil hele forsendelsen eller pallen er pakket og er klar til afhentning.

    - **Frigivelsespolitik for container** – Vælg en af følgende indstillinger for at definere, hvad der skal ske, når containeren frigives fra pakkelokationen:

        - *Gør disponibel ved endelig afsendelseslokation* – Opdater containeren til den endelige afsendelseslokation. Hvis du vælger dette, skal du bruge feltet **Standardlokation for endelig forsendelse** til at angive containerens foretrukne lokation, når den er lukket.
        - *Opret arbejde, der skal flytte containere fra pakkestation* – Opret arbejde for at flytte containeren fra pakkestationen til det midlertidige lagringsområde eller direkte til lagerporten. Brug feltet **Arbejdsskabelon** til at angive den arbejdsskabelon, der skal anvendes, når der oprettes arbejde for containeren.
        - *Tildel container til udgående sorteringsposition* – Denne indstilling bruges sammen med den [udgående sorteringsfunktionalitet](outbound-sorting.md).

        I de fleste tilfælde anbefales det, at du opretter arbejde med flytning af containere, da denne tilgang bedre repræsenterer de faktiske manuelle processer på lagerstedet. Men for simple scenarier eller situationer, hvor pakkestationen er placeret direkte i lagerportens område, kan det være at foretrække, at containeren straks kan benyttes på den endelige afsendelseslokation.

    - **Arbejdsskabelon** – Vælg den arbejdsskabelon, der skal anvendes, når der oprettes arbejde for containeren. Dette felt er kun tilgængeligt, når feltet **Frigivelsespolitik for container** er angivet til *Opret arbejde til flytning af container fra pakkestation* og relateret til en arbejdsordretype med navnet *Plukning af pakket container*. Du kan finde flere oplysninger i [Arbejdsskabeloner og lokationsvejledninger](control-warehouse-location-directives.md).

    I de resterende trin kan du konfigurere de indstillinger, der har relation til *manifestering*. manifestering består i at angive vægten på en container, containergruppe eller forsendelse sammen med det sporings-id, der modtages fra en transportudbyder. Dynamics 365 Supply Chain Management kan ikke integreres med eksterne transportudbydersystemer. I stedet skal lagerarbejdere udskrive labels, der er modtaget fra transportudbyderen, og derefter scanne et sporingsnummer, når de fuldfører manifestproceduren.

    Da manifestkravene varierer fra kunde til kunde og også fra forsendelse til forsendelse, giver pakkepolitikkerne mulighed for stor fleksibilitet i arbejdsgangen. Du kan konfigurere manifester til containere, containergrupper og forsendelser i alle kombinationer.

    Hvis du bruger en procedure med flere manifestniveauer, skal arbejderne manifestere alle containere, før de manifesterer den tilhørende containergruppe, og de skal manifestere alle containergrupper, før de manifesterer den relaterede forsendelse.

1. I oversigtspanelet **Containermanifest** skal du angive følgende felter:

    - **Automatisk manifest ved containerlukning** – Angiv denne indstilling til *Ja* , hvis du vil anvende manifestoplysningerne som del af containerlukningsprocessen. Hvis du ikke benytter transportintegration, skal oplysningerne registreres manuelt.
    - **Manifestkrav til container** – Vælg en af følgende indstillinger:

        - *Ingen* – Der anvendes ingen manifestering.
        - *Manuel* – Manifestering vil være påkrævet af pakkearbejdsprocessen. Systemet tillader ikke, at en container lukkes eller frigives, før manifestering er fuldført.
        - *Transportstyring* – Manifestering sker ved hjælp af TMS-satsprogrammet (Transportation Management). Da denne indstilling kræver tilpasset udvikling for at implementere et bestemt program til transportudbyderen, virker det ikke som standard i den aktuelle version.

    - **Udskriv containerindholdet** – Angiv denne indstilling til *Ja*, hvis rapporten med containerindholdet automatisk skal udskrives, når en container registreres som lukket. Den kan også udskrives efter behov.

1. Vælg en af følgende indstillinger i oversigtspanelet **Manifest for containergruppe** i feltet **Manifestkrav til containergruppe**:

    - *Ingen* – Containergruppemanifest medtages ikke som et krav i pakkearbejdsgangen.
    - *Manuel* – Containergruppemanifest medtages som et krav i pakkearbejdsgangen. Alle containere i gruppen skal være lukket, før containergruppen kan manifesteres. Vælg denne indstilling, hvis du skal fuldføre et manifest for hver containergruppe, der er pakket på pakkestationen. Denne indstilling vælges som regel, hvis containere pakkes på en palle, og hele pallen manifesteres.

    > [!NOTE]
    > Den aktuelle version understøtter ikke manifestrapporter for containergrupper, og der er ingen understøttelse fra TMS-programmet til containergrupper.

1. I oversigtspanelet **Forsendelsesmanifest** skal du angive følgende felter:

    - **Manifestkrav til forsendelse** – Vælg en af følgende indstillinger:

        - *Ingen* – Forsendelsesmanifest medtages ikke som et krav i pakkearbejdsgangen.
        - *Manuel* – Forsendelsesmanifest medtages som et krav i pakkearbejdsgangen. Der kan ikke frigives containere til en forsendelse, før manifestering er fuldført.
        - *Transportstyring* – Manifestering sker ved hjælp af TMS-satsprogrammet. Da denne indstilling kræver tilpasset udvikling for at implementere et bestemt program til transportudbyderen, virker det ikke som standard i den aktuelle version.

        Forsendelsesmanifestering skal aktiveres, hvis du skal fuldføre et manifest for hele den forsendelse, der er pakket på pakkestationen. Den bruges typisk, når der kræves ét konsolideret manifest, selvom forsendelsen består af flere containere eller containergrupper.

    - **Udskriv følgeseddel** – Angiv denne indstilling til *Ja* , hvis følgesedlen automatisk skal udskrives som en del af forsendelsens manifest. Den kan også udskrives efter behov.

### <a name="set-up-container-types"></a>Konfigurere containertyper

Under den manuelle pakkeproces skal der oprettes containere, før varerne kan pakkes i dem. Hver container skal være baseret på en *containertype*, som definerer en containers maksimale fysiske volumen og vægtkapacitet.

Følg disse trin for at konfigurere en containertype.

1. Gå til **Lagerstedsstyring \> Konfiguration \> Containere \> Containertyper**.
1. Vælg i handlingsruden **Ny** for at tilføje en containertype.
1. Angiv følgende felter for den nye containertype:

    - **Containertypekode** – Angiv et entydigt id for containertypen.
    - **Beskrivelse** – Indtast en detaljeret beskrivelse den nye containertype.
    - **Taravægt** – Angiv den faktiske eller anslåede vægt af containeren.
    - **Maksimal nettovægt** – Angiv den maksimumvægt, som containeren kan indeholde.

1. I felterne **Længde**, **Bredde**, **Højde** og **Volumen** i sektionen **Containerdimensioner** skal du angive de fysiske dimensioner for selve containeren.
1. I felterne **Længde**, **Bredde**, **Højde** og **Volumen** i sektionen **Maksimum** skal du angive de fysiske maksimumdimensioner, som containeren kan klare.
1. Du kan definere flere attributter for containertyper, der er knyttet til andre operationer, hvor der bruges containere. Du kan finde flere oplysninger under [Containerisering](wave-containerization.md).

> [!NOTE]
> Til manuel pakkeproces bruger systemet kun værdien fra feltet **Maksimal nettovægt** og værdien i feltet **Volumen** i sektionen **Maksimum**.

### <a name="set-up-packing-profiles"></a>Konfigurere pakkeprofiler

*Pakkeprofiler* er obligatoriske for pakkeprocessen. De kan vælges eller angives som standard, når du starter en pakkeoperation på siden **Pak**.

Følg disse trin for at konfigurere en pakningsprofil.

1. Gå til **Lokationsstyring \> Konfiguration \> Emballage \> Pakningsprofiler**.
1. Vælg enten en eksisterende profil i listeruden, eller vælg **Ny** i handlingsruden for at oprette en ny.
1. Udfyld følgende felter i hovedet for den nye eller valgte profil:

    - **Pakkeprofil--id** – Angiv et kort id for profilen.
    - **Beskrivelse** – Indtast en beskrivelse af pakkeprofilen.
    - **Politik for containerpakning** – Vælg den pakkepolitik, der gælder for profilen. Yderligere oplysninger kan du se i afsnittet [Konfigurere politik for containerpakning](#packing-policy) i denne artikel.
    - **Tilstanden Container-id** – Vælg, om der automatisk genereres et container-id, når der oprettes en container, eller det skal oprettes manuelt.
    - **Containertype** – Vælg den containertype, der bruges som standard, når der oprettes en ny container.
    - **Opret automatisk container ved containerlukning** – Markér dette afkrydsningsfelt, hvis der automatisk skal oprettes en ny container, hvis den foregående container er lukket, og der er en eller flere linjer tilbage i den aktuelle forsendelse.

### <a name="set-up-warehouse-workers"></a>Konfigurere lagerarbejdere

Alle brugere eller arbejdere, der pakker containere ved hjælp af webklientens **Pak**-side eller aktivitetskoden *Pakning* i mobilappen Warehouse Management, skal have en brugerkonto, der er tilknyttet en *arbejder-/personpost*, som de nødvendige sikkerhedsadgangsrettigheder er tildelt. (Du kan finde flere oplysninger om, hvordan du konfigurerer brugere, i [Oprette nye brugere](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md)).

Benyt følgende fremgangsmåde for at konfigurere en *arbejder-/personpost* for pakkeprocessen.

1. Gå til **Lokationsstyring \> Konfiguration \> Arbejder**.
1. Vælg **Ny** i handlingsruden for at tilføje en arbejdsbruger.
1. Angiv feltet **Arbejder** til den eksisterende arbejderpost, der er defineret i modulet **Personale** for den bruger, der skal fuldføre pakkeprocessen.
1. I oversigtspanelet **Profil** skal du indstille følgende felter:

    - **Politik for containerpakning** – Vælg en politik for containerpakning, der definerer, hvordan containere på pakkestationen skal behandles. Den politik for containerpakning, som du vælger, vælges på forhånd for arbejderen, når denne åbner pakkestationen. Yderligere oplysninger finder du i følgende blogindlæg: [Forbedret funktionalitet af pakning](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Pakkeprofil-id** – Vælg et pakkeprofil-id, der definerer de indstillinger for pakkepolitik og container, der skal bruges. Hvis det valgte pakkeprofil-id er knyttet til en politik for containerpakning, kan du ikke ændre indstillingen **Politik for containerpakning** på denne side.

1. Vælg det standardsted, det lagersted og den lokation, der gælder for arbejderen, i oversigtspanelet **Standard for pakkestation**.
1. Hvis arbejderen vil bruge mobilappen Warehouse Management til at administrere og registrere sit arbejde med containerpakning, skal du i oversigtspanelet **Brugere** oprette en eller flere konti, som arbejderen kan bruge til at logge på appen. Yderligere oplysninger finder du i [Brugerkonti til mobilenheder](mobile-device-work-users.md).

## <a name="example-scenario"></a><a name="scenario"></a>Eksempelscenario

Dette afsnit indeholder et eksempelscenario, der viser, hvordan du kan oprette en ordre og pakke varerne.

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

Du kan også bruge dette scenarie som vejledning i at bruge funktionen i et produktionssystem. I dette tilfælde skal du dog erstatte dine egne værdier for hver af de indstillinger, der beskrives her.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Logge på som en bruger, der kan udføre pakkearbejde

Log på Supply Chain Management ved hjælp af en brugerkonto, der har de rettigheder, der er nødvendige for at pakke containere. Brugeren *Julia Funderburk* er medtaget som en del af demodataene og har de nødvendige tilladelser. Denne bruger har bruger-id'et *Admin*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Oprette en salgsordre og fuldføre arbejdet

Benyt følgende fremgangsmåde for at oprette en salgsordre, og fuldfør arbejdet med at flytte de bestilte varer til pakkestationen.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Gå til dialogboksen **Opret salgsordre**, og vælg **US-005** i feltet *Debitorkonto*.
1. Vælg **OK** for at lukke dialogboksen.
1. Den nye salgsordre åbnes og indeholder en enkelt tom linje i oversigtspanelet **Salgsordrelinjer**. På den nye ordrelinje skal du angive følgende værdier:

    - **Varenummer:** *A0001*
    - **Antal:** *2*
    - **Lokation:** *6*
    - **Lagersted:** *62*

1. Mens ordrelinjen stadig er valgt skal du vælge **Lager \> Reservation** på værktøjslinjen i oversigtspanelet **Salgsordrelinjer**.
1. På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.

    En meddelelse viser forsendelses- og bølge-id'erne for ordren.

1. Mens ordrelinjen stadig er valgt skal du vælge **Lagersted** \> **Arbejdsdetaljer** på værktøjslinjen i oversigtspanelet **Salgsordrelinjer**. Hvis du bruger batchafvikling til at køre bølgen, kan du blive nødt til at vente kort tid på, at arbejdet oprettes.
1. I handlingsruden på siden **Arbejde** skal du under fanen **Arbejde** vælge **Fuldfør arbejde**.
1. Angiv feltet **Bruger-id** til **62** på siden *Fuldførelse af arbejde*.
1. Vælg derefter **Valider arbejde** i handlingsruden.
1. Når du modtager en meddelelse om, at dit arbejde er gyldigt, skal du vælge **Fuldfør arbejde** for at fuldføre plukprocessen for lagervarerne og lægge dem på lokationen *Pak*.
1. Notér værdien af det **Forsendelses-id**, der vises for arbejdet i det øverste gitter.

### <a name="pack-the-ordered-items-into-a-container"></a>Pakke de bestilte varer i en container

Lagervarerne er nu flyttet til pakkeområdet og er klar til at blive pakket i containere. Følg disse trin for at oprette en ny container i systemet og pakke den.

1. Gå til **Lokationsstyring \> Pakning og containerisering \> Pakke**.
1. Angiv følgende værdier i dialogboksen **Vælg pakkestation**:

    - **Lokation:** *6*
    - **Lagersted:** *62*
    - **Lokation:** *Pakke*
    - **Pakkeprofil-id:** *WH62*

1. Vælg **OK**.
1. På til siden **Pakke** skal du i feltet **Nummerplade eller forsendelse** angive det forsendelses-id, du noterede dig tidligere. Nu bør nu se de resterende ikke-pakkede varer i oversigtspanelet **Åbne linjer**.
1. Vælg **Ny container** i handlingsruden for at oprette en container i systemet.
1. I dialogboksen **Id for den nye container** skal du indstille feltet **Containertype** til *SmallBox*.
1. Vælg **OK** for at oprette containeren.
1. Vælg **OK** for at vende tilbage til siden **Pak**. Oversigtspanelet **Åbne containere** viser nu værdien for **Container-id'** for den container, du har oprettet.
1. I dette scenario skal du kun pakke en af de bestilte varer indtil videre. I oversigtspanelet **Varepakning** skal du derfor angive følgende værdier:

    - **Antal:** *1.00*
    - **Identifikator:** *A0001*

    Umiddelbart efter at du har valgt værdien **Identifikator**, opdaterer siden oversigtspanelerne **Åbne linjer** og **Alle linjer** for at angive, at én vare er pakket. Du skulle nu have pakket et af de to styk af varen *A0001*.

1. Gå til handlingsruden, og vælg **Luk container**.
1. I dialogboksen **Luk container** skal du vælge **Hent systemvægt** for at udfylde standardværdien af **Bruttovægt**.
1. Vælg **OK** for at lukke containeren.

> [!TIP]
> Containere kan vises på forskellige måder alt efter kontekst. Når du f.eks. pakker en forsendelse, er det ofte en fordel at få vist en af de containere, der indgår i forsendelsen, eller alle containere, der fysisk er på en pakkestation. Siden **Pakkestation** har knapper, som du kan bruge til at få vist alle åbne og lukkede containere på en pakkestation. Disse visninger er ikke begrænset til en bestemt forsendelse. De kan være meget nyttige i situationer, hvor en arbejder pakker en container, og en anden arbejder manifesterer og frigiver containeren.
>
> En konsolideret visning af alle containere er også tilgængelig. Denne visning er oftest nyttig for brugere, der arbejder uden for rammerne af en enkelt pakkestation. Se den ved at gå til **Lokationsstyring \> Emballage og containerisering \> Containere**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
