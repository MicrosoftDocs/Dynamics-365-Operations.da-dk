---
title: Antallet kan ikke reduceres, når en salgsordre annulleres
description: Antallet kan ikke reduceres, når en salgsordre annulleres.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3453c83b5e8ead4269a6054167d73a0cd12381ba374b98bc407c01edaa68a1c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752628"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Antallet kan ikke reduceres, når en salgsordre annulleres

Fejlkode: SYS138831

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Antallet kan ikke reduceres. Antallet af lagertransaktioner i en ordre er for lavt, fordi antallet eller en del af det refereres til fra en udlagringsordre eller en produktionsordre eller er markeret i forhold til andre transaktioner.

## <a name="cause"></a>Årsag

Hvis arbejdet er knyttet til en salgsordre, kan du ikke annullere salgsordren, før arbejdet er annulleret og tilbageført. Dette krav gælder, selvom det arbejde, der er tilknyttet salgsordren, er lukket.

## <a name="resolution"></a>Løsning

Du kan løse dette problem ved at udføre følgende opgaver:

1. Annuller åbent arbejde.
1. Slet lasten.
1. Reducer det antal, der plukkes.

### <a name="cancel-open-work"></a>Annullere åbent arbejde

Hvis du vil annullere åbent arbejde, skal du benytte følgende fremgangsmåde.

1. Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.
1. I feltet **Arbejds-id** skal du angive id'et for det arbejde, du vil annullere, og som i øjeblikket har en værdien for **Arbejdsstatus** *Åben*, *I gang*, *Annulleret*, *Kombineret* eller *Lukket*.
1. Vælg **OK**.
1. Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.

### <a name="delete-the-load"></a>Slette lasten

Benyt følgende fremgangsmåde for at slette en last.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Åbn den relevante salgsordre.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Lagersted \> Arbejdsdetaljer**.
1. Gå til handlingsruden og vælg **Annuller arbejde** i gruppen **Arbejde** under fanen **Arbejde** på siden **Arbejde**.
1. Bekræft, at feltet **Arbejdsstatus** er angivet til *Annulleret*.
1. Luk siden **Arbejde**.
1. På siden med salgsordredetaljer skal du i oversigtspanelet **Salgsordrelinjer** vælge **Lagersted \> Lastdetaljer**.
1. Vælg **Slet** i handlingsruden.
1. Vælg **Ja** for at bekræfte, at du vil slette lasten.
1. Luk siden **Last**.

### <a name="reduce-the-picked-quantity"></a>Reducere det antal, der plukkes

Når alt arbejde er annulleret, skal du benytte følgende fremgangsmåde for at reducere det plukkede antal.

1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Åbn den relevante salgsordre.
1. I oversigtspanelet **Salgsordrelinjer** skal du vælge **Opdater linje \> Pluk** på værktøjslinjen.
1. Vælg den linje, hvor feltet **Afgangsstatus** er angivet til **Plukket** i sektionen **Transaktioner** på siden *Pluk*.
1. Vælg **Tilføj pluklinje** på værktøjslinjen i sektionen **Transaktioner**.
1. Vælg **Bekræft pluk af alt** på værktøjslinjen i sektionen **Pluklinjer**.
1. Luk siden **Pluk**.
1. På siden med salgsordredetaljer i handlingsruden skal du vælge **Annuller** i gruppen **Vedligehold** under fanen **Salgsordre**.
1. Vælg **Ja** for at bekræfte, at du vil annullere salgsordren.
