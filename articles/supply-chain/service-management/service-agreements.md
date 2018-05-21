---
title: Serviceaftaler
description: "Med serviceaftaler kan du definere de ressourcer, der bruges under et typisk servicebesøg, og hvordan disse ressourcer faktureres til kunden."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf9df2a31c758ba6b63ac7952e00065df04552dc
ms.openlocfilehash: aaff0c1d71fcf2656d5d6e76a2bf4b7b3a699281
ms.contentlocale: da-dk
ms.lasthandoff: 02/19/2018

---

# <a name="service-agreements"></a>Serviceaftaler

[!include [banner](../includes/banner.md)]

Med serviceaftaler kan du definere de ressourcer, der bruges under et typisk servicebesøg, og hvordan disse ressourcer faktureres til kunden.

Alle serviceaftaler er knyttet til projekter, som posteringer bogføres og faktureres gennem. Men du kan også fakturere serviceordreposteringer direkte gennem projektet uden først at skulle knytte serviceordren til en serviceaftale. Det kan du beslutte dig for at gøre, hvis serviceordren gælder et enkeltstående servicebesøg, og behovet for at behandle serviceposteringer hurtigt opvejer behovet for at vedligeholde detaljerede oplysninger i en serviceaftale om kunden over en tidsperiode.

## <a name="service-agreement"></a>Serviceaftale

I de enkelte serviceaftaler skal du angive et projekt, et serviceaftale-id og en serviceaftalegruppe. Serviceaftalegruppen kan bruges til at sortere og organisere serviceaftaler.

Et serviceaftalehoved indeholder indstillinger, der gælder for alle tilknyttede aftalelinjer:

-  Hvorvidt serviceaftalen er suspenderet. Hvis serviceaftalen er suspenderet, kan du ikke oprette serviceordrer ud fra serviceaftalen.
-  Serviceaftalens varighed.
-  Hvordan serviceordrelinjer skal samles i serviceordrer.
-  Hvorvidt serviceaftalen er en skabelon.

I sidehovedet til serviceaftalen skal du også angive alle de serviceobjekter og serviceopgaver, der kan bruges sammen med serviceaftalen ved at angive den specifikke serviceopgave eller det specifikke serviceobjekt, der skal knyttes til linjerne i aftalen.

Fra sidehovedet til serviceaftalen kan du også kopiere serviceaftalelinjer eller serviceskabelonlinjer til den aktuelle serviceaftale.

Du kan suspendere serviceaftaler og stoppe individuelle serviceaftalelinjer.

Hvis du markerer afkrydsningsfeltet **Suspenderet** i en serviceaftale, kan du ikke:

-    Oprette serviceordrer automatisk eller manuelt fra serviceaftalen.

Hvis du markerer afkrydsningsfeltet **Stoppet** på en linje i serviceaftalen, kan du ikke:

-    Oprette serviceordrer automatisk eller manuelt fra serviceaftalelinjen.
-    Kopiere serviceaftalelinjen til en anden serviceaftale eller serviceordre.


> [!NOTE]
> Hvis en serviceaftale suspenderes, stoppes alle tilknyttede linjer uanset deres individuelle status.

## <a name="service-agreement-lines"></a>Serviceaftalelinjer

Serviceaftalelinjerne indeholder en detaljeret beskrivelse af indholdet af det foreslåede servicearbejde. Linjerne indeholder følgende indstillinger:

-  Posteringstypen og en beskrivelse af posteringstypen.
-  Den medarbejder, der udfører servicearbejdet.
-  De objekter, servicen skal udføres på for serviceaftalen.
-  Den hyppighed, arbejdet udføres med, og tilknyttede vare-, udgifts- og gebyrposteringer registreres.
-  Det tidsvindue, hvor serviceordrelinjer kan grupperes i en serviceordre.
-  Serviceopgaver bruges til at gruppere flere sæt aftalelinjer sammen i arbejdsopgaver og til at give servicemedarbejdere og kunder en overordnet beskrivelse af, hvilken serviceopgave der skal udføres.
-  Hvorvidt en linje er standset. Hvis en linje er standset, kan du ikke oprette serviceordrer for den pågældende linje.
-  Projektindstillinger som kategori og linjeegenskab.

## <a name="related-topics"></a>Relaterede emner

[Oprette serviceaftaler](create-service-agreements.md)

