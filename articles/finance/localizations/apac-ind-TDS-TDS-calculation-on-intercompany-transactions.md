---
title: Beregning af kildeskat for interne transaktioner
description: Denne artikel beskriver den proces, der bruges til at beregne kildeskat (TDS – Tax Deducted at Source) på interne transaktioner i faser.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c27bea997804f2c5eff6be2b20064b272ccd062f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888967"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>Beregning af kildeskat for interne transaktioner

[!include [banner](../includes/banner.md)]

Denne artikel beskriver den proces, der bruges til at beregne kildeskat (TDS – Tax Deducted at Source) på interne transaktioner i faser.

Når der oprettes en intern indkøbsordre eller salgsordre, bruges den standardgruppe for kildeskat, som er defineret for debitoren eller kreditoren, til at beregne skattebeløbet. Når fakturaen bogføres, bogføres skattebeløbet på de relevante konti for tilgodehavende eller skyldig skat.

Der oprettes automatisk en intern salgsordre eller indkøbsordre for den oprindelige indkøbsordre eller salgsordre. Standardskattegruppen vises på den interne ordre, så kildeskatten kan beregnes. Du kan ændre kildeskattegruppen. Fakturaen kan kun bogføres, hvis nettofakturabeløbet på den interne ordre, som er oprettet automatisk, svarer til nettofakturabeløbet på den oprindelige ordre. (Nettobeløbet er fakturabeløbet, efter kildeskatten er fratrukket).

Der oprettes f.eks. en salgsfaktura på 50.000, og kildeskattegruppen **10 %** bliver tilknyttet. Det bogførte fakturabeløb er 45.000, og det bogførte skattebeløb for salgsfakturaen er 5.000. Der oprettes automatisk en indkøbsordre for den interne salgsordre, og kildeskattegruppen **10 %** bliver tilknyttet. Hvis du ændrer TDS-gruppen til **15 %**, kan du ikke bogføre fakturaen, da nettofakturabeløbet for den interne salgsordre, der er oprettet automatisk, ikke svarer til nettofakturabeløbet på den oprindelige salgsordre.

Der oprettes og bogføres automatisk en betalingskladde for en intern faktura. Denne betalingskladde kan kun bogføres, hvis nettobetalingsbeløbet på den svarer til nettobetalingsbeløbet på den oprindelige betalingskladde.
