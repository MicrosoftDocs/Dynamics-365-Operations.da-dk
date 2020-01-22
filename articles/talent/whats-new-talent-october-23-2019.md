---
title: Nyheder eller ændringer i Dynamics 365 Talent (23. oktober 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
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
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7506953c797f5a55a93f1169bf48af8b06eb440e
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896790"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (23. oktober 2019)

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard
Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2569. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Platform update 30 til Finance and Operations-apps

Du kan finde flere oplysninger i [Nyheder eller ændringer i Platform update 30 til Finance and Operations-apps (november2019)](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Fjerne åben tilmelding som frynsegoder som prøveversionsfunktion

Sammen med vores meddelelse i blogindlægget [Strategiske investeringer i Core HR som drivkraft bag ekspertise](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) fjerner Microsoft frynsegoder som åben tilmeldingsfunktion fra offentlig prøveversion d. 18. oktober 2019. Der vil i stedet blive udgivet nye funktioner i fremtiden. Produktionens anvendelse af frynsegoder som åben tilmeldingsfunktion, der i øjeblikket findes i offentlig prøveversion, understøttes ikke.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Der opstod en fejl under valg af land/område i arbejderformularen endnu en gang (350294)

Med denne uges udgivelse er problemet blevet løst, når du vælger et land/område i formularen **Arbejder**.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Økonomiske dimensionsværdier bruges som standard til kombinationsvisningsfeltet, når Tillad ikke manuel angivelse er angivet til sand (340097)

Når du med denne ændring konfigurerer økonomiske dimensioner og bruger muligheden for ikke at tillade manuel indtastning, vil standardværdien for dimensionsværdi blive korrekt angivet i feltet **Kombinationsvisning**.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Nye relationstyper skal føjes til relationsopslag i formularen til personlige kontakter (347691)

Denne version indeholder nye funktioner til at tilføje nye relationstyper i tabellen **Relationstyper** og afspejler disse ændringer i relationsopslag for personlige kontakter.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Yderligere listeværdier i brugerdefinerede felter vises ikke i Common Data Service (379599)

Med denne uges udgivelse vil tilføjelse af en ny listeværdi i et eksisterende brugerdefineret felt, der allerede er synkroniseret med Common Data Service, vise værdier for den nye plukliste, når der er anvendt ændringer på enheden.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>På siden Ansættelsesvilkår vises alle medarbejdernes ansættelsesvilkår, når du har valgt Åbn i Excel (348073)

I denne version er det kun ansættelsesvilkårene for de valgte medarbejdere, der åbnes i Excel. Al firmasikkerhed overholdes også.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>Tilknytningen mellem ferieobjektet i arbejdskalenderen og arbejdskalenderobjektet mangler i Common Data Service (324178)

Denne relation er blevet tilføjet med udgivelsen. Denne ændring vil gøre det muligt at få vist arbejdsdage for en medarbejder i PowerApps. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Fejl ved brug af arbejdsgange for medarbejderselvbetjening med konfigurerbare hierarkier (370132)

I denne version findes der bedre meddelelser om, hvordan du kan konfigurere arbejdsgange med konfigurerbare hierarkier. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>Systemet tillader oprettelse af nye stillinger, hvor Tilgængelig for tildeling-datoen er tidligere end aktiveringsdatoen (340103)

Denne ændring viser en advarsel, når **Tilgængelig for tildeling**-datoen ligger før stillingens **Aktivering**-dato.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Se [Udskrive performancegennemgange](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019 frigivelsesbølge 2-plan.

### <a name="feature-management-workspace"></a>Arbejdsområdet Administration af funktioner

Funktioner tilføjes og opdateres i alle versioner. Administrationen af funktioner indeholder et arbejdsområde, hvor du kan få vist en liste over de funktioner, der er leveret i hver version. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem.

Du kan få mere at vide om de ændringer, der kommer til funktionsstyring, under [Oversigt over funktionsstyring](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
