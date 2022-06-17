---
title: Forbedret håndtering af batchsporede varer
description: I denne artikel beskrives den forbedrede håndtering af batchsporede varer under processen til bogføring af opgørelsen i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 736ab8dd21f04d7119cca6d53bfeb5e408b8cbd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881872"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Forbedret håndtering af batchsporede varer

[!include [banner](includes/banner.md)]

I denne artikel beskrives den forbedrede håndtering af batchsporede varer under processen til bogføring af opgørelsen i Microsoft Dynamics 365 Commerce.

I Dynamics 365 Commerce POS kan batchnumre ikke hentes til batchsporede varer på tidspunktet for salget. For specifikke konfigurationer vil Commerce dog forvente, at der findes gyldige batchnumre til varer med batchsporing, når salg bogføres i Commerce-hovedkontoret via kundeordrer eller opgørelsesbogføring, og at de skal bruges i faktureringsprocessen.

Hvis der er gyldige batchnumre for produkter, bruges begge af faktureringsprocessen for kundeordren og faktureringsprocessen for salgsordren fra opgørelsesbogføring. Hvis gyldige batchnumre ikke er tilgængelige for produkter, kan debitorordre faktureringsprocessen ikke bogføres, og kassebrugeren modtager en fejlmeddelelse. Bogføringen af opgørelsen går derefter videre til fejltilstand, også selvom negativt lager er blevet slået til for produkterne.

Forbedringer, der er foretaget i hjælpen til Commerce, sikrer, at kundeordrefakturering og salgsordrefakturering via opgørelsesbogføring ikke spærres for batchsporede varer, når negativt lager er aktiveret for disse varer, hvis lageret er 0 (nul), eller et batchnummer ikke er tilgængeligt. Den forbedrede funktionalitet bruger et standardbatch-id til salgslinjerne, når batchnumre ikke er tilgængelige.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Definere det standardbatch-id, der bruges til debitorordrer

Du definerer det standardbatch-id, der bruges til debitorordrer, ved at følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** i Commerce-hovedkontoret.
1. Angiv en værdi i feltet **Standardbatch-id** på fanen **Debitorordrer** i oversigtspanelet **Ordre**.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Definer det standardbatch-id, der skal bruges til salgsordrefakturering via bogføring af opgørelser

Du definerer det standardbatch-id, der skal bruges til salgsordrefakturering via bogføring af opgørelser, ved at følge disse trin.

1. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** i Commerce-hovedkontoret.
1. Angiv en værdi i feltet **Standardbatch-id** på fanen **Bogføring** i oversigtspanelet **Opdatering af lager**.

> [!NOTE]
> - Funktionen Standardbatch-id er kun tilgængelig, når avanceret lagerstyring er aktiveret for det specifikke lagersted og for varerne. I en fremtidig version understøtter funktionen Standardbatch-id også de scenarier, hvor den avanceret lagerstedsadministration ikke bruges.
> - Understøttelse af den forbedrede håndtering af batchsporede varer under opgørelsesbogføring af scenarier med ikke-avancerede lagerstedsadministration blev introduceret i Commerce version 10.0.5 udgaven.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
