---
title: Titres de recette i den offentlige sektor i Frankrig
description: Titres de recette bruges af direktøren til at underrette og autorisere bogholderen til at opkræve og deponere et specifikt beløb fra en anden enhed.
author: brpotter
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: France
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 19931
ms.search.industry: Public sector
ms.search.form: CustFreeInvoice
ms.openlocfilehash: 1335157c451aa9d080b1de44037dac6649d54fd0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268550"
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
