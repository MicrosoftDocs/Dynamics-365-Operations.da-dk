---
title: Personlige udgifter i en udgiftsrapport
description: "Dette emne forklarer de to metoder til håndtering af en arbejders personlige udgifter i Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 27698b02795b709a167235537d8b1ca871bdd371
ms.contentlocale: da-dk
ms.lasthandoff: 03/13/2018

---

# <a name="personal-expenses-on-an-expense-report"></a>Personlige udgifter i en udgiftsrapport

[!INCLUDE [banner](../includes/banner.md)]

Under forretningsrejser kan arbejdere undertiden kreditere personaleudgifter på deres firmaets kreditkort. Hvis du ikke definerer en proces til håndtering af personlige udgifter, kan godkendelsesprocessen for udgiftsrapporter blive afbrudt, når arbejderne sender deres specificerede udgiftsrapporter. 

I Microsoft Dynamics 365 for Finance and Operations er der to metoder til håndtering af en arbejders personlige udgifter:

- **Betalt af medarbejder** – Organisationen betaler ikke personlige udgifter, der figurerer på firmaets kreditkort. Den opretter i stedet en rapport, der viser de personlige udgifter sammen med de firmaudgifter, der blev krediteret på firmaets kreditkort.
- **Betalt af firma** – Organisationen betaler hele fakturaen, der er betalt med firmaets kreditkort, og debiterer derefter arbejderens konto for de personlige udgifter.

Du kan vælge den metode, som organisationen bruger, på siden **Parametre for udgiftsstyring**.

