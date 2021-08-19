---
title: Arbejde kan ikke annulleres, fordi det er blokeret
description: Arbejde kan ikke annulleres, fordi det er blokeret
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a24f199484c7596189b19e4cddf344e9186c6044edd2906affca9b530de44168
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722193"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Arbejde kan ikke annulleres, fordi det er blokeret

Fejlkode: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Arbejde %1 kan ikke annulleres, fordi det er blokeret af årsagstype %2. Arbejdets blokering skal fjernes, før det kan annulleres.

## <a name="cause"></a>Årsag

Arbejdet er blokeret og kan ikke annulleres.

På siden **Arbejde** under fanen **Generelt** er indstillingen **Blokeret** angivet til *Ja*. Denne indstilling angiver, at arbejdet er blokeret. Fanen **Blokeringsårsager** viser, hvorfor arbejdet er blokeret.

## <a name="resolution"></a>Løsning

Hvis du vil fjerne blokeringen af arbejdet, skal du vælge fanen **Blokeringsårsager** og derefter følge et af disse trin:

- Hvis feltet **Årsag til blokering af arbejde** er angivet til *Ikke-defineret årsag*: Vælg **Fjern blokering af arbejde** i gruppen **Arbejde** under fanen **Arbejde** i handlingsruden.
- Hvis feltet **Årsag til blokering af arbejde** er angivet til *Behandler bølge*: Vælg **Bølge** i gruppen **Relaterede oplysninger** under fanen **Relaterede oplysninger** i handlingsruden. Vælg **Ryd op i bølgedata** i gruppen **Bølge** under fanen **Bølge** på siden **Bølger** i handlingsruden.

## <a name="workaround"></a>Løsning

Hvis de foregående trin ikke løser problemet, kan du annullere arbejdet med følgende fremgangsmåde.

1. Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.
1. I feltet **Arbejds-id** skal du angive id'et for det arbejde, du vil annullere, og som i øjeblikket har en værdien for **Arbejdsstatus** *Åben*, *I gang*, *Annulleret*, *Kombineret* eller *Lukket*.
1. Vælg **OK**.
1. Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.

Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).
