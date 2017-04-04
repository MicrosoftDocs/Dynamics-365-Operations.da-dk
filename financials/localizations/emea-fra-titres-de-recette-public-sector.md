---
title: Titres de recette i den offentlige sektor i Frankrig
description: "Titer de recette bruges af direktøren for at underrette bogholderen, at organisationen er berettiget til at indsamle et bestemt beløb fra en anden enhed og at tillade, at bogholderen til at indbetale beløbet. Direktøren eller bogholderen kan uddelegere en repræsentant til at udføre opgaven, men ansvaret for hver opgave forbliver med direktøren eller bogholderen. Titeren vedligeholder stram separation, der skal bruges mellem direktøren operationelle rolle og rollen regnskab for bogholderen."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19931
ms.assetid: 01d7ba2b-32b7-43aa-8edb-7a2ed700363a
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 17896328b0ba056650da7f882cc2c5a3334d5100
ms.lasthandoff: 03/31/2017


---

# <a name="titres-de-recette-in-the-public-sector-in-france"></a>Titres de recette i den offentlige sektor i Frankrig

Titer de recette bruges af direktøren for at underrette bogholderen, at organisationen er berettiget til at indsamle et bestemt beløb fra en anden enhed og at tillade, at bogholderen til at indbetale beløbet. Direktøren eller bogholderen kan uddelegere en repræsentant til at udføre opgaven, men ansvaret for hver opgave forbliver med direktøren eller bogholderen. Titeren vedligeholder stram separation, der skal bruges mellem direktøren operationelle rolle og rollen regnskab for bogholderen.

I Microsoft Dynamics 365 for operationer, er hver titer tildelt en enkelt fritekstfakturalinje. Dette garanterer, at hver titer vedrører kun én debitor, og indeholder kun én konto i budgettet. En gruppe af relaterede titres sammen med alle dokumentation er tildelt en bordereau de titer for afsendelse til bogholderen.

## <a name="directors-tasks"></a>Direktørens opgaver
Fra den **Vedligehold titres de recette** siden direktør kan udføre følgende opgaver:

-   **Tildele en titer de recette fakturalinjer.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til en titer, kan du filtrere de hentede linjer af den **titer** kolonne.
-   **Tillade fakturalinjer, der er tildelt titres samling.** Dette kan også gøres fra den **titer de recette** tab på siden fritekst-faktura.
-   **Tildele en bordereau de titer titeren.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til en bordereau de titer, kan du filtrere de hentede linjer af den **Bordereau de titer** kolonne.

For at sende titres til bogholder for indbetalingen, indsamler direktøren udskrevne titeren og deres relateret dokumentation under en borderau de titer.

-   Udskrive titeren tildelt en bordereau fra den **poster der skal medtages** oversigtspanelet på den **titer de recette rapport** side.
-   Udskrive bordereau fra den **poster der skal medtages** oversigtspanelet på den **Bordereau de titer rapport** side.

## <a name="accountants-tasks"></a>Revisorens opgaver
Fra den **Vedligehold titres de recette** side eller fra den **titer de recette** tab på fritekst faktura siden bogholderen kan acceptere, afvise eller holde titeren. Når en titer afvises, direktør status ændres til ikke gennemset, og titer og bordereau de titer-numre er fjernet.

## <a name="using-the-database-inquiry-page"></a>Ved hjælp af siden database-forespørgsel
Sådan åbnes siden database forespørgsel på den **Vedligehold titres de recette** skal du angive, hvilke datoer, du vil vælge fakturaer fra. Klik derefter på **hente linjer**. Dette åbner siden database forespørgsel, hvor du kan angive kriterier for de fakturalinjer, der skal hentes. Når du lukker formen, hentes alle de fakturalinjer, der opfylder de kriterier, der er valgt i gitteret. Linjer fra de fakturaer, der er ved at blive redigeret, vil ikke kunne hentes. **Tip**: bruger følgende kriterier på siden database-forespørgsel til at hente linjerne.

-   Fakturalinjer, der ikke er gennemset af direktøren.
    | Tabellen | Afledt tabel | Felt                         | Afgrænsning       |
    |-------|---------------|-------------------------------|----------------|
    | Titre | Titre         | Status for direktørgodkendelse | "Ikke gennemgået" |

-   Fakturalinjer fra titres, der er godkendt til samling af direktøren, men endnu ikke godkendt af bogholderen.
    | Tabellen | Afledt tabel | Felt                         | Afgrænsning       |
    |-------|---------------|-------------------------------|----------------|
    | Titre | Titre         | Status for direktørgodkendelse | "Tilladelse"   |
    | Titre | Titre         | Bogholders acceptstatus  | "Ikke gennemgået" |

-   Fakturalinjer fra titres, der afvises af bogholderen.
    | Tabellen | Afledt tabel | Felt                        | Afgrænsning   |
    |-------|---------------|------------------------------|------------|
    | Titre | Titre         | Bogholders acceptstatus | "Afvist" |




