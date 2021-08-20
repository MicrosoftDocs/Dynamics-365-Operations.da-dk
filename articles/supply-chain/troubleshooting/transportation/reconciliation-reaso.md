---
title: Du kan kun tilføje hovedkontoen som kreditkontoen af afstemningsmæssige årsager
description: Når du konfigurerer en afstemningsårsag i Transportstyring, kan du kun tilføje hovedkontoen som kreditkonto.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750876"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Du kan kun tilføje hovedkontoen som kreditkontoen af afstemningsmæssige årsager

KB-nummer: 4603538

## <a name="symptoms"></a>Symptomer

Når du konfigurerer en afstemningsårsag i Transportstyring, kan du kun tilføje hovedkontoen som kreditkonto. Du kan ikke tilføje en bærer eller en anden dimension som kreditkonto. Debetkontoen giver dig dog mulighed for at vælge andre dimensioner.

## <a name="resolution"></a>Løsning

Hvis afstemningen ikke sker for at betale kreditoren, men for at kreditere en bestemt hovedkonto, giver systemet dig ikke mulighed for at vælge en økonomisk dimension til kreditkontoen, når du konfigurerer afstemningsårsagen.

Hvis kontostrukturen kræver en bestemt økonomisk dimensionsværdi for kredithovedkontoen, kan den kreditorkladde, der oprettes som resultat, ikke bogføres automatisk, fordi den økonomiske dimensionsværdi mangler. Derfor skal du først angive kreditkontoen manuelt ved hjælp af siden **Fakturakladde**.

Da der kræves en dimensionsværdi for kreditkontoen, kan kreditorfakturakladden ikke bogføres automatisk. Du skal bogføre den manuelt, når du manuelt har føjet dimensionsværdien til hovedkontoen for kreditlinjen.
