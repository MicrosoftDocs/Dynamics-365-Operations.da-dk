---
title: Fakturastyring til B2B-e-handelswebsteder
description: Dette emne beskriver funktionerne for fakturastyring i Microsoft Dynamics 365 Commerce business-to-business (B2B)-e-handelswebsteder.
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c1f0cc6820063a9a87e79fd6df25c7cffc01e228
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312568"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>Fakturastyring til B2B-e-handelswebsteder

[!include [banner](../../includes/banner.md)]

Dette emne beskriver funktionerne for fakturastyring i Microsoft Dynamics 365 Commerce business-to-business (B2B)-e-handelswebsteder.

Det er almindelig praksis, at firmaer, der håndterer B2B-transaktioner, accepterer ordrer på kundekredit og derefter sender en faktura til kunderne, når de har opfyldt ordren. Der er defineret betalingsbetingelser for kunder, og der kan være visse rabatter, der kan være med til at motivere kunderne til at betale til tiden eller før. For at øge sandsynligheden for, at betalinger vil blive modtaget til tiden, giver B2B-e-handelswebsteder kunderne mulighed for at se alle deres fakturaer. Kunden kan nemt filtrere fakturaerne for at få vist betalte, ubetalte og delvist betalte fakturaer sammen med forfaldsdatoerne.

![Siden Fakturaer på et B2B-websted.](../media/ViewInvoices.png)

> [!NOTE]
> En bruger, der er logget på, kan kun se og betale sine egne fakturaer. Hvis en organisationskonto er konfigureret på rullemenuen **Fakturakonto** i oversigtspanelet **Faktura og levering** for debitorposten i Commerce-hovedkontoret, vil brugeren kunne se og betale fakturaer for organisationskontoen.

På siden **Fakturaer** på et B2B-websted kan en bruger vælge en ubetalt eller delvist betalt faktura og derefter vælge **Betal faktura**. Den valgte faktura føjes til indkøbsvognen, og brugeren kan fortsætte med betalingen. Brugeren kan derefter beslutte, om fakturabeløbet skal betales fuldt ud eller en del af beløbet. Betalingsmetoden aconto kan ikke bruges til at betale for fakturaer.

> [!NOTE]
> Fakturaer kan kun føjes til indkøbsvognen, hvis der i øjeblikket ikke er nogen varer i den. Omvendt kan varer kun føjes til indkøbsvognen, hvis der i øjeblikket ikke er nogen fakturaer i den. Microsoft planlægger at fjerne denne begrænsning i fremtidige Commerce-versioner.

![Indkøbsvognsside på et B2B-websted.](../media/PayInvoice.png)

På siden **Fakturaer** kan en bruger også vælge **Anmod om faktura** ud for en faktura. På den måde kan brugeren anmode om, at fakturaoplysningerne sendes til den registrerede mailadresse.

![Dialogboksen Anmod om faktura.](../media/RequestInvoice2.png)

Når en bruger anmoder om en faktura, flyttes anmodningen til sektionen **B2B-anmodninger** på siden **Min konto**. Når **P-0001** og **Synkroniser ordrer og kanalanmodninger** derefter køres i Commerce-hovedkontoret, udløses fakturamailen, og statussen for B2B-anmodningen markeres som fuldført.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
