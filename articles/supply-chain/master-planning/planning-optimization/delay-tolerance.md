---
title: Forsinkelsestolerance (negative dage)
description: Dette emne indeholder oplysninger om beregning af forsinkelsestolerance, og hvordan det påvirker oprettelsen af ordreforslag i planlægningsoptimering.
author: ChristianRytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cb03ccb208f19f540fefafd9964f74309736dc05
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577474"
---
# <a name="delay-tolerance-negative-days"></a>Forsinkelsestolerance (negative dage)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Funktionen til forsinkelsestolerance giver planlægningsoptimering mulighed for at overveje den værdi for **Negative dage**, der er angivet for disponeringsgrupper. Den bruges til at forlænge den forsinkelsestoleranceperiode, der anvendes under behovsplanlægning. På denne måde kan du undgå at oprette nye forsyningsordrer, hvis eksisterende forsyninger kan dække behovet med kort forsinkelse. Formålet med funktionen er at bestemme, om det giver mening at oprette en ny forsyningsordre for en given efterspørgsel.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funktionen i systemet

Du kan gøre funktionen til forsinkelsestolerance tilgængelig i systemet ved at gå til [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Negative dage for Planlægningsoptimering*.

## <a name="delay-tolerance-in-planning-optimization"></a>Forsinkelsestolerance i planlægningsoptimering

Forsinkelsestolerance er det antal dage efter leveringstiden, du er villig til at vente, før du bestiller ny genopfyldning, når der allerede er planlagt en eksisterende forsyning. Forsinkelsestolerance defineres ved hjælp af kalenderdage og ikke arbejdsdage.

Når systemet beregner forsinkelsestolerancen, tages indstillingen af **Negative dage** med i beregningen på tidspunktet for behovsplanlægning. Du kan enten angive værdien for **Negative dage** på siden **Disponeringsgrupper** eller på siden **Varedisponering**.

Systemet knytter beregningen af forsinkelsestolerancen til den *tidligste genopfyldningsdato*, hvilket er lig med dags dato plus gennemløbstiden. Forsinkelsestolerancen beregnes ved at bruge følgende formel, hvor *max()* finder den største af to værdier:

*max(Tidligste genopfyldningsdato, Forfaldsdato for efterspørgsel)* – *Forfaldsdato for efterspørgsel* + *Negative dage*

Denne formel sikrer, at varedisponering ikke opretter nye leveringsordrer, når den eksisterende forsyning er tilstrækkelig under produktets gennemløbstid.

> [!NOTE]
> Beregningen af forsinkelsestolerance i Planlægningsoptimering bruger altid beregningen af dynamiske negative dage fra en indbygget behovsplanlægning. Indstillingen **Brug dynamiske negative dage** på siden **Parametre for behovsplanlægning** har ingen indflydelse på denne funktionsmåde.

Hvis den eksisterende forsyning medfører en forsinkelse i efterspørgsel, der er mindre end eller lig med den beregnede forsinkelsestolerance, udligner Planlægningsoptimering den eksisterende forsyning med efterspørgslen. I nogle tilfælde er det bedre at udskyde behovet end at ende med for stor forsyning.

Følgende undersektioner indeholder eksempler på, hvordan forsinkelsestolerance påvirker oprettelsen af ordreforslag i Planlægningsoptimering.

### <a name="example-1"></a>Eksempel 1

Et produkt har følgende konfiguration:

- **Leveringstid:** *10*
- **Negative dage:** *2*

Der findes følgende udbud og efterspørgsel for produktet:

- **Efterspørgsel for i dag**: En salgsordre på et antal på 10
- **Forsyning om 12 dage:** En indkøbsordre på et antal på 10

Eksisterende forsyning kan dække behovet inden for 12 dage, og denne periode er lig med forsinkelsestolerancen. Når behovsplanlægningen køres, oprettes der derfor ikke ordreforslag.

### <a name="example-2"></a>Eksempel 2

Et produkt har følgende konfiguration:

- **Leveringstid:** *10*
- **Negative dage:** *0*

Der findes følgende udbud og efterspørgsel for produktet:

- **Efterspørgsel for i dag**: En salgsordre på et antal på 10
- **Forsyning om 12 dage:** En indkøbsordre på et antal på 10

Eksisterende forsyning kan først dække behovet efter 12 dage. Men forsinkelsestolerancen er 10 dage. Når varedisponering køres, oprettes der derfor et ordreforslag på 10.

### <a name="example-3"></a>Eksempel 3

Et produkt har følgende konfiguration:

- **Leveringstid:** *10*
- **Negative dage:** *2*

Der findes følgende udbud og efterspørgsel for produktet:

- **Efterspørgsel om 11 dage**: En salgsordre på et antal på 10
- **Forsyning om 14 dage:** En indkøbsordre på et antal på 10

Eksisterende forsyning kan først dække behovet efter tre dage. Men forsinkelsestolerancen er to dage. I dette tilfælde omfatter forsinkelsestolerancen kun de to negative dage. Efterspørgselsdatoen medtages ikke, fordi den ligger efter produktets leveringstid. Når varedisponering køres, oprettes der derfor et ordreforslag på 10.
