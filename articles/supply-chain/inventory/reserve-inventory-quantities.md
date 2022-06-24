---
title: Reservere lagerantal
description: Denne artikel beskriver de forskellige indstillinger, der er tilgængelige for lagerreservation.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c407b45f3df91d569c2bf043ff9f83b640837bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899434"
---
# <a name="reserve-inventory-quantities"></a>Reservere lagerantal

[!include [banner](../includes/banner.md)]

Denne artikel beskriver de forskellige indstillinger, der er tilgængelige for lagerreservation.

Der kan automatisk reserveres lagerantal i forbindelse med en bestemt ordre. Det betyder, at reserveret lager ikke kan trækkes fra lagerstedet i forbindelse med andre ordrer, medmindre lagerreservationen eller en del af lagerreservationen annulleres.

Der er følgende årsager til en reservation af lager:
-   Først bestilt, først leveret, hvilket betyder, at kunder modtager disponible varer i samme rækkefølge, som de afgiver ordrerne.
-   Mangel på varer i tilfælde af lang eller ukendt leveringstid fra leverandøren. Du kan evt. sikre dig, at bestemte kunder eller ordrer modtager de først disponible varer.
-   Visse kunder og visse ordretyper har første prioritet i forbindelse med levering.
-   Varer med serie- eller batchnumre. Du kan markere bestemte varer, der er eller vil blive leveret, til bestemte ordrer.
-   Varer, der er specielt bestilt, og som reserveres i forbindelse med bestemte ordrer.
-   Produktionsordrer. Du kan f.eks. markere varer, der er produceret til og tilpasset bestemte ordrer.

Lageret kan reserveres automatisk, når der oprettes en ny ordrelinje, eller lageret kan reserveres manuelt for de enkelte ordrer. Det er også muligt at reservere lager på forskellige stadier i en produktionsproces. Kun produkter på lager kan reserveres. Serviceydelser kan ikke reserveres, fordi der ikke er nogen disponibel lagerbeholdning. Både disponibel lagerbeholdning og bestilt, men endnu ikke modtaget lager, kan reserveres. Hvis der reserveres et større antal, end der findes i den disponible lagerbeholdning, får du vist en meddelelse om, at det ikke er muligt at reservere et så stort antal. Du kan derefter enten reservere antallet alligevel, eller du kan ændre det bestilte antal. Antallet kan enten reserveres eller ændres. Hvis der reserveres flere varer end det disponible antal, dækkes mankoen ind, næste gang der er disponible varer til levering.

## <a name="inventory-reservation-policies"></a>Politikker for lagerreservation
Politikker for lagerreservation angives på siden **Varemodelgrupper,** siden **Parametre til lager- og lokationsstyring** og siden **Produktionsparametre**.
### <a name="policies-on-the-item-model-groups-page"></a>Politikker på siden Varemodelgrupper

Afsnittet **Lagerpolitikker** indeholder følgende reservationspolitikker.

| &nbsp;                  | &nbsp;                                                                                                                                     |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reservationspolitik**  | **Beskrivelse**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| FIFO-datokontrolleret    | Hvis du vælger indstillingen **FIFO-datokontrolleret**, styres lagerreservationen af en sorteringsdato i overensstemmelse med FIFO-princippet. Batches reserveres ud fra den tidligste dato for varetilgang ifølge FIFO-princippet.                                                                                                                                                                                                                                                                       |
| Bagud fra afsendelsesdato | Denne indstilling er kun tilgængelig, hvis du har valgt indstillingen **FIFO-datokontrolleret**. Hvis du vælger **Bagud fra afsendelsesdato**, foretages lagerreservationen bagud fra den ønskede afsendelsesdato i overensstemmelse med LIFO-princippet. Hvis ingen tilgange er tilgængelige før afsendelsesdatoen, bruges der en FIFO-reservation.                                                                                                                                                                                                           |
| Reservation af varesalg  | Bestemmer, om reservationen er manuel eller automatisk. Hvis en reservation er automatisk, reserveres lager, når der oprettes ordrelinjer. Det er muligt at foretage reservationer på varenummerniveau til styklister (**Automatisk**-indstilling) eller for de enkelte elementer af en Stykliste (**Udfoldning**-indstilling). Standardværdien for **Reservation af varesalg** kan nedarves fra **Debitorparametre.** På denne side angives værdien i feltet Reservation i **sektionen** **Salgsstandardværdier** under fanen **Generelt**. |
| Valg af samme batch    | Hvis du reserverer fra samme batch, kan du reservere lager til en salgsordrelinje i forhold til en enkelt lagerbatch. Hvis du vil bruge denne indstilling, skal du også angive indstillingen **Konsolider krav** til **Ja**. Der er flere indstillinger, der skal bruges til sporingsdimensionsgruppen og lagringsdimensionsgruppen. Yderligere oplysninger finder du [Reserver samme batch for en salgsordre](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Konsolider krav | Denne indstilling er meget lig **Valg af samme batch** og konsoliderer lager, der er reserveret til salgsordrelinjer i et enkelt krav.                                                                                                                                                                                                                                                                                                                                                                                      |
| FEFO-datokontrolleret    | Denne indstilling gør det muligt at reservere batches, der er tæt på deres udløbsdato eller sidste holdbarhedsdato. Du skal også angive feltet **Kriterier for plukning** til enten **Udløbsdato** eller **Bedst før-dato**.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>Eksempel på FIFO-datokontrolleret og Bagud fra afsendelsesdato

I dette eksempel findes disponibel lagerbeholdning for varenummer A for tre forskellige batchnumre.

| varenummer | Batchnummer | Mængde | Dato             |
|-------------|--------------|----------|------------------|
| A           | 1000         | 5        | 2. februar 2016 |
| A           | 1001         | 3        | 1. januar 2016  |
| A           | 1002         | 7        | 3. marts 2016    |

Ved en salgsordre, der skal reserveres automatisk og leveres den 4. april 2016, reserveres følgende batchnumre:
-   Hvis hverken afkrydsningsfeltet **FIFO-datokontrolleret** eller **Bagud fra afsendelsesdato** er markeret, reserveres batch 1000, da det har det laveste nummer.
-   Hvis afkrydsningsfeltet **FIFO-datokontrolleret** er markeret, og **Bagud fra afsendelsesdato** ikke er markeret, reserveres batch 1001, da det har første tilgangsdato (FIFO).
-   Hvis både afkrydsningsfeltet **FIFO-datokontrolleret** og **Bagud fra afsendelsesdato** markeres, reserveres batch 1002, da det er den batchtilgang, der er nærmest salgsordrens afsendelsesdato.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Politikker på parametersiden for lager- og lokationsstyring

Der er to indstillinger, der er relateret til reservationer på siden **Parametre til lager- og lokationsstyring**:
-   Med indstillingen **Reserver bestilte varer** under fanen **Generelt** kan du reservere varetilgange, som kun bestilles ud fra vareafgange i Debitor, Projektstyring og regnskab og Produktionsstyring. Hvis du fravælger denne indstilling, kan du kun reservere varer, som fysisk er modtaget på lageret. Hvis en bestemt vare er konfigureret til at acceptere negativt lager, er dette felt ikke relevant.
-   Indstillingen **Reserver varer automatisk** under fanen **Transport** bestemmer standardindstillingen, hvis varerne er reserveret automatisk til flytteordrer. Indstillingen kan tilsidesættes for enkelte flytteordrer.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Politikker for lagerreservation på siden Produktionsparametre

Værdien af feltet **Reservation** under fanen **Generelt** på siden **Produktionsparametre** angiver standardpunkt i produktionsprocessen, hvor lageret skal reserveres. For eksempel kunne lageret reserveres, når arbejdet planlægges, eller når arbejdet startes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]