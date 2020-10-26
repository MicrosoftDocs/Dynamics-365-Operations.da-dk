---
title: Butiksordreopfyldning
description: Dette emne giver en oversigt over butiksordreopfyldning.
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: fb535b1f20d97042e6205b680de1cc687350f071
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975141"
---
# <a name="store-order-fulfillment"></a>Butiksordreopfyldning

[!include [banner](includes/banner.md)]

Mange detailhandlere ønsker at optimere deres ordreopfyldning ved at gøre det muligt for butikker at opfylde ordrer. Ordreopfyldning på butiksniveau kan afhjælpe situationer med overfyldte lagre i en bestemt butik eller kan være nødvendigt fra et logistisk synspunkt i tilfælde, hvor en butik har ekstra kapacitet eller ligger inden for nærmere leveringsafstand i forhold til kunden. Du kan løse dette behov ved hjælp af en samlet ordreopfyldningsoperation, der er tilgængelig på salgsstedet (POS).

På opfyldningsordrer i en bestemt butik er butikkens lagersted angivet på hovedet eller linjerne i ordren.

Ordreopfyldningsoperationen på POS'et indeholder et enkelt arbejdsområde på POS'et, der kan bruges til behandling af ordrer. Dette omfatter alt fra accept af ordren til at markere den som leveret eller start af afhentning i butikken.

## <a name="access-unified-order-fulfillment-in-the-point-of-sale"></a>Adgang til samlet ordreopfyldning på POS'et

Ordreopfyldning, [Handlings-id 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations) kan bruges til at få adgang til arbejdsområdet Butiksordreopfyldning på POS'et.

Ordreopfyldningsoperationen ikke har sin egen standardrettighed, men i fremtiden kan brugerne bruge rettigheden **Tillad hentning af ordre** til at aktivere operationen fra POS'et.

Der findes en konfigurationsindstilling på butiksniveau, som kan bruges til at bestemme, om en ordrelinje skal accepteres manuelt fra POS'et. Hvis denne konfigurationsindstilling ikke er indstillet, accepteres ordrelinjer som standard. Hvis denne konfigurationsindstilling er aktiveret, skal brugere på POS'et vælge rettigheden **Tillad accept af ordre** for at acceptere ordrer fra POS'et.

Ordrelinjer kan også blive afvist fra POS'et. Afvisning af en ordrelinje betyder, at den ikke bliver opfyldt i den pågældende butik, og linjen sendes tilbage til omfordeling til en anden butik eller lagersted. Rettigheden til ordrelinjeafvisning gives via rettigheden **Tillad ordreafvisning**.

## <a name="order-fulfillment-operation-parameters"></a>Parametre for ordreopfyldningsoperation

Ordreopfyldningen indeholder standardparametre, der kan anvendes på operationen, når den kaldes på POS'et. Når **Alle ordrer**-parameteren er konfigureret, vises alle ordrer, når operationen bruges. Parameteren **Ordrer, der skal afsendes** viser kun ordrer, der skal leveres fra butikken og **Ordrer, der skal afhentes** viser ordrer, der bliver afhentet i butikken.

## <a name="orders-for-fulfillment"></a>Ordrer til opfyldning

Ordreopfyldningsoperationen viser kun ordrer, der enten bliver afhentet i eller afsendt fra den aktuelle butik. Ordrer for andre butikker, der skal opfyldes, vises ikke, når du bruger ordreopfyldningsoperationen.

## <a name="line-selection"></a>Valg af linje

Linjer kan vælges ved hjælp af funktionen **Vælg** i handlingsruden. Når **Vælg** er aktiveret, kan der vælges flere linjer til behandling. Du kan fjerne markering af linjer ved at klikke på samme linje igen.

## <a name="line-details"></a>Linjedetaljer

Linjedetaljerne kan ses ved hjælp af pop op-menuen med linjedetaljer. Når denne menu bruges, findes der tre faner med yderligere oplysninger om den valgte linje. Den første fane, **Linjedetaljer**, indeholder oplysninger om selve linjen, f.eks. det bestilte og det resterende antal. Der vises yderligere oplysninger, herunder plukket, pakket og faktureret antal samt leveringsmåde og leveringsadresse. Fanen **Ordredetaljer** indeholder oplysningerne i ordrehovedet herunder kunde, kunde-id, ordrenummer, ordretotal og saldo. Fanen **Lager** indeholder oplysninger for den valgte linje i form af fysisk disponible lagerbeholdning, reserveret lagerbeholdning og bestilt lagerbeholdning.

Hvis flere linjer er markeret, angiver pop op-menuen med ordrelinjedetaljer kun, at der er valgt flere linjer. Ryd linjerne, indtil der kun én linje mangler, hvis du vil se detaljerne for en linje.

## <a name="pending-order-lines"></a>Ventende ordrelinjer

Samlet ordreopfyldning omfatter muligheden for at acceptere ordrer manuelt. Som standard accepteres opfyldningsordrer allerede i butikken. Hvis forretningsprocesser angiver, at en arbejder på butiksniveau skal acceptere ordrer, kan manuel godkendelse dog aktiveres på detailbutiksniveau. Hvis du vil aktivere ordreaccept, skal du gå til **Retail og Commerce** \> **Kanaler** \> **Butikker** \> **Alle butikker**. Åbn den ønskede butik og under fanen **Generelt** skal du finde underoverskriften **Ordreopfyldning**. Denne underoverskrift har indstillingen **Manuel godkendelse**, der er angivet til **Nej** som standard. Ved at angive denne indstilling til **Ja** og synkronisere ændringerne til kanaldatabasen, kan ordrelinjer gå igennem godkendelsesprocessen.

Arbejdere med rettigheden **Tillad accept af ordre** kan åbne ordreopfyldning og vælge linjer for accept. Når linjer er blevet godkendt, ændres deres status fra **Afventer** til **Accepteret**, og resten af ordreopfyldningsprocessen kan fortsætte. Når **Manuel godkendelse** er aktiveret, bliver ordrer ikke behandlet, før de er blevet godkendt.

Ordrer til afhentning i butikken har aldrig tilstanden **Venter**. Det er for at undgå et scenario, hvor en kunde ankommer til butikken, og hvor ordrelinjen ikke kan behandles, fordi en arbejder med de korrekte rettigheder ikke er tilgængelig.

## <a name="accepted-order-lines"></a>Accepterede ordrelinjer

Ordrer med linjetilstanden **Accepteret** kan fortsætte gennem resten af ordreopfyldningsprocessen på POS'et. Når en ordre er blevet accepteret, kan resterende handlinger udføres mod ordrelinjen.

Eksempelvis kan en accepteret ordrelinje vælges og derefter afhentes direkte uden at bruge pluklister og følgesedler.

## <a name="line-actions"></a>Linjehandlinger

### <a name="pick"></a>Pluk

Kategorien **Pluk** for handlinger er med til at støtte processen med at plukke ordrelinjerne fra hylder. Plukhandlingen kan kun udføres på ordrelinjer, der tidligere er godkendt.

**Handling: Pluk**

- **Resultatstatus for POS:** Pluk
- **Resultatstatus for administration:** Ingen ændring

Når en ordre er blevet accepteret, kan linjer vælges og markeret som **Pluk**. Markering af en linje, som **Pluk** er en måde at angive, at der allerede udføres plukarbejde på en linje. Dette forhindrer, at to arbejdere forsøger at plukke de samme ordrelinjer på samme tid.

**Handling: Udskriv plukliste**

- **Resultatstatus:** Pluk
- **Resultatstatus for administration:** Ingen ændring

Pluklister kan udskrives på POS'et, så det er nemmere for arbejdere at udføre plukprocessen. En udskrevet plukliste kan overføres til den arbejder, der udfører plukket, og efterhånden som produkterne plukkes, skal arbejderen manuelt markere dem som plukket på pluklisten.

Pluklisteformat konfigureres i Commerce og føjes til kvitteringsprofilen. Du kan finde flere oplysninger om opsætning af kvitteringsprofiler i [Kvitteringsskabeloner og udskrivning](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).

Hvis der er valgt linjer, og der udskrives en plukliste for disse linjer, opdateres de automatisk med status **Pluk**.

**Handling: Markér som plukket**

- **Resultatstatus:** Plukket eller delvist plukket
- **Resultatstatus for administration:** Plukket eller delvist plukket

Når den fysiske plukproces er blevet udført, kan linjer markeres som **Plukket**. Hvis du vælger en linje og markere den som **Plukket**, udføres et realtidsopkald for at opdatere ordrelinjen. Når linjen er markeret som **Plukket**, opdateres status i administrationen på POS'et også til **Plukket**, og lagertransaktioner afspejler, at det angivne antal er reduceret.

Med tiden kan delmængder af ordrer, der behandles, blive behandlet for en bestemt linje. Hvis der vælges en linje og handlingen **Markér som plukket**, og antallet er større end 1, bliver brugeren bedt om at angive antallet. Det resterende antal, der skal plukkes, udfyldes automatisk. Hvis et antal, der er mindre end det resterende antal, angives, bliver status for linjen **Delvist plukket**. Når ordrelinjen opdateres i administrationen, afspejler den også status som delvist plukket, og det antal, der er angivet af brugeren, bruges til opdatering af lageret.

Hvis en ordrelinje plukkes ved en fejl, skal plukningsfortrydelsesprocessen udføres på ordrelinjen i administrationen. Der understøttes i øjeblikket ingen handling til fortrydelse af pluk på POS'et.

Ordrelinjer fra forskellige ordrer kan vælges og markeres som **Pluk**, udskrives på samme plukliste eller markeres som **Plukket**.

### <a name="pack"></a>Pakke

Ordrelinjer kan pakkes på et hvilket som helst tidspunkt, efter at ordrelinjen er blevet accepteret.

**Handling: Udskriv følgeseddel**

- **Resultatstatus:** Pakket eller delvist pakket
- **Resultatstatus for administration:** Leveret eller delvist leveret

Denne handling markerer linjer som pakkede eller delvist pakkede og udskriver en følgeseddel. Du kan udskrive en følgeseddel for at validere de produkter, der er pakket sammen. Følgeseddelformatet konfigureres i Commerce og føjes til kvitteringsprofilen. Du kan finde flere oplysninger om opsætning af kvitteringsprofiler i [Kvitteringsskabeloner og udskrivning](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).

**Handling: Markér som pakket**

- **Resultatstatus:** Pakket eller delvist pakket
- **Resultatstatus for administration:** Leveret eller delvist leveret

Handlingen **Markér som pakket** kan bruges til at angive, at linjerne pakkes, uden at der udskrives en følgeseddel. Både **Udskrivning af følgeseddel** og **Markér som pakket** medfører lagertransaktioner i administrationen. Følgeseddellinjer på POS'et medfører, at der oprettes følgeseddeljournaler i administrationen.

Hvis en ordrelinje pakkes ved en fejl, skal det rettes i følgeseddeljournalen i administrationen.

Kun linjer i samme ordre og med samme leveringsmåden kan pakkes på samme tid.

I øjeblikket er det ikke muligt at markere er butiksafhentningslinjer som **Pakket**. Denne funktion tilføjes i en senere version. Processen til oprettelse af følgesedler bliver udvidet med understøttelse af tilførsel af tredjeparts forsendelsesoplysninger i følgeseddelprocessen.

### <a name="pick-up"></a>Hent

Ordrer til afhentning i butikken kan direkte afhentes, når de er hentet på POS'et. Ordrer til afhentning i butikken er ikke underlagt accept.

**Handling: Afhent**

- **Resultatstatus:** Faktureret eller delvist faktureret
- **Resultatstatus for administration:** Faktureret eller delvist faktureret

Hvis en linje vælges til pluk fra samlet ordreopfyldning, indlæses hele ordren på POS'et, og hele antallet for den valgte linje markeres. Andre linjer i ordren indlæses også i transaktionsvisningen på POS'et, men med antal markeret som nul.

Når linjerne for afhentning er blevet indlæst i transaktionsvisningen, kan transaktionen betales som normalt.

Linjer, der faktureres fuldt ud via afhentning, vises ikke længere i den samlede ordrebehandling. Linjer, der er blevet delvist afhentet, vil fortsat blive vist i den samlede ordreopfyldning, indtil de er helt afhentet.

Hvis en linje er afhentet ved en fejl, skal der udføres en returnering for at rette fejlen.

Kun linjer i samme ordre og med samme leveringsmåden kan afhentes på samme tid.

### <a name="shipping"></a>Forsendelse

Ordrelinjer, der skal afsendes fra lageret, kan behandles via samlet ordreopfyldning ved hjælp af handlingen **Send**. Hvis godkendelse af manuel ordrelinje konfigureres på kanalniveau, skal ordrer godkendes inden levering. Efter at en ordre er blevet godkendt og har status **Afventer** eller anden status, kan linjer leveres.

**Handling: Send**

- **Resultatstatus:** Faktureret eller delvist faktureret
- **Resultatstatus for administration:** Faktureret eller delvist faktureret

Linjer, der er leveret fra samlet ordreopfyldning, faktureres fra administrationen svarende til, hvis ordren faktureres direkte fra administrationen. Linjer, der leveres fra samlet ordreopfyldning, indlæses ikke i transaktionsvisningen, og der foretages ingen betaling på det tidspunkt, hvor linjerne leveres.

Ordrelinjer, der er fuldt afsendt, vises ikke længere i den samlede ordreopfyldning. Delvist afsendte linjer vil fortsat blive vist i den samlede ordreopfyldning, indtil de er helt afsendt.

Kun linjer fra den samme ordre kan leveres på samme tid. Hvis linjerne fra den samme ordre har forskellige leveringstilstande, kan de stadig vælges til levering på samme tid.

### <a name="reject"></a>Afvis

Linjer eller delvise linjer kan afvises. Dette gør muligt at omfordele dem fra administrationen til en anden butik eller lagersted. Linjer kan kun afvises, hvis de endnu ikke er plukket eller pakket. Hvis du vil afvise en linje, der allerede er plukket eller pakket, skal plukningen eller pakningen af linjen fjernes af administrationen.

**Handling: Afvis**

- **Resultatstatus:** Afvist
- **Resultatstatus for administration:** Ingen ændring

De afviste ordrelinjer kan ses i arbejdsområdet **Salgsordrebehandling og -forespørgsel**. Fjern personfilteret i arbejdsområdet for at få vist alle de afviste ordrelinjer på tværs af butikkerne. Fanen **Afviste ordrelinjer** under sektionen **Ordrer og foretrukne** viser ordrelinjeoplysningerne. Desuden kan brugerne klikke på knappen **Afviste ordrelinjer** under sektionen **Oversigt** for at navigere til en salgsordrevisning. Her vises alle de ordrer, der har en eller flere afviste ordrelinjer. Hvis distribueret ordrestyring (DOM) er aktiveret, omfordeles disse afviste ordrer automatisk til de relevante butikker for at blive opfyldt, men disse ordrelinjer kan også omfordeles manuelt. Hvis du vil gøre det, skal du markere linjen, der viser **Opfyldelsesstatus** **Afvist**, og ændre lokation/lagersted efter behov. Klik på rullemenuen **Opdater linje**, og klik på **Nulstil opfyldningsstatus** for at ændre opfyldningsstatus fra **Afvist** til **Accepteret** eller **Afventer**, afhængigt af opsætningen af ordreopfyldningen. Når opfyldningsstatussen er nulstillet, kan medarbejderne i butikken se ordrelinjerne på POS'et.

## <a name="line-quantity-tracking"></a>Sporing af linjeantal

En enkelt ordrelinje med et antal, der er større end en, kan behandles med tiden, hvilket medfører flere underordnede tilstande for ordrelinjer. Hvis f.eks. en byggefirma har et projekt, der kræver 500 plader, men byggefirmaet kun vil afhente nogle få plader ad gangen eller få dem leveret i løbet af projektet, kan der være plader, der skal plukkes, pakkes og afsendes på samme tid.

Hver gang der vælges en linje, udfyldes det resterende antal for linjen automatisk, idet det antages, at det resterende antal behandles. I eksemplet ovenfor, hvis 200 plader er blevet plukket, og linjen for pladerne er markeret til pluk, bliver det resterende antal på 300 automatisk angivet i feltet Antal. Det samme gælder, hvis der allerede er faktureret 200 plader. I så fald bliver kun det resterende antal udfyldt automatisk.

I eksemplet ovenfor, hvis 200 plader markeres som pakket, og levering er valgt, bliver det fulde antal på 500 automatisk udfyldt. Hvis kun 200 plader leveres, antages det, at de tidligere pakkede plader er ved at blive afsendt, og det pakkede antal reduceres. Hvis 201 plader leveres, reduceres antallet af pakkede plader først med den resterende enkelte plade, som det resterende antal nedbringes med.

## <a name="line-statuses"></a>Linjestatusser

Ordrelinjer på POS'et har flere statusser, som afspejler tilstanden for ordrelinjen. Statusser på POS'et og i administrationen er ikke ens i alle tilfælde. Status for ordrelinjen kan ses fra POS'et ved hjælp af ordreopfyldningsoperationerne. I administrationen fremgår ordrelinjerne af ordreoplysningerne. Der er adgang til ordreoplysningerne via **Retail og Commerce** \> **Kunder** \> **Alle kundeordrer**. Vælg **Ordre-id** for at se ordreoplysningerne. Fra ordreoplysningerne skal du vælge fanen **Salgsordre** og derefter vælge **Detaljeret status** under underoverskriften **Vis**.

- **Afventer** – Ordrelinjer, der er tildelt til en butik, men som endnu ikke er accepteret, har status **Afventer**, når de vises på POS'et. Linjer, der afventer accept på POS'et, får status **Ordrebehandling** i administrationen.
- **Accepteret** – Ordrelinjer, der er accepteret manuelt eller automatisk, har status **Accepteret**, når de vises på POS'et. Linjer med status **Accepteret** vises som **Ordrebehandling** i administrationen.
- **Pluk** – Linjer, der i øjeblikket plukkes på butiksniveau, har status **Pluk**. Når de samme linjer vises i administrationen, bliver de vist som **Ordrebehandling**.
- **Plukket** og **Delvist plukket** – Linjer, der er plukket eller delvist plukket på POS'et får status **Plukket** eller **Delvist plukket**. De samme linjer i administrationen vises også som **Plukket** eller **Delvist plukket**.
- **Pakket** og **Delvist pakket** – Linjer, der er pakket eller delvist pakket på POS'et får status **Pakket** eller **Delvist pakket**. De samme linjer i administrationen vises også som **Leveret** eller **Delvist leveret**.
- **Delvist faktureret** – Linjer, der er delvist afhentet eller delvist leveret, får status **Delvist faktureret** på POS'et og i administrationen.
- **Faktureret** – Linjer, der er fuldt faktureret på POS'et, vises ikke længere til opfyldning. I administrationen er status for disse linjer **Faktureret**.

## <a name="order-fulfillment-filtering"></a>Ordreopfyldningsfiltrering

Ordreopfyldning på POS'et omfatter filtrering, så brugerne nemt kan finde det, de har brug for. Filtre kan ændres via handlingsruden nederst på skærmbilledet **POS**. Som standard anvendes et **Leveringstype**-filter, baseret på hvordan operationen er konfigureret. Hvis operationen er konfigureret med parameteren **Alle ordrer**, anvendes dette filter ved adgang til ordreopfyldning. Det samme gælder for parametrene **Afhentning i butik** og **Afsend fra butik**. Andre filtre, der kan anvendes til ordreopfyldningsvisningen, omfatter:

- Kundenummer
- Kundenavn
- Kundens mail
- Ordrenummer
- Leveringsmåde
- Kvitteringsnummer
- Id for kanalreference
- Nummer på oprindelig butik
- Linjestatus
- Oprettet dato
- Leveringsdato
- Modtagelsesdato
