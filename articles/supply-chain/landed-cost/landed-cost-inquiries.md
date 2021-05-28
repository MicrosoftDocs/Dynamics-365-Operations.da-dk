---
title: Forespørgsler om landingsomkostninger
description: Dette emne beskriver, hvordan du finder og bruger de forskellige typer forespørgsler, der er tilgængelige i modulet Landingsomkostninger.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c1441a7006bc8647efc449bec6fa6fa801c141b0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018655"
---
# <a name="landed-cost-inquiries"></a>Forespørgsler om landingsomkostninger

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Forespørgsler på fragtlinjer

Forespørgslen **Fragtlinjer** viser alle fragtlinjer, som de vedrører lageret. Denne forespørgsel kan bruges som filter, så du lettere kan finde en vare, en indkøbsordre eller en anden nyttig oplysning. Den kan også bruges til at identificere den forventede leveringsdato for en vare, der kan være i en eller flere fragter. På denne måde kan den hjælpe dig med at administrere forventet lagertilgang.

Du kan åbne denne forespørgsel ved at gå til **Landingsomkostninger \> Forespørgsler \> Fragtlinjer**.

### <a name="overview-tab"></a>Fanen Oversigt

Fanen **Oversigt** på forespørgselssiden **Fragtlinjer** indeholder et gitter, der viser grundlæggende oplysninger om hver relevant fragtlinje. Følgende tabel beskriver kolonnerne i gitteret.

| Kolonne | Beskrivelse |
|---|---|
| **Varenummer** | Varen for fragtlinjen. |
| **Reference** | Ordretypen (indkøbsordre eller flytteordre). |
| **Tal** | Nummeret på indkøbsordren eller flytteordren. |
| **Specifikation** | Den folio, som fragtlinjen er tilknyttet. |
| **Forsendelsescontainer** | Den forsendelsescontainer, som fragtlinjen er tilknyttet. |
| **Fragt** | Den fragt, som fragtlinjen er tilknyttet. |
| **Kvantitet** | Vareantallet for fragtlinjen. |
| (Andre dimensioner) | Du kan få vist kolonnerne for flere dimensioner efter behov. Disse dimensioner omfatter batchnummer, lagerstatus og lagersted. Vælg **Lager \> Vis dimensioner** i handlingsruden for at åbne en dialogboks, hvor du kan vælge de dimensioner, der skal medtages. |

### <a name="general-tab"></a>Fanen Generelt

Vælg fanen **Generelt** for at få vist flere oplysninger om den linje, der aktuelt er valgt under fanen **Oversigt**.

### <a name="dimensions-tab"></a>Fanen Dimensioner

Vælg fanen **Dimensioner** for at få vist værdier for alle tilgængelige dimensioner for den linje, der aktuelt er valgt under fanen **Oversigt**, uanset hvilke dimensioner du har valgt at få vist under denne fane.

## <a name="cost-estimate-inquiries"></a>Forespørgsler om omkostningsestimat

Hver gang du genererer et omkostningsestimat, føjes estimatet til forespørgselssiden **Omkostningsestimater**. Du kan få detaljerede oplysninger om, hvordan du kan generere, se og arbejde med omkostningsestimater (herunder estimater på forespørgselssiden), under [Estimere og administrere landingsomkostninger](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Varesporing

Du kan bruge siden **Varesporing** til at få vist åbne indkøbsordrelinjer og deres aktuelle status. Linjer behøver ikke at være knyttet til en fragt for at blive vist her. Hvis en vare er tilknyttet en fragt, viser postlinjen med varesporing dog fragt-id'et.

Du kan åbne denne side ved at gå til **Landingsomkostninger \> Forespørgsler \> Sporing \> Varesporing**.

Da dit system sandsynligvis indeholder et meget stort antal indkøbsordrelinjer, viser siden **Varesporing** først ingen poster. Start med at bruge filterfelterne øverst på siden til at definere det sæt indkøbsordrelinjer, du søger efter. Vælg derefter **Opdater** i handlingsruden for at generere listen. Du kan bruge en stjerne (\*) som jokertegn i alle filterfelter. Hvis du f.eks. vil finde alle indkøbsordrelinjer for varer, der indeholder ordet "DVD" i navnet, skal du angive feltet **Type** til **Produktnavn** og angive *\*DVD\** i feltet **Feltværdi**.

> [!NOTE]
> Restordrer inkluderer i øjeblikket kun salgsordrer. Salgstilbud vises ikke eller betragtes som restordrer.

I følgende tabel beskrives kolonnerne i gitteret på siden **Varesporing**.

| Kolonne | Beskrivelse |
|---|---|
| **Til havn** | Den endelige destination. |
| **Bekræftet** | Den bekræftede dato for indkøbsordrelinjen. |
| **Leveringsdato** | Leveringsdatoen for indkøbsordrelinjen. |
| **Rute** | Fragt-id, hvis linjen er tilknyttet en fragt. |
| **Forsendelsescontainer** | Hvis linjen er tilknyttet en forsendelsescontainer, er det container-id'et. |
| **Forsendelseshavn** | Den aktuelle havn baseret på den første etape i sporingsformularen, hvor der ikke er angivet en faktisk dato for den forsendelsescontainer, der er tilknyttet indkøbsordrelinjen. |
| **Aktivitet** | Den aktuelle aktivitet baseret på den første etape i sporingsformularen, hvor der ikke er angivet en faktisk dato for den forsendelsescontainer, der er tilknyttet indkøbsordrelinjen. |
| **Forventet slutdato** | Den dato, hvor fragten forventes at blive modtaget på destinationslagerstedet. |
| **Navn** | Kreditorens navn. |
| **Fragtstatus** | Den forsendelsesstatus, som indkøbsordrelinjen er tilknyttet. |
| **Varenummer** | Varenummeret til indkøbsordrelinjen. |
| **Eksternt** | Leverandørens varenavn. |
| **Produktnavn** | Navnet på varen for indkøbsordrelinjen. |
| **Kvantitet** | Antallet for indkøbsordrelinjen. |
| **Enhed** | Måleenheden for indkøbsordrelinjen. |
| **Reference** | Ordretypen (indkøbsordre eller flytteordre) |
| **Referencenummer** | Nummeret på indkøbsordren eller flytteordren. |
| **Restordre** | Et symbol angiver, at der er salgsrestordrer for varen. |
| (Andre dimensioner) | Du kan få vist kolonnerne for flere dimensioner efter behov. Disse dimensioner omfatter batchnummer, lagerstatus og lagersted. Vælg **Vis dimensioner** i handlingsruden for at åbne en dialogboks, hvor du kan vælge de dimensioner, der skal medtages. |

### <a name="related-information-about-backorders"></a>Relaterede oplysninger om restordrer

Du kan få vist flere oplysninger om restordrer ved at vælge fanen **Relaterede oplysninger** i højre side af siden og derefter vælge **Restordrer**. Hvis du vil have vist endnu flere oplysninger om en bestemt restordre, skal du markere rækken for den og derefter vælge linket **Mere**.

## <a name="individual-shipping-container-tracking"></a>Sporing af individuel forsendelsescontainer

Forespørgslen **Sporing af individuel forsendelsescontainer** indeholder et filter, som giver dig mulighed for at finde en forsendelsescontainer og derefter identificere alle fragtlinjer i den pågældende container.

Du kan åbne denne forespørgsel ved at gå til **Landingsomkostninger \> Forespørgsler \> Sporing \> Sporing af individuel forsendelsescontainer**.

## <a name="multiple-shipping-container-tracking"></a>Sporing af flere forsendelsescontainere

Forespørgslen **Sporing af flere forsendelsescontainere** indeholder et filter, som giver dig mulighed for at finde en samling af forsendelsescontainere og derefter identificere alle fragtlinjer i disse containere.

Du kan åbne denne forespørgsel ved at gå til **Landingsomkostninger \> Forespørgsler \> Sporing \> Sporing af flere forsendelsescontainere**.
