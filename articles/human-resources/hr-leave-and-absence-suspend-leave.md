---
title: Suspendere orlov
description: Du kan suspendere en orlov for en medarbejder i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SuspendLeave, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9c8262fb34175f6f9326d6be82c922b2170fc5a7
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805254"
---
# <a name="suspend-leave"></a>Stop orlov midlertidigt

>[!Important]
>De funktioner, der nævnes i denne artikel, er i øjeblikket tilgængelige for kunder med enkeltstående Dynamics 365 Human Resources. Nogle eller alle funktionerne vil være tilgængelige som en del af en fremtidig version af Finance-infrastrukturen efter Finance-frigivelse 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan suspendere en medarbejders orlov for at stoppe behandling af orlovsperiodisering for de valgte orlovstyper.

## <a name="suspend-leave-and-absence-for-an-employee"></a>Suspendere orlov og fravær for en medarbejder

1. Vælg **Orlov** i medarbejderens post.

2. Vælg **Suspender orlov**.

3. Vælg **Ny**.

4. Vælg **Orlovstype** sammen med **Startdato** og **Slutdato** for suspensionen i dialogboksen **Suspender periodisering af orlov**.

5. Du kan også føje en **Kommentar** til suspensionen. 

Hvis periodiseringer behandles, mens medarbejderens orlov er suspenderet, foretages der ingen periodisering af de suspenderede orlovstyper.

> [!NOTE]
> Orlovsanmodninger suspenderer anmodninger om fravær, men anmodninger om fravær suspenderer ikke anmodninger om orlov.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
- [Konfigurere orlovs- og fraværstyper](hr-leave-and-absence-types.md)
- [Periodisere orlovs- og fraværsplaner](hr-leave-and-absence-accrue.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
