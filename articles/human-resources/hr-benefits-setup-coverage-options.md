---
title: Oprette dækningsindstillinger
description: Dækningsindstillinger i Microsoft Dynamics 365 Human Resources er niveauer for en deltagers valg i en frynsegodeplan eller et program.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e8f13075a9835963c231a8e4e8a737368a952ba
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558219"
---
# <a name="create-coverage-options"></a>Oprette dækningsindstillinger

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dækningsindstillinger bestemmer, hvem der er dækket, eller hvor meget dækning der er til rådighed i en forsikringsplan. I forbindelse med en sundhedsplan kan du f.eks. vælge en indstilling for **kun medarbejder**, **medarbejder +1** og **familie**. Med hensyn til livsforsikring kan du tilbyde dækning for **1 x løn** eller **2 x løn**.

Når du har defineret indstillingerne for frynsegodedækning, kan de genbruges. Du kan knytte en indstilling til en eller flere planer.

> [!IMPORTANT]
> Når du har defineret dækningsindstillingerne, skal du knytte dem til en type af frynsegodeplan. Plantypen knyttes derefter til en frynsegodeplan eller et frynsegodeprogram. Dækningsindstillinger, der er knyttet til plantype, vil være tilgængelige for alle planer af denne type, som bliver oprettet.

## <a name="create-coverage-options"></a>Oprette dækningsindstillinger
1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Dækningsindstillinger** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Dækningsindstilling** | Et entydigt navn på en dækningsindstilling. |
   | **Beskrivelse** | En beskrivelse af dækningsindstillingen. |
   | **Dækningskode** | Dækningskoder tilknytter minimum- og maksimumbeløb for alle berettigede dækkede persontyper. En dækningskode angiver, hvem der er dækket, eller dækningsbeløbet, der er tilladt for en plantype. Du kan udtrykke dækningsbeløbet som et kronebeløb eller en procentdel. F.eks.:<ul><li>**Medarbejder+1** – for at blive kvalificeret skal medarbejderen have valgt én afhængig (hvis der er valgt mere end én, er de ikke længere kvalificerede).</li><li>**Medarbejder+familie** – for at blive kvalificeret skal medarbejderen have valgt mindst to afhængige.</li></ul> |
   | **Maks. antal** | Maks. antal af afhængige. |
   | **Status** | Statussen for dækningsindstillingen. Hvis status for dækningsindstillingen er angivet til Inaktiv, kan indstillingen Dækning ikke vælges for plantyper. |
   | **Procent** | Beløb i procent. Dette felt er kun aktivt, hvis % x løn blev valgt i feltet Dækningskode. |
   | **Nævner** | Den divisor, der skal bruges i beregningen, når du vælger dækningskode % x løn. |
   | **Min. procentdel** | Den minimale procentdel, når du vælger dækningskoden Procent. |
   | **Maks. procent** | Den maksimale procentdel, når du vælger dækningskoden Procent. |

4. Under **Indstillinger for berettigelse for personlige kontakter** skal du knytte den relevante indstilling for personlig kontaktberettigelse til de enkelte dækningsindstillinger.

5. Under **Selvbetjening** skal du angive værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Tillad medarbejderbidragsbeløb** | Angiver, om medarbejdere skal kunne redigere bidragsbeløbet via selvbetjening for frynsegoder, når de vælger frynsegoder. Hvis du markerer dette afkrydsningsfelt, beregner systemet parametre for frynsegodeplanen baseret på det bidragsbeløb, som medarbejderen indtaster i selvbetjeningstjenesten for frynsegoder. |
   | **Tillad medarbejderdækningsbeløb** | Angiver, om medarbejdere skal kunne redigere dækningsbeløbet via selvbetjening for frynsegoder, når de vælger frynsegoder. Hvis du markerer dette afkrydsningsfelt, beregner systemet parametre for frynsegodeplanen baseret på det dækningsbeløb, som medarbejderen indtaster i selvbetjeningstjenesten for medarbejdere. |

6. Vælg **Gem**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
