---
title: Produktionsplanlægning
description: Dette emne beskriver produktionsplanlægning med en forklaring af, hvordan du redigerer planlagte produktionsordrer ved hjælp af Planlægningsoptimering.
author: ChristianRytt
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 22b78f44940f71097ca8b1cdb74edb06274bba75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839217"
---
# <a name="production-planning"></a>Produktionsplanlægning

Planlægningsoptimering understøtter flere produktionsscenarier. Hvis du migrerer fra det eksisterende, indbyggede varedisponeringsprogram, er det vigtigt, at du er opmærksom på ændret adfærd.

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

I forbindelse med planlægningsscenarier, der omfatter produktion, anbefales det, at du undgår filtrerede varedisponeringskørsler. Hvis du vil sikre, at Planlægningsoptimering har de oplysninger, der er nødvendige for at beregne det korrekte resultat, skal du medtage alle produkter, der har relation til produkter, i hele styklistestrukturen i ordreforslaget.

Selvom afhængige underordnede varer registreres og medtages i varedisponeringskørsler, når det indbyggede varedisponeringsprogram bruges, udfører Planlægningsoptimering ikke denne handling.

Hvis f.eks. en enkelt rulle fra styklistestrukturen i produkt A også bruges til at producere produkt B, skal alle produkter i styklistestrukturen for produkter A og B medtages i filteret. Da det kan være meget kompliceret at sikre, at alle produkter indgår i filteret, anbefales det, at du undgår filtrerede varedisponeringskørsler, når der er produktionsordrer involveret.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]