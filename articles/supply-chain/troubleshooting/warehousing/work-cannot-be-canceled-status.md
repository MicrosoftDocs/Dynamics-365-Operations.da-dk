---
title: Arbejde kan ikke annulleres på grund af dets status
description: Arbejde kan ikke annulleres på grund af dets status
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924249"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Arbejde kan ikke annulleres på grund af dets status

Fejlkode: WAX2190

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Du kan ikke annullere arbejdet %1, fordi det har statussen %2.

## <a name="cause"></a>Årsag

Arbejdet kan ikke annulleres i dets aktuelle tilstand.

Arbejdshovedet eller arbejdslinjerne har ikke den forventede værdi for **Arbejdsstatus**. Feltet **Arbejdsstatus** i arbejdshovedet er ikke angivet til *Åben* eller *I gang*.

## <a name="resolution"></a>Løsning

Hvis du vil annullere arbejdet, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.
1. Angiv id'et for det arbejde, du vil annullere, i feltet **Arbejds-id**.
1. Vælg **OK**.
1. Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.

Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).
