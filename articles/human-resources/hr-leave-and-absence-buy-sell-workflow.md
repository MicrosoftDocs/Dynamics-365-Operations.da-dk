---
title: Oprette en arbejdsproces for køb og salg af orlov
description: Opret en arbejdsproces for køb og salg af orlov for at administrere anmodninger om køb og salg af orlov i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b9e56c130cd831e6a1ad258c679562cb6de57d9b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070659"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Oprette en arbejdsproces for køb og salg af orlov


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan oprette en arbejdsproces i Dynamics 365 Human Resources for at administrere anmodninger om køb og salg af orlov konsekvent. En arbejdsproces for **Køb og salg af orlov** giver dig mulighed for at:

- Definere opgaver
- Afgøre, hvem der skal udføre opgaverne
- Angive, hvem der kan godkende eller afvise anmodninger

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Oprette en arbejdsproces for køb og salg af orlov

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Arbejdsgange for Human Resources** under **Konfiguration**.

3. Vælg **Ny**, og vælg derefter **Anmodning om køb og salg af orlov**. 

4. Når meddelelsen **Åbn denne fil?** vises, skal du vælge **Åbn** og logge på med dit firmas legitimationsoplysninger.

5. Brug arbejdsgangseditoren til at oprette en arbejdsgang til orlovsanmodninger. Yderligere oplysninger om at arbejde med arbejdsgange finder du i [Oversigt over oprettelse af arbejdsgange](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Dataelementer for arbejdsgang for orlovs- og fraværsanmodninger

Du kan bruge følgende dataelementer til at oprette betingede eller automatiske godkendelser i arbejdsgange for anmodninger om køb og salg af orlov:

- **Beløb**
- **Politik for køb og salg af orlov**
- **Regnskab**
- **Oprettet af**
- **Dato og klokkeslæt for oprettelse**
- **Slutdato**
- **Orlovstype**
- **Ændret af**
- **Dato og klokkeslæt for ændring**
- **Anmodnings-id**
- **Igangsæt dato**
- **Status** 
- **Indsendelsesdato**
- **Sendt af**
- **Sendt af HR**
- **Sendt af leder**
- **Sendt på vegne af**
- **Arbejdstråd**

## <a name="workflow-examples"></a>Eksempler på arbejdsgange

Disse eksempler viser, hvordan du kan oprette forskellige typer betingelser for arbejdsgange via disse dataelementer:

- Brug **Sendt af HR** og **Sendt af leder** i en automatisk handling for at godkende anmodninger om for køb og salg af orlov automatisk, som disse roller sender på vegne af medarbejdere. Du kan finde flere oplysninger om automatiske handlinger under [Konfigurere godkendelsesprocesser i en arbejdsgang](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Brug **Orlovstype** i en betingelsessætning eller automatisk handling til at styre, hvordan arbejdsgangen sender anmodninger med bestemte orlovstyper.

## <a name="see-also"></a>Se også

[Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)<br>
[Administrere politikker for køb og salg af orlov](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[Køb og sælg orlov](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
