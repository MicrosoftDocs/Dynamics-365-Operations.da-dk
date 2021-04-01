---
title: Aktivere forsinket momsberegning på kladder
description: I dette emne forklares det, hvordan du kan bruge funktionen Forsinket momsberegning til at forbedre ydeevnen af momsberegninger, når antallet af kladdelinjer er meget stort.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d842b60b3cca8c29b281ab4a6a1b6c3b0bad3684
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236716"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Aktivere forsinket momsberegning på kladder
[!include [banner](../includes/banner.md)]


Dette emne forklarer, hvordan du kan forsinke momsberegningen på kladder. Denne facilitet hjælper med at forbedre ydeevnen af momsberegninger, når der er mange kladdelinjer.

Momsbeløb på kladdelinjer beregnes som standard, når momsrelaterede felter opdateres. Disse felter omfatter felterne til momsgrupper og varemomsgrupper. Enhver opdatering af en kladdelinje medfører, at momsbeløb genberegnes for alle kladdelinjer. Selvom denne funktionsmåde hjælper brugeren med at se momsbeløb beregnet i realtid, kan det også påvirke ydeevnen, hvis antallet af kladdelinjer er meget stort.

Med funktionen til forsinket beregning af moms kan du forsinke momsberegningen på kladder og dermed løse problemer med ydeevnen. Hvis denne funktion er slået til, vil momsbeløb kun blive beregnet, når brugeren vælger **Moms** eller bogfører kladden.

Du kan forsinke beregningen af moms på tre niveauer:

- Juridisk enhed
- Kladdenavn
- Kladdehoved

Systemet giver prioriteten til indstillingen for kladdehovedet. Denne indstilling hentes som standard fra kladdenavnet. Indstillingen for kladdenavnet hentes som standard fra indstillingen på siden **Finansparametre**, når kladdenavnet oprettes. I følgende afsnit forklares det, hvordan du aktiverer forsinket momsberegning for juridiske enheder, kladdenavne og kladdehoveder.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Aktivere forsinket momsberegning på juridisk enhedsniveau

1. Gå til **Finans \> Opsætning Finans \> Finansparametre**.
2. Under fanen **Moms** i oversigtspanelet **Generelt** skal du vælge **Ja** i indstillingen **Forsinket momsberegning**.

![Billede af finansparametre](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Aktivere forsinket momsberegning på kladdenavnsniveau

1. Gå til **Finans \> Kladdeopsætning \> Kladdenavne**.
2. I sektionen **Moms** i oversigtspanelet **Generelt** skal du vælge **Ja** i indstillingen **Forsinket momsberegning**.

![Billede af kladdenavne](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Aktivere forsinket momsberegning på kladdehovedniveau

1. Gå til **Finans \> Kladdeposteringer \> Finanskladder**.
2. Vælg **Ny**.
3. Vælg et kladdenavn.
4. Under fanen **Opsætning** skal du angive indstillingen **Forsinket momsberegning** til **Ja**.

![Billede af siden Finanskladde](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]