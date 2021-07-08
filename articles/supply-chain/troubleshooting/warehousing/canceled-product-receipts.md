---
title: Transaktionsstatussen for annullerede produktkvitteringer opdateres ikke til Registreret
description: Når du har annulleret produktkvitteringerne ved en indgående last, opdaterer systemet automatisk lagertransaktionens status fra Modtaget til Bestilt.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294036"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Transaktionsstatussen for annullerede produktkvitteringer opdateres ikke til Registreret

## <a name="symptoms"></a>Symptomer

Når du har kørt handlingen **Annuller produktkvitteringer** ved en indgående last, opdaterer systemet automatisk lagertransaktionens status fra *Modtaget* til *Bestilt*.

## <a name="resolution"></a>Løsning

Når følgesedler annulleres ved udgående laster, forbliver statussen for lagertransaktioner *Plukket*. Men når produktkvitteringer fra en indgående last annulleres, gendannes statussen for lagertransaktioner ikke til *Registreret*. Når en produktkvittering fra en indgående last annulleres, skal lagerarbejderen derfor registrere vareantal for lasten igen.

Du kan finde flere oplysninger i [Registrere vareantal, der ankommer ved en indgående last](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
