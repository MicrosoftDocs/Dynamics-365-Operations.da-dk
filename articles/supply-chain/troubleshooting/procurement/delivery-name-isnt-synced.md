---
title: Leveringsnavnet synkroniseres ikke efter ændring af en leveringsadresse for en indkøbsordre
description: Efter at du har ændret leveringsadressen på et indkøbsordrehoved, synkroniseres leveringsnavnet ikke
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
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475872"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Leveringsnavnet synkroniseres ikke efter ændring af en leveringsadresse for en indkøbsordre

## <a name="symptoms"></a>Symptomer

Adressen på hovedet i en indkøbsordre opdateres til en adresse, der ikke er en leveringsadresse. Selvom adressen opdateres på indkøbsordren, opdateres leveringsnavnet ikke på basis af den opdaterede adresse.

## <a name="resolution"></a>Løsning

Denne funktionsmåde er tilsigtet. Den valgte adresse skal klassificeres som en leveringsadresse. Ellers opdateres leveringsnavnet ikke på basis af den valgte adresse.
