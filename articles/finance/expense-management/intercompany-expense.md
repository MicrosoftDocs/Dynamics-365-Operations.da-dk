---
title: Interne udgifter
description: En medarbejder, der er ansat af en juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation. I denne situation kan du bruge funktionaliteten til interne udgifter til at tildele medarbejderens udgifter til den juridiske enhed, som arbejdet blev udført for.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390878"
---
# <a name="intercompany-expenses"></a>Interne udgifter

[!include [banner](../includes/banner.md)]

En medarbejder, der er ansat af en juridisk enhed i en organisation, kan udføre arbejde for en anden juridisk enhed i den samme organisation. I denne situation kan du bruge funktionaliteten til interne udgifter til at tildele medarbejderens udgifter til den juridiske enhed, som arbejdet blev udført for. Den juridiske enhed, der ansætter medarbejderen, kaldes den juridiske udlånsenhed. Den juridiske enhed, som medarbejderen har udgifter for, kaldes den juridiske låneenhed. 

Før en arbejder kan oprette og sende udgifter for arbejde, der udføres for en anden juridisk enhed i den juridiske udlånsenhed, skal du på siden **Parametre for udgiftsstyring** vælge indstillingen **Tillad interne udgiftslinjer**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Skattepostering for interne udgifter

[!include [banner](../includes/banner.md)]

Hvis du vil bruge momsgrupper, der er knyttet til den juridiske enhed for udlånet (kilden) i stedet for den juridiske enhed for lånet (destinationen) i udgiftsrapporten, skal du konfigurere den under momskonfigurationen i Finans. Hvis Finans-parameteren **Juridisk enhed for bogføring af intern skat** er angivet til **Kilde**, og **Anvend momsregler** er angivet til **Nej**, vil momskombinationen for den juridiske enhed for udlån blive brugt. Når den samme parameter er angivet til **Destination**, vil momskombinationen for den juridisk enhed for lån blive anvendt. Når det gælder juridiske enheder i USA, hvor parameteren er indstillet til **Kilde**, skal feltet **Indgående moms** også konfigureres på den nye side **Finanskonteringsgrupper**. Regnskabsprogrammet bruger oplysningerne fra dette felt til momsrelateret regnskabspost.   
Funktionaliteten stemmer ikke overens med de udgiftslinjer, der er bogført med eller uden et projekt.  
