---
title: Konfigurere færdigheder
description: Du kan spore arbejderens færdigheder i Dynamics 365 Human Resources. Du kan også angive de færdigheder, der kræves til et bestemt job.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076553"
---
# <a name="configure-skills"></a>Konfigurere færdigheder

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan spore arbejderens færdigheder i Dynamics 365 Human Resources. Du kan også angive de færdigheder, der kræves til et bestemt job.

Eksempler på færdigheder, du kan spore, omfatter:

- Supervision – evnen til at føre tilsyn med andres arbejde.
- Ledelse – evnen til at lede medarbejdere og forretningsområder.
- Planlægning – evnen til at se fremad, formulere visioner og få dem gennemført.
- HTML – evnen til at skrive HTML-kode.

Hvis du ikke allerede har konfigureret færdighedstyper og klassifikationsmodeller, skal du tilføje nogle, før du opretter færdigheder.

Følgende personer kan angive færdigheder for en arbejder:

- Arbejdere kan indtaste færdigheder for sig selv i medarbejderselvbetjening. Disse færdigheder kræver en leders godkendelse.
- Ledere kan indtaste færdigheder for deres arbejdere. Du kan oprette en arbejdsproces, der automatisk godkender disse færdigheder.

## <a name="create-a-skill-type"></a>Oprette en færdighedstype

Færdighedstyper er kategorier, som individuelle færdigheder hører under, f.eks. Administration eller Salg.

1. I arbejdsområdet **Medarbejderudvikling** skal du vælge **Links**.

2. Vælg **Kompetencetyper** under **Kompetenceopsætning**.

3. Vælg **Ny**.

4. Udfyld følgende felter:

   - **Færdighedstype**: Angiv et navn til færdighedstypen.
   - **Beskrivelse**: Angiv en beskrivelse af færdighedstypen.

5. Vælg **Gem**.

## <a name="create-a-rating-model"></a>Oprette en rangeringsmodel

Rangeringsmodeller er en hjælp til at evaluere en persons faktiske færdighedsniveau, det niveau de skal tilsigte, eller det færdighedsniveau, der kræves til et job. Hvert niveau i en klassifikationsmodel er tildelt en faktor.

1. I arbejdsområdet **Medarbejderudvikling** skal du vælge **Links**.

2. Vælg **Rangeringsmodeller** under **Opsætning af kompetence**.

3. Vælg **Ny**.

4. Udfyld følgende felter:

   - **Rangering**: Angiv et navn til rangeringsmodellen, **Færdigheder**.
   - **Beskrivelse**: Angiv en beskrivelse af rangeringsmodellen, f.eks. **Færdighedsrangering**.

5. Vælg **Ny** i sektionen **Niveauer**. For hvert niveau, du vil tilføje, skal du udfylde følgende felter:

   - **Niveau**: Angiv et navn til niveauet.
   - **Beskrivelse**: Angiv en beskrivelse af niveauet.
   - **Faktor**: Angiv en faktorværdi fra 0-9. Faktorer hjælper med at normalisere resultaterne af færdigheder, der bruger forskellige rangeringsmodeller. Hvert niveau skal have en entydig faktor. Niveauer med højere faktorværdier vægter mere i rangeringsmodellen.

   Fortsæt med at tilføje niveauer efter behov. Du kan angive op til ti niveauer for hver rangeringsmodel.

6. Vælg **Gem**.

## <a name="create-a-skill"></a>Oprette en færdighed

Før du kan tildele en færdighed eller oprette en færdighedssøgning eller en færdighedsprofil, skal du angive oplysninger om færdighederne på siden **Færdigheder**. Du kan vælge en færdighedstype og en rangeringsmodel for hver færdighed.

1. I arbejdsområdet **Medarbejderudvikling** skal du vælge **Links**.

2. Vælg **Færdigheder** under **Kompetenceopsætning**.

3. Vælg **Ny**.

4. Udfyld følgende felter:

   - **Færdighed**: Angiv et navn til færdigheden.
   - **Beskrivelse**: Angiv en beskrivelse af færdigheden.
   - **Rangering**: Vælg den rangeringsmodel, som du vil bruge til denne færdighed.
   - **Færdighedstype** : Vælg på listen over færdighedstyper.

5. Vælg **Gem**.

## <a name="see-also"></a>Se også

[Angive færdigheder](hr-develop-enter-skills.md)<br>
[Tilknytte færdigheder](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]