---
title: Angive færdigheder
description: Arbejdere og ledere kan indtaste færdigheder i Dynamics 365 Human Resources.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 32f08fa45c023c587d89623a12f101f50ef4a5fb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692997"
---
# <a name="enter-skills"></a>Angive færdigheder

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan angive målfærdigheder eller reelle færdigheder for arbejdere, ansøgere eller kontakter i Dynamics 365 Human Resources. En målfærdighed er en færdighed, som en person har til hensigt at opnå. En reel færdighed er en færdighed, som en person har i øjeblikket.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Oprette en arbejdsproces, der godkender færdigheder automatisk

Hvis du vil angive færdigheder uden at kræve godkendelse, skal du oprette en arbejdsproces for automatisk godkendelse af færdigheder.

> [!NOTE]
> Færdigheder, der indtastes af arbejdere, kræver altid en leders godkendelse. Denne arbejdsproces godkender kun færdigheder automatisk, hvis de er angivet af ledere på vegne af deres arbejdere.

1. Vælg **Links** i arbejdsområdet **Personalestyring**.

2. Vælg **Arbejdsgange for Human Resources** under **Konfiguration**.

3. Vælg **Ny**.

4. Vælg **Medarbejderfærdigheder** i ruden **Opret arbejdsproces**.

   [![Vælg arbejdsprocessen Medarbejderfærdigheder.](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. Vælg **Åbn** i dialogboksen **Åbn denne fil?** Indtast dine legitimationsoplysninger, når du bliver bedt om det.

6. Vælg arbejdsgangselementet **Godkend færdigheder** i arbejdsproceseditoren, og træk det til lærredet.

   [![Vælg arbejdsgangselementet Godkend færdigheder.](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Knyt elementet **Start** til elementet **Godkend færdigheder 1**, og knyt derefter elementet **Godkend færdigheder 1** til elementet **Slut**. Du skal muligvis rulle ned for at se elementet **Slut**. Du kan trække det tættere på de andre elementer.

   [![Tilknyt arbejdsgangselementer.](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Dobbeltklik på arbejdsgangselementet **Godkend færdigheder 1**, og højreklik derefter på elementet **Trin 1**. Højreklik på elementet **Trin 1**, og vælg derefter **Egenskaber**.

9. Vælg **Betingelse** på navigationslinjen til venstre i vinduet **Egenskaber**.

10. Vælg **Kør kun dette trin, når følgende betingelse er opfyldt**.

11. Vælg **Tilføj betingelse**. Vælg **Medarbejders selvbetjeningsfærdigheder** efter **Hvor**, og vælg derefter **Medarbejders selvbetjeningsfærdigheder.Person**. Efter **er** skal du vælge **felt** og derefter vælge **Relation mellem bruger og person.Person**.

    [![Angiv betingelse.](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Vælg **Tildeling** på navigationslinjen til venstre.

13. Vælg **Hierarki** under fanen **Tildelingstype**.

14. Vælg **Ledelseshierarki** i feltet **Hierarkitype:** under fanen **Valg af hierarki**.

    [![Angiv ledelseshierarki.](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Vælg **Luk**, vælg **Arbejdsproces** i brødkrummen på lærredet, og vælg derefter **Gem og luk**.

Yderligere oplysninger om oprettelse af arbejdsprocesser finder du i [Oversigt over arbejdsgangssystem](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).

## <a name="enter-skills-for-a-worker"></a>Angive færdigheder for en arbejder

1. Vælg en arbejder.

2. Vælg **Person** på handlingslinjen på siden **Arbejder**, og vælg derefter **Færdigheder**.

3. Udfyld følgende felter for hver færdighed på siden **Færdigheder**:

   - **Færdighed**: Vælg en færdighed.
   - **Niveautype**: Vælg **Faktisk** for en færdighed, som arbejderen allerede har, eller vælg **Mål** for en færdighed, som arbejderen arbejder hen imod.
   - **Niveau**: Vælg et niveau for arbejderens færdighed.
   - **Niveaudato**: Vælg en dato i kalenderværktøjet.
   - **Eksaminator**: Vælg eventuelt en eksaminator på listen. Du kan filtrere søgningen.
   - **Års erfaring**: Indtast års erfaring.
   - **Bekræftet**: Hvis færdigheden er bekræftet, skal du markere afkrydsningsfeltet.
   - **Bekræftet af**: Angiv navnet på den person, der har bekræftet.

4. Når du er færdig med at indtaste færdigheder, skal du vælge **Gem**.

## <a name="see-also"></a>Se også

[Konfigurere færdigheder](hr-develop-skills.md)<br>
[Tilknytte færdigheder](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
