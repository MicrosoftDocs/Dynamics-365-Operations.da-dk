---
title: Periodiser orlovs- og fraværsplaner
description: Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba60fc2e5b17ec32aa6ad7eb104e8ae55ddee3bb
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092332"
---
# <a name="accrue-leave-and-absence-plans"></a>Periodiser orlovs- og fraværsplaner

Du kan periodisere orlov og fravær Dynamics 365 Human Resources for flere medarbejdere eller for en enkelt person.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Periodisere orlov og fravær for flere medarbejdere

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Under **Administrer orlov** skal du vælge **Periodiser orlovs- og fraværsplaner**.

3. Vælg enten **Dags dato**, eller vælg **Brugerdefineret dato** i **Periodisering pr.** i dialogboksen **Periodiser orlovs- og fraværsplaner**, og angiv en brugerdefineret dato.

4. Hvis du vil køre periodiseringsprocessen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

   1. Angiv oplysninger om periodiseringsprocessen.

   2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.

   3. Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.

   4. Vælg **OK**. Periodiseringsprocessen køres med de parametre, du angiver.

## <a name="accrue-leave-and-absence-for-an-employee"></a>Periodisere orlov og fravær for en medarbejder

1. Vælg **Orlov**i medarbejderens post.

2. Vælg **Periodiser orlovs- og fraværsplaner**.

3. Vælg enten **Dags dato**, eller vælg **Brugerdefineret dato** i **Periodisering pr.** i dialogboksen **Periodiser orlovs- og fraværsplaner**, og angiv en brugerdefineret dato.

4. Hvis du vil køre periodiseringsprocessen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:

   1. Angiv oplysninger om periodiseringsprocessen.

   2. Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.

   3. Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.

   4. Vælg **OK**. Periodiseringsprocessen køres med de parametre, du angiver.

## <a name="preview-features-for-leave-and-absence"></a>Visningsfunktioner for orlov og fravær

[!include [banner](includes/preview-feature-leave-absence.md)]

Du kan aktivere følgende visningsfunktioner for orlov og fravær:

- **Slet periodiseringer af orlovs- og fraværsplaner**. Slet periodiseringsposter for en specifik plan og et bestemt datointerval. Periodiseringsdatoer skal være dateret i dag eller i fremtiden.

- **Revision af orlovsperiodisering**. Viser, hver gang en person kører eller sletter en periodisering for en eller flere medarbejdere, sammen med datoen og, hvem der udførte handlingen.

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
- [Oprette en orlovs- og fraværsplan](hr-leave-and-absence-plans.md)