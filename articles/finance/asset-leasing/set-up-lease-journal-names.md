---
title: Oprette leasingkladdenavne
description: Dette emne forklarer, hvordan du kan definere navne på leasingkladder. Navne på leasekladder angiver de kladder, som poster, der stammer fra aktivleasing, bogføres på.
author: moaamer
ms.date: 12/03/2021
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
ms.openlocfilehash: b9d8136ae4f960a586b9526751fc8bf6e7675c8d
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890744"
---
# <a name="set-up-lease-journal-names"></a>Oprette leasingkladdenavne

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Navne på leasingkladder angiver de kladder, som transaktioner fra aktivleasing, bogføres på. Kun de kladdenavne, der er tildelt **Aktivleasing** kladdetypen, vises i felterne **Oprindelig genkendelse** og **Månedlig kladdenavn** på siden **Parametre til aktivleasing**. Kun kladdetypen **Kreditorfakturaregistrering** kan tildeles til feltet **Fakturakladdenavn**.

Systemet låser visse økonomifelter mod at blive redigeret for at forhindre afvigelser mellem transaktionerne og planerne. Nogle af felterne, der er låst, omfatter: **Konto**, **Beløb**, **Økonomiske dimensioner**, **Valuta** og **Posteringstype**. Derudover kan du ikke tilføje eller slette kladdeposteringslinjer i nogen kladdeposteringer for aktivleasing, da dette kan medføre afvigelser mellem tidsplanerne og transaktionerne.


Benyt følgende fremgangsmåde for at konfigurere leasingkladdenavne.

1. Gå til **Aktivleasing \> Opsætning \> Parametre til aktivleasing**.
2. Under fanen **Generelt** i feltet **Første genkendelseskladdenavn** og vælg en kladde. Alle posteringer i den første genkendelseskladde bogføres på dette kladdenavn.
3. Vælg en kladde i feltet **Fakturakladdenavn**. Hvis indstillingen **Betal til kreditor** er angivet til **Ja** for leasingkartoteket, vil leasing- og udgiftsbetalingsfakturaer blive bogført på dette kladdenavn.
4. Vælg en kladde i feltet **Leasingkladdenavn**. Alle poster for afskrivning, renter og kortfristede omposteringer bogføres på dette kladdenavn. Hvis indstillingen **Betal til kreditor** er angivet til **Nej** for leasingkartoteket, vil leasing- og udgiftsbetalingsbetalinger også blive bogført på dette kladdenavn.
5. Vælg en kladde i feltet **Kladdenavn på leasingændringer**. Posteringer for leasingreguleringer, afslutning og værdiforringelse bogføres på dette kladdenavn. Det kladdenavn, du vælger, må ikke have en tilknyttet arbejdsgang eller godkendelse. Hvis kladdenavnet for leasingændringen ikke er defineret, bogføres transaktionerne for leasingregulering, afslutning og værdiforringelse til det kladdenavn, der er valgt i feltet **Leasingkladdenavn**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
