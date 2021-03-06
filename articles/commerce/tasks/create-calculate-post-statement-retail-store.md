---
title: Oprette, beregne og bogføre opgørelser for en detailbutik
description: Dette emne gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58900ca4d3f6893689822a8cc5657d8c91772f65
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798531"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Oprette, beregne og bogføre opgørelser for en detailbutik

[!include [banner](../includes/banner.md)]

Dette emne gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik. Der er også batchjob, der kan konfigureres for de samme opgaver. Trin til konfiguration og kørsel af batchjob findes i andre emner. Hvis du vil fuldføre denne procedure, skal du have transaktioner, der blev fuldført i POS og derefter hentet ind i Dynamics 365 Commerce. Denne registrering bruger USRT-firmaets demodata.

1. Vælg **Butiksregnskab** på startsiden.
2. Vælg **Ny opgørelse**.
3. Vælg en indstilling på rullelisten i feltet **Butiksnummer**.
4. Vælg **OK**.
5. Gruppen **Konfiguration** har de indstillinger, der styrer, hvilke transaktioner der medtages i opgørelsen, og hvordan de grupperes på linjer i opgørelsen. Du kan åbne gruppen **Konfiguration** og ændre disse indstillinger, eller du kan bruge standardindstillingerne.  
    - Feltet **Opgørelsesmetode** definerer, hvordan opgørelseslinjerne grupperes.  
    - Vælg en medarbejder eller et kasseapparat i feltet **Medarb./kasse**, hvis du kun vil beregne en opgørelse for den specifikke medarbejder eller det specifikke kasseapparat.  
6. Vælg en indstilling i feltet **Lukkemetode**.
7. Vælg **Beregn opgørelse** i handlingsruden.
8. Vælg **Ja**.
    - Når du har beregnet opgørelsen, skal der være linjer, der er oprettet med samlede beløb for hver betalingsmetode og opgørelsesmetode, der blev brugt.  
    - Angiv et optalt beløb på hver linje, hvis det skal angives eller opdateres. Det optalte felt udfyldes med beløb fra kasseoptællinger udført i POS.  
9. Vælg **Bogfør opgørelse** i handlingsruden.
10. Vælg **Luk**.
11. Luk ruden.
12. Vælg **Butiksregnskab** på startsiden.
13. Vælg fanen **Bogførte opgørelser**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]