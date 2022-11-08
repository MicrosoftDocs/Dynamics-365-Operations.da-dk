---
title: Referencekoder til fejl i betalingsmodulet
description: Denne artikel beskriver referencekoder for fejl i betalingsmodulet, der vises som fejlmeddelelser for brugeren i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 952cb932522b4e0bb91be985e4f8974cb6cd8bc0
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728239"
---
# <a name="checkout-module-error-reference-codes"></a>Referencekoder til fejl i betalingsmodulet

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikel beskriver fejlkoder i betalingsmodulet, der vises som fejlmeddelelser for brugeren i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce har indført standardfejlreferencer, der kan inkluderes i fejl ved betaling via onlinekanal, som vises for onlinekunder. I Commerce version 10.0.31 og senere indeholder fejlmeddelelser i betalingsmodulet fejlkoder, og de viser ikke unødvendige oplysninger for onlinekunden. Fejlkoderne refererer til fejl, der er beskrevet i denne artikel.

Afhængigt af den fejl, der opstår, indeholder tabellen i denne artikel følgende oplysninger:

- En beskrivelse af den betingelse, der forårsagede fejlen, eller flere oplysninger
- Oplysninger, der skal overvejes i konfigurationer af miljøet eller betalings-connector
- Oplysninger, der kan refereres til i en supportsag, hvis der kræves yderligere hjælp

## <a name="prerequisites"></a>Forudsætninger

Hvis du vil aktivere referencekoder for fejl i modulet til betaling ved kassen, skal du gå til **Indstillinger for websted \> Udvidelser**, og i sektionen **Indkøbsvogn og betaling** skal du vælge **Aktivér udvidet visning af fejlmeddelelser i onlinekanal**. 

## <a name="checkout-module-error-reference-codes"></a>Referencekoder til fejl i betalingsmodulet

Du kan bruge tabellen nedenfor til at få flere detaljer om fejlkodereferencer, der leveres af kunder eller opleves i onlinebutikken. Rul til højre for at få vist kolonnen **Fejlbeskrivelse**.

| Fejlkode | Dynamics-korreleret fejlkode | Fejlbeskrivelse |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | Betalingen blev ikke godkendt. Korttype-id'et i **TokenizedPaymentCard** mangler, eller det angivne korttype-id understøttes ikke. |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | Afvist. Betalingen blev ikke godkendt. |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | Betalingen blev ikke godkendt. Der kræves flere oplysninger fra kunden. |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | Et eller andet gik galt. Resultatet af accepten af kortbetalingen kunne ikke anskaffes. Prøv igen, eller kontakt systemadministratoren. |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | Betalingen kunne ikke foretages på grund af manglende egenskaber for forhandlerbetaling. Kontakt din systemadministrator. |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | Det var ikke muligt at hente betalingsmiddeltjenesten for operationen. Kontrollér opsætningen af betalingsmåde for den valgte betalingsmiddeltype. |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | Der er allerede anvendt en kundekontobetaling, og kun én betaling er tilladt pr. transaktion. |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | Debitorkontogrænsen er forskellig fra det skyldige beløb. Prøv en anden betalingsmåde, eller kontakt kundesupport for at få hjælp. |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | Debitorkontobetalingen overstiger det samlede forfaldne beløb for de viste varer. Prøv igen senere, eller kontakt kundesupport for at få hjælp. |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | Kundekontobetalingen kræver sin egen konto eller en tilsvarende fakturakonto på en kasselinje. |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | En kundekontobetaling kan ikke behandles på nuværende tidspunkt – overgrænseværdien er overskredet. |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | Denne kunde har ikke tilladelse til at betale aconto. |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | Et eller andet gik galt. Betalingen blev ikke annulleret. Prøv igen. |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | Der opstod en fejl under behandling af betalingen. Prøv igen senere. |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | Fordelskundebetalingsbeløbet overstiger det tilladte beløb for fordelskundekortet i denne transaktion. |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | Kundefordelsrefusionsbeløbet overstiger det tilladte for kundefordelskortet i denne transaktion. |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | Fordelskundekortnummeret blev ikke fundet. Du skal enten aktivere fordelskundekortnummeret eller angive et andet kortnummer og derefter prøve igen. |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | Fordelskundekortnummeret er ikke tilgængeligt. Angiv et andet fordelskundekortnummer, og prøv derefter igen. |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | Dette fordelskundekort berettiger ikke til indløsning af fordelskundepoint for denne transaktion. |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | Der er opstået en fejl i gavekortnummeret. Prøv et andet gavekort, eller kontakt kundesupport for at få hjælp. |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | Beløbet overstiger saldoen på gavekortet. Angiv et andet beløb, og prøv derefter igen. |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | Transaktionen kan ikke indeholde mere end én linje med fordelskundebetaling. |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | Betalingsoplysningerne enten mangler eller er forkerte. Kontrollér betalingsoplysningerne, og prøv igen. |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | Ordren kan ikke behandles i øjeblikket. Prøv igen senere. |
| CCR025     | Front-end-timeout for API til betaling ved kassen | Der er opstået timeout for front end-operationen. Bekræft, om ordren er blevet behandlet i Dynamics 365 Commerce headquarters. |
| CCR026     | Oprindeligt godkendt beløb ændret | Ordrebeløbet er ændret fra det oprindelige godkendelsesbeløb, der er behandlet med betalings-gateway'en. Det kan skyldes, at en kupon, kampagne eller et salg er udløbet på et bestemt tidspunkt. |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | Der opstod en fejl under behandling af en betaling. Den reference, der er angivet til API'en for indkøbsvognen, har en anden reference end forventet (angivelse af mulig uoverensstemmelse under betalingsprocessen). |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | Der er opstået en fejl i den betalingsmetode, der blev forsøgt. Kontakt support for at gennemgå kontoindstillingerne, eller prøv igen med en anden betalingsmetode. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Ofte stillede spørgsmål om betalinger](dev-itpro/payments-retail.md)

[Betalingsmodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)
