---
title: Standardbeskrivelser af finans
description: Standardbeskrivelser kan bruges til opdatering af feltet Beskrivelse i bilagsbogføringer til finans.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d5a38af57d614ae2c93b0af74ec4a1c085519d46
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841884"
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
