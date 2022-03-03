---
title: Oprydning af salgsopdateringshistorikken mislykkes, eller der er problemer med ydeevnen
description: Batchjobbet til oprydning af salgshistorikken kan mislykkes eller tage meget lang tid, hvis der er en stor mængde salgsopdateringsdata.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 371a8c7178cd7c5091d6dd9a91d0ee03b943a269
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103182"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Oprydning af salgsopdateringshistorikken mislykkes, eller der er problemer med ydeevnen

## <a name="symptoms"></a>Symptomer

**Oprydning af salgsopdateringshistorikken** mislykkes, eller der er problemer med ydeevnen.  

## <a name="cause"></a>Årsag

Dette kan ske, når systemet indeholder et stort antal salgsopdateringer, hvilket kan resultere i en stor mængde salgsopdateringsdata. Ved oprydningsjobbet bliver det forsøgt at rydde op i alle disse data i én postering. Derfor kan det tage meget lang tid at køre jobbet eller mislykke det.

## <a name="resolution"></a>Løsning

En ny version af jobbet til **oprydning af salgsopdateringshistorikken** er tilgængeligt for Supply Chain Management version 10.0.19 og højere. Denne funktion er som standard ikke slået til. Yderligere oplysninger om, hvordan det fungerer, og hvordan det aktiveres i funktionsstyring, finder du i [Forbedringer af ydeevne i salgshistorikken](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

