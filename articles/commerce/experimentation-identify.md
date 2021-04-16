---
title: Identificere en hypotese og fastslå målepunkter for et eksperiment
description: Dette emne indeholder en beskrivelse af, hvordan du kan identificere hypoteser og succesmålepunkter for et eksperiment, du kører på et e-handelswebsted i Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: a3f5d44e008e4092557d75c8f5d830d5ae36a091
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799035"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Identificere en hypotese og fastslå succesmålepunkter for et eksperiment
Den første fase i eksperiments livscyklus omfatter identifikation af hypotesen til eksperimentet og bestemmelse af, hvilke målepunkter du vil spore for at evaluere succesen. I følgende diagram vises alle de trin, der er nødvendige for at [konfigurere og køre et eksperiment](experimentation-overview.md) på et e-handelswebsted i Dynamics 365 Commerce. Yderligere trin behandles i separate emner. 

[ ![Eksperimenteringens brugerrejse - identifikation](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

En hypotese er et udsagn, hvor du forudsiger resultatet af eksperimentet. Mange faktorer går ud på at definere en hypotese, f.eks. research om brugeradfærd og webstedsdata, du har indsamlet. Med hypotesen kan du definere den antagelse eller teori, du vil validere med dit eksperiment. Et eksempel på en hypotese til dit eksperiment kan være "*et billede af en hvid t-shirt på min startside vil skabe mere trafik end en sweater i sommermånederne, da folk vil være let påklædt i lyse farver om sommeren*". I dette tilfælde skal du oprette variationer, der omfatter en hvid t-shirt og en sweater, og publicere begge dele på samme tid.

Hvis du vil validere en hypotese, skal det vellykkede eller mislykkede eksperiment være direkte knyttet til brugerhandlinger. Hvis webstedets bruger f.eks. klikker på et link eller en knap. Disse handlinger skal svare til hændelser, der rapporteres til en tredjepartstjenestes sporing af eksperimentet. Over tid vil den procentdel af brugerne, der udfører handlingen, blive talt som en metrikværdi, som du kan bruge til at generere rapporter og foretage analyser. Du kan se alle de tilgængelige hændelser og attributter under [Commerce-komponenthændelser for diagnosticering og fejlfinding](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).

## <a name="previous-step"></a>Forrige trin
[Eksperimenteren i Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>Næste trin
[Opsætning af et eksperiment](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]