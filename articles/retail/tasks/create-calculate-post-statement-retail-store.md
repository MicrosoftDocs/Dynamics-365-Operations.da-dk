--- 
title: "Oprette, beregne og bogføre et opgørelse for en detailbutik"
description: "Denne procedurer gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 60bcafffc922e6d57e52a5dff104a0fbb252f6ce
ms.contentlocale: da-dk
ms.lasthandoff: 07/28/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a>Oprette, beregne og bogføre et opgørelse for en detailbutik

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedurer gennemgår de manuelle trin til oprettelse, beregning og bogføring af en opgørelse for en butik. Der er også batchjob, der kan konfigureres for de samme opgaver. Trin til konfiguration og kørsel af batchjob findes i andre emner. Hvis du vil fuldføre denne procedure, skal du have transaktioner, der blev fuldført i POS og derefter hentet ind i Dynamics AX. Denne registrering bruger USRT-firmaets demodata. Denne procedure henviser måske til Microsoft Dynamics AX. Bemærk, at Dynamics AX nu kaldes Microsoft Dynamics 365 for Operations.

1. Gå til Alle arbejdsområder > .. > Detailbutiksregnskab.
2. Klik på Ny opgørelse.
3. Klik på rullelisten i feltet Butiksnummer for at åbne opslaget.
4. Klik op linket i den valgte række på listen.
5. Klik på OK.
    * Gruppe til opsætning har de indstillinger, der styrer, hvilke transaktioner der medtages i opgørelsen, og hvordan de grupperes på linjer i opgørelsen. Du kan åbne gruppen til opsætning og ændre disse indstillinger, eller du kan bruge standardindstillingerne.  
    * Feltet Opgørelsesmetode definerer, hvordan opgørelseslinjerne grupperes.  
    * Vælg en medarbejder eller et kasseapparat, hvis du kun vil beregne en opgørelse for den specifikke medarbejder eller det specifikke kasseapparat.  
6. Vælg en indstilling i feltet Lukkemetode.
7. Klik på Beregn opgørelse.
8. Klik på Ja.
    * Når du har beregnet opgørelsen, skal der være linjer, der er oprettet med samlede beløb for hver betalingsmetode og opgørelsesmetode, der blev brugt.  
    * Angiv et optalt beløb på hver linje, hvis det skal angives eller opdateres. Det optalte felt udfyldes med beløb fra kasseoptællinger udført i POS.  
9. Klik på Bogfør opgørelse.
10. Klik på Luk.
11. Gå til Detail og handel > Kanaler > Detailbutiksregnskab.
12. Klik på fanen Bogførte opgørelser.

