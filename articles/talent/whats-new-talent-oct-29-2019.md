---
title: Nyheder eller ændringer i Dynamics 365 Talent (29. oktober 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529678"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (29. oktober 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2586. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Slet parter uden roller skal være aktiveret som standard (371233)

Når du klargør et nyt miljø i Talent, skal du **Slette parter uden roller**, hvis der ikke findes nogen roller, der som standard er slået til. Når du sletter en arbejder, fjernes den part, der er knyttet til arbejderen, ikke, medmindre denne indstilling er aktiveret. Denne ændring begrænser dublerede poster i det globale adressekartotek, når du har brug for at importere, ændre eller genimportere arbejdere.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Kladder og annullerede orlovsanmodninger skal have tilladelse til at blive slettet i Common Data Service (376999)

Med denne ændring kan du nu slette orlovsanmodninger med statussen **Kladde** eller **Annulleret** i Common Data Service.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Yderligere listeværdier i brugerdefinerede felter afspejles ikke i Common Data Service, når der klikkes på Anvend på brugerdefinerede formularfelter (379599)

Når du tilføjer nye listeværdier til et eksisterende brugerdefineret felt, der allerede er synkroniseret med Common Data Service, er de nu tilgængelige i Common data service, når du har anvendt ændringerne i formularen **Brugerdefinerede felter** .

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Anvend onboarding-kontrollister på tværs af juridiske enheder, når der findes mere end én ansættelse (371270)

I denne uges udgivelse kan du anvende kontrollister på medarbejdere med mere end én ansættelse i **Arbejderformular > Checklister**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Forhåndsvisning af Åben tilmelding som frynsegoder er blevet fjernet

Sammen med vores meddelelse i blogindlægget [Strategiske investeringer i Core HR som drivkraft bag ekspertise](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) har Microsoft fjernet frynsegoder som åben tilmeldingsfunktion fra offentlig prøveversion. Nye funktioner bliver udgivet i fremtiden. Produktionsanvendelsen af funktionen åben tilmelding som frynsegoder understøttes ikke.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Se [Udskrive performancegennemgange](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019 frigivelsesbølge 2-plan.

### <a name="feature-management-workspace"></a>Arbejdsområdet Administration af funktioner

Funktioner tilføjes og opdateres i alle versioner. Administrationen af funktioner indeholder et arbejdsområde, hvor du kan få vist en liste over de funktioner, der er leveret i hver version. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem.

Du kan få mere at vide om de ændringer, der kommer til funktionsstyring, under [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
