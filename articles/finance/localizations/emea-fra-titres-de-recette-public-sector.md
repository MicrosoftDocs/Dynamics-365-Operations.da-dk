---
title: Titres de recette i den offentlige sektor i Frankrig
description: Titres de recette bruges af direktøren til at underrette og autorisere bogholderen til at opkræve og deponere et specifikt beløb fra en anden enhed.
author: rschloma
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: kfend
ms.custom: 19931
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 888bacf65a5255e1186ebbf212b961f18cc6036cd53b09a1f44262cb60a97125
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725989"
---
# <a name="titres-de-recette-in-the-public-sector-in-france"></a>Titres de recette i den offentlige sektor i Frankrig

[!include [banner](../includes/banner.md)]

Direktøren bruger titres de recette til at underrette og autorisere bogholderen til at opkræve og deponere et specifikt beløb fra en anden enhed. Direktøren eller bogholderen kan delegere en repræsentant til at udføre opgaven. Ansvaret for hver opgave er dog stadig direktørens eller bogholderens. Titre opretholder en nødvendig stram adskillelse mellem direktørens operationelle rolle og bogholderens regnskabsrolle.

I Dynamics 365 Finance tildeles hver titre en enkelt fritekstfakturalinje. Denne tildeling garanterer, at hver titre kun vedrører én debitor og indeholder kun én konto i budgettet. En gruppe af relaterede titres sammen med al understøttende dokumentation tildeles til en bordereau de titre for afsendelse til bogholderen.

## <a name="directors-tasks"></a>Direktørens opgaver
Fra siden **Vedligehold titres de recette** kan direktøren udføre følgende opgaver:

-   **Tildele fakturalinjer til et titre de recette.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til et titre, ved at filtrere de hentede linjer efter kolonnen **Titre**.
-   **Godkende opkrævning af fakturalinjer, der er tildelt til titres.** Godkendelse kan også ske fra fanen **Titre de recette** på siden **Fritekstfaktura**.
-   **Tildele titres to a bordereau de titre.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til et Bordereau de titre, ved at bruge kolonnen **Bordereau de titre** til at filtrere de hentede linjer.

Hvis du vil sende titres til bogholderen til indbetaling, indsamler direktøren de udskrevne titres og relateret dokumentation under en borderau de titre.

-   Udskriv titres, der er tildelt til en bordereau, fra oversigtspanelet **Poster, der skal indgå** på siden **Titre de recette rapport**.
-   Udskriv bordereau fra oversigtspanelet **Poster, der skal indgå** på siden **Bordereau de titre rapport**.

## <a name="accountants-tasks"></a>Bogholderens opgaver
Fra siden **Vedligehold titres de recette** eller fra fanen **Titre de recette** på fritekstfakturasiden kan bogholderen acceptere, afvise eller spærre titeren. Når et titre afvises, ændres direktørstatus til Ikke gennemset. Tal for titre og bordereau de titre ryddes.

## <a name="using-the-database-inquiry-page"></a>Brug af Database-forespørgselssiden
Du kan åbne siden **Databaseforespørgsel** fra siden **Vedligehold titres de recette** ved at angive, hvilke datoer du vil vælge fakturaer fra. Klik derefter på **Hent linjer**. Siden **Databaseforespørgsel** åbnes, og her kan du angive kriterierne for de fakturalinjer, du vil hente. Når du lukker siden, hentes alle fakturalinjer, der opfylder de kriterier, der er valgt, til gitteret. Linjer fra fakturaer, der er ved at blive redigeret, kan ikke hentes. 

Brug følgende kriterier på databaseforespørgselssiden for at hente linjerne.

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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]