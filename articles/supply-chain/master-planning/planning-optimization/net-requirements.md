---
title: Nettobehov og udligningsoplysninger
description: Denne artikel indeholder oplysninger om beregnede nettobehov og udligningsoplysninger.
author: t-benebo
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a31ff5490b08d92f0d966388b65de02bca25b050
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748432"
---
# <a name="net-requirements-and-pegging-information"></a>Nettobehov og udligningsoplysninger

[!include [banner](../../includes/banner.md)]

Når du kører varedisponering, er det vigtigt, at du forstår dets output, hvordan eksisterende forsyning dækker behovet, og hvorfor der er genereret specifik forsyning. Du kan bruge siden **Nettobehov** til bedre at forstå de beregnede behov, som varedisponeringen medfører.

På siden **Nettobehov** vises de nettobehov, som varedisponering har beregnet for produktet. Den viser også de disponeringsindstillinger, der blev anvendt under kørslen af varedisponeringen, en oversigt over behovstotalerne efter transaktionstype og oplysninger om udligning.

## <a name="open-the-net-requirements-page"></a>Åbne siden Nettobehov

Du kan åbne siden **Nettobehov** på en af følgende måder:

- Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**. Vælg eller åbn et produkt. Vælg derefter **Nettobehov** i gruppen **Behov** under fanen **Plan** i handlingsruden.
- Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**. Åbn en salgsordre. Vælg derefter **Produkt og forsyning \> Nettobehov** på værktøjslinjen i oversigtspanelet **Salgsordrelinjer**.
- Gå til **Varedisponering \> Varedisponering \> Ordreforslag**. Vælg eller åbn et ordreforslag. Vælg derefter **Behovsprofil** i gruppen **Behov** under fanen **Visning** i handlingsruden.

## <a name="use-the-net-requirements-page"></a>Bruge siden Nettobehov

Siden **Nettobehov** består af øvre og nedre sektioner. Handlingsruden på denne side indeholder en **Opdater**-knap. Når denne knap er valgt, vises en menu med kommandoer.

### <a name="select-a-master-plan-to-view"></a>Vælge en behovsplan, der skal vises

Før du gennemser nettobehovet for produktet, skal du sørge for at vælge den relevante behovsplan i feltet **Plan** øverst på siden.

### <a name="upper-section"></a>Øvre sektion

I den øverste del af siden vises følgende faner:

- **Oversigt** – Se varebehovene for produktdimensionerne.
- **Varedisponering** – Se de disponeringsindstillinger, der blev brugt under beregning af behov.
- **Oversigt** – Se en fordeling af behovstotalerne efter transaktionstype.
- **Periode** – Se tilgange, afgange og forventet disponibel beholdning for hver periode, der er defineret af periodeskabelonen. Du kan også få vist en grafisk fremstilling af den forventede disponible beholdning.

### <a name="lower-section"></a>Nedre sektion

I den nedre del af siden vises følgende faner:

- **Oversigt** – Få vist listen over produktbehov, der blev beregnet under varedisponeringskørslen, sammen med afgangs- og tilgangsposteringer, der svarer til behovene. Listen sorteres som standard efter behovsdato. Når du vælger et behov, viser oversigtspanelet **Udligning** i den nederste sektion enten kilden til behovet eller de posteringer, der opfylder behovet.
- **Generelt** – Få vist detaljerede oplysninger om det valgte behov.
- **Handling** – Få vist handlingsmeddelelser for behovene.

### <a name="the-action-pane"></a>Handlingsruden

De følgende kommandoer er tilgængelige i handlingsruden:

- **Opdater \> Varedisponering** – Kør Varedisponering direkte fra siden **Nettobehov**.
- **Opdater \> Hovedplanlægning** – Kør hovedplanlægning direkte fra siden **Nettobehov**. Planlægningsoptimering understøtter ikke denne handling.
- **Opdater \> Kontinuitetsplanlægning** – Kør kontinuitetsplanlægning direkte fra siden **Nettobehov**. Planlægningsoptimering understøtter ikke denne handling.

## <a name="example-scenario"></a>Eksempelscenario

Dette eksempel viser, hvordan oplysninger om udligning vises på siden **Nettobehov**.

### <a name="prerequisites"></a>Forudsætninger

Før du kan arbejde dig gennem dette scenarie, skal følgende forudsætninger være klar:

1. Du skal arbejde på et system, hvor standardeksempeldataene er tilgængelige, og du skal indstille den juridiske enhed til *USMF*.
2. I dette eksempel bruges produkt *1000*, som er en del af USMF-eksempeldataene. Kontrollér, at dette produkt er tilgængeligt, og at det er konfigureret på følgende måde:

    - **Standardordretype:** *Indkøbsordre*
    - **Disponibelt lager:** *10,00*

3. Opret en salgsordre for et antal på *25,00* af produkt *1000*. Brug lagringsdimensionerne, hvor den disponible beholdning er placeret.
4. Kør varedisponering for *DynPlan*-behovsplanen.

### <a name="review-the-calculated-requirements"></a>Gennemgå de beregnede behov

Derefter åbner du siden **Nettobehov** for produkt *1000* for at gennemse, hvordan beregnede behov svarer til hinanden.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg det produkt, der har **Varenummer**-værdien *1000*.
1. Vælg derefter **Nettobehov** i gruppen **Behov** under fanen **Plan** i handlingsruden.
1. På siden **Nettobehov** skal du angive feltet **Plan** til *DynPlan*.
1. Kontrollér, at følgende krav er vist som rækker i gitteret under fanen **Oversigt** i den nederste del af siden.

    | Reference | Behovsmængde | Akkumuleret |
    |---|---|---|
    | Beholdninger | 10.00 | 10.00 |
    | Indkøbsordreforslag | 15.00 | 25.00 |
    | Salgsordre | -25,00 | (Tom) |

    > [!NOTE]
    > Feltet **Behovsantal** repræsenterer det samlede antal, som behovet enten kræver (hvis værdien er negativ) eller forsyner (hvis værdien er positiv). Feltet **Akkumuleret** repræsenterer de samlede tilgangs- og afgangsantal, der akkumuleres gennem den valgte periode.

1. Vælg behovslinjen *Beholdninger*, og gennemse derefter de behov, der dækkes af denne forsyning, i oversigtspanelet **Udligning**. Følgende række skal vises der.

    | Reference | Behovsmængde | Dækket antal |
    |---|---|---|
    | Salgsordre | -25,00 | -10,00 |

    Den eksisterende lagerbeholdning dækker delvist den efterspørgsel, der kommer fra salgsordren.

    ![Udligningsoplysninger for den disponible lagerbeholdning](media/pegging-on-hand.png "Udligningsoplysninger for den disponible lagerbeholdning")

1. Vælg behovslinjen *Indkøbsordreforslag*, og gennemse derefter de behov, der dækkes af denne forsyning, i oversigtspanelet **Udligning**. Følgende række skal vises der.

    | Reference | Behovsmængde | Dækket antal |
    |---|---|---|
    | Salgsordre | -25,00 | -15,00 |

    Da salgsordren allerede er delvist dækket, opretter systemet et indkøbsordreforslag for det resterende antal, der ikke er dækket ind.

    ![Udligningsoplysninger til indkøbsordreforslaget](media/pegging-planned-purchase-order.png "Udligningsoplysninger til indkøbsordreforslaget")

1. Vælg behovslinjen *Salgsordre*, og gennemse derefter de behov, der dækker af denne efterspørgsel, i oversigtspanelet **Udligning**. Følgende rækker skal vises der.

    | Reference | Behovsmængde | Dækket antal |
    |---|---|---|
    | Beholdninger | 10.00 | 10.00 |
    | Indkøbsordreforslag | 15.00 | 15.00 |

    ![Udligningsoplysninger til salgsordre](media/pegging-planned-purchase-order.png "Udligningsoplysninger til salgsordre")

> [!NOTE]
> *Sikkerhedslager*-behovet medtages ikke på siden **Nettobehov**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
