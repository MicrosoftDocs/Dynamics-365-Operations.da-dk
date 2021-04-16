---
title: Indkøbs- og forsyningsarbejdsgange
description: I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen. Du kan oprette en arbejdsgang for at oprette en godkendelsesproces.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd9ee69e180f2ff605c4f373a95d2346ccc73c0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807938"
---
# <a name="procurement-and-sourcing-workflows"></a>Indkøbs- og forsyningsarbejdsgange

[!include [banner](../includes/banner.md)]

I visse organisationer kræves det, at indkøbsrekvisitioner og indkøbsordrer skal godkendes af en anden bruger end den person, som har indtastet transaktionen. Du kan oprette en arbejdsgang for at oprette en godkendelsesproces.

En arbejdsgang repræsenterer en forretningsproces. Den definerer, hvordan et dokument "flyder" gennem systemet, og viser, hvem der skal udføre en opgave eller godkende et dokument. Der er flere fordele ved at bruge arbejdsgangssystemet i organisationen:

- **Ensartede processer** – Du kan bruge arbejdsgangssystemet til at definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter. Du kan bruge arbejdsgangssystemet som en hjælp til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.
- **Synliggørelse af processer** – Du kan spore status, historik og performanceværdier for en bestemt arbejdsgangsforekomst. Dette hjælper dig med at bestemme, om der skal foretages ændringer i arbejdsgangen for at forbedre effektiviteten.
- **Centraliseret arbejdsliste**– Brugerne kan få vist en centraliseret arbejdsliste for at få vist opgaverne i arbejdsgangen og godkendelser, der er tildelt til dem på tværs af alle arbejdsprocesser, som de deltager i. Dette er tilgængeligt på siden Workflowopgaver.

## <a name="the-types-of-workflows-that-you-can-create"></a>De typer arbejdsgange, du kan oprette

Der er følgende tilgængelige arbejdsgangstyper for Indkøb og forsyning.

| Type | Brug denne type til at |
|---|---|
| Gennemgang af indkøbsrekvisition | Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsrekvisitioner. |
| Evaluering af indkøbsrekvisitionslinjer | Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsrekvisitionslinjer. |
| Arbejdsgang for indkøbsordre | Opret evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer. |
| Arbejdsgang for indkøbsordrelinje | Oprette evaluerings- og godkendelsesarbejdsgange for indkøbsordrelinjer. |
| Arbejdsgang for ansøgning om tilføjelse af kreditor | Oprette arbejdsgange for gennemsyn og godkendelse for at tilføje nye kreditorer via kreditoranmodninger. |

> [!IMPORTANT]
> Når du tilføjer en ny arbejdsproces, kan du også se følgende forældede arbejdsprocesser, der er angivet i dialogboksen **Opret arbejdsproces**. Disse er relateret til den *bekræftelse af tilgang*-funktion, der var tilgængelig i [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), men som nu frarådes. Disse arbejdsprocesser understøttes ikke i øjeblikket.
> 
> - Arbejdsgang for besked om dato for forfalden til levering
> - Arbejdsgang for besked om modtaget faktura
> - Arbejdsgang for besked om, at produktkvitteringen mislykkedes
> - Arbejdsgang til besked om afvisning af ikke-bekræftet produktkvittering

## <a name="creating-a-workflow"></a>Oprettelse af en arbejdsgang

Hvis du vil oprette en arbejdsgang, skal du gå til Indkøb og forsyning &gt; Opsætning &gt; Indkøbs- og forsyningsarbejdsgange og oprette en ny arbejdsgang ved at vælge den type arbejdsgang, du vil oprette. 

På lærredet for arbejdsgangen kan du trække arbejdsgangselementer til designeren og sammenkæde elementerne til en arbejdsgang. Arbejdsgangselementerne bør være konfigureret. Du kan konfigurere, hvilken deltager der bør træffe foranstaltninger, i forbindelse med arbejdsgangselementer af typerne godkendelse og opgave.

## <a name="types-of-participants"></a>Deltagertyper

Du kan knytte et godkendelsestrin til følgende deltagergrupper.

| Brugergruppe | Beskrivelse |
|---|---|
| Deltager | Tildel godkendelsestrinnet til medlemmer af en gruppe eller en rolle. |
| Hierarki | Tildel godkendelsestrinnet til brugere i et bestemt organisationshierarki. |
| Arbejdsgangsbruger | Tildel godkendelsestrinnet til brugere i denne arbejdsgang. |
| Kø | Tildel godkendelsestrinnet til en workflowopgavekø. |
| Bruger | Tildel godkendelsestrinnet til bestemte brugere. |

## <a name="additional-resources"></a>Yderligere ressourcer

- [Definition af forretningsprocesarbejdsgange for indkøbsrekvisitioner](https://www.microsoft.com/download/details.aspx?id=101821)
- [Arbejdsgang for indkøbsrekvisitioner](purchase-requisitions-workflow.md)
- [Modtage kreditorer](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]