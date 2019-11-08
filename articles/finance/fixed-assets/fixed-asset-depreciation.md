---
title: Afskrivning af anlægsaktiv
description: Dette emne indeholder en oversigt over afskrivning af anlægsaktiver.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1056dadab4294072cc064670f5cfcda239e22e19
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176960"
---
# <a name="fixed-asset-depreciation"></a>Afskrivning af anlægsaktiv

[!include [banner](../includes/banner.md)]

Dette emne indeholder en oversigt over afskrivning af anlægsaktiver.

Afskrivning er en periodisk transaktion, der normalt reducerer anlægsaktivets værdi i balancen og faktureres som en udgift på driftskontoen (resultatopgørelsen). Derfor bruges en hovedkonto normalt til kreditering af den periodiske afskrivning i balancen. En modkonto er en konto på driftskontodelen af kontoplanen.

## <a name="depreciation-adjustment"></a>Afskrivningsregulering
Normalt er det kun en regulering af en allerede bogført afskrivningspostering, der bogføres som en afskrivningsjustering. Derfor er både hovedkontoen og modkontoen konfigureret som konti til afskrivning. En afskrivningsregulering kan være et positivt eller negativt beløb, men funktionen af hovedkontoen (som en statuskonto) og funktionen af modkontoen (normalt som en driftskonto) forbliver den samme.

## <a name="extraordinary-depreciation"></a>Ekstraordinær afskrivning
Ekstraordinær afskrivning fungerer ligesom grundlæggende afskrivning. Derfor bruges en hovedkonto til kreditering af afskrivningsbeløbet på balancen og reducering af værdien af anlægsaktivet. En modkonto er en driftskonto, hvor den afskrivning, der beregnes for regnskabsperioden, opkræves som en udgift. 

Ekstraordinær afskrivning fungerer uafhængigt af grundlæggende afskrivning. Fordi ekstraordinær afskrivning er en separat posteringstype, kan du bogføre og rapportere ekstraordinær afskrivning separat fra den grundlæggende afskrivning.

## <a name="special-depreciation-allowance"></a>Særlig afskrivning
Du kan bruge særlig afskrivning til ekstraafskrivningsbeløb det første år, hvor et anlægsaktiv tages i anvendelse og afskrives. Særlig afskrivning skal foretages før eventuelle andre afskrivningsberegninger. Da særlige afskrivninger ofte er ukendt indtil senere i den samlede levetid for anlægsaktivet, er det bedst at bruge denne type afskrivning med en bog, der ikke bogføres i finansmodulet. Du kan bruge indstillingen Slet transaktioner, der ikke er bogført i Finans til at slette transaktionshistorikken for disse bøger. Du kan derefter slette afskrivningshistorikken for anlægsaktivets bog, bogføre den særlige afskrivning, når den er kendt, og derefter bogføre de resterende afskrivningsposteringer for året. 

Du kan oprette et ubegrænset antal poster for særlig afskrivning. Når du har tildelt aktivgruppebogen disse poster, anvendes de i aktivbogen. 

Særlig afskrivning angives som enten en procentsats eller et fast beløb. Når du bogfører afskrivningsforslag, bogføres posteringerne for særlig afskrivning i bogen som posteringer, der er adskilt fra afskrivningsposteringer.

## <a name="depreciation-calendars"></a>Afskrivningskalendere
Hver bog har en kalender, der bruges ved afskrivning af anlægsaktiver. Hvis du ikke angiver en kalender på bogen, bruger bogen som standard finansregnskabskalenderen. Du skal vælge en regnskabskalender til en bog, når den afskrivningsprofil, der er knyttet til bogen, bruger et regnskabsmæssigt afskrivningsår. 

Du kan oprette delte kalendere ved hjælp af siden **Regnskabskalendere** i Finans.

Du kan finde flere oplysninger under [Afskrivningsmetoder og -principper](depreciation-methods-conventions.md).


