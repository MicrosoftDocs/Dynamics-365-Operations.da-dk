---
title: Konfigurere indekssatser
description: I dette emne forklares, hvordan du konfigurerer indekssatser. Der kræves indekssatser, hvis organisationen knytter leasingbetalinger til et sæt indekssatser.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c6396b8c12520abb0e33cda713d5483f61610db4
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726516"
---
# <a name="set-up-index-rates"></a>Konfigurere indekssatser

[!include [banner](../includes/banner.md)]

Hvis leasingbetalingerne afhænger af et indeks, kan indekssatstyperne tilføjes og vedligeholdes i systemet. Hvis du vil værdiregulere leasingbetalinger fra siden **Indekssatstype**, bruger processen til værdiregulering af indekssatsen den seneste indekssats fra datoen for værdiregulering.

Udfør følgende trin for at tilføje indekssatstyper og indekssatser.

1. Gå til **Aktivleasing \> Konfiguration \> Indekssatstype**.
2. Vælg **Ny**.
3. Angiv satstypen og navnet på indekssatsen i de relevante felter.
4. Hvis du vil tilføje en ny indekssatsværdi, skal du vælge indekssatstypen og derefter vælge **Tilføj**.
5. Vælg satsens gældende startdato, og vælg satsværdien.

Du skal vælge enten **Differenceværdi for indekssats** eller **Værdi for indekssats** for indekssatsmetode.

- Vælg metoden **Værdiforskel for indekssats** for at beregne en ny leasingbetaling, baseret på forskellen mellem indekssatsen på startdatoen og den seneste indekssats. Indekssatsen defineres i feltet **Indekssats (%)**.
- Vælg metoden **Værdi af indekssats** for at beregne leasingbetaling ved hjælp af den procentdel, der er angivet i feltet **Indekssats (%)**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
