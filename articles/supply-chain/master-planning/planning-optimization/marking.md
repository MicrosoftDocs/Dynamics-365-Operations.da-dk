---
title: Lagerafmærkning med planlægningsoptimering
description: Dette emne indeholder oplysninger om de indstillinger, der er tilgængelige for at afmærke lagerbeholdningen i autoriserede ordrer, når du bruger Planlægningsoptimering.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7813f570afb0260e6740507c9504320c3e87be93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263344"
---
# <a name="inventory-marking-with-planning-optimization"></a>Lagerafmærkning med planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Dette emne indeholder oplysninger om de indstillinger, der er tilgængelige for at afmærke lagerbeholdningen i autoriserede ordrer, når du bruger Planlægningsoptimering.

*Afmærkning* bruges til at sammenkæde udbud og efterspørgsel. Det ligner *udligning*, som angiver, hvordan varedisponering forventer at dække behov. Fra et planlægningssynspunkt er den væsentligste forskel, at afmærkning er mere permanent end udligning.

Der blev introduceret afmærkning for at understøtte særlige efter efterkalkulationsscenarier for FIFO (First In, First Out) og LIFO (Last In First Out). Men det bruges nu også til visse ikke-efterkalkulationsscenarier. Afmærkningen mellem udbud og efterspørgsel er valgfri og næsten permanent. Afmærkning kan fjernes manuelt af brugeren, eller den kan fjernes ved at køre en udfoldning af salgsordrelinje, hvor indstillingen **Fjern afmærkning** er valgt.

Udligning styres af varedisponeringen under disponeringen for at knytte efterspørgslen til det påkrævede udbud. Udligningen kan opdateres for hver planlægningskørsel for at optimere den forsyning, der kræves for at dække behovet. Når varedisponering opdaterer oplysninger om udligning, respekteres de eventuelle eksisterende afmærkninger.

Udligningen starter ved at inkludere relevant afmærkning, reservation af disponibelt lager og reservation ved ordreafgivelse i følgende rækkefølge:

1. Afmærkning mellem efterspørgsel og udbud
1. Reservationer af disponibelt lager
1. Reservationer ved ordreafgivelse

Når du autoriserer et ordreforslag, indeholder dialogboksen **Autorisation** feltet **Opdater afmærkning**, som du bruger til at angive afmærkningsindstillinger for de ordrer, der oprettes under autorisation. Vælg en af følgende værdier:

- **Nej** – Der anvendes ikke lagerafmærkning.
- **Standard** – Lagerafmærkning opdateres i henhold til udligningen. En behovsordre (efterspørgsel) afmærkes i forhold til en opfyldningsordre (udbud). Hvis der er et restantal på opfyldningsordren, er det ikke afmærket, og referenceoplysningerne er tomme. Hvis en salgsordre på 100 styk f.eks. udlignes mod en indkøbsordre på 150 styk, tildeles referenceoplysningerne kun til salgsordren.
- **Udvidet** – Både behovsordren (efterspørgsel) og opfyldningsordren (udbud) afmærkes, uafhængigt af om der er et restantal i opfyldningsordren. Hvis en salgsordre på 100 styk f.eks. udlignes mod en indkøbsordre på 150 styk, tildeles referenceoplysningerne både til salgsordren og indkøbsordren.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]