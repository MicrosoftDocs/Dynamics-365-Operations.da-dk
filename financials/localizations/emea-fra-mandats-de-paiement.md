---
title: Mandats de paiement i den offentlige sektor i Frankrig
description: "Mandat de paiement bruges af direktøren for at underrette bogholderen om, at organisationen er forpligtet til at betale et bestemt beløb til en anden enhed, og til at godkende, at bogholderen betaler beløbet. Mandatet opretholder en nødvendig stram adskillelse mellem direktørens operationelle rolle og bogholderens regnskabsrolle."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27231
ms.assetid: e63d4d9d-27d4-42c9-ad87-66040b8680db
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: f51eb98479dd48ca87ac40c4f2a9ec7a288228b9
ms.lasthandoff: 03/31/2017


---

# <a name="mandats-de-paiement-in-the-public-sector-in-france"></a>Mandats de paiement i den offentlige sektor i Frankrig

[!include[banner](../includes/banner.md)]


Mandat de paiement bruges af direktøren for at underrette bogholderen om, at organisationen er forpligtet til at betale et bestemt beløb til en anden enhed, og til at godkende, at bogholderen betaler beløbet. Mandatet opretholder en nødvendig stram adskillelse mellem direktørens operationelle rolle og bogholderens regnskabsrolle.

<a name="directors-tasks"></a>Direktørens opgaver
----------------

Fra siden **Vedligehold mandats paiement** kan direktør udføre følgende opgaver:

-   **Tildele fakturalinjer til et mandat de paiement.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til et mandat, ved at filtrere de hentede linjer efter kolonnen **Mandat**.
-   **Godkende betaling af fakturalinjer, der er tildelt til mandater.** Dette kan også gøres fra fanen **Mandat de paiement** på kreditorfakturasiden eller kreditorposteringssiden.
-   **Tildele mandater til en bordereau de mandat.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til et Bordereau de mandat, ved at filtrere de hentede linjer efter kolonnen **Bordereau de mandat**.
-   **Udstede en rekvisitionsordre.** Tildel fakturalinjen til et nyt mandat, før den sendes til bogholderen som en rekvisitionsordre.

Hvis du vil sende mandater til bogholderen til betaling, indsamler direktøren de udskrevne mandater og relateret dokumentation under en bordereau de mandat.

-   Udskriv mandater, der er tildelt til en bordereau, fra oversigtspanelet **Poster, der skal indgå** på siden **Mandat de paiement rapport**.
-   Udskriv bordereau fra oversigtspanelet **Poster, der skal indgå** på siden **Bordereau de mandat rapport**.

## <a name="accountants-tasks"></a>Bogholderens opgaver
Fra siden **Vedligehold mandats de paiement** eller fra fanen **Mandat de paiement** på siden for ventende kreditorfakturaer eller åbne kreditorfakturaer kan bogholderen acceptere eller afvise mandats eller sætte dem på hold. Når et mandat er blevet afvist, ændres direktørstatus til **Ikke gennemset**, og mandat- og bordereau de mandat-numre fjernes.

## <a name="using-the-database-inquiry-page"></a>Brug af databaseforespørgselssiden
For at åbne databaseforespørgselssiden skal du på siden **Vedligehold mandats de paiement** angive, om du vil arbejde med ventende eller bogførte fakturaer og hvilke datoer, du vil vælge fakturaer fra. Klik derefter på **Hent linjer**. Dette åbner siden **Database****forespørgsel**, hvor du kan angive kriterierne for de fakturalinjer, du vil hente. Når du lukker formularen, hentes alle fakturalinjer, der opfylder de kriterier, der er valgt, til gitteret. Linjer fra fakturaer, der er ved at blive redigeret, kan ikke hentes. **Tip**! Brug følgende kriterier på databaseforespørgselssiden for at hente linjerne.

-   Fakturalinjer, der ikke er gennemset af direktøren.
    | Tabellen  | Afledt tabel | Felt                         | Afgrænsning       |
    |--------|---------------|-------------------------------|----------------|
    | Mandat | Mandat        | Status for direktørgodkendelse | "Ikke gennemset" |

-   Fakturalinjer fra mandats, der er godkendt til betaling af direktøren, men endnu ikke godkendt af bogholderen.
    | Tabellen  | Afledt tabel | Felt                         | Afgrænsning       |
    |--------|---------------|-------------------------------|----------------|
    | Mandat | Mandat        | Status for direktørgodkendelse | "Godkendt"   |
    | Mandat | Mandat        | Bogholders acceptstatus  | "Ikke gennemset" |

-   Fakturalinjer fra mandats, der er afvist af bogholderen.
    | Tabellen  | Afledt tabel | Felt                        | Afgrænsning   |
    |--------|---------------|------------------------------|------------|
    | Mandat | Mandat        | Bogholders acceptstatus | "Afvist" |






