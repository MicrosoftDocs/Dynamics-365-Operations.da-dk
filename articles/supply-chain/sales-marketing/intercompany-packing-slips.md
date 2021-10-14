---
title: Interne følgesedler
description: Dette emne beskriver, hvordan der genereres og udskrives følgesedler for interne transaktioner
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 72d052d2daba90d49ba372fb3fb480bdd0877398
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548178"
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
