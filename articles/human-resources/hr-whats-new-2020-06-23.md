---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (25. juni 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 6/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc1931cee0f3da15e07908f221282ad6b57e1681
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500431"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (23. juni 2020)

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3347. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Når en tilmelding er udløbet for en fratrådt medarbejder, ryddes orlovstypen, saldoen og beløbet i formularen Orlovstilmelding (444867)

Værdierne i **Orlovstype**, **Saldo** og **Beløbet** bevares nu i stedet for at blive ryddet, når dette valg foretages.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Forkert budgetteret saldo, når den nye funktion (Orlovsperiodisering for et enkelt firma eller en enkelt plan) er aktiveret (456553)

Den rigtige budgetterede prognose vises nu, når orlovsperiodiseringen for et enkelt firma eller en enkelt plan er aktiveret.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Enheder med relationer, der resulterer i dublerede navigationsegenskaber (456486)

Denne version retter et problem med navigationsegenskaberne (relationen) for flere enheder. Dublerede relationer registreres. Disse scenarier er alle blevet rettet.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Kommentarer på tværs af firmaer ved performance-gennemgang (455536)

Kommentarer på tværs af firmaer kan nu ses på performance-gennemgange med denne rettelse. Denne ændring korrigerer visningen af validators kommentarer, der er angivet i forskellige firmaer for den samme performance-gennemgang.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Inkonsistens i visning af kompensationsstyringsdata (432562)

En ensartet visning af kompensationsdata vedligeholdes nu i lederselvbetjening. Afhængigt af, hvordan du navigerer til en arbejders **kompensationsoplysninger**, vises kompensationsdataene nu altid for lederne.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Ikrafttrædelsesdato for fast løn angives som standard til dags dato (411994)

Startdatoen for kompensation er nu baseret på startdatoen for den stilling, der tildeles medarbejderen.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Formularen Aktivér halvdagsdefinition for orlov og fravær er deaktiveret, når formularen åbnes (452607)

Med denne ændring aktiveres **Aktivér Halvdagsdefinition**, indtil der findes nye orlovsposteringer. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Der kan ikke udgives til HcmDiscussionEntity via Excel. Fejl i feltet TotalRatingScore (453899)

Du kan nu opdatere feltet **TotalRatingScore** ved hjælp af **HCMDiscussionEntity** i Excel-projektmappedesigneren.

## <a name="in-preview"></a>Som eksempel

## <a name="database-logging"></a>Databaselogføring

Databaselogning gør det muligt at bestemme, hvilke tabeller og felter der skal overvåges. Du kan også bestemme, hvilke hændelser der skal udløse ændringssporing. Du kan bruge logføringsfunktioner for databasen til at se disse ændringer over tid. Du kan finde flere oplysninger under [Konfigurere og administrere databaselogning](hr-admin-database-logging.md).

## <a name="mandatory-fields"></a>Obligatoriske felter 

Du kan nu gøre felter obligatoriske ved hjælp af funktionerne til tilpasning til personale. Denne funktion kræver **Gemte visninger**.

## <a name="human-resources-application-in-teams"></a>Human Resources-app i Teams

Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams. De kan interagere med en bot for at oprette orlovsanmodninger. Yderligere oplysninger finder du i [Human Resources-appen i Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-enheder (Data Management Framework) til styring af frynsegoder
 
Enheder til håndtering af frynsegoder frigives. Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring. En skabelon til frynsegodestyring kan også bruges til at flytte data. Skabelonen eksporterer og importerer dataene sekventielt for at respektere dataafhængigheder.

## <a name="buy-and-sell-leave"></a>Købe og sælge orlov 

Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov. Denne proces styres ofte manuelt. Denne funktion automatiserer administration af politikker og anmodninger for HR-afdelingen. Den effektiviserer orlovsprocessen og medvirker til at eliminere fejltagelser. Du kan finde flere oplysninger i:

- [Administrere politikker for køb og salg af orlov](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Købe og sælge orlov](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Orlovsperiodisering for et enkelt firma eller en enkelt plan

Kunderne kan behandle periodiseringer for et enkelt firma eller en enkelt orlovs- fraværsplan. Denne mulighed giver klarhed over periodiseringsprocessen for kunder med forskellige sabbatår eller politikker for orlovsperiodisering. Du kan finde flere oplysninger under [Periodiseret orlov pr. firma eller pr. orlovsplan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).

## <a name="add-attachments-to-time-off-requests"></a>Føje vedhæftede filer til anmodninger om fravær

Muligheden for at føje vedhæftede filer til anmodninger om godkendt orlov er afgørende i det aktuelle COVID-19-miljø. Medarbejderne kan nu tilføje disse vedhæftede filer. De har også en mere indsigt i, hvordan der foretages opdateringer af anmodninger om orlov. Du kan finde flere oplysninger under [Føje en vedhæftet fil til en eksisterende anmodning](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Føje årsagskode til periodiseringssuspenderinger 

Årsagskoder er føjet til periodiseringssuspenderingen.

## <a name="carry-forward-rules"></a>Overføre regler 

Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres. Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage. Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Suspendere orlovsperiodisering for angivne orlovstyper

Du kan oprette en regel om suspendering af orlovsperiodiseringer for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov. Ubetalt orlov kan være en type, men behøver ikke at være det. Du kan suspendere enhver orlov baseret på en anden orlovstype.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhed er tilgængelig for periodiseringssuspenderinger 

En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.

## <a name="coming-soon"></a>Kommer snart

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurere navnet på medarbejderselvbetjening

En ny indstilling vil være tilgængelig i **Human Resources-parametrene** for at opdatere navnet på arbejdsområdet for medarbejderselvbetjening.

## <a name="checklist-entities-included-in-common-data-service"></a>Kontrollisteenheder inkluderet i Common Data Service

Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Common Data Service.
