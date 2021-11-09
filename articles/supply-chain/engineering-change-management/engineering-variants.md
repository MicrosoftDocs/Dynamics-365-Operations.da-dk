---
title: Generere varianter for tekniske produkter
description: Dette emne indeholder en beskrivelse af, hvordan du kan generere varianter for tekniske produkter
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e24bceac9457212ecaafda876d19ba62df049371
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/27/2021
ms.locfileid: "7471830"
---
# <a name="generate-variants-for-engineering-products"></a>Generere varianter for tekniske produkter

[!include [banner](../includes/banner.md)]

Dette emne indeholder en beskrivelse af, hvordan du kan generere varianter for tekniske produkter.

## <a name="turn-on-variant-generation-for-engineering-products"></a>Aktivere variantgenerering for tekniske produkter

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *styring af tekniske ændringer*
- **Funktionsnavn:** *Variantgenerering for tekniske produkter*

> [!IMPORTANT]
> Funktionen til *variantgenerering af produkter til teknikerarbejde* kan først ses i systemet, når du har aktiveret konfigurationsnøglen til *Ændringsstyring for teknikerarbejde*. Yderligere oplysninger finder du i [Oversigt over teknisk ændringsstyring](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Generere en eller flere nye varianter af et teknisk produkt

Du kan oprette en eller flere nye varianter af et produkt uden at kopiere oplysninger fra et eksisterende produkt. Dette er nyttigt, når du har brug for at oprette flere produktvarianter på én gang.

Følgende procedure viser et eksempel på, hvordan du kan oprette flere varianter, der omfatter farvedimensionen.

1. Åbn siden **Frigivne produkter** (gå f.eks. til **Styring af tekniske ændringer \> Fælles \> Frigivne produkter**).
1. Åbn fanen **Produkt** i handlingsruden, og vælg **Teknisk produkt** i gruppen **Nyt**.
1. Dialogboksen **Nyt produkt** åbnes. Vælg relevant **Teknisk kategori**.
1. Hvis den valgte tekniske kategori inkluderer variantdimensioner, kan du angive værdier for dem nu. Hvis kategorien i dette eksempel har en **Farve**-dimension, kan du angive den til *Blå*.
1. Foretag andre indstillinger efter behov. Vælg **OK** for at oprette produktet.
1. Produktet og den blå V-1 variant oprettes, og det nye produkt åbnes nu.
1. Tilføj en stykliste og rute til varianten efter behov.
1. Åbn fanen **Produkt** i handlingsruden, og vælg **Produktdimensioner** i gruppen **Produktmaster**.
1. Siden **Produktdimensioner** åbnes. Denne side indeholder en fane for hver tilgængelige dimension. Under hver fane skal du tilføje en række for hver værdi, du vil understøtte for hver relevant dimension. (I dette eksempel kan du tilføje rækker under fanen **Farve** for *Hvid*, *Gul* og *Grøn*).
1. Luk siden, og vælg **Frigivne produktvarianter**. Bemærk, at den første variant, du har oprettet (blå V-1), vises.
1. I handlingsruden skal du på fanen **Produktvariant** vælge **Variantforslag**.
1. Benyt en af følgende fremgangsmåde i dialogboksen **Variantforslag**:

    - Øverst i dialogboksen er der et afsnit med hver tilgængelig dimension. For hver dimension skal du markere afkrydsningsfeltet for hver værdi, du vil generere et variantforslag for, og derefter vælge **Foreslag** på værktøjslinjen. Relevante forslag føjes til sektionen **Foreslåede varianter**.
    - Vælg **Foreslå alle** på værktøjslinjen for at generere variantforslag til alle tilgængelige kombinationer af dimensionsværdier. Relevante forslag føjes til sektionen **Foreslåede varianter**.

1. Marker afkrydsningsfeltet for hver variant, du vil oprette, i sektionen **Foreslåede varianter**. Vælg de foreslåede varianter, og vælg **Opret** for at frigive varianterne til den tekniske virksomhed. Følgende betingelser gælder:

    - Ingen af de oprettede varianter har en stykliste eller rute.
    - Attributterne for disse varianter vil som standard være fra den tekniske kategori og vil ikke være kopieret fra den forrige variant.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Generere en variant som en kopi af en anden produktvariant

Du kan oprette en variant af et produkt på grundlag af en anden produktvariant. Styklisten og ruten fra kildeproduktvarianten kopieres til den nye variant. Dette kan være nyttigt ved diskret produktion, hvor det kan være nyttigt at oprette styklisten på basis af en startstykliste og holde styr på ændringerne fra den forrige variant. For at bevare sporingen registrerer systemet den variant, som blev kopieret for at oprette en ny kopi.

Følgende procedure viser et eksempel på, hvordan du kan oprette en ny variant, der omfatter farvedimensionen, ved at oprette en kopi af en eksisterende variant

1. Åbn siden **Frigivne produkter** (gå f.eks. til **Styring af tekniske ændringer \> Fælles \> Frigivne produkter**).
1. Åbn fanen **Produkt** i handlingsruden, og vælg **Teknisk produkt** i gruppen **Nyt**.
1. Dialogboksen **Nyt produkt** åbnes. Vælg relevant **Teknisk kategori**.
1. Hvis den valgte tekniske kategori inkluderer variantdimensioner, kan du angive værdier for dem nu. Hvis kategorien i dette eksempel har en **Farve**-dimension, kan du angive den til *Blå*.
1. Foretag andre indstillinger efter behov. Vælg **OK** for at oprette produktet.
1. Produktet og den blå V-1 variant oprettes, og det nye produkt åbnes nu.
1. Tilføj en stykliste og rute til varianten efter behov.
1. Tilføj attributter i produktvarianten efter behov.
1. Føj den blå V-1 produktvariant til en teknisk ændringsordre.
1. Angiv **Virkning** til *Ny variant*.
1. Vælg den nye farveværdi (f.eks. *Hvid*). Bemærk, at der gælder følgende betingelser: 
    - Den nye variant har en stykliste og rute, der er kopieret fra den forrige variant.
    - Den nye variant har attributterne kopieret fra den forrige variant.
1. Godkend ændringsordren.
1. Foretag behandling af ændringsordren. Når ordren er behandlet, oprettes den nye variant V-1, som frigives til den tekniske virksomhed.
