---
title: Standardbeskrivelser af finans
description: Standardbeskrivelser kan bruges til opdatering af feltet Beskrivelse i bilagsbogføringer til finans.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7020c39dd599be047e07caa391d6d4c69c426328
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889542"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Standardbeskrivelser af finans

[!include [banner](../../includes/banner.md)]

Standardbeskrivelser kan bruges til opdatering af feltet **Beskrivelse** i bilagsbogføringer til finans. Denne funktionalitet er forbedret, så den kan fungere med Landingsomkostninger.

Du kan oprette standardbeskrivelser til finansbogføringer ved at gå til **Organisationsadministration \> Opsætning \> Standardbeskrivelser**.

Følgende tabel indeholder de nye værdier, der er blevet føjet til feltet **Beskrivelse** på siden **Standardbeskrivelser** for at understøtte landingsomkostninger.

| Beskrivelsestype | Notater |
|---|---|
| Importér efterkalkulation - omkostningsperiodisering | Når en indkøbsordrefaktura bogføres, behandles en omkostningsperiodisering for de estimerede fragtomkostninger. Der kan angives standardbeskrivelser, hvis du vil føje fragtnummeret til beskrivelsen. Brug *%4* som forsendelsesnummer. |
| Importefterkalkulation – Ordre i varer i transit | Hvis du bruger behandling i transit, bogføres indkøbsordrefakturaen, og varerne på en konto for varer i transit. Der kan angives standardbeskrivelser, hvis du vil føje transitordrenummeret til beskrivelsen. Brug *%4* til transitordrenummeret. |
| Lager - Lukning - Regulering | Når kreditorfakturaen behandles for en fragtomkostning, behandles der en lagerregulering for at estimere fragtomkostninger. Der kan angives standardbeskrivelser, hvis du vil føje fragtnummeret til beskrivelsen. Brug *%4* som forsendelsesnummer. |

Du kan finde flere oplysninger om, hvordan du arbejder med siden **Standardbeskrivelser**, i [Oprette standardbeskrivelser til automatisk bogføring](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
