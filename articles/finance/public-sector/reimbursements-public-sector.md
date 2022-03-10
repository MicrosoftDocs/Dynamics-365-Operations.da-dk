---
title: Refusioner i den offentlige sektor
description: I dette emne besvares almindelige spørgsmål i forbindelse med refusioner i den offentlige sektor.
author: v-kiarnd
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustBillingClassification
audience: Application User
ms.reviewer: roschlom
ms.custom: 27311
ms.assetid: 9d61d1d8-1672-4bd0-ae0d-605b09240890
ms.search.region: Global
ms.search.industry: Public sector
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ed6f4925ed9045fe737210f8794c05de6dfec34
ms.sourcegitcommit: 52a6b038d42ab28092bb942c61f5196330db3a7b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2021
ms.locfileid: "7817689"
---
# <a name="reimbursements-in-the-public-sector"></a>Refusioner i den offentlige sektor

[!include [banner](../includes/banner.md)]

I dette emne besvares almindelige spørgsmål i forbindelse med refusioner i den offentlige sektor. 

## <a name="what-happens-if-i-create-a-separate-reimbursement-transaction-for-each-billing-classification"></a>Hvad sker der, hvis jeg opretter en separat refusionspostering for hver faktureringsklassifikation?

Når du opretter en separat refusionspostering for hver faktureringsklassifikation, samles kreditnotaposteringer, der er fordelt til den samme finanskonto, og som har samme faktureringsklassifikation til en enkelt refusionspostering. Der oprettes separate refusionsposteringer for kreditnotaposteringer, der er fordelt til den samme finanskonto, og som har forskellige faktureringsklassifikationer. Lad os f.eks. antage, du behandler refusioner til tre kreditnotaer. Alle tre kreditnotaer er $1000.

-   Første kreditnota har faktureringsklassifikation UTL, er fordelt på tre firmaer, med 15 % til konto 1110, 30 % til konto 2210 og 55 % til konto 3210.
-   Den anden kreditnota har også faktureringsklassifikation UTL. Den er distribueret 100 % til konto 3210.
-   Den tredje kreditnota med faktureringsklassifikationen GEN er distribueret 100 % til konto 1110.

Hvis du opretter en separat refusionspostering for hver faktureringsklassifikation, vil fire refusionsposteringer blive oprettet, på følgende måde:

-   $150 til konto 1110
-   $1000 til konto 1110
-   $300 til konto 2210
-   $1550 til konto 3210

De beløb, der går til konto 3210, kombineres, fordi de begge bruger samme faktureringsklassifikation. De beløb, der går til konto 1110, kombineres ikke, fordi de ikke bruger samme faktureringsklassifikation. Hvis du ikke opretter en separat refusion for hver faktureringsklassifikation, vil posteringerne for konto 1110 blive kombineret, og kun tre refusionsposteringer vil blive oprettet.

## <a name="how-do-billing-classifications-affect-reimbursements-for-overpayments"></a>Hvordan påvirker faktureringsklassifikationer refusioner for overbetalinger?
Det gør de ikke. Faktureringsklassifikationer anvendes aldrig til debitorbetalinger, så de bruges ikke ved behandling af refusioner for overbetalinger.

## <a name="can-i-process-a-reimbursement-for-a-customer-who-has-outstanding-debit-transactions"></a>Er det muligt at behandle en refusion til en kunde, der har udestående debiteringer?
Ja. Hvis du vil behandle en refusion for en kunde med udestående debiteringer, skal du bruge filtre på siden refusion til at vælge debitoren og vælge indstillingen for at medtage debitorer med udestående debiteringer. Når du gør dette, oprettes refusionsposteringer for det fulde beløb af alle kundens kreditposteringer. De udestående debetbeløb er ikke trukket fra kreditbeløbene.

## <a name="can-i-process-reimbursements-for-customers-who-have-pending-settlements"></a>Kan jeg ikke behandle refusioner for kunder, der har ventende udligninger?
Nej. Refusioner behandles ikke for en kunde, der har ventende udligninger, der ikke er blevet bogført til journalen.

## <a name="can-i-reverse-reimbursement-settlements"></a>Kan jeg fortryde refusionsudligninger?
Nej, ikke direkte. Du kan dog bruge finanskladdeposter til at oprette posteringer, der ville medføre tilbageførsel af finansposterne.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
