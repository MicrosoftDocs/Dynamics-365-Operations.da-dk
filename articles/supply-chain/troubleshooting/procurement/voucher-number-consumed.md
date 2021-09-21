---
title: Et bilagsnummer til en produktkvittering forbruges, også selvom der ikke oprettes et bilag
description: Bilagsnummeret på produktkvitteringen forbruges, selvom der ikke genereres et økonomisk bilag under produktkvittering
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475898"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Et bilagsnummer til en produktkvittering forbruges, også selvom der ikke oprettes et bilag

## <a name="symptoms"></a>Symptomer

Bilagsnummeret på produktkvitteringen forbruges, selvom der ikke genereres et økonomisk bilag under produktkvittering.

## <a name="resolution"></a>Løsning

Hvis indstillingen **Periodiser passiver ved produktmodtagelse** er angivet til *Nej* for varemodelgruppen, vil der ikke blive bogført til Finans. Der vil dog blive registreret en fysisk hændelse med det formål at foretage regnskabsføring i en reskontro, og den pågældende hændelse kræver et bilagsnummer. Dette bilagsnummer er det bilagsnummer, der refereres til i lagertransaktionerne.

Det anbefales, at du angiver indstillingen **Periodiser passiver ved produktmodtagelse** til *Ja* som beskrevet i følgende blogindlæg: [Bogføre diverse gebyrer på tidspunktet for produktmodtagelse](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
