---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (28. maj 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37f21fffe209e17a6fe89c2661e49fc0dc8b9655
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443458"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (28. maj 2020)

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3287. Tallene i parenteser i nogle overskrifter henviser til LCS-supportnumre som reference.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>LeaveRequest-enheden fungerer ikke, når du aktiverer flere typer pr. orlovsplan (447498)

Med denne ændring er **LeaveEnrollmentV2Entity** nu tilgængelig til at rette den fejl, der opstår, når du aktiverer flere orlovstyper.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Funktion til reduktion af batchindhold (prøveversion) (446619)

Når du aktiverer denne funktion, kan du forvente en reduktion i blokeringen af batchstrukturtabeller, mens du vælger opgaver og afslutter job.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict, der sparer arbejderen, forhindrer redigering af en post i People (427915)

Denne ændring retter en fejl ved tilføjelse af en ny arbejder, med opdatering af adresseoplysninger og ændring af foretrukket sprog. I dette entydige scenarie blev der vist en fejl, som angiver, at posten ikke kunne opdateres. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Det var ikke muligt at føje en vedhæftet fil til en godkendt orlovsanmodning, der skulle sendes igen (425407)

Denne ændring tillader nu, at der vedhæftes filer til godkendte orlovsanmodninger.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Brugeren kan angive kompensation for en medarbejder i en anden juridisk enheds formular (409529)

Denne ændring deaktiverer kompensationsindstillingerne for at forhindre utilsigtet indtastning af kompensationsposter for den forkerte juridiske enhed.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Fejl, når du overfører en medarbejder, og datoen for arbejderens stillingstildeling er før stillingens varighed (429402)

Fejlmeddelelser, når en medarbejder overføres i dette scenarie, er blevet opdateret, så de indeholder en bedre beskrivelse af de ændringer, der er nødvendige for at løse problemet.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Egenskaber for vedhæftede filer i tilmelding til frynsegoder i medarbejderselvbetjening
 
Nu kan du tilføje vedhæftede filer under tilmeldingsprocessen for frynsegoder for hver enkelt plan, som medarbejderen tilmelder sig. Du kan derefter få vist de vedhæftede filer i formularen **Frynsegode, som arbejderen er tilmeldt**.

## <a name="in-preview"></a>Som eksempel

## <a name="human-resources-application-in-teams"></a>Human Resources-app i Teams

Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams. De kan interagere med en bot for at oprette orlovsanmodninger. Yderligere oplysninger finder du i [Human Resources-appen i Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="leave-suspension"></a>Forlad suspension

Du kan afbryde orlov og fravær i Human Resources for en medarbejder. Når du suspendere orlov, stoppes orloven for de valgte orlovstyper. Hvis suspensionen finder sted, når en periodisering er blevet behandlet, opretter suspensionen en forholdsmæssig justering til medarbejderens orlov. Du kan finde flere oplysninger i [Suspender orlov](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Opdatere brugeroplevelsen for at angive, at periodiseringen er udsat (429550)

Brugeroplevelsen indikerer nu, at periodiseringen er blevet suspenderet for en plan.

## <a name="coming-soon"></a>Kommer snart

## <a name="database-logging-in-preview-in-june"></a>Databaselogning (i prøveversion i juni)

Du kan bruge funktionen til databaselogning til at bestemme, hvilken tabel og hvilke felter der skal overvåges. Du kan også bestemme, hvilke hændelser der skal udløse ændringssporing. Du kan få vist forespørgselsfunktioner for at se disse ændringer over tid.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Købe og sælge orlov (i prøveversion d. 1. juni)

Nogle organisationer giver et frynsegode, der giver medarbejderne mulighed for at købe eller sælge deres orlov. Denne proces styres ofte manuelt. Denne funktion giver en mere automatiseret metode til at administrere politikker og anmodninger for personaleafdelingen, og den hjælper med at eliminere fejl, samtidig med at orlovsprocessen strømlines. Du kan finde flere oplysninger i:

- [Administrere politikker for køb og salg af orlov](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Købe og sælge orlov](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>DMF-enheder (Data Management Framework) til styring af frynsegoder
 
Enheder til håndtering af frynsegoder frigives. Med DMF-enheder kan du importere og eksportere data, så du nemt kan konfigurere frynsegodestyring. En skabelon til frynsegodestyring kan også bruges til at flytte data. Skabelonen eksporterer og importerer dataene på en sekventiel måde for at respektere dataafhængigheder.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Føje årsagskoder til periodiseringssuspensioner (1. juni)

Årsagskoder er føjet til periodiseringssuspenderingen.

## <a name="carry-forward-rules-june-1"></a>Overføre regler (1. juni)

Du kan angive en orlovstype for overførselssaldi, hvor gennemførte reguleringer overføres. Hvis en medarbejder f.eks. overfører 10 dage, kan du vælge en anden orlovstype for disse 10 dage. Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Suspendere orlovsperiodisering for angivne orlovstyper (1. juni)

I denne udgave kan HR oprette en regel om periodiseringer for suspendering af orlov for medarbejdere med orlovsanmodninger, der er angivet til ubetalt orlov. Ubetalt orlov kan være en type, men behøver ikke at være det. Du kan suspendere enhver orlov baseret på en anden orlovstype.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF-enhed er tilgængelig for periodiseringssuspenderinger (1. juni)

En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.