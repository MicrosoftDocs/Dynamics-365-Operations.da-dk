---
title: Oprette et batchjob
description: Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "313353"
---
# <a name="create-a-batch-job"></a>Oprette et batchjob

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

