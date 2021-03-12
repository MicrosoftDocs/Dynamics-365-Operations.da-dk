---
title: Mandats de paiement i den offentlige sektor i Frankrig
description: Mandat de paiement bruges af direktøren til at underrette og autorisere bogholderen til at betale et specifikt beløb til en anden enhed.
author: rschloma
manager: AnnBe
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 27231
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e142c118371f39d3c7f1b7ffab4f26b9c50b649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002945"
---
# <a name="mandats-de-paiement-in-the-public-sector-in-france"></a>Mandats de paiement i den offentlige sektor i Frankrig

[!include [banner](../includes/banner.md)]

Mandat de paiement bruges af direktøren til at underrette og autorisere bogholderen til at betale et specifikt beløb til en anden enhed. Mandatet opretholder en nødvendig stram adskillelse mellem direktørens operationelle rolle og bogholderens regnskabsrolle.

## <a name="directors-tasks"></a>Direktørens opgaver

Fra siden **Vedligehold mandats paiement** kan direktør udføre følgende opgaver:

-   **Tildele fakturalinjer til et mandat de paiement.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til et mandat, ved at bruge kolonnen **Mandat** til at filtrere de hentede linjer.
-   **Godkende betaling af fakturalinjer, der er tildelt til mandater.** Betalinger kan også godkendes fra fanen **Mandat de paiement** på siden **Kreditorfaktura** eller siden **Kreditorposteringer**.
-   **Tildele mandater til en bordereau de mandat.** Du kan finde de fakturalinjer, der endnu ikke er tildelt til et Bordereau de mandat, ved at filtrere de hentede linjer efter kolonnen **Bordereau de mandat**.
-   **Udstede en rekvisitionsordre.** Tildel fakturalinjen til et nyt mandat, før den sendes til bogholderen som en rekvisitionsordre.

Hvis du vil sende mandater til bogholderen til betaling, indsamler direktøren de udskrevne mandater og relateret dokumentation under en bordereau de mandat.

-   Udskriv mandater, der er tildelt til en bordereau, fra oversigtspanelet **Poster, der skal indgå** på siden **Mandat de paiement rapport**.
-   Udskriv bordereau fra oversigtspanelet **Poster, der skal indgå** på siden **Bordereau de mandat rapport**.

## <a name="accountants-tasks"></a>Bogholderens opgaver
Bogholderen kan acceptere, afvise eller sætte mandats på hold på følgende placeringer:

  - Siden **Vedligehold mandats de paiement**
  - Siden **Ventende kreditorfakturaer** under fanen **Mandat de paiement**  
  - Siden **Åbne kreditorfakturaer** under fanen **Mandat de paiement**
  
Når et mandat afvises, ændres direktørstatus til **Ikke gennemset**. Tal for mandat og bordereau de mandat ryddes.

## <a name="using-the-database-inquiry-page"></a>Brug af Database-forespørgselssiden
For at åbne siden **Databaseforespørgsel** skal du på siden **Vedligehold mandats de paiement** angive, om du vil arbejde med ventende eller bogførte fakturaer. Angiv det datointerval, du vil vælge fakturaer fra, og vælg derefter **Hent linjer**. Siden **Databaseforespørgsel** åbnes, og her kan du angive kriterierne for de fakturalinjer, du vil hente. Når du lukker siden, hentes alle fakturalinjer, der opfylder de kriterier, der er valgt, til gitteret. Linjer fra fakturaer, der er ved at blive redigeret, kan ikke hentes. 

Brug følgende kriterier på databaseforespørgselssiden for at hente linjerne.

- Fakturalinjer, der ikke er gennemset af direktøren.

  | Tabellen  | Afledt tabel |             Felt             |    Afgrænsning    |
  |--------|---------------|-------------------------------|----------------|
  | Mandat |    Mandat     | Status for direktørgodkendelse | "Ikke gennemset" |


- Fakturalinjer fra mandats, der er godkendt til betaling af direktøren, men endnu ikke godkendt af bogholderen.

  | Tabellen  | Afledt tabel |             Felt             |    Afgrænsning    |
  |--------|---------------|-------------------------------|----------------|
  | Mandat |    Mandat     | Status for direktørgodkendelse |  "Godkendt"  |
  | Mandat |    Mandat     | Bogholders acceptstatus  | "Ikke gennemset" |


- Fakturalinjer fra mandats, der er afvist af bogholderen.

  | Tabellen  | Afledt tabel | Felt                        | Afgrænsning   |
  |--------|---------------|------------------------------|------------|
  | Mandat | Mandat        | Bogholders acceptstatus | "Afvist" |





