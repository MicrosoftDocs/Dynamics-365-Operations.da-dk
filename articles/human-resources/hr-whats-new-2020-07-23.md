---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (23. juli 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 23. juli 2020.
author: andreabichsel
manager: tfehr
ms.date: 07/23/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f5e10d6d1dedfc251a1a00110b50c9096314d75b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127515"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (23. juli 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3416. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Sletning af økonomiske dimensioner på en stilling fungerer ikke som forventet (445476)

Hvis du fjerner dimensioner fra en stilling, fjerner du nu de samme stillinger fra Dataverse.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Stillinger, der ikke er i hierarki, viser inaktive stillinger (397257)

Stillinger, der er inaktive (har en udløbet varighed), vises ikke længere i stillingshierarkiet som **Stillinger, der ikke er i hierarki**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Validering, der sker mellem LeaveEnrollmentEntity og HcmWorkerEntity under import af Data Management Framework (DMF), medfører langsom dataindlæsning (442324)

Ændringer i denne frigivelse øger ydeevnen af **LeaveEnrollmentEntity**.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Det er ikke muligt at tilpasse i organisationsadministration (447490)

Med denne ændring kan du nu tilpasse linkene i **Organisationsadministration**.

## <a name="in-preview"></a>Som eksempel

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

Kunderne kan behandle periodiseringer for et enkelt firma eller en enkelt orlovs- fraværsplan. Denne mulighed giver klarhed over periodiseringsprocessen for kunder med forskellige sabbatår eller politikker for orlovsperiodisering. Du kan finde flere oplysninger under [Periodiseret orlov pr. firma eller pr. orlovsplan](hr-leave-and-absence-accrue.md).

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

## <a name="checklist-entities-included-in-dataverse"></a>Kontrollisteenheder inkluderet i Dataverse

Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.

## <a name="platform-changes"></a>Platformsændringer

Platform update 10.0.12 (36)

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)
