---
title: Oprette et batchjob
description: Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling.
author: maertenm
ms.date: 11/22/2021
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
ms.openlocfilehash: 76c6c68f7effad0c40282b22ea2a6bf991862cf5
ms.sourcegitcommit: d7d997ad84623ad952672411c0eb6740972ae0b1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/24/2021
ms.locfileid: "7864167"
---
# <a name="create-a-batch-job"></a>Oprette et batchjob

[!include [banner](../../includes/banner.md)]

Et batchjob er en gruppe opgaver, der sendes til en AOS-forekomst (applikationsobjektserver) til automatisk behandling. Batchjob køres ved hjælp af sikkerhedslegitimationsoplysningerne for den bruger, der har oprettet jobbet. Du kan bruge følgende procedure for at oprette et batchjob. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="create-the-batch-job"></a>Opret batchjobbet
1. Gå til **Navigationsrude > Moduler > Systemadministration > Forespørgsler > Batchjob**.
2. Vælg **Ny**.
3. Angiv en beskrivelse af batch-jobbet i feltet **Jobbeskrivelse**.
4. Angiv den dato og det klokkeslæt, hvor batchjobbet skal køre, i feltet **Planlagt startdato/-tidspunkt**.
5. Vælg **Gem**.

## <a name="create-a-recurrence"></a>Opret en gentagelse
1. Vælg **Batchjob** i handlingsruden.
2. Vælg **Gentagelse**. Brug disse indstillinger til at angive et interval og mønster for gentagelsen.  
3. Vælg **OK**.

## <a name="add-alerts"></a>Tilføj beskeder
1. Vælg **Batchjob** i handlingsruden.
2. Vælg **Påmindelser**. Angiv, om der skal sendes meddelelser om påmindelser til dig, når batchjobbet afsluttes, støder på en fejl eller annulleres. Angiv derefter, om der skal vises påmindelser som pop op-meddelelser.   
3. Vælg **OK**.

## <a name="add-a-task-to-a-batch-job"></a>Føje en opgave til et batchjob
1.  Gå til siden **Batchjob**, og vælg **Vis opgaver**.
2.  Vælg **Ctrl+N** for at oprette en opgave.
3.  Angiv en beskrivelse af batch-opgaven.
4.  Vælg den regnskabsdatabase, som opgaven skal køre i, i feltet **Regnskab**.
5.  Marker den proces, hvor opgaven skal køres i feltet **Klassenavn**. 
6.  Hvis det er nødvendigt, skal du vælge en batchgruppe for opgaven.

    Klientopgaver skal tilhøre en batchgruppe. De tilknyttes automatisk standardbatchgruppen (også kendt som en tom batchgruppe).

7.  Vælg **Ctrl+S** for at gemme opgaven.
8.  Hvis du vil gøre den valgte opgave afhængig af en anden opgave i jobbet, skal du markere gitteret **Har betingelser** og derefter udføre disse trin for hver betingelse, du vil definere:

    1. Vælg **Ctrl+N** for at oprette en betingelse.
    2. Vælg opgave-id for den overordnede opgave.
    3. Vælg den status, den overordnede opgave skal have, før den afhængige opgave kan køre.
    4. Vælg **Ctrl+S** for at gemme betingelsen.

    Hvis du definerer mere end én betingelse, og hvis *alle* betingelser skal være opfyldt, før den afhængige opgave kan køres, skal du vælge betingelsestypen **Alle**. Vælg betingelsestypen *Alle*, hvis den afhængige opgave kan køre, når én af betingelserne **Alle** er opfyldt.

9.  Vælg, hvordan opgavefejl skal håndteres. Hvis du vil ignorere fejlene i en bestemt opgave, skal du gå til fanen **Generelt** og markere indstillingen **Ignorér opgavefejl** for den pågældende opgave. Hvis denne indstilling er markeret, medfører en fejl ved opgaven ikke, at jobbet mislykkes. Du kan også bruge feltet **Maks. antal forsøg** til at angive det antal gange, der skal gøres forsøg på at køre en opgave igen, før den opfattes som mislykket. Som best practice anbefales det, at du ikke angiver feltet **Maks. antal forsøg** til en værdi på mere end **5**.

    Du kan finde flere oplysninger om batchjob i [Aktiver batch-gentagelser](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Justere status for batchjob
1. Gå til **Systemadministration > Forespørgsler > Batchjob**.
2. Vælg det relevante batchjob.
3. Vælg **Batchjob > Funktioner > Skift status** i handlingsruden.
4. Vælg den relevante status:
    - **Tilbagehold**: Angiv batchjobbet som **tilbageholdt**, så det tilbageholdes fra batchjobbets planlægger. Svarer til *stop*.
    - **Venter**: Angiv batchjobbet til **venter**, så det venter på at blive afhentet af batchjobbets planlægger. Svarer til *start*.
5. Vælg **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
