---
title: Periodiser orlovs- og fraværsplaner
description: Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 348c8e5336854eb2a1c04a1f98a97a2c9dba7176
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464904"
---
# <a name="accrue-leave-and-absence-plans"></a>Periodiser orlovs- og fraværsplaner

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Periodisere orlov og fravær for flere medarbejdere

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Under **Administrer orlov** skal du vælge **Periodiser orlovs- og fraværsplaner**.

3. Dialogboksen **Periodisere planer for orlov og fravær** vises. I **Periodisering pr.** skal du vælge **Dags dato** eller **Brugerdefineret dato** og angive en brugerdefineret dato.

4. Hvis du vil køre periodiseringer for alle firmaer, skal du vælge **Alle firmaer**. Hvis du vil behandle periodiseringer for en enkelt orlovsplan, skal du vælge **Nej** for **Alle planer** og derefter vælge en **Orlovsplan**. Hvis du vælger alle firmaer, kan du ikke vælge en individuel orlovsplan. 

5. Hvis du vil køre periodiseringsprocessen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

   1. Angiv oplysninger om periodiseringsprocessen.

   2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.

   3. Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.

   4. Vælg **OK**. Periodiseringsprocessen køres med de parametre, du angiver.

## <a name="accrue-leave-and-absence-for-an-employee"></a>Periodisere orlov og fravær for en medarbejder

1. Vælg **Orlov** i medarbejderens post.

2. Vælg **Periodiser orlovs- og fraværsplaner**.

3. Dialogboksen **Periodisere planer for orlov og fravær** vises. I **Periodisering pr.** skal du vælge **Dags dato** eller **Brugerdefineret dato** og angive en brugerdefineret dato.

4. Hvis du vil køre periodiseringer for alle firmaer, skal du vælge **Alle firmaer**. Hvis du vil behandle periodiseringer for en enkelt orlovsplan, skal du vælge **Nej** for **Alle planer** og derefter vælge en **Orlovsplan**. Hvis du vælger alle firmaer, kan du ikke vælge en individuel orlovsplan. 

5. Hvis du vil køre periodiseringsprocessen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

   1. Angiv oplysninger om periodiseringsprocessen.

   2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.

   3. Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.

   4. Vælg **OK**. Periodiseringsprocessen køres med de parametre, du angiver.

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a>Slette periodiseringer af orlov og fravær for flere medarbejdere

Slet periodiseringsposter for en specifik plan og et bestemt datointerval. Periodiseringsdatoer skal være dateret i dag eller i fremtiden.

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Under **Administrer orlov** skal du vælge **Slet periodiseringer af orlovs- og fraværsplaner**.

3. Vælg **Orlovsplan** i dialogboksen **Slet periodiseringer af orlovs- og fraværsplaner**. 

4. Vælg **Slet saldoreguleringer**, hvis det er relevant.

5. Angiv eller vælg en **Dato for orlovsperiodisering**. Denne dato skal være i dag eller i fremtiden. 

6. Vælg **OK**. Periodiseringsprocessen sletter periodiseringer med de parametre, du angiver. 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a>Slette periodiseringer af orlov og fravær for en enkelt medarbejder

1. Vælg **Orlov** i medarbejderens post.

2. Vælg **Slet periodiseringer af orlovs- og fraværsplaner**.

3. Vælg **Orlovsplan** i dialogboksen **Slet periodiseringer af orlovs- og fraværsplaner**. 

4. Vælg **Slet saldoreguleringer**, hvis det er relevant.

5. Angiv eller vælg en **Dato for orlovsperiodisering**. Denne dato skal være i dag eller i fremtiden. 

6. Vælg **OK**. Periodiseringsprocessen sletter periodiseringer med de parametre, du angiver. 

## <a name="review-leave-accrual-and-deletion-processes"></a>Gennemse processer til orlovsperiodisering og sletning

**Revision af orlovsperiodisering** vises, hver gang du kører eller sletter en periodisering for en eller flere medarbejdere. Datoen og den person, der udførte handlingen, vises også.

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Under **Administrer orlov** skal du vælge **Slet revision af orlovsperiodisering**.

## <a name="see-also"></a>Se også

[Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)</br>
[Oprette en plan for orlov og fravær](hr-leave-and-absence-plans.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]