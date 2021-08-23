---
title: Oprette en teamkalender
description: Få vist og opret teamkalendere i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ccbf12d4dcc75e22fc62c356653a91b9a8a8d1761ccefb18c93e65f343250830
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744220"
---
# <a name="view-team-and-company-calendars"></a>Vis team- og firmakalendere

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan få vist team- og firmakalendere i Dynamics 365 Human Resources. Teamkalendere viser kun direkte underordnede som defineret i linjehierarkiet.

## <a name="view-your-team-calendar-as-an-employee"></a>Få vist din teamkalender som medarbejder

- Vælg **Teamfraværskalender** under **Oversigt** i arbejdsområdet **Medarbejderselvbetjening**.

## <a name="view-your-team-calendar-as-a-manager"></a>Få vist din teamkalender som leder

1. Vælg **Mit team** i arbejdsområdet **Medarbejderselvbetjening**.

2. Vælg **Orlov og fravær**, og vælg derefter **Vis cheffraværskalender**.

Ledere kan også få adgang til teamkalenderen fra **Afventer anmodninger om fridage for mit team**, **Godkendt fritid** og **Anmodninger om fridage**. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Få vist kalender for fraværsadministrator som fraværsadministrator

> [!NOTE]
> Hvis du vil se kalenderen for fraværsadministrator, skal du først aktivere funktionen **(Forhåndsversion) Fraværsadministrator, der administrerer orlov** i Funktionsstyring. Du kan få flere oplysninger om aktivering af prøveversionsfunktioner under [Administrere funktioner](hr-admin-manage-features.md).

Brugere i rollen Fraværsadministrator kan få vist anmodninger om fridage i kalenderen. Følg disse trin for at få adgang til orlovskalenderen.

1. I arbejdsområdet **Medarbejderselvbetjening** skal du vælge **Orlovsstyring** og derefter **Kalender for fraværsadministratorer**.

2. Angiv de ønskede datoer i feltet **Dato**.

3. Opdater visningsindstillingerne efter behov.

Kalenderen for fraværsadministratorer viser alle poster for de medarbejdere, der rapporterer til fraværsadministratoren i orlovshierarkiet.

## <a name="view-a-company-calendar"></a>Få vist en firmakalender

Personer, der har HR-roller, kan få vist firmakalendere. I firmakalendere vises alle medarbejdere. Kalenderen viser som standard dags dato plus 28 dage, men du kan ændre datointervallet. Du kan også filtrere kalenderen efter **Navn**, **Personalenummer** og **Orlovstype.**

1. Vælg **Links** i arbejdsområdet **Orlov og fravær**.

2. Vælg **Orlovs- og fraværskalender**.

Human Resources-roller kan også få adgang til firmakalenderen fra **Orlovs- og fraværsanmodninger**, **Godkendt fritid** og **Anmodninger om fridage**. 

Kalenderne indeholder nu yderligere filtre og indstillinger. Alle kalendere indeholder visningsindstillinger for:

- Godkendte anmodninger
- Ventende anmodninger
- Medarbejdere med orlovsanmodninger
- Medarbejdere uden orlovsanmodninger
- Medarbejdernes fødselsdage
- Anmodninger om fri 
- Orlovsanmodninger

Kalenderkonfiguration i orlovs- og fraværsparametre bestemmer tilgængelige visningsindstillinger.

Du kan også filtrere kalendere efter leder eller afdeling. Den primære stillingstildeling bestemmer, hvilke medarbejdere der vises, når disse filtre angives. 

> [!IMPORTANT]
> Du kan aktivere funktionen **Orlovsvisning på tværs af virksomheder** i Funktionsstyring. Derefter skal du aktivere funktionen på siden **Delte parametre for personale** for at vise filteret for juridiske enheder i kalendere. Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværsparametre](hr-leave-and-absence-parameters.md).
> 
> Du kan filtrere kalenderen efter juridisk enhed. Hvis du vil se alle medarbejdere uanset juridisk enhed, skal du fjerne markeringen i filtreringsfeltet og derefter vælge **Angiv**. 

Du kan få flere oplysninger om kalenderindstillinger i [Konfigurere kalenderparametre](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
