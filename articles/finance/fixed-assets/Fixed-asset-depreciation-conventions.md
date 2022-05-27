---
title: Principper for afskrivning af anlægsaktiver
description: Dette emne beskriver principperne for afskrivning af anlægsaktiver.
author: moaamer
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e151d20fbfb9aa8fca9afc5be4f112b3de13cc7
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719799"
---
# <a name="fixed-asset-depreciation-conventions"></a>Principper for afskrivning af anlægsaktiver

[!include [banner](../includes/banner.md)]

Dette emne beskriver principperne for afskrivning af anlægsaktiver. Afskrivningsprincipper bruges til at bestemme, hvornår og hvordan afskrivningen beregnes både for det år, hvor anlægsaktivet er anskaffet, og det år, hvor anlægsaktivet er solgt/kasseret.

Afskrivningsprincipper kan tildeles opsætningen af en bog for anlægsaktivgrupper. Vælg gruppen **Anlægsaktiv** i opsætningsområdet for anlægsaktiver for at gennemse eller tildele afskrivningsprincippet. Vælg knappen **Bøger**. I så fald bruges de afskrivningsprincipper, der er tildelt som standardværdier, da bøgerne for anlægsaktiver blev oprettet. Afskrivningsprincipper kan også angives for en enkelt anlægsaktivbog. For at gøre dette skal du vælge **Bøger** i opsætningsområdet for anlægsaktiver og dernæst vælge knappen **Anlægsaktivgrupper**.

| Afskrivningsprincip   | Beskrivelse |
|---------------------------|-------------|
| Ingen                      | Aktivers afskrivning begynder på den angivne <strong>Ibrugtagningsdato</strong>. |
| Halvår                 | Du kan fratrække et halvt års afskrivning både for det første år og det sidste år, hvor ejendommen afskrives. Du kan fratrække et helt års afskrivning for alle andre år i afskrivningsperioden. |
| Hel måned                | Aktiver med en <strong>Ibrugtagningsdato</strong>, der optræder på ethvert tidspunkt i måneden, afskrives på den første dag i den pågældende måned. Til afskrivningsformål betragtes aktiver som afviklet den sidste dag i den forrige måned. Den specifikke dag i måneden, hvor de blev afviklet, tages ikke i betragtning. |
| Midt i kvartal               | For at beregne dine afskrivningsfradrag for det år, hvor du tager ejendommen i brug, ganges afskrivningen for et helt år med procenten for det kvartal, hvor ejendommen er taget i brug, som vist i følgende tabel.<table><thead><tr><th>Kvartal</th><th>Procent</th></tr></thead><tbody><tr><td>Første</td><td>87,5</td></tr><tr><td>Anden</td><td>62,5</td></tr><tr><td>Tredje</td><td>37,5</td></tr><tr><td>Fjerde</td><td>12.5</td></tr></tbody></table>Et halvt kvartals afskrivning bogføres i kvartalet, hvor aktivet blev kasseret (eller det kvartal, hvor det er fuldt afskrevet). |
| Midt i måned (d. 1. i måneden)  | Aktiver, der har en <strong>Ibrugtagningsdato</strong> i første halvdel af måneden (dag 1 til 15), afskrives fra den første dag i måneden i måneden for den angivne <strong>Ibrugtagningsdato</strong>. Aktiver, der har en <strong>Ibrugtagningsdato</strong> i anden halvdel af måneden (dag 16 til månedens afslutning), afskrives fra den første dag i måneden efter den angivne <strong>Ibrugtagningsdato</strong>. Aktiver, der er afviklet i den første halvdel af måneden (dag 1 til 15), betragtes som afviklet i forhold til afskrivningen på den sidste dag i den foregående måned. Aktiver, der er afviklet i den anden halvdel af måneden (dag 16 til månedens afslutning), betragtes som afviklet i forhold til afskrivningen på den sidste dag i afviklingsmåneden. |
| Midt i måned (d. 15. i måneden) | For at beregne afskrivningsfradraget for det år, hvor du tager ejendommen i brug, skal du gange afskrivningen for et helt år med en brøk. Tælleren (øverste tal) i denne brøk er antallet hele måneder i det år, hvor ejendommen er taget i brug, plus 1/2 eller (0,5). Nævneren (nederste tal) er 12. Hvis du sælger/kasserer ejendommen inden udgangen af afskrivningsperioden, kan du bruge samme metode til at beregne afskrivningsfradraget for året for salget/kassationen. |
| Halvår (årsstart) | Aktiver, der har en <strong>Ibrugtagningsdato</strong> i første halvdel af året, afskrives på den første dag i året (hele året). Aktiver, der har en <strong>Ibrugtagningsdato</strong> i anden halvdel af året, afskrives midt på året. |
| Halvår (næste år)     | Aktiver, der har en <strong>Ibrugtagningsdato</strong> i første halvdel af året, afskrives på den første dag i året (hele året). Aktiver, der har en <strong>Ibrugtagningsdato</strong> i anden halvdel af året, afskrives på den første dag i det efterfølgende år. Aktiver, der er afviklet i den første halvdel af året, betragtes som afviklet i forhold til afskrivningen på den sidste dag i det foregående år. Enhver afskrivning, der bogføres i det indeværende år, skal tilbageføres eller justeres. Aktiver, der er afviklet i den anden halvdel af året, betragtes afviklet i forhold til afskrivningen på den sidste dag i året for afviklingen. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
