---
title: Den seneste lukkede arbejdslinje skal være Læg på lager
description: Den seneste lukkede arbejdslinje skal være Læg på lager
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
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924369"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Den seneste lukkede arbejdslinje skal være Læg på lager

Fejlkode: WAX1285

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Den seneste lukkede arbejdslinje skal være Læg på lager.

## <a name="cause"></a>Årsag

Arbejdet kan ikke annulleres i dets aktuelle tilstand.

På den sidste arbejdslinje er feltet **Arbejdsstatus** angivet til *Lukket*, men feltet **Arbejdstype** er ikke angivet til *Læg på lager*.

## <a name="resolution"></a>Løsning

Hvis du vil annullere arbejdet, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.
1. Angiv id'et for det arbejde, du vil annullere, i feltet **Arbejds-id**.
1. Vælg **OK**.
1. Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.

Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).
