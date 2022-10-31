---
title: Forbedring af ydeevne ved aktivering af kontostruktur
description: Denne artikel beskriver den nye forbedring af ydeevnen til aktiveringsprocessen af kontostrukturen.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713993"
---
# <a name="account-structure-activation-performance-enhancement"></a>Forbedring af ydeevne ved aktivering af kontostruktur

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne forbedring af ydeevnen lader dig aktivere kontostrukturer hurtigere ved at køre flere transaktionsopdateringer samtidigt. Desuden er selve strukturen markeret som aktiv, når den er valideret, og transaktionsbehandlingen kan fortsætte mens eksisterende ikke-bogførte transaktioner opdateres til den nye struktur. Da transaktionsopdateringer kan tage et stykke tid, kan du spore status af din aktivering ved at vælge **Vis aktiveringsstatus** over gitteret på siden **Kontostrukturer**. Du kan også få vist din aktiveringsstatus ved at vælge **Vis** på handlingsruden og derefter vælge **Aktiveringsstatus** på rullemenuen.

[![Siden Kontostrukturer.](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Når du har valgt **Vis aktiveringsstatus**, vises en dialogboks, som viser den enkelte opgave, der kører, som del af aktiveringsprocessen. For hver opgave kan du få vist status og, når opgaven er fuldført, fuldførelsesdatoen og -klokkeslættet.

[![Tidslinje for aktivering af kontostruktur.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Aktiveringstip til kontostruktur

Den dialogboks til aktivering af kontostrukturen, som vises, når du vælger **Aktiver** for en kladdekontostruktur, har en fanesektion med navnet **Opdater ikke-bogførte transaktioner**. Denne sektion indeholder en indstilling med navnet **Gennemtving opdatering**. Du kan vælge denne indstilling for at opdatere alle ikke-bogførte transaktioner til den aktuelle struktur. Du bør imidlertid kun bruge denne indstilling, når er der opstået en fejl, eller Microsoft Support har bedt dig om at bruge den.

Her er nogle af de faktorer, der kan påvirke aktiveringsprocessens ydeevne:

- Et stort antal ikke-bogførte kladdeposter
- Et stort antal åbne kildedokumentposter, f.eks. fritekstfakturaer, kreditorfakturaer og relaterede dokumenter, der bruger kildedokumentstruktur og har åbne regnskabsfordelinger
- Datamængden i TaxUncommitted
- Beløbet af åbne budgetdata
- Importere kladdedata, mens der stadig køres aktiveringsopgaver

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
