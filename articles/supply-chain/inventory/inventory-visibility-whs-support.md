---
title: Understøttelse af Inventory Visibility for WMS-varer
description: Denne artikel beskriver lagersynlighed at understøtte varer, der er aktiveret til lokationsstyringsprocesser (WMS-varer).
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066604"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Understøttelse af Inventory Visibility for WMS-varer

[!include [banner](../includes/banner.md)]

Denne artikel beskriver lagersynlighed at understøtte varer, der er aktiveret til lokationsstyringsprocesser (WMS). Den funktion, der føjer denne egenskab til lagersynlighed, kaldes *Avanceret WMS*.

## <a name="wms-items"></a>WMS-varer

En WMS-vare er en vare, der er aktiveret til behandling af lokationsstyringsprocesser, som også er WMS-aktivereret.

Du kan finde flere oplysninger om WMS og modulet **Lagerstedsstyring** i Microsoft Dynamics 365 Supply Chain Management i [Oversigt over Lagerstedsstyring](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Område for funktionen

Funktionen Avanceret WMS for Lagersynlighed fokuserer på beregninger af lagerbeholdninger, der er baseret på beholdningsforespørgsler. Funktionen, der har til formål at give dig mulighed for at bruge Lagersynlighed til at administrere lagerstedsbehandlingsaktiviteter generelt. Lagersynlighed viser ikke lagerstedsspecifikke begreber for brugerne. Her er nogle eksempler på disse koncepter:

- Reservationshierarki
- Om en vare eller et lagersted er WMS-aktiveret
- Id for enhedsseriegruppe
- Lagerstedsspecifikke processer som f.eks. forsendelser, belastninger, bølger og arbejde

Lagersynlighed udleder disse oplysninger, baseret på de data, der sendes fra Supply Chain Management. De WMS-specifikke data (dvs. data fra tabellen `WHSInventReserve`), der ikke er synlige for brugerne.

Når du bruger funktionen Avanceret WMS til lagersynlighed, vil alle forespørgselsresultater være identiske med resultaterne af forespørgsler, der foretages direkte i Supply Chain Management. De vil dog ikke være identiske med resultaterne fra forespørgsler, der foretages ved hjælp af mobilappen Warehouse Management, da mobilappen bruger en lidt anden beregningslogik.

## <a name="when-to-use-the-feature"></a>Hvornår bruges funktionen

Det anbefales, at du bruger funktionen Avanceret WMS til lagersynlighed i scenarier, hvor alle følgende betingelser er opfyldt:

- Du synkroniserer Supply Chain Management-data med lagersynlighed.
- Du bruger WMS i Supply Chain Management.
- Brugere foretager reservationer af WMS-varer på andre niveauer end lagerstedsniveauet (f.eks. fordi du bruger lagerstedsarbejde).

I andre scenarier er resultaterne af beholdningsforespørgslen de samme, uanset om funktionen Avanceret WMS for Lagersynlighed er aktiveret. Desuden er ydeevnen bedre, hvis du ikke aktiverer funktionen i disse scenarier, da der er færre beregninger og mindre indirekte omkostninger.

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>Aktivere funktionen Avanceret WMS for lagersynlighed

Aktivere funktionen Avanceret WMS for lagersynlighed ved at følge disse trin.

1. Log på dit Supply Chain Management som administrator.
1. Åbn arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), og aktivér følgende funktioner således:

    1. *Integration af lagersynlighed*
    1. *Aktivér lagerstedsvarer i lagersynlighed*

1. Gå til **Lagerstyring \> Opsætning \> Parametre for integration af lagersynlighed**.
1. Under fanen **Aktiver WMS-enheder** skal du angive indstillingen **Aktivér WMS-enheder** til *Ja*.
1. Log på Power Apps.
1. Hvis du vil bruge dem, skal du åbne siden **Konfiguration** i **Funktionsstyring** og derefter aktivere funktionen *AdvancedWHS*.
1. Gå til **Lagerstyring \> Periodiske opgaver \> Integration af lagersynlighed** i Supply Chain Management.
1. Vælg **Deaktiver** i handlingsruden, hvis du midlertidigt vil deaktivere lagersynlighed.
1. I handlingsruden skal du vælge **Aktiver** for at udføre lagerreguleringen. Tilføjelsesprogrammet indlæses igen, og den nye funktion er nu aktiveret. Dine WMS-relaterede data begynder at blive synkroniseret med lagersynlighed.

## <a name="query-on-hand-quantities-of-wms-items"></a>Forespørge på disponible antal af WMS-varer

Hvis du vil forespørge på WMS-varer, skal du bruge samme [API (Application Programming Interface)](inventory-visibility-api.md) og den samme meddelelsessyntaksen for alle varer, der ikke er fra WMS. Du behøver ikke angive, om en vare er en WMS-vare eller en anden vare end WMS-varen. Under lagersynlighed skelnes der automatisk mellem varer på basis af de data, der gemmes.

Resultaterne af forespørgslerne for WMS-varer er stort set de samme som resultaterne af varer, der ikke er med WMS-varer. Den eneste forskel er, at følgende fysiske mål fra `fno`-datakilden beregnes ud fra WMS-logik i Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Alle andre fysiske målinger beregnes på samme måde, som når funktionen Avanceret WMS til lagersynlighed deaktiveres.

Du kan finde detaljerede oplysninger om, hvordan lagerberegninger for WMS-varer arbejder, i hvidbogen [Reservationer i Lagerstedsstyring](https://www.microsoft.com/download/details.aspx?id=43284).

De dataenheder, der eksporteres til Dataverse, kan endnu ikke opdatere antallet af WMS-varer. De antal, der vises i dataenhederne, er korrekte, både for varer, der ikke er fra WMS, og for antal, der ikke påvirkes af WMS-logikken (det vil sige, målinger undtagen `AvailPhysical`, `AvailOrdered`, `ReservPhysical` og `ReservOrdered` i datakilden `fno`).

Ændringer i WMS-vareantal, der er lagret i datakilden for Supply Chain Management, er ikke tilladt. Hvad det er for andre funktioner i lagersynlighed, der gennemtvinges for at forhindre konflikter.

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>Foreløbig reservation af WMS-varer i Lagersynlighed

Generelt understøttes [foreløbige reservationer](inventory-visibility-reservations.md) på WMS-varer. Du kan medtage WMS-relaterede fysiske mål i beregninger af forhåndsreservationer. 

Inden for en kendt begrænsning understøttes den *aktuelt tilgængelige for reservationsberegning* ikke for WMS-varer. Hvis der derfor er en reservation over de aktuelle dimensioner, hvor der forekommer en forhåndsreservation, er den *tilgængelige for reservationsberegningen* forkert. Foreløbige reservationer påvirkes ikke, når indstillingen **ifCheckAvailForReserv** er deaktiveret i [API til reservation](inventory-visibility-api.md#create-one-reservation-event).

Denne begrænsning gælder også for funktioner og tilpasninger, der er baseret på særlige reservationer (f.eks. tildeling).

## <a name="calculate-available-to-promise-quantities"></a>Beregne disponible mængder

Løsningen understøtter fuldt ud [den disponible til tilsagn (ATP)](inventory-visibility-available-to-promise.md) for WMS-varer. Du kan definere ATP-beregninger uden behovsspecifikke WMS-oplysninger.
