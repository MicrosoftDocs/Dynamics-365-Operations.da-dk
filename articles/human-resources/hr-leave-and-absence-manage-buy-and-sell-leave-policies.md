---
title: Administrere politikker for køb og salg af orlov
description: Du kan give medarbejderne mulighed for at købe og sælge orlov i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429007"
---
# <a name="manage-buy-and-sell-leave-policies"></a>Administrere politikker for køb og salg af orlov

[!include [banner](includes/preview-feature.md)]

Du kan give medarbejderne mulighed for at købe orlov ved at oprette en politik for køb af orlov.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Give medarbejdere mulighed for at købe og sælge orlov

1. På siden **Parametre for orlov og fravær** skal du vælge **Ja** for **Tillad medarbejderne at købe orlov**. 

## <a name="create-a-buy-leave-policy"></a>Oprette en politik for køb af orlov

1. På siden **Orlov og fravær** skal du vælge fanen **Links**. 

2. Vælg **Politik for køb oig salg af orlov**.

3. Vælg **Ny**.

4. Angiv et **Navn** og en **Beskrivelse** for politikken under **Politik for køb og salg af orlov**. 

5. Vælg en **Politiktype**. 

   De tilgængelige politiktyper er **Beløb** og **Timer pr. uge**. Vælg **Beløb** for at angive et **Fast beløb** for de maksimale beløb, som medarbejderne kan købe og sælge. Hvis du vælger **Timer pr. uge**, bruges den arbejdstid, der er defineret i medarbejderens tildelte arbejdstidskalender, til at bestemme det maksimale antal for politikken. 

6. Vælg en **Startdato** og en **Slutdato** for politikken. Anmodninger om at købe eller sælge orlov vil kun kunne sendes i løbet af denne tidsramme. 

7. Under **Politik for køb** skal du vælge **Fuldtidsækvivalens** (FTÆ) for at opnå det maksimale beløb baseret på den FTÆ, der er defineret folr medarbejderens stilling. Hvis politiktypen er **Beløb**, skal du angive et **Maksimalt fast beløb**. 

8. Vælg **Tilføj** for at tilføje orlovstyper, som medarbejderne kan købe orlov for. Du kan føje flere orlovstyper til politikken. 

9. Angiv **Måneders tjeneste** for orlovstypen for at aktivere forskellige tjenestemåneder og bestemme det maksimale beløb, som en medarbejder kan købe. 

10. Angiv **Maksimalt beløb** for orlovstypen. 

11. Angiv den **Lønsats**, som medarbejderen skal købe orloven med. 

12. Du kan vælge at angive den **Lønkode**, der skal bruges til købet af orlov. 

13. Du kan evt. angive, om du vil bruge FTÆ til at bestemme det maksimale beløb for orlovstypen. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Føje politikken for køb og salg af orlov til en orlovs- og fraværsplan

1. På siden **Orlov og fravær** skal du vælge en orlovs- og fraværsplan.

2. Under **Regler** skal du vælge **Politik for køb og salg af orlov**.

## <a name="see-also"></a>Se også

[Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)</br>
[Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md)</br>
[Periodiser orlovs- og fraværsplaner](hr-leave-and-absence-accrue.md)</br>
[Køb og sælg orlov](hr-employee-self-service-buy-sell-leave.md)

