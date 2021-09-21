---
title: Standardmomsgruppe og kasserabat angives ikke fra fakturakontoen
description: Der udfyldes ikke en standardmomsgruppe og en standardkasserabat fra fakturakontoen
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475897"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Standardmomsgruppe og kasserabat angives ikke fra fakturakontoen

## <a name="symptoms"></a>Symptomer

Hvis du bruger en fakturakonto, der er forskellig fra debitorkontoen, udfyldes der ikke en standardmomsgruppe og en standardkasserabat fra fakturakontoen, når der oprettes en indkøbsordre.

## <a name="resolution"></a>Løsning

Denne funktionsmåde er tilsigtet. Standardværdierne for momsgruppen, kasserabatter og andre prisoplysninger er baseret på debitorkontoen – ikke fakturakontoen.
