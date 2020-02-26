---
title: Returnere varer på tværs af flere kundeordrer og fakturaer
description: Dette emne beskriver den funktionalitet, der muliggør returneringer på tværs af flere kundeordrer og fakturaer i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004452"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Returnere varer på tværs af flere kundeordrer og fakturaer

[!include [banner](includes/banner.md)]


Returneringer kan foretages på tværs af flere kundeordrer og fakturaer. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfigurere Commerce til at understøtte returneringer på tværs af flere kundeordre og fakturaer

1. Gå til **Commerce-parametre \> Kundeordrer**.
1. Aktivér parameteren **Aktivér returneringer af flere ordrer**. 

## <a name="process-returns"></a>Behandl returneringerne

Når parameteren er aktiveret, og ændringerne synkroniseres til butikkerne, kan kassereren i butikken kan vælge flere salgsordrer til en kunde til deres returnering.

Når ordrerne markeres, vises en liste over alle produkter, der kan returneres, på tværs af alle fakturaer for ordrerne. Kassereren kan derefter vælge de produkter, der skal returneres. Der oprettes en enkelt returordre for alle de valgte produkter.
