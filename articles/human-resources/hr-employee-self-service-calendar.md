---
title: Oprette en teamkalender
description: Få vist og opret teamkalendere i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 11/02/2020
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
ms.openlocfilehash: cedff4031c6455b446af9c56a770a00f3b2efc80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052091"
---
# <a name="view-team-and-company-calendars"></a>Vis team- og firmakalendere

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan få vist team- og firmakalendere i Dynamics 365 Human Resources. Teamkalendere viser kun direkte underordnede som defineret i linjehierarkiet.

## <a name="view-your-team-calendar-as-an-employee"></a>Få vist din teamkalender som medarbejder

1. Vælg **Teamfraværskalender** under **Oversigt** i arbejdsområdet **Medarbejderselvbetjening**.

## <a name="view-your-team-calendar-as-a-manager"></a>Få vist din teamkalender som leder

1. Vælg **Mit team** i arbejdsområdet **Medarbejderselvbetjening**.

2. Vælg **Orlov og fravær**, og vælg derefter **Vis cheffraværskalender**.

Ledere kan også få adgang til teamkalenderen fra **Afventer anmodninger om fridage for mit team**, **Godkendt fritid** og **Anmodninger om fridage**. 

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

>[!IMPORTANT]
>Visning af orlov og fravær på tværs af firmaer er i øjeblikket i prøveversion. Du skal aktivere den i dit **Sandkasse**-miljø. Du kan finde flere oplysninger om aktivering af prøveversionsfunktioner i [Administrere funktioner](hr-admin-manage-features.md).<br><br>
>Derefter skal du aktivere funktionen i **Delte parametre for personale** for at få vist filteret for juridiske enheder i kalendere. Du kan finde flere oplysninger i [Konfigurere orlovs- og fraværsparametre](hr-leave-and-absence-parameters.md).<br><br>
>Du kan filtrere kalenderen efter juridisk enhed. Hvis du vil se alle medarbejdere uanset juridisk enhed, skal du fjerne markeringen i filtreringsfeltet og vælge Angiv. 

Du kan få flere oplysninger om kalenderindstillinger i [Konfigurere kalenderparametre](hr-leave-and-absence-parameters.md?configure-calendar-parameters).



[!INCLUDE[footer-include](../includes/footer-banner.md)]