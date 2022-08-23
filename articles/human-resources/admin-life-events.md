---
title: Angive administratorrettigheder for livshændelser
description: Denne artikel forklarer, hvordan du kan konfigurere administratorrettigheder for livshændelser i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229891"
---
# <a name="set-administrator-rights-for-life-events"></a>Angive administratorrettigheder for livshændelser

[!include [banner](../includes/preview-banner.md)]

Administratorer kan opdatere indstillinger for livshændelser afhængigt af konfigurationsindstillingerne. På siden **Parametre for Human Resource** kan du konfigurere parametre, der giver administratorer mulighed for at foretage ændringer i planvalg. Du kan også begrænse administratorer fuldt ud i at foretage ændringer.

På siden **Parametre for Human Resource** kan du konfigurere begrænsninger for ændringer af bekræftede planer og indstillinger for livshændelser.

Hvis indstillingen **Bekræftede planer** er valgt, kan der kun foretages ændringer, hvis en tilmeldingsperiode er aktiv. (Eksempler på tilmeldingsperioder omfatter åbne tilmeldingsperioder, tilmeldingsperioder for nyansættelse og tilmeldingsperioder for livshændelser). Hvis denne indstilling ikke er valgt, kan der altid foretages ændringer.

Hvis **Indstillinger for livshændelse** er valgt, begrænses planændringerne i en livshændelse af de indstillinger for livshændelser, der er defineret for plantypen. Hvis denne indstilling ikke er valgt, kan planvalg ændres under en livshændelse.

## <a name="set-plan-change-restrictions"></a>Angive begrænsninger for planændring

På siden **Parametre for Human Resources** under fanen **Personalegodeadministration** er følgende felter tilgængelige.

| Felt | Beskrivende tekst |
|-------|-------------|
| Bekræftede planer | Vælg denne indstilling, hvis ændringer i en plan kun er tilladt, hvis en tilmeldingsperiode er aktiv. Hvis denne indstilling ikke er valgt, kan der altid foretages ændringer. |
| Indstillinger for livshændelse | Vælg denne indstilling, hvis planændringer begrænses i en livshændelse af de indstillinger for livshændelser, der er defineret for plantypen. Hvis denne indstilling ikke er valgt, kan planvalg ændres under en livshændelse. |
