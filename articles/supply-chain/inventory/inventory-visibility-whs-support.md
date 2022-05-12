---
title: Understøttelse af Inventory Visibility for WHS-varer
description: Dette emne beskriver lagersynlighed at understøtte varer, der er aktiveret til avancerede lagerstedsprocesser (WHS-varer).
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
ms.openlocfilehash: cfbff05697f4159cb74d110887b8029f28fbf96b
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625383"
---
# <a name="inventory-visibility-support-for-whs-items"></a>Understøttelse af Inventory Visibility for WHS-varer

[!include [banner](../includes/banner.md)]

Dette emne beskriver lagersynlighed at understøtte varer, der er aktiveret til avancerede lagerstedsprocesser (WHS-varer). Den funktion, der føjer denne egenskab til lagersynlighed, kaldes *Avanceret WHS*.

## <a name="whs-items"></a>WHS-varer

En WHS-vare er en vare, der er aktiveret til behandling af avancerede lagersteder (WHS) og behandles på et lagersted, som også er WHS-aktivereret.

Du kan finde flere oplysninger om WHS og modulet **Lagerstedsstyring** i Microsoft Dynamics 365 Supply Chain Management i [Oversigt over Lagerstedsstyring](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Område for funktionen

Funktionen Avanceret WHS for Lagersynlighed fokuserer på beregninger af lagerbeholdninger, der er baseret på beholdningsforespørgsler. Funktionen, der har til formål at give dig mulighed for at bruge Lagersynlighed til at administrere lagerstedsbehandlingsaktiviteter generelt. Lagersynlighed viser ikke lagerstedsspecifikke begreber for brugerne. Her er nogle eksempler på disse koncepter:

- Reservationshierarki
- Om en vare eller et lagersted er WHS-aktiveret
- Id for enhedsseriegruppe
- Lagerstedsspecifikke processer som f.eks. forsendelser, belastninger, bølger og arbejde

Lagersynlighed udleder disse oplysninger, baseret på de data, der sendes fra Supply Chain Management. De WHS-specifikke data (dvs. data fra tabellen `WHSInventReserve`), der ikke er synlige for brugerne.

Når du bruger funktionen Avanceret WHS til lagersynlighed, vil alle forespørgselsresultater være identiske med resultaterne af forespørgsler, der foretages direkte i Supply Chain Management. De vil dog ikke være identiske med resultaterne fra forespørgsler, der foretages ved hjælp af mobilappen Warehouse Management, da mobilappen bruger en lidt anden beregningslogik.

## <a name="when-to-use-the-feature"></a>Hvornår bruges funktionen

Det anbefales, at du bruger funktionen Avanceret WHS til lagersynlighed i scenarier, hvor alle følgende betingelser er opfyldt:

- Du synkroniserer Supply Chain Management-data med lagersynlighed.
- Du bruger WHS i Supply Chain Management.
- Brugere foretager reservationer af WHS-varer på andre niveauer end lagerstedsniveauet (f.eks. fordi du bruger lagerstedsarbejde).

I andre scenarier er resultaterne af beholdningsforespørgslen de samme, uanset om funktionen Avanceret WHS for Lagersynlighed er aktiveret. Desuden er ydeevnen bedre, hvis du ikke aktiverer funktionen i disse scenarier, da der er færre beregninger og mindre indirekte omkostninger.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Aktivere funktionen Avanceret WHS for lagersynlighed

Aktivere funktionen Avanceret WHS for lagersynlighed ved at følge disse trin.

1. Log på dit Supply Chain Management som administrator.
1. Åbn arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), og aktivér følgende funktioner således:

    1. *Integration af lagersynlighed*
    1. *Aktivér lagerstedsvarer i lagersynlighed*

1. Gå til **Lagerstyring \> Opsætning \> Parametre for integration af lagersynlighed**.
1. Under fanen **Aktiver WHS-enheder** skal du angive indstillingen **Aktivér WHS-enheder** til *Ja*.
1. Log på Power Apps.
1. Hvis du vil bruge dem, skal du åbne siden **Konfiguration** i **Funktionsstyring** og derefter aktivere funktionen *AdvancedWHS*.
1. Gå til **Lagerstyring \> Periodiske opgaver \> Integration af lagersynlighed** i Supply Chain Management.
1. Vælg **Deaktiver** i handlingsruden, hvis du midlertidigt vil deaktivere lagersynlighed.
1. I handlingsruden skal du vælge **Aktiver** for at udføre lagerreguleringen. Tilføjelsesprogrammet indlæses igen, og den nye funktion er nu aktiveret. Dine WHS-relaterede data begynder at blive synkroniseret med lagersynlighed.

## <a name="query-on-hand-quantities-of-whs-items"></a>Forespørge på disponible antal af WHS-varer

Hvis du vil forespørge på WHS-varer, skal du bruge samme [API (Application Programming Interface)](inventory-visibility-api.md) og den samme meddelelsessyntaksen for alle varer, der ikke er fra WHS. Du behøver ikke angive, om en vare er en WHS-vare eller en anden vare end WHS-varen. Under lagersynlighed skelnes der automatisk mellem varer på basis af de data, der gemmes.

Resultaterne af forespørgslerne for WHS-varer er stort set de samme som resultaterne af varer, der ikke er med WHS-varer. Den eneste forskel er, at følgende fysiske mål fra `fno`-datakilden beregnes ud fra WHS-logik i Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Alle andre fysiske målinger beregnes på samme måde, som når funktionen Avanceret WHS til lagersynlighed deaktiveres.

Du kan finde detaljerede oplysninger om, hvordan lagerberegninger for WHS-varer arbejder, i hvidbogen [Reservationer i Lagerstedsstyring](https://www.microsoft.com/download/details.aspx?id=43284).

De dataenheder, der eksporteres til Dataverse, kan endnu ikke opdatere antallet af WHS-varer. De antal, der vises i dataenhederne, er korrekte, både for varer, der ikke er fra WHS, og for antal, der ikke påvirkes af WHS-logikken (det vil sige, målinger undtagen `AvailPhysical`, `AvailOrdered`, `ReservPhysical` og `ReservOrdered` i datakilden `fno`).

Ændringer i WHS-vareantal, der er lagret i datakilden for Supply Chain Management, er ikke tilladt. Hvad det er for andre funktioner i lagersynlighed, der gennemtvinges for at forhindre konflikter.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>Foreløbig reservation af WHS-varer i Lagersynlighed

Generelt understøttes [foreløbige reservationer](inventory-visibility-reservations.md) på WHS-varer. Du kan medtage WHS-relaterede fysiske mål i beregninger af forhåndsreservationer. 

Inden for en kendt begrænsning understøttes den *aktuelt tilgængelige for reservationsberegning* ikke for WHS-varer. Hvis der derfor er en reservation over de aktuelle dimensioner, hvor der forekommer en forhåndsreservation, er den *tilgængelige for reservationsberegningen* forkert. Foreløbige reservationer påvirkes ikke, når indstillingen **ifCheckAvailForReserv** er deaktiveret i [API til reservation](inventory-visibility-api.md#create-one-reservation-event).

Denne begrænsning gælder også for funktioner og tilpasninger, der er baseret på særlige reservationer (f.eks. tildeling).

## <a name="calculate-available-to-promise-quantities"></a>Beregne disponible mængder

Løsningen understøtter fuldt ud [den disponible til tilsagn (ATP)](inventory-visibility-available-to-promise.md) for WHS-varer. Du kan definere ATP-beregninger uden behovsspecifikke WHS-oplysninger.
