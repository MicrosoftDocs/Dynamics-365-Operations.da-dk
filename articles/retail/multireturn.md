---
title: Returnere varer på tværs af flere kundeordrer og fakturaer
description: Dette emne beskriver den funktionalitet, der muliggør returneringer på tværs af flere kundeordrer og fakturaer i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
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
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2019
ms.locfileid: "373062"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Returnere varer på tværs af flere kundeordrer og fakturaer

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

I Dynamics 365 for Finance and Operations version 10.0 kan returneringer foretages på tværs af flere ordrer og fakturaer, men i versioner før 10.0 kan returneringer kun behandles for en enkelt faktura ad gangen. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfigurere Retail til at understøtte returneringer på tværs af flere kundeordre og fakturaer

1. Gå til **Detailparametre \> Kundeordrer**.
1. Aktivér parameteren **Aktivér returneringer af flere ordrer**. 

## <a name="process-returns"></a>Behandl returneringerne

Når parameteren er aktiveret, og ændringerne synkroniseres til butikkerne, kan kassereren i butikken kan vælge flere salgsordrer til en kunde til deres returnering.

Når ordrerne markeres, vises en liste over alle produkter, der kan returneres, på tværs af alle fakturaer for ordrerne. Kassereren kan derefter vælge de produkter, der skal returneres. Der oprettes en enkelt returordre for alle de valgte produkter.
