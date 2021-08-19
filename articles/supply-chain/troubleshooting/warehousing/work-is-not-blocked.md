---
title: Arbejde er ikke blokeret
description: Arbejde er ikke blokeret
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719545"
---
# <a name="work-isnt-blocked"></a>Arbejde er ikke blokeret

Fejlkode: WSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Arbejde med id'et %1 er ikke blokeret.

## <a name="cause"></a>Årsag

Indstillingen **Blokeret bølge** for bølgen er angivet til *Nej*. Blokering af arbejdet kan ikke fjernes, da arbejdet ikke er blokeret i øjeblikket.

## <a name="resolution"></a>Løsning

 Det er kun arbejde, hvor indstillingen **Blokeret bølge** er angivet til *Ja*, hvor blokering kan fjernes.
