---
title: Synkronisere ressourcekapacitet
description: Dette emne giver oplysninger om, hvordan du kan synkronisere en ressources kapacitet på tværs af kalendere og projekter.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760502"
---
# <a name="synchronize-resource-capacity"></a>Synkronisere ressourcekapacitet

[!include [banner](../includes/banner.md)]

Processerne til ressourcesynkronisering hjælper med at sikre, at oplysningerne til kalenderen og basiskalenderen videreføres til ressourceplanlægning for projektet. Hvis kalenderen ændres, foretager processerne de nødvendige opdateringer af planlægningen af projektressourcerne. Processerne forbedrer også ydeevnen, da kalenderens ressourceoplysninger synkroniseres på forhånd. Opdateringer til oplysninger om ressourceplanlægning udføres derfor hurtigere. Vi anbefaler, at du planlægger processerne som en batch i stedet for én ad gangen. Ellers er der risiko for, at nogen vil glemme inklusive-datoerne, hvor oplysningerne sidst blev synkroniseret. Hvis inklusive-datoer ikke bruges, kan der opstå mellemrum under synkronisering af datoer.

![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synkronisér ressourcekapacitet, opkøb

Synkroniseringsprocessen er designet til at synkronisere alle oplysninger i ressourcekalenderen. Disse oplysninger omfatter basiskalenderoplysninger om eventuelle ændringer af projektets tabel for ressourcekalenderkapacitet. Hvis der tilføjes nye ressourcer i projektet, hjælper synkroniseringen med at sikre, at de opdaterede kalenderoplysninger er tilgængelige. Denne synkronisering kan udføres når som helst.

Vi anbefaler, at du bruger en batch. Indstillingerne er tilgængelige under synkronisering af kapacitetsreservationer.

1. Vælg **Projektstyring og regnskab** &gt; **Periodisk** &gt; **Kapacitetssynkronisering** &gt; **Synkronisér ressourcekapacitet akkumuleringer**.
2. Angiv indstillingerne i følgende tabel.

    | Indstilling      | Beskrivelse |
    |-------------|-------------|
    | Periodekode | Vælg datointervalkoden for Finans for at angive start- og slutdatoer for synkroniseringsprocessen for ressourcekapacitet akkumuleringer. |
    | Igangsæt dato  | Angiv startdatoen for synkroniseringsprocessen for ressourcekapacitet akkumuleringer. |
    | Slutdato    | Angiv slutdatoen for synkroniseringsprocessen for ressourcekapacitet akkumuleringer. |

[![Synkroniseringsproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
