---
title: Vise gebyrer for en produceret vare
description: En produceret vares konstante omkostninger afspejler opstillingstiderne for operationer og komponenter, der har et konstant antal eller et konstant skrotbeløb.
author: JennySong-SH
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f97495488dbbe504a5e79ef7f65fa97eb287d17b
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675425"
---
# <a name="display-charges-for-a-manufactured-item"></a>Vise gebyrer for en produceret vare

[!include [banner](../includes/banner.md)]

En produceret vares konstante omkostninger afspejler opstillingstiderne for operationer og komponenter, der har et konstant antal eller et konstant skrotbeløb.

Det beregnede beløb for en vares gebyrer kan vises med varens enhedsomkostninger. Gebyrerne vises dog nogle gange som separate felter, og de medtages ikke i varens enhedsomkostninger. Når gebyrerne vises i separate felter, viser et felt det samlede gebyrbeløb, og et andet felt viser, hvilken lotstørrelse for efterkalkulationen der blev brugt til at amortisere beløbet. På siden Varepris vises f.eks. gebyrerne som to separate felter. På siden Fuldført vises dog varens samlede omkostninger pr. enhed, og de amortiserede omkostninger medtages i enhedsomkostningerne.

Gebyrerne for en produceret vare medtages altid i varens enhedsomkostning til brug i standardomkostninger. Hvis det ønskes, kan de medtages til brug i planlagte omkostninger. En politik i efterkalkulationsversionen gennemtvinger inkludering af gebyrer i en produceret vares omkostninger. Når du aktiverer en vares omkostningspost, opdaterer du gebyrerne for varens basisomkostningsoplysninger, som de vises på siden Varepris. Gebyrerne vises som to separate felter, og de medtages ikke i varens enhedsomkostning. Ved hver enkelt aktivering opdateres oplysningerne om varens basiskostpris, selvom aktiveringen afspejler forskellige lokationer. Derfor skal oplysninger om basiskostpris betragtes som referenceoplysninger.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]