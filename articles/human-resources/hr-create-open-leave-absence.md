---
title: Oprette en orlov uden afslutning
description: Denne artikel forklarer, hvordan du opretter en orlov uden afslutning i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805336"
---
# <a name="create-an-open-ended-leave-of-absence"></a>Oprette en orlov uden afslutning

> [!IMPORTANT]
> De funktioner, der er beskrevet i denne artikel, vil være tilgængelige som en del af en fremtidig version af Finance-infrastrukturen efter Microsoft Dynamics 365 Finance-frigivelse 10.0.31.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan sende en anmodning om orlov uden afslutning og se status for dine orlovsanmodninger i Dynamics 365 Human Resources.

## <a name="prerequisites"></a>Forudsætninger

1. Under **Funktionsstyring** skal du sikre dig, at funktionen **Orlov uden afslutning** er aktiveret.

    > [!IMPORTANT]
    > Funktionen kan ikke deaktiveres, efter den er blevet aktiveret.

2. Opret en orlovstype for fravær.
3. Angiv detaljer som orlovstype, beskrivelse og arbejdsgangs-id.
4. Vælg **Orlov** i feltet **Anmodningstype**.
5. I detaljesektionen skal du angive indstillingen **Uden afslutning** til **Ja** for orlov uden afslutning.
6. Angiv indstillingen **Meddelelse om retur til arbejde** til **Ja** eller **Nej**.
7. Du kan vælge at anmode om en meddelelse om retur til arbejde for anmodninger om orlov uden afslutning.

> [!NOTE]
> Når denne funktion er aktiveret, vil funktionen **Krævet vedhæftet fil** være aktiveret.

## <a name="request-an-open-ended-leave-of-absence"></a>Anmode om en orlov uden afslutning

1. I arbejdsområdet **Selvbetjeningsservice** skal du vælge **Mere (...)** i feltet **Fritidssaldi**.
2. Hvis du vil sende en orlovsanmodning, skal du vælge **Anmod om orlov**.
3. Indtast oplysninger i felterne **Orlovstype** og **Startdato**. Angiv en foreløbig slutdato i feltet **Slutdato**.
4. Hvis du skal sende understøttende dokumentation, skal du vælge **Upload** under **Vedhæftede filer**.
5. Vælg **Send**, når du er klar til at sende din anmodning. Ellers skal du vælge **Gem kladde**.
6. Hvis du vil opdatere en anmodning om orlov uden afslutning, skal du vælge anmodningen, angive en slutdato i feltet **Slutdato**, angive indstillingen **Bekræft slutdato** til **Ja** og uploade dokumentation.
7. Hvis indstillingen **Meddelelse om retur til arbejde** er angivet til **Ja**, skal du vælge **Upload** og derefter markere afkrydsningsfeltet for at bekræfte, at en gyldig meddelelse om returnering til arbejde er blevet uploadet.
8. Når alle detaljer er angivet, skal du vælge **Send**.
