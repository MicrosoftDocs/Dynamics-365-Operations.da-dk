---
title: Oprette callcenter-ordrer
description: Denne artikel gennemgår en eksempelprocedure, hvor en callcenter-bruger slår en kunde op, opretter en ny ordre, søger efter et produkt og opkræver betaling fra kunden i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228504"
---
# <a name="create-call-center-orders"></a>Oprette callcenter-ordrer

[!include [banner](../includes/banner.md)]

Denne artikel gennemgår en eksempelprocedure, hvor en callcenter-bruger slår en kunde op, opretter en ny ordre, søger efter et produkt og opkræver betaling fra kunden i Microsoft Dynamics 365 Commerce. Denne procedure bruger demodatafirmaet USRT og er beregnet til salgsassistenter. 

## <a name="prerequisites"></a>Forudsætninger

Brugeren, der udfører denne procedure, skal være oprettet som bruger af et callcenter. Det er valgfrit, at Fabrikams halvårlige katalog kan udgives med mindst én kildekode.

### <a name="add-yourself-as-a-call-center-user"></a>Tilføje dig selv som callcenter-bruger

Følg disse trin for at tilføje dig selv som callcenter-bruger.

1. Gå i Commerce headquarters til **Detail og Commerce \> Kanaler \> Call centre \> Alle call centre**.
1. Vælg **Kanalbrugere** i feltet **Brugere**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Angiv dit bruger-id i feltet **Bruger-id**.
1. Indtast dit brugernavn i feltet **Navn**. Brugernavnet kan være det samme som bruger-id'et.
1. Vælg **Gem** i handlingsruden.
1. Gå tilbage til **Retail og Commerce \> Kanaler \> Call centre \> Alle call centre**.
1. Vælg callcenterets detailkanal-id.
1. Kontrollér, at indstillingen **Aktivér ordrefuldførelse** er angivet til **Ja**. Hvis indstillingen ikke er synlig, kan du springe dette trin over.

## <a name="complete-the-example-call-center-procedure"></a>Fuldføre proceduren for eksempelcallcenter

Udfør følgende trin for at fuldføre eksemplet med callcenter-proceduren.

1. Gå til **Retail og Commerce \> Kunder \> Kundeservice**.
1. Angiv søgekriterierne for at søge efter kunden under fanen **Kundesøgning**. Til denne eksempelprocedure skal du skrive **Karen**.
1. Vælg **Søg**. Dialogboksen **Kundesøgning** vises med søgeresultaterne.
1. Vælg kundeposten for **Karen Berg**, der har kundekontonummer **2001**, og vælg derefter **Vælg**.
1. Vælg **Ny salgsordre** i handlingsruden.
1. Til højre skal du vælge fanen **Overskrift**.
1. Vælg **99 Standard** i feltet **Leveringsmåde** i oversigtspanelet **Levering**.

    ![Vælg en leveringsmåde.](../media/Select_Mode_of_Delivery.png)

1. Til højre skal du vælge fanen **Linjer**.
1. Angiv det varenummer, du vil søge efter, i feltet **Varenummer** i den nye række til den nye salgslinje i sektionen **Salgsordrelinjer**. I dette eksempel skal du skrive **81327** og derefter vælge produktet på rullelisten for at føje det til salgsordren.
1. Angiv salgsantallet i feltet **Antal**.
1. Vælg kildekoden for kataloget i feltet **Kildekode**. Hvis der ikke er nogen aktive kildekoder, kan du springe dette trin over.
1. Vælg **Fuldført** i handlingsruden for at hente kundebetalingen. Denne handling åbner dialogboksen **Salgsordreoversigt**, der viser det samlede forfaldne beløb. Handlingen udløser også beregning af eventuelle gebyrer, f.eks. forsendelse og håndtering, og viser dem i dialogboksen **Salgsordreoversigt**.

    ![Knappen Fuldfør.](../media/Complete_button.png)

1. Vælg **Tilføj** i oversigtspanelet **Betalinger** i dialogboksen **Salgsordreoversigt** for at hente betalingerne.

    ![Dialogboksen Salgsordreoversigt.](../media/order_summary.png)

1. Vælg betalingsmåden i feltet **Betalingsmåde** i dialogboksen **Angiv oplysninger om debitorbetaling**. Til denne eksempelprocedure skal du vælge **Kontant**.
1. Angiv betalingsbeløbet i feltet **Betalingsbeløb**. I dette eksempel skal du angive **120,00**, hvilket svarer til den ordresaldo, der vises i dialogboksen **Salgsordreoversigt**. Ved at indtaste dette beløb kan du fuldføre ordren som fuldt ud betalt.
1. Vælg **OK**.
1. Vælg **Send**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilpasse transaktionsmails efter leveringsmåde](../customize-email-delivery-mode.md)

[Skifte leveringsmåde til i POS](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
