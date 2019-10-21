---
title: Oprette et batchjob
description: Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27541c84a40fe9b7e7705162e06167ad4f7e4ed9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191379"
---
# <a name="create-a-batch-job"></a>Oprette et batchjob

[!include [task guide banner](../../includes/task-guide-banner.md)]

Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling. Batchjob køres ved hjælp af sikkerhedslegitimationsoplysningerne for den bruger, der har oprettet jobbet. Du kan bruge følgende procedure for at oprette et batchjob. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-the-batch-job"></a>Opret batchjobbet
1. Gå til **Navigationsrude > Moduler > Systemadministration > Forespørgsler > Batchjob**.
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Stillingsbeskrivelse**.
4. Angiv en dato og et klokkeslæt i feltet **Planlagt startdato/-klokkeslæt**.
5. Klik på **Gem**.

## <a name="create-a-recurrence"></a>Opret en gentagelse
1. Klik på **Batchjob** i handlingsruden.
2. Klik på **Gentagelse**. Brug disse indstillinger til at angive et interval og mønster for gentagelsen.  
3. Klik på **OK**.

## <a name="add-alerts"></a>Tilføj beskeder
1. Klik på **Batchjob** i handlingsruden.
2. Klik på **Beskeder**. Angiv, om der skal sendes meddelelser om påmindelser til dig, når batchjobbet afsluttes, støder på en fejl eller annulleres. Angiv derefter, om der skal vises påmindelser som pop op-meddelelser.   
3. Klik på **OK**.

## <a name="adjust-batch-job-status"></a>Justere status for batchjob
1. Gå til **Systemadministration > Forespørgsler > Batchjob**.
2. Vælg det relevante batchjob.
3. Klik på **Batchjob > Funktioner > Skift status** i handlingsruden.
4. Vælg den relevante status:
    - **Tilbagehold**: Angiv batchjobbet som **tilbageholdt**, så det tilbageholdes fra batchjobbets planlægger. Svarer til *stop*.
    - **Venter**: Angiv batchjobbet til **venter**, så det venter på at blive afhentet af batchjobbets planlægger. Svarer til *start*.
5. Klik på **OK**.
