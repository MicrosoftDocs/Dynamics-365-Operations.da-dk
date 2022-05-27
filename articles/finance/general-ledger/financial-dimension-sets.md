---
title: Økonomiske dimensionsopsætninger
description: I dette emne beskrives økonomiske dimensionsopsætninger, og du kan få tip til optimering af deres brug.
author: yukonpeegs
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: c583a2a89b45b59ea76ffd8e38b6206c9ca9ed41
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722570"
---
# <a name="financial-dimension-sets"></a>Økonomiske dimensionsopsætninger

[!include [banner](../includes/banner.md)]

I dette emne beskrives økonomiske dimensionsopsætninger, og du kan få tip til optimering af deres brug.

En dimensionsopsætning er en ordnet liste over økonomiske dimensioner, der kan bruges til at opsummere finansdata på en brugerdefineret måde. Dimensionssæt bruges primært til at definere en råbalance.

Den eneste standarddimensionsopsætning er den dimensionsopsætning, der kun indeholder hovedkontoen.

Du kan bruge siden **Økonomiske dimensionsopsætninger** til at oprette og administrere økonomiske dimensionsopsætninger.

## <a name="dimension-set-balances"></a>Saldi for dimensionsopsætninger

En dimensionsopsætning kan have saldi, der er baseret på dens økonomiske dimensioner. Saldi findes i Finans og er baseret på definitionen af dimensionsopsætning. Saldi opsummeres ud fra finansdataene for at forbedre ydeevnen, når de hentes (f.eks. når der genereres en råbalance).

## <a name="create-balances"></a>Oprette saldi

Brug knappen **Opret saldi** til at initialisere saldi for en dimensionsopsætning, der ikke aktuelt har saldi.

> [!NOTE]
> Det anbefales, at du begrænser antallet af dimensionsopsætninger, der har saldi, da saldoopdateringer påvirker alle finanskonteringsaktiviteter.

## <a name="update-balances"></a>Opdatere saldi

Brug knappen **Opdater saldi** til at medtage den seneste finanskonteringsaktivitet i saldi. Saldoopdateringer er lette operationer. De skal kun behandle den finanskonteringsaktivitet, der er opstået efter den seneste opdatering.

> [!NOTE]
> Visningen af råbalancen fremtvinger en opdatering for at sikre, at de viste saldi er aktuelle. Overvej at bruge et tilbagevendende batchjob, så opdateringer af de ofte anvendte dimensionsopsætninger sker hurtigt. På den måde er du med til at minimere den tid, som brugere af råbalance skal vente.

## <a name="rebuild-balances"></a>Gendanne saldi

Du kan bruge knappen **Gendan saldi** til at gendanne saldi fra bunden. På denne måde er du med til at sikre, at de svarer til dataene i Finans. En gendannelse af saldi kræver masser af behandling og bør normalt ikke være påkrævet.

> [!NOTE]
> Hvis du har et scenario, der jævnligt kræver en gendannelse af saldi, anbefales det, at du kontakter kundesupport. Kundesupport kan hjælpe dig med at finde ud af, hvorfor saldi ikke stemmer overens med dataene i Finans.

## <a name="clear-balances"></a>Afstemme saldi

Brug knappen **Afstem saldi** til at fjerne saldi og stoppe eventuelle yderligere opdateringer. Dimensionsopsætningen har ikke længere indflydelse på bogføringsaktiviteterne i Finans.

## <a name="delete-a-dimension-set"></a>Slette en dimensionsgruppe

Du må ikke **slette og genoprette** dimensionssæt som nogen form for løsning af potentielle problemer med saldodataene for et bestemt dimensionssæt. Det er dyrt at genoprette et dimensionssæt. Kontakt kundesupport, hvis du ønsker yderligere hjælp til problemer. 


Du kan finde flere oplysninger under [Økonomiske dimensioner](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
