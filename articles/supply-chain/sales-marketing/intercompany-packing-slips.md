---
title: Interne følgesedler
description: Denne artikel beskriver, hvordan der genereres og udskrives følgesedler for interne transaktioner
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3516058bbf925df4b0a0c75286a3d97457cc1e69
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900848"
---
# <a name="intercompany-packing-slips"></a>Interne følgesedler

## <a name="generate-intercompany-packing-slips"></a>Generere interne følgesedler

[!include [banner](../../includes/banner.md)]

Hvis du arbejder med direkte levering, genereres følgesedlen altid automatisk både på den interne indkøbsordre og på den oprindelige salgsordre, når du genererer følgesedlen på den interne salgsordre. Den interne indkøbsordrefaktura baseres på følgesedlen til den interne indkøbsordre, der er genereret tidligere.

Hvis du opdaterer noget på følgesedlen på den interne salgsordre, afspejles disse opdateringer både på den interne indkøbsordre og den oprindelige salgsordre.

Hvis du ikke arbejder med direkte levering, skal du generere følgesedlen manuelt på den interne salgsordre, den interne indkøbsordre og den oprindelige salgsordre.

## <a name="print-intercompany-packing-slips"></a>Udskrive interne følgesedler

[!include [banner](../../includes/banner.md)]

Hvis du arbejder med direkte levering, kan der automatisk udskrives en følgeseddel for den interne indkøbsordre og den oprindelige salgsordre, når du bogfører følgesedlen på den interne salgsordre.

Hvis der automatisk skal udskrives følgesedler, skal du markere begge felter til **automatisk udskrivning af følgesedler** på siden **Intern handel** for indkøbsordrer.

Hvis du opdaterer følgesedlen på den interne salgsordre, afspejles ændringerne automatisk på den interne indkøbsordre og den oprindelige salgsordre.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
