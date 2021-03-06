---
title: Oprette disponeringsindstillinger
description: Dækningsindstillinger i Microsoft Dynamics 365 Human Resources er niveauer for en deltagers valg i en frynsegodeplan eller et program.
author: andreabichsel
ms.date: 04/06/2020
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
ms.openlocfilehash: d9f67a97ec57bade840e1035c6011b94427a77c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055574"
---
# <a name="create-coverage-options"></a>Oprette disponeringsindstillinger

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dækningsindstillinger i Microsoft Dynamics 365 Human Resources er niveauer for en deltagers valg i en frynsegodeplan eller et program. Dækningsindstillinger kan f.eks. omfatte **Kun medarbejder** for en medicinsk plan eller **2 x løn** til en livsforsikring. Når den er defineret, kan du genbruge indstillingerne for frynsegodedækning. Du kan knytte en indstilling til en eller flere planer.

Når du har defineret dækningsindstillingerne, skal du knytte dækningsindstillingerne til en type af frynsegodeplan. Plantypen knyttes derefter til en frynsegodeplan eller et frynsegodeprogram. Dækningsindstillinger, der er knyttet til plantype, vil være tilgængelige for alle de planer, der oprettes med den pågældende plantype. 

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Disponeringsindstillinger** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Disponeringsindstilling** | Et entydigt navn på en disponeringsindstilling. |
   | **Beskrivelse** | En beskrivelse af disponeringsindstillingen. |
   | **Dækningskode** | Disponeringskoder tilknytter minimum- og maksimumbeløb for alle berettigede disponerede persontyper. En disponeringskode angiver, hvem der er disponeret, eller disponeringsbeløbet, der er tilladt for en plantype. Du kan udtrykke beløbet for disponering som et kronebeløb eller en procentdel. F.eks.:</br></br>- **EMP+1** – for at blive kvalificeret skal medarbejderen have valgt én afhængig (hvis der er valgt mere end én, er de ikke længere kvalificeret).</br></br>- **EMP+familie** – for at blive kvalificeret skal medarbejderen have valgt mindst to afhængige. |
   | **Maks. antal** | Maks. antal af afhængige. |
   | **Status** | Statussen for disponeringsindstillingen. Hvis status for disponeringsindstillingen er angivet til Inaktiv, kan indstillingen Disponering ikke vælges for plantyper. |
   | **Procent** | Beløb i procent. Dette felt er kun aktivt, hvis % x løn blev valgt i feltet Disponeringskode. |
   | **Nævner** | Den divisor, der skal bruges i beregningen, når du vælger disponeringskode % x løn. |
   | **Min. procentdel** | Den minimale procentdel, når du vælger Procentdisponeringskode. |
   | **Maks. procent** | Den maksimale procentdel, når du vælger Procentdisponeringskode. |

4. Under **Indstillinger for berettigelse for personlige kontakter** skal du knytte den relevante indstilling for personlig kontaktberettigelse til de enkelte disponeringsindstillinger.

5. Under **Selvbetjening** skal du angive værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Tillad medarbejderbidragsbeløb** | Angiver, om medarbejdere skal kunne redigere bidragsbeløbet via selvbetjening for frynsegoder, når de vælger frynsegoder. Hvis du markerer dette afkrydsningsfelt, beregner systemet parametre for frynsegodeplanen baseret på det bidragsbeløb, som medarbejderen indtaster i selvbetjeningstjenesten for frynsegoder. |
   | **Tillad medarbejderdækningsbeløb** | Angiver, om medarbejdere skal kunne redigere disponeringsbeløbet via selvbetjening for frynsegoder, når de vælger frynsegoder. Hvis du markerer dette afkrydsningsfelt, beregner systemet parametre for frynsegodeplanen baseret på det disponeringsbeløb, som medarbejderen indtaster i selvbetjeningstjenesten for medarbejdere. |

6. Vælg **Gem**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]