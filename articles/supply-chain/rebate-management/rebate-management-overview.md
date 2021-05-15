---
title: Oversigt over modulet Rabatstyring
description: Dette emne indeholder en oversigt over modulet Rabatstyring til Microsoft Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 7917f36d8ff3c1ae2d37c5390806ef82771b5211
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920031"
---
# <a name="rebate-management-module-overview"></a>Oversigt over modulet Rabatstyring

[!include [banner](../includes/banner.md)]

Du kan bruge modulet **Rabatstyring** til at oprette kontrakter, handler eller aftaler mellem din virksomhed og dens kunder eller leverandører, så du kan beregne rabatter, fradrag og royalties. Rabatstyring sporer og vedligeholder rabat- og fradragstransaktioner et centralt sted, hvor brugerne effektivt kan oprette, gennemgå og behandle dem.

Rabatstyring understøtter oprettelse, vedligeholdelse og behandling af *rabatter*. En rabat er returneringen af en del af købsprisen af en sælger eller en køber. Rabatter er typisk baseret på købet af et bestemt antal eller for en bestemt værdi af varer i en bestemt periode. I modsætning til tilbudsrabatter udføres disse rabatter, når indkøbsbeløbet er fuldt faktureret.

Rabatstyring understøtter også *fradrag*. Et fradrag er en kompensation, en modydelse eller et vederlag, der enten betales for en licens eller rettigheden til at bruge immaterielle rettigheder som f.eks. et brand, copyright eller en patent, eller for rettigheden til at bruge en naturlig ressource til et formål som f.eks. fiskeri, jagt eller minedrift. Fradrag beregnes normalt som en procentdel af indtægten eller overskuddet fra realiseret brug. Jo mere de immaterielle rettigheder eller naturlige ressourcer bruges, jo større er det fradrag, der realiseres.

Rabatstyring understøtter desuden kunders *royalties*. Royalties er betalinger, som en part foretager til licenstageren eller franchisetageren for rettigheden til at bruge et aktiv.

Rabatstyring giver dig mulighed for at definere posteringsprofiler for hensættelser, rabatter og afskrivninger. Derudover kan posteringerne defineres for en bestemt debitor eller kreditor. På den måde kan aftaler, der ikke gælder for alle debitor- eller kreditorscenarier, spores via posteringer.

Rabattransaktioner genereres automatisk på basis af den beregningsmetode, der er valgt og planlagt i batchjob. Derudover kan du konfigurere arbejdsprocesser til at administrere, gennemgå og godkende aftaler.

## <a name="basis-calculation"></a>Beregningsbasis

Kunderabatter, kunderoyalties og leverandørrabatter kan alle have forskellige grundlag afhængigt af dine forretningsbehov:

- Kunderabatter kan baseres på salgsordrer, følgesedler eller fakturaer.
- Kunderoyalties kan baseres på salgsordrer, følgesedler eller betalte fakturaer.
- Leverandørrabatter kan baseres på enten indkøbsordrer eller salgsordrer. De kan beregnes ud fra produkter, der er købt fra rabatleverandøren og solgt til kunder via salgsfakturaer.

## <a name="flexible-calculations"></a>Fleksible beregninger

Rabatberegningsperioder er tilgængelige for både kundeaftaler og leverandøraftaler. En beregningsperiode definerer aftalens længde, beregningsfrekvensen og beregningsperioden. Rabatterne kan periodiseres på basis af salgsordreantal eller -beløb for kvalificerede produkter i løbet af rabatperioden.

For hver aftaleberegning kan du angive en af følgende perioder:

- Fakturaer
- Dag
- Uge
- Måned
- Kvartal
- År
- Tilpasset periode
- Et multiplum af en eller flere af de tidligere viste perioder

Beregningen kan anvendes på de enkelte kunder og produkter, grupper af kunder og produkter eller alle kunder og produkter. Rabatter, der har flere detaljelinjer, kan have forskellige kvalificeringsdatointervaller. Hensættelses- og kravsperioderne kan variere. Hensættelser kan f.eks. behandles hver dag, mens krav behandles en gang om måneden.

Rabatter kan konfigureres ud fra mange forskellige parametre. De kan f.eks. konfigureres som en procent, en sats eller et fast beløb. Der findes fire hovedberegningsmetoder:

- Trinvis
- Akkumuleret
- Glidende
- Samlet værdi

Resultater af rabatberegninger kan også reduceres med andre rabatter, afhængigt af om rabatten er konfigureret til at beregne ud fra nettobeløbet.

På kreditorsiden kan rabatter beregne prisen ud fra en FIFO-regel (First In, First Out), den seneste købspris, den gennemsnitlige købspris eller salgsprisen.

## <a name="rebate-target-transactions"></a>Rabatmåltransaktioner

De output, som rabataftalen eller -handlen genererer, kan være økonomiske eller varemæssige.

Økonomiske output bestemmes af den betalingstype, der er tildelt aftalen fra posteringsprofilen. Disse output kan omfatte debitorfradragskladder, fritekstfakturaer og kreditorfakturaer. Økonomiske rabatmåltransaktioner omfatter en reference til den oprindelige rabataftale af revisionsmæssige årsager.

Vareoutput opretter en gratis varesalgsordre for kunderabatter og en indkøbsordre for leverandørrabatter. Posteringer af varerabatmål giver mulighed for at bestemme, hvilken rabatreference der skal angives på den gratis varesalgsordre eller indkøbsordre.

## <a name="accurate-rebate-calculations"></a>Nøjagtige rabatberegninger

Kombinationen af de tilknyttede aftaler, frekvensen af beregninger, beregningsgrundlaget og den valgte beregningsmetode bestemmer nøjagtigheden og præcisionen af rabatberegningerne. Rabathensættelser kan bruges til at periodisere bogførte og indkasserede værdier.

Hensættelser kan håndteres dagligt eller månedligt. Funktionen kan dog tildele eller betale rabatten eller modtage betaling af den ved en defineret frekvens. Brugerne kan nemt justere en plan eller betalingsbeløb når som helst under udbetalingen.

Brugerne behøver ikke længere at håndtere aftaler eller hensættelser i to trin. Hensættelser og afskrivninger bogføres direkte i finansmodulet. Der kan desuden oprettes kreditnotaer automatisk. Der er derfor fuld integration med kreditorer og debitorer. Under behandlingen tager beregningerne højde for udligningsrabatter, betalte fakturaer, handelsrabatter og eksisterende kreditnotaer for at sikre, at beløb og værdier beregnes korrekt.

Når der beregnes rabatter, oprettes der transaktioner, som kan gennemgås, før bogføringen finder sted. Der kan derefter oprettes en kladde-, kreditnota- eller debettransaktion. En separat proces bogfører rabat- og fradragstransaktioner. Rapporteringsopgørelser og transaktionslister kan anskaffes for at sikre overholdelse af angivne standarder, effektivitet og gennemsigtighed.

## <a name="guaranteed-royalty-payments"></a>Garanterede betalinger af royalty

Ved hjælp af automatisk betalingsgenerering i Rabatstyring kan royalties håndteres hurtigt og nemt, også selvom der gælder minimumgarantier. 

## <a name="maximizing-spend-versus-rebates"></a>Maksimere forbrug i forhold til rabatter

Leverandører og produkter kan grupperes efter distrikt, og der kan gives forskellige tilbud, afhængigt af landet eller området for transaktionen. Når brugere vælger produkter, kan de definere, hvilke varer der skal medtages, og antallet af varer, der skal bruges i rabatudligningen.