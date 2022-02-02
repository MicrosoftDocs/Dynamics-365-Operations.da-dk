---
title: Tilføje typer af betalingsbeløb
description: Dette emne beskriver, hvordan du konfigurerer typer af betalingsbeløb i Aktivleasing.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 037afa458277a3a07bcb937c6ec4d961d0dd5ca9
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968318"
---
# <a name="add-payment-amount-types"></a>Tilføje typer af betalingsbeløb

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer typer af betalingsbeløb i Aktivleasing. På denne måde kan du specificere leasingbetalingsbeløb i stedet for at lægge engangsbeløbet til på betalingsplanlinjerne.

Følg disse trin for at tilføje typer af betalingsbeløb.

1. Gå til **Aktivleasing \> Konfiguration \> Typer af betalingsbeløb**.
2. Vælg **Ny**.
3. Angiv den nye betalingstype og en beskrivelse.

> [!NOTE]
> I forbindelse med værdiregulering af IFRS 16-indeks skal du oprette én betalingsbeløbstype og markere den som **Brugt til værdiregulering af IRPF 16-indeks**. Denne betalingsbeløbstype bruges, når processen til værdiregulering af indeks foretages i forhold til IFRS 16-kartotek, og den vil overveje de ændringer, der er sket på grund af processen til værdiregulering af indeks.
>
> Når indstillingen af **Opdeling af betalinger** i lejen er angivet til **Ja**, og værdireguleringen af IFRS 16-indeks køres, men der ikke er nogen betalingstype for IFRS 16, fuldføres processen ikke.

Der kan kun markeres én post som **Bruges til værdiregulering af IFRS16-indeks**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
