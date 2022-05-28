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
ms.openlocfilehash: f95dff3a77a552d5788d813b3d13dc30579be715
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695701"
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
