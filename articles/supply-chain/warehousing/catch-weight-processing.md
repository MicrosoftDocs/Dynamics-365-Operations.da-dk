---
title: Behandling af fastvægtprodukter med lokationsstyring
description: I dette emne beskrives, hvordan du kan bruge arbejdsskabeloner og lokationsvejledninger til at bestemme, hvordan og hvor arbejde skal udføres på lageret.
author: perlynne
manager: AnnBe
ms.date: 01/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 5161860e3b1c5b0ae795d109159268be085ec5af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "334053"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Behandling af fastvægtprodukter med lokationsstyring
[!include [preview banner](../../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

**Visning af funktioner**

Når du vil bruge lokationsstyring til at behandle fastvægtprodukter, skal du bruge en licenskonfigurationsnøgle til at aktivere funktionen. (Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**. Klik derefter på fanen **Konfigurationsnøgler**, udvid **Handel \> Lagersted- og transportstyring**, og marker afkrydsningsfeltet for **Fastvægt til lagersted**).

> [!NOTE]
> Både **Lagersted- og transportstyring**-licenskonfigurationsnøglen og **Procesdistribution - fastvægt**-licenskonfigurationsnøglerne skal være aktiveret.

Når licenskonfigurationsnøglen er aktiveret, og du opretter et frigivet produkt, kan du vælge **Fastvægt**. Du kan også knytte det frigivne produkt til en lagerdimensionsgruppe, som parameteren **Brug lokationsstyringsprocesser** er markeret for.

Før du kan bruge produktet i Lokationsstyring, skal du udføre en grundlæggende produktspecifik opsætning for fastvægt:

- Definer omregning af nominel vægt mellem fastvægtenheden (boks) og lagerenheden (kilogram \[kg\]) som en del af en definition af enhedsomregning.
- Definer minimum- og maksimumvægttolerancer som en del af opsætningen af fastvægtenheden.
- Opret en enhedsseriegruppe, hvor fastvægtenheden defineres som den laveste lagerenhed (SKU).
- Opret en politik for håndtering af fastvægtvarer.

Du kan finde flere oplysninger i [Konfigurere og vedligeholde fastvægtvarer](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Posteringsreguleringer

Da vægten af lagervaren, når den leveres på et lagersted, kan afvige fra vægten, når lagervaren sendes fra lagerstedet, skal behandlingen af fastvægtproduktet regulerer lagervaren.

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

Hvis den faktiske vægt registreres på pakkestationen under containerpakningsprocesser, bliver lagermedarbejdere ikke bedt om at registrere vægten under plukarbejdet. I stedet bruges den gennemsnitlige vægt af den fysiske lagervare som vægten af den plukkede lagervare, som sendes til pakkeområdet.

Ved interne lokationsstyringsprocesser som rettelser til optælling og regulering kan du angive, om vægten skal registreres eller ej. Hvis vægten ikke registreres, bruges den nominelle vægt.

Du kan også definere, hvordan vægten registreres. I et af de to vigtigste flows spores fastvægtkoder og bruges til at registrere vægten. I det andet flow spores fastvægtkoder ikke.

- **Ja** – Varen bruger fastvægtkoder. Hvert kodenummer repræsenterer én fastvægtenhed (kasse), og en vægt og andre oplysninger knyttes til koden. Ved udgående processer bruges den vægt, der er knyttet til koden.
- **Nej** – Varen bruger ikke fastvægtkoder. De indgående og udgående vejeprocesser er baseret på den faktiske vægt, der registreres under hver proces.

Processen til sporing af fastvægtkoder kan bruges til varer, der ikke ændrer vægt i lagerperioden. Vægten registreres kun i forbindelse med den indgående lagerproces. Under den udgående proces scannes fastvægtkoderne blot, og vægten, der er tilknyttet koderne, bruges til behandlingen af de udgående transaktioner.

### <a name="how-to-capture-catch-weight"></a>Sådan registreres fastvægt

Når der bruges sporing af fangstvægtkode, skal der altid oprettes en kode for hver fastvægtenhed, der modtages, og alle koder skal altid være tilknyttet en vægt.

**Kasse** er f.eks. fastvægtenheden, og du modtager en palle med otte kasser. I dette tilfælde skal der oprettes otte entydige fastvægtkoder, og der skal knyttes en vægt til hver kode. Alt efter den indgående fastvægtkode kan vægten af alle de otte kasser registreres, og den gennemsnitlige vægt kan derefter distribueres til hver kasse, eller der kan registreres en entydig vægt for hver kasse.

Når sporing af fastvægtkode ikke bruges, kan vægten registreres for hver dimensionsopsætning (f.eks. for hvert id og sporingsdimension). Vægten kan også registreres på basis af et samlet niveau, f.eks. fem id-numre (paller).

For metoder til registrering af udgående vægt kan du angive, om vejningen udføres for de enkelte fastvægtenheder (dvs. pr. kasse), eller om vægten registreres ud fra det antal, der bliver plukket (for eksempel tre kasser). Bemærk, at for produktionslinjeplukprocessen bruges den gennemsnitlige vægt, hvis indstillingen **Ikke registreret** bruges.

## <a name="supported-scenarios"></a>Understøttede scenarier

Ikke alle arbejdsgange understøtter behandling af fastvægtprodukter med lokationsstyring. Aktuelt gælder følgende begrænsninger.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Konfiguration af fastvægtprodukter til lokationsstyringsprocesser

- For fastvægtprodukter kan lagringsdimensionsgruppen for varer ikke ændres (så lokationsstyringsprocesser kan bruges til dem).
- Kun formelbehandling understøttes for fastvægtprodukter (ikke styklister).
- Fastvægtprodukter kan ikke knyttes til en sporingsdimensionsgruppe ved hjælp af ejerdimensionen.
- Fastvægtprodukter ikke kan bruges som tjenester.
- Fastvægtprodukter kan bruges som "lagerførte produkter", men kun som en del af varemodelgruppen.
- Fastvægtprodukter kan ikke bruges sammen med funktionen til sporing af "Aktiv i salgsproces".
- Fastvægtprodukter kan ikke bruges sammen med funktionen til registrering af serienumre. Derfor kan produkter ikke flyttes fra et "tomt" til et serienummer som en del af pluk/pakningsprocessen.
- Fastvægtprodukter kan ikke bruges sammen med funktionen til registrering af serienumre før forbrug.
- Fastvægtprodukter, hvor varianter er aktiveret, kan ikke bruges sammen med funktionen til konvertering af varianter af måleenheder.
- Fastvægtprodukter kan ikke markeres som "detailproduktpakke".
- Fastvægtprodukter kan kun bruges sammen med en enhedsseriegruppe, som har fastvægtmaterialehåndteringsenheder, og som har fastvægtenheden som den laveste serie.
- For fastvægtprodukter kan lagerenheden kun omregnes til fastvægtenheden, hvis omregningen resulterer i et nominelt antal, der er mere end 1.
- Opsætningen af stregkoder for fastvægtprodukter understøtter ikke opsætning af en variabel vægt.
 
### <a name="order-processing"></a>Ordrebehandling

- Intern ordrebehandling understøttes ikke.
- Oprettelse af Advance Shipping Notice (ASN/pakkestrukturer) understøtter ikke vægtoplysninger.
- Ordreantallet skal vedligeholdes ud fra fangstvægtenheden.
 
### <a name="inbound-warehouse-processing"></a>Indgående lagerstedsbehandling

- Modtagelse af id'er kræver, at der tildeles vægte ved registreringen, fordi vægtoplysninger ikke understøttes som en del af Advance Shipping Notice. Når der bruges fastvægtkodeprocesser, skal kodenummeret tildeles manuelt pr. fastvægtenhed.
- Modtagelse af blandede id'er understøttes ikke for fastvægtprodukter.
 
### <a name="inventory-and-warehouse-operations"></a>Lager- og lokationshandlinger

- Manuel oprettelse af karantæneordrer understøttes ikke for fastvægtprodukter.
- Manuel flytning af lager, der er relateret til arbejde, understøttes ikke for fastvægtprodukter.
- Konsolidering af id'er understøttes ikke for fastvægtprodukter.
- Ændringer af status for lagervarer fra lagerstedet som en del af en periodisk opgave understøttes ikke for fastvægtprodukter.
- Ændringer af lagerstatus, der er defineret af en forespørgsel, understøttes ikke for fastvægtprodukter. (Ændringer i kvalitetsordrens lagerstatus understøttes heller ikke).
- For fastvægtprodukter kan lagerstatus ikke ændres fra siden **Disponibel efter lokation**.
- For fastvægtprodukter kan lagerstatus ikke ændres som en del af bevægelsesarbejdet for lagerstedsapps.
- Indlæsning af id for at initialisere lagerstedets lagerbeholdning understøttes ikke for fastvægtprodukter.
- Batchtilpasningsprocesser understøttes ikke for fastvægtprodukter.
- Håndtering af negativt fysisk lager understøttes ikke for fastvægtprodukter.
- Lagermarkering ikke kan bruges til fastvægtprodukter.
 
### <a name="outbound-warehouse-processing"></a>Udgående lagerstedsbehandling

- Funktionen til pluk af klynger understøttes ikke for fastvægtprodukter.
- Pluk og pak-lagerstedsbehandling understøttes ikke for fastvægtprodukter.
- For fastvægtprodukter kan der ikke udføres arbejde fra siden **Arbejde**.
- For fastvægtprodukter kan arbejde, der er defineret i en arbejdsskabelon, køres automatisk.
- Funktionen til tilbageførsel af arbejde understøttes ikke for fastvægtprodukter.
- For fastvægtprodukter understøttes manuel pakkestationsbehandling, hvor arbejde oprettes, efter at containere er lukket, ikke.
- Funktionen til stykvis scanning understøttes ikke for fastvægtprodukter.
 
### <a name="production-processing"></a>Produktionsbehandling

- Ved fastvægtprodukter understøttes kun batchordrer for formelprodukter.
- Kanban-funktioner understøttes ikke for fastvægtprodukter.
- Ved fastvægtprodukter kan serienumre ikke registreres før forbrug.
- Funktionen til tilbageførsel af id'er understøttes ikke for fastvægtprodukter.
- Ved fastvægtprodukter kan færdigmelding registreres af serienummeret.

### <a name="transportation-management-processing"></a>Transportstyringsbehandling

- Lastopbygningspanelbehandling understøttes ikke for fastvægtprodukter.
- Transportanmodningslinjer understøttes ikke for fastvægtprodukter.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Andre begrænsninger og funktionsmåder for fastvægtproduktbehandling med lokationsstyring

- Når fastvægtkoder registreres som en del af behandlingen af lagerstedsapps, kan brugeren ikke annullere arbejdsgangen.
- Under plukprocesser, hvor brugeren ikke bliver bedt om at identificere sporingsdimensioner, udføres vægttildelingen ud fra den gennemsnitlige vægt. Dette sker, når f.eks. en kombination af sporingsdimensioner bruges på samme sted, og når der kun er en sporingsdimensionsværdi tilbage på stedet, efter at en bruger har behandlet pluk.
- Når lageret er reserveret et fastvægtprodukt, der er konfigureret til lokationsstyringsprocesser, foretages reservationen ud fra den mindste vægt, der er defineret, selvom dette antal er det sidste antal til håndtering af beholdningen. Denne funktionsmåde adskiller sig fra funktionsmåden for varer, der ikke er konfigureret til lokationsstyringsprocesser.
- Processer, der bruger vægten som en del af kapacitetsberegninger (bølgegrænser, maksimale arbejdspauser, containermaksimumværdier, lokalitetsbelastningskapaciteter osv.), bruger ikke den faktiske vægt af lageret. I stedet er processerne baseret på den fysiske håndteringsvægt, der er defineret for produktet.
- Generelt understøttes Retail-funktioner ikke for fastvægtprodukter.
 
### <a name="catch-weight-tags"></a>Fastvægtkoder

Denne funktion for fastvægtkoder understøttes i øjeblikket kun som en del af følgende scenarier:

- Under behandling af modtagelse på indkøbsordrens lagerstedsapp.
- Under behandling af lastmodtagelse via lagerstedsapp.
- Ved modtagelse via id, der er relateret til en indkøbsordrebelastning, anmodes om tildeling af vægt under tilgangsprocessen. I modsætning hertil bruges vægten fra forsendelsesdataene for overførselsordren ved overførselsordretilgang.
- For varemodtagelse i flytteordre og -linje, der kommer fra et lagersted til ikke-lokationsstyringsproces.
- Behandling af salgsreturordremodtagelse kan registrere fastvægtkoder, men behandlingen valideres ikke, hvis koderne er de samme som dem, der oprindeligt blev leveret til en bestemt salgsordrelinje.
- Når behandlingen af en lagerstatus ændres ved hjælp af lagerstedsappen.
- Når en lageroverførsel sker ved hjælp af lagerstedsappen.
- Ved behandling af justering ind og ud via lagerstedsappen.
- Når plukarbejde behandles for salgs- og flytteordrer. (Bemærk, at fastvægtkoder ikke kan registreres til produktionskomponentpluk).
- Når plukkede mængder reduceres fra lastlinjer, uanset om containere anvendes.
- Når produkter pakkes i containere på en pakkestation.
- Når containere genåbnes.
- Når formularprodukter er færdigmeldt ved hjælp af lagerstedsappen.
- Når transportlaster behandles ved hjælp af lagerstedsappen.
