---
title: Produktionsplanlægning
description: Dette emne beskriver produktionsplanlægning med en forklaring af, hvordan du redigerer planlagte produktionsordrer ved hjælp af Planlægningsoptimering.
author: ChristianRytt
ms.date: 06/01/2021
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ffee79f152141297ceb24e2d7a40523eac18ffaf
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129747"
---
# <a name="production-planning"></a>Produktionsplanlægning

Planlægningsoptimering understøtter flere produktionsscenarier. Hvis du migrerer fra det eksisterende, indbyggede varedisponeringsprogram, er det vigtigt, at du er opmærksom på ændret funktionsmåde.

Følgende video indeholder en kort introduktion til nogle af de begreber, der beskrives i dette emne: [Dynamics 365 Supply Chain Management: Forbedringer af planlægningsoptimering](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funktion i dit system

Hvis systemet ikke allerede indeholder de funktioner, der er beskrevet i dette emne, skal du gå til [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Produktionsordreforslag til planlægningsoptimering*.

## <a name="planned-production-orders"></a>Produktionsordreforslag

Når varedisponering opretter ordreforslag for at opfylde kravene, fastlægges ordretypen af værdien i feltet **Ordreforslagstype**. Hvis feltet **Ordreforslagstype** er angivet til *Produktion*, oprettes der produktionsordreforslag. Disse produktionsordreforslag omfatter oplysninger om den aktive stykliste (BOM) og rute-id'et fra den relaterede produktionsopsætning.

## <a name="requirements-from-boms"></a>Krav fra styklister

Styklisteoplysninger anvendes under varedisponering. Outputforslaget omfatter materialeforsyning for at dække relateret materialebehov til produktion.

Under varedisponering bruges den aktuelle, aktive stykliste til at bestemme, hvilke materialer der kræves til produktionen. Dette trin udføres gennem alle niveauer i styklistestrukturen, der er relateret til den nødvendige produktionsordre. Materialebehovet opfyldes ved hjælp af tilgængeligt lager, eksisterende forsyning i ordren og godkendte ordreforslag. Hvis der skal bruges yderligere materialer på et hvilket som helst sted, oprettes der et ordreforslag, der skal dække behovet.

## <a name="scheduling-during-firming"></a>Planlægning under autorisation

Produktionsordreforslag omfatter det rute-id, der kræves ved produktionsplanlægning. Planlægning af support under kørslen af disponeringen for ordreforslag afventer dog. Rute-id'et bruges til at planlægge produktionsordreforslag under autorisation. Leveringstiden for produktionsordreforslag kan derfor være forskellig fra leveringstiden for relaterede planlagte, autoriserede produktionsordrer, der oprettes fra dem, som beskrevet her:

- **Produktionsordreforslag** – Leveringstiden er baseret på den statiske leveringstid fra det frigivne produkt.
- **Autoriseret produktionsordre** – Leveringstiden er baseret på planlægning, der bruger ruteoplysninger og relaterede ressourcebegrænsninger.

Yderligere oplysninger om forventet tilgængelighed af funktioner finder du i [Analyse af tilpasning af Planlægningsoptimering](planning-optimization-fit-analysis.md).

Hvis du er afhængig af, at produktionsfunktionaliteten endnu ikke er tilgængelig for Planlægningsoptimering, kan du fortsætte med at bruge det indbyggede varedisponeringsprogram. Der kræves ingen undtagelse.

## <a name="delays"></a>Forsinkelser

Hvis leveringstiden for påkrævet materiale er længere end perioden mellem dags dato og datoen for materialebehov, forsinkes ordreforslaget for det påkrævede materiale og den relaterede produktionsordre. For ordreforslag beregnes forsinkelsen (i dage) på grundlag af leveringstiden fra det frigivne produkt. Oplysningerne om forsinkelsen udbredes derefter gennem alle niveauer af styklistestrukturen. Du kan derfor følge indvirkningen af forsinkede råmaterialer hele vejen frem til debitorsalgsordren.

## <a name="modifying-planned-orders"></a>Ændre ordreforslag

Når du ændrer oplysningerne i et ordreforslag, modtager du følgende meddelelse: "Bemærk, at indvirkningen af manuelle ændringer på ordreforslag ikke afspejles i resten af planen, før næste varedisponeringskørsel."

Hvis du vil ændre oplysningerne i et ordreforslag og se, hvordan det påvirker de relaterede materialebehov, skal du følge disse trin.

1. Opdater ordreforslaget.
2. Godkend ordreforslaget.
3. Kør varedisponering.

Når du kører varedisponering, skal du ikke bruge filtre, hvis produktionsordreforslag medtages. Du kan finde flere oplysninger i afsnittet [Filtre](#filters) nedenfor i dette emne.

> [!NOTE]
> Hvis leveringsdatoen for ordreforslaget ændres til en senere dato, kan behovet udlignes i forhold til et nyt ordreforslag. Denne funktionsmåde forekommer, når den nye leveringsdato medfører forsinkelse for den udlignede efterspørgsel, men forsinkelsen kan undgås ifølge indstillingerne for leveringstiden.

## <a name="explosion-page"></a>Siden Udfoldning

Du kan bruge siden **Udfoldning** til at analysere den efterspørgsel, der kræves i forbindelse med en bestemt produktionsordre eller et bestemt produktionsordreforslag, den relaterede disponering og udligningsoplysninger. Oplysninger på siden **Udfoldning** opdateres under varedisponering. Du kan ikke opdatere oplysningerne direkte fra siden **Udfoldning**.

## <a name="filters"></a><a name="filters"></a>Filtre

Hvis du vil sikre, at Planlægningsoptimering har de oplysninger, der er nødvendige for at beregne det korrekte resultat, skal du medtage alle produkter, der har relation til produkter, i hele styklistestrukturen i ordreforslaget. I forbindelse med planlægningsscenarier, der omfatter produktion, anbefaler vi derfor, at du undgår filtrerede varedisponeringskørsler.

Selvom afhængige underordnede varer registreres og medtages i varedisponeringskørsler, når det indbyggede varedisponeringsprogram bruges, udfører Planlægningsoptimering ikke denne handling i øjeblikket.

Hvis f.eks. en enkelt rulle fra styklistestrukturen i produkt A også bruges til at producere produkt B, skal alle produkter i styklistestrukturen for produkter A og B medtages i filteret. Da det kan være kompliceret at sikre, at alle produkter indgår i filteret, anbefales det, at du undgår filtrerede varedisponeringskørsler, når der er produktionsordrer involveret. Ellers giver behovsplanlægningen uønskede resultater.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Årsager til at undgå filtrerede behovsplanlægningskørsler

Når du kører filtreret varedisponering for et produkt, registrerer Planlægningsoptimering (i modsætning til det indbyggede varedisponeringsprogram) ikke alle underproduktionerne og råvarerne i styklistestrukturen for det pågældende produkt og medtager dem derfor ikke i varedisponeringskørslen. Selvom Planlægningsoptimering identificerer det første niveau i produktets styklistestruktur, indlæses der ingen produktindstillinger (f.eks. standardordretypen eller varedisponering) fra databasen.

I Planlægningsoptimering indlæses dataene for kørslen på forhånd og anvender filtrene. Det betyder, at hvis et underprodukt eller et råmateriale i et bestemt produkt ikke er en del af filteret, registreres der ikke oplysninger om det under kørslen. Hvis underproduktet eller råvaren også indgår i et andet produkt, vil en filtreret kørsel, der kun indeholder det oprindelige produkt og dets komponenter, fjerne det eksisterende planlagte behov, der blev oprettet for det andet produkt.

Denne logik kan medføre, at filtrerede behovsplanlægningskørsler giver uventede resultater. Følgende afsnit indeholder eksempler på de uventede resultater, der kan forekomme.

### <a name="example-1"></a>Eksempel 1

Færdigvaren *FG* består af følgende komponenter:

- Råvarer *R*
- Underprodukt *S1*, som består af underprodukt *S2*

Der er lagerbeholdning for råvaren *R*, mens underprodukt *S1* ikke findes på lageret.

Når du kører en filtreret behovsplanlægning for færdigvaren *FG*, modtager du et produktionsordreforslag til færdigvaren *FG*, et indkøbsordreforslag for råvare *R* og et indkøbsordreforslag for underprodukt *S1*. Dette er et uønsket resultat, fordi Planlægningsoptimering har ignoreret den eksisterende forsyning med råmateriale *R*, og underprodukt *S1*, skal produceres ved hjælp af *S2* i stedet for bestilt direkte. Det sker, fordi Planlægningsoptimering kun har listen over komponenter for den færdige vare *FG* uden relaterede oplysninger som f.eks. eksisterende forsyning af komponenterne eller standardordreindstillingerne.

### <a name="example-2"></a>Eksempel 2

Ud fra ovenstående eksempel bruger *FG2* også underprodukt *S1*. Der findes et ordreforslag for færdigvaren *FG2*, og der findes en planlagt efterspørgsel efter alle dets komponenter, herunder *S1*.

Du beslutter dig for at omgås de uønskede resultater af den filtrerede behovsplanlægning, der er kørt i forrige eksempel, ved at føje alle underprodukter og råmaterialer fra styklistestrukturen for færdigvare *FG* til filteret og derefter køre fuld regenerering.

Når du kører den fulde regenerering, sletter systemet alle eksisterende resultater for alle de inkluderede produkter og gendanner derefter resultaterne på baggrund af de nye beregninger. Det betyder, at eksisterende planlagt efterspørgsel på produkt *S1* slettes og derefter kun genoprettes under hensyntagen til færdigvare *FG*, mens *FG2*-behov ignoreres. Det sker, fordi når du kører planlægningsoptimering, omfatter dette ikke det planlagte behov for andre produktionsordreforslag. Det er kun ordreforslaget, der er genereret under kørslen, der bruges.

> [!NOTE]
> Hvis det eksisterende ordreforslag for færdigvare *FG2* har statussen *Godkendt*, medtages det godkendte ordreforslag, selvom det overordnede produkt ikke er føjet til filteret.

Medmindre du tilføjer alle komponenterne i færdigvare *FG*, færdigvare *FG2* og alle andre produkter, som disse komponenter er en del af (sammen med deres komponenter), giver den filtrerede kørsel af behovsplanlægning uønskede resultater.

Da det kan være kompliceret at sikre, at alle produkter indgår i filteret, anbefales det, at du undgår filtrerede varedisponeringskørsler, når der er produktionsordrer involveret.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
