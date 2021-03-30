---
title: Bogføring af onlinesalg og betalinger
description: Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e24c2be8a1b0da3c34919fdb44aa744f8e7fc87c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215406"
---
# <a name="posting-of-online-sales-and-payments"></a>Bogføring af onlinesalg og betalinger

[!include [banner](../includes/banner.md)]

Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik.

Bogføring af onlinesalg og -betalinger er en proces i to faser.

- Hentning af online handelstransaktionsdata i hovedkvarteret.
- Synkronisering af ordrer for at oprette salgsordrer i hovedkvarteret.

Når du henter online transaktionsdata, kan du enten gøre det ved at udføre P-job manuelt eller ved at oprette et tilbagevendende batchjob.

### <a name="manually-running-the-p-job"></a>Manuel kørsel af P-job

1. Gå til Alle arbejdsområder > Retail og Commerce IT.
2. Klik på Distributionsplan.
3. Vælg P-0001.
4. Juster kanaldatabasegrupper, hvis det er nødvendigt.
5. Klik på Kør nu.
6. Klik på Ja.

### <a name="scheduling-a-recurring-p-job"></a>Planlægning af et tilbagevendende P-job

1. Gå til Alle arbejdsområder > Retail og Commerce IT.
2. Klik på Distributionsplan.
3. Vælg P-0001.
4. Klik på Opret batchjob.
5. Klik på Kør i baggrunden.
5. Aktivér batchbehandling.
6. Klik på Gentagelse.
7. Vælg indstillingen Slutdato mangler.
8. Angiv intervallet mellem kørslerne i minutter i feltet Antal. Dette vil typisk være 5-10.
9. Klik på OK.
10. Klik på OK.

Ordrer kan synkroniseres enten via manuel kørsel af "Synkroniser ordrer"-job eller ved at oprette et tilbagevendende batchjob.

### <a name="manually-running-order-synchronization"></a>Manuel kørsel af ordresynkronisering 

Udfør følgende trin for manuelt at køre jobbet "Synkroniser ordrer" én gang.

1. Gå til Alle arbejdsområder > Butiksregnskab.
2. Kik på Synkroniser ordrer.
3. Vælg 'Butikker efter område' i feltet Organisationshierarki.
    * Vælg enten en bestemt onlinebutik, eller vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.  
    * Klik på pilen for at føje dit valg.  
4. Klik på fanen Kør i baggrunden.
5. Deaktiver batchbehandling.
6. Klik på Gentagelse.
7. Vælg indstillingen Afslut efter.
8. Angiv 1 i feltet Afslut efter.
9. Klik på OK.
10. Klik på OK.

### <a name="scheduling-recurring-order-synchronization"></a>Planlægge synkronisering af tilbagevendende ordrer

Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik. Denne procedure bruger USRT-firmaets demodata.

1. Gå til Alle arbejdsområder > Butiksregnskab.
2. Kik på Synkroniser ordrer.
3. Vælg 'Butikker efter område' i feltet Organisationshierarki.
    * Vælg enten en bestemt onlinebutik, eller vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.  
    * Klik på pilen for at føje dit valg.  
4. Klik på fanen Kør i baggrunden.
5. Aktivér batchbehandling.
6. Klik på Gentagelse.
7. Vælg indstillingen Slutdato mangler.
8. Angiv intervallet mellem kørslerne i minutter i feltet Antal. Dette er typisk 2-20.
9. Klik på OK.
10. Klik på OK.

## <a name="data-entities-involved-in-the-process"></a>Dataenheder, der er involveret i processen

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans


[!INCLUDE[footer-include](../../includes/footer-banner.md)]