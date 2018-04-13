---
title: Udgiftsrapporter og flere godkendere
description: "Dette emne indeholder oplysninger om udgiftsrapporter, der kræver godkendelse af mere end én person."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 0f7592c580a21040c8b630885939ceaab3855c2c
ms.contentlocale: da-dk
ms.lasthandoff: 03/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a>Udgiftsrapporter og flere godkendere

[!INCLUDE [banner](../includes/banner.md)]

Afhængigt af organisationens politikker for godkendelse af udgifter kan det være nødvendigt med mere end én person til at godkende en udgiftsrapport, der er sendt af en medarbejder. Når du opretter arbejdsgangsprocessen til godkendelse af udgiftsrapporter, kan du tilføje arbejdsgangelementer, der omfatter opgaver eller trin for en eller flere godkendere af udgiftsrapporter. Du kan f.eks. kræve, at alle udgiftsrapporter først godkendes af chefen for den medarbejder, der har indsendt rapporten, og derefter af kreditorkoordinatoren.

Hvis du beslutter at kræve flere godkendere af udgiftsrapporter, kan du tilføje arbejdsgangelementer på en af følgende måder:

- Tilføj ét godkendelseselement, der har ét trin. Trinnet kan f.eks. kræve, at der tildeles en udgiftsrapport til en brugergruppe, og at den godkendes af 50 procent af medlemmerne af brugergruppen.
- Tilføj ét godkendelseselement, der har flere trin. Godkendelseselementet kan f.eks. have følgende trin:

    1. Chefen for den medarbejder, som har indsendt udgiftsrapporten, godkender den.
    2. Kreditormedarbejderen kontrollerer kvitteringerne og posterne i udgiftsrapporten.
    3. Ejeren af budgettet godkender udgiftsrapporten.

- Tilføj flere godkendelseselementer, som hver har ét trin. For eksempel kan du tilføje et separat godkendelseselement for hver af følgende trin:

    1. Medarbejderens chef godkender udgiftsrapporten.
    2. Ejeren af budgettet godkender udgiftsrapporten.

