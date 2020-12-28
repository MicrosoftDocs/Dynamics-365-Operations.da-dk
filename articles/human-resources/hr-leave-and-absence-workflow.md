---
title: Oprette en arbejdsgang for orlovsanmodninger
description: Opret en arbejdsgang for orlovs- og fraværsanmodninger for at administrere anmodninger om orlov i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
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
ms.openlocfilehash: 209f0ec7236778cc0a828102e554b02206b45b73
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417744"
---
# <a name="create-a-leave-request-workflow"></a>Oprette en arbejdsgang for orlovsanmodninger

Du kan oprette en arbejdsgang i Dynamics 365 Human Resources for at administrere orlovs- og fraværsanmodninger konsekvent. En **Orlovs- og fraværsarbejdsgang** giver dig mulighed for at:

- Definere opgaver
- Afgøre, hvem der skal udføre opgaverne
- Angive, hvem der kan godkende eller afvise anmodninger

## <a name="create-a-leave-and-absence-request-workflow"></a>Oprette en arbejdsgang for orlovs- og fraværsanmodninger

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Arbejdsgange for Personale** under **Konfiguration**.

3. Vælg **Ny**, og vælg derefter **Anmodning om orlov og fravær**. 

4. Når meddelelsen **Åbn denne fil?** vises, skal du vælge **Åbn** og logge på med dit firmas legitimationsoplysninger.

5. Brug arbejdsgangseditoren til at oprette en arbejdsgang til orlovsanmodninger. Yderligere oplysninger om at arbejde med arbejdsgange finder du i [Oversigt over oprettelse af arbejdsgange](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

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

- Brug **Årsagskode** i en betingelsessætning til at sende orlovsanmodninger for sygefravær med årsagskoden **Kirurgi** til HR mht. godkendelse – andre årsagskoder sendes til lederen. Du kan finde flere oplysninger om betingelsessætninger under [Konfigurere betingede beslutninger i en arbejdsgang](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow). 

- Brug **Sendt af HR** og **Sendt af leder** i en automatisk handling for at godkende orlovsanmodninger automatisk, som disse roller sender på vegne af medarbejdere. Du kan finde flere oplysninger om automatiske handlinger under [Konfigurere godkendelsesprocesser i en arbejdsgang](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- Brug **Orlovstype** i en betingelsessætning eller automatisk handling til at styre, hvordan arbejdsgangen sender anmodninger med bestemte orlovstyper.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
