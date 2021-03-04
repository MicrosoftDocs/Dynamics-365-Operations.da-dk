---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (11. juni 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 11. juni 2020.
author: Darinkramer
manager: AnnBe
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0720b2024a865fcd42cd80fd905586d626388f8f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417850"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (11. juni 2020)

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3316. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>Strømlinede medarbejderformularer bevirker nogle gange, at lukke (X)-knapper i underordnede formularer holder op med at fungere (442369)

Når den nye formular **Arbejder** blev aktiveret, fungerede knappen Luk (**X**) indimellem ikke i underordnede formularer. Dette problem var periodisk. Du kunne lukke formen, når du var gået væk fra den og vendte tilbage til den. Du kunne f.eks. vælge et menupunkt til venstre og gå tilbage til **Arbejder**-formularen og derefter lukke den. Denne uges frigivelse løser dette problem. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>Arbejderens personlige kontaktpersonenhed eksporterer ikke personlige kontakter med en overordnet relationstype

Med denne frigivelse eksporterer objektet **Arbejders personlige kontaktperson** alle relationstyper.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>HcmPositionWorkerAssignmentV2Entity skal være en del af Ceridian-lønintegrationspakken som standard (448506)

Med denne ændring er **HcmPositionWorkerAssignmentV2Entity** inkluderet i Ceridian-lønintegrationspakken.

## <a name="in-preview"></a>Som eksempel

## <a name="database-logging"></a>Databaselogføring

Du kan bruge funktionen til databaselogning til at bestemme, hvilke tabeller og felter der skal overvåges. Du kan også bestemme, hvilke hændelser der skal udløse ændringssporing. Du kan bruge logføringsfunktioner for databasen til at se disse ændringer over tid. Du kan finde flere oplysninger under [Konfigurere og administrere databaselogning](hr-admin-database-logging.md).

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

## <a name="new-platform-capabilities"></a>Nye platformsmuligheder 

Du kan gøre felter obligatoriske ved hjælp af tilpasning. Denne funktion kræver, at du aktiverer **Gemte visninger**.

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurere navnet på medarbejderselvbetjening

En ny indstilling vil være tilgængelig i Human Resources-parametrene for at opdatere navnet på arbejdsområdet for medarbejderselvbetjening. 

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]