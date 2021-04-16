---
title: Brug af kontinuitetsprogram
description: Denne procedure gennemgår salg af et kontinuitetsprogram og behandling af relaterede salgsordrer.
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58eca42634ad995f174350bc3a1996ddc4c449b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804083"
---
# <a name="using-continuity-program"></a>Brug af kontinuitetsprogram

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår salg af et kontinuitetsprogram og behandling af relaterede salgsordrer. For at udføre denne procedure skal brugeren være oprettet som bruger af et callcenter. Proceduren bruger USRT-demodatafirmaet.

1. Gå til Retail og Commerce > Kunder > Kundeservice.
2. Skriv 'Karen' i feltet Søgetekst, og tryk derefter på tabulatortasten.
    * Dialogboksen for avanceret søgning åbnes. Hvis ikke, skal du klikke på Søg til højre for feltet.  
3. Markér den valgte række på listen.
    * Der er én række, hvor Karen Berg vises. Vælg rækken ved at klikke på markeringskolonnen yderst til venstre i gitteret.  
4. Klik på Vælg.
5. Klik på Ny salgsordre.
    * Det er en god ide at notere salgsordrenummeret. Du skal bruge det senere i denne procedure.  
6. Skriv '88000' i feltet Varenummer, og tryk derefter på tabulatortasten.
    * Dette er en kontinuitetsvare i USRT-demodata.  
7. Klik på Fuldført.
8. Vælg 'Visa' i feltet Betalingsmetode.
9. Klik på Tilføj kreditkort.
    * Angiv de nødvendige kreditkortoplysninger på denne side.  
10. Klik på OK.
11. Vis sektionen Betaling.
    * Hvis du vil sende en ordre via et callcenter, skal der angives betalinger for ordren.  
12. Klik på OK.
13. Klik på Send.
    * Du har oprettet en ny kontinuitetsordre. Derefter skal du køre to batchprocesser, der bruges til at behandle kontinuitetsordrerne.  
14. Luk siden.
15. Gå til Retail og Commerce > Kontinuitet > Udfør behandling af fortløbende betalinger.
16. Skriv '88000' i feltet Fortløbende vare, og tryk derefter på tabulatortasten.
17. Klik på OK.
18. Gå til Retail og Commerce > Kontinuitet > Opret fortløbende underordnede ordrer.
    * Denne proces opretter nye salgsordrer, der er baseret på indstillingerne for kontinuitetsprogrammerne.  
19. Skriv '88000' i feltet Fortløbende vare, og tryk derefter på tabulatortasten.
    * Vare '88000' er en kontinuitetsvare i USRT-demodata.  
20. Indtast eller vælg en værdi i feltet Salgsordre.
    * Angiv nummeret på salgsordren, du noterede tidligere i proceduren. Derved reduceres behandlingstiden til et minimum for denne procedure. Feltet Salgsordre er valgfrit – du kan behandle alle ordrer for alle ét program.  
21. Klik på OK.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]