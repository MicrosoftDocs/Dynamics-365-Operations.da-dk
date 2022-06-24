---
title: Sky- og kantskaleringsenheder til arbejdsbyrder i warehouse management
description: Denne artikel indeholder oplysninger om funktionen, der gør det muligt for skaleringsenheder at køre udvalgte processer fra din arbejdsbyrde i warehouse management.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, InventTransferOrders, SalesTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f9839ad9a18eb543734c2ba43a56b568460a64c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893491"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Arbejdsbelastninger i forbindelse med Warehouse Management for sky- og edge-skaleringsenheder

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ikke alle forretningsfunktioner i Warehouse Management understøttes fuldt ud på lagersteder, der kører en arbejdsbyrde på en skaleringsenhed. Sørg for kun at bruge de processer, som denne artikel direkte beskriver som understøttede.

## <a name="warehouse-execution-on-scale-units"></a>Lagerudførelse på skaleringsenheder

Warehouse management-arbejdsbelastninger giver mulighed for, at der kan køres sky- og kantskalaenheder, så udvalgte processer køres fra funktionerne til Warehouse management.

## <a name="prerequisites"></a>Forudsætninger

Før du begynder at arbejde med arbejdsbyrden i lokationsstyring, skal systemet være forberedt som beskrevet i dette afsnit.

### <a name="deploy-a-scale-unit-with-the-warehouse-management-workload"></a>Udrulle en skalaenhed med arbejdsbyrde for lokationsstyring

Du skal have en Dynamics 365 Supply Chain Management-hub og en skaleringsenhed, der er implementeret med arbejdsbyrden for warehouse management. Du kan finde flere oplysninger om arkitekturen og installationsprocessen i [Skaler enheder i en distribueret hybridtopologi](cloud-edge-landing-page.md).

### <a name="turn-on-required-features-in-feature-management"></a>Aktivere påkrævede funktioner i funktionsstyring

I arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) skal du aktivere begge disse funktioner. (Begge funktioner er opført under modulet *Lokationsstyring*).

- Afkobl læg på lager-arbejde fra ASN'er
- (Forhåndsversion) Understøttelse af skalaenhed til indgående og udgående lagerstedsordrer

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Sådan fungerer udførelse af lagerstedsarbejdsbyrde på skaleringsenheder

I forbindelse med processerne i arbejdsbyrden for Warehouse Management synkroniseres dataene mellem hubben og skaleringsenhederne.

En skaleringsenhed kan kun vedligeholde de data, som den ejer. Dataejerskabsbegrebet for skaleringsenheder medvirker til at forhindre multimasterkonflikter. Det er derfor vigtigt, at du forstår, hvilke procesdata der ejes af hubben, og hvilke som ejes af skaleringsenhederne.

Afhængigt af forretningsprocesserne kan samme datapost skifte ejer mellem hub og skaleringsenheder. Du kan se et eksempel på dette scenario i følgende afsnit.

> [!IMPORTANT]
> Nogle data kan oprettes både på hub'en og på vægtenheden. Det kan f.eks. være **id'er** og **batchnumre**. Der findes til den givne konflikthåndteringer i tilfælde af et scenario, hvor den samme entydige post både oprettes på hub'en og en vægtenhed under samme synkroniseringscyklus. Når det sker, mislykkes den næste synkronisering, og du skal gå til **Systemadministration > Forespørgsler > Forespørgsler > Dubletter af poster**, hvor du kan få vist og flette dataene.

## <a name="outbound-process-flow"></a>Udgående procesflow

Før du udruller en arbejdsbyrde for lokationsstyring på en sky- eller edge-skaleringsenhed, skal du sørge for, at funktionen *Skaler enhedssupport til frigivelse til lagersted af udgående ordrer* er aktiveret i din virksomhedshub. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Warehouse Management*
- **Funktionsnavn:** *Skaler enhedssupport til frigivelse til lagersted af udgående ordrer*

Den udgående dataejerproces afhænger af, om du bruger belastningsplanlægningsprocessen. I alle tilfælde ejer hub *kildedokumenterne*, f.eks. salgsordrer og flytteordrer, ordrefordelingsprocessen og de relaterede ordretransaktionsdata. Men når du bruger belastningsplanlægningsprocessen, oprettes belastningerne i hub og ejes derfor i begyndelsen af hub. Som en del af processen for *frigivelse til lagersted* overføres ejerskabet af belastningsdataene til den tildefinerede implementering af vægtenheden, som vil blive ejer af den efterfølgende *behandling af forsendelser* (f.eks. arbejdsfordeling, opfyldningsarbejde og oprettelse af efterspørgselsarbejde). Lagerarbejdere kan derfor kun behandle udgående salgs- og flytteordrearbejde ved hjælp af en mobilapp til Warehouse Management, der er knyttet til den installation, der kører den specifikke arbejdsbyrde for vægtenheden.

Så snart den endelige arbejdsproces placerer lagerbeholdningen på en endelig forsendelseslokation (Baydoor), signalerer skaleringsenheden til hubben om at opdatere lagertransaktionerne for kildedokumentet til *Plukket*. Indtil denne proces køres og synkroniseres tilbage, reserveres den lagerbaserede arbejdsbyrde på lagerstedsniveau fysisk, og du kan med det samme behandle den udgående forsendelsesbekræftelse uden at vente på, at denne synkronisering fuldføres. Den efterfølgende salgs følgeseddel og fakturering eller flytteordreforsendelse for aflæsningen håndteres i hubben.

I følgende diagram vises udgående processer, og det angives, hvor de enkelte forretningsprocesser finder sted. (Vælg diagrammet for at markere det.)

[![Udgående behandlingsflow.](media/wes_outbound_warehouse_processes-small.png "Udgående behandlingsflow")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Udgående behandling med planlægning af last

Når du bruger proces til planlægning af belastninger, oprettes der belastninger og forsendelser i hub'et, og ejerskabet af dataene overføres til vægtenhederne som en del af processen for *frigivelse til lagersted*, som det er illustreret i nedenstående illustration.

![Udgående behandling med planlægning af last.](./media/wes_outbound_processing_with_load_planning.png "Udgående behandling med planlægning af last")

### <a name="outbound-processing-without-load-planning"></a>Udgående behandling uden planlægning af last

Når du ikke bruger belastningsplanlægningsprocessen, oprettes der forsendelser på vægtenhederne. Der oprettes også belastninger på vægtenhederne som en del af bølgeprocessen.

![Udgående behandling uden planlægning af last.](./media/wes_outbound_processing_without_load_planning.png "Udgående behandling uden planlægning af last")

## <a name="inbound-process-flow"></a>Indgående procesflow

Hubben ejer følgende data:

- Alle kildedokumenter, f.eks. indkøbsordrer og produktionsordrer
- Indgående lastbehandling
- Alle opdateringer af omkostning og økonomi

> [!NOTE]
> Det indgående indkøbsordreflow er grundlæggende forskelligt fra det udgående flow. Du kan operere det samme lagersted på enten skaleringsenheden eller hubben, afhængigt af om indkøbsordren er frigivet til lagerstedet. Når du har frigivet en ordre til lagerstedet, kan du kun arbejde med den pågældende ordre, når du er logget på skaleringsenheden.
>
> Hvis du bruger *Frigiv til lagersted* som proces, oprettes der [*lagerstedsordrer*](cloud-edge-warehouse-order.md), og ejerskabet af det tilknyttede modtagelsesflow tildeles til skaleringsenheden. Hubben kan ikke registrere indgående modtagelse.

Du skal logge på hubben for at bruge *Frigiv til lagersted*-processen. Mht købsordrebehandling skal du gå til en af følgende sider for at køre eller planlægge det:

- **Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer > Lagersted > Handlinger > Frigiv til lagersted**.
- **Warehouse Management > Frigiv til lagersted > Automatisk frigivelse af indkøbsordrer**

Når du bruger **Automatisk frigivelse af indkøbsordrer**, kan du vælge bestemte indkøbsordrelinjer ud fra en forespørgsel. Det vil typisk være at konfigurere et tilbagevendende batchjob, der frigiver alle de bekræftede indkøbsordrelinjer, der forventes at ankomme næste dag.

Arbejderne kan køre modtagelsen ved hjælp af mobilappen Warehouse Management, der er tilknyttet skaleringsenheden. Dataene registreres derefter af skaleringsenheden og rapporteres i forhold til den indgående lagerordre. Oprettelsen og afviklingen af det efterfølgende læg på lager-arbejde vil også blive håndteret af skaleringsenheden.

Hvis du ikke bruger processen *frigivelse til lagersted*, og du derfor ikke bruger *lagerordrer*, kan hubben behandle lagermodtagelse og arbejde uafhængigt af skaleringsenheder.

![Indgående procesflow.](./media/wes-inbound-ga.png "Indgående procesflow")

Når en arbejder registrerer indgående registrering ved hjælp af en modtagelsesproces i Warehouse Management-mobilappen i forhold til vægtenheden, registreres der en tilgang i forhold til den tilknyttede lagerstedsordre, som gemmes på vægtenheden. Arbejdsbyrden for vægtens enhed signalerer derefter til hub'en, om de relaterede indkøbsordrelinjetransaktioner opdateres til *Registreret*. Når dette er gjort, kan du køre en indkøbsordreproduktkvittering på hubben.

I følgende diagram vises indgående processer, og det angives, hvor de enkelte forretningsprocesser finder sted. (Vælg diagrammet for at markere det.)

[![Indgående behandlingsflow](media/wes_inbound_warehouse_processes-small.png "Indgående behandlingsflow")](media/wes_inbound_warehouse_processes.png)

## <a name="production-control"></a>Produktionsstyring

Arbejdsbyrden for lokationsstyring understøtter følgende tre produktionsflow i appen Warehouse Management:

- Færdigmeld, og læg på lager
- Start produktionsordre
- Registrer materialeforbrug

### <a name="report-as-finished-and-put-away"></a>Færdigmeld, og læg på lager

Arbejderne kan bruge flowet **Færdigmeld, og læg på lager** i appen Warehouse Management til at færdigmelde en produktions- eller batchordre. De kan også færdigmelde samprodukter og biprodukter i en batchordre. Når et job er færdigmeldt, genererer systemet normalt læg på lager-arbejde på skalaenheden. Hvis du ikke kræver læg på lager-arbejde, kan du konfigurere dine arbejdspolitikker til at udelade det.

### <a name="start-production-order"></a>Start produktionsordre

Arbejderne kan bruge flowet **Start produktionsordre** i appen Warehouse Management til at registrere starten af en produktions- eller batchordre.

### <a name="register-material-consumption"></a>Registrer materialeforbrug

Arbejderne kan bruge flowet **Registrer materialeforbrug** i appen Warehouse Management til at rapportere materialeforbrug for en produktions- eller batchordre. Der oprettes derefter en pluklistekladde for det rapporterede materiale på produktions- eller batchordren på skalaenheden. Kladdelinjerne foretager en fysisk reservation af det forbrugte lager. Når data synkroniseres mellem skalaenheden og hub'en, genereres der en pluklistekladde, som bogføres på hub-forekomsten.

## <a name="supported-processes-and-roles"></a>Understøttede processer og roller

Ikke alle processer til Warehouse Management understøttes i en udførelse af lagerstedsarbejdsbyrde på en skaleringsenhed. Det anbefales derfor, at du tildeler roller, der stemmer overens med de funktioner, der er tilgængelige for de enkelte brugere.

For at lette denne proces inkluderes en eksempelrolle med navnet *Lagerchef på arbejdsbyrde* i demodataene i **Systemadministration \> Sikkerhed \> Sikkerhedskonfiguration**. Formålet med denne rolle er at gøre det muligt for lagercheferne at få adgang til udførelse af lagerstedsarbejdsbyrde på skaleringsenheden. Rollen giver adgang til de sider, der er relevante i forbindelse med en arbejdsbyrde, der har en skaleringsenhed som vært.

Brugerroller på en skaleringsenhed tildeles som en del af den første datasynkronisering fra hubben til skaleringsenheden.

Hvis du vil redigere de roller, der er tildelt til en bruger, skal du gå til **Systemadministration \> Sikkerhed \> Tildele brugere til roller**. Brugere, der kun fungerer som lagerchefer på skaleringsenheder, bør kun tildeles rollen *Lagerchef på arbejdsbyrde*. Denne fremgangsmåde sikrer, at de pågældende brugere kun har adgang til de understøttede funktioner. Fjern eventuelle andre roller, der er tildelt til disse brugere.

Brugere, der kun fungerer som lagerchefer på både hubben og skaleringsenheder, bør tildeles den eksisterende rolle *Lagerarbejder*. Bemærk, at denne rolle giver lagerarbejderne adgang til funktioner (f.eks. modtagelsesbehandling af flytteordre), der vises i brugergrænsefladen, men ikke understøttes i øjeblikket på skaleringsenheder.

### <a name="supported-warehouse-execution-processes"></a>Understøttede afviklingsprocesser for lagersteder

Følgende processer til lagerudførelse kan aktiveres for en udførelse af lagerstedsarbejdsbyrde på en skaleringsenhed:

- Udvalgte metoder til salgs- og flytteordrer (validering, oprettelse af last, fordeling, efterspørgselsopfyldning, containerisering, oprettelse af arbejde og udskrivning af label til bølge)

- Behandle arbejde med salgs- og flytteordrelagersteder ved hjælp af lagerstedsappen (herunder genopfyldningsarbejde)
- Forespørge på disponibel lagerbeholdning ved hjælp af lagerstedsappen
- Oprette og køre lagerbevægelser ved hjælp af lagerstedsappen
- Oprette og behandle procesoptællingsarbejde ved hjælp af lagerstedsappen
- Foretage lagerreguleringer ved hjælp af lagerstedsappen
- Registrere indkøbsordrer og udføre læg på lager-arbejde med lagerstedsappen

Følgende arbejdstyper kan oprettes på en vægtenhed og kan derfor behandles som en del af en udførelse af lagerstedsarbejdsbyrde:

- **Lagerbevægelser** - manuel bevægelse og bevægelse efter skabelonarbejde.
- **Cyklusoptælling** - herunder en afvigende godkendelses- og afvisningsproces som en del af optællingsoperationer.
- **Indkøbsordrer** - læg på lager-arbejde via en lagerstedsordre, når indkøbsordrer ikke er tilknyttet laster.
- **Salgsordrer** - simpelt pluk- og lastarbejde.
- **Overførselskvittering** – Via nummerplade, der modtages.
- **Overfør afgang** – Simpel pluk og indlæsning.
- **Genopfyldning** - uden råvarer til produktion.
- **Færdigvarer, der er blevet lagt på lager** – Efter produktionsprocessen for færdigmeldingen.
- **Med-produkt og under-produkt, der er lagt væk** – Efter produktionsprocessen er færdigmeldt.
<!-- - **Packed container picking** - After manual packing station processing. -->

Ingen anden behandling af kildedokument eller lagerstedsarbejde understøttes i øjeblikket på skaleringsenheder. Når du f.eks. kører i forhold til en lagerstedsudførelsesbelastning på en skalaenhed, kan du ikke bruge processen til modtagelse af salgsreturordrer til at behandle returordrer. I stedet skal denne behandling udføres af hub-forekomsten.

> [!NOTE]
> Menupunkter og knapper til mobilenheder til funktioner, der ikke understøttes, vises ikke i _mobilappen Warehouse Management_, når den er knyttet til en implementering af skaleringsenhed.
>
> Der kræves et par ekstra trin at konfigurere mobilappen Warehouse Management til at arbejde i en sky- eller edge-skalaenhed. Du kan finde flere oplysninger under [Konfigurere mobilappen Warehouse Management til sky- og edge-skaleringsenheder](cloud-edge-workload-setup-warehouse-app.md).
>
> Når du kører en arbejdsbyrde i en skaleringsenhed, kan du ikke køre processer, der ikke understøttes, for det specifikke lagersted på hubben. Tabellerne senere i denne artikel dokumenterer de understøttede egenskaber.
>
> Valgte arbejdstyper for lagersteder kan oprettes både på hubben og skaleringsenheder, men kan kun vedligeholdes af ejerhubben eller -skaleringsenheden (den installation, der har oprettet dataene).
>
> Selv når en bestemt proces understøttes i skaleringsenheden, skal du være opmærksom på, at alle nødvendige data muligvis ikke bliver synkroniseret fra hubben til skaleringsenheden eller fra skaleringsenheden til hubben, hvilket udgør en risiko for uventet systembehandling. Eksempler på dette scenario omfatter:
>
> - Hvis du bruger en forespørgsel om lokationsvejledning, der tilknytter en datatabelpost, som kun findes i hubimplementeringen.
> - Hvis du bruger lokationsstatus og/eller lokationsmængder som lastfunktioner. Disse data synkroniseres ikke mellem implementeringerne og vil derfor kun fungere, når lokationslagerbeholdningen opdateres for en af installationerne.

Følgende warehouse management-funktioner understøttes ikke i øjeblikket i arbejdsbelastninger på skaleringsenheder:

- Indgående behandling af indkøbsordrelinjer, der er tilknyttet en last.
- Indgående behandling af indkøbsordrer for et projekt.
- Administration af landingsomkostninger, der bruger rejser, og sporing af varer undervejs.
- Indgående og udgående behandling af varer, der har aktive sporingsdimensioner **Ejer** og/eller **Serienummer**.
- Behandling af lager, der har en blokeringsstatusværdi.
- Ændring af lagerstatus under en hvilken som helst arbejdsbevægelsesproces.
- Ordrebekræftede fleksible reservationer for dimension på lagerstedsniveau.
- Brug af funktionen *Lokationsstatus for lagersted* (dataene synkroniseres ikke mellem implementeringerne).
- Brug af funktionen *Placering af lokations-id*.
- Brug af *Produktfiltre* og *Produktfiltergrupper*, herunder indstillingen **Antal dage til at sammensætte batches**.
- Integration med kvalitetsstyring.
- Behandling med fastvægtvarer.
- Behandling med varer, der kun er aktiveret til transportstyring (TMS).
- Behandling med negativ disponibel lagerbeholdning.
- Datadeling af produkter på tværs af firma. <!-- Planned -->
- Behandling af lagerstedsarbejde med forsendelsesnoter (f.eks. følgesedler på pakkestation).
- Billeder af produktmasterdata (f.eks. på mobilappen Warehouse Management).
- Behandling af lagerstedsarbejde med materialehåndtering/warehouse automation.

> [!WARNING]
> Nogle af lagerstedsfunktionerne er ikke tilgængelige for lagersteder, der kører arbejdsbyrderne for Warehouse Management på en skaleringsenhed, og de understøttes heller ikke i hubben eller i arbejdsbyrden for skaleringsenheden.
>
> Andre egenskaber kan behandles på begge, men vil kræve nøje brug i visse scenarier, f.eks. når lagerbeholdning opdateres for det samme lagersted på både hubben og skaleringsenheden på grund af den asynkrone dataopdateringsproces.
>
> Specifikke funktioner (som f.eks. *blokringsarbejde*), der understøttes på både hubben og skaleringsenheder, vil kun blive understøttet for ejeren af dataene.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Udgående (kun understøttet for salgsordrer og flytteordrer)

I følgende tabel vises, hvilke udgående funktioner der understøttes, og hvor de understøttes, når arbejdsbelastningen for Warehouse Management bruges i sky- og kantskaleringsenheder.

| Behandling                                                      | Hub | Udførelse af lagerstedsarbejdsbyrde på skaleringsenheder |
|--------------------------------------------------------------|-----|------------------------------|
| Behandling af kildedokument                                   | Ja | Nej |
| Last- og transportstyringsbehandling                | Ja, men kun processerne til belastningsplanlægning. Behandlingen af transportstyring understøttes ikke  | Nej |
| Frigiv til lagersted                                         | Ja | Nej |
| Planlagt direkte levering                                        | Nej  | Nej |
| Konsolidering af forsendelse                                       | Ja, når du bruger belastningsplanlægning | Ja |
| Behandling af forsendelsesbølge                                     | Nej  |Ja, undtagen **Indlæs bygning og sortering** |
| Vedligeholde forsendelser for bølge                                  | Nej  | Ja|
| Lagerstedsbehandling (inkl. udskrivning af nummerplade)        | Nej  | Ja, men kun for ovennævnte understøttede egenskaber |
| Klyngepluk                                              | Nej  | Ja|
| Manuel behandling af pakkestation  | Nej  | Nej |
| Behandling af udgående sortering                                  | Nej  | Nej |
| Udskrivning af lastrelaterede dokumenter                           | Ja | Ja|
| Fragtseddel og ASN-generering                            | Nej  | Ja|
| Forsendelsesbekræftelse                                             | Nej  | Ja|
| Forsendelsesbekræftelse med "Bekræft og flyt"            | Nej  | Ja|
| Behandling af følgesedler og fakturering                        | Ja | Nej |
| Kort pluk (salgs- og flytteordrer)                    | Nej  | Ja, uden at fjerne reservationer for kildedokumenter|
| Overpluk (salgs- og flytteordrer)                     | Nej  | Ja|
| Konsolider id'er                                   | Nej  | Ja|
| Ændring af arbejdssteder (salgs- og flytteordrer)         | Nej  | Ja|
| Fuldføre arbejde (salgs- og flytteordrer)                    | Nej  | Ja|
| Udskrive arbejdsordrerapport                                            | Ja | Ja|
| Bølgelabel                                                   | Nej  | Ja|
| Arbejdsopdeling                                                   | Nej  | Ja|
| Arbejdsbehandling – Styres af "Lastning af transport"            | Nej  | Nej |
| Reducer det antal, der er plukket                                       | Nej  | Ja|
| Tilbagefør arbejde                                                 | Nej  | Ja|
| Tilbagefør forsendelsesbekræftelse                                | Nej  | Ja|
| Anmode om annullering af ordrelinjer på lagersted                      | Ja | Nej, men anmodningen godkendes eller afvises |
| <p>Frigiv flytteordrer til modtagelse</p><p>Denne proces vil automatisk finde sted som en del af forsendelsesprocessen for flytteordren. Den kan dog bruges manuelt til at aktivere modtagelse af nummerplader med en skalaenhed, hvis indgående lagerstedsordrelinjer er blevet annulleret, eller som en del af en ny udrulningsproces for arbejdsbyrder.</p> | Ja | Nej|
<!--| Manuel behandling på pakkestation, herunder arbejdet "Plukning af pakket container"  | Nej  | Ja, men uden TMS-forsendelsesmanifest og bogføring af salgsfølgesedlen og uden pakkenoter og produktbilleder |-->

### <a name="inbound"></a>Indgående

I følgende tabel vises, hvilke indgående funktioner der understøttes, og hvor de understøttes, når arbejdsbelastningen for Warehouse Management bruges i sky- og kantskaleringsenheder.

| Behandling                                                          | Hub | Udførelse af lagerstedsarbejdsbyrde på skaleringsenheder<BR>*(Varer, der er markeret "Ja", gælder kun for lagerstedsordrer)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Behandling&nbsp;af&nbsp;kildedokument                             | Ja | Nej |
| Last- og transportstyringsbehandling                    | Ja | Nej |
| Modtagelse af varer undervejs og landingsomkostninger                       | Ja | Nej |
| Bekræftelse af indgående forsendelse                                    | Ja | Nej |
| Frigivelse af indkøbsordre til lagersted (behandling af lagerstedsordre) | Ja | Nej |
| Anmode om annullering af ordrelinjer på lagersted                            | Ja | Nej, men anmodningen godkendes eller afvises |
| Behandle produktkvittering for indkøbsordres kildedokument                         | Ja | Nej |
| Indkøbsordrevare til modtagelse og læg på lager                       | <p>Ja,&nbsp;når&nbsp;der&nbsp;ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, når en indkøbsordre ikke er del af en <i>last</i></p> |
| Indkøbsordrelinje til modtagelse og læg på lager                       | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, når en indkøbsordre ikke er del af en <i>last</i></p></p> |
| Modtagelse af returordre og placering på lager                              | Ja | Nej |
| Modtagelse af blandede id'er og placering på lager                       | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ja |
| Modtagelse af varelast                                              | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Indkøbsordre-id til modtagelse og læg på lager              | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Flytteordre-id til modtagelse og læg på lager             | Nej | Ja |
| Modtagelse af vare i flytteordre og placering på lager                       | Ja | Nej |
| Flytteordrelinje til modtagelse og placering på lager                       | Ja | Nej |
| Indkøbsordre, der modtages med underlevering                      | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ja, men kun ved at foretage en annulleringsanmodning fra hubben |
| Indkøbsordre, der modtages med overlevering                       | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ja  |
| Modtagelse med oprettelse af *Cross-docking*-arbejde                 | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse med oprettelse af *Kvalitetsordre*-arbejde                  | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse med oprettelse af *Kvalitetsvareprøve*-arbejde          | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse med oprettelse af *Kvalitet i kvalitetskontrol*-arbejde       | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Modtagelse med oprettelse af kvalitetsordre                            | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Nej |
| Arbejdsbehandling – Styres af *Læg på lager-klynge*                 | Ja | Nej |
| Arbejdsbehandling med *Kort pluk*                               | Ja | Nej |
| Annuller arbejde (indgående)                                            | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | <p>Ja, men kun når indstillingen <b>Fjern registrering af modtagelse, når du annullerer arbejde</b> på siden <b>Parametre til lokationsstyring</b> er ryddet</p> |
| Indlæsning af nummerplade                                           | Ja | Ja |

### <a name="warehouse-operations-and-exception-handing"></a>Lagerstedsoperationer og håndtering af undtagelser

I følgende tabel vises, hvilke funktioner til håndtering af lageroperationer og undtagelser der understøttes, og hvor de understøttes, når arbejdsbelastningen for Warehouse Management bruges i sky- og kantskaleringsenheder.

| Behandling                                            | Hub | Udførelse af lagerstedsarbejdsbyrde på skaleringsenheder |
|----------------------------------------------------|-----|------------------------------|
| Forespørge på nummerplade                              | Ja | Ja                          |
| Vareforespørgsel                                       | Ja | Ja                          |
| Lokationsforespørgsel                                   | Ja | Ja                          |
| Skift lagersted                                   | Ja | Ja                          |
| Bevægelse                                           | Ja | Ja                          |
| Bevægelse efter skabelon                               | Ja | Ja                          |
| Overførsel af lagersted                                 | Ja | Nej                           |
| Oprette flytteordre fra lagerstedsappen           | Ja | Nej                           |
| Regulering (ind/ud)                                | Ja | Ja, men ikke for det udreguleringsscenarie, hvor lagerreservationen skal fjernes ved hjælp af indstillingen **Fjern reservationer** for lagerreguleringstyperne</p>                           |
| Ændring af lagerstatus                            | Ja | Nej                           |
| Behandling af cyklusoptælling og optællingsafvigelser | Ja | Ja                           |
| Genudskrive etiket (udskrive nummerplade)             | Ja | Ja                          |
| Id-build                                | Ja | Nej                           |
| Id-pause                                | Ja | Nej                           |
| Pak til indlejrede id'er                      | Ja | Nej                           |
| Chaufførens check-in                                    | Ja | Nej                           |
| Chaufførens check-ud                                   | Ja | Nej                           |
| Skifte batchdispositionskode                      | Ja | Ja                          |
| Vis oversigt over åbne opgaver                             | Ja | Ja                          |
| Behandling af min./maks. og zonetærskelopfyldning| Ja <p>Anbefalingen er ikke at medtage de samme lokationer som en del af forespørgslerne</p>| Ja                          |
| Behandle allokeringsgenopfyldning                  | Ja  | Ja<p>Bemærk, at opsætningen skal udføres på skaleringsenheden</p>                           |
| Blokere og fjerne blokering af arbejde                             | Ja | Ja                          |
| Skift bruger                                        | Ja | Ja                          |
| Skift arbejdspulje på arbejde                           | Ja | Ja                          |
| Annuller arbejde                                        | Ja | Ja                          |

### <a name="production"></a>Produktion

I følgende tabel vises en oversigt over produktionsscenarier for warehouse management, der (ikke) understøttes i øjeblikket i arbejdsbelastninger på skaleringsenheder.

| Behandling | Hub | Udførelse af lagerstedsarbejdsbyrde på skaleringsenheder |
|---------|-----|----------------------------------------------|
| Behandling af kildedokument til produktionsordre    | Ja | Nej |
| Frigiv til lagersted                           | Ja | Nej |
| Start produktionsordre                         | Ja | Ja|
| Oprette lagerstedsordrer                        | Ja | Nej |
| Anmode om annullering af ordrelinjer på lagersted        | Ja | Nej, men anmodningen godkendes eller afvises |
| Færdigmelde og lægge færdigvarer på lager | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ja|
| Samprodukt og biprodukt, læg på lager             | <p>Ja, når der ikke er en lagerordre</p><p>Nej, når der er en lagerordre</p> | Ja|
| Registrer materialeforbrug                  | Ja | Ja|
| Produktionsbølgebehandling                     | Ja | Nej |
| Råvarepluk                           | Ja | Nej |
| Kanban-læg på lager                                | Ja | Nej |
| Kanban-pluk                                 | Ja | Nej |
| Tøm kanban                                   | Ja | Nej |
| Produktionsspild                               | Ja | Nej |
| Sidste produktionspalle                         | Ja | Nej |
| Genopfyldning af råvarer                     | Nej  | Nej |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Vedligeholde skaleringsenheder til lagerstedsudførelse

Flere batchjob kører på både hubben og skaleringsenheder.

Under installationen af hub kan du vedligeholde følgende batchjob manuelt:

- Administrer følgende batchjob i **Lokationsstyring \> Periodiske opgaver \> Backoffice-styring af arbejdsbyrder**:

    - Skaleringsenhed til meddelelsesprocessors hub
    - Registrer kvitteringer på kildeordre
    - Fuldfør lagerstedsordrer
    - Generér manglende udgående lagerstedsordrer

- Administrer følgende batchjob i **Lokationsstyring \> Periodiske opgaver \> Styring af arbejdsbyrder**:

    - Meddelelsesprocessor for lagerstedshub til skaleringsenhed
    - Udfør behandling af lagerstedsordrelinjekvitteringer for bogføring af lagerstedskvittering

Ved udrulninger af skaleringsenheder kan du administrere følgende batchjob i **Lokationsstyring \> Periodiske opgaver \> Styring af arbejdsbyrder**:

- Behandl bølgetabelposter
- Meddelelsesprocessor for lagerstedshub til skaleringsenhed
- Udfør behandling af lagerstedsordrelinjekvitteringer for bogføring af lagerstedskvittering

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
