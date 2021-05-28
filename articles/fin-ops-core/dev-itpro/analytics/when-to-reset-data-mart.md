---
title: Hvornår et datacenter skal nulstilles
description: I dette emne kan du se de forhold, der kan blive forbedret, hvis du nulstiller et datacenter, og forhold, hvor nulstilling af datacenteret sandsynligvis ikke hjælper.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988986"
---
# <a name="when-to-reset-a-data-mart"></a>Hvornår et datacenter skal nulstilles

Nulstilling af et datacenter kan være tidskrævende. Afhængigt af forholdene er denne handling muligvis ikke den løsning, der er brug for. I dette emne kan du se de forhold, der kan blive forbedret, hvis du nulstiller et datacenter, samt forhold, hvor nulstilling af datacenteret sandsynligvis ikke hjælper.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Hvornår skal jeg nulstille et datacenter?
Overvej følgende spørgsmål, før du nulstiller et datacenter. Hvis du svarer ja til et eller flere spørgsmål, kan det være en fordel for din organisation at nulstille datacenteret.

- Blev programdatabasen gendannet?
- Hvis du har åbnet en supporthændelse, som en supporttekniker har givet dig besked på at nulstille datacenteret som en del af et fejlfindingstrin?
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Hvornår er det ikke relevant at nulstille et datacenter?
Der er nogle forhold, hvor vi ikke anbefaler, at du nulstiller et datacenter. Blandt andet: 

- Du oplever forskellige performance-problemer, der er forbundet med datasynkronisering. 
- Hvis oplever har et tilbagevendende nulstillingsmønster af en af følgende årsager: 
  - **Manglende data** 
  - **Låst integrationstilstand** 
  - **Gamle poster** – Gamle poster i sig selv berettiger ikke nødvendigvis en nulstilling af datacenteret. Hvis du har et stort datasæt, tager det et stykke tid at køre nulstillingsprocessen, men der sker sandsynligvis ingen forbedring.
 
## <a name="what-is-a-data-mart-reset"></a>Hvad er nulstilling af et datacenter?
- En nulstilling starter kun, når eksisterende opgaver er fuldført. Derved sikres, at gamle data ikke indsættes. På dette tidspunkt vil du muligvis få vist en meddelelse som f.eks. "Nulstillingen af datacenteret kunne ikke behandles på grund af en aktiv opgave. Prøv igen senere."
- Nulstillingen deaktiverer integrationsopgaverne og sletter alle data i datacenteret. Integrationen er aktiveret igen.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Hvis jeg nulstiller datacenteret, mister jeg så rapporter, som jeg allerede har udarbejdet? 
Nej, rapporterne gemmes i SQL-tabeller, der ikke påvirkes af, at dataene nulstilles. Hvis du er bange for at miste rapporter, du har oprettet, kan du sikkerhedskopiere de design, du ikke ønsker at miste. Du kan sikkerhedskopier dem ved at åbne Report Designer og gå til **Firma > Firmaer > Komponenter > Eksporter**.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Er det nødvendigt, at alle brugere forlader systemet, når dataene skal nulstilles?
Nej, brugere kan fortsætte med at arbejde i systemet, når data nulstilles. De vil dog ikke kunne få adgang til rapporter, der er oprettet med Financial Reporter, før nulstillingen er fuldført. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
