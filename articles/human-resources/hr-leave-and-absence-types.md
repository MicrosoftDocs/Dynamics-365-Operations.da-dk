---
title: Konfigurere orlovs- og fraværstyper
description: Konfigurer de orlovstyper, medarbejderne kan tage i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008526"
---
# <a name="configure-leave-and-absence-types"></a>Konfigurere orlovs- og fraværstyper

Orlovstyper i Dynamics 365 Human Resources bruges til at definere de forskellige typer fravær, som medarbejdere kan rapportere. Du kan skræddersy orlovstyper i henhold til organisationens behov. Eksempler på orlovstyper omfatter:

- Betalt fravær (PTO)
- Orlov uden løn
- Ferie med løn
- Sygeorlov
- Sygeorlov
- Forældreorlov
- Kortvarigt handicap
- Tjenestefrihed ved dødsfald

## <a name="add-a-leave-type"></a>Tilføje en orlovstype

1. På siden **Orlov og fravær** skal du vælge fanen **Links**.

2. Vælg **Orlovs- og fraværstyper** under **Konfiguration**.

3. Vælg **Ny**.

4. Angiv et navn til orlovstypen under **Type**, vælg en arbejdsgang fra **Arbejdsgangs-id**, og indtast en **Beskrivelse**.

5. I **Generelt** skal du vælge **Ingen**, **Planlagt** eller **Ikke planlagt** på rullelisten **Kategori**.

6. Vælg en lønkode på rullelisten **Lønkode**.

7. Under **Årsagskode skal angives** skal du vælge, om du vil kræve en årsagskode. Hvis du vil kræve årsagskoder, skal du muligvis tilføje dem. Under **Årsagskoder** skal du vælge **Tilføj**, vælge en årsagskode og derefter markere afkrydsningsfeltet **Aktiveret** ved siden af.

8. Under **Begræns adgangen til valgte roller** skal du vælge, om du vil begrænse adgangen. Vælg derefter sikkerhedsrollerne under **Sikkerhedsroller for denne orlovstype**. Sikkerhedsrollerne defineres i den arbejdsgang, du valgte under **Arbejdsgangs-id** tidligere i denne procedure.

9. Vælg **Gem**.

## <a name="configure-preview-features"></a>Konfigurere prøveversioner

Hvis du har aktiveret prøvefunktioner for orlov og fravær, skal du også konfigurere indstillingerne for dem.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Angiv afrundingsindstillinger for orlovstypen. Indstillingerne omfatter **Ingen**, **Op**, **Ned** og **Nærmeste**. Du kan også angive afrundingspræcision for orlovstypen.

2. Angiv **Helligdagskorrektion** for orlovstypen. Når du vælger denne indstilling, bruger Personale det antal helligdage, der falder på en arbejdsdag, til at bestemme, hvordan der skal periodiseres tid for orlovstypen. Hvis juledag f.eks. falder på en mandag, trækker Personale én dag fra orlovstypen ved behandling af periodiseringer.

   Du kan angive helligdage i arbejdstidskalenderen. Du kan finde flere oplysninger under [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)

## <a name="see-also"></a>Se også

- [Oversigt over orlov og fravær](hr-leave-and-absence-overview.md)
- [Oprette en orlovs- og fraværsplan](hr-leave-and-absence-plans.md)
- [Oprette en arbejdstidskalender](hr-leave-and-absence-working-time-calendar.md)