---
title: Interne batch- og serienumre
description: Dette emne forklarer, hvad der sker, når du registrerer batchnumre og serienumre for interne ordrer
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
ms.openlocfilehash: 4da936263bb57c24eeb7021ac61b3945bb2777fb
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548182"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Interne batch- og serienumre

[!include [banner](../../includes/banner.md)]

Firmaer, der bruger serie- eller batchnumre til at spore deres varer, skal også spore serienumrene og batchnumrene for plukkede varer. Den interne funktion automatiserer skub/træk af serienumre og batchnumre fra ét firma til et andet. Når du registrerer batchnumre og serienumre for varerne i en intern salgsordre, kan du angive, at programmet automatisk skal overføre - skubbe - disse numrene til den interne indkøbsordre og den oprindelige salgsordre. Du skal definere de relevante parametre på siden **Intern** for salgsordren:

- Hvis du markerer **Batch-nummer**-feltet på siden **Salgsordrepolitikker**, synkroniseres batchnummeret efter lagertransaktionerne på de interne indkøbsordrelinjer, når følgesedlen bogføres for den interne salgsordre.
- Hvis du markerer feltet **Serienummer**, synkroniseres serienumrene efter lagertransaktionerne på de interne indkøbsordrelinjer, når følgesedlen bogføres for den interne salgsordre.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
