--- 
title: Oprette et batchjob
description: Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ca2b755406fb7fce4b11457be86f6a8685004438
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-batch-job"></a>Oprette et batchjob

[!include[task guide banner](../../includes/task-guide-banner.md)]

Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling. Batchjob køres ved hjælp af sikkerhedslegitimationsoplysningerne for den bruger, der har oprettet jobbet. Du kan bruge følgende procedure for at oprette et batchjob. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-the-batch-job"></a>Opret batchjobbet
1. Gå til Systemadministration > Forespørgsler > Batchjob.
2. Klik på Ny.
3. Indtast en værdi i feltet Stillingsbeskrivelse.
4. Angiv en dato og et klokkeslæt i feltet Planlagt startdato/-klokkeslæt.
5. Klik på Gem.

## <a name="create-a-recurrence"></a>Opret en gentagelse
1. Klik på Batchjob i handlingsruden.
2. Klik på Gentagelse.
    * Brug disse indstillinger til at angive et interval og mønster for gentagelsen.  
3. Klik på OK.

## <a name="add-alerts"></a>Tilføj beskeder
1. Klik på Batchjob i handlingsruden.
2. Klik på Beskeder.
    * Angiv, om der skal sendes meddelelser om påmindelser til dig, når batchjobbet afsluttes, støder på en fejl eller annulleres. Angiv derefter, om der skal vises påmindelser som pop op-meddelelser.   
3. Klik på OK.


