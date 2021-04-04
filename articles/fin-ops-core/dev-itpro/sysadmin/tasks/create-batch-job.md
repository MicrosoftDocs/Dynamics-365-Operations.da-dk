---
title: Oprette et batchjob
description: Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 753a78dd140ca82c8c42ff8fdd3772e66b5a1cb0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571071"
---
# <a name="create-a-batch-job"></a>Oprette et batchjob

[!include [banner](../../includes/banner.md)]

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]