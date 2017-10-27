---
title: "Måleenhed og lagerføringspolitikker"
description: I denne artikel beskrives det, hvordan standardenheder, enhedssekvenser og enhedsomregninger bruges i lagerprocesser.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 80bd5978ffe137e48da3f5eac6c75ad0f5e2f06a
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# Måleenhed og lagerføringspolitikker

[!include[banner](../includes/banner.md)]


I denne artikel beskrives det, hvordan standardenheder, enhedssekvenser og enhedsomregninger bruges i lagerprocesser.

Enhedsseriegrupperne definerer rækkefølgen af de enheder, der kan bruges i lageraktiviteter. De oprettes på siden **Enhedsseriegrupper**. Serien viser forholdet mellem de forskellige enheder. Du kan f.eks. gemme paller, der indeholder kasser, der indeholder de enkelte varer. I dette tilfælde skal du angive de tre forskellige enheder og den logiske rækkefølge af lagene. Med enhedsseriegrupper kan du definere politikker for gruppering af nummerplader og de standardenheder, der skal bruges til forskellige lagerprocesser. Denne artikel gælder for både den avancerede lagerstedsløsning, der er tilgængelige i Lagerstedsstyring og den mere grundlæggende lagerstedsløsning, der findes i Lagerstyring.

## Enhedsseriegrupper for frigivne produkter
Hvis du vil bruge frigivne produkter i processer for lagerstedsarbejde, skal en enhedsseriegruppe tildeles til dem. Hvis du validerer et produkt, der er knyttet til en lagringsdimensionsgruppe, og indstillingen **Brug lokationsstyringsprocesser** for lagerdimensionsgruppen er angivet til **Ja**, modtager du en fejlmeddelelse, hvis der ikke er defineret et enhedsseriegruppe-id for produktet. Hvis den enhedsseriegruppe, som du bruger, indeholder flere linjer (og derfor flere enheder), skal du angive en enhedsomregning mellem enhederne. Du fuldfører konfigurationen på siden **Enhedsomregninger**. Den mindste enhed i en seriegruppe, du knytter til et frigivet produkt, skal svare til den lagerenhed, der er defineret for det tilsvarende produkt. Lagerenheden er den enhed, der bruges til grundlæggende beregninger af den disponible lagerbeholdning. Du kan også oprette konvertering af måleenheder for produktvarianter for produktmastere ved hjælp af indstillingen **Aktivér konverteringer af måleenheder**.

## Gruppering af nummerplader
Du kan angive, om modtagelser, som er større end eller mere end en bestemt enhed, skal grupperes i ét id-nummer eller opdeles i et id-nummer for hver enhed. Du kan konfigurere denne funktionsmåde ved at bruge indstillingen **Gruppering af nummerplader** under fanen **Linjedetaljer** på siden **Enhedsseriegrupper**. Hvis du vil bruge gruppering af id-numre, når du behandler arbejdet med en mobilenhed, skal du vælge indstillingen **Gruppering af nummerplader** i menupunktet **Mobilenhed**. Du bruger f.eks. en mobilenhed til at registrere en vare, der er knyttet til en enhedsseriegruppe, som har to linjer. Den første linje er for stykker, og indstillingen **Gruppering af nummerplader** er angivet til **Ja**. Den anden linje er for pallen, og indstillingen **Gruppering af nummerplader** er angivet til **Nej**. I dette tilfælde kan systemet automatisk udføre opdeling og oprettelse af nummerplader pr. 100 styk.

## Enheder til cyklusoptælling
Hvis du vil definere, hvilke enheder der skal bruges som en del af processerne for cyklusoptælling, skal du vælge **Brug enhed til cyklusoptælling** på siden **Enhedsseriegrupper**. Du kan vælge op til fire enheder i seriegruppen. Hvis du vælger mere end fire enheder, kan de ekstra enheder ikke ses på mobilenheden.

## Standardenheder for modtageprocesser for en mobilenhed
Hvis du vil angive standardenheder, der skal bruges til at modtageprocesser på mobilenheder, skal du aktivere indstillingerne **Standardenhed til indkøb og overførsel** og **Standardenhed til produktion** på siden **Enhedsseriegrupper**. Du kan f.eks. angive, at systemet som standard skal bruge pallemængder, når der modtages købsordre for den disponible lagerbeholdning ved hjælp af en mobilenhed, men at lagerstyringsenheden skal være Styk. For at få konverteringen for det antal stykker, som hver palle indeholder, skal du definere en enhedsomregning, f.eks 100 stk. = 1 PL.

## Standardindstillinger for ordre
Som en del af oprettelsen af frigivne produkter skal du vælge standardenhederne for køb, salg og lager for at behandle de forskellige ordrer. Du kan angive standardenheder og mængder for de forskellige kildedokumenter ved hjælp af siderne **Standardindstillinger for ordre** og **Stedspecifikke ordreindstillinger**. Du kan få adgang til disse sider fra siden **Frigivne produkter**.



