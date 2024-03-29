---
title: Oversigt over kredit og rykkere
description: Denne artikel indeholder en oversigt over funktionerne for kredit og opkrævninger.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72a5ae9330be1b5b8284c12dd7974e1b7e479ebb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845339"
---
# <a name="credit-and-collections-overview"></a>Oversigt over kredit og opkrævninger

[!include [banner](../includes/banner.md)]

Du kan administrere kreditmaksimum for kunderne og udføre rykkeraktiviteter, når det bliver nødvendigt.

## <a name="credit-management"></a>Kreditstyring

Du kan bruge kundekreditstyring til at administrere kreditmaksimum og styre forløbet af salgsordrer via bogføringsprocessen ud fra de kreditregler, du opretter.

Kreditstyringsprocessen kan omfatte et eller flere af følgende trin:

- Opdatering af kreditattributter for kunder for at give yderligere oplysninger om deres kreditværdighed.
- Oprettelse af kreditmaksimum for kunder ved hjælp af kreditmaksimumreguleringer.
- Oprettelse af midlertidigt kreditmaksimum for kunder ved hjælp af kreditmaksimumreguleringer. På denne måde kan du midlertidigt øge eller mindske kundens kreditmaksimum på basis af forretningsbehov.
- Tilføjelse af oplysninger, der kan påvirke kreditmaksimum, f.eks. oplysninger om forsikring og garantier.
- Oprettelse af kundekreditgrupper, der knytter kunder sammen, så de deler ét kreditmaksimum.
- Tildeling af risikovurderinger til kunderne med efterfølgende anvendelse af vurderinger til automatisk generering af kreditmaksimum for disse kunder via kreditmaksimumreguleringer.
- Oprettelse af blokeringsregler, der sætter en ordre på hold under en eller flere bogføringsprocesser, baseret på faktorer som risiko, betalingsbetingelser, kreditmaksimum, forfaldne beløb og den procentdel af kreditmaksimum, der er brugt.
- Administration af en liste over salgsordrer, der er på hold, gennemgang af årsagerne til ventepositionen og afhjælpning af problemerne.
- Frigivelse af salgsordrer, så de fortsætter gennem bogføringsprocessen.
- Konfiguration af en arbejdsgang for at administrere godkendelse af ændringer af kreditmaksimum og salgsordrefrigivelser.

## <a name="collections-management"></a>Opkrævningsstyring

Siden **Rykkere** indeholder en centraliseret visning til administration af oplysninger om rykkere for debitorer. De opkrævningsansvarlige kan bruge denne centraliserede visning til at administrere rykkere. Inkassatorerne kan begynde rykkerprocessen enten fra debitorlisten, der genereres ved hjælp af foruddefinerede rykkerkriterier, eller fra siden **Debitorer**.

Før du begynder at oprette eller arbejde med rykkere, skal du kende følgende begreber:

- Aldersfordelte øjebliksbillede for debitorer indeholder saldooplysninger på et bestemt tidspunkt.
- Kundepuljer for rykkere hjælper dig med at organisere dit arbejde.
- Inkassatorer kan have deres egne kundepuljer.
- Listesider organiserer kunder, aktiviteter og sager for rykkere.
- Alle rykkeroplysningerne for en debitor findes på en side, og du kan udføre handlinger fra den pågældende side.
- Renter og gebyrer kan frafaldes, genindføres eller tilbageføres i ét trin.
- Afskrivningsposteringer kan oprettes i ét trin.
- Betalinger med ikke tilstrækkelige midler – NSF-betalinger (Non-sufficient Funds – USA) – kan behandles i ét trin.

Beskrivelser af disse begreber finder du i [Nøglebegreber for opkrævningsstyring](./cm-collections-concepts.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfiguration af parametre for kundekreditstyring](./cm-credit-mgmt-setup.md)

[Konfigurationsoplysninger for kundekreditstyring](./cm-setup-information.md)

[Tilføje kreditstyringsoplysninger for en kunde](./cm-add-credit-mgmt-information-customer.md)

[Kundekreditgrupper](./cm-customer-credit-groups.md)

[Reguleringer af kundekreditmaksimum](./cm-credit-limit-adjustments.md)

[Kredithold for salgsordrer](./cm-sales-order-credit-holds.md)

[Periodiske opgaver for kundekreditstyring](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
