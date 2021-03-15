---
title: Oprette callcenter-ordrer
description: Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08a806514a92a99a9f0b18b36817f49a09516ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964839"
---
# <a name="create-call-center-orders"></a>Oprette callcenter-ordrer

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden. Denne procedure bruger demodatafirmaet USRT og er beregnet til salgsassistenter. Forudsætninger: Den bruger, der udfører proceduren, er konfigureret som call center-brugere, og Fabrikams halvårlige katalog udgives med mindst én kildekode i.

1. Gå til **Retail og Commerce \> Kunder \> Kundeservice**.
2. Angiv søgekriterierne for at søge efter kunden i feltet **Søgetekst**.
    * Til denne eksempelprocedure skal du skrive "Karen" og vælge **Tab**.  
3. Vælg Søg.
    * Da der kun er én kunde med navnet "Karen" i demodataene, vælges resultatet automatisk.  
4. Vælg **Ny salgsordre**.
5. Udvis eller skjul overskriftssektionen **Salgsordre**.
6. Vælg kildekoden til kataloget.
    * Hvis der ikke er nogen aktive kildekoder, kan du springe dette trin over.  
7. Vælg **Tilføj linje**.
8. Indtast søgeordet til varen i feltet **Varenummer**.
    * Til denne eksempelprocedure skal du angive en del af et varenummer, "8111" og trykke på tab. Denne handling åbner vinduet til varesøgning.  
9. Vælg det produkt, der skal føjes til salgsordren.
10. Angiv salgsantallet.
11. Vælg **Opret**.
12. Vælg **Fuldført** for at hente kundebetalingen.
13. Vælg **Tilføj**.
    * Linket Tilføj findes under fanen Betalinger. Udvid fanen Betalinger, hvis den er skjult.  
14. Vælg betalingsmåden.
    * Til denne procedure skal du vælge kontantbetalingsmetoden.  
15. Luk siden.
16. Indtast beløbet.
    * Til denne procedure skal du angive et beløb svarende til ordresaldoen, som kan ses på oversigtssiden Salgsordre til venstre for feltet Beløb. Denne handling giver dig mulighed for at fuldføre ordren som fuldt ud betalt.  
17. Vælg **OK**.
18. Vælg **Send**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilpasse transaktionsmails efter leveringsmåde](../customize-email-delivery-mode.md)

[Skifte leveringsmåde til i POS](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]