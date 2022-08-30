---
title: Forespørge på data ved brug af omveje i Warehouse Management-mobilappen
description: Denne artikel beskriver, hvordan du konfigurerer menupunkter i dataforespørgsler på mobilenheder og bruger dem som en del af omveje.
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cc013e962b4da803764f16e451b1d433666e75c2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336599"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Forespørge på data ved brug af omveje i Warehouse Management-mobilappen

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Funktionsintroduktion

Ved at levere mulighed for scanning af stregkoder giver en Warehouse Management-mobilapp dig en nem og præcis måde at registrere data på som en del af lagerstedsprocesserne. Stregkoderne beskadiges dog nogle gange og bliver ulæselige, eller de nødvendige data findes muligvis ikke som stregkode i forretningsprocesflowet. I disse tilfælde kan manuel indtastning af data tage lang tid, og det kan også medføre, at forkerte data registreres. Resultatet kan være reduceret effektivitet og et lavere serviceniveau.

Ved hjælp af en fleksibel dataforespørgselsproces kan arbejderne nemt slå de nødvendige oplysninger op som en del af de integrerede Warehouse Management-mobilappflows og anvende filtreringsindstillinger, så kun de relevante data vises. Derfor er manuel udvælgelse hurtigere og mere præcis.

I modtagelsesflowet for indkøbsordren skal der f.eks. kræves et indkøbsordrenummer for at matche det indkommende lager. Som en del af denne proces kan du nemt konfigurere menupunkter, så du får vist en kortliste over de relevante indkøbsordrenumre. På denne måde kan du fortsætte tilgangsflowet ved at bruge en hurtig peg og vælg-fremgangsmåde. Denne artikel indeholder eksempelscenarier, men funktionaliteten kan også bruges i en hvilken som helst af eller alle dine Warehouse Management-mobilappflows.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Aktivere funktionen til dataforespørgselsflow og dens forudsætninger

Før du kan bruge de funktioner, der er beskrevet i denne artikel, skal du gennemføre følgende procedure for at aktivere de påkrævede funktioner.

1. Gå til **Systemadministration \> Arbejdsområder \> Funktionsstyring**. (Du kan finde flere oplysninger om brug af administration af arbejdsområdet **Funktionsstyring** under [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)).
1. Hvis du kører Supply Chain Management version 10.0.28 eller tidligere, skal du aktivere er funktionen, der er angivet på følgende måde:

    - **Modul:** *Warehouse Management*
    - **Funktionsnavn:** *Trininstruktioner for lagerstedsappen*

    Denne funktion er en forudsætning for funktionen *Dataforespørgselsflow til app til Warehouse Management*. Fra og med Supply Chain Management version 10.0.29 er den obligatorisk og kan ikke deaktiveres. Du kan finde flere oplysninger om trinnet *Vejledninger til trin i lagerstedsapp* i [Tilpasse trintitler og instruktioner til Warehouse Management-mobilappen](mobile-app-titles-instructions.md).

1. Aktivér funktionen, der vises, på følgende måde:

    - **Modul:** *Warehouse Management*
    - **Funktionsnavn:** *Omveje i Warehouse Management-app*

    Denne funktion er en forudsætning for funktionen *Dataforespørgselsflow til app til Warehouse Management*. Fra og med Supply Chain Management version 10.0.29 er den som standard aktiveret. Yderligere oplysninger om funktionen *Omveje i Warehouse Management-app* finder du i [Konfigurere omveje til trin i menupunkter på mobilenheder](warehouse-app-detours.md).

1. Hvis funktionen *Omveje i Warehouse Management-app* allerede er aktiveret, skal du opdatere feltnavnene i Warehouse Management-mobilappen ved at gå til **Warehouse Management \> Opsætning \> Mobilenhed \> Feltnavne for lagerstedsapp** og vælge **Opret standardkonfiguration**. Gentag dette trin for hver juridisk enhed (firma), hvor du bruger mobilappen Warehouse Management. Du kan finde flere oplysninger i [Konfigurere felter til mobilappen Lokationsstyring](configure-app-field-names-priorities-warehouse.md).
1. Aktivér funktionen, der vises, på følgende måde:

    - **Modul:** *Warehouse Management*
    - **Funktionsnavn:** *Dataforespørgselsflow til app til Warehouse Management*

    Denne funktion er den, der er beskrevet i denne artikel.

## <a name="example-scenarios"></a>Eksempelscenarier

I denne artikel bruges eksempelscenarier til at vise, hvordan du kan bruge funktionen *Dataforespørgselsflow til app til Warehouse Management* til at forbedre tilgangsflowet for indkøb. I scenarierne bruges standardeksempeldataene, som omfatter et flow med navnet *Modtag indkøb*. Dette flow starter med at bede arbejderne om at identificere et indkøbsordrenummer, som de vil modtage for. For at gøre det nemmere for arbejderne at identificere indkøbsordren, vil du forbedre den første side i flowet ved at tilføje følgende nye forespørgselsindstillinger som [omveje](warehouse-app-detours.md):

- **Opslag af indkøbsordrer efter leverandør** – Åbn en side, hvor arbejderne bliver bedt om at angive et leverandørnavn eller en del af et leverandørnavn. Du kan bruge jokertegn. Hvis en arbejder f.eks. forventer en indgående levering i dag fra en leverandør, der inkluderer *Tailspin* i sit navn, kan de angive **Tail\*** for at se et sæt kort med åbne indkøbsordrer og denne tekst. Hvert kort indeholder flere felter, der indeholder oplysninger om hver indkøbsordre. Ud over leverandørens navn kan du designe kortene, så de viser kreditorkontonummeret, leveringsdatoen og dokumentstatus.
- **Søge efter IO'er for i dag** – Åbn en side, hvor arbejderne ikke bliver bedt om at angive data, men i stedet viser forudkonfigurerede filtre (f.eks. dags dato). Derefter vises et sæt kort, der svarer til filteret, på siden. Arbejderne fortsætter ved at vælge et kort til den indkøbsordre, som de vil registrere lagervarer for.
- **Slå IO'er op efter vare** – Åbn en side, hvor arbejderne bliver bedt om at scanne stregkoden for alle varer på det ankomne lager. Derefter vises alle åbne indkøbsordrer, der indeholder linjer for det scannede varenummer. For at dække situationer, hvor en stregkode ikke kan læses, kan du føje et opslag med omveje til denne side, så arbejderne kan søge efter varenumre i en bestemt indkøbsordre.

I hvert tilfælde identificerer arbejderen en indkøbsordre ved at vælge et kort og returneres derefter til den første side med det valgte indkøbsordrenummer. Arbejderen kan derefter fortsætte det indgående flow til registrering af lagervarer.

## <a name="enable-sample-data"></a>Aktivér eksempeldata

Hvis du vil arbejde gennem eksempelscenarier, der vises i denne artikel, skal du arbejde på et system, hvor [standarddemodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed *USMF* (firma), før du starter.

## <a name="configure-the-mobile-device-menu-items"></a>Konfigurere menupunkter til mobilenhed

Hvis du vil oprette hver af de nye forespørgselsindstillinger, som du skal føje til første side i flowet, skal du konfigurere den som et menupunkt på en mobilenhed. Du kan senere gøre forespørgselsindstillingerne tilgængelige som omveje til flowet *Modtag indkøb*.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Oprette menupunktet "Slå IO'er op efter leverandør"

Opret menupunktet **Slå IO'er op efter leverandør** ved at følge disse trin.

1. Gå til **Warehouse Management \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg **Ny** i handlingsruden for at tilføje et menupunkt til mobilenhed.
1. Angiv følgende værdier for det nye menupunkt:

    - **Menupunktnavn:** *Slå IO'er op efter leverandør*
    - **Titel:** *Slå IO'er op efter leverandør*
    - **Tilstand:** *Indirekte*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Aktivitetskode:** *Dataforespørgsel*
    - **Brug procesvejledning:** *Ja* (denne værdi vælges automatisk).
    - **Tabelnavn:** *PurchTable* (du vil slå indkøbsordrenumre op fra denne tabel).

1. Vælg **Rediger forespørgsel** i handlingsruden for at definere en forespørgsel, der er baseret på den valgte basistabel (i dette tilfælde tabellen indkøbsordrer).
1. I forespørgselseditoren skal du under fanen **Interval** tilføje følgende linjer i gitteret.

    | Tabellen | Afledt tabel | Felt | Afgrænsning |
    |---|---|---|---|
    | Indkøbsordrer | Indkøbsordrer | Status for indkøbsordre | Åben ordre |
    | Indkøbsordrer | Indkøbsordrer | Leveringsdato | (dayRange(-10,10)) |
    | Indkøbsordrer | Indkøbsordrer | Leverandørnavn | |

1. Vælg **OK**.

    I dette eksempel konfigureres det nye menupunkt til at finde åbne indkøbsordrer, der forventes at ankomme mellem 10 dage bagud og 10 dage forud.

    I forespørgslen er kolonnen **Kriterier** for *Leverandørnavn* ikke udfyldt. Arbejderne kan derfor angive denne værdi, når de bruger mobilappen Warehouse Management.

    Hvis du vil angive, hvordan listen skal sorteres, kan du konfigurere sortering under fanen **Sortering**.

1. Udover at definere forespørgslen skal du også vælge, hvilke felter der skal vises på kortene på forespørgselslistesiden. Vælg derfor **Feltliste** i handlingsruden.
1. På siden **Feltliste** kan du angive følgende værdier:

    - **Vis felt 1:** *PurchId* (dette felt vises som overskrift for hvert kort).
    - **Vis felt 2:** *PurchStatus*
    - **Vis felt 3:** *PurchName*
    - **Vis felt 4:** *OrderAccount*
    - **Vis felt 5:** *DeliveryDate*
    - **Vis felt 6:** *displayDocumentStatus()* (denne værdi er en visningsmetode, som "()" i slutningen angiver).

1. Vælg **Gem** i handlingsruden. Luk derefter siden.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Oprette menupunktet "Søge efter IO'er for i dag"

Opret menupunktet **Søge efter IO'er for i dag** ved at følge disse trin.

1. Gå til **Warehouse Management \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg **Ny** i handlingsruden for at tilføje et menupunkt til mobilenhed.
1. Angiv følgende værdier for det nye element:

    - **Menupunktnavn:** *Søge efter IO'er for i dag*
    - **Titel:** *Søge efter IO'er for i dag*
    - **Tilstand:** *Indirekte*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Aktivitetskode:** *Dataforespørgsel*
    - **Brug procesvejledning:** *Ja* (denne værdi vælges automatisk).
    - **Tabelnavn:** *PurchTable* (du vil slå indkøbsordrenumre op fra denne tabel).

1. Vælg **Rediger forespørgsel** i handlingsruden for at definere en forespørgsel, der er baseret på den valgte basistabel (i dette tilfælde tabellen indkøbsordrer).
1. I forespørgselseditoren skal du under fanen **Interval** tilføje følgende linjer i gitteret.

    | Tabellen | Afledt tabel | Felt | Afgrænsning |
    |---|---|---|---|
    | Indkøbsordre | Indkøbsordre | Status for indkøbsordre | Åben ordre |
    | Indkøbsordre | Indkøbsordre | Leveringsdato | (Day(0)) |

1. Vælg **OK**.

    I dette eksempel konfigureres det nye menupunkt til at finde åbne indkøbsordrer, der forventes at ankomme i dag.

    Hvis du vil angive, hvordan listen skal sorteres, kan du konfigurere sortering under fanen **Sortering**.

1. Udover at definere forespørgslen skal du også vælge, hvilke felter der skal vises på kortene på forespørgselslistesiden. Vælg derfor **Feltliste** i handlingsruden.
1. På siden **Feltliste** kan du angive følgende værdier:

    - **Vis felt 1:** *PurchName* (dette felt vises som overskrift for hvert kort).
    - **Vis felt 2:** *PurchId*
    - **Vis felt 3:** *PurchStatus*
    - **Vis felt 4:** *DlvMode*
    - **Vis felt 5:** *DlvTerm*
    - **Vis felt 6:** *OrderAccount*
    - **Vis felt 7:** *VendorName()* (denne værdi er en visningsmetode, som "()" i slutningen angiver).

1. Vælg **Gem** i handlingsruden. Luk derefter siden.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Oprette menupunktet "Slå IO'er op efter vare"

Opret menupunktet **Slå IO'er op efter vare** ved at følge disse trin.

1. Gå til **Warehouse Management \> Opsætning \> Mobilenhed \> Menupunkter i mobilenhed**.
1. Vælg **Ny** i handlingsruden for at tilføje et menupunkt til mobilenhed.
1. Angiv følgende værdier for det nye element:

    - **Menupunktnavn:** *Slå IO'er op efter vare*
    - **Titel:** *Slå IO'er op efter vare*
    - **Tilstand:** *Indirekte*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Aktivitetskode:** *Dataforespørgsel*
    - **Brug procesvejledning:** *Ja* (denne værdi vælges automatisk).
    - **Tabelnavn:** *PurchLine* (du vil slå indkøbsordrenumre op på basis af varenummeret via linjedataene).

1. Vælg **Rediger forespørgsel** i handlingsruden for at definere en forespørgsel, der er baseret på den valgte basistabel (i dette tilfælde tabellen med indkøbsordrelinjer, men du kan bruge alle de værdier, der er relateret til overskriften, ved at knytte til *PurchTable*).
1. I forespørgselseditoren skal du under fanen **Interval** tilføje følgende linjer i gitteret.

    | Tabellen | Afledt tabel | Felt | Afgrænsning |
    |---|---|---|---|
    | Indkøbsordrelinjer | Indkøbsordrelinjer | Linjestatus | Åben ordre |
    | Indkøbsordrelinjer | Indkøbsordrelinjer | Leveringsdato | (dayRange(-10,10)) |
    | Indkøbsordrelinjer | Indkøbsordrelinjer | Varenummer | |

1. Vælg **OK**.

    I dette eksempel konfigureres det nye menupunkt til at finde åbne indkøbsordrelinjer, der forventes at ankomme mellem 10 dage bagud og 10 dage forud.

    I forespørgslen er kolonnen **Kriterier** for *Varenummer* ikke udfyldt. Arbejderne kan derfor angive denne værdi, når de bruger mobilappen Warehouse Management.

    Hvis du vil angive, hvordan listen skal sorteres, kan du konfigurere sortering under fanen **Sortering**.

1. Udover at definere forespørgslen skal du også vælge, hvilke felter der skal vises på kortene på forespørgselslistesiden. Vælg derfor **Feltliste** i handlingsruden.
1. På siden **Feltliste** kan du angive følgende værdier:

    - **Vis felt 1:** *PurchId* (dette felt bruges som overskrift for hvert kort).
    - **Vis felt 2:** *VendAccount*
    - **Vis felt 3:** *PurchQty*
    - **Vis felt 4:** *PurchUnit*
    - **Vis felt 5:** *PurchStatus*

1. Vælg **Gem** i handlingsruden. Luk derefter siden.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Føje de nye menupunkter til en mobilenhedsmenu

De tre nye menupunkter på mobilenheder er nu klar til at blive føjet til menuen i mobilenheder. Denne opgave skal være fuldført, før menupunkterne kan bruges som del af en omvejsproces. I dette eksempel opretter du en ny undermenu og føjer de nye menupunkter til den.

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv følgende værdier på overskriften for den nye post:

    - **Navn:** *Forespørg*
    - **Beskrivelse:** *Forespørg*

1. På listen **Tilgængelig menuer og menupunkter** skal du vælge de menupunktet til mobilenhed, du lige har oprettet. Vælg den højre pileknap for at flytte menupunktet til listen **Menustruktur**.
1. Gentag det forrige trin for de to andre nye menupunkter.
1. Vælg **Hoved**-menuen i venstre listerude.
1. Rul ned til sektionen **Menuer** i rullelisten **Tilgængelige menuer og menupunkter**, og vælg den nye menu **Forespørg**. Vælg den højre pileknap for at flytte menupunktet til listen **Menustruktur**.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Konfigurere omveje til trin på mobilenheder

For at fuldføre opsætningen skal du nu bruge konfigurationen af omvejen på siden **Trin i mobilenhed** til at føje de tre nye menupunkter for mobilenhed til det eksisterende trin til identifikation af indkøbsordrer i flowet *Modtag indkøb*.

1. Gå til **Lagerstedsstyring \> Opsætning > Mobilenhed \> Trin for mobilenhed**.
1. I feltet **Filter** skal du angive *PONum*. Vælg derefter *Trin-id: "PONum"* på rullelisten.
1. Mens den post, der blev fundet, er valgt i gitteret, skal du vælge **Tilføj trinkonfiguration** i handlingsruden. Angiv feltet **Menupunkt** i dialogboksen med rullelisten til *Modtag indkøb*. Vælg derefter **OK** for at lukke dialogboksen.
1. Vælg **Tilføj** på værktøjslinjen på detaljesiden for den nye trinkonfiguration (**Modtag indkøb: PONum**) i oversigtspanelet **Tilgængelige omveje (menupunkter)**.
1. I dialogboksen **Tilføj omvej** skal du finde og vælge menupunktet **Slå IO'er op efter leverandør**, du tidligere har oprettet.
1. Vælg **OK** for at lukke dialogboksen og føje det valgte menupunkt til listen med omveje.
1. Vælg den nye omvej, og vælg derefter **Vælg felter, der skal sendes** på værktøjslinjen.
1. I dialogboksen **Vælg felter, der skal sendes**, skal du ikke føje noget til sektionen **Send fra købsmodtagelse**, da du ikke vil overføre værdier til menupunktet Omvej. Angiv dog følgende værdi for den tomme række, der allerede er tilføjet der, i sektionen **Hent tilbage fra opslag af IO'er efter leverandør**:

    - **Kopiér fra opslag af IO'er efter leverandør:** *Indkøbsordre*
    - **Indsæt i indkøbsmodtagelse:** *Indkøbsordre*

1. Vælg **OK** for at lukke dialogboksen.
1. Gentag trin 4 til 9 for de to andre nye menupunkter (**Søge efter IO'er for i dag** og **Slå IO'er op efter vare**). For menupunktet **Slå IO'er op efter leverandør**, skal du ikke sende data til disse omveje, men du vil returnere et indkøbsordrenummer.
1. Luk siden.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Prøve en proces for modtagelse af indkøb, der indeholder en dataforespørgsel som del af en omvej

Følg disse trin for at teste konfigurationen af den nye mobilapp.

1. Opret flere indkøbsordrer, der har linjer for lagersted 51.
1. Gå til en mobilenhed eller emulator, der kører mobilappen Lokationsstyring, og log på lagersted 51 ved at bruge *51* som bruger-id og *1* som adgangskode.
1. Vælg **Indgående** og derefter **Modtag indkøb** i mobilappens menu.

    Du skulle kunne se følgende side, der indeholder de tre nye menupunkter.

    ![Indkøbsmodtagelse ved hjælp af indkøbsordrenummer.](media/wma-purchase-receive-po-num-with-detours.png "Indkøbsmodtagelse ved hjælp af indkøbsordrenummer")

1. Prøv de forskellige egenskaber, og læg mærke til, at du kan sende et indkøbsordrenummer tilbage ved at vælge et af kortene på listen.

    ![Indkøbsmodtagelse med IO-opslag efter leverandør, eksempel 1.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Indkøbsmodtagelse med IO-opslag efter leverandør, eksempel 1")

    ![Indkøbsmodtagelse med IO-opslag efter leverandør, eksempel 2.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Indkøbsmodtagelse med IO-opslag efter leverandør, eksempel 2")

> [!TIP]
> I stedet for at køre modtagelsesflowet ved at foretage et opslag fra menupunktet **Modtag indkøb**, kan du starte fra et forespørgselsflow (**Hoved \> Forespørgsel \> Slå IO'er op efter leverandør**) og aktivere en omvej for at køre det ønskede flow ved at vælge et af kortene på listen. Hvis du vil bruge denne metode, kan du definere en omvej på siden **Trin i mobilenhed** for trinnet med en **Trin-id**-værdi af *GenericDataInquiryList*. Da dette flow er et omvejsflow, kan du ikke kalde flere omveje fra det. Derfor vil opslaget ikke være tilgængeligt på det, når du kommer til skærmbilledet til varenummerindtastning, da systemet i øjeblikket kun understøtter ét omvejsniveau.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
