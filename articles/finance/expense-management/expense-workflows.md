---
title: Konfigurere arbejdsgange for Udgiftsstyring
description: Du kan oprette en proces for en arbejdsgang, der bruges til at gennemse og godkende rejse- og udgiftsdokumenter.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153984"
---
# <a name="set-up-workflows-for-expense-management"></a>Konfigurere arbejdsgange for Udgiftsstyring

[!include [banner](../includes/banner.md)]

Du kan oprette en proces for en arbejdsgang, der bruges til at gennemse og godkende rejse- og udgiftsdokumenter. De dokumenter, der kan være defineret en arbejdsgang for, omfatter udgiftsrapporter, rejserekvisitioner og anmodninger om kontaktforskud.

En arbejdsgang repræsenterer en forretningsproces. Den definerer, hvordan et dokument "flyder" gennem systemet, og viser, hvem der skal udføre en opgave eller godkende et dokument. Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:

-   **Ensartede processer** – Du kan bruge arbejdsgangssystemet til at definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter. Du kan bruge arbejdsgangssystemet som en hjælp til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.

-   Synliggørelse af processer – Du kan spore status, historik og performanceværdier for en bestemt arbejdsgangsforekomst. Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.

-   Centraliseret arbejdsliste – Brugerne kan få vist en centraliseret arbejdsliste for at se opgaverne i arbejdsgangen og de godkendelser, der er knyttet til dem. 

**De typer arbejdsgange, du kan oprette**

Tabellen nedenfor viser de typer arbejdsgange, du kan oprette i **Udgift**.


|              <strong>Type</strong>              |                   <strong>Brug denne type til at</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Udgiftsrapport</strong>         |            Oprette godkendelsesarbejdsgange for udgiftsrapporter.             |
|  <strong>Automatisk bogføring af udgiftsrapport</strong>   |        Oprette arbejdsgange for automatisk bogføring for udgiftsrapporter.        |
|       <strong>Udgiftslinjeelement</strong>        |     Oprette godkendelsesarbejdsgange for linjevarer i udgiftsrapporter.      |
| <strong>Automatisk bogføring af udgiftslinjeelement</strong> | Oprette arbejdsgange for automatisk bogføring for linjevarer i udgiftsrapporter. |
|       <strong>Rejserekvisition</strong>       |          Oprette godkendelsesarbejdsgange for rejserekvisitioner.           |
|      <strong>Anmodning om kontantforskud</strong>      |         Oprette arbejdsgange for anmodninger om kontantforskud.          |
|        <strong>Momsopkrævning</strong>        | Oprette godkendelsesarbejdsgange for momsopkrævning.  |

