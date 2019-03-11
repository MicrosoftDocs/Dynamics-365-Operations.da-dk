---
title: Nyheder eller ændringer i Dynamics 365 for Talent Core HR (1. oktober 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97820cd25ece48dc0b8045d9ba509d0971ca5aad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303711"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a>Nyheder eller ændringer i Dynamics 365 for Talent Core HR (1. oktober 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.1035.0**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.

## <a name="turn-off-electronic-payment-validation"></a>Slå validering af elektroniske betalinger fra

Validering af elektroniske betalingsoplysninger foretages, hvis du konfigurerer udbetalinger til direkte indbetaling enten via **Medarbejderselvbetjening**-arbejdsområdet (ESS) eller direkte i medarbejderformen. Denne indstilling giver dig mulighed for at fjerne denne validering, hvis du ikke har brug valideringskontrol af beløb og resterende værdier. Denne funktion er nyttig, hvis du integrerer med et eksternt lønsystem, der har andre krav.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Selvbetjening for leder - Tilføj mål for teammedlemmer via feltet Mål for teamperformance

Før denne version kan ledere føje mål til deres medarbejdere individuelt via performancemål, der er knyttet til hver medarbejder. Med denne opdatering kan ledere få adgang til feltet **Mål for teamperformance** og oprette nye mål ved at vælge en af deres direkte underordnede.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Selvbetjening for leder - Tilføj evalueringer for teammedlemmer via feltet Evalueringer af teamperformance

Før denne version kan ledere føje evalueringer til deres medarbejdere individuelt via de evalueringer, der er knyttet til hver medarbejder. Med denne opdatering kan ledere få adgang til feltet **Evalueringer af teamperformance** og oprette nye evalueringer ved at vælge en af deres direkte underordnede.

## <a name="configure-proration-options-by-leave-plan"></a>Konfigurer indstillinger for proportionalitet efter orlovsplan

Organisationer beregner fravær forskelligt afhængigt af, hvornår medarbejdere starter i eller forlader firmaet. For visse organisationer får medarbejderne fuld tildeling på deres startdato, mens andre beregner bonus forholdsmæssigt. Der findes nye indstillinger i denne version, så du kan vælge, hvordan forholdsmæssig bonus og periodisering beregnes for nytilkomne og afgående personer i en organisation. Indstillingerne omfatter: Beregnet forholdsmæssigt, Fuld periodisering og Ingen periodisering.

## <a name="other-changes"></a>Andre ændringer

-   Medarbejderenhed opdateret – Titlen **Personligt** kan nu opdateres ved hjælp af Excel-tilføjelsesprogram/datastyring.

-   Sikkerhedsændring, der tillader fjernelse af knapperne **Slet** og **Deaktiver** i medarbejderselvbetjeningens betalingsoplysninger.

## <a name="known-issue"></a>Kendt problem

-   **Problem:** Når du føjer en ny vedhæftet fil til en arbejder, bliver **Ny**- og **Rediger**-knapperne nedtonede. **Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukkede. Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil **Vedhæftede filer**-knapperne blive aktiveret. (Dette problem vil blive løst i den næste platformsopdatering).
