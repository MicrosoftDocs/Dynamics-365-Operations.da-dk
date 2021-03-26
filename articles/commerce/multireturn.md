---
title: Returnere varer på tværs af flere kundeordrer og fakturaer
description: Dette emne beskriver den funktionalitet, der muliggør returneringer på tværs af flere kundeordrer og fakturaer i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4d1be6606793d498d01be91de6205e3a45c6dfdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251253"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Returnere varer på tværs af flere kundeordrer og fakturaer

[!include [banner](includes/banner.md)]


I denne artikel beskrives to funktioner, der optimerer kundeordrereturneringer over flere fakturaer. 

## <a name="enable-refunds-over-multiple-captures"></a>Aktivér refusioner via flere opsamlinger

Denne funktion giver mulighed for flere sammenkædede refusioner i forhold til den samme kundeordre. 

1. Gå til arbejdsområdet **Funktionsstyring**, og søg efter **Aktivér refusioner via flere opsamlinger**.
2. Vælg **Aktivér refusioner via flere opsamlinger**, og klik derefter på **Aktivér**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Aktivér beregning af passende moms for returneringer med delvist antal

Denne funktion sikrer, at momsen i sidste ende er lig med det oprindeligt opkrævede momsbeløb, når en ordre returneres ved hjælp af flere fakturaer. 

1. Gå til arbejdsområdet **Funktionsstyring**, og søg efter **Aktivér beregning af passende moms for returneringer med delvist antal**.
2. Vælg **Aktivér beregning af passende moms for returneringer med delvist antal**, og klik derefter på **Aktivér**. 


## <a name="process-returns"></a>Behandl returneringerne

Når disse funktioner er aktiveret, og ændringerne synkroniseres til butikkerne, kan kassereren i butikken kan vælge flere salgsordrer til en kunde til deres returnering.

Når ordrerne markeres, vises en liste over alle produkter, der kan returneres, på tværs af alle fakturaer for ordrerne. Kassereren kan derefter vælge de produkter, der skal returneres. Der oprettes en enkelt returordre for alle de valgte produkter.

Hvis ordren returneres fuldt ud, er det beløb, der returneres til kunden, lig med det momsbeløb, der oprindeligt blev opkrævet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]