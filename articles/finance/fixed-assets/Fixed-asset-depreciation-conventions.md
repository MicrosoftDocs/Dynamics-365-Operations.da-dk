---
title: Principper for afskrivning af anlægsaktiver
description: Dette emne indeholder en oversigt over principperne for afskrivning af anlægsaktiver.
author: saraschi2
manager: AnnBe
ms.date: 03/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad44282de9d999aa211548601eb416f4bdba2047
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176963"
---
# <a name="fixed-asset-depreciation-conventions"></a>Principper for afskrivning af anlægsaktiver

[!include [banner](../includes/banner.md)]

Afskrivningsprincipper bruges til at bestemme, hvornår og hvordan afskrivningen beregnes både for det år, hvor anlægsaktivet er anskaffet, og det år, hvor anlægsaktivet er solgt/kasseret.

Afskrivningsprincipper kan tildeles opsætningen af en bog for anlægsaktivgrupper. Vælg gruppen **Anlægsaktiv** i opsætningsområdet for anlægsaktiver for at gennemse eller tildele afskrivningsprincippet. Vælg knappen **Bøger**. I så fald bruges de afskrivningsprincipper, der er tildelt som standardværdier, da bøgerne for anlægsaktiver blev oprettet. Afskrivningsprincipper kan også angives for en enkelt anlægsaktivbog. For at gøre dette skal du vælge **Bøger** i opsætningsområdet for anlægsaktiver og dernæst vælge knappen **Anlægsaktivgrupper**.


|  Afskrivningsprincip  |   Beskrivelse  |
|---------------------------|-----------------|
|           Ingen            |  Aktivers afskrivning begynder på den angivne <strong>Ibrugtagningsdato</strong>.|
|         Halvår         |  Fratræk et halvt års afskrivninger for både det første år og det sidste år, hvor ejendommen afskrives. Fratræk et helt års afskrivninger for alle andre år i afskrivningsperioden. |
|        Hel måned         | Aktiver med en <strong>Ibrugtagningsdato</strong>, der optræder på ethvert tidspunkt i måneden, afskrives på den første dag i den pågældende måned. Aktiver, der er udgået på ethvert tidspunkt i måneden, betragtes som trukket tilbage i forhold til afskrivningen på den sidste dag i den foregående måned.  |
|        Midt i kvartal        | For at beregne dine afskrivningsfradrag for det år, hvor du tager ejendommen i brug, ganges afskrivningen for et helt år med procenten for det kvartal, hvor ejendommen er taget i brug, som vist i følgende tabel.<table><thead><tr><th>Kvartal</th><th>Procent</th></tr></thead><tbody><tr><td>Første</td><td>87,5</td></tr><tr><td>Anden</td><td>62,5</td></tr><tr><td>Tredje</td><td>37,5</td></tr><tr><td>Fjerde</td><td>12,5</td></tr></tbody></table>Et halv kvartals afskrivning bogføres i kvartalet for kassation/salg (eller det kvartal, hvor ejendommen er fuldt afskrevet). |
| Midt i måned (d. 1. i måneden)  | Aktiver, der har en <strong>Ibrugtagningsdato</strong> i første halvdel af måneden (dag 1 til 15), afskrives fra den første dag i måneden i måneden for den angivne <strong>Ibrugtagningsdato</strong>. Aktiver, der har en <strong>Ibrugtagningsdato</strong> i anden halvdel af måneden (dag 16 til månedens afslutning), afskrives fra den første dag i måneden efter den angivne <strong>Ibrugtagningsdato</strong>. Aktiver, der er trukket tilbage i den første halvdel af måneden (dag 1 til 15), betragtes som trukket tilbage i forhold til afskrivningen på den sidste dag i den foregående måned. Aktiver, der er trukket tilbage i den anden halvdel af måneden (dag 16 til månedens afslutning), betragtes som trukket tilbage i forhold til afskrivningen på den sidste dag i måneden for tilbagetrækningen. |
| Midt i måned (d. 15. i måneden) |  For at beregne afskrivningsfradraget for det år, hvor du tager ejendommen i brug, skal du gange afskrivningen for et helt år med en brøk. Tælleren (øverste tal) i denne brøk er antallet hele måneder i det år, hvor ejendommen er taget i brug, plus 1/2 eller (0,5). Nævneren (nederste tal) er 12. Hvis du sælger/kasserer ejendommen inden udgangen af afskrivningsperioden, kan du bruge samme metode til at beregne afskrivningsfradraget for året for salget/kassationen.   |
| Halvår (årsstart) | Aktiver, der har en <strong>Ibrugtagningsdato</strong> i første halvdel af året, afskrives på den første dag i året (hele året). Aktiver, der har en <strong>Ibrugtagningsdato</strong> i anden halvdel af året, afskrives midt på året.|
|   Halvår (næste år)   |   Aktiver, der har en <strong>Ibrugtagningsdato</strong> i første halvdel af året, afskrives på den første dag i året (hele året). Aktiver, der har en <strong>Ibrugtagningsdato</strong> i anden halvdel af året, afskrives på den første dag i det efterfølgende år. Aktiver, der er trukket tilbage i den første halvdel af året, betragtes som trukket tilbage i forhold til afskrivningen på den sidste dag i det foregående år. Enhver afskrivning, der bogføres i det indeværende år, skal tilbageføres eller justeres. Aktiver, der er trukket tilbage i den anden halvdel af året, betragtes trukket tilbage i forhold til afskrivningen på den sidste dag i året for tilbagetrækningen.|
