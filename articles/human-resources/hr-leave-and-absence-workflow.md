---
title: Oprette en arbejdsgang for orlovsanmodninger
description: Opret en arbejdsgang for orlovs- og fraværsanmodninger for at administrere anmodninger om orlov i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4ce8d0a121e2fa24e3c221a30eb13debd6e44ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855080"
---
# <a name="create-a-leave-request-workflow"></a>Oprette en arbejdsproces for orlovsanmodning

> [!Important]
> De funktioner, der nævnes i denne artikel, er i øjeblikket tilgængelige for kunder med enkeltstående Dynamics 365 Human Resources. Nogle eller alle funktionerne vil være tilgængelige som en del af en fremtidig version af Finance-infrastrukturen efter Finance-frigivelse 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan oprette en arbejdsgang i Dynamics 365 Human Resources for at administrere orlovs- og fraværsanmodninger konsekvent. En **Orlovs- og fraværsarbejdsgang** giver dig mulighed for at:

- Definere opgaver
- Afgøre, hvem der skal udføre opgaverne
- Angive, hvem der kan godkende eller afvise anmodninger

## <a name="create-a-leave-and-absence-request-workflow"></a>Oprette en arbejdsgang for orlovs- og fraværsanmodninger

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Arbejdsgange for Human Resources** under **Konfiguration**.

3. Vælg **Ny**, og vælg derefter **Anmodning om orlov og fravær**. 

4. Når meddelelsen **Åbn denne fil?** vises, skal du vælge **Åbn** og logge på med dit firmas legitimationsoplysninger.

5. Brug arbejdsgangseditoren til at oprette en arbejdsgang til orlovsanmodninger. Yderligere oplysninger om at arbejde med arbejdsgange finder du i [Oversigt over oprettelse af arbejdsgange](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Dataelementer for arbejdsgang for orlovs- og fraværsanmodninger

Du kan bruge følgende dataelementer til at oprette betingede eller automatiske godkendelser i arbejdsgange for orlovs- og fraværsanmodninger:

- **Beløb**
- **Kommentar**
- **Regnskab**
- **Oprettet af**
- **Dato og klokkeslæt for oprettelse**
- **Slutdato**
- **Orlovstype**
- **Ændret af**
- **Dato og klokkeslæt for ændring**
- **Årsagskode**
- **Anmodnings-id**
- **Igangsæt dato**
- **Status** 
- **Indsendelsesdato**
- **Sendt af**
- **Sendt af HR**
- **Sendt af leder**
- **Sendt på vegne af**
- **Arbejdstråd**
- **Arbejdertype**

Disse eksempler viser, hvordan du kan oprette forskellige typer betingelser for arbejdsgange via disse dataelementer:

- Brug **Årsagskode** i en betingelsessætning til at sende orlovsanmodninger for sygefravær med årsagskoden **Kirurgi** til HR mht. godkendelse – andre årsagskoder sendes til lederen. Du kan finde flere oplysninger om betingelsessætninger under [Konfigurere betingede beslutninger i en arbejdsgang](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Brug **Sendt af HR** og **Sendt af leder** i en automatisk handling for at godkende orlovsanmodninger automatisk, som disse roller sender på vegne af medarbejdere. Du kan finde flere oplysninger om automatiske handlinger under [Konfigurere godkendelsesprocesser i en arbejdsgang](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Brug **Orlovstype** i en betingelsessætning eller automatisk handling til at styre, hvordan arbejdsgangen sender anmodninger med bestemte orlovstyper.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
