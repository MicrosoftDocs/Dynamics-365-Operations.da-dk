---
title: Titres de recette i den offentlige sektor i Frankrig
description: "Titre de recette bruges af direktøren for at underrette bogholderen om, at organisationen er berettiget til at indsamle et bestemt beløb fra en anden enhed, og til at godkende, at bogholderen indbetaler beløbet. Direktøren eller bogholderen kan delegere en repræsentant til at udføre opgaven, men ansvaret for hver opgave forbliver hos direktøren eller bogholderen. Titre opretholder en nødvendig stram adskillelse mellem direktørens operationelle rolle og bogholderens regnskabsrolle."
author: rschloma
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 19931
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b87d96dca92f3ef4e755e71649bd0b183f62f982
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="titres-de-recette-in-the-public-sector-in-france"></a>Titres de recette i den offentlige sektor i Frankrig

[!include [banner](../includes/banner.md)]

Titre de recette bruges af direktøren for at underrette bogholderen om, at organisationen er berettiget til at indsamle et bestemt beløb fra en anden enhed, og til at godkende, at bogholderen indbetaler beløbet. Direktøren eller bogholderen kan delegere en repræsentant til at udføre opgaven, men ansvaret for hver opgave forbliver hos direktøren eller bogholderen. Titre opretholder en nødvendig stram adskillelse mellem direktørens operationelle rolle og bogholderens regnskabsrolle.

I Microsoft Dynamics 365 for Finance and Operations er hver titre tildelt en enkelt fritekstfakturalinje. Dette garanterer, at hver titre kun vedrører én debitor og indeholder kun én konto i budgettet. En gruppe af relaterede titres sammen med al understøttende dokumentation tildeles til en bordereau de titre for afsendelse til bogholderen.

## <a name="directors-tasks"></a>Direktørens opgaver
Fra siden **Vedligehold titres de recette** kan direktøren udføre følgende opgaver:

-   **Tildele fakturalinjer til et titre de recette.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til et titre, ved at filtrere de hentede linjer efter kolonnen **Titre**.
-   **Godkende opkrævning af fakturalinjer, der er tildelt til titres.** Dette kan også gøres fra fanen **Titre de recette** på fritekstfakturasiden.
-   **Tildele titres to a bordereau de titre.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til et Bordereau de titre, ved at filtrere de hentede linjer efter kolonnen **Bordereau de titre**.

Hvis du vil sende titres til bogholderen til indbetaling, indsamler direktøren de udskrevne titres og relateret dokumentation under en borderau de titre.

-   Udskriv titres, der er tildelt til en bordereau, fra oversigtspanelet **Poster, der skal indgå** på siden **Titre de recette rapport**.
-   Udskriv bordereau fra oversigtspanelet **Poster, der skal indgå** på siden **Bordereau de titre rapport**.

## <a name="accountants-tasks"></a>Bogholderens opgaver
Fra siden **Vedligehold titres de recette** eller fra fanen **Titre de recette** på fritekstfakturasiden kan bogholderen acceptere, afvise eller spærre titeren. Når et titre er blevet afvist, ændres direktørstatus til Ikke gennemset, og titre- og bordereau de titre-numre fjernes.

## <a name="using-the-database-inquiry-page"></a>Brug af databaseforespørgselssiden
Du kan åbne databaseforespørgselssiden på siden **Vedligehold titres de recette** ved at angive, hvilke datoer du vil vælge fakturaer fra. Klik derefter på **Hent linjer**. Dette åbner databaseforespørgselssiden, hvor du kan angive kriterierne for de fakturalinjer, du vil hente. Når du lukker formularen, hentes alle fakturalinjer, der opfylder de kriterier, der er valgt, til gitteret. Linjer fra fakturaer, der er ved at blive redigeret, kan ikke hentes. **Tip**! Brug følgende kriterier på databaseforespørgselssiden for at hente linjerne.

- Fakturalinjer, der ikke er gennemset af direktøren.

  | Tabellen | Afledt tabel |             Felt             |    Afgrænsning    |
  |-------|---------------|-------------------------------|----------------|
  | Titre |     Titre     | Status for direktørgodkendelse | "Ikke gennemset" |


- Fakturalinjer fra titres, der er godkendt til opkrævning af direktøren, men endnu ikke godkendt af bogholderen.

  | Tabellen | Afledt tabel |             Felt             |    Afgrænsning    |
  |-------|---------------|-------------------------------|----------------|
  | Titre |     Titre     | Status for direktørgodkendelse |  "Godkendt"  |
  | Titre |     Titre     | Bogholders acceptstatus  | "Ikke gennemset" |


- Fakturalinjer fra titres, der er afvist af bogholderen.

  | Tabellen | Afledt tabel | Felt                        | Afgrænsning   |
  |-------|---------------|------------------------------|------------|
  | Titre | Titre         | Bogholders acceptstatus | "Afvist" |






