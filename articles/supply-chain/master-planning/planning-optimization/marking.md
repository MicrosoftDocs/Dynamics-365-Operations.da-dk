---
title: Lagermarkering
description: Denne artikel indeholder oplysninger om de indstillinger, der er tilgængelige for at afmærke lagerbeholdningen i autoriserede ordrer.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c86db6a670d7d0f7bfe74b7466b9bce766e4a08d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740570"
---
# <a name="inventory-marking"></a>Lagermarkering

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder oplysninger om de indstillinger, der er tilgængelige for at afmærke lagerbeholdningen i autoriserede ordrer.

*Afmærkning* bruges til at sammenkæde udbud og efterspørgsel. Det ligner *udligning*, som angiver, hvordan varedisponering forventer at dække behov. Fra et planlægningssynspunkt er den væsentligste forskel, at afmærkning er mere permanent end udligning.

Der blev introduceret afmærkning for at understøtte særlige efter efterkalkulationsscenarier for FIFO (First In, First Out) og LIFO (Last In First Out). Men det bruges nu også til visse ikke-efterkalkulationsscenarier. Afmærkningen mellem udbud og efterspørgsel er valgfri og næsten permanent. Afmærkning kan fjernes manuelt af brugeren, eller den kan fjernes ved at køre en udfoldning af salgsordrelinje, hvor indstillingen **Fjern afmærkning** er valgt.

Udligning styres af varedisponeringen under disponeringen for at knytte efterspørgslen til det påkrævede udbud. Udligningen kan opdateres for hver planlægningskørsel for at optimere den forsyning, der kræves for at dække behovet. Når varedisponering opdaterer oplysninger om udligning, respekteres de eventuelle eksisterende afmærkninger.

Udligningen starter ved at inkludere relevant afmærkning, reservation af disponibelt lager og reservation ved ordreafgivelse i følgende rækkefølge:

1. Afmærkning mellem efterspørgsel og udbud
1. Reservationer af disponibelt lager
1. Reservationer ved ordreafgivelse

Når du autoriserer et ordreforslag, indeholder dialogboksen **Autorisation** feltet **Opdater afmærkning**, som du bruger til at angive afmærkningsindstillinger for de ordrer, der oprettes under autorisation. Vælg en af følgende værdier:

- *Nej* – Der anvendes ikke lagerafmærkning.
- *Standard* – Lagerafmærkning opdateres i henhold til udligningen. En behovsordre (efterspørgsel) afmærkes i forhold til en opfyldningsordre (udbud). Hvis der er et restantal på opfyldningsordren, er det ikke afmærket, og referenceoplysningerne er tomme. Hvis en salgsordre på 100 styk f.eks. udlignes mod en indkøbsordre på 150 styk, tildeles referenceoplysningerne kun til salgsordren.
- *Udvidet* – Både behovsordren (efterspørgsel) og opfyldningsordren (udbud) afmærkes, uafhængigt af om der er et restantal i opfyldningsordren. Hvis en salgsordre på 100 styk f.eks. udlignes mod en indkøbsordre på 150 styk, tildeles referenceoplysningerne både til salgsordren og indkøbsordren.
- *Enkelt niveau, standard* – Der bruges markering på enkelt niveau. Markering på enkelt niveau markerer kun hovedvaren og ikke styklistekomponenterne. Du kan derfor sikre, at komponenttildelingen for produktionsordrer er fleksibel efter autorisation. Markering på enkelt niveau giver systemet mulighed for at optimere for sidste minuts efterspørgselsændringer. Ved *standard*-markering på et enkelt niveau markeres behovsordrer i forhold til deres opfyldningsordrer, men opfyldningsordrer markeres ikke, hvis de har et restantal.
- *Enkelt niveau, udvidet* – Der bruges markering på enkelt niveau. Ved *udvidet*-markering på et enkelt niveau markeres behovsordrer i forhold til deres opfyldningsordrer, og opfyldningsordrer markeres altid, uanset om de har et restantal.

Hvis du vil angive standardmarkeringsindstillingen for systemet, skal du gå til **Varedisponering \> Konfiguration \> Varedisponeringsparametre**. Angiv derefter feltet **Opdater markering** til den foretrukne indstilling under fanen **Standardopdatering**.

> [!NOTE]
> Indstillingerne *Enkelt niveau, standard* og *Enkelt niveau, udvidet* er kun tilgængelige, hvis funktionen *Automatisering af forsyning af levering til ordre* er aktiveret i systemet. Du kan finde flere oplysninger om denne funktion, og hvordan du aktiverer den, i [Automatisering af forsyning af levering til ordre](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
