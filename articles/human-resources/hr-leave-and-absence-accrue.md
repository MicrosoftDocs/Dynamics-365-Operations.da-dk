---
title: Periodiser orlovs- og fraværsplaner
description: Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: f045cb7ab9f5e7aa4259f29e1b026f110425c236
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429053"
---
# <a name="accrue-leave-and-absence-plans"></a>Periodiser orlovs- og fraværsplaner

Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Periodisere orlov og fravær for flere medarbejdere

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Under **Administrer orlov** skal du vælge **Periodiser orlovs- og fraværsplaner**.

3. Dialogboksen **Periodisere planer for orlov og fravær** vises. I **Periodisering pr.** skal du vælge **Dags dato** eller **Brugerdefineret dato** og angive en brugerdefineret dato.

4. Hvis du vil køre periodiseringsprocessen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

   1. Angiv oplysninger om periodiseringsprocessen.

   2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.

   3. Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.

   4. Vælg **OK**. Periodiseringsprocessen køres med de parametre, du angiver.

## <a name="accrue-leave-and-absence-for-an-employee"></a>Periodisere orlov og fravær for en medarbejder

1. Vælg **Orlov**i medarbejderens post.

2. Vælg **Periodiser orlovs- og fraværsplaner**.

3. Dialogboksen **Periodisere planer for orlov og fravær** vises. I **Periodisering pr.** skal du vælge **Dags dato** eller **Brugerdefineret dato** og angive en brugerdefineret dato.

4. Hvis du vil køre periodiseringsprocessen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

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

1. Vælg **Orlov**i medarbejderens post.

2. Vælg **Slet periodiseringer af orlovs- og fraværsplaner**.

3. Vælg **Orlovsplan** i dialogboksen **Slet periodiseringer af orlovs- og fraværsplaner**. 

4. Vælg **Slet saldoreguleringer**, hvis det er relevant.

5. Angiv eller vælg en **Dato for orlovsperiodisering**. Denne dato skal være i dag eller i fremtiden. 

6. Vælg **OK**. Periodiseringsprocessen sletter periodiseringer med de parametre, du angiver. 

## <a name="review-leave-accrual-and-deletion-processes"></a>Gennemse processer til orlovsperiodisering og sletning

**Revision af orlovsperiodisering** vises, hver gang du kører eller sletter en periodisering for en eller flere medarbejdere. Datoen og den person, der udførte handlingen, vises også.

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Under **Administrer orlov** skal du vælge **Slet revision af orlovsperiodisering**.

## <a name="configure-preview-features"></a>Konfigurere prøveversioner

[!include [banner](includes/preview-feature-leave-absence.md)]

Hvis du har aktiveret prøvefunktioner for orlov og fravær, skal du også konfigurere indstillingerne for dem.

### <a name="accrue-leave-per-company-or-per-leave-plan"></a>Periodiser orlov pr. firma eller pr. orlovsplan

Når du periodiserer orlovs- og fraværsplaner, kan du vælge at periodisere for alle firmaer. Hvis du vælger alle firmaer, kan du ikke vælge planer for personlig orlov. Hvis du vælger ikke at periodisere for alle firmaer, kan du periodisere for en bestemt orlovsplan. 

Disse indstillinger er tilgængelige, når du periodiserer for alle medarbejdere eller enkelte medarbejdere. 

## <a name="see-also"></a>Se også

[Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)</br>
[Oprette en plan for orlov og fravær](hr-leave-and-absence-plans.md)
