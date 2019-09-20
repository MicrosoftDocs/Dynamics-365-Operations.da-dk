---
title: Nyheder eller ændringer i Dynamics 365 for Talent (27. august 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a405ee96c36dd803fb46894ab58eca9dbfd81b5f
ms.sourcegitcommit: 097492a9e4f53a5e1fd5385d8764798518326818
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/29/2019
ms.locfileid: "1927980"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Nyheder eller ændringer i Dynamics 365 for Talent (27. august 2019)

[!include [banner](includes/banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2447. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Visningsfunktioner er kun aktiverede i sandkasseforekomster

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er Produktion eller Sandkasse. Forekomster af typen Sandkasse giver mulighed for tidlig test af nye funktioner. Alle eksisterende Talent-forekomster vil blive opdateret til Produktion-forekomsttypen. Hvis en af de eksisterende forekomster skal opdateres til Sandkasse-forekomsttypen, skal du kontakte Support for at starte ændringsanmodningen.

Du kan finde flere oplysninger om, hvordan ændringer udgives, ved at se [Klargøre Talent](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Få vist udvidede oplysninger om performance i selvbetjeningstjeneste

En ny indstilling gør det muligt for lederne at få vist performance for både direkte underordnede og deres udvidede underordnede. I øjeblikket kan linjechefer tildele og opdatere præstationsmålsætninger og udstede nye fornyede gennemgange. Desuden kan direkte ledere og deres medarbejdere vedligeholde og opdatere performancekladder for at hjælpe med at sikre, at performancegennemgangsprocessen går problemfrit. Når denne ændring er implementeret, kan ledere få vist og vedligeholde oplysninger, der er relateret til performance, for deres udvidede underordnede ud over deres direkte underordnede.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Sletning af juridiske enheder er ikke tilladt, hvis der findes medarbejdere i firmaet (339849)

Med denne ændring kan du ikke fjerne eller slette firmaer, hvis der findes medarbejdere og andre relaterede data for den juridiske enhed.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Kompensationsstyringens Business Intelligence-analyse stemmer ikke overens med arbejdsområdet til kompensation (322493)

I denne version er kompensationsanalysen justeret, så den præcist afspejler de planer, der er tildelt medarbejdere.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Pladsholderen %company% i arbejdsgang viser DAT ved ansættelse af medarbejdere via arbejdsgang (343905)

I denne version viser firmaets pladsholder den juridiske enhed, der er knyttet til ansættelsen af den nye medarbejder.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>CDSJobPosition-enheden viser en fejl, når der er angivet gyldig til-dato (349387)

I denne version tillader datakilderne **Stillingsdetaljer** og **Stillings varighed** på **CDSJobPosition**-enheden redigeringer fra Common Data Service til felterne **Gyldig fra**. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>For medarbejderens fratrædelse udfyldes den sidste arbejdsdag på tildelingens slutdato (332496)

Denne ændring bruger nu som standard **Slutdato for ansættelse** for **Slutdato for tildeling**. Du kan ændre disse standarder, mens du indtaster data.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Juridiske enheder er ikke begrænset til ansættelse (338871)
 
Denne ændring begrænser ansættelsesprocessen, så den kun viser de juridiske enheder, som brugeren har adgang til.  

## <a name="in-preview"></a>Som eksempel

### <a name="streamlined-employee-entry-and-navigation"></a>Strømlinet medarbejderangivelse og navigation

Denne funktionalitet er nu tilgængelig i sandkasse- og prøvemiljøer. Hvis du vil aktivere funktionen, skal du gå til **Systemadministration > Links > Opsætning > Systemparametre > Funktioner i prøveversion**. Vælg **Udvidet arbejderform og navigation**. Dette aktiverer disse ændringer for alle brugere. Du kan deaktivere denne indstilling på et hvilket som helst tidspunkt.

Du kan finde oplysninger under [Strømlinet medarbejderangivelse og navigation](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Kommer snart

### <a name="platform-update-29"></a>Platform update 29

Du kan finde yderligere oplysninger om Platform update 29 under [Funktioner i prøveversionen af Dynamics 365 for Finance and Operations platform update 29 (oktober 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
