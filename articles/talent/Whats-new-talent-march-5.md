---
title: Nyheder eller ændringer i Dynamics 365 for Talent (5. marts 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fe24846ab98a75d474df045a62a72bfc41c64866
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741884"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a>Nyheder eller ændringer i Dynamics 365 for Talent (5. marts 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Talent

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="extending-option-sets-in-attract"></a>Udvide grupperede indstillinger i Attract

I Attract er der adskillige felter, som er grupperede indstillinger, i Common Data Service. Der er indført nye funktioner til udvidelse af grupperede indstillinger, startende med felterne **Årsag til afvisning**, **Medarbejdertype** og **Anciennitetstype**.

> [!IMPORTANT]
> Funktionen til jobopslag på LinkedIn kræver brug af felterne **Medarbejdertype** og **Anciennitetstype** på siden **Jobdetaljer**. Standardværdierne i disse felter understøttes af LinkedIn og vises, når jobbet er opslået. Hvis du laver jobopslag på LinkedIn, og du ændrer de eksisterende værdier for disse felter med grupperede indstillinger, bliver jobbet opslået, men LinkedIn viser ikke de brugerdefinerede værdier i **Medarbejdertype** og **Anciennitetstype**.

## <a name="changes-in-onboarding"></a>Ændringer i Onboarding

### <a name="private-preview-for-onboard-teams"></a>Privat prøveversion til Onboard-teams
Du kan nu nemt dele og samarbejde om skabeloner på tværs af hele organisationen. Yderligere oplysninger finder du i [Dele de bedste fremgangsmåder på tværs af organisationen ved hjælp af Onboard-teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).

### <a name="private-preview-for-assignee-placeholders"></a>Privat prøveversion med pladsholdere for modtagere
Du kan forbedre dine skabeloner ved at tildele aktiviteter til roller i stedet for personer. Roller tildeles derefter til personer på tidspunktet for oprettelse af guiden. Yderligere oplysninger finder du i [Strømline guideadministration ved at tildele aktiviteter til roller](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).

## <a name="changes-in-core-hr"></a>Ændringer i Core HR
**Build 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>Konfigurere arbejdsgang til automatisk at godkende eller følge arbejdsgang, når en personale- eller linjechef sender eller opdaterer anmodninger om fridage
Nye betingelser for arbejdsgange er tilføjet for at tillade, at anmodninger om fridage godkendes automatisk, hvis de sendes af en medarbejders chef eller af personaleafdelingen. Én måde at opnå denne automatiske godkendelse i en arbejdsgang er gennem aktivering af en automatisk handling under godkendelsen af arbejdsgangen.

De poster, som er medtaget, omfatter:

- Sendt af - Bruges til at evaluere systembruger-id'et for den bruger, der har sendt anmodningen til arbejdsgangen.
- Sendt på vegne af - Bruges til at vurdere, om orlovsanmodningen er sendt på vegne af den arbejder, der er knyttet til anmodningen.
- Sendt af Personale - Bruges til at vurdere, om den systembruger, der har sendt anmodningen til arbejdsgangen, har en Personale-rolle.
- Sendt af chef – Bruges til at vurdere, om den bruger, der sendte orlovsanmodningen til arbejdsgangen, er leder af linjehierarkiet for den arbejder, der er knyttet til anmodningen.

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>Muliggøre fast medarbejderløn for fremtidige stillingstildelinger
Det er almindeligt, at nye medarbejdere i en organisation ansættes med en fremtidig startdato. Med denne ændring kan fast løn defineres for kommende medarbejdere med fremtidige stillingstildelinger.

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>Lønfelter for stillingen er tomme, når du redigerer stillingen
Med denne ændring får lønfelterne nu de aktuelle standardværdier, når der anmodes om ændringer af eksisterende stillinger.

### <a name="other-miscellaneous-bug-fixes"></a>Diverse andre fejlrettelser
Andre mindre fejlrettelser er medtaget i denne version.

### <a name="upgrade-to-common-data-service"></a>Opgrader til Common Data Service
Fristerne for at opgradere til Common Data Service nærmer sig med hastige skridt. Log på PowerApps Administration for at finde ud af, om din database skal opgraderes. Du kan finde flere oplysninger om frister og de nødvendige trin for at opgradere under [Opgrader til Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="coming-soon"></a>Kommer snart

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avanceret lønsikkerhed (fast og variabel)
I mange organisationer har chefer for løn og frynsegoder kun har adgang til bestemte lønposter, f.eks. poster, der er beregnet til ledere eller medarbejdere i bestemte områder. Med denne ændring kan du administrere og vedligeholde lønstrukturer for forskellige medarbejdergrupper i organisationen. faste og variable strukturer kan tildeles til sikkerhedsroller, som bestemmer adgangen til strukturerne og de medarbejderdata, der er knyttet til strukturerne, f.eks. løn- eller bonusposter. Kun roller med den givne adgang kan behandle løn for de pågældende medarbejdere.

###  <a name="platform-update-24"></a>Platformsopdatering 24
Yderligere oplysninger om Platform update 24 finder du i [Nyheder eller ændringer i Dynamics 365 for Finance and Operations Platform update 24 (marts 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).
