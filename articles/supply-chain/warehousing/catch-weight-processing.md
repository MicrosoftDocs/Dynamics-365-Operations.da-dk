---
title: Behandling af fastvægtprodukter med lokationsstyring
description: I dette emne beskrives, hvordan du kan bruge arbejdsskabeloner og lokationsvejledninger til at bestemme, hvordan og hvor arbejde skal udføres på lageret.
author: perlynne
manager: tfehr
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: b1d106fa6fe5072eb74813495253731dd988c376
ms.sourcegitcommit: 9a0be1ceee90e80f4c75f241aba847547b5032e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2020
ms.locfileid: "3693273"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Behandling af fastvægtprodukter med lokationsstyring

[!include [banner](../includes/banner.md)]


## <a name="feature-exposure"></a>Visning af funktioner

Når du vil bruge lokationsstyring til at behandle fastvægtprodukter, skal du bruge en licenskonfigurationsnøgle til at aktivere funktionen. Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**. Klik derefter på fanen **Konfigurationsnøgler**, udvid **Handel \> Lagersted- og transportstyring**, og marker afkrydsningsfeltet for **Fastvægt til lagersted**.

> [!NOTE]
> Både **Lagersted- og transportstyring**-licenskonfigurationsnøglen og **Procesdistribution \> Fastvægt**-licenskonfigurationsnøglerne skal være aktiveret. Hvis du vil angive konfigurationsnøgler for fastvægt, skal du også aktivere funktionen ved hjælp af arbejdsområdet **Funktionsstyring**. Den hovedfunktion, der skal slås til, er **Behandling af fastvægtprodukter med lokationsstyring**. To relaterede, men valgfrie funktioner, som du måske vil aktivere, er **Ændringer af lagerstatus for fangstvægtprodukter** og **Brug eksisterende fangstvægtkoder, når produktionsordrer færdigmeldes**.

Når licenskonfigurationsnøglen er aktiveret, og du opretter et frigivet produkt, kan du vælge **Fastvægt**. Du kan også knytte det frigivne produkt til en lagerdimensionsgruppe, som parameteren **Brug lokationsstyringsprocesser** er markeret for.

Før du kan bruge produktet i Lokationsstyring, skal du udføre en grundlæggende produktspecifik opsætning for fastvægt:

- Definer omregning af nominel vægt mellem fastvægtenheden (boks) og lagerenheden (kilogram \[kg\]) som en del af en definition af enhedsomregning.
- Definer minimum- og maksimumvægttolerancer som en del af opsætningen af fastvægtenheden.
- Opret en enhedsseriegruppe, hvor fastvægtenheden defineres som den laveste lagerenhed (SKU).
- Opret en politik for håndtering af fastvægtvarer.

Du kan finde flere oplysninger i [Konfigurere og vedligeholde fastvægtvarer](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Posteringsreguleringer

Da vægten af lagervaren, når den leveres på et lagersted, kan afvige fra vægten, når lagervaren sendes fra lagerstedet, skal behandlingen af fastvægtproduktet regulerer lagervaren.

> [!NOTE]
> Aktivitet af mobilenhed udløser kun transaktionsreguleringer, hvis metoden til beregning af den udgående vægtafvigelse for varens håndteringspolitik for fastvægtvarer er **Tillad vægtafvigelse**.

**Eksempel 1**

Under en **Færdigmelding**-produktionsproces registreres den indgående vægt af et id, der indeholder otte kasser med et fastvægtprodukt, som 80,1 kg. Id'et gemmes derefter i området for færdigvarer, og under oplagringsperioden går noget af vægten tabt.

Vægten af det samme id registreres senere som 79,8 kg som en del af en salgsordreplukproces. Derfor har du nu i systemet en vægtdifference som en del af den fysiske dimensionsopsætning.

I sådanne tilfælde regulerer systemet automatisk forskellen ved at bogføre en postering for de manglende 0,3 kg.

**Eksempel 2**

I definitionen konfigureres et produkt til at acceptere en mindstevægt på 8 kg og en maksimal vægt på 12 kg for fastvægtenheden **Kasse**.

Du har to kasser med produktet, og de har en registreret vægt på 16 kg. Hvis en lagermedarbejder plukker og vejer en af kasserne, og vægten registreres som 9 kg, vejer den resterende kasse 7 kg. Men da 7 kg er under minimumvægten, udfører systemet en automatisk regulering for at øge vægten af den disponible lagerbeholdning med 1 kg.

Du kan konfigurere de konti, som disse reguleringer bogføres til, ved at gå til **Omkostningsstyring \> Konfiguration af politikker for finansintegration \> Bogføring**. Under fanen **Lager** kan du derefter definere følgende konti:

- Fastvægt - tabskonto
- Fastvægt - profitkonto

## <a name="catch-weight-item-handling-policy"></a>Politik for håndtering af fastvægtvarer

Politikken for håndtering af fastvægtvarer definerer to primære lokationsstyringsflow for varerne: Når vægten af varerne registreres, og hvordan den bliver registreret.

Du kan definere, hvornår vægten registreres ved behandling af salgsordrer og flytteordrer. Vægten kan registreres under en af følgende processer:

- **Pluk** – Vægten registreres under de første plukarbejdslinjer i ordrearbejde.
- **Emballering** – Vægten registreres under manuel emballering. (Du skal sende varerne til en pakkestation).

Hvis den faktiske vægt registreres på pakkestationen under containerpakningsprocesser, bliver lagermedarbejdere ikke bedt om at registrere vægten under plukarbejdet. I stedet bruges den gennemsnitlige vægt af den fysiske lagervare som vægt af den plukkede lagervare, der sendes til pakkeområdet. Dette begreb gælder også for fastvægtvarer, der spores efter koder. I forbindelse med kodeporede varer bestemmer disse parametre, hvornår koden registreres. Koden kan registreres på pluktidspunktet vha. mobilenheden eller under den manuelle pakning.

> [!NOTE]
> Da indstillingen **Emballage** medfører, at lageret opdateres med den gennemsnitlige plukkede vægt, kan det udløse en uoverensstemmelse, der kan forårsage en regulering af fastvægtprofit/tab og/eller en difference mellem den disponible lagervægt og fastvægtkoden.

Ved interne lokationsstyringsprocesser, som f.eks. rettelser til optælling og regulering, kan du angive, om vægten skal registreres. Hvis den ikke registreres, bruges den nominelle vægt. Andre indstillinger giver dig mulighed for at registrere vægt pr. fastvægtenhed og pr. optællingsantal.

Du kan også definere, hvordan vægten registreres. I et af de to vigtigste flows spores fastvægtkoder og bruges til at registrere vægten. I det andet flow spores fastvægtkoder ikke.

- **Ja** – Varen bruger fastvægtkoder. Hvert kodenummer repræsenterer én fastvægtenhed (kasse), og en vægt og andre oplysninger knyttes til koden. Ved udgående processer bruges den vægt, der er knyttet til koden.
- **Nej** – Varen bruger ikke fastvægtkoder. De indgående og udgående vejeprocesser er baseret på den faktiske vægt, der registreres under hver proces.

Processen til sporing af fastvægtkoder kan bruges til varer, der ikke ændrer vægt i lagerperioden. Vægten registreres kun i forbindelse med den indgående lagerproces. Under den udgående proces scannes fastvægtkoderne blot, og vægten, der er tilknyttet koderne, bruges til behandlingen af de udgående transaktioner.

En anden vigtig parameter, der er relateret til behandlingen af fastvægtkoder, er **Sporingsmetode til dimensioner af fastvægtkode**. Koder kan være delvist eller fuldt sporet. Hvis en kode er delvist sporet, spores produktdimensioner, sporingsdimensioner og lagerstatus. Hvis en kode er fuldt sporet, spores produktdimensioner, sporingsdimensioner og **alle** lagerdimensioner.

Når en vare kodespores, findes der desuden en parameter til **Registreringsmetode for udgående kode**. Du kan angive denne parameter, så du altid bliver bedt om at angive koden på udgående transaktioner fra mobilenheden. Du kan også angive parameteren, så du kun får besked om koder, når der er brug for dem. Der er f.eks. fem fanstvægtkoder på lageret på et givet id, og du har angivet, at du vil plukke alle fem koder fra id'et. Hvis parameteren for **Registreringsmetode for udgående kode** er angivet til **Spørg kun efter kode, når det er nødvendigt**, plukkes de fem koder automatisk. Du behøver ikke at scanne de enkelte koder. Hvis parameteren er angivet til **Bed altid om kode**, skal du scanne hver enkel kode, selvom alle fem koder plukkes.

> [!NOTE]
> Som regel registreres og opdateres koder kun fra menupunkterne i mobilenheden. Der er dog nogle få situationer, hvor koder registreres et andet sted (f.eks. fra den manuelle pakkestation). Generelt bør menupunkterne i mobilenheden dog bruges til al lageraktivitet, hvis der bruges koder.

### <a name="how-to-capture-catch-weight"></a>Sådan registreres fastvægt

**Når der bruges sporing af fangstvægtkode**, skal der altid oprettes en kode for hver fastvægtenhed, der modtages, og alle koder skal altid være tilknyttet en vægt.

**Kasse** er f.eks. fastvægtenheden, og du modtager en palle med otte kasser. I dette tilfælde skal der oprettes otte entydige fastvægtkoder, og der skal knyttes en vægt til hver kode. Alt efter den indgående fastvægtkode kan vægten af alle de otte kasser registreres, og den gennemsnitlige vægt kan derefter distribueres til hver kasse, eller der kan registreres en entydig vægt for hver kasse.
Når du bruger funktionen **Brug eksisterende fangstvægtkoder, når produktionsordrer færdigmeldes** med den proces, der er aktiveret via et menupunkt i en mobil enhed, opdateres lageret på basis af eksisterende oplysninger om fangstvægtmærkatet. Derfor beder lagerstedsappen dig ikke om at registrere fangstvægtmærkatets data som del af en produktionsrapport som en færdigmeldt handling.

**Når sporing af fastvægtkode ikke bruges**, kan vægten registreres for hver dimensionsopsætning (f.eks. for hvert id og sporingsdimension). Vægten kan også registreres på basis af et samlet niveau, f.eks. fem id-numre (paller).

For metoderne til registrering af udgående vægt giver indstillingen **Pr. fastvægtenhed** dig mulighed for at angive, at vejningen skal udføres for hver fastvægtenhed (f.eks. pr. boks). Med indstillingen **Pr. plukenhed** kan du angive, at vægten skal registreres ud fra det antal, der skal plukkes (f.eks. tre kasser). Bemærk, at hvis indstillingen **Ikke registreret** anvendes, vil den gennemsnitlige vægt for produktionslinjeplukprocesserne og processerne for de interne bevægelse finde anvendelse.

Der defineres metoder til hentning af flere vægter på politikken for håndtering af fastvægtvarer. Hver parameter for metode til hentning af vægt anvendes af forskellige transaktioner. I følgende tabel vises en oversigt over, hvilke parametre der bruges til hvilke transaktioner.

| metode                                     | Postering                                |
|--------------------------------------------|--------------------------------------------|
| Registreringsmetode for udgående vægt           | Salgsplukning, flytteplukning            |
| Vægtregistreringsmetode for produktionspluk | Produktionsplukning, produktionsforbrug |
| Flyttemetode for vægtregistrering           | Bevægelse                                   |
| Tidspunkt for registrering af ændring af vægt       | Reguleringer, optælling                      |
| Registreringsmetode for optællingsvægt           | Tælling                                   |
| Registreringsmetode for vægt af lagerstedsoverførsel | Overførsel af lagersted                         |

Du kan bruge metoden for afvigelser i udgående vægt for at forhindre, at lokationsstyringsplukprocesserne registrerer vægte, der resulterer i reguleringer af overskud/underskud for fastvægt. Metoden til beregning af udgående vægt anvendes under følgende processer for mobilenheder: salgsplukning, flytteplukning, produktionsplukning, flytninger, optælling og lageroverførsler. Du kan bruge indstillingen **Begræns vægtafvigelse**, hvis vægten af fastvægtvaren ikke svinger under opbevaring i lageret, og hvis der ikke kræves regulering af fastvægtgevinst/tab. Du kan bruge indstillingen **Tillad vægtafvigelse**, hvis vægten kan svinge, og hvis der kræves justering af fastvægt for gevinst/tab, når der registreres vægtudsving.

## <a name="unsupported-scenarios"></a>Ikke-understøttede scenarier

Ikke alle arbejdsgange understøtter behandling af fastvægtprodukter med lokationsstyring. Aktuelt gælder følgende begrænsninger. De gælder for alle fastvægtvarer, uanset om de er kodet.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Konfiguration af fastvægtprodukter til lokationsstyringsprocesser

- Kun formelbehandling understøttes for fastvægtprodukter (ikke styklister).
- Fastvægtprodukter kan ikke knyttes til en sporingsdimensionsgruppe ved hjælp af ejerdimensionen.
- Fastvægtprodukter ikke kan bruges som tjenester.
- Fastvægtprodukter kan bruges som "lagerførte produkter", men kun som en del af varemodelgruppen.
- Fastvægtprodukter kan ikke bruges sammen med funktionen til sporing af "Aktiv i salgsproces".
- Fastvægtprodukter kan ikke bruges sammen med funktionen til registrering af serienumre. Derfor kan produkter ikke flyttes fra et "tomt" til et serienummer som en del af pluk/pakningsprocessen.
- Fastvægtprodukter kan ikke bruges sammen med funktionen til registrering af serienumre før forbrug.
- Fastvægtprodukter, hvor varianter er aktiveret, kan ikke bruges sammen med funktionen til konvertering af varianter af måleenheder.
- Fastvægtprodukter kan ikke kodes som en Commerce "produktpakke".
- Fastvægtprodukter kan kun bruges sammen med en enhedsseriegruppe, som har fastvægtmaterialehåndteringsenheder, og som har fastvægtenheden som den laveste serie.
- For fastvægtprodukter kan lagerenheden kun omregnes til fastvægtenheden, hvis omregningen resulterer i et nominelt antal, der er mere end 1.
- Opsætningen af stregkoder for fastvægtprodukter understøtter ikke opsætning af en variabel vægt.

### <a name="order-processing"></a>Ordrebehandling

- Oprettelse af Advance Shipping Notice (ASN/pakkestrukturer) understøtter ikke vægtoplysninger.
- Ordreantallet skal vedligeholdes ud fra fangstvægtenheden.

### <a name="inbound-warehouse-processing"></a>Indgående lagerstedsbehandling

- Modtagelse af id'er kræver, at der tildeles vægte ved registreringen, fordi vægtoplysninger ikke understøttes som en del af Advance Shipping Notice. Når der bruges fastvægtkodeprocesser, skal kodenummeret tildeles manuelt pr. fastvægtenhed.
- Indgående kvalitetskontrol er ikke understøttet for fastvægtprodukter. Hvis det er konfigureret, springes det pågældende kvalitetstjek over.

### <a name="inventory-and-warehouse-operations"></a>Lager- og lokationshandlinger

- Manuel oprettelse af karantæneordrer understøttes ikke for fastvægtprodukter.
- Manuel flytning af lager, der er relateret til åbent arbejde, understøttes ikke for fastvægtprodukter.
- Indlæsning af id for at initialisere lagerstedets lagerbeholdning understøttes ikke for fastvægtprodukter.
- Batchtilpasningsprocesser understøttes ikke for fastvægtprodukter.
- Håndtering af negativt fysisk lager understøttes ikke for fastvægtprodukter.
- Lagermarkering ikke kan bruges til fastvægtprodukter.

### <a name="outbound-warehouse-processing"></a>Udgående lagerstedsbehandling

- Funktionen til pluk af klynger understøttes ikke for fastvægtprodukter.
- Pluk og pak-lagerstedsbehandling understøttes ikke for fastvægtprodukter.
- For fastvægtprodukter kan arbejde, der er defineret i en arbejdsskabelon, ikke køres automatisk.
- For fastvægtprodukter understøtter systemet ikke manuel pakkestationsbehandling, hvor der oprettes emballeret containerplukkearbejde, efter at containere er lukket.
- Funktionen til stykvis scanning understøttes ikke for fastvægtprodukter.

### <a name="production-processing"></a>Produktionsbehandling

- Ved fastvægtprodukter understøttes kun batchordrer for formelprodukter.
- Kanban-funktioner understøttes ikke for fastvægtprodukter.
- Ved fastvægtprodukter kan serienumre ikke registreres før forbrug.
- Funktionen til tilbageførsel af id'er fra produktion understøttes ikke for fastvægtprodukter.
- Ved fastvægtprodukter kan færdigmelding ikke registreres af serienummeret.

### <a name="transportation-management-processing"></a>Transportstyringsbehandling

- Lastopbygningspanelbehandling understøttes ikke for fastvægtprodukter.
- Transportanmodningslinjer understøttes ikke for fastvægtprodukter.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Andre begrænsninger og funktionsmåder for fastvægtproduktbehandling med lokationsstyring

- Under plukprocesser, hvor brugeren ikke bliver bedt om at identificere sporingsdimensioner, udføres vægttildelingen ud fra den gennemsnitlige vægt. Dette sker, når f.eks. en kombination af sporingsdimensioner bruges på samme sted, og når der kun er en sporingsdimensionsværdi tilbage på stedet, efter at en bruger har behandlet pluk.
- Når lageret er reserveret et fastvægtprodukt, der er konfigureret til lokationsstyringsprocesser, foretages reservationen ud fra den mindste vægt, der er defineret, selvom dette antal er det sidste antal til håndtering af beholdningen. Denne funktionsmåde adskiller sig fra funktionsmåden for varer, der ikke er konfigureret til lokationsstyringsprocesser. Der er én undtagelse til denne begrænsning. Ved produktionsplukning, når det sidste håndteringsantal for et fastvægtprodukt, der er serienummerstyret, plukkes, bruges den faktiske vægt.
- Processer, der bruger vægten som en del af kapacitetsberegninger (bølgegrænser, maksimale arbejdspauser, containermaksimumværdier, lokalitetsbelastningskapaciteter osv.), bruger ikke den faktiske vægt af lageret. I stedet er processerne baseret på den fysiske håndteringsvægt, der er defineret for produktet.
- Generelt understøttes Commerce-funktioner ikke for fastvægtprodukter.
- For fastvægtprodukter kan lagerstatus ikke opdateres fra **Ændring af status for lagersted**.

### <a name="catch-weight-tags"></a>Fastvægtkoder

En kode for fastvægt kan oprettes ved at bruge en proces i lagerstedsappen, den kan oprettes manuelt i formularen, eller den kan oprettes ved at bruge en dataenhedsproces. Hvis en fastvægtkode tilknyttes en linje i et indgående kildedokument, såsom en linje i en indkøbsordre, registreres koden. Hvis linjen bruges til udgående behandling, vil koden blive opdateret som leveret.

Ud over de begrænsninger, der gælder for fastvægtprodukter, har kodede fastvægtprodukter andre begrænsninger, der gælder i øjeblikket.

- Alle manuelle opdateringer af lageret (dvs. opdateringer, der ikke udføres vha. en mobilenhed) skal omfatte tilsvarende manuelle opdateringer af de tilknyttede fastvægtkoder, da disse opdateringer ikke udføres automatisk. Manuelle justeringskladder opdaterer f.eks. lageret, men ikke de tilknyttede fastvægtkoder.
- Du skal opdatere fastvægtkoder manuelt for at afspejle bevægelser i genopfyldningsarbejdet. Det skyldes, at systemet ikke kan registrere vægte under behandling af genopfyldningsarbejdet, og registrerer derfor den gennemsnitlige vægt i stedet.
- Modtagelse af blandede id'er understøttes ikke i øjeblikket for aktiverede fastvægtvarer.
- Behandlingen af modtagelse af salgsreturvareordre kan registrere fastvægtkoder. Processen kontrollerer dog ikke, at returkoden er den samme, som er den, der oprindeligt blev leveret til en salgsordre.
- Menupunktet Mobilenhed, der har aktivitetskoden **Registrer materialeforbrug**, understøtter i øjeblikket ikke registrering af fastvægtkoder.
- Selvom optællingsprocesser understøttes for kodede fastvægtvarer, er de begrænset. Du kan f.eks. bruge indstillingerne for mobilenheden til optælling af kodede fastvægtvarer, og den gennemsnitlige vægt anvendes. Fastvægtkoder opdateres dog ikke automatisk af optællingstransaktionen. Når optællingstransaktionen er fuldført, skal fanstvægtkoderne opdateres manuelt, så de afspejler lageret. Hvis varer, der ikke oprindeligt var på et sted, optælles på dete sted, bruges den nominelle vægt.
- Konsolidering af id'er understøtter i øjeblikket ikke kodede fastvægtvarer.
- Funktionen Tilbagefør arbejde understøttes ikke for fastvægtvarer, der er kodenummersporet.

> [!NOTE]
> Ovenstående oplysninger om fastvægtkoder er kun gyldige, hvis fastvægtproduktet har en metode til sporing af fastvægtkodedimensionering, der er fuldt sporet (dvs. hvis parameteren for **Metode for dimensionssporingsmetode** for håndteringspolitikken af fastvægtvarer er angivet til **Produktdimensioner, sporingsdimensioner og alle lagerdimensioner**). Hvis fastvægtvaren kun er delvist kodesporet (dvs. hvis parameteren for metoden for **Dimensionssporingsmetode for fastvægtvare** er angivet til **Produktdimensioner, sporingsdimensioner og lagerstatus**), gælder der yderligere begrænsninger. Da synligheden går tabt mellem koden og lageret i dette tilfælde, er der nogle yderligere scenarier, der ikke understøttes.
