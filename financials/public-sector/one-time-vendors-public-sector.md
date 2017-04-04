---
title: "Engangsleverandører i den offentlige sektor"
description: Denne artikel indeholder oplysninger om, hvordan du opretter en engangskreditor og -faktura, og hvordan du importerer og opretter flere engangskreditorer og -fakturaer.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerTransVoucher, SysConfiguration, Tax1099Summary, VendTableListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19801
ms.assetid: 403857a3-bebb-4ff7-b1b5-c88f41fc18ae
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: d64f9228c538a08a2fc938bc6ff4ce11278b6fed
ms.openlocfilehash: a0f4051ec32891396dc4ebf6bd5d19b8ba7cc3ec
ms.lasthandoff: 03/31/2017


---

# <a name="one-time-vendors-in-the-public-sector"></a>Engangsleverandører i den offentlige sektor

Denne artikel indeholder oplysninger om, hvordan du opretter en engangskreditor og -faktura, og hvordan du importerer og opretter flere engangskreditorer og -fakturaer. 

Der kan være situationer, hvor du er nødt til at oprette en faktura for en ny kreditor, som du ikke har nogen regelmæssig relation til. I Microsoft Dynamics 365 for operationer, hvis godkendelse eller en aftale i form af en indkøbsordre ikke påkrævet, kan du hurtigt oprette en faktura på samme tid, som du opretter en post for kreditoren. Det kunne f.eks. være, at du er nødt til at betale referencer eller refusion, men der ikke findes en overordnet kreditorpost. Der kan også være situationer, hvor du er nødt til at oprette flere fakturaer for nye kreditorer, som du ikke har nogen regelmæssig relation til. Hvis der hverken kræves godkendelse eller en indkøbsordre, kan du hurtigt oprette fakturaer, samtidig med at du opretter poster for leverandørerne. Det kan f.eks. være, at du vil understøtte kreditorbetalinger af deltagelse i jury, registreringsbetalinger og refusioner til kreditorer eller andre betalinger, men der ikke findes hovedkreditorposter. Yderligere oplysninger finder du [planlægning for engangsleverandører i offentligt](plan-one-time-vendors-public-sector.md).

## <a name="how-do-i-create-a-onetime-vendor-and-invoice"></a>Hvordan opretter jeg en enkelt kreditor- og fakturakonto?
Kreditorposten bruger værdier fra standardengangskreditorkontoen, medmindre der er indtastet nye værdier. Der er angivet en konto i afsnittet **Generelt** på siden **Kreditorparametre**. Du kan få vist kontooplysningerne på siden **Alle kreditorer** og derefter klikke på kreditorkontonummeret for standardengangskreditoren.

## <a name="how-do-i-import-and-create-multiple-onetime-vendors-and-invoices"></a>Hvordan importerer og oprette flere enkelt leverandører og fakturaer?
Hvis du vil oprette flere engangskreditorer og fakturaer, du først oprette en fil, der indeholder det kreditor- og fakturaoplysninger og derefter importere filen til en midlertidig tabel i Microsoft Dynamics 365 for operationer. Derefter skal du behandle den importerede fil og generere fakturaerne. Du kan se flere oplysninger om, hvordan du opretter filen i [Planlægning for engangsleverandører i den offentlige sektor](plan-one-time-vendors-public-sector.md).  


