---
title: Engangsleverandører i den offentlige sektor
description: Denne artikel indeholder oplysninger om, hvordan du opretter en engangskreditor og -faktura, og hvordan du importerer og opretter flere engangskreditorer og -fakturaer.
author: v-kiarnd
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: v-kiarnd
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 19801
ms.assetid: 403857a3-bebb-4ff7-b1b5-c88f41fc18ae
ms.search.industry: Public sector
ms.search.form: LedgerTransVoucher, SysConfiguration, Tax1099Summary, VendTableListPage
ms.openlocfilehash: a99454fb66ff1ad78d159d1af54c25e76006bc8a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275859"
---
# <a name="one-time-vendors-in-the-public-sector"></a>Engangsleverandører i den offentlige sektor

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om, hvordan du opretter en engangskreditor og -faktura, og hvordan du importerer og opretter flere engangskreditorer og -fakturaer. 

Der kan være situationer, hvor du er nødt til at oprette en faktura for en ny kreditor, som du ikke har nogen regelmæssig relation til. Når der ikke kræves godkendelse eller en aftale i form af en indkøbsordre, kan du i Dynamics 365 Finance hurtigt oprette en faktura, samtidig med at du opretter en post for kreditoren. Det kunne f.eks. være, at du er nødt til at betale referencer eller refusion, men der ikke findes en overordnet kreditorpost. Der kan også være situationer, hvor du er nødt til at oprette flere fakturaer for nye kreditorer, som du ikke har nogen regelmæssig relation til. Hvis der hverken kræves godkendelse eller en indkøbsordre, kan du hurtigt oprette fakturaer, samtidig med at du opretter poster for leverandørerne. Det kan f.eks. være, at du vil understøtte kreditorbetalinger af deltagelse i jury, registreringsbetalinger og refusioner til kreditorer eller andre betalinger, men der ikke findes hovedkreditorposter. Du kan finde flere oplysninger under [Planlægning for engangsleverandører i den offentlige sektor](plan-one-time-vendors-public-sector.md).

## <a name="how-do-i-create-a-onetime-vendor-and-invoice"></a>Hvordan opretter jeg en engangskreditor og -faktura?
Kreditorposten bruger værdier fra standardengangskreditorkontoen, medmindre der er indtastet nye værdier. Der er angivet en konto i afsnittet **Generelt** på siden **Kreditorparametre**. Du kan få vist kontooplysningerne på siden **Alle kreditorer** og derefter klikke på kreditorkontonummeret for standardengangskreditoren.

## <a name="how-do-i-import-and-create-multiple-onetime-vendors-and-invoices"></a>Hvordan importerer og opretter jeg flere engangskreditorer og fakturaer?
Hvis du vil oprette flere engangskreditorer og fakturaer, skal du først oprette en fil, der indeholder oplysninger om kreditoren og fakturaen, og derefter importere filen til en midlertidig tabel. Derefter skal du behandle den importerede fil og generere fakturaerne. Du kan se flere oplysninger om, hvordan du opretter filen i [Plan for engangsleverandører i den offentlige sektor](plan-one-time-vendors-public-sector.md).  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
