---
title: Oprette en indkøbsordre, der er underlagt budgettet
description: Brug denne procedure, når du vil oprette en indkøbsordre, der skal kontrolleres for disponibelt budget.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016182"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Oprette en indkøbsordre, der er underlagt budgettet

[!include [banner](../../includes/banner.md)]

Brug denne procedure, når du vil oprette en indkøbsordre, der skal kontrolleres for disponibelt budget.

## <a name="review-the-budget-control-configuration"></a>Gennemse konfigurationen for budgetstyring

1. Gå til **Budgettering > Opsætning > Budgetstyring > Konfiguration af budgetstyring**.
1. Væl fanen **Tilgængelige budgetmidler**.
1. Vælg fanen **Dokumenter og journaler**.
1. Vælg fanen **Definer budgetstyringsregler**.
1. Vælg fanen **Definer budgetgrupper**.
1. Luk siden.

## <a name="create-a-purchase-order"></a>Oprette en indkøbsordre

1. Gå til **Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer**.
1. Vælg **Ny**.
1. Indtast eller vælg en værdi i feltet **Kreditorkonto**.
1. Udvid oversigtspanelet **Generelt**.
1. Indstil datoen i feltet **Regnskabsdato**.
1. Vælg **OK** for at lukke dialogboksen og åbne den nye indkøbsordre.
1. I oversigtspanelet **Indkøbsordrelinjer** skal du vælge **Tilføj linje** på værktøjslinjen for at tilføje en ny linje og derefter udfylde linjen efter behov for at føje en vare til ordren.
1. I oversigtspanelet **Indkøbsordrelinjer** skal du vælge **Finans \> Fordel beløb**.
1. I feltet **Finanskonto** skal du angive en konto.
1. Luk siden.

## <a name="perform-budget-checking"></a>Udfør budgetkontrol

1. Fortsæt med at arbejde med den indkøbsordre, du netop har føjet en linje til.
1. I oversigtspanelet **Indkøbsordrelinjer** skal du vælge **Finans \> Udfør budgetkontrol**.
1. I oversigtspanelet **Indkøbsordrelinjer** skal du vælge **Finans \> Fejl eller advarsler i forbindelse med budgetkontrol**.
1. Dialogboksen **Fejl eller advarsler i forbindelse med budgetkontrol** åbnes. Kontrollér resultatet af kontrollen, og vælg derefter **Luk** for at lukke dialogboksen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]