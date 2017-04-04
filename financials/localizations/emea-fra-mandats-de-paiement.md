---
title: Mandats de paiement i den offentlige sektor i Frankrig
description: "Mandat de paiement, der bruges af direktøren for at underrette bogholderen, organisationen er forpligtet til at betale et bestemt beløb til en anden enhed, og at tillade bogholder til at betale beløbet. Mandat vedligeholder stram separation, der skal bruges mellem direktøren operationelle rolle og rollen regnskab for bogholderen."
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

Mandat de paiement, der bruges af direktøren for at underrette bogholderen, organisationen er forpligtet til at betale et bestemt beløb til en anden enhed, og at tillade bogholder til at betale beløbet. Mandat vedligeholder stram separation, der skal bruges mellem direktøren operationelle rolle og rollen regnskab for bogholderen.

<a name="directors-tasks"></a>Direktørens opgaver
----------------

Fra den **Vedligehold mandats de paiement** siden direktør kan udføre følgende opgaver:

-   **Tildele et mandat de paiement fakturalinjer.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til et mandat, kan du filtrere de hentede linjer af den **Mandat** kolonne.
-   **Godkend betaling af fakturalinjer, der er tildelt mandats.** Dette kan også gøres fra den **Mandat de paiement** tab på siden kreditors faktura eller siden kreditors posteringer.
-   **Mandats tildeles en bordereau de mandat.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til en bordereau de mandat, kan du filtrere de hentede linjer af den **Bordereau de mandat** kolonne.
-   **Udstede en ordre på indkøbsrekvisitionen.** Tildele fakturalinjen til et nyt mandat, før de sendes til bogholderen som en ordre, en indkøbsrekvisition.

Hvis du vil sende mandats til bogholder til betaling, indsamler direktøren udskrevne mandats og relateret dokumentation herfor under en bordereau de mandat.

-   Udskrive mandats, der er tildelt til en bordereau fra den **poster der skal medtages** oversigtspanelet på den **Mandat de paiement rapport** side.
-   Udskrive bordereau fra den **poster der skal medtages** oversigtspanelet på den **Bordereau de mandat rapport** side.

## <a name="accountants-tasks"></a>Revisorens opgaver
Fra den **Vedligehold mandats de paiement** side eller fra den **Mandat de paiement** under fanen Kreditor ventende fakturaer eller åbne kreditorfakturaer side, at bogholderen kan acceptere, afvise eller holde mandats. Når et mandat er blevet afvist, direktør status ændres til **ikke gennemgået**, og mandat og bordereau de mandat nummer er fjernet.

## <a name="using-the-database-inquiry-page"></a>Ved hjælp af siden database-forespørgsel
Sådan åbnes siden database forespørgsel på den **Vedligehold mandats de paiement** skal du angive, om du vil arbejde med ventende eller bogførte fakturaer og hvilke datoer, du vil vælge fakturaer fra. Klik derefter på **hente linjer**. Dette åbner den **Database****undersøgelse** side, hvor du kan angive kriterierne, til de fakturalinjer, du vil hente. Når du lukker formen, hentes alle fakturalinjer, der opfylder de kriterier, der er valgt i gitteret. Linjer fra fakturaer, der er ved at blive redigeret, vil ikke kunne hentes. **Tip**: bruger følgende kriterier på siden database-forespørgsel til at hente linjerne.

-   Fakturalinjer, der ikke er gennemset af direktøren.
    | Tabellen  | Afledt tabel | Felt                         | Afgrænsning       |
    |--------|---------------|-------------------------------|----------------|
    | Mandat | Mandat        | Status for direktørgodkendelse | "Ikke gennemgået" |

-   Fakturalinjer fra mandats, der er godkendt til betaling af direktøren, men endnu ikke godkendt af bogholderen.
    | Tabellen  | Afledt tabel | Felt                         | Afgrænsning       |
    |--------|---------------|-------------------------------|----------------|
    | Mandat | Mandat        | Status for direktørgodkendelse | "Tilladelse"   |
    | Mandat | Mandat        | Bogholders acceptstatus  | "Ikke gennemgået" |

-   Fakturalinjer fra mandats, der afvises af bogholderen.
    | Tabellen  | Afledt tabel | Felt                        | Afgrænsning   |
    |--------|---------------|------------------------------|------------|
    | Mandat | Mandat        | Bogholders acceptstatus | "Afvist" |




