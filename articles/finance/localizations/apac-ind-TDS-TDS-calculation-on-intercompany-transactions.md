---
title: Beregning af kildeskat for interne transaktioner
description: Dette emne beskriver den proces, der bruges til at beregne kildeskat (TDS – Tax Deducted at Source) på interne transaktioner i faser.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c978c84891a0c1ce5a079484eec24590283027c4
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407916"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>Beregning af kildeskat for interne transaktioner

[!include [banner](../includes/banner.md)]

Dette emne beskriver den proces, der bruges til at beregne kildeskat (TDS – Tax Deducted at Source) på interne transaktioner i faser.

Når der oprettes en intern indkøbsordre eller salgsordre, bruges den standardgruppe for kildeskat, som er defineret for debitoren eller kreditoren, til at beregne skattebeløbet. Når fakturaen bogføres, bogføres skattebeløbet på de relevante konti for tilgodehavende eller skyldig skat.

Der oprettes automatisk en intern salgsordre eller indkøbsordre for den oprindelige indkøbsordre eller salgsordre. Standardskattegruppen vises på den interne ordre, så kildeskatten kan beregnes. Du kan ændre kildeskattegruppen. Fakturaen kan kun bogføres, hvis nettofakturabeløbet på den interne ordre, som er oprettet automatisk, svarer til nettofakturabeløbet på den oprindelige ordre. (Nettobeløbet er fakturabeløbet, efter kildeskatten er fratrukket).

Der oprettes f.eks. en salgsfaktura på 50.000, og kildeskattegruppen **10 %** bliver tilknyttet. Det bogførte fakturabeløb er 45.000, og det bogførte skattebeløb for salgsfakturaen er 5.000. Der oprettes automatisk en indkøbsordre for den interne salgsordre, og kildeskattegruppen **10 %** bliver tilknyttet. Hvis du ændrer TDS-gruppen til **15 %**, kan du ikke bogføre fakturaen, da nettofakturabeløbet for den interne salgsordre, der er oprettet automatisk, ikke svarer til nettofakturabeløbet på den oprindelige salgsordre.

Der oprettes og bogføres automatisk en betalingskladde for en intern faktura. Denne betalingskladde kan kun bogføres, hvis nettobetalingsbeløbet på den svarer til nettobetalingsbeløbet på den oprindelige betalingskladde.
