---
title: Returnere varer på tværs af flere kundeordrer og fakturaer
description: Denne artikel beskriver den funktionalitet, der muliggør returneringer på tværs af flere kundeordrer og fakturaer i Dynamics 365 Commerce.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 65ef700db5a81c49a962fd388af54e7811c088d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890315"
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
