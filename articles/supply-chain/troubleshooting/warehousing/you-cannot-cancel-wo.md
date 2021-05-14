---
title: Du kan ikke annullere arbejde, der er angivet for en bruger
description: Du kan ikke annullere arbejde, der er angivet for en bruger
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924395"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Du kan ikke annullere arbejde, der er angivet for en bruger

Fejlkode: WAX708

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Du kan ikke annullere arbejde, der er for en bruger.

## <a name="cause"></a>Årsag

Arbejdet låses af en bruger og kan ikke annulleres. Hvis du vil bekræfte dette, skal du åbne arbejds-id'et og derefter åbne fanen **Generelt**. Hvis arbejdet er låst, er feltet **Arbejdsstatus** angivet til *Igangværende*, og feltet **Låst efter** vil være angivet til et bruger-id.

## <a name="resolution"></a>Løsning

Hvis du vil annullere arbejdet, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.
1. Angiv id'et for det arbejde, du vil annullere, i feltet **Arbejds-id**.
1. Vælg **OK**.
1. Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.

Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).
