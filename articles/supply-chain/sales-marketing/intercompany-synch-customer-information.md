---
title: Synkronisere oplysninger om interne debitorer
description: Dette emne forklarer synkronisering af kundeoplysninger for interne handelsordrer
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
ms.openlocfilehash: c82216c8391f6c447bec74f25cd16b9db18d468d
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548175"
---
# <a name="synchronize-intercompany-customer-information"></a>Synkronisere oplysninger om interne debitorer

[!include [banner](../../includes/banner.md)]

Debitoroplysninger synkroniseres, hvis feltet **Kundeoplysninger** er aktiveret, når salgsordren oprettes, eller når der ændres i oplysningerne om debitor, leverandørreference eller debitorrekvisitionsnummer.

Du kan altid ændre værdien i disse synkroniseringsfelter. Du kan imidlertid kun bestemme, om værdien skal kopieres til andre interne ordrer ved at vælge denne parameter. Hvis du har aktiveret feltet **Kundeoplysninger** på den interne salgsordre, synkroniseres en ændring i den interne salgsordre til den interne indkøbsordre. Hvis du også har aktiveret feltet **Kundeoplysninger** på den interne indkøbsordre, synkroniseres det ligeledes tilbage til den oprindelige salgsordre.

> [!NOTE]
> Hvis du har aktiveret feltet **Kundeoplysninger** på både den interne indkøbsordre og den interne salgsordre, overstyres de opdateringer, der er udført af én person i ét firma, af opdateringer, der er udført af en anden person i et andet firma på samme ordre.

Den bedste fremgangsmåde er at aktivere feltet **Kundeoplysninger** på den interne indkøbsordre. Det gør det muligt at foretage synkronisering mellem den oprindelige salgsordre og den interne indkøbsordre og fra den interne indkøbsordre til den interne salgsordre.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
