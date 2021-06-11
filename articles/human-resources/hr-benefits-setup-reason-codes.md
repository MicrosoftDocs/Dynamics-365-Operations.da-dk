---
title: Definer årsagskoder
description: Dynamics 365 Human Resources bruger årsagskoder til at forklare, hvorfor en medarbejders frynsegoder ændres.
author: andreabichsel
ms.date: 01/25/2021
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
ms.openlocfilehash: 6fc641233a1bd217de5b9eb6e06560b989f91c7b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056342"
---
# <a name="set-up-reason-codes"></a>Definer årsagskoder

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources bruger årsagskoder til at forklare, hvorfor en medarbejders frynsegoder ændres.

> [!NOTE]
> Pr. januar 2021 overføres årsagskoder til arbejdsområdet **Personalestyring** i stedet for arbejdsområdet **Frynsegodeadministration**. Der er flere oplysninger i [Manuel overførsel af årsagskoder til Personalestyring](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Oprette årsagskoder

1. I arbejdsområdet **Personalestyring** (eller arbejdsområdet **Frynsegodeadministration**, hvis dine årsagskoder endnu ikke er overflyttet), skal du vælge **Links** og derefter vælge **Årsagskoder**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Årsagskode** | Et entydigt navn, der identificerer årsagen til, at en medarbejder vil ændre tilmeldingen til en frynsegodeplan. |
   | **Beskrivelse** | En beskrivelse af årsagskoden. |

4. Indstil **Frynsegodeadministration** under **Anvendelige scenarier** til **Ja**. (Kan ikke anvendes, hvis årsagskoderne endnu ikke er overflyttet til arbejdsområdet **Personalestyring**.)

5. Vælg **Gem**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Manuelt overføre årsagskoder til Personalestyring

I januar 2021 overføres årsagskoder til arbejdsområdet **Personalestyring** i stedet for arbejdsområdet **Frynsegodeadministration**. De fleste årsagskodedata overføres automatisk i dit miljø. Nogle årsagskodedata kan ikke overføres. Årsagskoder har f.eks. nu et maksimum på 15 tegn, så enhver årsagskode, der er længere end 15 tegn, overføres ikke automatisk.

Du får vist et banner på siden **Links** i arbejdsområdet til **Frynsegodeadministration**, der oplyser dig om overflytningen, og om årsagskoder ikke er blevet overflyttet.

1. Vælg **Årsagskoder** for oplysninger om overførselsstatus.

   [![Årsagskoder](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Vælg en årsagskode, der ikke kunne overføres.

   [![Status for overførsel af årsagskode](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Vælg **Overfør årsagskode**.

   [![Overfør årsagskode](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. I ruden **Overflytning af frynsegodeadministration** har du to muligheder for tilknytning til en årsagskode for personalestyring:

   - Hvis du vil bruge en eksisterende årsagskode i Personalestyring, skal du vælge en fra rullelisten **Brug eksisterende årsagskode**.
     > [!NOTE]
     > Du kan kun bruge en eksisterende årsagskode i Personalestyring, hvis en anden årsagskode for goder ikke allerede er overflyttet til den.
   - Hvis du vil oprette en ny årsagskode i Personalestyring, skal du angive en ny i **Ny årsagskode** og derefter angive en beskrivelse i **Ny beskrivelse**.

   [![Tilknytte en årsagskode for personalestyring](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Når årsagskoder er overført til Personalestyring, angives indstillingen for brug af dem i Styring af goder automatisk til **Ja**.

[![Bruge årsagskoder i administration af frynsegoder](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]