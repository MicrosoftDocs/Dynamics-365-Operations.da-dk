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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ec10e0f79e4eca7f51ba48c679dcf6fe745eb29
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141424"
---
# <a name="create-call-center-orders"></a>Oprette callcenter-ordrer

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden. Denne procedure bruger demodatafirmaet USRT og er beregnet til salgsassistenter. Forudsætninger: Den bruger, der udfører proceduren, er konfigureret som call center-brugere, og Fabrikams halvårlige katalog udgives med mindst én kildekode i.

1. Gå til Retail og Commerce > Kunder > Kundeservice.
2. Angiv søgekriterierne til at søge efter kunden i feltet Søgetekst.
    * Til denne eksempelprocedure skal du skrive "karen" og trykke på tab.  
3. Klik på Søg.
    * Da der kun er én kunde med navnet Karen i demodataene, vælges de automatisk.  
4. Klik på Ny salgsordre.
5. Udvis eller skjul sektionen Salgsordrehoved.
6. Vælg kildekoden til kataloget.
    * Hvis der ikke er nogen aktive kildekoder, kan du lukke feltet Kilde og springe dette trin over.  
7. Klik på Tilføj linje.
8. Indtast ordet til varesøgning i feltet Varenummer.
    * Til denne eksempelprocedure skal du angive en del af et varenummer, "8111" og trykke på tab. Så vises vinduet til varesøgning.  
9. Vælg det produkt, der skal føjes til salgsordren
10. Angiv salgsantallet.
11. Klik på Opret.
12. Klik på Fuldført for at hente kundebetalingen.
13. Klik på Tilføj.
    * Linket Tilføj findes under fanen Betalinger. Udvid fanen Betalinger, hvis den er skjult.  
14. Vælg betalingsmåden.
    * Til denne procedure skal du vælge kontantbetalingsmetoden.  
15. Luk siden.
16. Indtast beløbet.
    * Til denne procedure skal du angive et beløb svarende til ordresaldoen, som kan ses på oversigtssiden Salgsordre til venstre for feltet Beløb. Det giver dig mulighed for at fuldføre ordren som fuldt ud betalt.  
17. Klik på OK.
18. Klik på Send.

