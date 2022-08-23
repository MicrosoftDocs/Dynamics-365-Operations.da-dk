---
title: Beregne leveringsdatoer for salgsordrer ved hjælp af LE
description: Med leveringsevnen LE kan du give kunder realistiske datoer for, hvornår du kan love bestemte varer. Denne artikel beskriver, hvordan du kan konfigurere og bruge LE til hvert planlægningsprogram (Planlægningsoptimering og det indbyggede program).
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 9a2d8a66fe7e68ebd5729a401af3f0efe04051b1
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229932"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Beregne leveringsdatoer for salgsordrer ved hjælp af LE

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Med leveringsevnen LE kan du give kunder realistiske datoer for, hvornår du kan love bestemte varer. For hver salgslinje kan du angive en dato, der tager højde for eksisterende lagerbeholdning, produktionskapacitet og transporttider.

LE udvider DTT-funktionaliteten [available-to-promise](../../sales-marketing/delivery-dates-available-promise-calculations.md) ved at tage kapacitetsoplysninger med i betragtning. Mens DTT kun tager højde for materialetilgængelighed og forudsætter ressourcer med ubegrænset kapacitet, tager LE højde for tilgængeligheden af både materialer og kapacitet. Det giver derfor et mere realistisk billede af, om efterspørgslen kan opfyldes inden for en given tidsramme.

LE fungerer lidt anderledes baseret på den brugte varedisponering (Planlægningsoptimering eller det indbyggede program). Denne artikel beskriver, hvordan du konfigurerer den til hvert program. LE til Planlægningsoptimering understøtter i øjeblikket kun et undersæt af LE-scenarier, der understøttes af det indbyggede program.

## <a name="turn-on-ctp-for-planning-optimization"></a>Aktivere LE til planlægningsoptimering

LE til det indbyggede program til varedisponering er altid tilgængelig. Hvis du vil bruge LE til planlægningsoptimering, skal det dog være slået til for systemet. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Varedisponering*
- **Funktionsnavn:** *(Forhåndsversion) LE til planlægningsoptimering*

## <a name="how-ctp-compares-to-atp"></a>Sammenligning af LE med DTT

LE og DTT ligner hinanden, men LE kan ofte give et mere præcist resultat, som det følgende eksempel viser.

Vare A er en vare, der består af vare B og C, og det disponible antal af vare A er 0 (nul). Hvis du laver en DTT-kontrol, der kun tager højde for materialer, vil DTT-antallet også være 0 (nul). Men hvis du foretager en LE-kontrol, kontrollerer systemet tilgængeligheden af vare B og C, kontrollerer de ressourcer, der kræves for at gøre dem til vare A, og beregner, hvor mange af vare A der kan fremstilles. Derudover kan LE-beregningen kontrollere de ressourcer og materialer, der kræves for at få flere varer B og C, og bruge dem til at lave mere af vare A.

En LE-beregning, der tager højde for både materialer og ressourcer, kan vise et større antal end en beregning, hvor der kun kontrollerer materialer, især når den vare, der kontrolleres, er en montageordrevare. Dvs., at LE-funktionen er baseret på udfoldningsfunktionen og kan køres for en valgt salgsordrelinje for at beregne den forventede leveringsdato.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Hvordan LE varierer afhængigt af, hvilket varedisponeringsprogram du bruger

I følgende tabel opsummeres forskellene mellem LE til Planlægningsoptimering og LE til det indbyggede varedisponeringsprogram.

| Applikationsobjekt | Planlægningsoptimering | Indbygget varedisponeringsprogram |
|---|---|---|
| **Leveringsdatokontrol** for ordrer, ordrelinjer og produkter | *LE til planlægningsoptimering* | *LE* |
| Beregningstidspunkt | Beregningen udløses ved at køre en dynamisk plan som en planlagt opgave. | Beregningen udløses med det samme, hver gang du angiver eller opdaterer en salgsordrelinje. |
| **Status for LE til planlægningsoptimering**-feltværdi | <p>Værdien *Ikke klar* vises for ordrer og ordrelinjer, hvor den dynamiske plan ikke har kørt, siden ordrerne og linjerne blev oprettet eller opdateret sidst.</p><p>Værdien *Klar* vises for ordrer og linjer, hvor der er brugt LE til at beregne bekræftede leveringsdatoer ved at køre den dynamiske plan.</p> | Værdien *Klar* vises altid. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a>Angive standardmetoder for leveringsdatokontrol

Systemet kan bruge en hvilken som helst af flere forskellige metoder til at beregne estimater for leveringsdatoer for hver ordre og ordrelinje. Du skal angive den metode til leveringsdatokontrol, som du vil bruge oftest, som den globale standardmetode. Du kan også angive individuelle tilsidesættelser for hvert produkt. Du kan senere tilsidesætte standardmetoderne for hver ordre og/eller ordrelinje efter behov.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a>Angive global standard for leveringsdatokontrol

Standardmetoden for leveringsdatokontrol anvendes på alle nye ordrelinjer, hvor der ikke anvendes en tilsidesættelse. Vælg én ved at benytte følgende fremgangsmåde.

1. Gå til **Debitor \> Opsætning \> Debitorparametre**.
1. Vælg den metode,du vil bruge som standardmetode for dit firma, i feltet **Leveringsdatokontrol** i oversigtspanelet **Leveringskontrol** under fanen **Forsendelser**:

    - *Ingen* – Beregn ikke leveringsdatoer.
    - *Salgsleveringstid* – Salgsleveringstid er tiden mellem oprettelse af salgsordren og forsendelse af varerne. Beregningen af leveringsdatoen er baseret på antal dage og tager ikke hensyn til varernes tilgængelighed, kendte behov eller planlagte leveringer.
    - *DTT* – DTT er antallet af en vare, der er tilgængelig og kan være lovet til en kunde på en bestemt dato. DTT-beregningen omfatter leveringstider, der ikke er bindende, planlagte tilgange og afgange.
    - *DTT + Afgangsmargen*– Afsendelsesdatoen er lig med DTT-datoen plus varens afgangsmargen. Afgangsmargenen er den tid, der kræves for at klargøre varerne til afsendelse.
    - *CTP* – Brug den LE-beregning, der er angivet af det indbyggede varedisponeringsprogram. Hvis du bruger Planlægningsoptimering, er det ikke tilladt at bruge *LE*-leveringsdatokontrolmetoden, og hvis den er valgt, opstår der en fejl, når beregningen køres.
    - *LE til planlægningsoptimering* – Brug den LE-beregning, der er leveret af Planlægningsoptimering. Denne indstilling har ingen virkning, hvis du bruger det indbyggede varedisponeringsprogram.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Angive tilsidesættelser af leveringsdatokontrol for individuelle produkter

Du kan tildele tilsidesættelser for bestemte produkter, hvor du vil bruge en anden kontrolmetode for leveringsdato end den, der er angivet som global standardmetode.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Vælg det produkt, du vil konfigurere.
1. På fanen **Administrer lager** i handlingsruden i gruppen **Ordreindstillinger** skal du vælge **Standardordreindstillinger**.
1. Angiv indstillingen **Tilsidesæt leveringskontrol** til **Ja** i oversigtspanelet **Salgsordre** på siden *Standardindstillinger for ordre*.
1. Vælg den metode, der skal bruges til det valgte produkt, i feltet **Leveringsdatokontrol**. De samme indstillinger, der er beskrevet i afsnittet [Angive global standard for leveringsdatokontrol](#global-default), er tilgængelige.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a>Planlægge LE for beregninger af planlægningsoptimering

Når du bruger LE til planlægningsoptimering, skal du køre en dynamisk plan for at udløse systemet til at udføre LE-beregningerne og derefter angive de bekræftede afsendelses- og tilgangsdatoer for alle relevante ordrer. Planen skal indeholde alle varer, der er nødvendige for bekræftede afsendelses- og modtagelsesdatoer. (Når du bruger LE til det indbyggede planlægningsprogram, udføres LE-beregningerne med det samme lokalt. Derfor behøver du ikke køre en dynamisk plan for at se LE-resultaterne).

Hvis du vil sikre, at datoerne er tilgængelige i god tid for alle brugere, anbefales det, at du konfigurerer batchjob til at køre de relevante planer på gentagende basis. Et batchjob, der er konfigureret til at køre en dynamisk plan hvert 30. minut, angiver f.eks. de bekræftede afsendelses- og modtagelsesdatoer hvert 30. minut. Derfor skal brugere, der indtaster og importerer ordrer, vente maks. 30 minutter på at få de bekræftede afsendelses- og modtagelsesdatoer.

Hvis du vil konfigurere et batchjob til at køre en dynamisk plan regelmæssigt, skal du følge disse trin.

1. Gå til **Varedisponering \> Varedisponering \> Kørsel \> Varedisponering**.
1. I oversigtspanelet **Parametre** i dialogboksen **Varedisponering** skal du angive feltet **Behovsplan** til den dynamiske plan, som du vil køre.
1. Angiv **Batchbehandling** til **Ja** i oversigtspanelet *Kør i baggrunden*.
1. Vælg **Gentagelse**, og konfigurer tidsplanen efter behov.
1. Vælg **OK** for at gemme tidsplanen.
1. Vælg **OK** for at oprette batchjobbet og lukke dialogboksen.

## <a name="use-ctp-for-built-in-master-planning"></a>Bruge LE til indbygget varedisponering

### <a name="create-a-new-order-by-using-ctp-for-built-in-master-planning"></a>Oprette en ny ordre ved hjælp af LE til indbygget varedisponering

Hver gang du tilføjer en ny salgsordre eller ordrelinje, tildeles den en standardkontrolmetode for leveringsdato. Ordrehovedet starter altid med den globale standardmetode. Hvis der er knyttet en tilsidesættelse til en bestilt vare, bruger den nye ordrelinje denne tilsidesættelse. Ellers bruger den nye ordrelinje også den globale standardmetode. Du skal derfor angive standardmetoder, så de matcher den metode til leveringsdatokontrol, du bruger oftest. Når du har oprettet en ordre, kan du tilsidesætte standardmetoden på ordrehoved- og/eller ordrelinjeniveau efter behov. Yderligere oplysninger finder du i [Angive standardmetoder for leveringsdatokontrol](#default-methods) og [Ændre eksisterende salgsordrer, så de bruger LE](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-built-in-master-planning"></a>Se bekræftede leveringsdatoer, når du bruger LE til indbygget varedisponering

Hvis du bruger det indbyggede varedisponeringsprogram, anvendes LE-beregninger på ordrer og/eller ordrelinjer, hvor feltet **Leveringsdatokontrol** er angivet til *LE*.

Til salgslinjer, der bruger LE til indbygget varedisponering, indstiller systemet automatisk felterne **Bekræftet afsendelsesdato** og **Bekræftet modtagelsesdato**, hver gang du gemmer en salgslinje. Hvis du senere foretager en relevant ændring af en salgslinje (f.eks. ved at ændre antallet eller stedet), genberegnes datoerne med det samme.

- Hvis du vil have vist de bekræftede leveringsdatoer for en salgsordrelinje, skal du åbne salgsordren og vælge salgslinjen. I oversigtspanelet **Linjedetaljer** skal du under fanen **Levering** gennemgå felterne **Bekræftet afsendelsesdato** og **Bekræftet modtagelsesdato**.
- Hvis du vil have vist de bekræftede leveringsdatoer for en hel ordre, skal du åbne salgsordren og vælge **Overskrift**. I oversigtspanelet **Levering** skal du gennemgå værdierne af felterne **Bekræftet afsendelsesdato** og **Bekræftet modtagelsesdato**.

## <a name="use-ctp-for-planning-optimization"></a>Bruge LE til planlægningsoptimering

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Oprette en ny ordre ved hjælp af LE til planlægningsoptimering

Hver gang du tilføjer en ny salgsordre eller ordrelinje, tildeles den en standardkontrolmetode for leveringsdato. Ordrehovedet starter altid med den globale standardmetode. Hvis der er knyttet en tilsidesættelse til en bestilt vare, bruger den nye ordrelinje denne tilsidesættelse. Ellers bruger den nye ordrelinje også den globale standardmetode. Du skal derfor angive standardmetoder, så de matcher den metode til leveringsdatokontrol, du bruger oftest. Når du har oprettet en ordre, kan du tilsidesætte standardmetoden på ordrehoved- og/eller ordrelinjeniveau efter behov. Yderligere oplysninger finder du i [Angive standardmetoder for leveringsdatokontrol](#default-methods) og [Ændre eksisterende salgsordrer, så de bruger LE](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Se bekræftede leveringsdatoer, når der bruges LE til planlægningsoptimering

Hvis du bruger planlægningsoptimering, anvendes LE-beregninger på ordrer og/eller ordrelinjer, hvor feltet **Leveringsdatokontrol** er angivet til *LE til planlægningsoptimering*.

For salgslinjer, der bruger LE til planlægningsoptimering, er felterne **Bekræftet afsendelsesdato** og **Bekræftet modtagelsesdato** tomme, indtil du kører den relevante dynamiske plan (typisk ved hjælp af et periodisk batchjob). De angives derefter automatisk. Du kan finde flere oplysninger i [Planlægge LE for beregninger af planlægningsoptimering](#batch-job).

Feltet **Status for LE til planlægningsoptimering** angiver, om der er beregnet bekræftede datoer for hver linje, der bruger LE til planlægningsoptimering. Feltet viser værdien *Ikke klar* til linjer og ordrer, hvor de bekræftede leveringsdatoer enten ikke er beregnet endnu eller ikke længere er gyldige på grund af andre ændringer. Den viser værdien *Klar* til linjer og ordrer, der er beregnet. Du kan få vist status for hver linje og for hele ordren.

- Hvis du vil se status for en salgsordrelinje, skal du åbne salgsordren og vælge salgslinjen. Gennemgå derefter værdien for **LE til planlægningsoptimering** under fanen **Levering** i oversigtspanelet **Linjedetaljer**. Felterne **Bekræftet afsendelsesdato** og **Bekræftet modtagelsesdato** for linjen vises også under denne fane, når de er beregnet.
- Hvis du vil se status for en hel ordre, skal du åbne salgsordren og vælge **Overskrift**. Gennemgå derefter værdien for **LE til planlægningsoptimering** i oversigtspanelet **Levering**. Felterne **Bekræftet afsendelsesdato** og **Bekræftet modtagelsesdato** for ordren vises også under denne fane, når de er beregnet.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Hvis du opdaterer en salgsordrelinje, efter at LE til planlægningsoptimering har beregnet bekræftede datoer for den, rydder systemet disse datoer indtil næste gang, den relevante dynamiske plan køres.
> - Hvis du redigerer en relateret indstilling, der kan påvirke eksisterende bekræftede datoer (f.eks. ved at ændre leveringstider, reservationer eller afmærkninger), skal du rydde de bekræftede datoer for de relevante eksisterende ordrer. Denne handling bevirker, at status for hver relevant linje ændres til *Ikke klar*. Denne ændring vil medføre, at systemet genberegner de bekræftede datoer, næste gang den dynamiske plan køres.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a>Ændre eksisterende salgsordrer, så de bruger LE

Du kan når som helst ændre værdien af **Leveringsdatokontrol** for enhver åben ordre. Du kan ændre værdien på overskriftsniveau og/eller for hver linje efter behov.

### <a name="change-to-ctp-at-the-order-header-level"></a>Skifte til LE på ordreoverskriftsniveau

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Hvis du vil ændre en ordre, så den bruger LE på ordreoverskriftsniveau, skal du følge disse trin.

1. Gå til **Debitor \> Ordrer \> Alle salgsordrer**.
1. Åbn den salgsordre, du vil konfigurere, eller opret en ny.
1. Vælg **Overskrift** for at åbne overskriftsoplysningerne på siden **Oplysninger om salgsordre**.
1. I oversigtspanelet **Levering** skal du angive feltet **Leveringsdatokontrol** til en af følgende værdier, afhængigt af det planlægningsprogram du bruger:

    - *CTP* – Brug den LE-beregning, der er angivet af det indbyggede varedisponeringsprogram. Hvis du bruger Planlægningsoptimering, er metoden *LE* for leveringsdatokontrol ikke tilladt. Hvis du vælger denne værdi, opstår der derfor en fejl, når beregningen køres.
    - *LE til planlægningsoptimering* – Brug den LE-beregning, der er leveret af Planlægningsoptimering. Denne indstilling har ingen virkning, hvis du bruger det indbyggede varedisponeringsprogram.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Vælg **OK** for at anvende ændringerne.

### <a name="change-to-ctp-at-the-order-line-level"></a>Skifte til LE på ordrelinjeniveau

Hvis du har oprettet en ordrelinje ved at bruge en anden kontrolmetode for leveringsdato, kan du når som helst skifte til LE. Ændringer, du foretager på linjeniveau, påvirker ikke andre linjer. De kan dog medføre, at de overordnede leveringsdatoer for ordren flyttes frem eller tilbage, afhængigt af hvordan de enkelte opdaterede linjeberegninger ændres. <!-- KFM: Confirm this intro at next revision -->

Hvis du vil ændre en ordre, så den bruger LE til indbygget varedisponering på linjeniveau, skal du følge disse trin.

1. Gå til **Debitor \> Ordrer \> Alle salgsordrer**.
1. Åbn den salgsordre, du vil konfigurere, eller opret en ny.
1. Vælg den salgsordrelinje, du vil konfigurere, i oversigtspanelet **Salgsordrelinje** på siden **Salgsordredetaljer**.
1. Under fanen **Levering** i oversigtspanelet **Linjedetaljer** skal du angive feltet **Leveringsdatokontrol** til en af følgende værdier, afhængigt af det planlægningsprogram du bruger:

    - *CTP* – Brug den LE-beregning, der er angivet af det indbyggede varedisponeringsprogram. Hvis du bruger Planlægningsoptimering, er metoden *LE* for leveringsdatokontrol ikke tilladt. Hvis du vælger denne værdi, opstår der derfor en fejl, når beregningen køres.
    - *LE til planlægningsoptimering* – Brug den LE-beregning, der er leveret af Planlægningsoptimering. Denne indstilling har ingen virkning, hvis du bruger det indbyggede varedisponeringsprogram.

    Dialogboksen **Tilgængelige afsendelses- og modtagelsesdatoer** vises med de tilgængelige afsendelses- og modtagelsesdatoer. Denne dialogboks fungerer på samme måde for ordrelinjer som i ordreoverskriften som beskrevet i forrige afsnit.

1. Vælg **Gem** i handlingsruden.
