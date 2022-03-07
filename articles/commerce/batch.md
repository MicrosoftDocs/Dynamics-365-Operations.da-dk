---
title: Forbedret håndtering af batchsporede varer
description: I dette emne beskrives de forbedringer, der er foretaget i håndteringen af batches for batchsporede varer under bogføringsprocessen for opgørelsen.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 00e1fcb36d685798f3ad7d667805c97bddcceb36
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211147"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Forbedret håndtering af batchsporede varer


[!include [banner](includes/banner.md)]


I POS kan batchnumre ikke hentes til batchsporede varer på tidspunktet for salget. For specifikke konfigurationer, når salg bogføres i hovedkontoret via kundeordrer eller opgørelsesbogføring, vil Microsoft Dynamics-systemet dog forvente, at der findes gyldige batchnumre til varer med batchsporing, og at de skal bruges i faktureringsprocessen.

Hvis der er gyldige batchnumre for produkter, bruges de af faktureringsprocessen for kundeordren og faktureringsprocessen for salgsordren fra opgørelsesbogføring. Ellers kan faktureringsprocessen for kundeordren ikke bogføres, og POS-brugeren modtager en fejlmeddelelse. Opgørelsesbogføringen går derefter i fejltilstand. Denne fejltilstand forekommer, også selvom negativt lager er aktiveret for produkterne.

Forbedringer, der er foretaget i Retail version 10.0.4 og senere, er med til at sikre, at kundeordrefakturering og salgsordrefakturering via opgørelsesbogføring ikke spærres for batchsporede varer, når negativt lager er aktiveret for disse varer, hvis lageret er 0 (nul), eller et batchnummer ikke er tilgængeligt. Den nye funktionalitet bruger et standardbatch-id til salgslinjerne, når batchnumre ikke er tilgængelige.

Hvis du vil definere det standardbatch-id, der bruges til kundeordrer, skal du gå til siden **Commerce-parametre**, åbne fanen **Kundeordrer** i oversigtspanelet **Ordre** og udfylde feltet **Standardbatch-id**.

Hvis du vil definere det standardbatch-id, der bruges til salgsordrefakturering via opgørelsesbogføring, skal du gå til siden **Commerce-parametre**, åbne fanen **Postering** i oversigtspanelet **Opdatering af lager** og udfylde feltet **Standardbatch-id**.

> [!NOTE]
> Denne funktionalitet er kun tilgængelig, når avanceret lagerstyring er aktiveret for det specifikke lagersted og for varerne. I en senere version understøtter funktionen også de scenarier, hvor den avancerede lagerstyring ikke bruges.

> [!NOTE]
> Understøttelse af forbedret håndtering af batchsporede varer under opgørelsesbogføring af scenarier med ikke-avancerede lagerstyring blev introduceret i Retail version 10.0.5.


[!INCLUDE[footer-include](../includes/footer-banner.md)]