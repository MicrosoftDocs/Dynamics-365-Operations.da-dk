---
title: Lagerregulering for lagersted
description: Denne artikel indeholder oplysninger om lagerstedets lagerreguleringskladde og behandling, når du bruger skaleringsenheder.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a4d892cd9e7f518c43df7197fc443b9a284e72b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893549"
---
# <a name="warehouse-inventory-adjustment"></a>Lagerregulering for lagersted

[!include [banner](../includes/banner.md)]

Funktionen Lagersteds lagerregulering anvendes ved kørsel af cloud- og kantskaleringsenheder til [produktionsbelastninger](cloud-edge-workload-manufacturing.md) og [belastninger i lagerstyring](cloud-edge-workload-warehousing.md).

Når en arbejder udfører en lagerregulering ved hjælp af lagerstedsappen i forhold til belastningen for lagerstedsstyring i en skaleringsenhed, skal opdateringen af den fysiske disponible lagerbeholdning behandles af batchjobbet **Lagerregulering for lagersted**, som du kan køre og planlægge ved at gå til **Lagerstedsstyring > Periodiske opgaver > Lagerreguleringskladde for lagersted**.

Følgende arbejdsprocesser for lagerstedsappen bruger aktuelt **Lagerreguleringskladde for lagersted** til arbejdsbelastninger for skaleringsenhed:

- Regulering ind/ud
- Cyklusoptælling
- Indlæsning af nummerplade

Flere lagertransaktioner oprettes som en del af hver lagerreguleringsproces, fordi hubbens og skaleringsenhedens installationer deler lagerposter.

## <a name="inventory-adjustment-example"></a>Eksempel på lagerregulering

I dette eksempel har en lagerarbejder brugt lagerstedsappen til at registrere tilføjelse af disponibel lagerbeholdning.

For det første opretter arbejdsbelastningen for skaleringsenheden en lagerreguleringstransaktion for lagerstedet med henblik på den positive fysiske regulering, som derefter synkroniseres med hubben og resulterer i en stigning i den disponible lagerbeholdning i hubbben.

| Type                                    | Skalaenhed | Vej | Hub |
|-----------------------------------------|------------|-----------|-----|
| Lagerregulering for lagersted          | +1         | ->        | +1  |

Derefter behandler hubben en optællingskladdebogføring, der modtages via [meddelelser for meddelelsesprocessoren](cloud-edge-message-processor-messages.md). Derved opdateres den ekstra disponible lagerbeholdning. For at forhindre dobbelt disponibel lagerbeholdning opretter hubnen en modkontering som en del af denne proces og fjerner den tidligere registrerede disponible lagerbeholdning, som er knyttet til lagerreguleringen for lagerstedet.

| Type                                    | Skalaenhed | Vej | Hub |
|-----------------------------------------|------------|-----------|-----|
| Tælling                                | +1         | <-        | +1  |
| Lagerregulering for lagersted (modkontering) | -1         | <-        | -1  |

Når en skaleringsenhed har oprettet en **Lagerreguleringskladde for lagersted** i hubben, kan du gennemse både den **Optællingskladde** og **Modkonteringskladde**, som er oprettet af hubben som en del af reguleringsprocessen.

Du kan gennemgå hver af disse kladdeposter og transaktioner i Supply Chain Management ved at gøre følgende:

1. Log på skaleringsenheden.
1. Gå til **Lagerstedsstyring \> Periodiske opgaver \> Lagerreguleringskladde for lagersted**.
1. Søg efter og åbn den kladde, der registrerede ændringen af den disponible lagerbeholdning, på siden **Lagerreguleringskladde for lagersted**. Sektionen **Kladdelinjer** viser hver regulering, der er registreret i denne kladde.
1. Log på hubben.
1. Gå til **Lagerstedsstyring \> Periodiske opgaver \> Lagerreguleringskladde for lagersted**.
1. På siden **Lagerreguleringskladde for lagersted** bør du kunne se den samme kladde, hvis hubben og skaleringsenheden er synkroniserede.
1. Åbn kladden. Hvis [meddelelserne fra meddelelsesprocessoren](cloud-edge-message-processor-messages.md) er blevet behandlet, vises hyperlinks til **Optællingsklade** og **Modkonteringskladde** i hovedet.
    - **Optællingskladde** skal vise de samme dimensionsværdier som kladdelinjerne.
    - **Modkonteringskladde** skal vise modkonteringen, der fjerner den dobbelte lagerregulering.
    > [!NOTE]
    > Når al synkronisering og behandling er fuldført, synkroniseres **Optællingskladde** og **Modkonteringskladde** tilbage til skaleringsenheden. De kan også ses fra den relevante side for **Lagerreguleringskladde for lagersted**.
