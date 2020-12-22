---
title: Redigere økonomiske dimensioner for detailtransaktioner
description: Dette emne beskriver, hvordan du redigerer økonomiske dimensioner for detailtransaktioner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: e26bd4eb53fa44330f15c7cda004cb3d19dfec6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458724"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Redigere økonomiske dimensioner for detailtransaktioner

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du redigerer økonomiske dimensioner for detailtransaktioner i Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>Redigere økonomiske dimensioner

Hvis du vil redigere økonomiske dimensioner for detailtransaktioner i hovedkontoret Commerce, skal du følge disse trin.

1. Åbn siden **Konfiguration af økonomiske dimensioner til integrering af applikationer**.
1. Vælg den aktive post **Standarddimensioner til integrering**.
1. På oversigtspanelet **Økonomiske dimensioner** skal du sørge for, at alle de dimensioner, du vil redigere i Excel-regnearket, findes på listen **Valgte**. Du kan finde flere oplysninger under [Dataenheder](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).
1. Overfør og åbn Excel-filen fra siden **Opgørelser**, siden **Detailtransaktioner** eller feltet **Transaktionsvalideringsfejl** i arbejdsområdet **Butiksøkonomi**.
1. Hvis du vil ændre den økonomiske dimension for transaktionen, skal du vælge **Design** og derefter vælge blyantsymbolet ud for rækken **Transaktion (reviderbar)**.
1. Find og markér feltet **FinancialDimensionDisplayValue** , vælg en celle i øverste del af Excel-regnearket, og vælg derefter **Tilføj etiket**.
1. Markér en celle under den celle, du har valgt i forrige trin, vælg **Tilføj værdi**, og vælg derefter **Opdater**. De økonomiske dimensioner føjes til Excel-regnearket, og de kan derefter redigeres og publiceres.
1. Hvis du vil ændre dimensionerne på transaktionslinjerne, skal du vælge rækken **Salgstransaktioner (reviderbar)**, vælge blyantsymbolet og derefter gentage trin 6 og 7.
1. Hvis du vil ændre dimensionerne på betalingslinjerne, skal du vælge rækken **Betalingstransaktioner (reviderbar)**, vælge blyantsymbolet og derefter gentage trin 6 og 7.

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner](edit-cash-trans.md)

[Redigere og overvåge onlineordre- og asynkrone kundeordretransaktioner](edit-order-trans.md)

[Oprette en Excel-projektmappe for at redigere detailtransaktioner](create-excel-edit.md)

[Føje felter til en Excel-projektmappe for at redigere detailtransaktioner](add-fields-excel.md)
