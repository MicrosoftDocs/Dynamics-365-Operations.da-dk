---
title: Oprette leasingkladdenavne
description: Dette emne forklarer, hvordan du kan definere navne på leasingkladder. Navne på leasekladder angiver de kladder, som poster, der stammer fra aktivleasing, bogføres på.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880880"
---
# <a name="set-up-lease-journal-names"></a>Oprette leasingkladdenavne

[!include [banner](../includes/banner.md)]

Navne på leasingkladder angiver de kladder, som transaktioner fra aktivleasing, bogføres på. Kun de kladdenavne, der er tildelt **Aktivleasing** kladdetypen, vises i felterne **Oprindelig genkendelse** og **Månedlig kladdenavn** på siden **Parametre til aktivleasing**. Kun kladdetypen **Kreditorfakturaregistrering** kan tildeles til feltet **Fakturakladdenavn**.

Benyt følgende fremgangsmåde for at konfigurere leasingkladdenavne.

1. Gå til **Aktivleasing \> Opsætning \> Parametre til aktivleasing**.
2. Under fanen **Generelt** i feltet **Første genkendelseskladdenavn** og vælg en kladde. Alle posteringer i den første genkendelseskladde bogføres på dette kladdenavn.
3. Vælg en kladde i feltet **Fakturakladdenavn**. Hvis indstillingen **Betal til kreditor** er angivet til **Ja** for leasingkartoteket, vil leasing- og udgiftsbetalingsfakturaer blive bogført på dette kladdenavn.
4. Vælg en kladde i feltet **Leasingkladdenavn**. Alle poster for afskrivning, renter og kortfristede omposteringer bogføres på dette kladdenavn. Hvis indstillingen **Betal til kreditor** er angivet til **Nej** for leasingkartoteket, vil leasing- og udgiftsbetalingsbetalinger også blive bogført på dette kladdenavn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
