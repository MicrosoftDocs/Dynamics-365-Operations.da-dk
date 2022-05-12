---
title: Periodiser orlovs- og fraværsplaner
description: Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.
author: twheeloc
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c9b9602e5c219be5756f5987b0497f2ce5c269d
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644296"
---
# <a name="accrue-leave-and-absence-plans"></a>Periodiser orlovs- og fraværsplaner

>[!Important]
>De funktioner, der nævnes i dette emne, er i øjeblikket tilgængelige for kunder med enkeltstående Dynamics 365 Human Resources. Nogle eller alle funktionerne vil være tilgængelige som en del af en fremtidig version af Finance-infrastrukturen efter Finance-frigivelse 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Periodisere orlov og fravær for flere medarbejdere

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Under **Administrer orlov** skal du vælge **Periodiser orlovs- og fraværsplaner**.

3. Dialogboksen **Periodisere planer for orlov og fravær** vises. I **Periodisering pr.** skal du vælge **Dags dato** eller **Brugerdefineret dato** og angive en brugerdefineret dato.

4. Hvis du vil køre periodiseringer for alle firmaer, skal du vælge **Alle firmaer**. Hvis du vil behandle periodiseringer for en enkelt orlovsplan, skal du vælge **Nej** for **Alle planer** og derefter vælge en **Orlovsplan**. Hvis du vælger alle firmaer, kan du ikke vælge en individuel orlovsplan.

5. Hvis du vil køre periodiseringsprocessen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

    1. Angiv oplysninger om periodiseringsprocessen.
    2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og derefter vælge **OK**.
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

## <a name="leave-accrual-rounding"></a>Afrunding af orlovsperiodisering
Når en medarbejder enten er tilmeldt eller ikke-tilmeldt, forholdsmæssig afrunding af orlov. Tidligere var afrunding kun tilladt, da en orlovsplan blev indstillet til fremskrivning, og en medarbejder var tilmeldt eller ikke tilmeldt i midt i perioden. Periodiseringer afrundes nu, uanset om der er tilmelding til eller afmelding i en periode eller i starten af en periode.

## <a name="leave-accrual-transaction-auditing"></a>Revision af transaktion til orlovsperiodisering

Denne funktion hjælper orlovs- og fraværsadministratorer med at forstå posteringer til periodisering af orlov og fravær, der er relateret til en medarbejders fritidssaldi for en bestemt orlovstype.

Sådan får du vist transaktionsdetaljer:

1. Vælg **Orlov** i medarbejderens post.

2. Vælg **Vis fridage**, og vælg derefter fanen **Saldi**.

Hvis du vil have vist de periodiseringsposteringer, der er relateret til en bestemt orlovstype, skal du vælge den numeriske værdi i kolonnen **Aktuel saldo**.

Hvis du vil have vist posteringsoplysningerne for et bestemt periodiseringsbeløb, skal du vælge en periodiseringsrække, åbne panelet **Relaterede oplysninger** til højre og derefter åbne sektionen **Transaktionsoplysninger**. Afsnittet Transaktionsoplysninger viser:

- Ændringer i medarbejderens orlovstypesaldo
- Oplysninger om ansættelse for den angivne periodiseringsperiode
- Oplysninger om periodiseringsperioden og satser
- Eventuelle ændringer af konfigurationen af orlovsplan

![Få vist revision af transaktion til orlovsperiodisering.](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a>Se også

[Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)</br>
[Oprette en plan for orlov og fravær](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
