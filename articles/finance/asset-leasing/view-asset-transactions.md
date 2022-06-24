---
title: Få vist forpligtelses-, aktiv- og udgiftstransaktioner
description: Denne artikel forklarer, hvordan du får vist posteringer for et leaset aktiv. Disse posteringer omfatter leasede passivposteringer og faste posteringer, der er bogført.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 552b5a6044950c4dd7547a5239c1b3f7d355dbce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906407"
---
# <a name="view-liability-asset-and-expense-transactions"></a>Få vist forpligtelses-, aktiv- og udgiftstransaktioner

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du får vist posteringer for et leaset aktiv. Disse posteringer omfatter leasede passivposteringer og faste posteringer, der er bogført. De opbrugte værdier for passiv- og ROUs-aktiverne bruges i flere rapporter. De bruges også til at beregne reguleringsværdier.

## <a name="liability-transactions"></a>Forpligtelsestransaktioner

Hvis du vil have vist leasede passivposteringer, skal du vælge en leasingaftale på siden **Leasingoversigt** og derefter vælge **Kartoteker** for at åbne de kartoteker, der er tilknyttet leasingposten. Når der er bogført en første godkendelse, en faktura eller en rentekladde, skal du vælge **Ansvarsposteringer**.

På siden **Ansvarsposteringer** vises de transaktioner, der enten øger eller reducerer leasingforpligtelsen. Negative beløb på denne side repræsenterer kreditposteringer i standardapplikationen. Renteperiodiseringer vises som negative værdier og øger den samlede leasingforpligtelse. Eventuelle leasingreguleringer vises som positive eller negative værdier, afhængigt af arten og virkningen af leasingkartoteket. Den aktuelle nettosaldo for leasingforpligtelse for den valgte leasingaftale vises nederst til venstre på siden.

## <a name="asset-transactions"></a>Aktivtransaktioner

Hvis du vil have vist aktivposteringer for leasingen, skal du vælge en leasingaftale på siden **Leasingoversigt** og derefter vælge **Kartoteker** for at åbne de leasingkartoteker, der er tilknyttet leasingposten. Vælg derefter **Aktivtransaktioner**.

På siden **Aktivposter** vises de transaktioner, der enten øger eller reducerer aktivets anlægsaktiv og de akkumulerede afskrivningskonti. Debiteringer vises som positive værdier, og krediteringer vises som negative værdier som på siden **Ansvarsposteringer**. Den bogførte første genkendelse og den næste af den akkumulerede afskrivning vises nederst til venstre på siden som aktivsaldo. 

## <a name="expenses-transactions"></a>Udgiftsposteringer

Hvis du vil have vist udgiftsposteringer for leasingen, skal du vælge en leasingaftale på siden **Leasingoversigt** og derefter vælge **Kartoteker** for at åbne de leasingkartoteker, der er tilknyttet leasingposten. Vælg derefter **Udgiftsposteringer**.

På siden **Udgiftsposteringer** vises alle de udgifter, der er bogført i forhold til leasingaftalen, f. eks. renteudgifter, afskrivningsudgifter og eventuelle afviklede omkostninger.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
