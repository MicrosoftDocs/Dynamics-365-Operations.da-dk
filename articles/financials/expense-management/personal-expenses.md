---
title: Personlige udgifter i en udgiftsrapport
description: I dette emne beskrives de to metoder til håndtering af en arbejders personlige udgifter i Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6b6c505e7dc5e6544658b00d9f59e6062353608
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564733"
---
# <a name="personal-expenses-on-an-expense-report"></a>Personlige udgifter i en udgiftsrapport

[!include [banner](../includes/banner.md)]

Under forretningsrejser kan arbejdere undertiden kreditere personaleudgifter på deres firmaets kreditkort. Hvis du ikke definerer en proces til håndtering af personlige udgifter, kan godkendelsesprocessen for udgiftsrapporter blive afbrudt, når arbejderne sender deres specificerede udgiftsrapporter. 

I Microsoft Dynamics 365 for Finance and Operations findes der to metoder til håndtering af en arbejders personlige udgifter:

- **Betalt af medarbejder** – Organisationen betaler ikke personlige udgifter, der figurerer på firmaets kreditkort. Den opretter i stedet en rapport, der viser de personlige udgifter sammen med de firmaudgifter, der blev krediteret på firmaets kreditkort.
- **Betalt af firma** – Organisationen betaler hele fakturaen, der er betalt med firmaets kreditkort, og debiterer derefter arbejderens konto for de personlige udgifter.

Du kan vælge den metode, som organisationen bruger, på siden **Parametre for udgiftsstyring**.
